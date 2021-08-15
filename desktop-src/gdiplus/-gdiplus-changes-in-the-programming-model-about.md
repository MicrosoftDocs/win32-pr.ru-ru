---
description: в следующих разделах описывается несколько способов программирования с помощью Windows GDI+ отличается от программирования с помощью Windows интерфейс графических устройств (GDI).
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: Изменения в модели программирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05dd8b74662d0141405b9d11b9b4446ffb19dd4ef3bfdec788afe7a51a8c681a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249891"
---
# <a name="changes-in-the-programming-model"></a>Изменения в модели программирования

в следующих разделах описывается несколько способов программирования с помощью Windows GDI+ отличается от программирования с помощью Windows интерфейс графических устройств (GDI).

-   [Контексты устройств, дескрипторы и графические объекты](#device-contexts-handles-and-graphics-objects)
-   [Два способа рисования линии](#two-ways-to-draw-a-line)
    -   [Рисование линии с помощью GDI](#drawing-a-line-with-gdi)
    -   [рисование линии с GDI+ и интерфейсом класса C++](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [Перья, кисти, пути, изображения и шрифты в качестве параметров](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [Перегрузка методов](#method-overloading)
-   [Нет больше текущей должности](#no-more-current-position)
-   [Отдельные методы для рисования и заполнения](#separate-methods-for-draw-and-fill)
-   [Конструирование областей](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>Контексты устройств, дескрипторы и графические объекты

если вы написали программы с помощью GDI (интерфейс графических устройств, входящий в предыдущие версии Windows), вы знакомы с концепцией контекста устройства (DC). контекст устройства — это структура, используемая Windows для хранения сведений о возможностях конкретного устройства отображения и атрибутов, определяющих, как элементы будут отображаться на этом устройстве. Контекст устройства для экранного видео также связан с определенным окном на экране. Сначала вы получаете маркер контекста устройства (HDC), а затем передаете этот обработчик в качестве аргумента функциям GDI, которые фактически выполняют рисование. Вы также передаете этот обработчик в качестве аргумента функциям GDI, которые получают или устанавливают атрибуты контекста устройства.

при использовании GDI+ вам не нужно беспокоиться о дескрипторах и контекстах устройств, как это делается при использовании GDI. Вы просто создаете [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект, а затем вызываете его методы в привычном объектно-ориентированном стиле — Миграфиксобжект. DrawLine (*Parameters*). объект **Graphics** является ядром GDI+ точно так же, как контекстом устройства является ядро GDI. Контекст устройства и объект **Graphics** играют аналогичные роли, но существуют фундаментальные различия между моделью программирования на основе маркеров, используемой с контекстами устройств (GDI), и объектно-ориентированной моделью, используемой с **графическими** объектами (GDI+).

[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект, как и контекст устройства, связан с определенным окном на экране и содержит атрибуты (например, режим сглаживания и подсказку для визуализации текста), указывающий способ отрисовки элементов. Однако объект **Graphics** не привязан к Перу, кисти, пути, изображению или шрифту в качестве контекста устройства. Например, в GDI, прежде чем можно будет использовать контекст устройства для рисования линии, необходимо вызвать функцию [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) , чтобы связать объект Pen с контекстом устройства. Это называется выделением пера в контексте устройства. Все линии, нарисованные в контексте устройства, будут использовать это перо до тех пор, пока не будет выбрано другое перо. с GDI+ объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) передается в качестве аргумента методу [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) класса **Graphics** . Можно использовать другой объект **Pen** в каждом ряду вызовов метода DrawLine без связывания заданного объекта **Pen** с **графическим** объектом.

## <a name="two-ways-to-draw-a-line"></a>Два способа рисования линии

В следующих двух примерах каждый рисуется красная линия ширины 3 из расположения (20, 10) в положение (200 100). первый пример вызывает GDI, а второй вызывает GDI+ через интерфейс класса C++.

-   [Рисование линии с помощью GDI](#drawing-a-line-with-gdi)
-   [рисование линии с GDI+ и интерфейсом класса C++](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>Рисование линии с помощью GDI

Чтобы нарисовать линию с помощью GDI, необходимы два объекта: контекст устройства и перо. Вы получаете обработчик контекста устройства, вызывая [**бегинпаинт**](/windows/win32/api/winuser/nf-winuser-beginpaint), и указатель на перо, вызывая [креатепен](/windows/win32/api/wingdi/nf-wingdi-createpen). Затем следует вызвать функцию [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) , чтобы выбрать перо в контексте устройства. Установите для параметра "перо" значение (20, 10), вызвав [моветоекс](/windows/win32/api/wingdi/nf-wingdi-movetoex) , а затем нарисуйте линию с этой позицией пера на (200, 100), вызвав **lineTo**. Обратите внимание, что Моветоекс и [lineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) одновременно получают **HDC** в качестве аргумента.


```
HDC          hdc;
PAINTSTRUCT  ps;
HPEN         hPen;
HPEN         hPenOld;
hdc = BeginPaint(hWnd, &ps);
   hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
   hPenOld = (HPEN)SelectObject(hdc, hPen);
   MoveToEx(hdc, 20, 10, NULL);
   LineTo(hdc, 200, 100);
   SelectObject(hdc, hPenOld);
   DeleteObject(hPen);
EndPaint(hWnd, &ps);
```



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a>рисование линии с GDI+ и интерфейсом класса C++

чтобы нарисовать линию с GDI+ и интерфейсом класса C++, необходим объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) и объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . обратите внимание, что вы не запрашиваете Windows для дескрипторов этих объектов. Вместо этого конструкторы используются для создания экземпляра класса **Graphics** ( **графического** объекта) и экземпляра класса **Pen** (объект **Pen** ). Рисование линии включает вызов метода [**Graphics::D равлине**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) класса **Graphics** . Первый параметр метода **Graphics::D равлине** является указателем на объект **Pen** . Это более простая и более гибкая схема, чем выбор пера в контексте устройства, как показано в предыдущем примере GDI.


```
HDC          hdc;
PAINTSTRUCT  ps;
Pen*         myPen;
Graphics*    myGraphics;
hdc = BeginPaint(hWnd, &ps);
   myPen = new Pen(Color(255, 255, 0, 0), 3);
   myGraphics = new Graphics(hdc);
   myGraphics->DrawLine(myPen, 20, 10, 200, 100);
   delete myGraphics;
   delete myPen;
EndPaint(hWnd, &ps);
```



## <a name="pens-brushes-paths-images-and-fonts-as-parameters"></a>Перья, кисти, пути, изображения и шрифты в качестве параметров

В предыдущих примерах показано, что объекты [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) можно создавать и обслуживать отдельно от объекта [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , который предоставляет методы рисования. Объекты [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush), [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath), [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)и [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) также можно создавать и поддерживать отдельно от объекта **Graphics** . Многие из методов рисования, предоставляемых классом **Graphics** , получают объект **Brush**, **GraphicsPath**, **Image** или **Font** в качестве аргумента. Например, адрес объекта **Brush** передается в качестве аргумента в метод [филлректангле](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) , а адрес объекта **GraphicsPath** передается в качестве аргумента в метод [**Graphics::D равпас**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) . Аналогичным образом адреса объектов **Image** и **Font** передаются методам [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) и [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) . Это отличается от GDI, где вы выбрали кисть, путь, изображение или шрифт в контексте устройства, а затем передаем дескриптор контекста устройства в качестве аргумента функции рисования.

## <a name="method-overloading"></a>Перегрузка методов

многие из GDI+ методов перегружены; то есть несколько методов имеют одно и то же имя, но имеют разные списки параметров. Например, метод [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) имеет следующие формы:


```
Status DrawLine(IN const Pen* pen,
                IN REAL x1,
                IN REAL y1,
                IN REAL x2,
                IN REAL y2);
Status DrawLine(IN const Pen* pen,
                IN const PointF& pt1,
                IN const PointF& pt2);
Status DrawLine(IN const Pen* pen,
                IN INT x1,
                IN INT y1,
                IN INT x2,
                IN INT y2);
    
Status DrawLine(IN const Pen* pen,
                IN const Point& pt1,
                IN const Point& pt2);
```



Все четыре варианта [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) выше получают указатель на объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , координаты начальной точки и координаты конечной точки. Первые два варианта получают координаты в виде чисел с плавающей запятой, а последние два варианта получают координаты как целые числа. Первый и третий варианты получают координаты как список из четырех отдельных чисел, а второй и четвертый варианты получают координаты в виде пары объектов [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (или [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)).

## <a name="no-more-current-position"></a>Нет больше текущей должности

Обратите внимание, что в методах [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) , показанных ранее, начальная и конечная точки линии принимаются в качестве аргументов. Это отправлено из схемы GDI, где вы вызываете **моветоекс** для установки текущей позиции пера, за которой следует значение **lineTo** , чтобы нарисовать линию, начинающуюся с (**x1**, **Y1**) и заканчивая в (**x2**, **Y2**). GDI+ в целом, применяет понятие текущей должности.

## <a name="separate-methods-for-draw-and-fill"></a>Отдельные методы для рисования и заполнения

GDI+ является более гибкой, чем GDI, когда приходится рисовать контуры и заполнять внутренние области фигур, таких как прямоугольники. GDI имеет функцию [Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) , которая рисует контур и заполняет внутреннюю часть прямоугольника на один шаг. Контур рисуется с помощью выбранного пера, а внутренняя часть заполняется текущей выбранной кистью.


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



GDI+ имеет отдельные методы для рисования контура и заполнения внутренней части прямоугольника. Метод [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) имеет адрес объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) в качестве одного из его параметров, а метод [филлректангле](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) имеет адрес объекта [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) в качестве одного из его параметров.


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



обратите внимание, что методы [филлректангле](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) и [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) в GDI+ получают аргументы, указывающие левую границу, верхнюю, ширину и высоту прямоугольника. Это отличается от функции[Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) GDI, которая принимает аргументы, указывающие левый край прямоугольника, правый край, верхний и нижний. также обратите внимание, что конструктор для класса [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) в GDI+ имеет четыре параметра. Последние три параметра — это обычные значения красного, зеленого и синего. Первый параметр — это альфа-значение, указывающее экстент, в котором нарисованный цвет смешивается с цветом фона.

## <a name="constructing-regions"></a>Конструирование областей

GDI предоставляет несколько функций для создания регионов: Креатеректргн, Креатиллптикргн, Креатераундректргн, Креатеполигонргн и Креатеполиполигонргн. можно ожидать, что класс [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) в GDI+ имеет аналогичные конструкторы, принимающие прямоугольники, эллипсы, скругленные прямоугольники и многоугольники в качестве аргументов, но это не так. класс **Region** в GDI+ предоставляет конструктор, который получает ссылку на объект [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) и другой конструктор, получающий адрес объекта [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . Если вы хотите создать область на основе эллипса, скругленного прямоугольника или многоугольника, вы можете легко сделать это, создав объект **GraphicsPath** (который содержит эллипс), а затем передав адрес этого объекта **GraphicsPath** в конструктор **Region** .

GDI+ позволяет легко формировать сложные области путем объединения фигур и путей. Класс [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) содержит методы [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) и [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) , которые можно использовать для дополнения существующей области с путем или другим регионом. одной из удобных функций схемы GDI+ является то, что объект [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) не уничтожается, когда он передается в качестве аргумента в конструктор **Region** . В GDI можно преобразовать путь в область с помощью функции [пасторегион](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) , но путь уничтожается в процессе. Кроме того, объект **GraphicsPath** не уничтожается, когда его адрес передается в качестве аргумента в метод Union или INTERSECT, поэтому можно использовать заданный путь в качестве стандартного блока для нескольких отдельных регионов. Это показано в следующем примере. Предположим, что **онепас** является указателем на объект **GraphicsPath** (простой или сложный), который уже был инициализирован.


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
