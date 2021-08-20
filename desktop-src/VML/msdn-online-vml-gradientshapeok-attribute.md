---
title: Атрибут Градиентшапеок VML
description: Атрибут Градиентшапеок VML
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c25620f8ebc05905b83f3abab7b52f7a206b6bafb522b0104f06fd8f46d6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124777"
---
# <a name="vml-gradientshapeok-attribute"></a>Атрибут Градиентшапеок VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли путь градиента состоять из повторяющихся концентрических путей. Read/write. **Вгтристате**.

**Применимо к**:

[Путь](msdn-online-vml-path-element.md)

**Синтаксис тега**

<v: *element* градиентшапеок = " *выражение* " >

**Синтаксис сценария**

*element* . градиентшапеок = "*выражение*"

*выражение* = *element*. градиентшапеок

**Замечания**

Если **значение — true**, путь будет заполнен концентрическим градиентным заполнением с использованием пути как повторяющейся формы градиента. Значение по умолчанию — **false**.

*Стандартный атрибут VML*

**Пример**

Путь будет заполнен концентрическим градиентным заполнением, который состоит из повторяющихся прямоугольников.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 