---
title: Теневой элемент VML
description: Теневой элемент VML
ms.assetid: 3e7d3e8c-45f8-4db3-95f3-7d993b7c2ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd73bb7087c2736ba5bec75102ffcb4337407650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987549"
---
# <a name="vml-shadow-element"></a>Теневой элемент VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет тень для фигуры.

Следующие атрибуты изменяют тень.



| attribute                                          | Описание                                        |
|----------------------------------------------------|----------------------------------------------------|
| [Цвет](color-attribute--shadow--vml.md)          | Определяет цвет тени.                     |
| [Color2](color2-attribute--shadow--vml.md)        | Определяет второй цвет тени.              |
| [Идентификатор](id-attribute--shadow--vml.md)                | Задает уникальный идентификатор тени.       |
| [Матрица](matrix-attribute--shadow--vml.md)        | Определяет преобразование тени на перспективу.     |
| [Неясными](msdn-online-vml-obscured-attribute.md) | Определяет, является ли тень прозрачной.      |
| [Offset](offset-attribute--shadow--vml.md)        | Определяет, насколько далеко тень расширяется после фигуры. |
| [Offset2](msdn-online-vml-offset2-attribute.md)   | Определяет второе смещение.                           |
| [On](on-attribute--shadow--vml.md) (Вкл.)                | Определяет, отображается ли тень.          |
| [Непрозрачность](opacity-attribute--shadow--vml.md)      | Определяет прозрачность тени.           |
| [Лета](origin-attribute--shadow--vml.md)        | Определяет центр тени.                  |
| [Тип](type-attribute--shadow--vml.md)            | Задает тип тени.                      |



 

**Замечания**

Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .

Кроме того, атрибут [On](on-attribute--shadow--vml.md) должен иметь значение **true**.

Ниже приведен минимальный код, необходимый для создания тени.


```HTML
   <v:rect
   fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True"/>
   </v:rect>
```



Вы не можете заметить тень, если не увеличите значения [смещения](offset-attribute--shadow--vml.md) , так как смещение по умолчанию — 2pt, 2PT.

**Примеры**

-   [Пример простого тени](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/t_shadow.md)
-   [Пример динамической теневой копии](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/x_shadow.md)

 

 