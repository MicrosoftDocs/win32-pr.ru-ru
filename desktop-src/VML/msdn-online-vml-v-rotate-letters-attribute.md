---
title: Атрибут VML V-поверните-Letters
description: Атрибут VML V-поверните-Letters
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779f7878b01765416560dacaed5e3b81a1e00a25d4bf7c53e0071c8bb487d16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123784"
---
# <a name="vml-v-rotate-letters-attribute"></a>Атрибут VML V-поверните-Letters

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, поворачиваются ли буквы текста. Read/write. **Вгтристате**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "v-вращение-Letters: *Expression* " >

**Синтаксис сценария**

*element* . Style. v-вращение-Letters = "*выражение*"

*выражение* = *element*. Style. v-вращение-буквы

**Замечания**

Если **значение равно true**, буквы текста поворачиваются в 90 градусов. Значение по умолчанию равно **False**.

*Стандартный атрибут VML*

**Пример**

Буквы поворачиваются на 90 градусов.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 