---
title: Атрибут color2 (shadow) (VML)
description: Атрибут color2 (shadow) (VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793045"
---
# <a name="color2-attribute-shadowvml"></a>Атрибут color2 (shadow) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет второй цвет тени. Read/write. **Вгколор**.

**Применимо к**:

[Shadow](msdn-online-vml-shadow-element.md)

**Синтаксис тега**

<v: *element* color2 = " *выражение* " >

**Синтаксис сценария**

*element* . color2 = "*выражение*"

*выражение* = *element*. color2

**Замечания**

Используйте второй цвет для создания специальных эффектов тени. Дополнительные сведения о втором цветах см. в описании атрибута [Type](type-attribute--shadow--vml.md) .

*Стандартный атрибут VML*

**Пример**

Тень имеет синий цвет для второго цвета.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 