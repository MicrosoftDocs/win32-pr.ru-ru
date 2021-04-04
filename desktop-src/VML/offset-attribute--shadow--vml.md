---
title: Атрибут Offset (тень) (VML)
description: Атрибут Offset (тень) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987574"
---
# <a name="offset-attribute-shadowvml"></a>Атрибут Offset (тень) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 