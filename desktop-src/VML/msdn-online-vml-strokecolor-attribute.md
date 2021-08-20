---
title: Атрибут Строкеколор VML
description: Атрибут Строкеколор VML
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a419813c5bd9db4370320f9f181477013136c70265f4ba1d8572a38ae9e3c473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124237"
---
# <a name="vml-strokecolor-attribute"></a>Атрибут Строкеколор VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет цвет кисти, которая обозначает контур фигуры. Read/write. [Ивгколор](msdn-online-vml-ivgcolor.md).

**Применимо к**:

[Фигура](shape-element--vml.md)

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

 

 