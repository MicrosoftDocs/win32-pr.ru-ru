---
title: Атрибут Color (тень) (VML)
description: Атрибут Color (тень) (VML)
ms.assetid: 677615b7-b4a4-411f-b04e-3ed0399f4c05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73df77e65a3ae0f74c6e79b9c179c31da27698f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691526"
---
# <a name="color-attribute-shadowvml"></a>Атрибут Color (тень) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет цвет тени. Read/write. **Вгколор**.

**Применимо к**:

[Shadow](msdn-online-vml-shadow-element.md)

**Синтаксис тега**

<v: Color *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Color = "*выражение*"

*выражение* = *элемент*. Color

**Замечания**

Используйте атрибут Color, чтобы задать или получить цвет тени.

*Стандартный атрибут VML*

**Пример**

Тень горит зеленым цветом.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green"/>
   </v:shape>
```



 

 