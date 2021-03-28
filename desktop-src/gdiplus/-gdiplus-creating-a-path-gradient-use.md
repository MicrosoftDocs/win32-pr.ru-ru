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
# <a name="creating-a-path-gradient"></a>Создание градиента контура

Класс [**пасградиентбруш**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) позволяет настроить способ заливки фигуры с постепенно изменяющимися цветами. Объект **пасградиентбруш** имеет Граничный контур и центральную точку. Можно указать один цвет для центральной точки и другой цвет для границы. Можно также указать отдельные цвета для каждой из нескольких точек на границе.

> [!Note]  
> В GDI+ путь представляет собой последовательность линий и кривых, обслуживаемых объектом [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . Дополнительные сведения о путях GDI+ см. в разделе [paths](-gdiplus-paths-about.md) and [конструировать and Drawing paths](-gdiplus-constructing-and-drawing-paths-use.md).

 

В следующем примере заливка эллипса осуществляется с помощью кисти градиента вдоль пути. Центральная цвет устанавливается синим цветом, а цвет границы — голубым.


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



На следующем рисунке показан закрашенный эллипс.

![Иллюстрация с эллипсом с градиентной заливкой](images/pathgradient1.png)

По умолчанию кисть градиента контура не выходит за границы пути. При использовании кисти градиента вдоль пути для заливки фигуры, выходящей за пределы контура, область экрана за пределами контура не будет заполнена. На следующем рисунке показано, что происходит при изменении вызова [**Graphics:: филлеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) в предыдущем коде на `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .

![Иллюстрация, демонстрирующая Горизонтальный срез предыдущего эллипса](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a>Указание точек на границе

В следующем примере кисть градиента контура строится на основе траектории в форме звезды. Код вызывает метод [**пасградиентбруш:: сетцентерколор**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) , чтобы задать красный цвет в центроид звезды. Затем код вызывает метод [**пасградиентбруш:: сетсурраундколорс**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) для указания различных цветов (хранящихся в массиве [**Colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) ) в отдельных точках в массиве [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . Окончательный оператор Code заполняет траекторию в форме звезды с помощью кисти градиента вдоль пути.


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



На следующем рисунке показана заполненная звезда.

![Иллюстрация, показывающая пять точек звездочки, заполняемые от красного в центре к различным цветам в каждой точке звезды](images/pathgradient3.png)

В следующем примере создается кисть градиента контура на основе массива точек. Каждому из пяти точек в массиве назначается цвет. Если нужно соединить пять точек по прямым линиям, вы получите пять-сторонний многоугольник. Цвет также назначается центру (центроид) этого многоугольника — в этом примере центр (80, 75) имеет значение белого. Последняя инструкция Code в примере заполняет прямоугольник с помощью кисти градиента вдоль пути.

Цвет, используемый для заполнения прямоугольника, — белый в (80, 75), и изменения постепенно меняются по мере движения от (80, 75) к точкам в массиве. Например, при перемещении от (80, 75) к (0, 0) цвет меняется постепенно от белого к красному, а при перемещении от (80, 75) к (160, 0) цвет постепенно меняется от белого к зеленому.


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



Обратите внимание, что в приведенном выше коде отсутствует объект [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . Определенный конструктор [**пасградиентбруш**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) в примере получает указатель на массив точек, но не требует объект **GraphicsPath** . Кроме того, обратите внимание, что кисть градиента вдоль пути используется для заливки прямоугольника, а не контура. Прямоугольник больше, чем путь, используемый для определения кисти, поэтому часть прямоугольника не закрашивается кистью. На следующем рисунке показан прямоугольник (пунктирная линия) и часть прямоугольника, закрашенная кистью градиента вдоль пути.

![Иллюстрация, демонстрирующая прямоугольник, ограниченный пунктирной линией, частично окрашенный многоцветным градиентом](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a>Настройка градиента контура

Одним из способов настройки кисти градиента контура является установка ее фокусного масштабирования. Масштабирование фокуса определяет внутренний путь, который находится внутри основного пути. Центральный цвет отображается везде внутри этого внутреннего пути, а не только в центральной точке. Чтобы задать масштаб фокуса кисти градиента контура, вызовите метод [**пасградиентбруш:: сетфокусскалес**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) .

В следующем примере создается кисть градиента контура на основе эллиптического пути. Код устанавливает синий цвет границы, устанавливает цвет центрального цвета в голубой, а затем использует кисть градиента вдоль пути для заполнения эллиптического контура.

Далее код задает масштабное масштабирование кисти градиента вдоль пути. Масштаб фокуса x устанавливается равным 0,3, а масштаб фокуса по оси y устанавливается равным 0,8. Код вызывает метод [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , чтобы последующий вызов метода [**Graphics:: филлпас**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) заполнил эллипс, расположенный справа от первого эллипса.

Чтобы увидеть результат масштабирования фокуса, представьте себе маленький эллипс, который использует его центр с основным эллипсом. Маленький (внутренний) эллипс — это основной эллипс (по центру) по горизонтали на 0,3 и вертикальный коэффициент, равный 0,8. При переходе от границы внешнего эллипса к границе внутреннего эллипса цвет постепенно меняется от синего к голубому. При переходе от границы внутреннего эллипса к общему центру цвет остается голубым.


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



На следующем рисунке показаны выходные данные предыдущего кода. Эллипс слева имеет голубой цвет только в центральной точке. Эллипс справа — это голубой цвет везде внутри внутреннего пути.

![Иллюстрация, демонстрирующая два эллипса, которые закрашены от голубого цвета к синему: первый имеет очень маленький голубой цвет; второй имеет гораздо больше](images/focusscales1.png)

Другой способ настройки кисти градиента контура заключается в том, чтобы указать массив предустановленных цветов и массив позиций интерполяции.

В следующем примере создается кисть градиента контура на основе треугольника. Код вызывает метод [**пасградиентбруш:: сетинтерполатионколорс**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) кисти градиента вдоль пути, чтобы указать массив цветов интерполяции (темно-зеленый, голубой, синий) и массив позиций интерполяции (0, 0,25, 1). При переходе от границы треугольника к центральной точке цвет меняется постепенно с темно-зеленого на голубой, а затем с голубого на синий. Изменение с темно-зеленого на голубой происходит в 25% от темно-зеленого до синего.


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



На следующем рисунке показаны выходные данные предыдущего кода.

![Иллюстрация, на которой показан треугольник, который переводится от синего в центре к голубому цвету на краях](images/pathgradient4.png)

## <a name="setting-the-center-point"></a>Настройка центральной точки

По умолчанию Центральная точка кисти градиента контура находится в центроид пути, используемого для создания кисти. Расположение центральной точки можно изменить, вызвав метод [**пасградиентбруш:: сетцентерпоинт**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) класса [**пасградиентбруш**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) .

В следующем примере создается кисть градиента контура на основе эллипса. Центр эллипса находится в точке (70, 35), но Центральная точка кисти градиента контура имеет значение (120, 40).


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



На следующем рисунке показан закрашенный эллипс и Центральная точка кисти градиента контура.

![Иллюстрация, на которой показан эллипс, который заполняется от синего к голубому от центральной точки рядом с одним концом](images/pathgradient5.png)

Можно задать центральную точку кисти градиента контура, расположенную за пределами пути, который использовался для создания кисти. В приведенном выше коде, если вы замените вызов [**пасградиентбруш:: сетцентерпоинт**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) на `pthGrBrush.SetCenterPoint(Point(145, 35))` , вы получите следующий результат.

![Иллюстрация, на которой показан эллипс, который заполняется от красного к желтому от центральной точки, находящегося за границей эллипса](images/pathgradient6.png)

На предыдущем рисунке точки в дальней правой части эллипса не являются чисто синими (хотя они очень близки). Цвета в градиенте размещаются так, как если бы заливка была разрешена к точке (145, 35), цвет будет достигать чистого синего (0, 0, 255). Но заливка никогда не достигает (145, 35), так как кисть градиента контура рисует только внутри ее контура.

 

 
