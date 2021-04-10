---
title: Атрибут ID (Path) (VML)
description: Атрибут ID (Path) (VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133899"
---
# <a name="id-attribute-pathvml"></a>Атрибут ID (Path) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Имя, которое предоставляет уникальный идентификатор для пути. Read/write. **Строка**.

**Применимо к**:

[Путь](msdn-online-vml-path-element.md)

**Синтаксис тега**

<v: *element* ID = " *выражение* " >

**Синтаксис сценария**

*element* . ID = "*выражение*"

*выражение* = *element*. ID

**Замечания**

Используйте **ID** для ссылки на конкретный путь. После создания пути и присвоения ему идентификатора можно использовать имя идентификатора, если требуется управлять путем.

*Стандартный атрибут VML*

**Пример**

Фигура имеет идентификатор Path с именем «myPath».


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 