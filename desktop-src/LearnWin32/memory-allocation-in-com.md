---
title: Выделение памяти в COM
description: .
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62227f78287f184b019eee3e498ec8a25f25a03c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681612"
---
# <a name="memory-allocation-in-com"></a><span data-ttu-id="b5fdf-103">Выделение памяти в COM</span><span class="sxs-lookup"><span data-stu-id="b5fdf-103">Memory Allocation in COM</span></span>

<span data-ttu-id="b5fdf-104">Иногда метод выделяет буфер памяти в куче и возвращает адрес буфера вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-104">Sometimes a method allocates a memory buffer on the heap and returns the address of the buffer to the caller.</span></span> <span data-ttu-id="b5fdf-105">COM определяет пару функций для выделения и освобождения памяти в куче.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-105">COM defines a pair of functions for allocating and freeing memory on the heap.</span></span>

-   <span data-ttu-id="b5fdf-106">Функция [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) выделяет блок памяти.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-106">The [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) function allocates a block of memory.</span></span>
-   <span data-ttu-id="b5fdf-107">Функция [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) освобождает блок памяти, выделенный с помощью функции [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span><span class="sxs-lookup"><span data-stu-id="b5fdf-107">The [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function frees a block of memory that was allocated with [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc).</span></span>

<span data-ttu-id="b5fdf-108">Мы видели пример этого шаблона в [примере открытия диалогового окна](example--the-open-dialog-box.md):</span><span class="sxs-lookup"><span data-stu-id="b5fdf-108">We saw an example of this pattern in the [Open dialog box example](example--the-open-dialog-box.md):</span></span>


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



<span data-ttu-id="b5fdf-109">Метод " [**DisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) " выделяет память для строки.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-109">The [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) method allocates memory for a string.</span></span> <span data-ttu-id="b5fdf-110">На внутреннем уровне метод вызывает функцию [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) для выделения строки.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-110">Internally, the method calls [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) to allocate the string.</span></span> <span data-ttu-id="b5fdf-111">Когда метод возвращает значение, *псзфилепас* указывает на расположение памяти нового буфера.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-111">When the method returns, *pszFilePath* points to the memory location of the new buffer.</span></span> <span data-ttu-id="b5fdf-112">Вызывающий объект отвечает за вызов [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-112">The caller is responsible for calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory.</span></span>

<span data-ttu-id="b5fdf-113">Почему COM определяет собственные функции выделения памяти?</span><span class="sxs-lookup"><span data-stu-id="b5fdf-113">Why does COM define its own memory allocation functions?</span></span> <span data-ttu-id="b5fdf-114">Одна из причин — предоставить уровень абстракции для распределителя кучи.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-114">One reason is to provide an abstraction layer over the heap allocator.</span></span> <span data-ttu-id="b5fdf-115">В противном случае некоторые методы могут вызывать функцию **malloc** , а другие — как **New**.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-115">Otherwise, some methods might call **malloc** while others called **new**.</span></span> <span data-ttu-id="b5fdf-116">В некоторых случаях программе потребуется вызвать **бесплатную** функцию, а затем **Удалить** ее в других, а также быстро стать невозможной.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-116">Then your program would need to call **free** in some cases and **delete** in others, and keeping track of it all would quickly become impossible.</span></span> <span data-ttu-id="b5fdf-117">Функции выделения COM создают единообразный подход.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-117">The COM allocation functions create a uniform approach.</span></span>

<span data-ttu-id="b5fdf-118">Еще один вопрос заключается в том, что COM является *двоичным* стандартом, поэтому он не привязан к конкретному языку программирования.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-118">Another consideration is the fact that COM is a *binary* standard, so it is not tied to a particular programming language.</span></span> <span data-ttu-id="b5fdf-119">Таким образом, COM не может полагаться на любые специфические для конкретного языка формы выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="b5fdf-119">Therefore, COM cannot rely on any language-specific form of memory allocation.</span></span>

## <a name="next"></a><span data-ttu-id="b5fdf-120">Следующая</span><span class="sxs-lookup"><span data-stu-id="b5fdf-120">Next</span></span>

[<span data-ttu-id="b5fdf-121">Методики программирования COM</span><span class="sxs-lookup"><span data-stu-id="b5fdf-121">COM Coding Practices</span></span>](com-coding-practices.md)

 

 