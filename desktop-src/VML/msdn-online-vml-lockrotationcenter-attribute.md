---
title: Атрибут Локкротатионцентер VML
description: Атрибут Локкротатионцентер VML
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef0cfee24998cfa343265569274ace688a05f90a270b721317394e59589a51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598062"
---
# <a name="vml-lockrotationcenter-attribute"></a>Атрибут Локкротатионцентер VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, задается ли поворот вытянутого объекта атрибутом [ротатионангле](msdn-online-vml-rotationangle-attribute.md) . Read/write. **Вгтристате**.

**Применимо к**:

[Выдавливания](msdn-online-vml-extrusion-element.md)

**Синтаксис тега**

<o: *element* локкротатионцентер = " *выражение* " >

**Синтаксис сценария**

*element* . локкротатионцентер = "*выражение*"

*выражение* = *element*. локкротатионцентер

**Замечания**

Если **значение равно false**, поворот определяется атрибутом [Orientation](msdn-online-vml-orientation-attribute.md) . Значение по умолчанию равно **True**.

Обратите внимание на следующее.


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



тот же самый:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Microsoft Office Extensions, атрибут*

 

 