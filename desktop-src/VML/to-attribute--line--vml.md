---
title: К атрибуту (line) (VML)
description: К атрибуту (line) (VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793747"
---
# <a name="to-attribute-linevml"></a>К атрибуту (line) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет конечную точку линии. Read/write. **VgVector2D**.

**Применимо к**:

[Line](msdn-online-vml-line-element.md)

**Синтаксис тега**

<v: *element* to = " *выражение* " >

**Синтаксис сценария**

*element* . to = "*выражение*"

*выражение* = *element*. to

**Замечания**

Определяет конечную точку линии в пространстве координат родительского элемента. Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC). Значение по умолчанию — 10, 10.

**Стандартный атрибут VML**

**Пример**

Линия заканчивается в расположении 100 указывает на угол вниз, а 100 указывает на право верхнего левого угла родительского пространства.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 