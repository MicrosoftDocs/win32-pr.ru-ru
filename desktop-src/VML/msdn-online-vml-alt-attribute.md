---
title: Атрибут ALT VML
description: Атрибут ALT VML
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260993"
---
# <a name="vml-alt-attribute"></a>Атрибут ALT VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет альтернативный текст, отображаемый вместо графического. Read/write. **Строка**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* Alt = " *выражение* " >

**Синтаксис сценария**

*element* . Alt = "*выражение*"

*выражение* = *element*. Alt

**Замечания**

Атрибут **ALT** аналогичен стандартному атрибуту HTML **ALT** . Этот атрибут позволяет браузерам, которые преобразуют текст в речь для описания графических элементов на странице.

*Стандартный атрибут VML*

**См. также:**

[Фигурная](shape-element--vml.md)

**Пример**

В элементе **ALT** ниже отображается фраза "красный прямоугольник" в браузерах, которые преобразуют веб-страницы в речевые фразы.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Пример атрибута Alt](/previous-versions/bb229663(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 