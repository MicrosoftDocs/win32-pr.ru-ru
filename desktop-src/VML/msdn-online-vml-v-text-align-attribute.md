---
title: Атрибут VML V-Text-aligned
description: Атрибут VML V-Text-aligned
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6efb96bde980a4831f400ada7032f9ee37f1d976
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987629"
---
# <a name="vml-v-text-align-attribute"></a>Атрибут VML V-Text-aligned

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет выравнивание текста. Read/write. **Строка**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "v-Text-aligned: *Expression* " >

**Синтаксис сценария**

*element* . Style. v-Text-aligned = "*выражение*"

*выражение* = *element*. Style. v-Text-aligned

**Замечания**

К этим значениям относятся следующие.

-   **Left** (по умолчанию)
-   **Правильно**
-   **Center**
-   **формат**
-   **Выравнивание по буквам**
-   **растяжение по ширине**

*Стандартный атрибут VML*

**Пример**

Текст будет растянут по размеру пути, но дополнительное пространство будет размещаться между каждой буквой.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 