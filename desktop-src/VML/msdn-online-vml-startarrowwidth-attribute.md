---
title: Атрибут Стартарроввидс VML
description: Атрибут Стартарроввидс VML
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d427db8e504fca57fc77b24b7b5fa1360ed7716276cd67b43c55ee8d0552d8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513244"
---
# <a name="vml-startarrowwidth-attribute"></a>Атрибут Стартарроввидс VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет ширину стрелки для начала строки. Read/write. **Вгарровхеадвидс**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* стартарроввидс = " *выражение* " >

**Синтаксис сценария**

*element* . стартарроввидс = "*выражение*"

*выражение* = *element*. стартарроввидс

**Замечания**

К этим значениям относятся следующие.

-   Разрабатываем
-   Среднее (по умолчанию)
-   Широкий

Стандартный атрибут VML

**Пример**

Линия рисуется с помощью широкой классической стрелки в начале штриха.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 