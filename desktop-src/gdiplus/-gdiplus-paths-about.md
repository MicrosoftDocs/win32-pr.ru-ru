---
description: Контуры формируются путем объединения линий, прямоугольников и простых кривых. Взпомним о векторной графике, которые были признаны наиболее полезными для рисования изображений в следующих основных стандартных блоках.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Контуры (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554300"
---
# <a name="paths-gdi"></a><span data-ttu-id="b208f-104">Контуры (GDI+)</span><span class="sxs-lookup"><span data-stu-id="b208f-104">Paths (GDI+)</span></span>

<span data-ttu-id="b208f-105">Контуры формируются путем объединения линий, прямоугольников и простых кривых.</span><span class="sxs-lookup"><span data-stu-id="b208f-105">Paths are formed by combining lines, rectangles, and simple curves.</span></span> <span data-ttu-id="b208f-106">Взпомним [о векторной графике](-gdiplus-overview-of-vector-graphics-about.md) , которые были признаны наиболее полезными для рисования изображений в следующих основных стандартных блоках.</span><span class="sxs-lookup"><span data-stu-id="b208f-106">Recall from the [Overview of Vector Graphics](-gdiplus-overview-of-vector-graphics-about.md) that the following basic building blocks have proven to be the most useful for drawing pictures.</span></span>

-   <span data-ttu-id="b208f-107">Линии</span><span class="sxs-lookup"><span data-stu-id="b208f-107">Lines</span></span>
-   <span data-ttu-id="b208f-108">Прямоугольники</span><span class="sxs-lookup"><span data-stu-id="b208f-108">Rectangles</span></span>
-   <span data-ttu-id="b208f-109">Многоточие</span><span class="sxs-lookup"><span data-stu-id="b208f-109">Ellipses</span></span>
-   <span data-ttu-id="b208f-110">Дуги</span><span class="sxs-lookup"><span data-stu-id="b208f-110">Arcs</span></span>
-   <span data-ttu-id="b208f-111">многоугольники</span><span class="sxs-lookup"><span data-stu-id="b208f-111">Polygons</span></span>
-   <span data-ttu-id="b208f-112">Фундаментальные сплайны</span><span class="sxs-lookup"><span data-stu-id="b208f-112">Cardinal splines</span></span>
-   <span data-ttu-id="b208f-113">Сплайны Безье</span><span class="sxs-lookup"><span data-stu-id="b208f-113">Bézier splines</span></span>

<span data-ttu-id="b208f-114">В Windows GDI+ объект [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) позволяет собрать последовательность этих стандартных блоков в единый блок.</span><span class="sxs-lookup"><span data-stu-id="b208f-114">In Windows GDI+, the [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object allows you to collect a sequence of these building blocks into a single unit.</span></span> <span data-ttu-id="b208f-115">Затем вся последовательность линий, прямоугольников, многоугольников и кривых может быть выведена одним вызовом метода [**Graphics::D равпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="b208f-115">The entire sequence of lines, rectangles, polygons, and curves can then be drawn with one call to the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="b208f-116">На следующем рисунке показан путь, созданный путем объединения линии, дуги, сплайна Безье и фундаментального сплайна.</span><span class="sxs-lookup"><span data-stu-id="b208f-116">The following illustration shows a path created by combining a line, an arc, a Bézier spline, and a cardinal spline.</span></span>

![Иллюстрация контура, объединяющего линию, дугу, сплайн Безье и фундаментальный сплайн](images/aboutgdip02-art14.png)

<span data-ttu-id="b208f-118">Класс [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) предоставляет следующие методы для создания последовательности элементов для рисования: [аддлине](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [аддректангле](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [аддарк](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [аддполигон](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [аддкурве](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (для элементов кардинала) и [аддбезиер](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="b208f-118">The [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) class provides the following methods for creating a sequence of items to be drawn: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (for cardinal splines), and [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span></span> <span data-ttu-id="b208f-119">Каждый из этих методов перегружен; то есть каждый метод имеет несколько вариантов с разными списками параметров.</span><span class="sxs-lookup"><span data-stu-id="b208f-119">Each of these methods is overloaded; that is, each method comes in several variations with different parameter lists.</span></span> <span data-ttu-id="b208f-120">Например, один из вариантов метода Аддлине получает четыре целых числа, а другой вариант метода Аддлине получает два объекта [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="b208f-120">For example, one variation of the AddLine method receives four integers, and another variation of the AddLine method receives two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span>

<span data-ttu-id="b208f-121">Методы добавления линий, прямоугольников и сплайнов Безье в путь содержат вспомогательные методы, которые добавляют в путь несколько элементов в одном вызове: [аддлинес](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [аддректанглес](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))и [аддбезиерс](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span><span class="sxs-lookup"><span data-stu-id="b208f-121">The methods for adding lines, rectangles, and Bézier splines to a path have plural companion methods that add several items to the path in a single call: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint)), and [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span></span> <span data-ttu-id="b208f-122">Кроме того, метод [аддкурве](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) имеет вспомогательный метод [аддклоседкурве](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), который добавляет замкнутую кривую к контуру.</span><span class="sxs-lookup"><span data-stu-id="b208f-122">Also, the [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) method has a companion method, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), that adds a closed curve to the path.</span></span>

<span data-ttu-id="b208f-123">Чтобы нарисовать контур, необходим объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) и объект [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="b208f-123">To draw a path, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="b208f-124">Объект **Graphics** предоставляет метод [**Graphics::D равпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) , а объект **Pen** сохраняет атрибуты пути, такие как толщина линии и цвет.</span><span class="sxs-lookup"><span data-stu-id="b208f-124">The **Graphics** object provides the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method, and the **Pen** object stores attributes of the path, such as line width and color.</span></span> <span data-ttu-id="b208f-125">Объект **GraphicsPath** сохраняет последовательность линий, прямоугольников и кривых, составляющих путь.</span><span class="sxs-lookup"><span data-stu-id="b208f-125">The **GraphicsPath** object stores the sequence of lines, rectangles, and curves that make up the path.</span></span> <span data-ttu-id="b208f-126">Адреса объекта **Pen** и объекта **GraphicsPath** передаются в виде аргументов в метод **Graphics::D равпас** .</span><span class="sxs-lookup"><span data-stu-id="b208f-126">The addresses of the **Pen** object and the **GraphicsPath** object are passed as arguments to the **Graphics::DrawPath** method.</span></span> <span data-ttu-id="b208f-127">В следующем примере рисуется контур, состоящий из линии, эллипса и сплайна Безье.</span><span class="sxs-lookup"><span data-stu-id="b208f-127">The following example draws a path that consists of a line, an ellipse, and a Bézier spline.</span></span>


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="b208f-128">На следующем рисунке показан путь.</span><span class="sxs-lookup"><span data-stu-id="b208f-128">The following illustration shows the path.</span></span>

![Иллюстрация контура, который состоит из линии, эллипса и сплайна Безье](images/aboutgdip02-art15.png)

<span data-ttu-id="b208f-130">Помимо добавления линий, прямоугольников и кривых к контуру, можно добавлять пути к контуру.</span><span class="sxs-lookup"><span data-stu-id="b208f-130">In addition to adding lines, rectangles, and curves to a path, you can add paths to a path.</span></span> <span data-ttu-id="b208f-131">Это позволяет объединять существующие пути для формирования больших и сложных путей.</span><span class="sxs-lookup"><span data-stu-id="b208f-131">This allows you to combine existing paths to form large, complex paths.</span></span> <span data-ttu-id="b208f-132">Следующий код добавляет **graphicsPath1** и **graphicsPath2** в **миграфикспас**.</span><span class="sxs-lookup"><span data-stu-id="b208f-132">The following code adds **graphicsPath1** and **graphicsPath2** to **myGraphicsPath**.</span></span> <span data-ttu-id="b208f-133">Второй параметр метода [**GraphicsPath:: аддпас**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) указывает, подключен ли добавленный путь к существующему пути.</span><span class="sxs-lookup"><span data-stu-id="b208f-133">The second parameter of the [**GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) method specifies whether the added path is connected to the existing path.</span></span>


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



<span data-ttu-id="b208f-134">В путь можно добавить еще два элемента: строки и круги.</span><span class="sxs-lookup"><span data-stu-id="b208f-134">There are two other items you can add to a path: strings and pies.</span></span> <span data-ttu-id="b208f-135">Круговая диаграмма является частью внутренней части эллипса.</span><span class="sxs-lookup"><span data-stu-id="b208f-135">A pie is a portion of the interior of an ellipse.</span></span> <span data-ttu-id="b208f-136">В следующем примере создается контур из дуги, фундаментального сплайна, строки и круговой диаграммы.</span><span class="sxs-lookup"><span data-stu-id="b208f-136">The following example creates a path from an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="b208f-137">На следующем рисунке показан путь.</span><span class="sxs-lookup"><span data-stu-id="b208f-137">The following illustration shows the path.</span></span> <span data-ttu-id="b208f-138">Обратите внимание, что путь не обязательно должен быть подключен; Дуга, фундаментальная кривая, строка и круговая диаграмма разделяются.</span><span class="sxs-lookup"><span data-stu-id="b208f-138">Note that a path does not have to be connected; the arc, cardinal spline, string, and pie are separated.</span></span>

![Иллюстрация пути, состоящие из отключенных линий: дуги, фундаментального сплайна, строки и круговой диаграммы](images/aboutgdip02-art16.png)

 

 



