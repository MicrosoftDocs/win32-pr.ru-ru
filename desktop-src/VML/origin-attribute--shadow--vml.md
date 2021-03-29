---
title: Атрибут Origin (тень) (VML)
description: Атрибут Origin (тень) (VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793645"
---
# <a name="origin-attribute-shadowvml"></a>Атрибут Origin (тень) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет центр тени. Read/write. **VgVector2D**.

**Применимо к**:

[Shadow](msdn-online-vml-shadow-element.md)

**Синтаксис тега**

<v: *элемент* Origin = " *выражение* " >

**Синтаксис сценария**

*element* . Origin = "*выражение*"

*выражение* = *элемент*. Origin

**Замечания**

Пара дробных значений фигуры в диапазоне от 50% до-50%. Значение по умолчанию — 0, 0.

*Стандартный атрибут VML*

**Пример**

Тень имеет начало координат, равное 20% вниз и 20% справа от начала координат фигуры.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 