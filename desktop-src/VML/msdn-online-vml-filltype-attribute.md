---
title: Атрибут объекта FillType VML
description: Атрибут объекта FillType VML
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0264fe6cd8cd3dfb7592aea25ef855fda01632647b23f0ab2cffe84c4c504918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680804"
---
# <a name="vml-filltype-attribute"></a>Атрибут объекта FillType VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет тип заливки, используемый для фона штриха. Read/write. **Вгфиллтипе**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* объекта FillType = " *выражение* " >

**Синтаксис сценария**

*element* . объекта FillType = "*выражение*"

*выражение* = *element*. объекта FillType

**Замечания**

К этим значениям относятся следующие.



| DashStyle | Описание                                    |
|-----------|------------------------------------------------|
| Сплошная     | Шаблон заливки является сплошным. Значение по умолчанию.      |
| Tile      | Изображение заливки заполняется мозаикой.                       |
| Шаблон   | Изображение заливки растягивается для формирования шаблона. |
| Frame     | Изображение заливки превращается в границу фигуры. |



 

*Стандартный атрибут VML*

**Пример**

Штрих фигуры имеет мозаичную текстуру, созданную на основе изображения cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 