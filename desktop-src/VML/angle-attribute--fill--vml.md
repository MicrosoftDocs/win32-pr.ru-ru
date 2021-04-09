---
title: Атрибут Angle (Заливка) (VML)
description: Атрибут Angle (Заливка) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070532"
---
# <a name="angle-attribute-fillvml"></a>Атрибут Angle (Заливка) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет угол градиентной заливки. Read/write. [Вгангле](msdn-online-vml-vgangleindegrees-data-type.md) .

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: Angle *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Angle = "*выражение*"

*выражение* = *элемент*. угол

**Замечания**

Вектор градиента перпендикулярен вектору направления смешения от одного цвета к другому. Значение по умолчанию — 0 (нуль) градусов, то есть горизонтальный вектор слева направо. Положительные углы поворачивают градиент в направлении против часовой стрелки.

*Стандартный атрибут VML*

**Пример**

Заливка фигуры состоит из градиента двух цветов: от синего к красному по углу 45 градусов. Красный будет находиться в левом верхнем углу, а синий — в нижнем правом углу.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 