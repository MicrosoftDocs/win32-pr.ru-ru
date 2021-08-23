---
title: Атрибут Type (shadow) (VML)
description: Атрибут Type (shadow) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90a264cbaf77890e39f10d56103c8acdc84727de21d7f2de9946911b6df41dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513164"
---
# <a name="type-attribute-shadowvml"></a>Атрибут Type (shadow) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 