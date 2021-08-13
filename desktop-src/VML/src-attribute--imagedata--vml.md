---
title: Атрибут src (Имажедата) (VML)
description: Атрибут src (Имажедата) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688bc1e82afbaf0747a03465c93feb1d760cc60eb441792654ef11ec59cee749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596686"
---
# <a name="src-attribute-imagedatavml"></a>Атрибут src (Имажедата) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет источник изображения. Read/write. **Строка**.

**Применимо к**:

[ImageData](msdn-online-vml-imagedata-element.md)

**Синтаксис тега**

<v: *элемент* src = " *выражение* " >

**Синтаксис сценария**

*element* . src = "*выражение*"

*выражение* = *элемент*. src

**Замечания**

Этот атрибут должен всегда использоваться с элементом [имажедата](msdn-online-vml-imagedata-element.md) и указывать на допустимые данные изображения для отображения изображения. Если этот атрибут отображается без [href](https://www.bing.com/search?q=HRef) или [Title](title-attribute--imagedata--vml.md), то это изображение связывается.

*Стандартный атрибут VML*

**Пример**

Источником изображения является файл с именем "kids.jpg".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 