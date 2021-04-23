---
description: 'На следующем рисунке показаны две кривые: одна открытая и одна закрытая.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Незамкнутые и замкнутые кривые
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7587ec950f8a0abc21f8c9cfb000a7333e87297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569254"
---
# <a name="open-and-closed-curves"></a><span data-ttu-id="bec7b-103">Незамкнутые и замкнутые кривые</span><span class="sxs-lookup"><span data-stu-id="bec7b-103">Open and Closed Curves</span></span>

<span data-ttu-id="bec7b-104">На следующем рисунке показаны две кривые: одна открытая и одна закрытая.</span><span class="sxs-lookup"><span data-stu-id="bec7b-104">The following illustration shows two curves: one open and one closed.</span></span>

![Иллюстрация открытой кривой (изогнутая линия) и замкнутой кривой (контур фигуры)](images/aboutgdip02-art24.png)

<span data-ttu-id="bec7b-106">Замкнутые кривые имеют внутреннее пространство, поэтому их можно заполнить кистью.</span><span class="sxs-lookup"><span data-stu-id="bec7b-106">Closed curves have an interior and therefore can be filled with a brush.</span></span> <span data-ttu-id="bec7b-107">Класс [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) в Windows GDI+ предоставляет следующие методы заполнения замкнутых фигур и кривых: [филлректангле](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [филлеллипсе](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [филлпие](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [Филлполигон](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [филлклоседкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics:: филлпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)и [**Graphics:: филлрегион**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span><span class="sxs-lookup"><span data-stu-id="bec7b-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class in Windows GDI+ provides the following methods for filling closed figures and curves: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath), and [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span></span> <span data-ttu-id="bec7b-108">При каждом вызове одного из этих методов необходимо передать в качестве аргумента адрес одного из конкретных типов кисти ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**хатчбруш**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)или [**пасградиентбруш**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)).</span><span class="sxs-lookup"><span data-stu-id="bec7b-108">Whenever you call one of these methods, you must pass the address of one of the specific brush types ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), or [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) as an argument.</span></span>

<span data-ttu-id="bec7b-109">Метод [филлпие](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) является вспомогательным для метода [драварк](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) .</span><span class="sxs-lookup"><span data-stu-id="bec7b-109">The [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) method is a companion to the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method.</span></span> <span data-ttu-id="bec7b-110">Точно так же, как метод Драварк рисует часть контура эллипса, метод Филлпие заполняет часть внутренней части эллипса.</span><span class="sxs-lookup"><span data-stu-id="bec7b-110">Just as the DrawArc method draws a portion of the outline of an ellipse, the FillPie method fills a portion of the interior of an ellipse.</span></span> <span data-ttu-id="bec7b-111">В следующем примере рисуется дуга и заполняется соответствующая часть внутри эллипса.</span><span class="sxs-lookup"><span data-stu-id="bec7b-111">The following example draws an arc and fills the corresponding portion of the interior of the ellipse.</span></span>


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



<span data-ttu-id="bec7b-112">На следующем рисунке показана дуга и заполненная круговая диаграмма.</span><span class="sxs-lookup"><span data-stu-id="bec7b-112">The following illustration shows the arc and the filled pie.</span></span>

![Иллюстрация, показывающая сегмент закрашенного эллипса](images/aboutgdip02-art25.png)

<span data-ttu-id="bec7b-114">Метод [филлклоседкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) является вспомогательным для метода [дравклоседкурве](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="bec7b-114">The [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) method is a companion to the [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="bec7b-115">Оба метода автоматически закрывают кривую, подключив конечную точку к начальной точке.</span><span class="sxs-lookup"><span data-stu-id="bec7b-115">Both methods automatically close the curve by connecting the ending point to the starting point.</span></span> <span data-ttu-id="bec7b-116">В следующем примере рисуется кривая, которая проходит через (0, 0), (60, 20) и (40, 50).</span><span class="sxs-lookup"><span data-stu-id="bec7b-116">The following example draws a curve that passes through (0, 0), (60, 20), and (40, 50).</span></span> <span data-ttu-id="bec7b-117">Затем кривая автоматически закрывается путем подключения (40, 50) к начальной точке (0, 0), а внутренняя часть заполняется сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="bec7b-117">Then, the curve is automatically closed by connecting (40, 50) to the starting point (0, 0), and the interior is filled with a solid color.</span></span>


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



<span data-ttu-id="bec7b-118">Путь может состоять из нескольких иллюстраций (подконтуров).</span><span class="sxs-lookup"><span data-stu-id="bec7b-118">A path can consist of several figures (subpaths).</span></span> <span data-ttu-id="bec7b-119">Метод [**Graphics:: филлпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) заполняет внутреннюю часть каждой фигуры.</span><span class="sxs-lookup"><span data-stu-id="bec7b-119">The [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the interior of each figure.</span></span> <span data-ttu-id="bec7b-120">Если фигура не закрыта, метод **Graphics:: филлпас** заполняет область, которая будет заключена, если фигура была закрыта.</span><span class="sxs-lookup"><span data-stu-id="bec7b-120">If a figure is not closed, the **Graphics::FillPath** method fills the area that would be enclosed if the figure were closed.</span></span> <span data-ttu-id="bec7b-121">В следующем примере рисуется и заполняется контур, состоящий из дуги, фундаментального сплайна, строки и круговой диаграммы.</span><span class="sxs-lookup"><span data-stu-id="bec7b-121">The following example draws and fills a path that consists of an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="bec7b-122">На следующем рисунке показан путь до и после заполнения сплошной кистью.</span><span class="sxs-lookup"><span data-stu-id="bec7b-122">The following illustration shows the path before and after it is filled with a solid brush.</span></span> <span data-ttu-id="bec7b-123">Обратите внимание, что текст в строке имеет контур, но не заполняется методом [**Graphics::D равпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) .</span><span class="sxs-lookup"><span data-stu-id="bec7b-123">Note that the text in the string is outlined, but not filled, by the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method.</span></span> <span data-ttu-id="bec7b-124">Это метод [**Graphics:: филлпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) , который закрашивает внутренние части символов в строке.</span><span class="sxs-lookup"><span data-stu-id="bec7b-124">It is the [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method that paints the interiors of the characters in the string.</span></span>

![Иллюстрация, на которой дважды отображается текст, а также открытая и замкнутая кривая; они пусты и заполняются второй раз.](images/aboutgdip02-art26.png)

 

 



