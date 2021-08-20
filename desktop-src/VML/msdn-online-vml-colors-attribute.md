---
title: Атрибут Colors VML
description: Атрибут Colors VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a699b0ab8da898dd82fa4e1bf4823c0f9fdd443eb8275e25dbfaac6d2f039a6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999284"
---
# <a name="vml-colors-attribute"></a>Атрибут Colors VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет несколько цветов для градиентной заливки. Read/write. **Ивгградиентколораррай**.

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: Colors *Elements* = " *Expression* " >

**Синтаксис сценария**

*element* . Colors = "*выражение*"

*выражение* = *element*. Colors

**Замечания**

Используется для определения массива, состоящего из парных значений процентов ([вгфрактион](msdn-online-vml-vgfraction-data-type.md)) и Color ([вгколор](msdn-online-vml-ivgcolor.md)). Массив создает наложенную заливку с использованием каждой точки в массиве, начиная с 0% (определяется **цветом**) и заканчивая 100% (определяется с помощью **color2**). Промежуточные цвета, определяемые способом, можно определить, назначив значение цвета в процентах. Пара "процент и цвет" отделяется запятой, но пары разделяются друг от друга запятыми.

Стандартный атрибут VML

**Пример**

Фигура имеет градиентную заливку, состоящую из четырех цветов, начинающихся с красного цвета, смешения к желтому, зеленому и финаллиблуе.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 