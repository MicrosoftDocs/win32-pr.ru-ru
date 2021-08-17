---
title: Атрибут Митерлимит VML
description: Атрибут Митерлимит VML
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef82ce7e8e0d3bf99fc532a9e746a94006a6bb9deba282ce8edd6ab91d41902
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308374"
---
# <a name="vml-miterlimit-attribute"></a>Атрибут Митерлимит VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет гладкость соединения типа «уголок». Read/write. **Вгнумбер**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *element* митерлимит = " *выражение* " >

**Синтаксис сценария**

*element* . митерлимит = "*выражение*"

*выражение* = *element*. митерлимит

**Замечания**

Максимальное расстояние между внутренней точкой и внешней точкой соединения. Это число является кратным ширине линии.

Значение по умолчанию: 8.

*Стандартный атрибут VML*

**Пример**

Соединения в ломаной линии размещаются с ограничением 10, то есть 5 раз в две точки.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 