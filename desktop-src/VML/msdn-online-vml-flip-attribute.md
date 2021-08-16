---
title: Атрибут перелистывания VML
description: Атрибут перелистывания VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5293bdff5ab888b13fdc095038e74fdbcf725bbfb1948a04018fbf5a22c5677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346638"
---
# <a name="vml-flip-attribute"></a>Атрибут перелистывания VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Переключает ориентацию фигуры. Read/write. **Строка**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *элемент* Style = "отражение: *выражение* " >

**Синтаксис сценария**

*element* . Style. reпереворот = "*выражение*"

*выражение* = *element*. Style. переворот

**Замечания**

К этим значениям относятся следующие.



| Значение | Описание                                           |
|-------|-------------------------------------------------------|
| x     | Поворачивает вдоль оси y, отменяя координаты *x*. |
| y     | Переверните по оси *x*, отменив координаты y. |
| xy    | Переразите по осям y и *x*.                  |
| икс    | Переразите по оси *x* и *y*.                |



 

*Стандартный атрибут VML*

**См. также:**

[вгфлипориентатион](msdn-online-vector-markup-language-object-model-reference.md)

**Пример**

Фигура перемещается вдоль оси *y* путем обращения к координатам *x* .


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Пример атрибута для отражения](/previous-versions/bb229670(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 