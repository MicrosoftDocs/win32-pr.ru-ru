---
title: Атрибут Стартарровленгс VML
description: Атрибут Стартарровленгс VML
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413231"
---
# <a name="vml-startarrowlength-attribute"></a>Атрибут Стартарровленгс VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет длину стрелки для начала строки. Read/write. **Вгарровхеадленгс**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* стартарровленгс = " *выражение* " >

**Синтаксис сценария**

*element* . стартарровленгс = "*выражение*"

*выражение* = *element*. стартарровленгс

**Замечания**

К этим значениям относятся следующие.

-   Short
-   Среднее (по умолчанию)
-   Long

Стандартный атрибут VML

**Пример**

Линия рисуется с помощью короткой классической стрелки в начале штриха.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 