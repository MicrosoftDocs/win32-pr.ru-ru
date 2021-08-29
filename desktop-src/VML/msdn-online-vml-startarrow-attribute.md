---
title: Атрибут Стартарров VML
description: Атрибут Стартарров VML
ms.assetid: 484dfcdb-f68d-40f9-9a83-18abb054d1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97b0d1ce8d352ef119e2745d0f7768332ad074d134877b03433aa788f1bb2e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754486"
---
# <a name="vml-startarrow-attribute"></a>Атрибут Стартарров VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет наконечник для начала строки. Read/write. **Строка**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* стартарров = " *выражение* " >

**Синтаксис сценария**

*element* . стартарров = "*выражение*"

*выражение* = *element*. стартарров

**Замечания**

К этим значениям относятся следующие.

-   Нет (по умолчанию)
-   Блокировать
-   Классическая
-   Ромб
-   Овал
-   Открыть

Стандартный атрибут VML

**Пример**

Линия рисуется с помощью классической стрелки в начале штриха.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke StartArrow="classic"/>
   </v:line>
```



 

 