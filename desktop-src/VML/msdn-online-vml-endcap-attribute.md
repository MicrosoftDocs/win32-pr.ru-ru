---
title: Атрибут Ендкап VML
description: Атрибут Ендкап VML
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b2d36eb76b840ca8f89aebf3dadefaa68093394a07bd78db0e8fa0b18ed555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346719"
---
# <a name="vml-endcap-attribute"></a>Атрибут Ендкап VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет стиль конца штриха. Read/write. **Вглининдкапстиле**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* ендкап = " *выражение* " >

**Синтаксис сценария**

*element* . ендкап = "*выражение*"

*выражение* = *element*. ендкап

**Замечания**

К этим значениям относятся следующие.

-   Flat (по умолчанию)
-   Square
-   Round

*Стандартный атрибут VML*

**Пример**

Линия рисуется с плоским ограничением в конце штриха.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 