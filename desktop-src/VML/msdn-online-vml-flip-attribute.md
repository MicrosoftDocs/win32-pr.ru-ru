---
title: Атрибут перелистывания VML
description: Атрибут перелистывания VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793759"
---
# <a name="vml-flip-attribute"></a>Атрибут перелистывания VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Переключает ориентацию фигуры. Read/write. **Строка**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

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
| да     | Переверните по оси *x*, отменив координаты y. |
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

 

 