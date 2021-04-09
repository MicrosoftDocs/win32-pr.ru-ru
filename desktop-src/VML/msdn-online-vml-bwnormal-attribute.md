---
title: Атрибут Бвнормал VML
description: Атрибут Бвнормал VML
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070212"
---
# <a name="vml-bwnormal-attribute"></a>Атрибут Бвнормал VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет режим черно-белого цвета для обычных черно-белых выходных устройств. Read/write. [Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:бвнормал = " *выражение* " >

**Замечания**

Если для [бвмоде](msdn-online-vml-bwmode-attribute.md) задано значение **Auto**, этот атрибут используется для определения способа отрисовки фигуры в нормальном черном и белом режиме.

Дополнительные сведения о значениях этого атрибута см. в разделе [вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md) . Значение по умолчанию — **Auto**.

*Атрибут расширений Microsoft Office*

**Пример**

Фигура обрабатывается как изображение в градациях серого для обычных черно-белых выходных данных.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 