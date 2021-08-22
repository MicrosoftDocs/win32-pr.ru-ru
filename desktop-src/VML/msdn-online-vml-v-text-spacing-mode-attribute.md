---
title: Атрибут "режим пробельного текста" VML V
description: Атрибут "режим пробельного текста" VML V
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42137e8c8ec401548c4e0b027a50f34813fc7b45b04c4568011617906ac8e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057662"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>Атрибут "режим пробельного текста" VML V

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет режим для леттерспаЦинг. Read/write. **Строка**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "v-Text-просвет-Mode: *выражение* " >

**Синтаксис сценария**

*element* . Style. v-Text-просвет-Mode = "*выражение*"

*выражение* = Text. Style. v-режим пробельных текстовых *элементов*

**Замечания**

Значения включают

-   **усиление** (по умолчанию)
-   **отслеживающ**

Этот атрибут определяет, будет ли удалено место между каждой буквой (с сужением) или добавляться между каждой буквой (отслеживание). Объем леттерспаЦинг изменения определяется атрибутом « [интервалы по тексту](msdn-online-vml-v-text-spacing-attribute.md) ».

*Стандартный атрибут VML*

**Пример**

ЛеттерспаЦинг между каждой буквой увеличивается на 200 единиц.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 