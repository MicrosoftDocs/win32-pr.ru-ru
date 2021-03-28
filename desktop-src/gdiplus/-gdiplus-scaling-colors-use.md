---
description: Преобразование «масштабирование» умножает один или несколько четырех компонентов цвета на число. В следующей таблице приведены записи цветовой матрицы, представляющие масштабирование.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Масштабирование цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104273176"
---
# <a name="scaling-colors"></a><span data-ttu-id="81ed1-104">Масштабирование цветов</span><span class="sxs-lookup"><span data-stu-id="81ed1-104">Scaling Colors</span></span>

<span data-ttu-id="81ed1-105">Преобразование «масштабирование» умножает один или несколько четырех компонентов цвета на число.</span><span class="sxs-lookup"><span data-stu-id="81ed1-105">A scaling transformation multiplies one or more of the four color components by a number.</span></span> <span data-ttu-id="81ed1-106">В следующей таблице приведены записи цветовой матрицы, представляющие масштабирование.</span><span class="sxs-lookup"><span data-stu-id="81ed1-106">The color matrix entries that represent scaling are given in the following table.</span></span>



| <span data-ttu-id="81ed1-107">Масштабируемый компонент</span><span class="sxs-lookup"><span data-stu-id="81ed1-107">Component to be scaled</span></span> | <span data-ttu-id="81ed1-108">Запись матрицы</span><span class="sxs-lookup"><span data-stu-id="81ed1-108">Matrix entry</span></span> |
|------------------------|--------------|
| <span data-ttu-id="81ed1-109">Красный</span><span class="sxs-lookup"><span data-stu-id="81ed1-109">Red</span></span>                    | <span data-ttu-id="81ed1-110">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="81ed1-110">\[0\]\[0\]</span></span>   |
| <span data-ttu-id="81ed1-111">Зеленый</span><span class="sxs-lookup"><span data-stu-id="81ed1-111">Green</span></span>                  | <span data-ttu-id="81ed1-112">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="81ed1-112">\[1\]\[1\]</span></span>   |
| <span data-ttu-id="81ed1-113">Синий</span><span class="sxs-lookup"><span data-stu-id="81ed1-113">Blue</span></span>                   | <span data-ttu-id="81ed1-114">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="81ed1-114">\[2\]\[2\]</span></span>   |
| <span data-ttu-id="81ed1-115">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="81ed1-115">Alpha</span></span>                  | <span data-ttu-id="81ed1-116">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="81ed1-116">\[3\]\[3\]</span></span>   |



 

<span data-ttu-id="81ed1-117">В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="81ed1-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="81ed1-118">Затем код масштабирует синий компонент каждого пикселя изображения на коэффициент, равный 2.</span><span class="sxs-lookup"><span data-stu-id="81ed1-118">Then the code scales the blue component of each pixel in the image by a factor of 2.</span></span> <span data-ttu-id="81ed1-119">Исходное изображение отображается вместе с преобразованным изображением.</span><span class="sxs-lookup"><span data-stu-id="81ed1-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



<span data-ttu-id="81ed1-120">На следующем рисунке показано исходное изображение слева и масштабированное изображение справа.</span><span class="sxs-lookup"><span data-stu-id="81ed1-120">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Показывает четыре цветные полосы, а затем те же линии с разными цветами.](images/colortrans3.png)

<span data-ttu-id="81ed1-122">В следующей таблице показаны цветовые векторы для четырех полос до и после синего масштабирования.</span><span class="sxs-lookup"><span data-stu-id="81ed1-122">The following table shows the color vectors for the four bars before and after the blue scaling.</span></span> <span data-ttu-id="81ed1-123">Обратите внимание, что синий компонент на четвертой цветовой полосе перешел с 0,8 на 0,6.</span><span class="sxs-lookup"><span data-stu-id="81ed1-123">Note that the blue component in the fourth color bar went from 0.8 to 0.6.</span></span> <span data-ttu-id="81ed1-124">Это связано с тем, что в GDI+ сохраняется только дробная часть результата.</span><span class="sxs-lookup"><span data-stu-id="81ed1-124">That is because GDI+ retains only the fractional part of the result.</span></span> <span data-ttu-id="81ed1-125">Например, (2) (0,8) = 1,6, а дробная часть 1,6 — 0,6.</span><span class="sxs-lookup"><span data-stu-id="81ed1-125">For example, (2)(0.8) = 1.6, and the fractional part of 1.6 is 0.6.</span></span> <span data-ttu-id="81ed1-126">Сохранение только дробной части гарантирует, что результат всегда находится в диапазоне \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="81ed1-126">Retaining only the fractional part ensures that the result is always in the interval \[0, 1\].</span></span>



