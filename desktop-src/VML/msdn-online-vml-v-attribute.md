---
title: Атрибут VML V
description: Атрибут VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134066"
---
# <a name="vml-v-attribute"></a>Атрибут VML V

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет команды, составляющие путь. Read/write. **Строка**.

**Применимо к**:

[Путь](msdn-online-vml-path-element.md)

**Синтаксис тега**

<v: *element* v = " *выражение* " >

**Синтаксис сценария**

*element* . v = "*выражение*"

*выражение* = *element*. v

**Замечания**

Переопределяет атрибут **path** фигуры. Координаты могут быть фиксированными числами, относительными числами или ссылками на формулы (с использованием формата " @n ", где n — номер формулы; например, " @2 " ссылается на вторую формулу в массиве формул).

*Стандартный атрибут VML*

**Пример**

Прямоугольник создается с помощью атрибута **V** . Обратите внимание, что после первого набора координат с разделителями-запятыми используется строчная буква L (**lineTo** ).


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 