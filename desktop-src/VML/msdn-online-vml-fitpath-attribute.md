---
title: Атрибут Фитпас VML
description: Атрибут Фитпас VML
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805e59a50c63248ed936f6a849869057a34a6e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104261007"
---
# <a name="vml-fitpath-attribute"></a>Атрибут Фитпас VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 