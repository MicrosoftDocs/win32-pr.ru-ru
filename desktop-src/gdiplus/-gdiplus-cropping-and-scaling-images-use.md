---
title: Кадрирование и масштабирование изображений GDI+
description: Класс Graphics предоставляет несколько методов DrawImage, некоторые из которых имеют параметры исходного и целевого прямоугольника, которые можно использовать для кадрирования и масштабирования изображений.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c70a7b4f7aa0374602326ab856a01bbadc0047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987720"
---
# <a name="cropping-and-scaling-gdi-images"></a><span data-ttu-id="c13b6-103">Кадрирование и масштабирование изображений GDI+</span><span class="sxs-lookup"><span data-stu-id="c13b6-103">Cropping and scaling GDI+ images</span></span>

<span data-ttu-id="c13b6-104">Класс [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) предоставляет несколько методов **DrawImage** , некоторые из которых имеют параметры исходного и целевого прямоугольника, которые можно использовать для кадрирования и масштабирования изображений.</span><span class="sxs-lookup"><span data-stu-id="c13b6-104">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several **DrawImage** methods, some of which have source and destination rectangle parameters that you can use to crop and scale images.</span></span>

<span data-ttu-id="c13b6-105">В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла Apple.gif.</span><span class="sxs-lookup"><span data-stu-id="c13b6-105">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Apple.gif.</span></span> <span data-ttu-id="c13b6-106">Код рисует все изображение Apple в исходном размере.</span><span class="sxs-lookup"><span data-stu-id="c13b6-106">The code draws the entire apple image in its original size.</span></span> <span data-ttu-id="c13b6-107">Затем код вызывает метод **DrawImage** объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) для рисования части изображения Apple в прямоугольнике назначения, который больше, чем исходный образ Apple.</span><span class="sxs-lookup"><span data-stu-id="c13b6-107">The code then calls the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object to draw a portion of the apple image in a destination rectangle that is larger than the original apple image.</span></span>

<span data-ttu-id="c13b6-108">Метод **DrawImage** определяет, какая часть Apple будет рисовать, просматривая исходный прямоугольник, который задается третьим, четвертым, пятый и шестым аргументами.</span><span class="sxs-lookup"><span data-stu-id="c13b6-108">The **DrawImage** method determines which portion of the apple to draw by looking at the source rectangle, which is specified by the third, fourth, fifth, and sixth arguments.</span></span> <span data-ttu-id="c13b6-109">В этом случае Apple обрезается до 75 процентов от его ширины и 75 процентов от высоты.</span><span class="sxs-lookup"><span data-stu-id="c13b6-109">In this case, the apple is cropped to 75 percent of its width and 75 percent of its height.</span></span>

<span data-ttu-id="c13b6-110">Метод **DrawImage** определяет, где следует нарисовать обрезанный Apple, а также размер обрезкиного Apple, просмотрев прямоугольник назначения, который задается вторым аргументом.</span><span class="sxs-lookup"><span data-stu-id="c13b6-110">The **DrawImage** method determines where to draw the cropped apple and how big to make the cropped apple by looking at the destination rectangle, which is specified by the second argument.</span></span> <span data-ttu-id="c13b6-111">В этом случае размер прямоугольника назначения составляет 30%, а высота составляет 30 процентов от исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="c13b6-111">In this case, the destination rectangle is 30 percent wider and 30 percent taller than the original image.</span></span>


```
Image image(L"Apple.gif");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Make the destination rectangle 30 percent wider and
// 30 percent taller than the original image.
// Put the upper-left corner of the destination
// rectangle at (150, 20).
Rect destinationRect(150, 20, 1.3 * width, 1.3 * height);
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw a portion of the image. Scale that portion of the image
// so that it fills the destination rectangle.
graphics.DrawImage(
   &image,
   destinationRect,
   0, 0,              // upper-left corner of source rectangle
   0.75 * width,      // width of source rectangle
   0.75 * height,     // height of source rectangle
   UnitPixel);
```



<span data-ttu-id="c13b6-112">На следующем рисунке показан исходный Apple и масштабированный, обрезанный Apple.</span><span class="sxs-lookup"><span data-stu-id="c13b6-112">The following illustration shows the original apple and the scaled, cropped apple.</span></span>

![Иллюстрация, показывающая Apple, увеличенная часть исходного Apple](images/cropscale1.png)

 

 



