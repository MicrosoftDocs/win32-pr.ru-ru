---
description: Замкнутая фигура, например прямоугольник или эллипс, состоит из контура и внутренней части.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Кисти и закрашенные фигуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563461"
---
# <a name="brushes-and-filled-shapes"></a>Кисти и закрашенные фигуры

Замкнутая фигура, например прямоугольник или эллипс, состоит из контура и внутренней части. Структура рисуется с помощью объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , а внутренняя часть заполняется объектом [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . Windows GDI+ предоставляет несколько классов кистей для заполнения внутренних частей замкнутых фигур: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**хатчбруш**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)и [**пасградиентбруш**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush). Все эти классы наследуют от класса **Brush** . На следующем рисунке показан прямоугольник, заполненный сплошной кистью, и эллипс, заполненный штриховым кистью.

![Иллюстрация, демонстрирующая синий прямоугольник и пурпурный эллипс, заполненный синим шаблоном штриховки](images/aboutgdip02-art17.png)

 

-   [Сплошные кисти](#solid-brushes)
-   [Штриховые кисти](#hatch-brushes)
-   [Текстурные кисти](#texture-brushes)
-   [Градиентные кисти](#gradient-brushes)

## <a name="solid-brushes"></a>Сплошные кисти

Для заполнения замкнутой фигуры необходим [**графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект и объект [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . Объект **Graphics** предоставляет методы, такие как [филлректангле](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) и [филлеллипсе](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), а объект **Brush** сохраняет атрибуты заливки, такие как цвет и шаблон. Адрес объекта **Brush** передается в качестве одного из аргументов метода Fill. В следующем примере заливка эллипса осуществляется с помощью сплошного красного цвета.


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



Обратите внимание, что в предыдущем примере кисть относится к типу [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), который наследует от [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).

## <a name="hatch-brushes"></a>Штриховые кисти

При заполнении фигуры штриховой кистью необходимо указать цвет переднего плана, цвет фона и стиль штриховки. Цвет переднего плана — это цвет штриховки.


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



Интерфейс GDI+ предоставляет более 50 стилей штриховки, указанных в [**хатчстиле**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle). На следующем рисунке показаны три стиля: горизонтальный, ForwardDiagonalный и перекрестный.

![Иллюстрация с тремя сине-окрашенными эллипсами с различными стилями штриховки](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a>Текстурные кисти

Текстурная кисть позволяет заполнить фигуру шаблоном, хранящимся в растровом изображении. Например, предположим, что следующий рисунок хранится в файле на диске с именем MyTexture.bmp.

![снимок экрана с небольшим квадратом, заполненным различными цветами](images/aboutgdip02-art19.png)

В следующем примере выполняется заливка эллипса путем повторения изображения, хранящегося в MyTexture.bmp.


```
Image myImage(L"MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



На следующем рисунке показан закрашенный эллипс.

![Иллюстрация, показывающая эллипс, заполненный ранее заданным шаблоном](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a>Градиентные кисти

Можно использовать градиентную кисть для заливки фигуры цветом, который постепенно меняется от одной части фигуры к другой. Например, горизонтальная Градиентная кисть изменит цвет при переходе с левой стороны фигуры на правую. В следующем примере заливка эллипса выполняется с помощью горизонтальной градиентной кисти, которая меняется с синего на зеленую при переходе от левой части эллипса к правой стороне.


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



На следующем рисунке показан закрашенный эллипс.

![Иллюстрация с эллипсом с градиентной заливкой: синий справа — зеленый слева](images/aboutgdip02-art21.png)

Кисть градиента контура может быть настроена на изменение цвета при перемещении от центра фигуры к границе.

![илустратион эллипса, темно-синий в центре, затенение светлого цвета на границе](images/aboutgdip02-art22.png)

Кисти градиента вдоль пути являются достаточно гибкими. Градиентная кисть, используемая для заливки треугольника на следующем рисунке, постепенно меняется от красного в центре к каждому из трех различных цветов в вершинах.

![Иллюстрация красного цвета в центре, заливка к другому цвету на каждой вершине](images/aboutgdip02-art23.png)

 

 



