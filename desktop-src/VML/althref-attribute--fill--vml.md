---
title: Атрибут Алсреф (Fill) (VML)
description: Атрибут Алсреф (Fill) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181f98ace80403668f8f67c6f8412091271fdfcf2abcb5a1320d0685853d92bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603007"
---
# <a name="althref-attribute-fillvml"></a>Атрибут Алсреф (Fill) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет альтернативную ссылку для изображения. Read/write. **Строка**.

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: *element* о:алсреф = " *выражение* " >

**Синтаксис сценария**

*element* . алсреф = "*выражение*"

*выражение* = *element*. алсреф

**Замечания**

Поддерживает сохранение данных PICT через HTML переносе. При записи в формате HTML альтернативное представление (исходные данные PICT, если файл был создан из Apple Macintosh) сохраняется. При чтении HTML **алсреф** имеет приоритет над **src**.

*Microsoft Office Extensions, атрибут*

**Пример**

Заливка фигуры имеет **алсреф** , указывающую на файл с именем myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 