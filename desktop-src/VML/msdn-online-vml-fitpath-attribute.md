---
title: Атрибут Фитпас VML
description: Атрибут Фитпас VML
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8863fb4d8a382ac9ccddaf7cc55fe5e8ceeff221dc1f816e340fa0a78cf9d7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124787"
---
# <a name="vml-fitpath-attribute"></a>Атрибут Фитпас VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, соответствует ли текст контуру фигуры. Read/write. **Вгтристате**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: *element* фитпас = " *выражение* " >

**Синтаксис сценария**

*element* . фитпас = "*выражение*"

*выражение* = *element*. фитпас

**Замечания**

При **значении true** изменяет размер текста для заполнения пути, на котором он находится. По умолчанию **False**.

*Стандартный атрибут VML*

**Пример**

Текст будет соответствовать пути.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 