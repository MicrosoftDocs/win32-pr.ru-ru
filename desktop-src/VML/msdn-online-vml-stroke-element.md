---
title: Элемент штриха VML
description: Элемент штриха VML
ms.assetid: 300ecde5-f19d-4ff7-89a4-af9b8e82ae9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62048227fca074276b825ceedb793eaa9a5d84dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487857"
---
# <a name="vml-stroke-element"></a>Элемент штриха VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет штрих для фигуры.

Следующие атрибуты изменяют штрих.



| attribute                                                          | Описание                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------|
| [алсреф](althref-attribute--stroke--vml.md)                      | Указывает альтернативную ссылку для штриха.                |
| [Цвет](color-attribute--stroke--vml.md)                          | Определяет цвет штриха.                                |
| [Color2](color2-attribute--stroke--vml.md)                        | Определяет второй цвет для штриха.                          |
| [DashStyle](msdn-online-vml-dashstyle-attribute.md)               | Задает шаблон точки и штриха для штриха.              |
| [ендарров](msdn-online-vml-endarrow-attribute.md)                 | Определяет стиль наконечника для конца штриха.           |
| [ендарровленгс](msdn-online-vml-endarrowlength-attribute.md)     | Определяет длину наконечника для конца штриха.          |
| [ендарроввидс](msdn-online-vml-endarrowwidth-attribute.md)       | Определяет ширину стрелки для конца штриха.           |
| [ендкап](msdn-online-vml-endcap-attribute.md)                     | Определяет стиль конца штриха.                |
| [Объекта FillType](msdn-online-vml-filltype-attribute.md)                 | Определяет тип заливки, используемый для фона штриха. |
| [Полный](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229431(v=vs.85))    | Определяет URL-адрес исходного изображения для штриха.         |
| [Идентификатор](id-attribute--stroke--vml.md)                                | Определяет уникальный идентификатор для штриха.                   |
| [имажеалигншапе](msdn-online-vml-imagealignshape-attribute.md)   | Определяет выравнивание изображения штриха.                   |
| [имажеаспект](msdn-online-vml-imageaspect-attribute.md)           | Определяет, как будет сохраняться пропорции изображения обводки.  |
| [ImageSize](msdn-online-vml-imagesize-attribute.md)               | Определяет размер изображения для штриха.                 |
| [жоинстиле](msdn-online-vml-joinstyle-attribute.md)               | Определяет стиль объединения ломаной линии.                         |
| [линестиле](msdn-online-vml-linestyle-attribute.md)               | Определяет стиль линии для штриха.                           |
| [митерлимит](msdn-online-vml-miterlimit-attribute.md)             | Определяет гладкость соединения типа «уголок».                      |
| [On](on-attribute--stroke--vml.md) (Вкл.)                                | Определяет, будет ли отображаться штрих.              |
| [Непрозрачность](opacity-attribute--stroke--vml.md)                      | Определяет степень прозрачности штриха.               |
| [Src](src-attribute--stroke--vml.md)                              | Определяет исходное изображение для загрузки для заливки штриха.           |
| [стартарров](msdn-online-vml-startarrow-attribute.md)             | Определяет наконечник для начала штриха.              |
| [стартарровленгс](msdn-online-vml-startarrowlength-attribute.md) | Определяет длину стрелки для начала штриха.       |
| [стартарроввидс](msdn-online-vml-startarrowwidth-attribute.md)   | Определяет ширину стрелки для начала штриха.        |
| [Title](title-attribute--stroke--vml.md)                          | Определяет заголовок штриха.                                |
| [Weight](msdn-online-vml-weight-attribute.md)                     | Определяет толщину штриха.                            |



 

**Замечания**

Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .

В следующем коде показано, как можно использовать элемент **Stroke** для изменения линии.


```HTML
   <v:line
   to="300pt,50pt" from="50pt,50pt">
   <v:stroke weight="50pt" color="red" linestyle="ThickThin"/>
   </v:line>
```



**Примеры**

-   [Пример простой обводки](/previous-versions/bb229466(v=vs.85))
-   [Пример изображения обводки](/previous-versions/bb229468(v=vs.85))

 

 