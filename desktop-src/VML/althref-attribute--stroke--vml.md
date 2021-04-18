---
title: Атрибут Алсреф (Stroke) (VML)
description: Атрибут Алсреф (Stroke) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691622"
---
# <a name="althref-attribute-strokevml"></a>Атрибут Алсреф (Stroke) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Указывает альтернативную ссылку для изображения. Read/write. **Строка**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* о:алсреф = " *выражение* " >

**Синтаксис сценария**

*element* . алсреф = "*выражение*"

*выражение* = *element*. алсреф

**Замечания**

Поддерживает сохранение данных PICT через HTML переносе. При записи в формате HTML альтернативное представление (т. е. исходные данные PICT, если файл был создан из Macintosh) сохраняется. При чтении HTML **алсреф** имеет приоритет над **src**.

*Атрибут расширений Microsoft Office*

**Пример**

Штрих фигуры имеет **алсреф** , указывающий на файл с именем myimage.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 