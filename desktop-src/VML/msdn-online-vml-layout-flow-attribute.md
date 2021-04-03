---
title: Атрибут VML Layout-Flow
description: Атрибут VML Layout-Flow
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987672"
---
# <a name="vml-layout-flow-attribute"></a>Атрибут VML Layout-Flow

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 