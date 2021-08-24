---
title: Атрибут Преферрелативе VML
description: Атрибут Преферрелативе VML
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154297a528f18a3ac53f788ebbfe80ff59196f2872dd3dcb3789db16d5c91cb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654984"
---
# <a name="vml-preferrelative-attribute"></a>Атрибут Преферрелативе VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, сохраняется ли исходный размер объекта после переформатирования. Read/write. **Вгтристате**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:преферрелативе = " *выражение* " >

**Замечания**

По умолчанию **False**. Если **значение — true**, будет сохранен исходный размер объекта, а изменение размера будет основано на проценте от этого исходного размера. В противном случае при каждом изменении размера будет сброшен масштаб в 100%.

*Microsoft Office Extensions, атрибут*

**Пример**

При изменении размера фигуры исходный размер не будет сохранен.


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 