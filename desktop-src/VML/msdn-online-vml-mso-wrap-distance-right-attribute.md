---
title: Атрибут VML MSO-Wrap-Distance-right
description: Атрибут VML MSO-Wrap-Distance-right
ms.assetid: 2f0ec7a3-036e-4f45-a330-f8ddccb75791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf38fc62812b0ce300e4d18067a0f2497233f2e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890784"
---
# <a name="vml-mso-wrap-distance-right-attribute"></a>Атрибут VML MSO-Wrap-Distance-right

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет расстояние от правой стороны фигуры до текста, который обтекает вокруг него. Read/write. **Строка**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: Style *элемента* = "MSO-Wrap-Distance-Right: *выражение* " >

**Замечания**

Обратите внимание, что этот атрибут отличается от атрибута **поля** CSS. **Поле** изменяет источник фигуры, чтобы включить в него области полей, но расстояние по обтекания в Microsoft Office не изменяет происхождение фигуры.

*Атрибут расширений Microsoft Office*

**Пример**

Фигура имеет право на перенос в 10 пунктов.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-right:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 