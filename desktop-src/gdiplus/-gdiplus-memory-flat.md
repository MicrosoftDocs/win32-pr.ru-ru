---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Функции памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e748f8a68cc6f04deba3c9676638ee48ee2e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985153"
---
# <a name="memory-functions"></a><span data-ttu-id="1732e-103">Функции памяти</span><span class="sxs-lookup"><span data-stu-id="1732e-103">Memory Functions</span></span>

<span data-ttu-id="1732e-104">Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.</span><span class="sxs-lookup"><span data-stu-id="1732e-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="1732e-105">Функции в плоском API-интерфейсе GDI+ упаковываются в коллекцию из примерно 40 классов C++.</span><span class="sxs-lookup"><span data-stu-id="1732e-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="1732e-106">Не рекомендуется напрямую вызывать функции в плоском API.</span><span class="sxs-lookup"><span data-stu-id="1732e-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="1732e-107">При каждом вызове GDI+ это следует делать путем вызова методов и функций, предоставляемых оболочками C++.</span><span class="sxs-lookup"><span data-stu-id="1732e-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="1732e-108">Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API.</span><span class="sxs-lookup"><span data-stu-id="1732e-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="1732e-109">Дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="1732e-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="1732e-110">Следующие плоские функции API упаковываются классом C++ [**гдиплусбасе**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) .</span><span class="sxs-lookup"><span data-stu-id="1732e-110">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="1732e-111">Функции памяти и соответствующие методы-оболочки</span><span class="sxs-lookup"><span data-stu-id="1732e-111">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="1732e-112">Плоская функция</span><span class="sxs-lookup"><span data-stu-id="1732e-112">Flat function</span></span>                                          | <span data-ttu-id="1732e-113">Метод-оболочка</span><span class="sxs-lookup"><span data-stu-id="1732e-113">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="1732e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1732e-114">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1732e-115">Гпстатус ВИНГДИПАПИ Гдипаллок (размер \_ t)</span><span class="sxs-lookup"><span data-stu-id="1732e-115">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="1732e-116">**Гпстатус ВИНГДИПАПИ Гдиплусбасе void \* (оператор New) (размер \_ t в \_ размере)**</span><span class="sxs-lookup"><span data-stu-id="1732e-116">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="1732e-117">Выделяет память для одного объекта Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="1732e-117">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="1732e-118">Гдипаллок объявляется в Гдиплусмем. h.</span><span class="sxs-lookup"><span data-stu-id="1732e-118">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="1732e-119">Гпстатус ВИНГДИПАПИ Гдипфри (void \* PTR);</span><span class="sxs-lookup"><span data-stu-id="1732e-119">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="1732e-120">**Гпстатус ВИНГДИПАПИ Гдиплусбасе void (оператор DELETE) (void \* в \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="1732e-120">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="1732e-121">Освобождает память для одного объекта Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="1732e-121">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="1732e-122">Гдипфри объявляется в Гдиплусмем. h.</span><span class="sxs-lookup"><span data-stu-id="1732e-122">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
