---
description: 'В Windows GDI+ используются три пространства координат: мир, страница и устройство.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Типы систем координат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120629"
---
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="cac50-103">Типы систем координат</span><span class="sxs-lookup"><span data-stu-id="cac50-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="cac50-104">В Windows GDI+ используются три пространства координат: мир, страница и устройство.</span><span class="sxs-lookup"><span data-stu-id="cac50-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="cac50-105">При выполнении вызова `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` точки, передаваемые в [**Graphics::D метод равлине**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) — (0, 0) и (160, 80) — находятся в мировом пространстве координат.</span><span class="sxs-lookup"><span data-stu-id="cac50-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="cac50-106">До того, как интерфейс GDI+ может нарисовать линию на экране, координаты проходят через последовательность преобразований.</span><span class="sxs-lookup"><span data-stu-id="cac50-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="cac50-107">Одно преобразование преобразует координаты мира в координаты страницы, а другое преобразование преобразует координаты страницы в координаты устройства.</span><span class="sxs-lookup"><span data-stu-id="cac50-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="cac50-108">Предположим, что вы хотите работать с системой координат, имеющей свою точку в тексте клиентской области, а не в левом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="cac50-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="cac50-109">Предположим, например, что вы хотите, чтобы источник был 100 пикселей от левого края клиентской области и 50 пикселей от верхнего края клиентской области.</span><span class="sxs-lookup"><span data-stu-id="cac50-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="cac50-110">На следующем рисунке показана такая система координат.</span><span class="sxs-lookup"><span data-stu-id="cac50-110">The following illustration shows such a coordinate system.</span></span>

![снимок экрана окна, содержащего метки осей координат](images/aboutgdip05-art01.png)

