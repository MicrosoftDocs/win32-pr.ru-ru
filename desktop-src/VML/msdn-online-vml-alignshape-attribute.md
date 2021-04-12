---
title: Атрибут Алигншапе VML
description: Атрибут Алигншапе VML
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339028"
---
# <a name="vml-alignshape-attribute"></a>Атрибут Алигншапе VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли изображение согласовываться с фигурой. Read/write. **Вгтристате**.

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: *element* алигншапе = " *выражение* " >

**Синтаксис сценария**

*element* . алигншапе = "*выражение*"

*выражение* = *element*. алигншапе

**Замечания**

Если **значение — true**, изображение, используемое для создания заливки, будет согласовываться с фигурой. Если задано **значение false**, то изображение, используемое для создания заливки, будет согласовываться с окном. Значение по умолчанию — **True**.

*Стандартный атрибут VML*

**Пример**

Изображение мозаичной заливки, созданное из myimage.gif, согласуется с окном, а не с фигурой. Несмотря на то, что фигура поворачивается, изображение — нет.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 