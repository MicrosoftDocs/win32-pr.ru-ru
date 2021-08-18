---
title: Атрибут Clip для VML
description: Атрибут Clip для VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cab4afdef2a10c9c6f6a0561dedf5b4df3538a97152cb53181452b8ac531bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999294"
---
# <a name="vml-clip-attribute"></a>Атрибут Clip для VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, включено ли обрезание. Read/write. **Вгтристате**.

**Применимо к**:

[вмлфраме](msdn-online-vml-vmlframe-element.md)

**Синтаксис тега**

<v: *элемент* Clip = " *выражение* " >

**Синтаксис сценария**

*element* . Clip = "*выражение*"

*выражение* = *элемент*. Clip

**Замечания**

Если значение **Clip** равно **false**, фигура будет масштабироваться в соответствии с размерами рамки. Если **значение равно true**, то все части фигуры, находящиеся за пределами рамки, не будут отображаться.

Обратите внимание, что [источник](origin-attribute--vmlframe--vml.md) и [Размер](size-attribute--vmlframe.md) не будут использоваться, если только значение **Clip** не равно **true**.

*Стандартный атрибут VML*

**Пример**

Изображение, определенное во внешнем файле, будет обрезано.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 