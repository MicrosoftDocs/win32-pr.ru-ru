---
title: Атрибут Градиентшапеок VML
description: Атрибут Градиентшапеок VML
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413566"
---
# <a name="vml-gradientshapeok-attribute"></a>Атрибут Градиентшапеок VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 