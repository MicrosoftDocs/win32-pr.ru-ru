---
title: Атрибут Имажеаспект VML
description: Атрибут Имажеаспект VML
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f67d715d5cd10d36b4e8e7e32f939aeeef2bbdd894aba9da5a069ef03f0e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600357"
---
# <a name="vml-imageaspect-attribute"></a>Атрибут Имажеаспект VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, как будет сохраняться пропорции изображения обводки. Read/write. **Строка**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v:

element *имажеаспект = "* выражение *" >*

**Синтаксис сценария**

element *. имажеаспект = "* выражение *"*

*=* элемент Expression *. имажеаспект*

**Замечания**

К этим значениям относятся следующие.



| Значение   | Описание                                |
|---------|--------------------------------------------|
| Игнорировать  | Пропускать проблемы с аспектами.                      |
| Задать | Размер изображения по меньшей мере равен **ImageSize**. |
| атмост  | Размер изображения не превышает **ImageSize**.     |



 

В каждом случае атрибут **ImageSize** будет скорректирован для сохранения аспекта изображения.

*Стандартный атрибут VML*

**Пример**

Изображение обводки будет по крайней мере большим, чем размер изображения.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 