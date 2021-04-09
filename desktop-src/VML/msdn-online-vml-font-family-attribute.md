---
title: Атрибут VML Font-Family
description: Атрибут VML Font-Family
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070598"
---
# <a name="vml-font-family-attribute"></a>Атрибут VML Font-Family

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 