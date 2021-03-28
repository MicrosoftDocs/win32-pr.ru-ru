---
description: Перевод добавляет значение к одному или нескольким из четырех компонентов цвета. В следующей таблице приведены записи цветовой матрицы, представляющие переводы.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Преобразование цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563684"
---
# <a name="translating-colors"></a><span data-ttu-id="62c63-104">Преобразование цветов</span><span class="sxs-lookup"><span data-stu-id="62c63-104">Translating Colors</span></span>

<span data-ttu-id="62c63-105">Перевод добавляет значение к одному или нескольким из четырех компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="62c63-105">A translation adds a value to one or more of the four color components.</span></span> <span data-ttu-id="62c63-106">В следующей таблице приведены записи цветовой матрицы, представляющие переводы.</span><span class="sxs-lookup"><span data-stu-id="62c63-106">The color matrix entries that represent translations are given in the following table.</span></span>



| <span data-ttu-id="62c63-107">Преобразуемый компонент</span><span class="sxs-lookup"><span data-stu-id="62c63-107">Component to be translated</span></span> | <span data-ttu-id="62c63-108">Запись матрицы</span><span class="sxs-lookup"><span data-stu-id="62c63-108">Matrix entry</span></span> |
|----------------------------|--------------|
| <span data-ttu-id="62c63-109">Красный</span><span class="sxs-lookup"><span data-stu-id="62c63-109">Red</span></span>                        | <span data-ttu-id="62c63-110">\[4 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="62c63-110">\[4\]\[0\]</span></span>   |
| <span data-ttu-id="62c63-111">Зеленый</span><span class="sxs-lookup"><span data-stu-id="62c63-111">Green</span></span>                      | <span data-ttu-id="62c63-112">\[4 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="62c63-112">\[4\]\[1\]</span></span>   |
| <span data-ttu-id="62c63-113">Синий</span><span class="sxs-lookup"><span data-stu-id="62c63-113">Blue</span></span>                       | <span data-ttu-id="62c63-114">\[4 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="62c63-114">\[4\]\[2\]</span></span>   |
| <span data-ttu-id="62c63-115">Коэффициент альфа</span><span class="sxs-lookup"><span data-stu-id="62c63-115">Alpha</span></span>                      | <span data-ttu-id="62c63-116">\[4 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="62c63-116">\[4\]\[3\]</span></span>   |



 

<span data-ttu-id="62c63-117">В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла ColorBars.bmp.</span><span class="sxs-lookup"><span data-stu-id="62c63-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars.bmp.</span></span> <span data-ttu-id="62c63-118">Затем код добавляет 0,75 к красному компоненту каждого пикселя в изображении.</span><span class="sxs-lookup"><span data-stu-id="62c63-118">Then the code adds 0.75 to the red component of each pixel in the image.</span></span> <span data-ttu-id="62c63-119">Исходное изображение отображается вместе с преобразованным изображением.</span><span class="sxs-lookup"><span data-stu-id="62c63-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="62c63-120">На следующем рисунке показано исходное изображение слева и преобразованное изображение справа.</span><span class="sxs-lookup"><span data-stu-id="62c63-120">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![Иллюстрация, на которой показаны четыре цветные полосы, а затем те же линии с разными цветами](images/colortrans2.png)

<span data-ttu-id="62c63-122">В следующей таблице перечислены цветовые векторы для четырех полос до и после Красной трансляции.</span><span class="sxs-lookup"><span data-stu-id="62c63-122">The following table lists the color vectors for the four bars before and after the red translation.</span></span> <span data-ttu-id="62c63-123">Обратите внимание, что поскольку максимальное значение для компонента цвета равно 1, красный компонент во второй строке не изменяется.</span><span class="sxs-lookup"><span data-stu-id="62c63-123">Note that because the maximum value for a color component is 1, the red component in the second row does not change.</span></span> <span data-ttu-id="62c63-124">(Аналогичным образом, минимальное значение для компонента цвета равно 0.)</span><span class="sxs-lookup"><span data-stu-id="62c63-124">(Similarly, the minimum value for a color component is 0.)</span></span>



| <span data-ttu-id="62c63-125">До преобразования</span><span class="sxs-lookup"><span data-stu-id="62c63-125">Original</span></span>           | <span data-ttu-id="62c63-126">Переведенный текст</span><span class="sxs-lookup"><span data-stu-id="62c63-126">Translated</span></span>      |
|--------------------|-----------------|
| <span data-ttu-id="62c63-127">Черный (0, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="62c63-127">Black (0, 0, 0, 1)</span></span> | <span data-ttu-id="62c63-128">(0.75, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="62c63-128">(0.75, 0, 0, 1)</span></span> |
| <span data-ttu-id="62c63-129">Красный (1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="62c63-129">Red (1, 0, 0, 1)</span></span>   | <span data-ttu-id="62c63-130">(1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="62c63-130">(1, 0, 0, 1)</span></span>    |
| <span data-ttu-id="62c63-131">Зеленый (0, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="62c63-131">Green (0, 1, 0, 1)</span></span> | <span data-ttu-id="62c63-132">(0.75, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="62c63-132">(0.75, 1, 0, 1)</span></span> |
| <span data-ttu-id="62c63-133">Blue (0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="62c63-133">Blue (0, 0, 1, 1)</span></span>  | <span data-ttu-id="62c63-134">(0.75, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="62c63-134">(0.75, 0, 1, 1)</span></span> |



 

 

 



