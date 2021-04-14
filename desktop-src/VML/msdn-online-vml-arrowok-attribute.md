---
title: Атрибут Арровок VML
description: Атрибут Арровок VML
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413190"
---
# <a name="vml-arrowok-attribute"></a>Атрибут Арровок VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 