---
title: Атрибут Control1 VML
description: Атрибут Control1 VML
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b4c57a936a2820e5189be78cab119b4455d20af22735a47a66c444f721723f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601938"
---
# <a name="vml-control1-attribute"></a>Атрибут Control1 VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет первую контрольную точку кривой Безье. Read/write. **VgVector2D**.

**Применимо к**:

[Соединитель](msdn-online-vml-curve-element.md)

**Синтаксис тега**

<v: *element* Control1 = " *выражение* " >

**Синтаксис сценария**

*element* . Control1 = "*выражение*"

*выражение* = *element*. Control1

**Замечания**

Определяет первую контрольную точку кривой Безье третьего порядка в пространстве координат родительского элемента. Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC). Значение по умолчанию — 10, 10.

*Стандартный атрибут VML*

**Пример**

Кривая является улыбкой. Он начинается слева и заканчивается справа. Две контрольные точки располагаются по пути, так что для получения их внешнего вида улыбки нужно извлечь кривую вниз.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 