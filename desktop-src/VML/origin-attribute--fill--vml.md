---
title: Начальный атрибут (Fill) (VML)
description: Начальный атрибут (Fill) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413640"
---
# <a name="origin-attribute-fillvml"></a>Начальный атрибут (Fill) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет центр изображения заливки. Read/write. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: *элемент* Origin = " *выражение* " >

**Синтаксис сценария**

*element* . Origin = "*выражение*"

*выражение* = *элемент*. Origin

**Замечания**

Задает точку относительно верхнего левого угла изображения; Этот момент рассматривается как источник изображения. По умолчанию используется центр изображения. Вектор представляет собой часть ширины и высоты изображения.

*Стандартный атрибут VML*

**Пример**

Изображение заливки смещается влево до точки 50% ширины фигуры.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 