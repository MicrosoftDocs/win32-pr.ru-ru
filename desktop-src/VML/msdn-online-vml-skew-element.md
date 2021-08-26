---
title: Элемент отклонения VML
description: Элемент отклонения VML
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d659d16e6d10e9ec88875989a812de82403d2ac5b946580e7c7b7def956b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099044"
---
# <a name="vml-skew-element"></a>Элемент отклонения VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет наклон для фигуры.

Следующие атрибуты изменяют асимметрию.



| attribute                                 | Описание                                    |
|-------------------------------------------|------------------------------------------------|
| [WLAN](ext-attribute--skew--vml.md)       | Определяет способ отображения наклона.           |
| [Идентификатор](id-attribute--skew--vml.md)         | Определяет уникальный идентификатор для наклона.        |
| [Матрица](matrix-attribute--skew--vml.md) | Определяет преобразование перспективы для наклона.    |
| [Offset](offset-attribute--skew--vml.md) | Определяет смещение наклона.                  |
| [On](on-attribute--skew--vml.md) (Вкл.)         | Определяет, будет ли отображаться асимметрия. |
| [Исходный домен](origin-attribute--skew--vml.md) | Определяет источник наклона.               |



 

**Замечания**

Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .

Кроме того, [Матрица](matrix-attribute--skew--vml.md) и [атрибуты](on-attribute--skew--vml.md) должны иметь значение **true**.

Ниже приведен минимальный код, необходимый для создания наклона.


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



элемент **асимметрии** является Microsoft Office расширением для VML.

**Примеры**

-   [Пример простого наклона](/previous-versions/bb229482(v=vs.85))
-   [Пример динамической отклонения](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 