| <span data-ttu-id="81ed1-127">До преобразования</span><span class="sxs-lookup"><span data-stu-id="81ed1-127">Original</span></span>           | <span data-ttu-id="81ed1-128">Масштабировать</span><span class="sxs-lookup"><span data-stu-id="81ed1-128">Scaled</span></span>             |
|--------------------|--------------------|
| <span data-ttu-id="81ed1-129">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-129">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="81ed1-130">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-130">(0.4, 0.4, 0.8, 1)</span></span> |
| <span data-ttu-id="81ed1-131">(0.4, 0.2, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-131">(0.4, 0.2, 0.2, 1)</span></span> | <span data-ttu-id="81ed1-132">(0.4, 0.2, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-132">(0.4, 0.2, 0.4, 1)</span></span> |
| <span data-ttu-id="81ed1-133">(0.2, 0.4, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-133">(0.2, 0.4, 0.2, 1)</span></span> | <span data-ttu-id="81ed1-134">(0.2, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-134">(0.2, 0.4, 0.4, 1)</span></span> |
| <span data-ttu-id="81ed1-135">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-135">(0.4, 0.4, 0.8, 1)</span></span> | <span data-ttu-id="81ed1-136">(0.4, 0.4, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-136">(0.4, 0.4, 0.6, 1)</span></span> |



 

<span data-ttu-id="81ed1-137">В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="81ed1-137">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="81ed1-138">Затем код масштабирует красный, зеленый и синий компоненты каждого пикселя в изображении.</span><span class="sxs-lookup"><span data-stu-id="81ed1-138">Then the code scales the red, green, and blue components of each pixel in the image.</span></span> <span data-ttu-id="81ed1-139">Красные компоненты масштабируются на 25 процентов, а зеленые — на 35 процентов, а синие — на 50 процентов.</span><span class="sxs-lookup"><span data-stu-id="81ed1-139">The red components are scaled down 25 percent, the green components are scaled down 35 percent, and the blue components are scaled down 50 percent.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="81ed1-140">На следующем рисунке показано исходное изображение слева и масштабированное изображение справа.</span><span class="sxs-lookup"><span data-stu-id="81ed1-140">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Иллюстрация с четырьмя цветовыми полосами, а затем с разными цветами](images/colortrans4.png)

<span data-ttu-id="81ed1-142">В следующей таблице показаны цветовые векторы для четырех полос до и после красного, зеленого и синего масштабирования.</span><span class="sxs-lookup"><span data-stu-id="81ed1-142">The following table shows the color vectors for the four bars before and after the red, green and blue scaling.</span></span>



| <span data-ttu-id="81ed1-143">До преобразования</span><span class="sxs-lookup"><span data-stu-id="81ed1-143">Original</span></span>           | <span data-ttu-id="81ed1-144">Масштабировать</span><span class="sxs-lookup"><span data-stu-id="81ed1-144">Scaled</span></span>               |
|--------------------|----------------------|
| <span data-ttu-id="81ed1-145">(0.6, 0.6, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-145">(0.6, 0.6, 0.6, 1)</span></span> | <span data-ttu-id="81ed1-146">(0.45, 0.39, 0.3, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-146">(0.45, 0.39, 0.3, 1)</span></span> |
| <span data-ttu-id="81ed1-147">(0, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-147">(0, 1, 1, 1)</span></span>       | <span data-ttu-id="81ed1-148">(0, 0.65, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-148">(0, 0.65, 0.5, 1)</span></span>    |
| <span data-ttu-id="81ed1-149">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-149">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="81ed1-150">(0.75, 0.65, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-150">(0.75, 0.65, 0, 1)</span></span>   |
| <span data-ttu-id="81ed1-151">(1, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-151">(1, 0, 1, 1)</span></span>       | <span data-ttu-id="81ed1-152">(0.75, 0, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="81ed1-152">(0.75, 0, 0.5, 1)</span></span>    |



 

 

 



