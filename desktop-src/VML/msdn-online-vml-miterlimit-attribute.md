---
title: Атрибут Митерлимит VML
description: Атрибут Митерлимит VML
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487877"
---
# <a name="vml-miterlimit-attribute"></a>Атрибут Митерлимит VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 