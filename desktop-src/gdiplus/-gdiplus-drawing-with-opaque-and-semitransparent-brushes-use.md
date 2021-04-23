---
description: При заполнении фигуры необходимо передать адрес объекта Brush в один из методов Fill класса Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Рисование с помощью непрозрачных и полупрозрачных кистей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156195"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a><span data-ttu-id="21b3a-103">Рисование с помощью непрозрачных и полупрозрачных кистей</span><span class="sxs-lookup"><span data-stu-id="21b3a-103">Drawing with Opaque and Semitransparent Brushes</span></span>

<span data-ttu-id="21b3a-104">При заполнении фигуры необходимо передать адрес объекта [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) в один из методов Fill класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="21b3a-104">When you fill a shape, you must pass the address of a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="21b3a-105">Единственным параметром конструктора [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) является объект [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="21b3a-105">The one parameter of the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor is a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="21b3a-106">Чтобы залить непрозрачную фигуру, следует установить значение альфа-компонента цвета в 255.</span><span class="sxs-lookup"><span data-stu-id="21b3a-106">To fill an opaque shape, set the alpha component of the color to 255.</span></span> <span data-ttu-id="21b3a-107">Чтобы залить полупрозрачную фигуру, установите значение альфа-компонента в интервале от 1 до 254.</span><span class="sxs-lookup"><span data-stu-id="21b3a-107">To fill a semitransparent shape, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="21b3a-108">При заполнении полупрозрачной фигуры цвет фигуры смешивается с цветами фона.</span><span class="sxs-lookup"><span data-stu-id="21b3a-108">When you fill a semitransparent shape, the color of the shape is blended with the colors of the background.</span></span> <span data-ttu-id="21b3a-109">Альфа-компонент указывает, как цвета фигур и фона смешиваются. Альфа-значения рядом с 0 помещают больший вес на цвета фона, а альфа-значения около 255 помещают на цвет фигуры.</span><span class="sxs-lookup"><span data-stu-id="21b3a-109">The alpha component specifies how the shape and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the shape color.</span></span>

<span data-ttu-id="21b3a-110">В следующем примере рисуется изображение, которое затем заполняется тремя эллипсами, которые перекрывают изображение.</span><span class="sxs-lookup"><span data-stu-id="21b3a-110">The following example draws an image and then fills three ellipses that overlap the image.</span></span> <span data-ttu-id="21b3a-111">Для первого эллипса используется значение альфа-компонента, равное 255, поэтому он непрозрачен.</span><span class="sxs-lookup"><span data-stu-id="21b3a-111">The first ellipse uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="21b3a-112">Для второго и третьего эллипсов используется значение альфа-компонента, равное 128, поэтому они полупрозрачные и сквозь эллипсы видно фоновое изображение.</span><span class="sxs-lookup"><span data-stu-id="21b3a-112">The second and third ellipses use an alpha component of 128, so they are semitransparent; you can see the background image through the ellipses.</span></span> <span data-ttu-id="21b3a-113">Вызов [**Graphics:: сеткомпоситингкуалити**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) приводит к тому, что смешение третьего эллипса выполняется вместе с гаммой коррекцией.</span><span class="sxs-lookup"><span data-stu-id="21b3a-113">The call to [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third ellipse to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



<span data-ttu-id="21b3a-114">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="21b3a-114">The following illustration shows the output of the preceding code.</span></span>

![Иллюстрация, показывающая изображение, наложенное тремя эллипсами: один непрозрачный, один немного прозрачный, один очень прозрачный](images/compqualellipse.png)

 

 



