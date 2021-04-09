---
title: Атрибут размера (Fill) (VML)
description: Атрибут размера (Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987573"
---
# <a name="size-attribute-fillvml"></a>Атрибут размера (Fill) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет размер изображения для заливки. Read/write. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: size *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . size = "*выражение * * *"**

*выражение* = *элемент*. размер

**Замечания**

Значение по умолчанию — размер исходного изображения. Размеры, превышающие размер шапевилл, отображают увеличенную, но обрезанную версию изображения.

*Стандартный атрибут VML*

**Пример**

Несмотря на то, что исходный размер изображения составляет 50 точек по 50, изображение будет отображаться в центре заливки в виде 10-на 10 изображений.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 