---
title: Атрибут ID (Stroke) (VML)
description: Атрибут ID (Stroke) (VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efc9cfda1b7ddb359812d9ad28b37b851315da8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792403"
---
# <a name="id-attribute-strokevml"></a>Атрибут ID (Stroke) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Имя, которое предоставляет уникальный идентификатор для штриха. Read/write. **Строка**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* ID = " *выражение* " >

**Синтаксис сценария**

*element* . ID = "*выражение*"

*выражение* = *element*. ID

**Замечания**

Используйте **ID** для ссылки на конкретный штрих. После создания штриха и присвоения ему идентификатора можно использовать имя идентификатора, если требуется управлять обводкой.

*Стандартный атрибут VML*

**Пример**

Фигура имеет идентификатор Stroke с именем «мистроке».


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 