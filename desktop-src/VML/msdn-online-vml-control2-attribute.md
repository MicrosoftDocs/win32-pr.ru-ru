---
title: Атрибут Control2 VML
description: Атрибут Control2 VML
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7af3871981e26ff7eff471651de555483fd540
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133919"
---
# <a name="vml-control2-attribute"></a>Атрибут Control2 VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет вторую контрольную точку кривой Безье. Read/write. **VgVector2D**.

**Применимо к**:

[Соединитель](msdn-online-vml-curve-element.md)

**Синтаксис тега**

<v: *element* control2 = " *выражение* " >

**Синтаксис сценария**

*element* . control2 = "*выражение*"

*выражение* = *element*. control2

**Замечания**

Определяет вторую контрольную точку кривой Безье третьего порядка в пространстве координат родительского элемента. Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC). Значение по умолчанию — 20,0.

*Стандартный атрибут VML*

**Пример**

Кривая является улыбкой. Он начинается слева и заканчивается справа. Две контрольные точки располагаются по пути, так что для получения их внешнего вида улыбки нужно извлечь кривую вниз.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 