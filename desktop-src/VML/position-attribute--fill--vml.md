---
title: Атрибут расположения (Заливка) (VML)
description: Атрибут расположения (Заливка) (VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134503"
---
# <a name="position-attribute-fillvml"></a>Атрибут расположения (Заливка) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет расположение изображения заливки. Read/write. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: расположение *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Disposition = "*выражение*"

*выражение* = *element*. позиционировать

**Замечания**

Задает точку в фигуре для позиционирования начала изображения. По умолчанию используется центр прямоугольника контейнера. Вектор представляет собой часть ширины и высоты изображения.

*Стандартный атрибут VML*

**Пример**

Изображение заливки смещается вправо до точки 50% ширины фигуры.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 