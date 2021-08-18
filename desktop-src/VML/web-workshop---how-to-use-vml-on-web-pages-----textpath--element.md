---
title: Использование элемента Текстпас
description: Использование элемента Текстпас
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Веб-семинар, элемент текстпас
- Разработка веб-страниц, элемент текстпас
- Язык VML (VML), элемент текстпас
- VML (язык VML), элемент текстпас
- Векторная графика, элемент текстпас
- текстпас, элемент
- Элементы VML, текстпас
- Фигуры VML, элемент текстпас
- Язык VML (VML), Рисование текста
- VML (язык VML), Рисование текста
- Векторная графика, Рисование текста VML
- рисование текста
- Фигуры VML, Рисование текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5db3b76d0c4ad2e56c59cfcf6dd39a2af51317b63ee190f47d794933282b5a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056985"
---
# <a name="using-the-textpath-element"></a>Использование элемента Текстпас

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

В этом разделе будет показано, как использовать `<textpath>` элемент для рисования текста с различными стилями.

`<textpath>`Вложенный элемент можно поместить внутрь `<shape>` или `<shapetype>` для рисования текста. Затем можно использовать атрибуты свойств `<textpath>` вложенного элемента для настройки текста. Можно также использовать `<formulas>` вложенный элемент для определения контура текста.

Например, чтобы создать текст, показанный на следующем рисунке, можно ввести следующее представление VML. Обратите внимание, что мы используем `<shapetype>` элемент для определения прототипа для контура текста. Затем мы создаем две фигуры из одного шапетипе. Можно просто изменить атрибут свойства **строки** для вывода другого текста.

![\-1.gif shape1 (4898 байт)](images/shape1-1t.gif)

![\-2.gif shape1 (2789 байт)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .

 

 