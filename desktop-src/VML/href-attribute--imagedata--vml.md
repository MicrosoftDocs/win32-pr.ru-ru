---
title: Атрибут HRef (Имажедата) (VML)
description: Атрибут HRef (Имажедата) (VML)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791724"
---
# <a name="href-attribute-imagedatavml"></a>Атрибут HRef (Имажедата) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет URL-адрес изображения. Read/write. **Строка**.

**Применимо к**:

[ImageData](msdn-online-vml-imagedata-element.md)

**Синтаксис тега**

<v: *element* о:хреф = " *выражение* " >

**Синтаксис сценария**

*element* . href = "*выражение*"

*выражение* = *element*. href

**Замечания**

Когда вы щелкните фигуру, браузер загрузит URL-адрес. Атрибут **href** аналогичен стандартному атрибуту HTML **href** привязок.

Использование этого атрибута упрощает создание буттонсвис изображений на веб-странице.

Этот атрибут используется Microsoft Office только в том случае, если рисунок связан и внедрен. Microsoft Word имеет пользовательский интерфейс для вставки рисунков таким образом.

*Атрибут расширений Microsoft Office*

**Пример**

Когда вы щелкните изображение, браузер загрузит домашнюю страницу корпорации Майкрософт.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 