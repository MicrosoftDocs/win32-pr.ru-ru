---
title: Атрибут color2 (Stroke) (VML)
description: Атрибут color2 (Stroke) (VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d577843b7d65de4f6197beabc877c308cf00154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488044"
---
# <a name="color2-attribute-strokevml"></a>Атрибут color2 (Stroke) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет второй цвет для штрихов. Read/write. **Строка**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* color2 = " *выражение* " >

Синтаксис сценария

*element* . color2 = "*выражение*"

*выражение* = *element*. color2

**Замечания**

Второй цвет используется, если тип заливки обводки является шаблоном.

*Стандартный атрибут VML*

**Пример**

Обводка фигуры — это заливка узором, где заливка определяется исходным изображением, но прозрачный фон определяется вторым цветом.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 