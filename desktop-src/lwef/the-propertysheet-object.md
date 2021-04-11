---
title: Объект страница свойств
description: Объект страница свойств
ms.assetid: 9d15d198-a4fe-4c05-a7be-0807a179cd9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ae4ded2625440ba34170df605b60287f105800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132907"
---
# <a name="the-propertysheet-object"></a>Объект страница свойств

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Объект [**Страница свойств**](https://www.bing.com/search?q=**PropertySheet**) предоставляет несколько свойств, которые можно использовать, если требуется манипулировать символом относительно страницы свойств Microsoft Agent (также известной как окно дополнительных параметров символов).

-   [**Высота**](height-property-pso.md)
-   [**Слева**](left-property-pso.md)
-   [**Страниц**](page-property.md)
-   [**Вверх**](top-property-pso.md)
-   [**Visible**](visible-property.md)
-   [**Ширина**](width-property-pso.md)

Если вы запрашиваете свойства [**высоты**](height-property-pso.md), [**левого**](left-property-pso.md), [**верхнего**](top-property-pso.md)и [**ширины**](width-property-pso.md) до того, как страница свойств когда-либо отображалась, их значения возвращаются как нули (0). После отображения эти свойства возвращают последнюю расположение и размер окна (относительно текущего разрешения экрана).

 

 




