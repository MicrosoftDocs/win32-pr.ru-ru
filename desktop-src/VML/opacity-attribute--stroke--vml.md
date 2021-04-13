---
title: Атрибут непрозрачности (Stroke) (VML)
description: Атрибут непрозрачности (Stroke) (VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488241"
---
# <a name="opacity-attribute-strokevml"></a>Атрибут непрозрачности (Stroke) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет степень прозрачности штриха. Read/write. **Вгфрактион**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: Opacity *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Opacity = "*выражение*"

*выражение* = *элемент*. Opacity

**Замечания**

Значение по умолчанию — 1,0.

*Стандартный атрибут VML*

**Пример**

Штрих имеет прозрачный 50%.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 