<span data-ttu-id="cac50-112">Выполнив вызов `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , вы получите строку, показанную на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="cac50-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![снимок экрана предыдущего окна, но со синей линией, расширяющейся по диагонали от начала координат](images/aboutgdip05-art02.png)

<span data-ttu-id="cac50-114">Ниже приведены координаты конечных точек линии в трех координатных пространствах.</span><span class="sxs-lookup"><span data-stu-id="cac50-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



| <span data-ttu-id="cac50-115">Пробел</span><span class="sxs-lookup"><span data-stu-id="cac50-115">Space</span></span>       |  <span data-ttu-id="cac50-116">Координаты конечной точки</span><span class="sxs-lookup"><span data-stu-id="cac50-116">Endpoint coordinates</span></span>                       |
|--------|-------------------------|
| <span data-ttu-id="cac50-117">World</span><span class="sxs-lookup"><span data-stu-id="cac50-117">World</span></span>  | <span data-ttu-id="cac50-118">(от 0 до 0) до (160, 80)</span><span class="sxs-lookup"><span data-stu-id="cac50-118">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="cac50-119">Страница</span><span class="sxs-lookup"><span data-stu-id="cac50-119">Page</span></span>   | <span data-ttu-id="cac50-120">(100, 50) в (260, 130)</span><span class="sxs-lookup"><span data-stu-id="cac50-120">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="cac50-121">Устройство</span><span class="sxs-lookup"><span data-stu-id="cac50-121">Device</span></span> | <span data-ttu-id="cac50-122">(100, 50) в (260, 130)</span><span class="sxs-lookup"><span data-stu-id="cac50-122">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="cac50-123">Обратите внимание, что координатное пространство страницы имеет свой источник в левом верхнем углу клиентской области. Это всегда будет так.</span><span class="sxs-lookup"><span data-stu-id="cac50-123">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="cac50-124">Также обратите внимание, что поскольку единицей измерения является пиксель, координаты устройства совпадают с координатами страницы.</span><span class="sxs-lookup"><span data-stu-id="cac50-124">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="cac50-125">Если задать для единицы измерения значение, отличное от пикселей (например, дюймы), то координаты устройства будут отличаться от координат на странице.</span><span class="sxs-lookup"><span data-stu-id="cac50-125">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="cac50-126">Преобразование, которое сопоставляет мировые координаты с координатами страницы, называется *мировым преобразованием* и поддерживается [**графическим**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объектом.</span><span class="sxs-lookup"><span data-stu-id="cac50-126">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="cac50-127">В предыдущем примере преобразование «мир» представляет собой единицы перевода 100 в направлении x и 50 единиц по оси y.</span><span class="sxs-lookup"><span data-stu-id="cac50-127">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="cac50-128">В следующем примере задается универсальное преобразование **графического** объекта, а затем этот **графический** объект используется для отрисовки линии, показанной на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="cac50-128">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="cac50-129">Преобразование, которое сопоставляет координаты страницы с координатами устройства, называется *преобразованием «страница*».</span><span class="sxs-lookup"><span data-stu-id="cac50-129">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="cac50-130">Класс [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) предоставляет четыре метода для управления и проверки преобразования страницы: [**Graphics:: сетпажеунит**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics:: Жетпажеунит**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics:: сетпажескале**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)и [**Graphics:: жетпажескале**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span><span class="sxs-lookup"><span data-stu-id="cac50-130">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="cac50-131">Класс **Graphics** также предоставляет два метода, [**Graphics:: жетдпикс**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) и [**Graphics:: жетдпий**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), для проверки горизонтальной и вертикальной точек на дюйм устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="cac50-131">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="cac50-132">Для указания единицы измерения можно использовать метод [**Graphics:: сетпажеунит**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="cac50-132">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="cac50-133">В следующем примере рисуется линия от (0,0) до (2, 1), где точка (2, 1) имеет значение 2 дюйма справа и 1 дюйм вниз от точки (0, 0).</span><span class="sxs-lookup"><span data-stu-id="cac50-133">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="cac50-134">Если вы не укажете толщину пера при создании пера, в предыдущем примере будет нарисована линия шириной в один дюйм.</span><span class="sxs-lookup"><span data-stu-id="cac50-134">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="cac50-135">Можно указать ширину пера во втором аргументе конструктора [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) :</span><span class="sxs-lookup"><span data-stu-id="cac50-135">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="cac50-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="cac50-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="cac50-137">Если предполагается, что устройство вывода имеет 96 точек на дюйм в горизонтальном направлении и 96 точек на дюйм в вертикальном направлении, конечные точки строки в предыдущем примере имеют следующие координаты в трех координатных пространствах:</span><span class="sxs-lookup"><span data-stu-id="cac50-137">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="cac50-138">Пробел</span><span class="sxs-lookup"><span data-stu-id="cac50-138">Space</span></span>       | <span data-ttu-id="cac50-139">Координаты конечной точки</span><span class="sxs-lookup"><span data-stu-id="cac50-139">Endpoint coordinates</span></span>                    |
|--------|---------------------|
| <span data-ttu-id="cac50-140">World</span><span class="sxs-lookup"><span data-stu-id="cac50-140">World</span></span>  | <span data-ttu-id="cac50-141">(0, 0) на (2, 1)</span><span class="sxs-lookup"><span data-stu-id="cac50-141">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="cac50-142">Страница</span><span class="sxs-lookup"><span data-stu-id="cac50-142">Page</span></span>   | <span data-ttu-id="cac50-143">(0, 0) на (2, 1)</span><span class="sxs-lookup"><span data-stu-id="cac50-143">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="cac50-144">Устройство</span><span class="sxs-lookup"><span data-stu-id="cac50-144">Device</span></span> | <span data-ttu-id="cac50-145">(0, 0, до (192, 96)</span><span class="sxs-lookup"><span data-stu-id="cac50-145">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="cac50-146">Для получения различных эффектов можно сочетать преобразования «мир» и «страница».</span><span class="sxs-lookup"><span data-stu-id="cac50-146">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="cac50-147">Например, предположим, что вы хотите использовать дюйма в качестве единицы измерения и хотите, чтобы источник координат был 2 дюйма от левого края клиентской области и 1/2 дюйма от верхней части клиентской области.</span><span class="sxs-lookup"><span data-stu-id="cac50-147">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="cac50-148">В следующем примере настраивается преобразование «мир» и «страница» [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта, после чего рисуется строка от (0, 0) до (2, 1).</span><span class="sxs-lookup"><span data-stu-id="cac50-148">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="cac50-149">На следующем рисунке показана линия и система координат.</span><span class="sxs-lookup"><span data-stu-id="cac50-149">The following illustration shows the line and coordinate system.</span></span>

![снимок экрана предыдущего окна, но шире, с осями, расположенными слева, с пометкой по-другому](images/aboutgdip05-art03.png)

<span data-ttu-id="cac50-151">Если предполагается, что устройство вывода имеет 96 точек на дюйм в горизонтальном направлении и 96 точек на дюйм в вертикальном направлении, конечные точки строки в предыдущем примере имеют следующие координаты в трех координатных пространствах:</span><span class="sxs-lookup"><span data-stu-id="cac50-151">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="cac50-152">Пробел</span><span class="sxs-lookup"><span data-stu-id="cac50-152">Space</span></span>       | <span data-ttu-id="cac50-153">Координаты конечной точки</span><span class="sxs-lookup"><span data-stu-id="cac50-153">Endpoint coordinates</span></span>                        |
|--------|-------------------------|
| <span data-ttu-id="cac50-154">World</span><span class="sxs-lookup"><span data-stu-id="cac50-154">World</span></span>  | <span data-ttu-id="cac50-155">(0, 0) на (2, 1)</span><span class="sxs-lookup"><span data-stu-id="cac50-155">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="cac50-156">Страница</span><span class="sxs-lookup"><span data-stu-id="cac50-156">Page</span></span>   | <span data-ttu-id="cac50-157">(от 2, 0,5) до (4, 1,5)</span><span class="sxs-lookup"><span data-stu-id="cac50-157">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="cac50-158">Устройство</span><span class="sxs-lookup"><span data-stu-id="cac50-158">Device</span></span> | <span data-ttu-id="cac50-159">(192, 48) в (384, 144)</span><span class="sxs-lookup"><span data-stu-id="cac50-159">(192, 48) to (384, 144)</span></span> |



 

 

 
