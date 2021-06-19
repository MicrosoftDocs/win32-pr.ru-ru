---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций. Эти плоские функции API упаковываются с помощью класса Brush C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Функции Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395089"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="63df1-104">Функции Brush (GDI+)</span><span class="sxs-lookup"><span data-stu-id="63df1-104">Brush Functions (GDI+)</span></span>

<span data-ttu-id="63df1-105">Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.</span><span class="sxs-lookup"><span data-stu-id="63df1-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="63df1-106">Функции в плоском API-интерфейсе GDI+ упаковываются в коллекцию из примерно 40 классов C++.</span><span class="sxs-lookup"><span data-stu-id="63df1-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="63df1-107">Не рекомендуется напрямую вызывать функции в плоском API.</span><span class="sxs-lookup"><span data-stu-id="63df1-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="63df1-108">При каждом вызове GDI+ это следует делать путем вызова методов и функций, предоставляемых оболочками C++.</span><span class="sxs-lookup"><span data-stu-id="63df1-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="63df1-109">Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API.</span><span class="sxs-lookup"><span data-stu-id="63df1-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="63df1-110">Дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="63df1-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="63df1-111">Следующие плоские функции API упаковываются с помощью класса [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.</span><span class="sxs-lookup"><span data-stu-id="63df1-111">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="63df1-112">Функции-кисти и соответствующие методы-оболочки</span><span class="sxs-lookup"><span data-stu-id="63df1-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="63df1-113">Плоская функция</span><span class="sxs-lookup"><span data-stu-id="63df1-113">Flat function</span></span>                                                                        | <span data-ttu-id="63df1-114">Метод-оболочка</span><span class="sxs-lookup"><span data-stu-id="63df1-114">Wrapper method</span></span>                                          | <span data-ttu-id="63df1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="63df1-115">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63df1-116">Гпстатус ВИНГДИПАПИ Гдипклонебруш ( \* кисть гпбруш, гпбруш \* \* клонебруш)</span><span class="sxs-lookup"><span data-stu-id="63df1-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="63df1-117">**Кисть:: Clone**</span><span class="sxs-lookup"><span data-stu-id="63df1-117">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="63df1-118">Метод [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) создает новый объект [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) на основе этой кисти.</span><span class="sxs-lookup"><span data-stu-id="63df1-118">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="63df1-119">Гпстатус ВИНГДИПАПИ Гдипделетебруш ( \* кисть гпбруш)</span><span class="sxs-lookup"><span data-stu-id="63df1-119">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="63df1-120">Виртуальная ~ Brush ()</span><span class="sxs-lookup"><span data-stu-id="63df1-120">virtual ~Brush()</span></span>                                        | <span data-ttu-id="63df1-121">Очищает ресурсы, используемые объектом [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="63df1-121">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="63df1-122">Гпстатус ВИНГДИПАПИ Гдипжетбруштипе ( \* кисть гпбруш, \* тип гпбруштипе)</span><span class="sxs-lookup"><span data-stu-id="63df1-122">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="63df1-123">**Brush:: GetType**</span><span class="sxs-lookup"><span data-stu-id="63df1-123">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="63df1-124">Метод [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) получает тип этой кисти.</span><span class="sxs-lookup"><span data-stu-id="63df1-124">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




