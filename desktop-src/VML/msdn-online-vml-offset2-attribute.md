---
title: Атрибут Offset2 VML
description: Атрибут Offset2 VML
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533437"
---
# <a name="vml-offset2-attribute"></a>Атрибут Offset2 VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет второе смещение. Read/write. **VgVector2D**.

**Применимо к**:

[Shadow](msdn-online-vml-shadow-element.md)

**Синтаксис тега**

<v: *element* offset2 = " *выражение* " >

**Синтаксис сценария**

*element* . offset2 = "*выражение*"

*выражение* = *element*. offset2

**Замечания**

Значение по умолчанию для второго смещения для значения x равно 0, а значение по умолчанию для значения y равно 0. Значения — это либо абсолютное измерение, либо дробное значение Shape. Если дробная часть, значения находятся в диапазоне от 50% до-50%.

Используйте второе смещение для создания специальных эффектов тени. Дополнительные сведения о втором смещении см. в описании атрибута [Type](type-attribute--shadow--vml.md) .

*Стандартный атрибут VML*

**Пример**

Для фигуры создается двойная тень.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 