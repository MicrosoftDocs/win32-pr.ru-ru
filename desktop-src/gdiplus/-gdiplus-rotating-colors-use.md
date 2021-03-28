---
description: Вращение трехмерного цветового пространства сложно визуализировать.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Вращение цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897297"
---
# <a name="rotating-colors"></a><span data-ttu-id="418c2-103">Вращение цветов</span><span class="sxs-lookup"><span data-stu-id="418c2-103">Rotating Colors</span></span>

<span data-ttu-id="418c2-104">Вращение трехмерного цветового пространства сложно визуализировать.</span><span class="sxs-lookup"><span data-stu-id="418c2-104">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="418c2-105">Мы можем упростить визуализацию вращения, добавив одно из исправленных компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="418c2-105">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="418c2-106">Допустим, мы согласны, что альфа-компонент будет исправлен на 1 (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="418c2-106">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="418c2-107">Затем мы можем визуализировать трехмерное цветовое пространство с красной, зеленой и синей осями, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="418c2-107">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>

![Иллюстрация перспективного представления трехмерного цветового пространства с осями, обозначенными красным, зеленым и синим](images/recoloring03.png)

<span data-ttu-id="418c2-109">Цвет можно рассматривать как точку в трехмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="418c2-109">A color can be thought of as a point in 3-D space.</span></span> <span data-ttu-id="418c2-110">Например, точка (1, 0, 0) в пространстве представляет красный цвет, а точка (0, 1, 0) в пространстве представляет зеленый цвет.</span><span class="sxs-lookup"><span data-stu-id="418c2-110">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>

<span data-ttu-id="418c2-111">На следующем рисунке показано, что означает поворот цвета (1, 0, 0) на угол в 60 градусов на плоскости Red-Green.</span><span class="sxs-lookup"><span data-stu-id="418c2-111">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="418c2-112">Вращение в плоскости, параллельной плоскости Red-Green, можно рассматривать как поворот синей оси.</span><span class="sxs-lookup"><span data-stu-id="418c2-112">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>

![Иллюстрация, показывающая точку (1, 0, 0), повернутую на 60 градусов в (0,5, 0,866, 0)](images/recoloring04.png)

<span data-ttu-id="418c2-114">На следующем рисунке показано, как инициализировать матрицу цветов, чтобы выполнять вращение вокруг каждой из трех осей координат (красный, зеленый, синий).</span><span class="sxs-lookup"><span data-stu-id="418c2-114">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue).</span></span>

![Иллюстрация, демонстрирующая цветовые матрицы, выполняющие вращение вокруг каждой из трех осей координат](images/recoloring05.png)

<span data-ttu-id="418c2-116">Следующий пример принимает изображение, которое имеет один цвет (1, 0, 0,6) и применяет поворот на 60 градусов к синей оси.</span><span class="sxs-lookup"><span data-stu-id="418c2-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="418c2-117">Угол поворота Очистка на плоскости, которая параллельна плоскости Red-Green.</span><span class="sxs-lookup"><span data-stu-id="418c2-117">The angle of the rotation is swept out in a plane that is parallel to the Red-Green plane.</span></span>


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="418c2-118">На следующем рисунке показано исходное изображение слева и цветное изображение справа.</span><span class="sxs-lookup"><span data-stu-id="418c2-118">The following illustration shows the original image on the left and the color-rotated image on the right.</span></span>

![Иллюстрация, показывающая, что прямоугольники заполнены исходным изображением (фиолетово-красный) и цветовым изображением (зеленый цвет морской волны)](images/colortrans5.png)

<span data-ttu-id="418c2-120">Поворот цвета, выполненный в предыдущем примере кода, можно сделать наглядным, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="418c2-120">The color rotation performed in the preceding code example can be visualized as follows.</span></span>

![Иллюстрация, показывающая трехмерное цветовое пространство, а также точка (1, 0, 0,6), повернутая на 60 градусов в (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



