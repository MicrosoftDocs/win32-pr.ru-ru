---
title: Атрибут Линестиле VML
description: Атрибут Линестиле VML
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90be9c2aceeb3663f55c92e1140eb6a12f66aa23dd8856d0da63f0a306d8cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598287"
---
# <a name="vml-linestyle-attribute"></a>Атрибут Линестиле VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет стиль линии для штриха. Read/write. **Строка**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* линестиле = " *выражение* " >

**Синтаксис сценария**

*element* . линестиле = "*выражение*"

*выражение* = *element*. линестиле

**Замечания**

К этим значениям относятся следующие.

-   Single (по умолчанию)
-   синсин
-   синсикк
-   сикксин
-   сиккбетвинсин

*Стандартный атрибут VML*

**Пример**

Двойная линия рисуется с помощью двух тонких штрихов.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 