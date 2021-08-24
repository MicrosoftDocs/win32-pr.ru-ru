---
title: Атрибут Type (Shape) (VML)
description: Атрибут Type (Shape) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b20f663f8a403acca03ff8ab516a86dc91f7dd8d478eadedaa6be8b919ad48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513154"
---
# <a name="type-attribute-shapevml"></a>Атрибут Type (Shape) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет ссылку на идентификатор элемента [шапетипе](msdn-online-vml-shapetype-element.md) . Read/write. **Строка**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

``` syntax
<v:
          element 
          type=" expression ">
```

**Синтаксис сценария**

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

**Замечания**

Если атрибут **Type** ссылается на идентификатор элемента **шапетипе** , то заливки, контуры и штрихи **шапетипе** используются в качестве шаблонов для создания фигуры. Значения, производные от **шапетипе** , могут быть переопределены отдельными значениями фигур.

При использовании в тегах строковое значение должно начинаться с символа решетки ( \# ).

**Стандартный атрибут VML**

**Пример**

Фигура **шапетипе** создается с именем "MyType" в качестве идентификатора.


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



Затем, если создать фигуру с использованием значений **шапетипе** , фигура будет иметь атрибуты «MyType» **шапетипе**; то есть "shape01" будет иметь красную заливку с синей штриховкой.


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



Можно переопределить наследуемые значения, например, изменив цвет на зеленый.


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



[Пример атрибута Type](/previous-versions/bb264099(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 