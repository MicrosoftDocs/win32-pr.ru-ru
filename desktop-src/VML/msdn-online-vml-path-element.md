---
title: Элемент пути VML
description: Элемент пути VML
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb46ce43d2dc9ad80aeb21340dceacde80feba99d9debdf66920b662eeaf3a9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308184"
---
# <a name="vml-path-element"></a>Элемент пути VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет контур для фигуры.

Следующие атрибуты изменяют тень.



| attribute                                                        | Описание                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [арровок](msdn-online-vml-arrowok-attribute.md)                 | Определяет, будут ли отображаться стрелки.                                |
| [коннектанглес](msdn-online-vml-connectangles-attribute.md)     | Указывает, как кривая будет подключаться к точке соединения.                       |
| [коннектлокс](msdn-online-vml-connectlocs-attribute.md)         | Определяет расположение точек соединения по пути.                            |
| [коннекттипе](msdn-online-vml-connecttype-attribute.md)         | Определяет тип точки соединения, используемый для присоединения фигур к другим фигурам. |
| [екструсионок](msdn-online-vml-extrusionok-attribute.md)         | Определяет, будет ли отображаться объем на объеме.                              |
| [филлок](msdn-online-vml-fillok-attribute.md)                   | Определяет, будет ли отображаться заливка.                                    |
| [градиентшапеок](msdn-online-vml-gradientshapeok-attribute.md) | Определяет, будет ли отображаться фигура градиента.                          |
| [Идентификатор](id-attribute--path--vml.md)                                | Определяет уникальный идентификатор для пути.                                         |
| [лимо](msdn-online-vml-limo-attribute.md)                       | Определяет точку растяжения на пути.                                            |
| [шадовок](msdn-online-vml-shadowok-attribute.md)               | Определяет, будет ли отображаться тень.                                  |
| [строкеок](msdn-online-vml-strokeok-attribute.md)               | Определяет, будет ли отображаться штрих.                                  |
| [текстбоксрект](msdn-online-vml-textboxrect-attribute.md)         | Определяет одно или несколько текстовых полей внутри фигуры.                                   |
| [текстпасок](msdn-online-vml-textpathok-attribute.md)           | Определяет, будет ли отображаться текстпас.                                |
| [V](msdn-online-vml-v-attribute.md)                             | Определяет команды, составляющие путь.                                       |



 

**Замечания**

Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .

В следующем коде показано, как определить фигуру с путем.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Обратите внимание, что атрибут [V](msdn-online-vml-v-attribute.md) **пути** заменяет атрибут [path](msdn-online-vml-path-attribute.md) [фигуры](shape-element--vml.md).

**Примеры**

-   [Пример дочернего элемента простого пути](/previous-versions/bb229545(v=vs.85))
-   [Пример дочернего элемента динамического пути](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 