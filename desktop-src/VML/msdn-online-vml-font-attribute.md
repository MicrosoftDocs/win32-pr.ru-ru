---
title: Атрибут шрифта VML
description: Атрибут шрифта VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074aa0672002dcbbac55d21ed27383d5a3fd6e3b9ccfe9125ad89c2c43ac71ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986664"
---
# <a name="vml-font-attribute"></a>Атрибут шрифта VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Задает составное значение атрибутов шрифта. Read/write. **Строка**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "Font: *Expression* " >

**Синтаксис сценария**

*element* . Style. Font = "*выражение*"

*выражение* = *элемент*. Style. Font

**Замечания**

Определяет атрибуты шрифта, включая семейство, стиль, вес, размер и вариант. Порядок следования определений в строке: **Шрифт** **, начертание шрифта, начертание** **шрифта**, шрифт, **Размер шрифта**, **линия** и **семейство шрифтов**. Значения совпадают со стандартными атрибутами стиля HTML.

*Стандартный атрибут VML*

**Пример**

Шрифт текста текстпас имеет курсив, капитель, полужирный шрифт, 36 пт, Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 