---
title: Атрибут src (Fill) (VML)
description: Атрибут src (Fill) (VML)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487761"
---
# <a name="src-attribute-fillvml"></a>Атрибут src (Fill) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет изображение, которое загружается для заполнения. Read/write. **Строка**.

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: *элемент* src = " *выражение* " >

**Синтаксис сценария**

*element* . src = "*выражение * * *"**

*выражение* = *элемент*. src

**Замечания**

URL-адрес изображения, загружаемого для изображений и узорных заливок. Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения. Если этот атрибут встречается отдельно (то есть отсутствует атрибут **href** или **Title** ), то изображение связывается.

*Стандартный атрибут VML*

**Пример**

Отображается мозаичное изображение, использующее файл myimage.gif в качестве источника.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 