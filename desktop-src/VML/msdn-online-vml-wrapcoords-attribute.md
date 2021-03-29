---
title: Атрибут Врапкурдс VML
description: Атрибут Врапкурдс VML
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792121"
---
# <a name="vml-wrapcoords-attribute"></a>Атрибут Врапкурдс VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет ограничивающий многоугольник, который окружает фигуру. Read/write. **Строка**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:врапкурдс = " *выражение* " >

**Замечания**

Описывает разделенный запятыми список x и икурдинатес; то есть "x1, y1, x2, Y2, X3, Y3,..." Используется, когда текст тесно заключен вокруг фигуры. Значение по умолчанию — **null** (пустая строка), пока атрибуту **MSO-Wrap-Mode** не будет присвоено значение « **плотная** » или « **с**».

*Атрибут расширений Microsoft Office*

**Пример**

Фигура имеет ограничивающий прямоугольник с обтеканием текста 5 единиц, превышающий путь.


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 