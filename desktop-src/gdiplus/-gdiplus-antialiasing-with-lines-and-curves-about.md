---
description: При рисовании линии с помощью Windows GDI+ вы предоставляете начальную и конечную точки линии, но не нужно указывать никаких сведений об отдельных пикселях в строке.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Сглаживание прямых и кривых линий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c817d3e11b4699c9fc892b41dcc827c0861f192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812982"
---
# <a name="antialiasing-with-lines-and-curves"></a><span data-ttu-id="fbcb0-103">Сглаживание прямых и кривых линий</span><span class="sxs-lookup"><span data-stu-id="fbcb0-103">Antialiasing with Lines and Curves</span></span>

<span data-ttu-id="fbcb0-104">При рисовании линии с помощью Windows GDI+ вы предоставляете начальную и конечную точки линии, но не нужно указывать никаких сведений об отдельных пикселях в строке.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-104">When you use Windows GDI+ to draw a line, you provide the starting point and ending point of the line, but you don't have to provide any information about the individual pixels on the line.</span></span> <span data-ttu-id="fbcb0-105">Интерфейс GDI+ работает вместе с программным обеспечением драйвера экрана, чтобы определить, какие пикселы будут включены для отображения линии на конкретном устройстве отображения.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-105">GDI+ works in conjunction with the display driver software to determine which pixels will be turned on to show the line on a particular display device.</span></span>

<span data-ttu-id="fbcb0-106">Рассмотрим прямую красную линию, которая перемещается с точки (4, 2) на точку (16, 10).</span><span class="sxs-lookup"><span data-stu-id="fbcb0-106">Consider a straight red line that goes from the point (4, 2) to the point (16, 10).</span></span> <span data-ttu-id="fbcb0-107">Предположим, что у системы координат есть источник в левом верхнем углу и что единицей измерения является пиксель.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-107">Assume the coordinate system has its origin in the upper-left corner and that the unit of measure is the pixel.</span></span> <span data-ttu-id="fbcb0-108">Также предположим, что ось x указывает вправо, а ось y — вниз.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-108">Also assume that the x-axis points to the right and the y-axis points down.</span></span> <span data-ttu-id="fbcb0-109">На следующем рисунке показано увеличенное представление красной линии, нарисованной на многоцветном фоне.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-109">The following illustration shows an enlarged view of the red line drawn on a multicolored background.</span></span>

![Иллюстрация, показывающая сплошные красные пиксели на многоцветном фоне](images/aboutgdip02-art33.png)

<span data-ttu-id="fbcb0-111">Обратите внимание, что красные пиксели, используемые для визуализации линии, являются непрозрачными.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-111">Note that the red pixels used to render the line are opaque.</span></span> <span data-ttu-id="fbcb0-112">Нет частично прозрачных пикселов, участвующих в отображении линии.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-112">There are no partially transparent pixels involved in displaying the line.</span></span> <span data-ttu-id="fbcb0-113">Этот тип отрисовки линии дает линии зубчатый внешний вид, а линия выглядит немного так же, как лестница.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-113">This type of line rendering gives the line a jagged appearance, and the line looks a bit like a staircase.</span></span> <span data-ttu-id="fbcb0-114">Этот способ представления линии с лестницой называется псевдонимом; Лестница — это псевдоним теоретической линии.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-114">This technique of representing a line with a staircase is called aliasing; the staircase is an alias for the theoretical line.</span></span>

<span data-ttu-id="fbcb0-115">Более сложная методика отрисовки линий заключается в использовании частично прозрачных пикселей вместе с чисто красными пикселами.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-115">A more sophisticated technique for rendering a line involves using partially transparent pixels along with pure red pixels.</span></span> <span data-ttu-id="fbcb0-116">Пиксели устанавливаются в чистый красный цвет или на некоторое смешение красного и цвета фона в зависимости от того, насколько близко они находятся к линии.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-116">Pixels are set to pure red or to some blend of red and the background color depending on how close they are to the line.</span></span> <span data-ttu-id="fbcb0-117">Этот тип отрисовки называется сглаживанием и дает строку, которую человеческий глаз воспринимает как более гладкий.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-117">This type of rendering is called antialiasing and results in a line that the human eye perceives as more smooth.</span></span> <span data-ttu-id="fbcb0-118">На следующем рисунке показано, как определенные Пиксели смешиваются с фоном для создания сглаженной линии.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-118">The following illustration shows how certain pixels are blended with the background to produce an antialiased line.</span></span>

![Иллюстрация, отображающая Пиксели, которые являются оттенками красного цвета на одном фоне](images/aboutgdip02-art34.png)

<span data-ttu-id="fbcb0-120">Сглаживание можно также применять к кривым.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-120">Antialiasing (smoothing) can also be applied to curves.</span></span> <span data-ttu-id="fbcb0-121">На следующем рисунке показано увеличенное представление сглаженного эллипса.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-121">The following illustration shows an enlarged view of a smoothed ellipse.</span></span>

![Иллюстрация эллипса, состоящие из различных оттенков синего пикселя на белом фоне](images/aboutgdip02-art35.png)

<span data-ttu-id="fbcb0-123">На следующем рисунке показан тот же эллипс в его фактическом размере, один раз без сглаживания и один раз с сглаживанием.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-123">The following illustration shows the same ellipse in its actual size, once without antialiasing and once with antialiasing.</span></span>

![снимок экрана с двумя эллипсами: значок с сглаживанием выглядит более гладко](images/aboutgdip02-art36.png)

<span data-ttu-id="fbcb0-125">Чтобы нарисовать линии и кривые, использующие сглаживание, создайте объект [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и передайте *смусингмодеантиалиас* в его метод [**Graphics:: сетсмусингмоде**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="fbcb0-125">To draw lines and curves that use antialiasing, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass *SmoothingModeAntiAlias* to its [**Graphics::SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) method.</span></span> <span data-ttu-id="fbcb0-126">Затем вызовите один из методов рисования этого **графического** объекта.</span><span class="sxs-lookup"><span data-stu-id="fbcb0-126">Then call one of the drawing methods of that same **Graphics** object.</span></span>


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



<span data-ttu-id="fbcb0-127">**Смусингмодеантиалиас** является элементом перечисления [**смусингмоде**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) .</span><span class="sxs-lookup"><span data-stu-id="fbcb0-127">**SmoothingModeAntiAlias** is an element of the [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) enumeration.</span></span>

 

 



