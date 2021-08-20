---
title: Атрибут Даублекликкнотифи VML
description: Атрибут Даублекликкнотифи VML
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9945f4391890f33d3569d1c1aed39a8ec5bbe4b0be29258da1cca4b7caf895da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124834"
---
# <a name="vml-doubleclicknotify-attribute"></a>Атрибут Даублекликкнотифи VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Отправляет сообщение о событии при двойном щелчке фигуры. Read/write. **Вгтристате**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:даублекликкнотифи = " *выражение* " >

**Замечания**

Значение по умолчанию — **false**, что означает, что событие не будет запущено.

*Microsoft Office Extensions, атрибут*

**Пример**

Фигура активирует событие двойного щелчка при двойном щелчке.


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 