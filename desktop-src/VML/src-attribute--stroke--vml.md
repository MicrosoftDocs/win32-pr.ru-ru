---
title: Атрибут src (Stroke) (VML)
description: Атрибут src (Stroke) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bc71d7a36ee944a2352cde6bfa1ef33f0b5c480d78c7aada751ea67db9ca7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596630"
---
# <a name="src-attribute-strokevml"></a>Атрибут src (Stroke) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет исходное изображение для загрузки для заливки штриха. Read/write. **Строка**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v: *элемент* src = " *выражение* " >

**Синтаксис сценария**

*element* . src = "*выражение*"

*выражение* = *элемент*. src

**Замечания**

URL-адрес изображения, загружаемого для изображений и узорных заливок. Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения. Если этот атрибут встречается отдельно, то есть без **href** или **Title**, то изображение связывается.

*Стандартный атрибут VML*

**Пример**

Штрих создается с изображением, указанным в файле cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 