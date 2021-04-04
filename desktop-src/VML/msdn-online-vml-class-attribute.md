---
title: Атрибут класса VML
description: Атрибут класса VML
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987674"
---
# <a name="vml-class-attribute"></a>Атрибут класса VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Ссылается на определение стиля CSS. Read/write. **Строка**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* Class = " *выражение* " >

**Синтаксис сценария**

*element* . ClassName = "*выражение*"

*выражение* = *element*. classname

**Замечания**

Атрибут **Class** аналогичен стандартному атрибуту **класса** HTML, используемому в таблицах стилей CSS.

Обратите внимание, что вместо **класса** для создания скриптов используется **className** . Кроме того, обратите внимание, что для сценариев можно только прочитать **className** . изменение значения **className** не приведет к изменению отрисовки фигуры.

*Стандартный атрибут VML*

**См. также:**

[Фигурная](shape-element--vml.md)

**Пример**

Класс для **Width** создается с использованием стиля


```HTML
   .narrowstyle {width:50;height:100}
```



Затем на ширину добавляется ссылка, включающая стиль. Обратите внимание, что ширина андхеигхт не определена в атрибуте **Style** , но будет определяться стилем.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Обратите внимание, что **класс** применяется только к атрибутам типа CSS.

 

 