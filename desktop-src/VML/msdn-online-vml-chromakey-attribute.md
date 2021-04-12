---
title: Атрибут Чромакэй VML
description: Атрибут Чромакэй VML
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338140"
---
# <a name="vml-chromakey-attribute"></a>Атрибут Чромакэй VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет значение цвета изображения, которое будет считаться прозрачным. Read/write. **Вгколор**.

**Применимо к**:

[ImageData](msdn-online-vml-imagedata-element.md)

**Синтаксис тега**

<v: *element* чромакэй = " *выражение* " >

**Синтаксис сценария**

*element* . чромакэй = "*выражение*"

*выражение* = *element*. чромакэй

**Замечания**

Используйте этот атрибут, чтобы сделать части изображения прозрачными с помощью ключа прозрачности к определенному цвету. Например, если сделать значение **чромакэй** **черным**, то любая часть изображения, которая является черновой, будет прозрачной, а цвет заливки будет отображаться в этой части изображения.

*Стандартный атрибут VML*

**Пример**

Области изображения со сплошным черным цветом становятся прозрачными, что позволяет отображать зеленый цвет заливки через эти области.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 