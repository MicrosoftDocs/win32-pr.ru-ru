---
title: Атрибут VML Text-Decoration
description: Атрибут VML Text-Decoration
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474d76b9e37cb363a8b2a28b84c30be77f857159767cc4db221fd7a684b4951e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796034"
---
# <a name="vml-text-decoration-attribute"></a>Атрибут VML Text-Decoration

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 