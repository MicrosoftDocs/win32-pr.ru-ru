---
description: класс Graphics — это основа Windows GDI+. Для рисования можно создать графический объект, задать его свойства и вызвать его методы (DrawLine, DrawImage, DrawString и т. д.).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Состояние графического объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f68a2ba754aadc1f7d2572dcbc2ac40d08d7fe95d382ce60511cd72d441bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977334"
---
# <a name="the-state-of-a-graphics-object"></a>Состояние графического объекта

класс [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) — это основа Windows GDI+. Для рисования можно создать **графический** объект, задать его свойства и вызвать его методы ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))и т. д.).

В следующем примере создается [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , а затем вызывается метод [**Graphics::D равректангле**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) объекта **Graphics** :


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



В приведенном выше коде метод [бегинпаинт](/windows/win32/api/winuser/nf-winuser-beginpaint) возвращает маркер в контекст устройства, и этот маркер передается в конструктор [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . контекст устройства — это структура (поддерживаемая Windows), содержащая сведения о конкретном используемом устройстве вывода.

## <a name="graphics-state"></a>Состояние графики

[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект не предоставляет методы рисования, такие как [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) и [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)). **Графический** объект также поддерживает состояние графики, которое можно разделить на следующие категории:

-   Ссылка на контекст устройства
-   Параметры качества
-   Преобразования
-   Отсеченная область

### <a name="device-context"></a>Контекст устройства

Разработчикам приложений не нужно думать о взаимодействии между объектом [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и его контекстом устройства. это взаимодействие обрабатывается GDI+ в фоновом режиме.

### <a name="quality-settings"></a>качество Параметры

Объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) имеет несколько свойств, влияющих на качество элементов, отображаемых на экране. Вы можете просматривать эти свойства и управлять ими, вызывая методы get и Set. Например, можно вызвать метод [**Graphics:: сеттекстрендерингхинт**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) , чтобы указать тип сглаживания (при его наличии), применяемый к тексту. Другими методами Set, влияющими на качество, являются [**графические:: сетсмусингмоде**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics:: сеткомпоситингмоде**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics:: Сеткомпоситингкуалити**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)и [**Graphics:: сетинтерполатионмоде**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).

В следующем примере рисуются два эллипса, один с режимом сглаживания, установленным в * * * * [смусингмодеантиалиас * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) , а другой — с режимом сглаживания [* * * * смусингмодехигхспид * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a>Преобразования

[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект поддерживает два преобразования («мир» и «страница»), которые применяются ко всем элементам, рисуемым этим **графическим** объектом. Любое аффинное преобразование может храниться в мировом преобразовании. Аффинное преобразование включает масштабирование, вращение, отражение, наклон и преобразование. Преобразование «страница» можно использовать для масштабирования и для изменения единиц измерения (например, пикселей на дюймы). Дополнительные сведения о преобразованиях см. в разделе [системы координат и преобразования](-gdiplus-coordinate-systems-and-transformations-about.md).

В следующем примере устанавливаются преобразования мира и страницы [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта. Для универсального преобразования устанавливается поворот на 30 градусов. Преобразование страницы задается таким образом, чтобы координаты, передаваемые во вторую [**графику::D равеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) , обрабатывались как миллиметры, а не как пиксели. Код выполняет два идентичных вызова метода **Graphics::D равеллипсе** . Преобразование «мир» применяется к первому **графическому элементу::D вызов равеллипсе** , и оба преобразования (мир и страница) применяются ко второй **графике::D** вызове равеллипсе.


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



На следующем рисунке показаны два эллипса. Обратите внимание, что поворот на 30 градусов основан на происхождении системы координат (левый верхний угол клиентской области), а не на центрах эллипсов. Также обратите внимание, что ширина пера, равная 1, означает 1 пиксель для первого эллипса и 1 миллиметр для второго эллипса.

![снимок экрана окна, содержащего маленький, тонкий эллипс и крупный, толстый эллипс](images/graphicsascon1.png)

 

### <a name="clipping-region"></a>Область обрезки

[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект поддерживает область обрезки, которая применяется ко всем элементам, рисуемым этим **графическим** объектом. Можно задать отсеченную область, вызвав метод [сетклип](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) .

В следующем примере создается область в форме креста путем формирования объединения двух прямоугольников. Этот регион назначается в качестве вырезанной области объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Затем код выводит две строки, которые ограничены внутренней областью обрезки.


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



На следующем рисунке показаны обрезанные линии.

![Иллюстрация, демонстрирующая цветную фигуру, перекрестную на две диагональные красной линии](images/graphicsascon2.png)

 

 
