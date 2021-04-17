---
title: Атрибут Коннектортипе VML
description: Атрибут Коннектортипе VML
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672295"
---
# <a name="vml-connectortype-attribute"></a>Атрибут Коннектортипе VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Указывает тип соединителя, используемого для объединения фигур. Read/write. **Строка**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

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

*Атрибут расширений Microsoft Office*

**Пример**

Фигура использует прямую линию в качестве соединителя.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 