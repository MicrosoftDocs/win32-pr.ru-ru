---
title: Атрибут color2 (Fill) (VML)
description: Атрибут color2 (Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e651245ddf9fb2a3669c3529038b5d0d8cbb3922b8a112c201858d2efd786a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007894"
---
# <a name="color2-attribute-fillvml"></a>Атрибут color2 (Fill) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет второй цвет для заливок. Read/write. [Вгколор](msdn-online-vml-ivgcolor.md) .

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: *element* color2 = " *выражение* " >

**Синтаксис сценария**

*element* . color2 = "*выражение*"

*выражение* = *element*. color2

**Замечания**

Второй цвет используется, если тип заливки является шаблоном или градиентом. Значение по умолчанию — **белый**.

*Стандартный атрибут VML*

**Пример**

Тип заливки фигуры — это шаблон, где Заливка переднего плана определяется исходным изображением, но прозрачный фон определяется вторым цветом.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 