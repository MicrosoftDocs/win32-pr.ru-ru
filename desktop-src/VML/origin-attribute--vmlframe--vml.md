---
title: Атрибут Origin (Вмлфраме) (VML)
description: Атрибут Origin (Вмлфраме) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874b857a2408927e296f82f0f9aa0a5e15f6da69b1e2af6eaf6ebe2c5df746d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768264"
---
# <a name="origin-attribute-vmlframevml"></a>Атрибут Origin (Вмлфраме) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет источник области обрезки кадра. Read/write. **VgVector2D**.

**Применимо к**:

[вмлфраме](msdn-online-vml-vmlframe-element.md)

**Синтаксис тега**

<v: *элемент* Origin = " *выражение* " >

**Синтаксис сценария**

*element* . Origin = "*выражение*"

*выражение* = *элемент*. Origin

**Замечания**

Значение по умолчанию — 0, 0. Обратите внимание, что **источник** работает, только если функция [Clip](msdn-online-vml-clip-attribute.md) имеет **значение true**. В этом атрибуте источник определяется как левый верхний угол рамки.

*Стандартный атрибут VML*

**Пример**

Источником вырезанной области является 100pt, 100pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 