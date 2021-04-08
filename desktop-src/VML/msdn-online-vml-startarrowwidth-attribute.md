---
title: Атрибут Стартарроввидс VML
description: Атрибут Стартарроввидс VML
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ba4f5adddc328d1791fa2beb570f59da826f83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792553"
---
# <a name="vml-startarrowwidth-attribute"></a>Атрибут Стартарроввидс VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 