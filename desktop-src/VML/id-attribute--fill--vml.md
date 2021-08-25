---
title: Атрибут ID (Fill) (VML)
description: Атрибут ID (Fill) (VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f317cef4d588444f5c01770dafd5b56af0d2bca48ee228ff789a11b46348bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007874"
---
# <a name="id-attribute-fillvml"></a>Атрибут ID (Fill) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Имя, которое предоставляет уникальный идентификатор для заливки. Read/write. **Строка**.

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: *element* ID = " *выражение* " >

**Синтаксис сценария**

*element* . ID = "*выражение*"

*выражение* = *element*. ID

**Замечания**

Используйте **ID** для ссылки на определенную заливку. После создания заливки и присвоения ей идентификатора можно использовать имя идентификатора, если требуется управлять заливкой.

*Стандартный атрибут VML*

**Пример**

Фигура имеет идентификатор заполнения с именем «мифилл».


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 