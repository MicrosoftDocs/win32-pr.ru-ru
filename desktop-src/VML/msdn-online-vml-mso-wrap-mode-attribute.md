---
title: Атрибут VML MSO-Mode
description: Атрибут VML MSO-Mode
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e3743522b9286da8a7f30e9100e06205430b1b18fa3c62def60b57f54b65d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136987"
---
# <a name="vml-mso-wrap-mode-attribute"></a>Атрибут VML MSO-Mode

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет режим переноса текста. Read/write. **Строка**.

**Применимо к**:

[Фигура](shape-element--vml.md)

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



 

используется в Microsoft PowerPoint для сохранения в формате HTML, чтобы указать, включено ли перетекание слов в автофигуре (**квадрат**) или выключено (**нет**).

*Microsoft Office Extensions, атрибут*

**Пример**

Следующий код указывает, что функция WordWrap внутри автофигуры включена в PowerPoint.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 