---
title: Закрашенный атрибут VML
description: Закрашенный атрибут VML
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488256"
---
# <a name="vml-filled-attribute"></a>Закрашенный атрибут VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли заполнен замкнутый контур. Read/write. **Вгтристате**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *элемент* заполнен = " *выражение* " >

**Синтаксис сценария**

*element* . filled = "*выражение*"

*выражение* = *element*. filled

**Замечания**

Значение дублируется из атрибута **On** элемента [Fill](msdn-online-vml-fill-element.md) .

*Стандартный атрибут VML*

**Пример**

Контур фигуры заполнен.


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Пример атрибута с заливкой](/previous-versions/bb229669(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 