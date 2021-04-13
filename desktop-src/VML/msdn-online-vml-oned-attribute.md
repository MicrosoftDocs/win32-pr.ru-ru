---
title: Атрибут Онед VML
description: Атрибут Онед VML
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339017"
---
# <a name="vml-oned-attribute"></a>Атрибут Онед VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, скрываются ли дополнительные дескрипторы фигуры. Read/write. **Вгтристате**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:онед = " *выражение* " >

**Замечания**

Скрывает все маркеры фигур, кроме левого верхнего и нижнего правого. то есть те же маркеры, которые используются для сегмента прямой линии. По умолчанию **False**.

*Атрибут расширений Microsoft Office*

**Пример**

Все маркеры фигуры, кроме верхнего левого и нижнего правого угла, скрыты.


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 