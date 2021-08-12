---
title: Атрибут Коннектортипе VML
description: Атрибут Коннектортипе VML
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a552324582729c74ae87c9fcf1cd512334423bb84c43992f265c0b47fffcd98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601977"
---
# <a name="vml-connectortype-attribute"></a>Атрибут Коннектортипе VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Указывает тип соединителя, используемого для объединения фигур. Read/write. **Строка**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:коннектортипе = " *выражение* " >

**Замечания**

К этим значениям относятся следующие.



| Значение    | Описание                    |
|----------|--------------------------------|
| нет     | Нет соединителя.                  |
| линия | По умолчанию. Прямой соединитель. |
| расталкивая    | Соединитель с уступом.     |
| кругл   | Криволинейный соединитель.            |



 

Этот атрибут может также использоваться обработчиком правил графического редактора.

*Microsoft Office Extensions, атрибут*

**Пример**

Фигура использует прямую линию в качестве соединителя.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 