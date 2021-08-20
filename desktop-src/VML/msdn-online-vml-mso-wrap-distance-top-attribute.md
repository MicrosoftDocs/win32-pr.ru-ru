---
title: Атрибут VML MSO-Wrap-Distance-Top
description: Атрибут VML MSO-Wrap-Distance-Top
ms.assetid: 20444d16-fa84-4685-911c-288150c2674b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856082665ab1b46b9d9294bffdd2821e2fb5db4b6e066effef5dd2f081185f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124294"
---
# <a name="vml-mso-wrap-distance-top-attribute"></a>Атрибут VML MSO-Wrap-Distance-Top

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет расстояние от фигуры до текста, вокруг которого производится оболочка. Read/write. **Строка**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: Style *элемента* = "MSO-Wrap-Distance-Top: *выражение* " >

**Замечания**

Обратите внимание, что этот атрибут отличается от атрибута **поля** CSS. **поле** изменяет источник фигуры, чтобы включить в него области полей, но расстояние по обтекания в Microsoft Office не изменяет происхождение фигуры.

*Microsoft Office Extensions, атрибут*

**Пример**

Фигура имеет верхнее заданное расстояние в 10 пунктов.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 