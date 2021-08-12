---
title: Атрибут Реграупид VML
description: Атрибут Реграупид VML
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c304bb0ecbe19c62e6fa5a204749b61fad4a700fe4222b6e1ef993384d53abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597647"
---
# <a name="vml-regroupid-attribute"></a>Атрибут Реграупид VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет предыдущую группу для фигуры. Read/write. **Вгинтежер**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:реграупид = " *выражение* " >

**Замечания**

ИДЕНТИФИКАЦИОНный номер используется для идентификации групп фигур, которые больше не группируются. Позволяет программно перегруппировку фигур.

*Microsoft Office Extensions, атрибут*

**Пример**

Фигура была частью группы, обозначенной ИДЕНТИФИКАТОРом группы 040754.


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 