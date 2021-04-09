---
title: Атрибут StartAngle в формате VML
description: Атрибут StartAngle в формате VML
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070249"
---
# <a name="vml-startangle-attribute"></a>Атрибут StartAngle в формате VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет начальную точку дуги. Чтение и запись. [Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md) .

**Применимо к**:

[Arc](msdn-online-vml-arc-element.md)

**Синтаксис тега**

<v: *element* ендангле = " *выражение* " >

**Синтаксис сценария**

*element* . ендангле = "*выражение*"

*выражение* = *element*. ендангле

**Замечания**

Дуга определяется как штрих, нарисованный вдоль овала, ограниченного атрибутами **стиля** фигуры. Начало штриха определяется углом, измеренным с начала (12 часов) по часовой стрелке. Значение по умолчанию — 0 градусов.

Стандартный атрибут VML

**Пример**

Дуга является улыбкой. Начальная точка находится на точке 90 градусов вписанный внутри прямоугольника, ограничивающего фигуру. Конечная точка находится в точке овала в 270 градусов.


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 