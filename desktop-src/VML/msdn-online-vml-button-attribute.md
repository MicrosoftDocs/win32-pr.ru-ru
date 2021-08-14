---
title: Атрибут кнопки VML
description: Атрибут кнопки VML
ms.assetid: 273024ac-683f-48d2-b6a0-574824f4c05d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c505feebbf4614f7e56c856fa2c757e93160823d8bcd2fd5d539da80c436f32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754979"
---
# <a name="vml-button-attribute"></a>Атрибут кнопки VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли фигура обработана как кнопка. Read/write. **Вгтристате**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:буттон = " *выражение* " >

**Замечания**

По умолчанию **False**. Если **значение равно true**, фигура обрабатывается как кнопка.

*Microsoft Office Extensions, атрибут*

**Пример**

Фигура является кнопкой.


```HTML
   <v:rect id=myrect fillcolor="red" o:button="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 