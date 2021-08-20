---
title: Атрибут метода VML
description: Атрибут метода VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6b5ae67f94a2fc6e27451fb1a947c8341d1f77c08a721ca7946250cee3b7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124767"
---
# <a name="vml-method-attribute"></a>Атрибут метода VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет метод, используемый для создания градиентной заливки. Read/write. **Вгсигматипе**.

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: *element* method = " *выражение* " >

**Синтаксис сценария**

*element* . Method = "*выражение*"

*выражение* = *element*. Method

**Замечания**

К этим значениям относятся следующие.



| Значение  | Описание          |
|--------|----------------------|
| Нет   | Заполнение без сигм.       |
| Линейная | Заливка линейной Сигма.   |
| Sigma  | Сигма (Заливка). По умолчанию. |
| Любой    | Любое заполнение Сигма.      |



 

*Стандартный атрибут VML*

**Пример**

Фигура будет иметь красную линейную градиентную заливку.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 