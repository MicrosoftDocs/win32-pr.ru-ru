---
title: Атрибут ориентации VML
description: Атрибут ориентации VML
ms.assetid: 62298908-6e88-470d-bca2-0cfc1a38c2eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdbe13a21963972b4501ddc8224f23df89c7ccb5e850b8c1e0aa1087cb6c5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999124"
---
# <a name="vml-orientation-attribute"></a>Атрибут ориентации VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Задает вектор, вокруг которого можно поворачивать фигуру. Read/write. **VgVector3D**.

**Применимо к**:

[Выдавливания](msdn-online-vml-extrusion-element.md)

**Синтаксис тега**

<o: Orientation *элемента* = " *выражение* " >

**Синтаксис сценария**

*element* . Orientation = "*выражение*"

*выражение* = *элемент*. Orientation

**Замечания**

Используйте атрибут [ориентатионангле](msdn-online-vml-orientationangle-attribute.md) , чтобы указать величину поворота вокруг этого вектора. Значение по умолчанию — 100, 0, 0.

*Microsoft Office Extensions, атрибут*

 

 