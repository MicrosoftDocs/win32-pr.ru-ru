---
title: Атрибут Фитшапе VML
description: Атрибут Фитшапе VML
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672411"
---
# <a name="vml-fitshape-attribute"></a>Атрибут Фитшапе VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, умещается ли текст в ограничивающем прямоугольнике фигуры. Read/write. **Вгтристате**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: *element* фитшапе = " *выражение* " >

**Синтаксис сценария**

*element* . фитшапе = "*выражение*"

*выражение* = *element*. фитшапе

**Замечания**

Если **значение равно true**, растягивает текст до краев прямоугольника, определяющего всю фигуру. По умолчанию **False**.

*Стандартный атрибут VML*

**Пример**

Текст будет растянут по размеру фигуры.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 