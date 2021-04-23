---
description: При рисовании линии необходимо передать адрес объекта Pen методу DrawLine класса Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Рисование непрозрачных и частично прозрачных линий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f751e5808440c1051b3cd996f7ebcb2df0ccbcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564307"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a><span data-ttu-id="268f5-103">Рисование непрозрачных и частично прозрачных линий</span><span class="sxs-lookup"><span data-stu-id="268f5-103">Drawing Opaque and Semitransparent Lines</span></span>

<span data-ttu-id="268f5-104">При рисовании линии необходимо передать адрес объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) методу [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="268f5-104">When you draw a line, you must pass the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="268f5-105">Одним из параметров конструктора **пера** является объект [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="268f5-105">One of the parameters of the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="268f5-106">Чтобы нарисовать непрозрачную линию, установите альфа-компонент цвета равным 255.</span><span class="sxs-lookup"><span data-stu-id="268f5-106">To draw an opaque line, set the alpha component of the color to 255.</span></span> <span data-ttu-id="268f5-107">Чтобы нарисовать полупрозрачную линию, установите значение альфа-компонента в диапазоне от 1 до 254.</span><span class="sxs-lookup"><span data-stu-id="268f5-107">To draw a semitransparent line, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="268f5-108">При рисовании полупрозрачной линии на некотором фоне цвет линии смешивается с цветами фона.</span><span class="sxs-lookup"><span data-stu-id="268f5-108">When you draw a semitransparent line over a background, the color of the line is blended with the colors of the background.</span></span> <span data-ttu-id="268f5-109">Альфа-компонент указывает, как цвета линий и фона смешиваются. Альфа-значения рядом с 0 помещают больший вес на цвета фона, а альфа-значения около 255 помещают больше на цвет линии.</span><span class="sxs-lookup"><span data-stu-id="268f5-109">The alpha component specifies how the line and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the line color.</span></span>

<span data-ttu-id="268f5-110">В следующем примере рисуется изображение, а затем выводится три линии, которые используют изображение в качестве фона.</span><span class="sxs-lookup"><span data-stu-id="268f5-110">The following example draws an image and then draws three lines that use the image as a background.</span></span> <span data-ttu-id="268f5-111">Цвет первой линии имеет альфа-компонент, равный 255, поэтому она является непрозрачной.</span><span class="sxs-lookup"><span data-stu-id="268f5-111">The first line uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="268f5-112">Для второй и третьей линий используется альфа-компонент, равный 128, поэтому они являются полупрозрачными и сквозь них можно видеть фоновое изображение.</span><span class="sxs-lookup"><span data-stu-id="268f5-112">The second and third lines use an alpha component of 128, so they are semitransparent; you can see the background image through the lines.</span></span> <span data-ttu-id="268f5-113">Вызов [**Graphics:: сеткомпоситингкуалити**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) приводит к тому, что смешение третьей линии выполняется вместе с гаммой коррекцией.</span><span class="sxs-lookup"><span data-stu-id="268f5-113">The call to [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third line to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



<span data-ttu-id="268f5-114">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="268f5-114">The following illustration shows the output of the preceding code.</span></span>

![Иллюстрация, показывающая изображение, наложенное тремя широкими линиями: один непрозрачный, один немного прозрачный и один очень прозрачный](images/compqualline.png)

 

 



