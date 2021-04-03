---
title: Атрибут VML Text-Decoration
description: Атрибут VML Text-Decoration
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee85007db2dbca04221604cafd79c5d7052c91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987579"
---
# <a name="vml-text-decoration-attribute"></a>Атрибут VML Text-Decoration

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет стиль оформления текста. Read/write. **Строка**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: *element* Style = "Оформление текста: *выражение* " >

**Синтаксис сценария**

*element* . Style. TextDecoration = "*выражение*"

*выражение* = *element*. Style. TextDecoration

**Замечания**

К этим значениям относятся следующие.

-   нет (по умолчанию)
-   подчеркнутый
-   надчеркивание
-   со сквозной линией
-   blink

*Стандартный атрибут VML*

**Пример**

Текст будет подчеркнут.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 