---
title: Атрибут Ендарров VML
description: Атрибут Ендарров VML
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f289342c8bfb67e9a0c2ccc6e418f42bd954e9826a18f07260a2891bf4b4284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007834"
---
# <a name="vml-endarrow-attribute"></a>Атрибут Ендарров VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет наконечник для конца строки. Read/write. **Строка**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* ендарров = " *выражение* " >

**Синтаксис сценария**

*element* . ендарров = "*выражение*"

*выражение* = *element*. ендарров

**Замечания**

К этим значениям относятся следующие.

-   Нет (по умолчанию)
-   Блокировать
-   Классическая
-   Ромб
-   Овал
-   Открыть

*Стандартный атрибут VML*

**Пример**

Линия рисуется с помощью классической стрелки в конце штриха.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 