---
title: Атрибут непрозрачности (тень) (VML)
description: Атрибут непрозрачности (тень) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413094"
---
# <a name="opacity-attribute-shadowvml"></a>Атрибут непрозрачности (тень) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет прозрачность тени. Read/write. [Вгфрактион](msdn-online-vml-vgfraction-data-type.md) .

**Применимо к**:

[Shadow](msdn-online-vml-shadow-element.md)

**Синтаксис тега**

<v: Opacity *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Opacity = "*выражение*"

*выражение* = *элемент*. Opacity

**Замечания**

Значение по умолчанию — 1. Значение 0 выполнит прозрачную тень.

*Стандартный атрибут VML*

**Пример**

Фигура имеет тень на 50% прозрачна.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 