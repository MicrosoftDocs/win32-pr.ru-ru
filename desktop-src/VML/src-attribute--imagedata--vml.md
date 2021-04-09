---
title: Атрибут src (Имажедата) (VML)
description: Атрибут src (Имажедата) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070067"
---
# <a name="src-attribute-imagedatavml"></a>Атрибут src (Имажедата) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 