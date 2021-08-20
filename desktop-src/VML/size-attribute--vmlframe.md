---
title: Атрибут size (Вмлфраме)
description: Атрибут size (Вмлфраме)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32d496bc40b5b84b7a8a16bf6b84a2926010d56dcc311659dd63300363a7067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754129"
---
# <a name="size-attribute-vmlframe"></a>Атрибут size (Вмлфраме)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 