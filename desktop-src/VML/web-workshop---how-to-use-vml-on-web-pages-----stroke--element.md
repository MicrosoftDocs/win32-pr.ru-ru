---
title: Использование элемента Stroke
description: В этой статье описывается использование элемента Stroke элемента VML, который является устаревшим в Windows Internet Explorer 9.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Веб-семинар, элемент Stroke
- Разработка веб-страниц, элемент Stroke
- Язык VML (VML), элемент Stroke
- VML (язык VML), элемент Stroke
- Векторная графика, элемент Stroke
- элемент Stroke
- Элементы VML, Stroke
- Фигуры VML, элемент Stroke
- Язык VML (VML), атрибут свойства DashStyle
- VML (язык VML), атрибут свойства DashStyle
- Векторная графика, атрибут свойства DashStyle
- атрибут свойства DashStyle
- Язык VML (VML), атрибут свойства Opacity
- VML (язык VML), атрибут свойства Opacity
- Векторная графика, атрибут свойства Opacity
- атрибут свойства Opacity
- Язык VML (VML), атрибут свойства линестиле
- VML (язык VML), атрибут свойства линестиле
- Векторная графика, атрибут свойства линестиле
- атрибут свойства линестиле
- Язык VML (VML), атрибут свойства жоинстиле
- VML (язык VML), атрибут свойства жоинстиле
- Векторная графика, атрибут свойства жоинстиле
- атрибут свойства жоинстиле
- Язык VML (VML), атрибут свойства объекта FillType
- VML (язык VML), атрибут свойства объекта FillType
- Векторная графика, атрибут свойства объекта FillType
- атрибут свойства объекта FillType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407847"
---
# <a name="using-the-stroke-element"></a>Использование элемента Stroke

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Использование `<stroke>`

