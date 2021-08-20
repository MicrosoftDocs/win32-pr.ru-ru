---
title: Атрибут цвета (Fill) (VML)
description: Атрибут цвета (Fill) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ec72cab0562ae675ca2e22992369a7c0ad6534207cd2a6f6141f56c64e2f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125384"
---
# <a name="color-attribute-fillvml"></a>Атрибут цвета (Fill) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 