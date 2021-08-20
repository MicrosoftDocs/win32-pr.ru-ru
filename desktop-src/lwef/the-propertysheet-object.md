---
title: Объект страница свойств
description: Объект страница свойств
ms.assetid: 9d15d198-a4fe-4c05-a7be-0807a179cd9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef25ee66bdffc72da87ab85206deb51399251a0a43160448f784e01038e22519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887904"
---
# <a name="the-propertysheet-object"></a>Объект страница свойств

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

Объект [**Страница свойств**](https://www.bing.com/search?q=**PropertySheet**) предоставляет несколько свойств, которые можно использовать, если требуется манипулировать символом относительно страницы свойств Microsoft Agent (также известной как окно дополнительных параметров символов).

-   [**Высота**](height-property-pso.md)
-   [**Левый**](left-property-pso.md)
-   [**Страниц**](page-property.md)
-   [**Вверх**](top-property-pso.md)
-   [**Ярлык**](visible-property.md)
-   [**Ширина**](width-property-pso.md)

Если вы запрашиваете свойства [**высоты**](height-property-pso.md), [**левого**](left-property-pso.md), [**верхнего**](top-property-pso.md)и [**ширины**](width-property-pso.md) до того, как страница свойств когда-либо отображалась, их значения возвращаются как нули (0). После отображения эти свойства возвращают последнюю расположение и размер окна (относительно текущего разрешения экрана).

 

 




