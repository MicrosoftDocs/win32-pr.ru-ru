---
title: Атрибут оттенков VML
description: Атрибут оттенков VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413174"
---
# <a name="vml-grayscale-attribute"></a>Атрибут оттенков VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли изображение отображаться в режиме градаций серого. Read/write. **Вгтристате**.

**Применимо к**:

[ImageData](msdn-online-vml-imagedata-element.md)

**Синтаксис тега**

<v: градации серого *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . градации серого = "*выражение*"

*выражение* = *element*. оттенки серого

**Замечания**

Если **значение — true**, изображение будет отображаться в оттенках серого вместо цвета. По умолчанию **False**.

Значение основано на КЦИР рекомендации 709, что соответствует более зеленому весу и дает более привлекательные результаты для естественного цвета.

*Стандартный атрибут VML*

**Пример**

Изображение будет отображаться в оттенках серого вместо цвета.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 