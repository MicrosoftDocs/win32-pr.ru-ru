---
title: Атрибут непрозрачности (Fill) (VML)
description: Атрибут непрозрачности (Fill) (VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ea4f539eb2386dae7b8e863c95556cf70400c320ee515897cf7f96a85fe3ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057602"
---
# <a name="opacity-attribute-fillvml"></a>Атрибут непрозрачности (Fill) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет прозрачность заливки. Read/write. [Вгфрактион](msdn-online-vml-vgfraction-data-type.md).

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: Opacity *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Opacity = "*выражение*"

*выражение* = *элемент*. Opacity

**Замечания**

Значение по умолчанию — 1,0.

*Стандартный атрибут VML*

**Пример**

Заливка фигуры будет закрашена на 50% прозрачна.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 