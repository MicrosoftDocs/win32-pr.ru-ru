---
title: Атрибут VML Font-Variant
description: Атрибут VML Font-Variant
ms.assetid: f58bf3e0-e285-474c-83b1-203fce4f3c3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 243f8b36d36d8bb9b210a916cef239cda6061e0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413029"
---
# <a name="vml-font-variant-attribute"></a>Атрибут VML Font-Variant

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет вариант начертания шрифта. Read/write. **Строка**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "Font-Variant: *Expression* " >

**Синтаксис сценария**

*element* . Style. фонтвариант = "*выражение*"

*выражение* = *element*. Style. фонтвариант

**Замечания**

Значения качества производительности:

-   Обычная (по умолчанию)
-   малые прописные

Значения совпадают со стандартными атрибутами стиля HTML.

*Стандартный атрибут VML*

**Пример**

Шрифт подготавливается к просмотру как небольшие прописные буквы.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal small-caps normal 36pt Arial"/>
   </v:line>
```



 

 