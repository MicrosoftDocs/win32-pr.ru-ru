---
title: Атрибут Offset (тень) (VML)
description: Атрибут Offset (тень) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0683e9536e10bed141ecca56b4335d6221c5ced7e3d26220908aa388b453843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596909"
---
# <a name="offset-attribute-shadowvml"></a>Атрибут Offset (тень) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, насколько далеко тень расширяется после фигуры. Read/write. **VgVector2D**.

**Применимо к**:

[Shadow](msdn-online-vml-shadow-element.md)

**Синтаксис тега**

<v: смещение *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . offset = "*выражение*"

*выражение* = *элемент*. offset

**Замечания**

Смещение по умолчанию для значения x равно 2pt, а значение по умолчанию для значения y — 2PT. Значения — это либо абсолютное измерение, либо дробное значение Shape. Если дробная часть, они находятся в диапазоне от 50% до-50%.

*Стандартный атрибут VML*

**Пример**

Фигура имеет тень со смещением 5 пунктов вниз и 10 точками вправо.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 