---
title: Элемент Имажедата VML
description: Элемент Имажедата VML
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b416a53f97efc8a1f1875eda0e842c4cfbe96bf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672313"
---
# <a name="vml-imagedata-element"></a>Элемент Имажедата VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет изображение для фигуры.

Следующие атрибуты изменяют изображение.



| attribute                                                          | Описание                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [алсреф](althref-attribute--imagedata--vml.md)                   | Указывает альтернативную ссылку для изображения.                        |
| [билевел](msdn-online-vml-bilevel-attribute.md)                   | Определяет, будет ли изображение отображаться черно-белым цветом.          |
| [блакклевел](msdn-online-vml-blacklevel-attribute.md)             | Определяет интенсивность черного цвета в изображении.                        |
| [чромакэй](msdn-online-vml-chromakey-attribute.md)               | Определяет цвет в палатте, который будет считаться прозрачным. |
| [кропботтом](msdn-online-vml-cropbottom-attribute.md)             | Определяет процент удаления изображения с нижней стороны.       |
| [кроплефт](msdn-online-vml-cropleft-attribute.md)                 | Определяет процент удаления изображения с левой стороны.         |
| [кропригхт](msdn-online-vml-cropright-attribute.md)               | Определяет процент удаления изображения с правой стороны.        |
| [кроптоп](msdn-online-vml-croptop-attribute.md)                   | Определяет процент удаления изображения с верхней стороны.          |
| [детектмаусекликк](detectmouseclick-attribute--imagedata--vml.md) | Определяет, будет ли обнаружено нажатие кнопки мыши.                    |
| [ембоссколор](msdn-online-vml-embosscolor-attribute.md)           | Определяет цвет для рельефных цветовых эффектов.                         |
| [Выигрыш](msdn-online-vml-gain-attribute.md)                         | Определяет интенсивность всех цветов в изображении.                      |
| [Цвет](msdn-online-vml-gamma-attribute.md)                       | Определяет степень контрастности изображения.                          |
| [Оттенки серого](msdn-online-vml-grayscale-attribute.md)               | Определяет, будет ли изображение отображаться в режиме градации серого.          |
| [Полный](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Определяет URL-адрес изображения.                                           |
| [Идентификатор](id-attribute--image--vml.md)                                 | Определяет уникальный идентификатор изображения.                             |
| [Кинофильм](msdn-online-vml-movie-attribute.md)                       | Определяет указатель на изображение фильма.                                   |
| [олеид](msdn-online-vml-oleid-attribute.md)                       | Хранит идентификатор OLE изображения.                                        |
| [Src](src-attribute--imagedata--vml.md)                           | Определяет источник изображения.                                       |
| [Title](title-attribute--imagedata--vml.md)                       | Определяет заголовок изображения.                                        |



 

**Замечания**

Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .

Кроме того, атрибут [**src**](src-attribute--imagedata--vml.md) должен указывать на изображение.

Ниже приведен минимальный код, необходимый для создания образа.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> В предварительных версиях VML этот элемент назывался **Image** .

 

**Примеры**

-   [Пример простого Имажедата](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Пример динамического Имажедата](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 