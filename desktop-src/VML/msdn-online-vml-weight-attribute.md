---
title: Атрибут веса VML
description: Атрибут веса VML
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1a4dc7e33a4a1bf8421350bed9df374f7edd31a1c1a48a2b3e1549dc63084d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999094"
---
# <a name="vml-weight-attribute"></a>Атрибут веса VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет толщину штриха. Read/write. **Строка**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: вес *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Weight = "*выражение*"

*выражение* = *элемент*. вес

**Замечания**

Этот атрибут совпадает с атрибутом **Строкевеигхт** **фигуры** и переопределяет его. Значение по умолчанию — 1 точка.

*Стандартный атрибут VML*

**Пример**

Штрих имеет толщину 5 очков, а не 2 точки.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 