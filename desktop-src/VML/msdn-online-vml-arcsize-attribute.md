---
title: Атрибут Арксизе VML
description: Атрибут Арксизе VML
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691580"
---
# <a name="vml-arcsize-attribute"></a>Атрибут Арксизе VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет величину округления для скругленного прямоугольника. Read/write. [Вгфрактион](msdn-online-vml-vgfraction-data-type.md) .

**Применимо к**:

[раундрект](msdn-online-vml-roundrect-element.md)

**Синтаксис тега**

<v: *element* арксизе = " *выражение* " >

**Синтаксис сценария**

*element* . арксизе = "*выражение*"

*выражение* = *element*. арксизе

**Замечания**

Определяет скругленные углы скругленного прямоугольника в процентах от половины меньшего измерения длины и ширины прямоугольника. 0% будет иметь квадратные углы, и 100% будет формировать круглые углы. Квадрат с **арксизе** значением 1,0 будет окружностью. Значение по умолчанию — 0,2 (20%).

*Стандартный атрибут VML*

**Пример**

Скругленный прямоугольник рисуется с помощью строгого, но скругленного углов.


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 