---
title: Атрибут Локкротатионцентер VML
description: Атрибут Локкротатионцентер VML
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672383"
---
# <a name="vml-lockrotationcenter-attribute"></a>Атрибут Локкротатионцентер VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, задается ли поворот вытянутого объекта атрибутом [ротатионангле](msdn-online-vml-rotationangle-attribute.md) . Read/write. **Вгтристате**.

**Применимо к**:

[Выдавливания](msdn-online-vml-extrusion-element.md)

**Синтаксис тега**

<o: *element* локкротатионцентер = " *выражение* " >

**Синтаксис сценария**

*element* . локкротатионцентер = "*выражение*"

*выражение* = *element*. локкротатионцентер

**Замечания**

Если **значение равно false**, поворот определяется атрибутом [Orientation](msdn-online-vml-orientation-attribute.md) . Значение по умолчанию равно **True**.

Обратите внимание на следующее.


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



тот же самый:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Атрибут расширений Microsoft Office*

 

 