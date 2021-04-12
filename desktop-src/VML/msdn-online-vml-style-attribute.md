---
title: Атрибут стиля VML
description: Атрибут стиля VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487765"
---
# <a name="vml-style-attribute"></a>Атрибут стиля VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет стиль рамки. Read/write. **Строка**.

**Применимо к**:

[вмлфраме](msdn-online-vml-vmlframe-element.md)

**Синтаксис тега**

<v: Style *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Style = "*выражение*"

*выражение* = *элемент*. Style

**Замечания**

Этот атрибут использует обычные атрибуты стиля CSS для позиционирования.

*Стандартный атрибут VML*

**Пример**

Стиль определяет фактическую точку кадра.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 