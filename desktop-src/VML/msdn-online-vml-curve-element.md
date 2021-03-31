---
title: Элемент кривой VML
description: Элемент кривой VML
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b9e04086652bf9dde7d7e7f5ebdea0992f774c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260918"
---
# <a name="vml-curve-element"></a>Элемент кривой VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Стандартная фигура кривой.

**Кривая** использует атрибуты [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [Control1](msdn-online-vml-control1-attribute.md)и [control2](msdn-online-vml-control2-attribute.md) .

Ниже приведен минимальный код, необходимый для создания образа.


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 