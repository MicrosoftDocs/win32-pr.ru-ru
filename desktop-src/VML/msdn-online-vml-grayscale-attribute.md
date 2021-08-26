---
title: Атрибут оттенков VML
description: Атрибут оттенков VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683371e2441ffa93f96dc8f727e4eed293954b1897267db8848aa39ffa497af8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099214"
---
# <a name="vml-grayscale-attribute"></a>Атрибут оттенков VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли изображение отображаться в режиме градаций серого. Read/write. **Вгтристате**.

**Применимо к**:

[ImageData](msdn-online-vml-imagedata-element.md)

**Синтаксис тега**

<v: градации серого *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . градации серого = "*выражение*"

*выражение* = *element*. оттенки серого

**Замечания**

Если **значение — true**, изображение будет отображаться в оттенках серого вместо цвета. По умолчанию **False**.

Значение основано на КЦИР рекомендации 709, что соответствует более зеленому весу и дает более привлекательные результаты для естественного цвета.

*Стандартный атрибут VML*

**Пример**

Изображение будет отображаться в оттенках серого вместо цвета.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 