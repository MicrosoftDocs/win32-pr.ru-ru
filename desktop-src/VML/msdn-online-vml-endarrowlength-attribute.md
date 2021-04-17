---
title: Атрибут Ендарровленгс VML
description: Атрибут Ендарровленгс VML
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d9d8bfbd24a6a1b79208d50d4d2aef956a5bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691520"
---
# <a name="vml-endarrowlength-attribute"></a>Атрибут Ендарровленгс VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 