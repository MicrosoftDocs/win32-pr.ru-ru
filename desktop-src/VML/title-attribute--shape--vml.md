---
title: Атрибут Title (Shape) (VML)
description: Атрибут Title (Shape) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488240"
---
# <a name="title-attribute-shapevml"></a>Атрибут Title (Shape) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет текст, отображаемый при наведении указателя мыши на фигуру. Read/write. **Строка**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *элемент* Title = " *выражение* " >

**Синтаксис сценария**

*element* . Title = "*выражение*"

*выражение* = *элемент*. Title

**Замечания**

Атрибут **Title** аналогичен стандартному атрибуту **заголовка** HTML. Поведение заголовка аналогично подсказке Microsoft Windows.

**Стандартный атрибут VML**

**Пример**

Заголовок фигуры — «отображение подсказки» и появляется при перемещении указателя мыши над фигурой.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Пример атрибута Title](/previous-versions/bb264097(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 