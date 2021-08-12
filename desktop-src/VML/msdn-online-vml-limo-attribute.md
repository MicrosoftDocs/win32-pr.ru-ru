---
title: Атрибут Лимо VML
description: Атрибут Лимо VML
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa99325f396a3e4709fcd7ca1ee6ee82df1b653dff50df56df2df06ef2d513ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598314"
---
# <a name="vml-limo-attribute"></a>Атрибут Лимо VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет точку растяжения на пути. Read/write. **Vector2D**.

**Применимо к**:

[Путь](msdn-online-vml-path-element.md)

**Синтаксис тега**

<v: *element* Лимо = " *выражение* " >

**Синтаксис сценария**

*element* . Лимо = "*выражение*"

*выражение* = *element*. Лимо

**Замечания**

Значение по умолчанию — "0 0". Растягивание Лимо — это точки на границе фигуры, которые определяют, где и как можно растянуть фигуру пользователя в графическом редакторе.

*Стандартный атрибут VML*

**Пример**

Точка растяжения Лимо определяется вдоль горизонтальной линии.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 