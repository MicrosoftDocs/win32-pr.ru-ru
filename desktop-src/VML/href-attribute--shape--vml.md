---
title: Атрибут HRef (Shape) (VML)
description: Атрибут HRef (Shape) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070530"
---
# <a name="href-attribute-shapevml"></a>Атрибут HRef (Shape) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет URL-адрес для фигуры. Когда вы щелкните фигуру, браузер загрузит URL-адрес. Read/write. **Строка**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *элемент* href = " *выражение* " >

**Синтаксис сценария**

*element* . href = "*выражение*"

*выражение* = *element*. href

**Замечания**

Атрибут **href** аналогичен стандартному атрибуту HTML **href** привязок.

Использование **href** упрощает создание интересных кнопок на веб-странице.

*Стандартный атрибут VML*

**Пример**

Когда вы щелкните прямоугольник, браузер загрузит домашнюю страницу корпорации Майкрософт.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



[Пример атрибута href](/previous-versions/bb229672(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 