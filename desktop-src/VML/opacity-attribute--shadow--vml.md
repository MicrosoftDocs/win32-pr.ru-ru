---
title: Атрибут непрозрачности (тень) (VML)
description: Атрибут непрозрачности (тень) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43287a4bb6de9f2dd0d9d2b0af97d971314ab7e93ab2c4fae58b666ee1a94124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680624"
---
# <a name="opacity-attribute-shadowvml"></a>Атрибут непрозрачности (тень) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 