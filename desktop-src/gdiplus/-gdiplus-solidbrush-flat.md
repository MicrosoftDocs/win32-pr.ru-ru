---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Функции SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984433"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="ed8d3-103">Функции SolidBrush</span><span class="sxs-lookup"><span data-stu-id="ed8d3-103">SolidBrush Functions</span></span>

<span data-ttu-id="ed8d3-104">Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h.</span><span class="sxs-lookup"><span data-stu-id="ed8d3-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="ed8d3-105">Функции в плоском API-интерфейсе GDI+ упаковываются в коллекцию из примерно 40 классов C++.</span><span class="sxs-lookup"><span data-stu-id="ed8d3-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="ed8d3-106">Не рекомендуется вызывать функции непосредственно в неструктурированном API.</span><span class="sxs-lookup"><span data-stu-id="ed8d3-106">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="ed8d3-107">При каждом вызове GDI+ рекомендуется сделать это, вызвав методы и функции, предоставляемые оболочками C++.</span><span class="sxs-lookup"><span data-stu-id="ed8d3-107">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="ed8d3-108">Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API.</span><span class="sxs-lookup"><span data-stu-id="ed8d3-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="ed8d3-109">Дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="ed8d3-109">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="ed8d3-110">Следующие плоские функции API упаковываются классом [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++.</span><span class="sxs-lookup"><span data-stu-id="ed8d3-110">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="ed8d3-111">Функции-кисти и соответствующие методы-оболочки</span><span class="sxs-lookup"><span data-stu-id="ed8d3-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="ed8d3-112">Плоская функция</span><span class="sxs-lookup"><span data-stu-id="ed8d3-112">Flat function</span></span>                                                                               | <span data-ttu-id="ed8d3-113">Метод-оболочка</span><span class="sxs-lookup"><span data-stu-id="ed8d3-113">Wrapper method</span></span>                                                                                       | <span data-ttu-id="ed8d3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed8d3-114">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8d3-115">**Гпстатус ВИНГДИПАПИ Гдипкреатесолидфилл (цвет ARGB, \* \* кисть гпсолидфилл)**</span><span class="sxs-lookup"><span data-stu-id="ed8d3-115">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="ed8d3-116">[**SolidBrush:: SolidBrush (в цветовой& константы)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="ed8d3-116">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="ed8d3-117">Создает объект [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) на основе цвета</span><span class="sxs-lookup"><span data-stu-id="ed8d3-117">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="ed8d3-118">**Гпстатус ВИНГДИПАПИ Гдипсетсолидфиллколор ( \* кисть гпсолидфилл, цвет ARGB)**</span><span class="sxs-lookup"><span data-stu-id="ed8d3-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="ed8d3-119">**SolidBrush:: Сетколор (в цветах констант& Color)**</span><span class="sxs-lookup"><span data-stu-id="ed8d3-119">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="ed8d3-120">Задает цвет сплошной кисти</span><span class="sxs-lookup"><span data-stu-id="ed8d3-120">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="ed8d3-121">**Гпстатус ВИНГДИПАПИ Гдипжетсолидфиллколор ( \* кисть гпсолидфилл, \* цвет ARGB)**</span><span class="sxs-lookup"><span data-stu-id="ed8d3-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="ed8d3-122">**SolidBrush::-Color (цвет OUT \* ) const**</span><span class="sxs-lookup"><span data-stu-id="ed8d3-122">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="ed8d3-123">Возвращает цвет сплошной кисти</span><span class="sxs-lookup"><span data-stu-id="ed8d3-123">Gets the color of this solid brush</span></span>                                                      |



 

 

 
