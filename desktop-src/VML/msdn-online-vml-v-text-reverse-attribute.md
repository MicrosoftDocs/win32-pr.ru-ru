---
title: VML V-Text-обратный атрибут
description: VML V-Text-обратный атрибут
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f1535620c1fefe98ac23e2f842ef9a97e13b9cb39c65ec6b97f6f7d12b1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654624"
---
# <a name="vml-v-text-reverse-attribute"></a>VML V-Text-обратный атрибут

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 