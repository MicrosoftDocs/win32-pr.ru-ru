---
title: Атрибут Имажеалигншапе VML
description: Атрибут Имажеалигншапе VML
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86090936556ba8a4f022024f292293b396d953d46962423a222b172adc2a15f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600472"
---
# <a name="vml-imagealignshape-attribute"></a>Атрибут Имажеалигншапе VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет выравнивание изображения обводки. Read/write. **Вгтристате**.

**Применимо к**:

[Водок](msdn-online-vml-stroke-element.md)

**Синтаксис тега**

<v:

element *имажеалигншапе = "* выражение *" >*

**Синтаксис сценария**

element *. имажеалигншапе = "* выражение *"*

*=* элемент Expression *. имажеалигншапе*

**Замечания**

Если **значение равно true**, выровняйте изображение с фигурой, в противном случае выровняйте изображение с помощью окна. Значение по умолчанию равно **True**.

*Стандартный атрибут VML*

**Пример**

Изображение будет согласовано с окном.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 