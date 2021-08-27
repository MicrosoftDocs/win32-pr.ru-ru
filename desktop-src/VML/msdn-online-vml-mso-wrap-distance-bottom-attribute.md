---
title: Атрибут VML MSO-Wrap-Distance-Bottom
description: Атрибут VML MSO-Wrap-Distance-Bottom
ms.assetid: b096fc67-dd99-4833-bb82-73de7b06f43c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e28ea0f2d84b9bf9f5981f9ebb22f15af75a2071f07dd9f3e006ac70b34256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007684"
---
# <a name="vml-mso-wrap-distance-bottom-attribute"></a>Атрибут VML MSO-Wrap-Distance-Bottom

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет расстояние от нижней стороны фигуры до текста, который обтекает вокруг него. Read/write. **Строка**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: Style *элемента* = "MSO-Wrap-Distance-Bottom: *выражение* " >

**Замечания**

Обратите внимание, что этот атрибут отличается от атрибута **поля** CSS. **поле** изменяет источник фигуры, добавляя области полей, но расстояние по переносу в Microsoft Office не изменяет происхождение фигуры.

*Microsoft Office Extensions, атрибут*

**Пример**

Фигура имеет нижнюю границу обтекания в 10 пунктов.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-bottom:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 