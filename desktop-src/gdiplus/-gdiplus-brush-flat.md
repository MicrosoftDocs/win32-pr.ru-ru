---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Функции Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345105"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="f5083-103">Функции Brush (GDI+)</span><span class="sxs-lookup"><span data-stu-id="f5083-103">Brush Functions (GDI+)</span></span>

<span data-ttu-id="f5083-104">Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.</span><span class="sxs-lookup"><span data-stu-id="f5083-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="f5083-105">Функции в плоском API-интерфейсе GDI+ упаковываются в коллекцию из примерно 40 классов C++.</span><span class="sxs-lookup"><span data-stu-id="f5083-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="f5083-106">Не рекомендуется напрямую вызывать функции в плоском API.</span><span class="sxs-lookup"><span data-stu-id="f5083-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="f5083-107">При каждом вызове GDI+ это следует делать путем вызова методов и функций, предоставляемых оболочками C++.</span><span class="sxs-lookup"><span data-stu-id="f5083-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="f5083-108">Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API.</span><span class="sxs-lookup"><span data-stu-id="f5083-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="f5083-109">Дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="f5083-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="f5083-110">Следующие плоские функции API упаковываются с помощью класса [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.</span><span class="sxs-lookup"><span data-stu-id="f5083-110">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="f5083-111">Функции-кисти и соответствующие методы-оболочки</span><span class="sxs-lookup"><span data-stu-id="f5083-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="f5083-112">Плоская функция</span><span class="sxs-lookup"><span data-stu-id="f5083-112">Flat function</span></span>                                                                        | <span data-ttu-id="f5083-113">Метод-оболочка</span><span class="sxs-lookup"><span data-stu-id="f5083-113">Wrapper method</span></span>                                          | <span data-ttu-id="f5083-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f5083-114">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5083-115">Гпстатус ВИНГДИПАПИ Гдипклонебруш ( \* кисть гпбруш, гпбруш \* \* клонебруш)</span><span class="sxs-lookup"><span data-stu-id="f5083-115">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="f5083-116">**Кисть:: Clone**</span><span class="sxs-lookup"><span data-stu-id="f5083-116">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="f5083-117">Метод [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) создает новый объект [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) на основе этой кисти.</span><span class="sxs-lookup"><span data-stu-id="f5083-117">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="f5083-118">Гпстатус ВИНГДИПАПИ Гдипделетебруш ( \* кисть гпбруш)</span><span class="sxs-lookup"><span data-stu-id="f5083-118">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="f5083-119">Виртуальная ~ Brush ()</span><span class="sxs-lookup"><span data-stu-id="f5083-119">virtual ~Brush()</span></span>                                        | <span data-ttu-id="f5083-120">Очищает ресурсы, используемые объектом [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="f5083-120">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="f5083-121">Гпстатус ВИНГДИПАПИ Гдипжетбруштипе ( \* кисть гпбруш, \* тип гпбруштипе)</span><span class="sxs-lookup"><span data-stu-id="f5083-121">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="f5083-122">**Brush:: GetType**</span><span class="sxs-lookup"><span data-stu-id="f5083-122">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="f5083-123">Метод [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) получает тип этой кисти.</span><span class="sxs-lookup"><span data-stu-id="f5083-123">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




