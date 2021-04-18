---
title: Атрибут метода VML
description: Атрибут метода VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691604"
---
# <a name="vml-method-attribute"></a>Атрибут метода VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 