---
title: Атрибут ориентации VML
description: Атрибут ориентации VML
ms.assetid: 62298908-6e88-470d-bca2-0cfc1a38c2eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa19d8826638ef44ed99f9560e0db5dcb7ae455e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672405"
---
# <a name="vml-orientation-attribute"></a>Атрибут ориентации VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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

*Атрибут расширений Microsoft Office*

 

 