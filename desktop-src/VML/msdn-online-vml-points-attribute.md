---
title: Атрибут точек VML
description: Атрибут точек VML
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070099"
---
# <a name="vml-points-attribute"></a>Атрибут точек VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет набор точек, образующих ломаную линию. Read/write. [Ивгпоинтс](msdn-online-vml-ivgpoints-data-type.md) .

**Применимо к**:

[Ломаная линия](msdn-online-vml-polyline-element.md)

**Синтаксис тега**

<v: *element* Points = " *Expression* " >

**Синтаксис сценария**

*element* . Points = "*выражение * * *"**

*выражение* = *element*. Points

**Замечания**

Определяет набор прямых линейных сегментов, состоящих из нескольких точек. Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC). Значение по умолчанию — 0, 0 10, 10. Обратите внимание, что запятые не требуются, но они упрощают удобочитаемость.

*Стандартный атрибут VML*

**Пример**

Ломаная линия начинается в точке 10, 10 и заканчивается в 100 100, со значениями точек.


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 