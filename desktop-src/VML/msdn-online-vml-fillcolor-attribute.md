---
title: Атрибут VML FillColor
description: Атрибут VML FillColor
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e626e017437d14cf1088c188e659e1099dc38c7ba88215438a6c9a45166c7732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601364"
---
# <a name="vml-fillcolor-attribute"></a>Атрибут VML FillColor

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет цвет кисти, которая заполняет замкнутый контур фигуры. Read/write. [Ивгколор](msdn-online-vml-ivgcolor.md) .

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* FillColor = " *выражение* " >

**Синтаксис сценария**

*element* . FillColor = "*выражение*"

*выражение* = *элемент*. FillColor

**Замечания**

Значение **FillColor** дублируется из атрибута **Color** элемента **Fill** .

*Стандартный атрибут VML*

**См. также:**

[Форма](shape-element--vml.md), [Заливка](msdn-online-vml-fill-element.md), [ивгколор](msdn-online-vml-ivgcolor.md)

**Пример**

Цвет заливки прямоугольника — красный.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Пример атрибута FillColor](/previous-versions/bb229668(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 