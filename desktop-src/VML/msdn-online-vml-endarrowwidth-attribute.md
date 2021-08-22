---
title: Атрибут Ендарроввидс VML
description: Атрибут Ендарроввидс VML
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90270cfc554d7e2dea70b313507fd7f61bf3a073c0e27c03c82d8a696f2939a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119396084"
---
# <a name="vml-endarrowwidth-attribute"></a>Атрибут Ендарроввидс VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет ширину стрелки для конца строки. Read/write. **Вгарровхеадвидс**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* ендарроввидс = " *выражение* " >

**Синтаксис сценария**

*element* . ендарроввидс = "*выражение*"

*выражение* = *element*. ендарроввидс

**Замечания**

К этим значениям относятся следующие.

-   Разрабатываем
-   Среднее (по умолчанию)
-   Широкий

*Стандартный атрибут VML*

**Пример**

Линия рисуется с помощью широкой классической стрелки в конце штриха.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 