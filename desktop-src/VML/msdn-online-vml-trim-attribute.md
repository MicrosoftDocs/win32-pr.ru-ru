---
title: Атрибут Trim VML
description: Атрибут Trim VML
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05f7463465c10abb4f4f01267a7ebeac878cbf36c41f1effde6ec218bad1088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974615"
---
# <a name="vml-trim-attribute"></a>Атрибут Trim VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, удаляется ли дополнительное пространство выше и ниже текста. Read/write. **Вгтристате**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "Trim: *выражение* " >

**Синтаксис сценария**

*element* . Style. Trim = "*выражение*"

*выражение* = *element*. Style. Trim

**Замечания**

Если **значение — true**, пространство, зарезервированное для верхних и нижних колонтитулов, удаляется. Значение по умолчанию равно **False**.

*Стандартный атрибут VML*

**Пример**

Дополнительное пространство, расположенное выше и ниже, усекается.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 