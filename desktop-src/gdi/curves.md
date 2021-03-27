---
description: Обычная кривая — это набор выделенных пикселов на растровом дисплее (или точек на печатной странице), определяющих периметр (или часть периметра) раздела Коник.
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: Кривые
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e694edeb535dbc7dbd4191a5a2b0b44556b810e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898441"
---
# <a name="curves"></a><span data-ttu-id="a3c62-103">Кривые</span><span class="sxs-lookup"><span data-stu-id="a3c62-103">Curves</span></span>

<span data-ttu-id="a3c62-104">Обычная кривая — это набор выделенных пикселов на растровом дисплее (или точек на печатной странице), определяющих периметр (или часть периметра) раздела Коник.</span><span class="sxs-lookup"><span data-stu-id="a3c62-104">A regular curve is a set of highlighted pixels on a raster display (or dots on a printed page) that define the perimeter (or part of the perimeter) of a conic section.</span></span> <span data-ttu-id="a3c62-105">Неравномерные кривые — это набор пикселей, определяющий кривую, которая не соответствует периметру раздела Коник.</span><span class="sxs-lookup"><span data-stu-id="a3c62-105">An irregular curve is a set of pixels that define a curve that does not fit the perimeter of a conic section.</span></span> <span data-ttu-id="a3c62-106">Конечная точка исключается из кривой так же, как она исключается из строки.</span><span class="sxs-lookup"><span data-stu-id="a3c62-106">The ending point is excluded from a curve just as it is excluded from a line.</span></span>

<span data-ttu-id="a3c62-107">Когда приложение вызывает одну из функций кривых-Drawing, GDI разбивает кривую на ряд очень мелких дискретных линейных сегментов.</span><span class="sxs-lookup"><span data-stu-id="a3c62-107">When an application calls one of the curve-drawing functions, GDI breaks the curve into a number of extremely small, discrete line segments.</span></span> <span data-ttu-id="a3c62-108">Определив конечные точки (начальную и конечную точки) для каждого из этих сегментов линии, GDI определяет, какие пиксели (или точки) определяют каждую строку, применяя ее ДДА.</span><span class="sxs-lookup"><span data-stu-id="a3c62-108">After determining the endpoints (starting point and ending point) for each of these line segments, GDI determines which pixels (or dots) define each line by applying its DDA.</span></span>

<span data-ttu-id="a3c62-109">Приложение может рисовать эллипс или часть эллипса путем вызова функции [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) .</span><span class="sxs-lookup"><span data-stu-id="a3c62-109">An application can draw an ellipse or part of an ellipse by calling the [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) function.</span></span> <span data-ttu-id="a3c62-110">Эта функция Рисует кривую внутри периметра невидимого прямоугольника, называемого ограничивающим прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="a3c62-110">This function draws the curve within the perimeter of an invisible rectangle called a bounding rectangle.</span></span> <span data-ttu-id="a3c62-111">Размер эллипса определяется двумя невидимыми радиальными углами, которые расширяются от центра прямоугольника до сторон прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="a3c62-111">The size of the ellipse is specified by two invisible radials extending from the center of the rectangle to the sides of the rectangle.</span></span> <span data-ttu-id="a3c62-112">На следующем рисунке показана дуга (часть эллипса), нарисованная с помощью функции **дуги** .</span><span class="sxs-lookup"><span data-stu-id="a3c62-112">The following illustration shows an arc (part of an ellipse) drawn by using the **Arc** function.</span></span>

![Диаграмма, на которой показана дуга, представляющая три квартала полного круга](images/cslcv-03.png)

<span data-ttu-id="a3c62-114">При вызове функции [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) в приложении указываются координаты ограничивающего прямоугольника и радиальных элементов.</span><span class="sxs-lookup"><span data-stu-id="a3c62-114">When calling the [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) function, an application specifies the coordinates of the bounding rectangle and radials.</span></span> <span data-ttu-id="a3c62-115">На предыдущем рисунке показан прямоугольник и радиальные линии с пунктирными линиями, в то время как фактическая дуга была вырисована с помощью сплошной линии.</span><span class="sxs-lookup"><span data-stu-id="a3c62-115">The preceding illustration shows the rectangle and radials with dashed lines while the actual arc was drawn using a solid line.</span></span>

<span data-ttu-id="a3c62-116">При рисовании дуги другого объекта приложение может вызывать функции [**сетаркдиректион**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) и [**жетаркдиректион**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) для управления направлением (по часовой стрелке или против часовой стрелки), в котором рисуется объект.</span><span class="sxs-lookup"><span data-stu-id="a3c62-116">When drawing the arc of another object, the application can call the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) and [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) functions to control the direction (clockwise or counterclockwise) in which the object is drawn.</span></span> <span data-ttu-id="a3c62-117">По умолчанию для рисования дуг и других объектов используется направление против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="a3c62-117">The default direction for drawing arcs and other objects is counterclockwise.</span></span>

<span data-ttu-id="a3c62-118">В дополнение к рисованию эллипсов или частей эллипсов, приложения могут рисовать неравномерные кривые, называемые кривыми Безье.</span><span class="sxs-lookup"><span data-stu-id="a3c62-118">In addition to drawing ellipses or parts of ellipses, applications can draw irregular curves called Bézier curves.</span></span> <span data-ttu-id="a3c62-119">*Кривая Безье* — это неравномерные кривые, кривизна которых определяется четырьмя контрольными точками (P1, P2, P3 и P4).</span><span class="sxs-lookup"><span data-stu-id="a3c62-119">A *Bézier curve* is an irregular curve whose curvature is defined by four control points (p1, p2, p3, and p4).</span></span> <span data-ttu-id="a3c62-120">Контрольные точки P1 и P4 определяют начальную и конечную точки кривой, а управляющие точки P2 и P3 определяют форму кривой, помечая точки, в которых кривая меняет ориентацию, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="a3c62-120">The control points p1 and p4 define the starting and ending points of the curve, and the control points p2 and p3 define the shape of the curve by marking points where the curve reverses orientation, as shown in the following diagram.</span></span>

![Иллюстрация, демонстрирующая две кривые Безье, каждая между начальной и конечной точками и каждая с двумя контрольными точками](images/cslcv-04.png)

<span data-ttu-id="a3c62-122">Приложение может рисовать неравномерные кривые, вызывая функцию [**Безье**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) , предоставляя соответствующие контрольные точки.</span><span class="sxs-lookup"><span data-stu-id="a3c62-122">An application can draw irregular curves by calling the [**PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) function, supplying the appropriate control points.</span></span>

 

 



