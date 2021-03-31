---
title: Атрибут size (Вмлфраме)
description: Атрибут size (Вмлфраме)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070068"
---
# <a name="size-attribute-vmlframe"></a>Атрибут size (Вмлфраме)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет размер области обрезки рамки. Read/write. **VgVector2D**.

**Применимо к**:

[вмлфраме](msdn-online-vml-vmlframe-element.md)

**Синтаксис тега**

<v: size *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . size = "*выражение*"

*выражение* = *элемент*. размер

**Замечания**

Значение по умолчанию — 0, 0. Обратите внимание, что **size** работает, только если функция [Clip](msdn-online-vml-clip-attribute.md) имеет **значение true**. В этом атрибуте размер определяется как ширина и высота рамки.

*Стандартный атрибут VML*

**Пример**

Размер области отсечения будет 50Pt, 50Pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 