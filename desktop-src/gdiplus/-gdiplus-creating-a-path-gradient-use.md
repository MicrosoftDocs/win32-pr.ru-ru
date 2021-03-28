---
description: Класс Пасградиентбруш позволяет настроить способ заливки фигуры с постепенно изменяющимися цветами.
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: Создание градиента контура
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558105"
---
# <a name="creating-a-path-gradient"></a><span data-ttu-id="46252-103">Создание градиента контура</span><span class="sxs-lookup"><span data-stu-id="46252-103">Creating a Path Gradient</span></span>

<span data-ttu-id="46252-104">Класс [**пасградиентбруш**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) позволяет настроить способ заливки фигуры с постепенно изменяющимися цветами.</span><span class="sxs-lookup"><span data-stu-id="46252-104">The [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class allows you to customize the way you fill a shape with gradually changing colors.</span></span> <span data-ttu-id="46252-105">Объект **пасградиентбруш** имеет Граничный контур и центральную точку.</span><span class="sxs-lookup"><span data-stu-id="46252-105">A **PathGradientBrush** object has a boundary path and a center point.</span></span> <span data-ttu-id="46252-106">Можно указать один цвет для центральной точки и другой цвет для границы.</span><span class="sxs-lookup"><span data-stu-id="46252-106">You can specify one color for the center point and another color for the boundary.</span></span> <span data-ttu-id="46252-107">Можно также указать отдельные цвета для каждой из нескольких точек на границе.</span><span class="sxs-lookup"><span data-stu-id="46252-107">You can also specify separate colors for each of several points along the boundary.</span></span>

> [!Note]  
> <span data-ttu-id="46252-108">В GDI+ путь представляет собой последовательность линий и кривых, обслуживаемых объектом [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="46252-108">In GDI+, a path is a sequence of lines and curves maintained by a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="46252-109">Дополнительные сведения о путях GDI+ см. в разделе [paths](-gdiplus-paths-about.md) and [конструировать and Drawing paths](-gdiplus-constructing-and-drawing-paths-use.md).</span><span class="sxs-lookup"><span data-stu-id="46252-109">For more information about GDI+ paths, see [Paths](-gdiplus-paths-about.md) and [Constructing and Drawing Paths](-gdiplus-constructing-and-drawing-paths-use.md).</span></span>

 

<span data-ttu-id="46252-110">В следующем примере заливка эллипса осуществляется с помощью кисти градиента вдоль пути.</span><span class="sxs-lookup"><span data-stu-id="46252-110">The following example fills an ellipse with a path gradient brush.</span></span> <span data-ttu-id="46252-111">Центральная цвет устанавливается синим цветом, а цвет границы — голубым.</span><span class="sxs-lookup"><span data-stu-id="46252-111">The center color is set to blue and the boundary color is set to aqua.</span></span>


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



<span data-ttu-id="46252-112">На следующем рисунке показан закрашенный эллипс.</span><span class="sxs-lookup"><span data-stu-id="46252-112">The following illustration shows the filled ellipse.</span></span>

![Иллюстрация с эллипсом с градиентной заливкой](images/pathgradient1.png)

<span data-ttu-id="46252-114">По умолчанию кисть градиента контура не выходит за границы пути.</span><span class="sxs-lookup"><span data-stu-id="46252-114">By default, a path gradient brush does not extend outside the boundary of the path.</span></span> <span data-ttu-id="46252-115">При использовании кисти градиента вдоль пути для заливки фигуры, выходящей за пределы контура, область экрана за пределами контура не будет заполнена.</span><span class="sxs-lookup"><span data-stu-id="46252-115">If you use the path gradient brush to fill a shape that extends beyond the boundary of the path, the area of the screen outside the path will not be filled.</span></span> <span data-ttu-id="46252-116">На следующем рисунке показано, что происходит при изменении вызова [**Graphics:: филлеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) в предыдущем коде на `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .</span><span class="sxs-lookup"><span data-stu-id="46252-116">The following illustration shows what happens if you change the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) call in the preceding code to `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)`.</span></span>

![Иллюстрация, демонстрирующая Горизонтальный срез предыдущего эллипса](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a><span data-ttu-id="46252-118">Указание точек на границе</span><span class="sxs-lookup"><span data-stu-id="46252-118">Specifying Points on the Boundary</span></span>

<span data-ttu-id="46252-119">В следующем примере кисть градиента контура строится на основе траектории в форме звезды.</span><span class="sxs-lookup"><span data-stu-id="46252-119">The following example constructs a path gradient brush from a star-shaped path.</span></span> <span data-ttu-id="46252-120">Код вызывает метод [**пасградиентбруш:: сетцентерколор**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) , чтобы задать красный цвет в центроид звезды.</span><span class="sxs-lookup"><span data-stu-id="46252-120">The code calls the [**PathGradientBrush::SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) method to set the color at the centroid of the star to red.</span></span> <span data-ttu-id="46252-121">Затем код вызывает метод [**пасградиентбруш:: сетсурраундколорс**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) для указания различных цветов (хранящихся в массиве [**Colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) ) в отдельных точках в массиве [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="46252-121">Then the code calls the [**PathGradientBrush::SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) method to specify various colors (stored in the [**colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) array) at the individual points in the [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) array.</span></span> <span data-ttu-id="46252-122">Окончательный оператор Code заполняет траекторию в форме звезды с помощью кисти градиента вдоль пути.</span><span class="sxs-lookup"><span data-stu-id="46252-122">The final code statement fills the star-shaped path with the path gradient brush.</span></span>


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0),    Point(100, 50), 
                  Point(150, 50),  Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150),   Point(37, 75), 
                  Point(0, 50),    Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="46252-123">На следующем рисунке показана заполненная звезда.</span><span class="sxs-lookup"><span data-stu-id="46252-123">The following illustration shows the filled star.</span></span>

![Иллюстрация, показывающая пять точек звездочки, заполняемые от красного в центре к различным цветам в каждой точке звезды](images/pathgradient3.png)

<span data-ttu-id="46252-125">В следующем примере создается кисть градиента контура на основе массива точек.</span><span class="sxs-lookup"><span data-stu-id="46252-125">The following example constructs a path gradient brush based on an array of points.</span></span> <span data-ttu-id="46252-126">Каждому из пяти точек в массиве назначается цвет.</span><span class="sxs-lookup"><span data-stu-id="46252-126">A color is assigned to each of the five points in the array.</span></span> <span data-ttu-id="46252-127">Если нужно соединить пять точек по прямым линиям, вы получите пять-сторонний многоугольник.</span><span class="sxs-lookup"><span data-stu-id="46252-127">If you were to connect the five points by straight lines, you would get a five-sided polygon.</span></span> <span data-ttu-id="46252-128">Цвет также назначается центру (центроид) этого многоугольника — в этом примере центр (80, 75) имеет значение белого.</span><span class="sxs-lookup"><span data-stu-id="46252-128">A color is also assigned to the center (centroid) of that polygon — in this example, the center (80, 75) is set to white.</span></span> <span data-ttu-id="46252-129">Последняя инструкция Code в примере заполняет прямоугольник с помощью кисти градиента вдоль пути.</span><span class="sxs-lookup"><span data-stu-id="46252-129">The final code statement in the example fills a rectangle with the path gradient brush.</span></span>

<span data-ttu-id="46252-130">Цвет, используемый для заполнения прямоугольника, — белый в (80, 75), и изменения постепенно меняются по мере движения от (80, 75) к точкам в массиве.</span><span class="sxs-lookup"><span data-stu-id="46252-130">The color used to fill the rectangle is white at (80, 75) and changes gradually as you move away from (80, 75) toward the points in the array.</span></span> <span data-ttu-id="46252-131">Например, при перемещении от (80, 75) к (0, 0) цвет меняется постепенно от белого к красному, а при перемещении от (80, 75) к (160, 0) цвет постепенно меняется от белого к зеленому.</span><span class="sxs-lookup"><span data-stu-id="46252-131">For example, as you move from (80, 75) to (0, 0), the color changes gradually from white to red, and as you move from (80, 75) to (160, 0), the color changes gradually from white to green.</span></span>


```
// Construct a path gradient brush based on an array of points.
PointF ptsF[] = {PointF(0.0f, 0.0f), 
                 PointF(160.0f, 0.0f), 
                 PointF(160.0f, 200.0f),
                 PointF(80.0f, 150.0f),
                 PointF(0.0f, 200.0f)};

PathGradientBrush pBrush(ptsF, 5);

// An array of five points was used to construct the path gradient
// brush. Set the color of each point in that array.
Color colors[] = {Color(255, 255, 0, 0),  // (0, 0) red
                  Color(255, 0, 255, 0),  // (160, 0) green
                  Color(255, 0, 255, 0),  // (160, 200) green
                  Color(255, 0, 0, 255),  // (80, 150) blue
                  Color(255, 255, 0, 0)}; // (0, 200) red

int count = 5;
pBrush.SetSurroundColors(colors, &count);

// Set the center color to white.
pBrush.SetCenterColor(Color(255, 255, 255, 255));

// Use the path gradient brush to fill a rectangle.
graphics.FillRectangle(&pBrush, Rect(0, 0, 180, 220));
```



<span data-ttu-id="46252-132">Обратите внимание, что в приведенном выше коде отсутствует объект [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="46252-132">Note that there is no [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object in the preceding code.</span></span> <span data-ttu-id="46252-133">Определенный конструктор [**пасградиентбруш**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) в примере получает указатель на массив точек, но не требует объект **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="46252-133">The particular [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) constructor in the example receives a pointer to an array of points but does not require a **GraphicsPath** object.</span></span> <span data-ttu-id="46252-134">Кроме того, обратите внимание, что кисть градиента вдоль пути используется для заливки прямоугольника, а не контура.</span><span class="sxs-lookup"><span data-stu-id="46252-134">Also, note that the path gradient brush is used to fill a rectangle, not a path.</span></span> <span data-ttu-id="46252-135">Прямоугольник больше, чем путь, используемый для определения кисти, поэтому часть прямоугольника не закрашивается кистью.</span><span class="sxs-lookup"><span data-stu-id="46252-135">The rectangle is larger than the path used to define the brush, so some of the rectangle is not painted by the brush.</span></span> <span data-ttu-id="46252-136">На следующем рисунке показан прямоугольник (пунктирная линия) и часть прямоугольника, закрашенная кистью градиента вдоль пути.</span><span class="sxs-lookup"><span data-stu-id="46252-136">The following illustration shows the rectangle (dotted line) and the portion of the rectangle painted by the path gradient brush.</span></span>

![Иллюстрация, демонстрирующая прямоугольник, ограниченный пунктирной линией, частично окрашенный многоцветным градиентом](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a><span data-ttu-id="46252-138">Настройка градиента контура</span><span class="sxs-lookup"><span data-stu-id="46252-138">Customizing a Path Gradient</span></span>

<span data-ttu-id="46252-139">Одним из способов настройки кисти градиента контура является установка ее фокусного масштабирования.</span><span class="sxs-lookup"><span data-stu-id="46252-139">One way to customize a path gradient brush is to set its focus scales.</span></span> <span data-ttu-id="46252-140">Масштабирование фокуса определяет внутренний путь, который находится внутри основного пути.</span><span class="sxs-lookup"><span data-stu-id="46252-140">The focus scales specify an inner path that lies inside the main path.</span></span> <span data-ttu-id="46252-141">Центральный цвет отображается везде внутри этого внутреннего пути, а не только в центральной точке.</span><span class="sxs-lookup"><span data-stu-id="46252-141">The center color is displayed everywhere inside that inner path rather than only at the center point.</span></span> <span data-ttu-id="46252-142">Чтобы задать масштаб фокуса кисти градиента контура, вызовите метод [**пасградиентбруш:: сетфокусскалес**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) .</span><span class="sxs-lookup"><span data-stu-id="46252-142">To set the focus scales of a path gradient brush, call the [**PathGradientBrush::SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) method.</span></span>

<span data-ttu-id="46252-143">В следующем примере создается кисть градиента контура на основе эллиптического пути.</span><span class="sxs-lookup"><span data-stu-id="46252-143">The following example creates a path gradient brush based on an elliptical path.</span></span> <span data-ttu-id="46252-144">Код устанавливает синий цвет границы, устанавливает цвет центрального цвета в голубой, а затем использует кисть градиента вдоль пути для заполнения эллиптического контура.</span><span class="sxs-lookup"><span data-stu-id="46252-144">The code sets the boundary color to blue, sets the center color to aqua, and then uses the path gradient brush to fill the elliptical path.</span></span>

<span data-ttu-id="46252-145">Далее код задает масштабное масштабирование кисти градиента вдоль пути.</span><span class="sxs-lookup"><span data-stu-id="46252-145">Next the code sets the focus scales of the path gradient brush.</span></span> <span data-ttu-id="46252-146">Масштаб фокуса x устанавливается равным 0,3, а масштаб фокуса по оси y устанавливается равным 0,8.</span><span class="sxs-lookup"><span data-stu-id="46252-146">The x focus scale is set to 0.3, and the y focus scale is set to 0.8.</span></span> <span data-ttu-id="46252-147">Код вызывает метод [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , чтобы последующий вызов метода [**Graphics:: филлпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) заполнил эллипс, расположенный справа от первого эллипса.</span><span class="sxs-lookup"><span data-stu-id="46252-147">The code calls the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills an ellipse that sits to the right of the first ellipse.</span></span>

<span data-ttu-id="46252-148">Чтобы увидеть результат масштабирования фокуса, представьте себе маленький эллипс, который использует его центр с основным эллипсом.</span><span class="sxs-lookup"><span data-stu-id="46252-148">To see the effect of the focus scales, imagine a small ellipse that shares its center with the main ellipse.</span></span> <span data-ttu-id="46252-149">Маленький (внутренний) эллипс — это основной эллипс (по центру) по горизонтали на 0,3 и вертикальный коэффициент, равный 0,8.</span><span class="sxs-lookup"><span data-stu-id="46252-149">The small (inner) ellipse is the main ellipse scaled (about its center) horizontally by a factor of 0.3 and vertically by a factor of 0.8.</span></span> <span data-ttu-id="46252-150">При переходе от границы внешнего эллипса к границе внутреннего эллипса цвет постепенно меняется от синего к голубому.</span><span class="sxs-lookup"><span data-stu-id="46252-150">As you move from the boundary of the outer ellipse to the boundary of the inner ellipse, the color changes gradually from blue to aqua.</span></span> <span data-ttu-id="46252-151">При переходе от границы внутреннего эллипса к общему центру цвет остается голубым.</span><span class="sxs-lookup"><span data-stu-id="46252-151">As you move from the boundary of the inner ellipse to the shared center, the color remains aqua.</span></span>


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 200, 100);

// Create a path gradient brush based on the elliptical path.
PathGradientBrush pthGrBrush(&path);
pthGrBrush.SetGammaCorrection(TRUE);

// Set the color along the entire boundary to blue.
Color color(Color(255, 0, 0, 255));
INT num = 1;
pthGrBrush.SetSurroundColors(&color, &num);

// Set the center color to aqua.
pthGrBrush.SetCenterColor(Color(255, 0, 255, 255));
 
// Use the path gradient brush to fill the ellipse. 
graphics.FillPath(&pthGrBrush, &path);

// Set the focus scales for the path gradient brush.
pthGrBrush.SetFocusScales(0.3f, 0.8f);

// Use the path gradient brush to fill the ellipse again.
// Show this filled ellipse to the right of the first filled ellipse.
graphics.TranslateTransform(220.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="46252-152">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="46252-152">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="46252-153">Эллипс слева имеет голубой цвет только в центральной точке.</span><span class="sxs-lookup"><span data-stu-id="46252-153">The ellipse on the left is aqua only at the center point.</span></span> <span data-ttu-id="46252-154">Эллипс справа — это голубой цвет везде внутри внутреннего пути.</span><span class="sxs-lookup"><span data-stu-id="46252-154">The ellipse on the right is aqua everywhere inside the inner path.</span></span>

![Иллюстрация, демонстрирующая два эллипса, которые закрашены от голубого цвета к синему: первый имеет очень маленький голубой цвет; второй имеет гораздо больше](images/focusscales1.png)

<span data-ttu-id="46252-156">Другой способ настройки кисти градиента контура заключается в том, чтобы указать массив предустановленных цветов и массив позиций интерполяции.</span><span class="sxs-lookup"><span data-stu-id="46252-156">Another way to customize a path gradient brush is to specify an array of preset colors and an array of interpolation positions.</span></span>

<span data-ttu-id="46252-157">В следующем примере создается кисть градиента контура на основе треугольника.</span><span class="sxs-lookup"><span data-stu-id="46252-157">The following example creates a path gradient brush based on a triangle.</span></span> <span data-ttu-id="46252-158">Код вызывает метод [**пасградиентбруш:: сетинтерполатионколорс**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) кисти градиента вдоль пути, чтобы указать массив цветов интерполяции (темно-зеленый, голубой, синий) и массив позиций интерполяции (0, 0,25, 1).</span><span class="sxs-lookup"><span data-stu-id="46252-158">The code calls the [**PathGradientBrush::SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) method of the path gradient brush to specify an array of interpolation colors (dark green, aqua, blue) and an array of interpolation positions (0, 0.25, 1).</span></span> <span data-ttu-id="46252-159">При переходе от границы треугольника к центральной точке цвет меняется постепенно с темно-зеленого на голубой, а затем с голубого на синий.</span><span class="sxs-lookup"><span data-stu-id="46252-159">As you move from the boundary of the triangle to the center point, the color changes gradually from dark green to aqua and then from aqua to blue.</span></span> <span data-ttu-id="46252-160">Изменение с темно-зеленого на голубой происходит в 25% от темно-зеленого до синего.</span><span class="sxs-lookup"><span data-stu-id="46252-160">The change from dark green to aqua happens in 25 percent of the distance from dark green to blue.</span></span>


```
// Vertices of the triangle
Point points[] = {Point(100, 0), 
                  Point(200, 200), 
                  Point(0, 200)};

// No GraphicsPath object is created. The PathGradient
// brush is constructed directly from the array of points.
PathGradientBrush pthGrBrush(points, 3);

Color presetColors[] = {
   Color(255, 0, 128, 0),    // Dark green
   Color(255, 0, 255, 255),  // Aqua
   Color(255, 0, 0, 255)};   // Blue

REAL interpPositions[] = {
   0.0f,   // Dark green is at the boundary of the triangle.
   0.25f,  // Aqua is 25 percent of the way from the boundary
           // to the center point.
   1.0f};  // Blue is at the center point.
                  
pthGrBrush.SetInterpolationColors(presetColors, interpPositions, 3);

// Fill a rectangle that is larger than the triangle
// specified in the Point array. The portion of the
// rectangle outside the triangle will not be painted.
graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);
```



<span data-ttu-id="46252-161">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="46252-161">The following illustration shows the output of the preceding code.</span></span>

![Иллюстрация, на которой показан треугольник, который переводится от синего в центре к голубому цвету на краях](images/pathgradient4.png)

## <a name="setting-the-center-point"></a><span data-ttu-id="46252-163">Настройка центральной точки</span><span class="sxs-lookup"><span data-stu-id="46252-163">Setting the Center Point</span></span>

<span data-ttu-id="46252-164">По умолчанию Центральная точка кисти градиента контура находится в центроид пути, используемого для создания кисти.</span><span class="sxs-lookup"><span data-stu-id="46252-164">By default, the center point of a path gradient brush is at the centroid of the path used to construct the brush.</span></span> <span data-ttu-id="46252-165">Расположение центральной точки можно изменить, вызвав метод [**пасградиентбруш:: сетцентерпоинт**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) класса [**пасградиентбруш**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="46252-165">You can change the location of the center point by calling the [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) method of the [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class.</span></span>

<span data-ttu-id="46252-166">В следующем примере создается кисть градиента контура на основе эллипса.</span><span class="sxs-lookup"><span data-stu-id="46252-166">The following example creates a path gradient brush based on an ellipse.</span></span> <span data-ttu-id="46252-167">Центр эллипса находится в точке (70, 35), но Центральная точка кисти градиента контура имеет значение (120, 40).</span><span class="sxs-lookup"><span data-stu-id="46252-167">The center of the ellipse is at (70, 35), but the center point of the path gradient brush is set to (120, 40).</span></span>


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the center point to a location that is not the centroid of the path.
pthGrBrush.SetCenterPoint(Point(120, 40));

// Set the color at the center point to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



<span data-ttu-id="46252-168">На следующем рисунке показан закрашенный эллипс и Центральная точка кисти градиента контура.</span><span class="sxs-lookup"><span data-stu-id="46252-168">The following illustration shows the filled ellipse and the center point of the path gradient brush.</span></span>

![Иллюстрация, на которой показан эллипс, который заполняется от синего к голубому от центральной точки рядом с одним концом](images/pathgradient5.png)

<span data-ttu-id="46252-170">Можно задать центральную точку кисти градиента контура, расположенную за пределами пути, который использовался для создания кисти.</span><span class="sxs-lookup"><span data-stu-id="46252-170">You can set the center point of a path gradient brush to a location outside the path that was used to construct the brush.</span></span> <span data-ttu-id="46252-171">В приведенном выше коде, если вы замените вызов [**пасградиентбруш:: сетцентерпоинт**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) на `pthGrBrush.SetCenterPoint(Point(145, 35))` , вы получите следующий результат.</span><span class="sxs-lookup"><span data-stu-id="46252-171">In the preceding code, if you replace the call to [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) with `pthGrBrush.SetCenterPoint(Point(145, 35))`, you will get the following result.</span></span>

![Иллюстрация, на которой показан эллипс, который заполняется от красного к желтому от центральной точки, находящегося за границей эллипса](images/pathgradient6.png)

<span data-ttu-id="46252-173">На предыдущем рисунке точки в дальней правой части эллипса не являются чисто синими (хотя они очень близки).</span><span class="sxs-lookup"><span data-stu-id="46252-173">In the preceding illustration, the points at the far right of the ellipse are not pure blue (although they are very close).</span></span> <span data-ttu-id="46252-174">Цвета в градиенте размещаются так, как если бы заливка была разрешена к точке (145, 35), цвет будет достигать чистого синего (0, 0, 255).</span><span class="sxs-lookup"><span data-stu-id="46252-174">The colors in the gradient are positioned as if the fill had been allowed to reach the point (145, 35), the color would have reached pure blue (0, 0, 255).</span></span> <span data-ttu-id="46252-175">Но заливка никогда не достигает (145, 35), так как кисть градиента контура рисует только внутри ее контура.</span><span class="sxs-lookup"><span data-stu-id="46252-175">But the fill never reaches (145, 35) because a path gradient brush paints only inside its path.</span></span>

 

 
