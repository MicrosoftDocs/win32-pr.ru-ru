---
title: Атрибут Жоинстиле VML
description: Атрибут Жоинстиле VML
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbad649d2a8889846d1d0c1e1df3d62e94cb8e8ff03f0dfa5c47f7bd414dcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599368"
---
# <a name="vml-joinstyle-attribute"></a>Атрибут Жоинстиле VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет стиль объединения ломаной линии. Read/write. Строка.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* жоинстиле = " *выражение* " >

**Синтаксис сценария**

*element* . жоинстиле = "*выражение*"

*выражение* = *element*. жоинстиле

**Замечания**

К этим значениям относятся следующие.

-   Round (по умолчанию)
-   рамки
-   срезу

*Стандартный атрибут VML*

**Пример**

Соединения в ломаной линии багетны.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 