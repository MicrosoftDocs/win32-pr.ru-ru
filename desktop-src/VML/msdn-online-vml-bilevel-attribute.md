---
title: Атрибут Билевел VML
description: Атрибут Билевел VML
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b84f77777cfa21a5bd5c80cb59e447c5a5ce1da78875cc9bd5ff07548690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602874"
---
# <a name="vml-bilevel-attribute"></a>Атрибут Билевел VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли изображение отображаться черно-белым цветом. Read/write. **Вгтристате**.

**Применимо к**:

[ImageData](msdn-online-vml-imagedata-element.md)

**Синтаксис тега**

<v: *element* билевел = " *выражение* " >

**Синтаксис сценария**

*element* . билевел = "*выражение*"

*выражение* = *element*. билевел

**Замечания**

Если **значение — true**, изображение будет отображаться с использованием двух цветов (черный и белый). По умолчанию **False**. При этом создается результат, аналогичный афише.

*Стандартный атрибут VML*

**Пример**

Изображение будет отображаться только в черно-белом режиме.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 