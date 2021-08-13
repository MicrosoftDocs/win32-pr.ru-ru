---
title: Атрибут Ендарровленгс VML
description: Атрибут Ендарровленгс VML
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb11c07300127acd2446c7c2c643e0a891957d63f7650044514427f3e8535d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601354"
---
# <a name="vml-endarrowlength-attribute"></a>Атрибут Ендарровленгс VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет длину наконечника для конца строки. Read/write. **Вгарровхеадленгс**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* ендарровленгс = " *выражение* " >

**Синтаксис сценария**

*element* . ендарровленгс = "*выражение*"

*выражение* = *element*. ендарровленгс

**Замечания**

К этим значениям относятся следующие.

-   Short
-   Среднее (по умолчанию)
-   Long

*Стандартный атрибут VML*

**Пример**

Линия рисуется с помощью короткой классической стрелки в конце штриха.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 