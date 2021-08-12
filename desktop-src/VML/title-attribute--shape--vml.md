---
title: Атрибут Title (Shape) (VML)
description: Атрибут Title (Shape) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ec2a16df6740bca64357dae039f4222de956300604198b2d199977970c526d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596512"
---
# <a name="title-attribute-shapevml"></a>Атрибут Title (Shape) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет текст, отображаемый при наведении указателя мыши на фигуру. Read/write. **Строка**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *элемент* Title = " *выражение* " >

**Синтаксис сценария**

*element* . Title = "*выражение*"

*выражение* = *элемент*. Title

**Замечания**

Атрибут **Title** аналогичен стандартному атрибуту **заголовка** HTML. поведение заголовка похоже на подсказку Microsoft Windows.

**Стандартный атрибут VML**

**Пример**

Заголовок фигуры — «отображение подсказки» и появляется при перемещении указателя мыши над фигурой.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Пример атрибута Title](/previous-versions/bb264097(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 