---
title: Атрибут VML V-поверните-Letters
description: Атрибут VML V-поверните-Letters
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133943"
---
# <a name="vml-v-rotate-letters-attribute"></a>Атрибут VML V-поверните-Letters

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 