---
title: Атрибут скрытой VML
description: Атрибут скрытой VML
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070208"
---
# <a name="vml-obscured-attribute"></a>Атрибут скрытой VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, является ли тень прозрачной. Read/write. **Вгтристате**.

**Применимо к**:

[Shadow](msdn-online-vml-shadow-element.md)

**Синтаксис тега**

<v: *элемент* скрыт = " *выражение* " >

**Синтаксис сценария**

*element* . скрыто = "*выражение*"

*выражение* = *element*. замаскировано

**Замечания**

Если **значение — true**, позволяет видеть сквозь тень, если в фигуре Нет заливки. Значение по умолчанию — **False**.

*Стандартный атрибут VML*

**Пример**

Фон отображается сквозь тень.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 