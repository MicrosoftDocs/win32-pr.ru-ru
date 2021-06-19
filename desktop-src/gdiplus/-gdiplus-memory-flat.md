---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций. Эти плоские функции API упаковываются классом C++ Гдиплусбасе.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Функции памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395829"
---
# <a name="memory-functions"></a><span data-ttu-id="c3a43-104">Функции памяти</span><span class="sxs-lookup"><span data-stu-id="c3a43-104">Memory Functions</span></span>

<span data-ttu-id="c3a43-105">Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.</span><span class="sxs-lookup"><span data-stu-id="c3a43-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="c3a43-106">Функции в плоском API-интерфейсе GDI+ упаковываются в коллекцию из примерно 40 классов C++.</span><span class="sxs-lookup"><span data-stu-id="c3a43-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="c3a43-107">Не рекомендуется напрямую вызывать функции в плоском API.</span><span class="sxs-lookup"><span data-stu-id="c3a43-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="c3a43-108">При каждом вызове GDI+ это следует делать путем вызова методов и функций, предоставляемых оболочками C++.</span><span class="sxs-lookup"><span data-stu-id="c3a43-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="c3a43-109">Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API.</span><span class="sxs-lookup"><span data-stu-id="c3a43-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="c3a43-110">Дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="c3a43-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="c3a43-111">Следующие плоские функции API упаковываются классом C++ [**гдиплусбасе**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) .</span><span class="sxs-lookup"><span data-stu-id="c3a43-111">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="c3a43-112">Функции памяти и соответствующие методы-оболочки</span><span class="sxs-lookup"><span data-stu-id="c3a43-112">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="c3a43-113">Плоская функция</span><span class="sxs-lookup"><span data-stu-id="c3a43-113">Flat function</span></span>                                          | <span data-ttu-id="c3a43-114">Метод-оболочка</span><span class="sxs-lookup"><span data-stu-id="c3a43-114">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="c3a43-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="c3a43-115">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a43-116">Гпстатус ВИНГДИПАПИ Гдипаллок (размер \_ t)</span><span class="sxs-lookup"><span data-stu-id="c3a43-116">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="c3a43-117">**Гпстатус ВИНГДИПАПИ Гдиплусбасе void \* (оператор New) (размер \_ t в \_ размере)**</span><span class="sxs-lookup"><span data-stu-id="c3a43-117">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="c3a43-118">Выделяет память для одного объекта Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="c3a43-118">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="c3a43-119">Гдипаллок объявляется в Гдиплусмем. h.</span><span class="sxs-lookup"><span data-stu-id="c3a43-119">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="c3a43-120">Гпстатус ВИНГДИПАПИ Гдипфри (void \* PTR);</span><span class="sxs-lookup"><span data-stu-id="c3a43-120">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="c3a43-121">**Гпстатус ВИНГДИПАПИ Гдиплусбасе void (оператор DELETE) (void \* в \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="c3a43-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="c3a43-122">Освобождает память для одного объекта Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="c3a43-122">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="c3a43-123">Гдипфри объявляется в Гдиплусмем. h.</span><span class="sxs-lookup"><span data-stu-id="c3a43-123">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
