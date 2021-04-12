---
title: Атрибут VML MSO-Mode
description: Атрибут VML MSO-Mode
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338092"
---
# <a name="vml-mso-wrap-mode-attribute"></a>Атрибут VML MSO-Mode

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет режим переноса текста. Read/write. **Строка**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: Style *элемента* = "MSO-Wrap-Mode: *Expression* " >

**Замечания**

К этим значениям относятся следующие.



| Значение          | Описание                          |
|----------------|--------------------------------------|
| square         | Заключает текст вокруг фигуры в квадрат. |
| тесная          | Текст переносится вблизи фигуры.  |
| сверху вниз | Текст переходит сверху вниз.       |
| по        | Текст отображается через фигуру.     |
| нет           | Текст не переносится.                   |



 

Используется в Microsoft PowerPoint для сохранения в формате HTML, чтобы указать, включено ли перетекание слов в автофигуре (**квадрат**) или выключено (**нет**).

*Атрибут расширений Microsoft Office*

**Пример**

Следующий код показывает, что в PowerPoint включена функция переноса слов в автофигуре.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 