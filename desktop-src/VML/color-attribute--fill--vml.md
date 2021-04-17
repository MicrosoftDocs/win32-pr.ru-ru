---
title: Атрибут цвета (Fill) (VML)
description: Атрибут цвета (Fill) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487773"
---
# <a name="color-attribute-fillvml"></a>Атрибут цвета (Fill) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет цвет заливки. Read/write. **Вгколор**.

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: Color *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Color = "*выражение*"

*выражение* = *элемент*. Color

**Замечания**

Переопределяет атрибут **FillColor** фигуры. Значение по умолчанию — **белый**.

*Стандартный атрибут VML*

**Пример**

Цвет заливки фигуры — зеленый.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 