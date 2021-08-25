---
title: Атрибут ID (VML)
description: Атрибут ID (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0ba0addd2d6af8a8b38af4085c79123d3178a3299269468abd73fff1951d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007863"
---
# <a name="id-attribute-vml"></a>Атрибут ID (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Предоставляет уникальный идентификатор для элемента. Read/write. **Строка**.

**Применимо к**:

Все элементы VML.

**Синтаксис тега**

<v: *ElementName* ID = " *иднаме* " >

**Синтаксис сценария**

*ElementName* . ID = " *иднаме* "

*выражение* = *ElementName*. ID

**Замечания**

Используйте **ID** для ссылки на конкретный элемент. Создав фигуру и задавая ей идентификатор, можно использовать имя идентификатора, если требуется управлять элементом.

Для использования элемента [шапетипе](msdn-online-vml-shapetype-element.md) требуется **идентификатор** .

при создании VML с помощью Microsoft Office, если фигуре назначено имя объектной модели, то для **идентификатора** задается это имя. Если имя объектной модели не задано, то имя создается с помощью *SPID* (внутренний идентификатор фигуры) и префикса (S для Shape, M для главной фигуры, T для шапетипе).

*Стандартный атрибут VML*.

**Пример**

Чтобы изменить атрибуты фигуры, необходимо сначала присвоить ей идентификатор. Например, "мирект".


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



[Пример атрибута ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 