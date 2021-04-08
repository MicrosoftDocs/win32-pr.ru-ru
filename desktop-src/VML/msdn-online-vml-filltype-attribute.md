---
title: Атрибут объекта FillType VML
description: Атрибут объекта FillType VML
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987861"
---
# <a name="vml-filltype-attribute"></a>Атрибут объекта FillType VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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
| Модель   | Изображение заливки растягивается для формирования шаблона. |
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



 

 