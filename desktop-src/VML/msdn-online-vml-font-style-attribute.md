---
title: Атрибут VML Font-Style
description: Атрибут VML Font-Style
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f4fc2f299d78c3ccd8b194b8506cfce07abceb7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070078"
---
# <a name="vml-font-style-attribute"></a>Атрибут VML Font-Style

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет величину наклона для шрифта. Read/write. **Строка**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "Font-Style: *Expression* " >

**Синтаксис сценария**

*element* . Style. FontStyle = "*выражение*"

*выражение* = *element*. Style. FontStyle

**Замечания**

Значения качества производительности:

-   Обычная (по умолчанию)
-   наклонный
-   курсив

Большинство браузеров отображаются наклонным курсивом. Значения совпадают со стандартными атрибутами стиля HTML.

*Стандартный атрибут VML*

**Пример**

Шрифт имеет курсивное начертание (наклонное).


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 