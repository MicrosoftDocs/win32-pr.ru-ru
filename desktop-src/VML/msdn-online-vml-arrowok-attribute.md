---
title: Атрибут Арровок VML
description: Атрибут Арровок VML
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95b8fa7068f55246263e6622527a8ecec17d3351c284a0810cd77b085784aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124973"
---
# <a name="vml-arrowok-attribute"></a>Атрибут Арровок VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будут ли отображаться стрелки. Read/write. **Вгтристате**.

**Применимо к**:

[Путь](msdn-online-vml-path-element.md)

**Синтаксис тега**

<v: *element* арровок = " *выражение* " >

**Синтаксис сценария**

*element* . арровок = "*выражение*"

*выражение* = *element*. арровок

**Замечания**

Если задано **значение false**, то путь не будет иметь стрелок. По умолчанию **False**. Этот атрибут переопределяет все остальные атрибуты наконечника в родительском элементе или элементе **Stroke** .

*Стандартный атрибут VML*

**Пример**

У пути не будет стрелки.


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 