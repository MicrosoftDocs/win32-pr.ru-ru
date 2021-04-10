---
title: Атрибут Строкеколор VML
description: Атрибут Строкеколор VML
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070164"
---
# <a name="vml-strokecolor-attribute"></a>Атрибут Строкеколор VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет цвет кисти, которая обозначает контур фигуры. Read/write. [Ивгколор](msdn-online-vml-ivgcolor.md).

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* строкеколор = " *выражение* " >

**Синтаксис сценария**

*element* . строкеколор = "*выражение*"

*выражение* = *element*. строкеколор

**Замечания**

Значение дублируется из атрибута **Color** элемента [Stroke](msdn-online-vml-stroke-element.md) .

*Стандартный атрибут VML*

**Пример**

Цвет штриха прямоугольника — красный.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Пример атрибута строкеколор](/previous-versions/bb264093(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 