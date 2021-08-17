---
title: Атрибут Бвнормал VML
description: Атрибут Бвнормал VML
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2811a9cd734e0f2ca6ca2f707b6313d7434ac756a1f9cd8982d7179c75748bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754959"
---
# <a name="vml-bwnormal-attribute"></a>Атрибут Бвнормал VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет режим черно-белого цвета для обычных черно-белых выходных устройств. Read/write. [Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:бвнормал = " *выражение* " >

**Замечания**

Если для [бвмоде](msdn-online-vml-bwmode-attribute.md) задано значение **Auto**, этот атрибут используется для определения способа отрисовки фигуры в нормальном черном и белом режиме.

Дополнительные сведения о значениях этого атрибута см. в разделе [вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md) . Значение по умолчанию — **Auto**.

*Microsoft Office Extensions, атрибут*

**Пример**

Фигура обрабатывается как изображение в градациях серого для обычных черно-белых выходных данных.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 