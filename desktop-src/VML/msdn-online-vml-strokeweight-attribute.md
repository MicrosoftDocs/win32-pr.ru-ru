---
title: Атрибут Строкевеигхт VML
description: Атрибут Строкевеигхт VML
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac5efa964607fdd942c8dff31a4a124d424aa5fbfeede27abc6164fddef087
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680684"
---
# <a name="vml-strokeweight-attribute"></a>Атрибут Строкевеигхт VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет толщину кисти, которая обозначает контур фигуры. Read/write. **Вгленгс**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* строкевеигхт = " *выражение* " >

**Синтаксис сценария**

*element* . строкевеигхт = "*выражение*"

*выражение* = *element*. строкевеигхт

**Замечания**

Значение дублируется из атрибута **веса** элемента **Stroke** . Если указано число, но никакие единицы измерения не добавляются, то по умолчанию единицей измерений является ЕС. Если значение не указано, по умолчанию используется 1 пиксель (1px).

Однако для сценариев единицей измерения по умолчанию является точка.

*Стандартный атрибут VML*

**См. также:**

[Stroke](msdn-online-vml-stroke-element.md), [ивгленгс](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)

**Пример**

Толщина штриха фигуры равна 1 пункту.


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Пример атрибута строкевеигхт](/previous-versions/bb264095(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 