---
title: Атрибут фокусировки VML
description: Атрибут фокусировки VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070599"
---
# <a name="vml-focus-attribute"></a>Атрибут фокусировки VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет центр заливки линейного градиента. Read/write. **Вгфрактион**.

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: *элемент* Focus = " *выражение* " >

**Синтаксис сценария**

*element* . Focus = "*выражение*"

*выражение* = *element*. Focus

**Замечания**

Определяет начальную координату центра Blend. Диапазон значений — от 100% до-100%. Значение по умолчанию — 0. Значение 100% (или-100%) переместит фокус, чтобы направление смешения было обратным (в силе **Color** и **color2**). Значение 50% изменит смешение, чтобы **Цвет** **наColor2ся** на концах, а в середине —. Значение-50% изменит смешение, чтобы **color2** на обоих концах, а **Цвет** — в середине.

*Стандартный атрибут VML*

**Пример**

Фокус градиента заливки смещается таким образом, что красный **Цвет (Color**) будет полосой в центре фигуры, а верхняя и Нижняя будут синими (**color2**).


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 