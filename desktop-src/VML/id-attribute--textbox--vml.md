---
title: Атрибут ID (TextBox) (VML)
description: Атрибут ID (TextBox) (VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890800"
---
# <a name="id-attribute-textboxvml"></a>Атрибут ID (TextBox) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Имя, которое предоставляет уникальный идентификатор для текстового поля. Read/write. **Строка**.

**Применимо к**:

[TextBox](msdn-online-vml-textbox-element.md)

**Синтаксис тега**

<v: *element* ID = " *выражение* " >

**Синтаксис сценария**

*element* . ID = "*выражение*"

*выражение* = *element*. ID

**Замечания**

Используйте **ID** для ссылки на конкретное текстовое поле. После создания текстового поля и присвоения ему идентификатора можно использовать имя идентификатора, если вы хотите управлять текстовым полем.

*Стандартный атрибут VML*

**Пример**

Фигура имеет идентификатор TextBox с именем "митекстбокс".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 