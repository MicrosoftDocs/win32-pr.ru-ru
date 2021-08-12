---
title: Атрибут VML Layout-Flow
description: Атрибут VML Layout-Flow
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde6937a3f93ff2a462cfc5950c13b7f3910573c54d82449ef705bca4afbb068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599358"
---
# <a name="vml-layout-flow-attribute"></a>Атрибут VML Layout-Flow

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет поток макета текста в текстовом поле. Read/write. **Строка**.

**Применимо к**:

[TextBox](msdn-online-vml-textbox-element.md)

**Синтаксис тега**

<v: Style *элемента* = "макет-Flow: *выражение* " >

**Замечания**

К этим значениям относятся следующие.



| Значение                  | Описание                                 |
|------------------------|---------------------------------------------|
| horizontal             | Текст отображается горизонтально. По умолчанию.    |
| Вертикаль               | Текст отображается вертикально.               |
| по вертикали-идеографические   | Идеографическая текст отображается вертикально.   |
| горизонтально-идеографические | Идеографическая текст отображается горизонтально. |



 

*Стандартный атрибут VML*

**Пример**

Поток текста в текстовом поле будет передаваться по вертикали.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 