---
title: Атрибут Стартарров VML
description: Атрибут Стартарров VML
ms.assetid: 484dfcdb-f68d-40f9-9a83-18abb054d1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2c17569750c1e655a5538ca5bf233e49f827e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987687"
---
# <a name="vml-startarrow-attribute"></a>Атрибут Стартарров VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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
-   Классический
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



 

 