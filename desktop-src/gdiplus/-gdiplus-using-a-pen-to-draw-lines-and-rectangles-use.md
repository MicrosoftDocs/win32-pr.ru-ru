---
description: Для рисования линий и прямоугольников необходим объект Graphics и объект Pen. Объект Graphics предоставляет метод DrawLine, а объект Pen сохраняет функции линии, такие как цвет и ширина.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Рисование линий и прямоугольников с помощью пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991631"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a><span data-ttu-id="32341-104">Рисование линий и прямоугольников с помощью пера</span><span class="sxs-lookup"><span data-stu-id="32341-104">Using a Pen to Draw Lines and Rectangles</span></span>

<span data-ttu-id="32341-105">Для рисования линий и прямоугольников необходим объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="32341-105">To draw lines and rectangles, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="32341-106">Объект **Graphics** предоставляет метод [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) , а объект **Pen** сохраняет функции линии, такие как цвет и ширина.</span><span class="sxs-lookup"><span data-stu-id="32341-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores features of the line, such as color and width.</span></span>

<span data-ttu-id="32341-107">В следующем примере рисуется строка от (20, 10) до (300, 100).</span><span class="sxs-lookup"><span data-stu-id="32341-107">The following example draws a line from (20, 10) to (300, 100).</span></span> <span data-ttu-id="32341-108">Пусть **графика** — существующий объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="32341-108">Assume **graphics** is an existing [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



<span data-ttu-id="32341-109">Первый оператор кода использует конструктор класса [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) для создания черного пера.</span><span class="sxs-lookup"><span data-stu-id="32341-109">The first statement of code uses the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) class constructor to create a black pen.</span></span> <span data-ttu-id="32341-110">Одним из аргументов, передаваемых конструктору **Pen** , является объект [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="32341-110">The one argument passed to the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="32341-111">Значения, используемые для создания объекта **Color** — (255, 0, 0, 0) — соответствуют альфа-, красному, зеленому и синему компонентам цвета.</span><span class="sxs-lookup"><span data-stu-id="32341-111">The values used to construct the **Color** object — (255, 0, 0, 0) — correspond to the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="32341-112">Эти значения определяют непрозрачное черное перо.</span><span class="sxs-lookup"><span data-stu-id="32341-112">These values define an opaque black pen.</span></span>

<span data-ttu-id="32341-113">В следующем примере демонстрируется рисование прямоугольника с верхним левым углом в точке (10, 10).</span><span class="sxs-lookup"><span data-stu-id="32341-113">The following example draws a rectangle with its upper-left corner at (10, 10).</span></span> <span data-ttu-id="32341-114">Ширина прямоугольника равна 100 и высоте 50.</span><span class="sxs-lookup"><span data-stu-id="32341-114">The rectangle has a width of 100 and a height of 50.</span></span> <span data-ttu-id="32341-115">Второй аргумент, передаваемый конструктору [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , указывает, что ширина пера равна 5 пикселам.</span><span class="sxs-lookup"><span data-stu-id="32341-115">The second argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor indicates that the pen width is 5 pixels.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



<span data-ttu-id="32341-116">При прорисовке прямоугольника перо центрируется по границе прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="32341-116">When the rectangle is drawn, the pen is centered on the rectangle's boundary.</span></span> <span data-ttu-id="32341-117">Так как ширина пера равна 5, стороны прямоугольника выводятся в ширину 5 пикселей, то есть 1 пиксель рисуется на границе, 2 пиксела нарисованы внутри, а 2 пиксела — снаружи.</span><span class="sxs-lookup"><span data-stu-id="32341-117">Because the pen width is 5, the sides of the rectangle are drawn 5 pixels wide, such that 1 pixel is drawn on the boundary itself, 2 pixels are drawn on the inside, and 2 pixels are drawn on the outside.</span></span> <span data-ttu-id="32341-118">Дополнительные сведения о выравнивании пера см. в разделе [Настройка ширины и выравнивания пера](-gdiplus-setting-pen-width-and-alignment-use.md).</span><span class="sxs-lookup"><span data-stu-id="32341-118">For more details on pen alignment, see [Setting Pen Width and Alignment](-gdiplus-setting-pen-width-and-alignment-use.md).</span></span>

<span data-ttu-id="32341-119">На следующем рисунке показан итоговый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="32341-119">The following illustration shows the resulting rectangle.</span></span> <span data-ttu-id="32341-120">Пунктирные линии показывают, где будет нарисован прямоугольник, если толщина пера была равна одному пикселю.</span><span class="sxs-lookup"><span data-stu-id="32341-120">The dotted lines show where the rectangle would have been drawn if the pen width had been one pixel.</span></span> <span data-ttu-id="32341-121">Увеличенное представление верхнего левого угла прямоугольника показывает, что толстые черные линии центрируются по пунктирным линиям.</span><span class="sxs-lookup"><span data-stu-id="32341-121">The enlarged view of the upper-left corner of the rectangle shows that the thick black lines are centered on those dotted lines.</span></span>

![Иллюстрация прямоугольника, рисуемого толстой черной линией, которая окружает тонкую, серую, пунктирную линию](images/pens1.png)

 

 



