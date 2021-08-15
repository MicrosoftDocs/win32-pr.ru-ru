---
title: Атрибут VML Font-Family
description: Атрибут VML Font-Family
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1254be6f7264e0d8f77d5881a11b9c2ec5085a931a0cad713813c059c60e5e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754745"
---
# <a name="vml-font-family-attribute"></a>Атрибут VML Font-Family

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет семейство шрифта текстпас. Read/write. **Строка**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "Font-Family: *Expression* " >

**Синтаксис сценария**

*element* . Style. FontFamily = "*выражение*"

*выражение* = *элемент*. Style. FontFamily

**Замечания**

Определяет имя шрифта. Можно использовать специальные имена, такие как Arial, или универсальные типы, такие как serif, sans-serif, рукописный ввод, фэнтези или моноширинная. Значения совпадают со стандартными атрибутами стиля HTML.

*Стандартный атрибут VML*

**Пример**

Семейство шрифтов текста — Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 