---
description: Наклон увеличивает или уменьшает компонент цвета на величину, пропорциональную другому компоненту цвета.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Наклон цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156178"
---
# <a name="shearing-colors"></a><span data-ttu-id="52160-103">Наклон цветов</span><span class="sxs-lookup"><span data-stu-id="52160-103">Shearing Colors</span></span>

<span data-ttu-id="52160-104">Наклон увеличивает или уменьшает компонент цвета на величину, пропорциональную другому компоненту цвета.</span><span class="sxs-lookup"><span data-stu-id="52160-104">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="52160-105">Например, рассмотрим преобразование, при котором красный компонент увеличивается на одну половину значения синего компонента.</span><span class="sxs-lookup"><span data-stu-id="52160-105">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="52160-106">При таком преобразовании цвет (0,2, 0,5, 1) станет равен (0,7, 0,5, 1).</span><span class="sxs-lookup"><span data-stu-id="52160-106">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="52160-107">Новый красный компонент — 0,2 + (1/2) (1) = 0,7.</span><span class="sxs-lookup"><span data-stu-id="52160-107">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>

<span data-ttu-id="52160-108">В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла ColorBars4.bmp.</span><span class="sxs-lookup"><span data-stu-id="52160-108">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="52160-109">Затем код применяет преобразование «наклонное», описанное в предыдущем абзаце, к каждому пикселу изображения.</span><span class="sxs-lookup"><span data-stu-id="52160-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="52160-110">На следующем рисунке показано исходное изображение слева и наклонное изображение справа.</span><span class="sxs-lookup"><span data-stu-id="52160-110">The following illustration shows the original image on the left and the sheared image on the right.</span></span>

![Иллюстрация, на которой показаны четыре цветные полосы, а затем те же линии с разными цветами](images/colortrans6.png)

<span data-ttu-id="52160-112">В следующей таблице показаны цветовые векторы для четырех полос до и после преобразования «наклон».</span><span class="sxs-lookup"><span data-stu-id="52160-112">The following table shows the color vectors for the four bars before and after the shearing transformation.</span></span>



| <span data-ttu-id="52160-113">До преобразования</span><span class="sxs-lookup"><span data-stu-id="52160-113">Original</span></span>           | <span data-ttu-id="52160-114">С наклоном</span><span class="sxs-lookup"><span data-stu-id="52160-114">Sheared</span></span>            |
|--------------------|--------------------|
| <span data-ttu-id="52160-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="52160-115">(0, 0, 1, 1)</span></span>       | <span data-ttu-id="52160-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="52160-116">(0.5, 0, 1, 1)</span></span>     |
| <span data-ttu-id="52160-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="52160-117">(0.5, 1, 0.5, 1)</span></span>   | <span data-ttu-id="52160-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="52160-118">(0.75, 1, 0.5, 1)</span></span>  |
| <span data-ttu-id="52160-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="52160-119">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="52160-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="52160-120">(1, 1, 0, 1)</span></span>       |
| <span data-ttu-id="52160-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="52160-121">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="52160-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="52160-122">(0.6, 0.4, 0.4, 1)</span></span> |



 

 

 



