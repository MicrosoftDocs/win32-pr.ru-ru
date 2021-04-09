---
title: VML V-Text-обратный атрибут
description: VML V-Text-обратный атрибут
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070309"
---
# <a name="vml-v-text-reverse-attribute"></a>VML V-Text-обратный атрибут

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, изменяется ли порядок макета строк на обратный. Read/write. **Вгтристате**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "v-Text-Reverse: *выражение* " >

**Синтаксис сценария**

*element* . Style. v-Text-Reverse = "*выражение*"

*выражение* = *element*. Style. v-Text-Reverse

**Замечания**

Если **значение равно true**, порядок расположения строк изменяется на обратный. Этот атрибут используется для вертикального макета текста. Значение по умолчанию равно **False**.

*Стандартный атрибут VML*

**Пример**

Порядок макета изменяется на обратный.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 