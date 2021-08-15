---
title: Элемент заливки VML
description: Элемент заливки VML
ms.assetid: ea790017-5aaa-4e75-8fc7-77fc94fd1d1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b314e2d735b8b7800321eacffbd63c686b17e870fd136e086c52231ad801456e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346628"
---
# <a name="vml-fill-element"></a>Элемент заливки VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет заливку для фигуры.

Следующие атрибуты изменяют заливку.



| attribute                                                          | Описание                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [алигншапе](msdn-online-vml-alignshape-attribute.md)             | Определяет, будет ли изображение согласовываться с фигурой.   |
| [алсреф](althref-attribute--fill--vml.md)                        | Указывает альтернативную ссылку для изображения.         |
| [Под](angle-attribute--fill--vml.md)                            | Определяет угол градиентной заливки.                  |
| [Аспект](msdn-online-vml-aspect-attribute.md)                     | Указывает, как будет сохранен аспект изображения заливки. |
| [Цвет](color-attribute--fill--vml.md)                            | Определяет цвет заливки.                           |
| [Color2](color2-attribute--fill--vml.md)                          | Определяет второй цвет заливки.                   |
| [Цвета](msdn-online-vml-colors-attribute.md)                     | Определяет несколько цветов для градиентной заливки.           |
| [детектмаусекликк](detectmouseclick-attribute--fill--vml.md)      | Определяет, обнаруживается ли щелчок мыши.          |
| [Фокус](msdn-online-vml-focus-attribute.md)                       | Определяет центр заливки линейного градиента.          |
| [фокуспоситион](msdn-online-vml-focusposition-attribute.md)       | Определяет центр заливки радиального градиента.          |
| [фокуссизе](msdn-online-vml-focussize-attribute.md)               | Определяет размер фокуса для радиальной заливки.              |
| [Полный](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Определяет URL-адрес исходного файла изображения.              |
| [Идентификатор](id-attribute--fill--vml.md)                                  | Определяет уникальный идентификатор для заливки.              |
| [Метод](msdn-online-vml-method-attribute.md)                     | Определяет метод, используемый для создания градиентной заливки.   |
| [On](on-attribute--fill--vml.md) (Вкл.)                                  | Определяет, отображается ли будет заливка.          |
| [Непрозрачность](opacity-attribute--fill--vml.md)                        | Определяет прозрачность заливки.                    |
| [Opacity2](msdn-online-vml-opacity2-attribute.md)                 | Определяет прозрачность второго цвета заливки.     |
| [Исходный домен](origin-attribute--fill--vml.md)                          | Определяет центр изображения.                        |
| [Позиция](position-attribute--fill--vml.md)                      | Определяет расположение изображения.                      |
| [Размер](size-attribute--fill--vml.md)                              | Определяет размер изображения.                          |
| [Src](src-attribute--fill--vml.md)                                | Определяет изображение, которое загружается для заполнения.                  |
| [Title](title-attribute--fill--vml.md)                            | Определяет заголовок заливки.                           |
| [Тип](type-attribute--fill--vml.md)                              | Определяет тип заливки.                              |



 

**Замечания**

Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .

В следующем коде показана простая Градиентная заливка для фигуры.


```HTML
   <v:shape
   style="position:relative;top:1;left:1;width:400;height:400"
   path = "m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type=gradient color="blue" color2="yellow"/>
   </v:shape>
```



**Примеры**

-   [Простая Градиентная заливка](/previous-versions/bb229620(v=vs.85))
-   [Пример динамической заливки](/previous-versions/bb229621(v=vs.85))

 

 