Как вы узнали, вы можете использовать атрибуты свойств **строкеколор** и **строкевеигхт** предопределенной фигуры, такие как `<oval>` ,,,, `<line>` `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --для указания цвета и веса контура фигуры. В этом разделе показано, как нарисовать фигуру с более сложной структурой.

`<stroke>`Вложенный элемент можно поместить внутри `<shape>` , или или `<shapetype>` любого предопределенного элемента Shape, чтобы описать, как рисовать контур фигуры. Затем можно использовать атрибуты свойств, например [DashStyle](#dashstyle), [Opacity](#opacity), [линестиле](#linestyle), [жоинстиле](#joinstyle), [объекта FillType](#filltype) --из `<stroke>` вложенного элемента для настройки структуры.

[![назад ](images/top.gif) к началу](#top)

## <a name="dashstyle"></a>DashStyle

Можно использовать атрибут свойства **DashStyle** `<stroke>` вложенного элемента для рисования контура с различными стилями пунктира.

**Примеры:**

Если указать `<v:stroke dashstyle="solid" />` внутри `<line>` элемента, можно создать сплошную линию, как показано в следующем представлении VML:

![solid.gif (96 байт)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Если изменить атрибут свойства **DashStyle** на "точка", можно создать пунктирную линию, как показано в следующем представлении VML:

![dot.gif (144 байт)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Если изменить атрибут свойства **DashStyle** на "тире", можно создать пунктирную линию, как показано в следующем представлении VML:

![dash.gif (137 байт)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Если изменить атрибут свойства **DashStyle** на "дашдот", можно создать линию с пунктирным и пунктирным стилем, как показано в следующем представлении VML:

![dashdot.gif (145 байт)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Если изменить атрибут свойства **DashStyle** на "лонгдаш", можно создать строку с длинным пунктирным стилем, как показано в следующем представлении VML:

![longdash.gif (123 байт)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Если изменить атрибут свойства **DashStyle** на "лонгдашдот", можно создать строку с длинным пунктирным и пунктирным стилем, как показано в следующем представлении VML:

![longdashdot.gif (135 байт)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Если поместить `<v:stroke dashstyle="dashdot" />` внутри `<rect>` элемента, можно создать прямоугольник, имеющий пунктирный и пунктирный контур, как показано в следующем представлении VML:

![rect.gif (615 байт)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![назад ](images/top.gif) к началу](#top)

## <a name="opacity"></a>непрозрачность

Атрибут свойства **Opacity** `<stroke>` вложенного элемента можно использовать для рисования контура с различными стилями непрозрачности. Значением атрибута **Opacity** свойства может быть любое число от 0 до 1. По умолчанию это 1, что означает полную непрозрачность.

**Примеры:**

Следующее представление VML создает линию с полной прозрачностью:

![line1.gif (96 байт)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Если добавить `<v:stroke opacity="0.5" />` внутри `<line>` элемента, можно создать линию со степенью непрозрачности 50%, как показано в следующем представлении VML:

![line2.gif (108 байт)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![назад ](images/top.gif) к началу](#top)

## <a name="linestyle"></a>линестиле

Можно использовать атрибут свойства **линестиле** `<stroke>` вложенного элемента для рисования контура с различными стилями линий.

**Примеры:**

Если указать `<v:stroke linestyle="single" />` внутри `<rect>` элемента, можно создать прямоугольник с одной структурой, как показано в следующем представлении VML:

![single.gif (537 байт)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Если изменить атрибут свойства **линестиле** на "синсин", можно создать прямоугольник с контуром (1:1:1), как показано в следующем представлении VML:

![thinthin.gif (642 байт)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Если изменить атрибут свойства **линестиле** на "синсикк", можно создать прямоугольник с контуром (1:1:2), как показано в следующем представлении VML:

![thinthick.gif (646 байт)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Если изменить атрибут свойства **линестиле** на "сикксин", можно создать прямоугольник с контуром (2:1:1), как показано в следующем представлении VML:

![thickthin.gif (676 байт)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Если изменить атрибут свойства **линестиле** на "сиккбетвинсин", можно создать прямоугольник с контуром (1:1:2:1:1), как показано в следующем представлении VML:

![thickbthin.gif (669 байт)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![назад ](images/top.gif) к началу](#top)

## <a name="joinstyle"></a>жоинстиле

С помощью атрибута **жоинстиле** `<stroke>` вложенного элемента можно определить, как объединяются линии.

Например, чтобы создать фигуру с контуром круглого объединения, как показано на следующем рисунке, можно указать `<v:stroke joinstyle="round" />` внутри `<polyline>` элемента, как показано в следующем представлении VML:

![round.gif (660 байт)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Если изменить атрибут свойства **жоинстиле** на «скос», можно создать фигуру с контуром рельефного объединения, как показано в следующем представлении VML:

![bevel.gif (650 байт)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Если изменить атрибут свойства **жоинстиле** на «угловой», можно создать фигуру с контуром «угловой соединитель», как показано в следующем представлении VML:

![miter.gif (702 байт)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![назад ](images/top.gif) к началу](#top)

## <a name="filltype"></a>объекта FillType

Атрибут свойства **объекта FillType** `<stroke>` вложенного элемента можно использовать для рисования контура с различными эффектами заливки.

**Примеры:**

Если указать `<v:stroke filltype="solid" />` внутри `<roundrect>` элемента, можно создать скругленный прямоугольник с заполненной сплошной структурой, как показано в следующем представлении VML:

![solid.gif (701 байт)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Если изменить атрибут свойства **объекта FillType** на «pattern», укажите в атрибуте свойства **src** расположение файла изображения шаблона и задайте атрибуту свойства **color2** второй цвет шаблона, а затем можно создать скругленный прямоугольник с контуром шаблона, как показано в следующем представлении VML:

![pattern.gif (1055 байт)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Если изменить атрибут свойства **объекта FillType** на "плитку" и указать атрибуту свойства **src** расположение файла изображения, можно создать скругленный прямоугольник с мозаичным контуром, как показано в следующем представлении VML:

![tile.gif (6617 байт)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Если изменить атрибут свойства **объекта FillType** на "Frame" и указать атрибуту свойства **src** расположение файла изображения, можно создать скругленный прямоугольник с контуром изображения, как показано в следующем представлении VML:

![frame.gif (6203 байт)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .

 

 