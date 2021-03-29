---
title: Атрибут Ендарроввидс VML
description: Атрибут Ендарроввидс VML
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793765"
---
# <a name="vml-endarrowwidth-attribute"></a>Атрибут Ендарроввидс VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет ширину стрелки для конца строки. Read/write. **Вгарровхеадвидс**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* ендарроввидс = " *выражение* " >

**Синтаксис сценария**

*element* . ендарроввидс = "*выражение*"

*выражение* = *element*. ендарроввидс

**Замечания**

К этим значениям относятся следующие.

-   Разрабатываем
-   Среднее (по умолчанию)
-   Широкий

*Стандартный атрибут VML*

**Пример**

Линия рисуется с помощью широкой классической стрелки в конце штриха.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 