---
title: Использование элемента Handles
description: Использование элемента Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Веб-семинар, обрабатывает элемент
- Разработка веб-страниц, обработка элемента
- Язык VML (VML), обрабатывает элемент
- VML (язык VML), обрабатывает элемент
- Векторная графика, Handles, элемент
- обрабатывает элемент
- Элементы VML, дескрипторы
- Фигуры VML, обработка элемента
- Язык VML (VML), присоединение текста к фигурам
- VML (язык VML), присоединение текста к фигурам
- Векторная графика, присоединение текста к фигурам
- Фигуры VML, присоединение текста
- присоединение текста к фигурам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d504024a3d5c42caf8af116a08e5bd8787905991f14c4181fe3a75b10f4814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057218"
---
# <a name="using-the-handles-element"></a>Использование элемента Handles

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

В этом разделе будет показано, как использовать `<handles>` элемент для присоединения текста к фигуре.

`<handles>`Вложенный элемент можно поместить внутри `<shape>` или `<shapetype>` , чтобы определить элементы пользовательского интерфейса, которые могут варьировать значения  назначений в фигуре.

Например, как показано в следующем представлении VML, можно задать маркер регулировки (желтый квадрат), который пользователи могут просто перетаскивать для изменения формы.

примечание. маркеры доступны при просмотре этой фигуры VML в Microsoft Office приложениях, где фигура должна быть манипулабле.

![shape1.gif (564 байт)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Обратите внимание, что единственным различием между предыдущим представлением VML и следующим является значение **года** .

![shape2.gif (1361 байт)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .

 

 