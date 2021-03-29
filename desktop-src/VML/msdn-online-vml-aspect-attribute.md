---
title: Атрибут аспекта VML
description: Атрибут аспекта VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792402"
---
# <a name="vml-aspect-attribute"></a>Атрибут аспекта VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Указывает, как будет сохраняться пропорции изображения заливки. Read/write. **Строка**.

**Применимо к**:

[Заполнить](msdn-online-vml-fill-element.md)

**Синтаксис тега**

<v: аспект *element* = " *выражение* " >

**Синтаксис сценария**

*element* . аспект = "*выражение*"

*выражение* = *element*. аспект

**Замечания**

К этим значениям относятся следующие.



| Значение   | Описание                           |
|---------|---------------------------------------|
| ignore  | Пропускать проблемы с аспектами. По умолчанию.        |
| задать | Размер изображения не меньше **размера**. |
| атмост  | **Размер** изображения не превышает.     |



 

*Стандартный атрибут VML*

**Пример**

Изображение, составляющее заливку, больше или равно размеру 10 пунктов на 10 пунктов.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 