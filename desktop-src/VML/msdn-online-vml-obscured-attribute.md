---
title: Атрибут скрытой VML
description: Атрибут скрытой VML
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9122b3a9828fde816684cb20035949628ef25e38d06fb188d8271f0d5384f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308284"
---
# <a name="vml-obscured-attribute"></a>Атрибут скрытой VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 