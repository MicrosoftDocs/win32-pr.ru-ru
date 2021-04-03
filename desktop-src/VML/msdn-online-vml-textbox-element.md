---
title: Элемент TextBox в формате VML
description: Элемент TextBox в формате VML
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a46ce8b6636b79099b7f7423fd8f746602a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791826"
---
# <a name="vml-textbox-element"></a>Элемент TextBox в формате VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет текстовое поле для фигуры.

Следующие атрибуты изменяют текстовое поле.



| attribute                                                                    | Описание                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Направление](msdn-online-vml-direction-attribute.md)                         | Определяет направление текста.                         |
| [Идентификатор](id-attribute--textbox--vml.md)                                         | Определяет уникальный идентификатор для текстового поля.               |
| [Вставка](msdn-online-vml-inset-attribute.md)                                 | Задает значения внутренних полей для текстового поля.            |
| [инсетмоде](msdn-online-vml-insetmode-attribute.md)                         | Определяет, как приложение будет допускать значения настраиваемых отступов. |
| [Макет — поток](msdn-online-vml-layout-flow-attribute.md)                     | Определяет поток текста в текстовом поле.            |
| [MSO-Direction-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Определяет альтернативные направления для текста в текстовых полях.        |
| [MSO-Fit-Shape-to-Text](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Определяет, растягивается ли фигура по размеру текста.       |
| [MSO-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Определяет, будет ли текст растянут до размера фигуры.       |
| [MSO-Layout-Flow-Alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Определяет альтернативный поток макета для текста в текстовом поле.   |
| [MSO-Next-TextBox](msdn-online-vml-mso-next-textbox-attribute.md)           | Указывает следующее текстовое поле в ряду.                    |
| [MSO — поворот](msdn-online-vml-mso-rotate-attribute.md)                       | Определяет, поворачивается ли текст с поворотной фигурой.      |
| [MSO-Text-Scale](msdn-online-vml-mso-text-scale-attribute.md)               | Определяет коэффициент масштабирования для подгонки текста к фигурам.     |
| [синглекликк](msdn-online-vml-singleclick-attribute.md)                     | Определяет возможность выбора текста одним щелчком. |
| [V-Text-Anchor](msdn-online-vml-v-text-anchor-attribute.md)                 | Определяет вертикальную привязку текста в текстовом поле.       |



 

**Замечания**

Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .

Ниже приведен минимальный код, необходимый для создания текстового поля.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Обратите внимание, что текст, отображаемый в текстовом поле, заключен в теги TextBox. Текст внутри тегов может быть изменен обычными тегами HTML.

**Пример**

-   [Пример простого текстового поля](/previous-versions/bb264075(v=vs.85))

 

 