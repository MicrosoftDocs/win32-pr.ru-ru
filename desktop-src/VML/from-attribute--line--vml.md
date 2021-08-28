---
title: Из атрибута (line) (VML)
description: Из атрибута (line) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a8bf41462f698397b193835d08655f8d6acefb2df77b17e035ec170c3c4781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099314"
---
# <a name="from-attribute-linevml"></a>Из атрибута (line) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет начальную точку линии. Read/write. **VgVector2D**.

**Применимо к**:

[Линия](msdn-online-vml-line-element.md)

**Синтаксис тега**

<v: *элемент* из = " *выражение* " >

**Синтаксис сценария**

*element* . from = "*выражение*"

*выражение* = *элемент*. from

**Замечания**

Определяет начальную точку линии в пространстве координат родительского элемента. Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC). Значение по умолчанию — 0, 0.

*Стандартный атрибут VML*

**Пример**

Линия начинается с позиции 10, а затем на 10 пунктов справа от верхнего левого угла родительского пространства.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 