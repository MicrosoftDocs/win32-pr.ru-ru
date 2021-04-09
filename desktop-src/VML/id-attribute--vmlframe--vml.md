---
title: Атрибут ID (Вмлфраме) (VML)
description: Атрибут ID (Вмлфраме) (VML)
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070218"
---
# <a name="id-attribute-vmlframevml"></a>Атрибут ID (Вмлфраме) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет уникальный идентификатор для кадра. Read/write. **Строка**.

**Применимо к**:

[вмлфраме](msdn-online-vml-vmlframe-element.md)

**Синтаксис тега**

<v: *element* ID = " *выражение* " >

**Синтаксис сценария**

*element* . ID = "*выражение*"

*выражение* = *element*. ID

**Замечания**

Используйте **идентификатор** для ссылки на кадр. Например, можно переместить фрейм вокруг страницы, изменив положение кадра, на которое ссылается **идентификатор**.

*Стандартный атрибут VML*

**Пример**

**Идентификатор** кадра — "frame01".


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 