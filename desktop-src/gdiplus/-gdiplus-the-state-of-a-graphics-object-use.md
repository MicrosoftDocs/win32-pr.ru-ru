---
description: Класс Graphics является основой Windows GDI+. Для рисования можно создать графический объект, задать его свойства и вызвать его методы (DrawLine, DrawImage, DrawString и т. д.).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Состояние графического объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555248"
---
# <a name="the-state-of-a-graphics-object"></a><span data-ttu-id="cb227-104">Состояние графического объекта</span><span class="sxs-lookup"><span data-stu-id="cb227-104">The State of a Graphics Object</span></span>

<span data-ttu-id="cb227-105">Класс [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) является ОСНОВОЙ Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="cb227-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is at the heart of Windows GDI+.</span></span> <span data-ttu-id="cb227-106">Для рисования можно создать **графический** объект, задать его свойства и вызвать его методы ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))и т. д.).</span><span class="sxs-lookup"><span data-stu-id="cb227-106">To draw anything, you create a **Graphics** object, set its properties, and call its methods ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)), and the like).</span></span>

<span data-ttu-id="cb227-107">В следующем примере создается [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , а затем вызывается метод [**Graphics::D равректангле**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) объекта **Graphics** :</span><span class="sxs-lookup"><span data-stu-id="cb227-107">The following example constructs a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and then calls the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object:</span></span>


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



<span data-ttu-id="cb227-108">В приведенном выше коде метод [бегинпаинт](/windows/win32/api/winuser/nf-winuser-beginpaint) возвращает маркер в контекст устройства, и этот маркер передается в конструктор [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="cb227-108">In the preceding code, the [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) method returns a handle to a device context, and that handle is passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="cb227-109">Контекст устройства — это структура (поддерживаемая Windows), содержащая сведения об используемом конкретном устройстве вывода.</span><span class="sxs-lookup"><span data-stu-id="cb227-109">A device context is a structure (maintained by Windows) that holds information about the particular display device being used.</span></span>

## <a name="graphics-state"></a><span data-ttu-id="cb227-110">Состояние графики</span><span class="sxs-lookup"><span data-stu-id="cb227-110">Graphics State</span></span>

<span data-ttu-id="cb227-111">[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект не предоставляет методы рисования, такие как [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) и [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="cb227-111">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object does more than provide drawing methods, such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) and [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span></span> <span data-ttu-id="cb227-112">**Графический** объект также поддерживает состояние графики, которое можно разделить на следующие категории:</span><span class="sxs-lookup"><span data-stu-id="cb227-112">A **Graphics** object also maintains graphics state, which can be divided into the following categories:</span></span>

-   <span data-ttu-id="cb227-113">Ссылка на контекст устройства</span><span class="sxs-lookup"><span data-stu-id="cb227-113">A link to a device context</span></span>
-   <span data-ttu-id="cb227-114">Параметры качества</span><span class="sxs-lookup"><span data-stu-id="cb227-114">Quality settings</span></span>
-   <span data-ttu-id="cb227-115">Преобразования</span><span class="sxs-lookup"><span data-stu-id="cb227-115">Transformations</span></span>
-   <span data-ttu-id="cb227-116">Отсеченная область</span><span class="sxs-lookup"><span data-stu-id="cb227-116">A clipping region</span></span>

### <a name="device-context"></a><span data-ttu-id="cb227-117">Контекст устройства</span><span class="sxs-lookup"><span data-stu-id="cb227-117">Device Context</span></span>

<span data-ttu-id="cb227-118">Разработчикам приложений не нужно думать о взаимодействии между объектом [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и его контекстом устройства.</span><span class="sxs-lookup"><span data-stu-id="cb227-118">As an application programmer, you don't have to think about the interaction between a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and its device context.</span></span> <span data-ttu-id="cb227-119">Это взаимодействие обрабатывается GDI+ в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="cb227-119">This interaction is handled by GDI+ behind the scenes.</span></span>

### <a name="quality-settings"></a><span data-ttu-id="cb227-120">Параметры качества</span><span class="sxs-lookup"><span data-stu-id="cb227-120">Quality Settings</span></span>

<span data-ttu-id="cb227-121">Объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) имеет несколько свойств, влияющих на качество элементов, отображаемых на экране.</span><span class="sxs-lookup"><span data-stu-id="cb227-121">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object has several properties that influence the quality of the items that are drawn on the screen.</span></span> <span data-ttu-id="cb227-122">Вы можете просматривать эти свойства и управлять ими, вызывая методы get и Set.</span><span class="sxs-lookup"><span data-stu-id="cb227-122">You can view and manipulate these properties by calling get and set methods.</span></span> <span data-ttu-id="cb227-123">Например, можно вызвать метод [**Graphics:: сеттекстрендерингхинт**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) , чтобы указать тип сглаживания (при его наличии), применяемый к тексту.</span><span class="sxs-lookup"><span data-stu-id="cb227-123">For example, you can call the [**Graphics::SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method to specify the type of antialiasing (if any) applied to text.</span></span> <span data-ttu-id="cb227-124">Другими методами Set, влияющими на качество, являются [**графические:: сетсмусингмоде**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics:: сеткомпоситингмоде**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics:: Сеткомпоситингкуалити**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)и [**Graphics:: сетинтерполатионмоде**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span><span class="sxs-lookup"><span data-stu-id="cb227-124">Other set methods that influence quality are [**Graphics::SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics::SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality), and [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span></span>

<span data-ttu-id="cb227-125">В следующем примере рисуются два эллипса, один с режимом сглаживания, установленным в \* \* \* \* [смусингмодеантиалиас \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) , а другой — с режимом сглаживания [\* \* \* \* смусингмодехигхспид \* \* \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span><span class="sxs-lookup"><span data-stu-id="cb227-125">The following example draws two ellipses, one with the smoothing mode set to [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) and one with the smoothing mode set to [\*\*\*\*SmoothingModeHighSpeed\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a><span data-ttu-id="cb227-126">Преобразования</span><span class="sxs-lookup"><span data-stu-id="cb227-126">Transformations</span></span>

<span data-ttu-id="cb227-127">[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект поддерживает два преобразования («мир» и «страница»), которые применяются ко всем элементам, рисуемым этим **графическим** объектом.</span><span class="sxs-lookup"><span data-stu-id="cb227-127">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains two transformations (world and page) that are applied to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="cb227-128">Любое аффинное преобразование может храниться в мировом преобразовании.</span><span class="sxs-lookup"><span data-stu-id="cb227-128">Any affine transformation can be stored in the world transformation.</span></span> <span data-ttu-id="cb227-129">Аффинное преобразование включает масштабирование, вращение, отражение, наклон и преобразование.</span><span class="sxs-lookup"><span data-stu-id="cb227-129">Affine transformations include scaling, rotating, reflecting, skewing, and translating.</span></span> <span data-ttu-id="cb227-130">Преобразование «страница» можно использовать для масштабирования и для изменения единиц измерения (например, пикселей на дюймы).</span><span class="sxs-lookup"><span data-stu-id="cb227-130">The page transformation can be used for scaling and for changing units (for example, pixels to inches).</span></span> <span data-ttu-id="cb227-131">Дополнительные сведения о преобразованиях см. в разделе [системы координат и преобразования](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="cb227-131">For more information on transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="cb227-132">В следующем примере устанавливаются преобразования мира и страницы [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта.</span><span class="sxs-lookup"><span data-stu-id="cb227-132">The following example sets the world and page transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="cb227-133">Для универсального преобразования устанавливается поворот на 30 градусов.</span><span class="sxs-lookup"><span data-stu-id="cb227-133">The world transformation is set to a 30-degree rotation.</span></span> <span data-ttu-id="cb227-134">Преобразование страницы задается таким образом, чтобы координаты, передаваемые во вторую [**графику::D равеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) , обрабатывались как миллиметры, а не как пиксели.</span><span class="sxs-lookup"><span data-stu-id="cb227-134">The page transformation is set so that the coordinates passed to the second [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) will be treated as millimeters instead of pixels.</span></span> <span data-ttu-id="cb227-135">Код выполняет два идентичных вызова метода **Graphics::D равеллипсе** .</span><span class="sxs-lookup"><span data-stu-id="cb227-135">The code makes two identical calls to the **Graphics::DrawEllipse** method.</span></span> <span data-ttu-id="cb227-136">Преобразование «мир» применяется к первому **графическому элементу::D вызов равеллипсе** , и оба преобразования (мир и страница) применяются ко второй **графике::D** вызове равеллипсе.</span><span class="sxs-lookup"><span data-stu-id="cb227-136">The world transformation is applied to the first **Graphics::DrawEllipse** call, and both transformations (world and page) are applied to the second **Graphics::DrawEllipse** call.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



<span data-ttu-id="cb227-137">На следующем рисунке показаны два эллипса.</span><span class="sxs-lookup"><span data-stu-id="cb227-137">The following illustration shows the two ellipses.</span></span> <span data-ttu-id="cb227-138">Обратите внимание, что поворот на 30 градусов основан на происхождении системы координат (левый верхний угол клиентской области), а не на центрах эллипсов.</span><span class="sxs-lookup"><span data-stu-id="cb227-138">Note that the 30-degree rotation is about the origin of the coordinate system (upper-left corner of the client area), not about the centers of the ellipses.</span></span> <span data-ttu-id="cb227-139">Также обратите внимание, что ширина пера, равная 1, означает 1 пиксель для первого эллипса и 1 миллиметр для второго эллипса.</span><span class="sxs-lookup"><span data-stu-id="cb227-139">Also note that the pen width of 1 means 1 pixel for the first ellipse and 1 millimeter for the second ellipse.</span></span>

![снимок экрана окна, содержащего маленький, тонкий эллипс и крупный, толстый эллипс](images/graphicsascon1.png)

 

### <a name="clipping-region"></a><span data-ttu-id="cb227-141">Область обрезки</span><span class="sxs-lookup"><span data-stu-id="cb227-141">Clipping Region</span></span>

<span data-ttu-id="cb227-142">[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект поддерживает область обрезки, которая применяется ко всем элементам, рисуемым этим **графическим** объектом.</span><span class="sxs-lookup"><span data-stu-id="cb227-142">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains a clipping region that applies to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="cb227-143">Можно задать отсеченную область, вызвав метод [сетклип](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) .</span><span class="sxs-lookup"><span data-stu-id="cb227-143">You can set the clipping region by calling the [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method.</span></span>

<span data-ttu-id="cb227-144">В следующем примере создается область в форме креста путем формирования объединения двух прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="cb227-144">The following example creates a plus-shaped region by forming the union of two rectangles.</span></span> <span data-ttu-id="cb227-145">Этот регион назначается в качестве вырезанной области объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="cb227-145">That region is designated as the clipping region of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="cb227-146">Затем код выводит две строки, которые ограничены внутренней областью обрезки.</span><span class="sxs-lookup"><span data-stu-id="cb227-146">Then the code draws two lines that are restricted to the interior of the clipping region.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



<span data-ttu-id="cb227-147">На следующем рисунке показаны обрезанные линии.</span><span class="sxs-lookup"><span data-stu-id="cb227-147">The following illustration shows the clipped lines.</span></span>

![Иллюстрация, демонстрирующая цветную фигуру, перекрестную на две диагональные красной линии](images/graphicsascon2.png)

 

 
