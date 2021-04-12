---
title: Атрибут Type (shadow) (VML)
description: Атрибут Type (shadow) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413310"
---
# <a name="type-attribute-shadowvml"></a>Атрибут Type (shadow) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Задает тип тени. Read/write. **Строка**.

**Применимо к**:

[Shadow](msdn-online-vml-shadow-element.md)

**Синтаксис тега**

<v: *element* Type = " *выражение* " >

**Синтаксис сценария**

*element* . Type = "*выражение*"

*выражение* = *element*. Type

**Замечания**

К этим значениям относятся следующие.



| Значение           | Описание                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| single          | Одна тень. По умолчанию.                                                                                                                                                                              |
| double          | Двойная тень. [Color2](color2-attribute--shadow--vml.md) используется для цвета второй тени и [Offset2](msdn-online-vml-offset2-attribute.md) используется для смещения второй тени. |
| перспектива     | Тень перспективы.                                                                                                                                                                                |
| шаперелативе   | Тень создается относительно фигуры.                                                                                                                                                         |
| дравингрелативе | Тень создается относительно рисунка.                                                                                                                                                       |
| поднят          | Тень выглядит приподнятой.                                                                                                                                                                     |



 

**Стандартный атрибут VML**

**Пример**

Двойная тень создается со второй тенью зеленого цвета и смещением 5 точек вниз и вправо.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 