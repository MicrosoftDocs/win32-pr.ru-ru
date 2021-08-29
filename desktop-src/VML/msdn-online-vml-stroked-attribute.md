---
title: Атрибут VML Stroke
description: Атрибут VML Stroke
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9398452365ee6076309cafa40c0373dcaa12d52a868e71eb77e4b42780badb0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754449"
---
# <a name="vml-stroked-attribute"></a>Атрибут VML Stroke

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли контур обводкам. Read/write. [Вгтристате](msdn-online-vml-vgtristate.md) .

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* с обводкой = " *выражение* " >

**Синтаксис сценария**

*element* . strokeed = "*выражение*"

*выражение* = *элемент*. strokeed

**Замечания**

Значение дублируется из атрибута **On** элемента [Stroke](msdn-online-vml-stroke-element.md) .

*Стандартный атрибут VML*

**Пример**

Контур фигуры является обводкой.


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Пример атрибута с обводкой](/previous-versions/bb264094(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 