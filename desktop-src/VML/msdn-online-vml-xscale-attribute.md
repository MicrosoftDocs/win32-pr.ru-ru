---
title: Атрибут VML XScale
description: Атрибут VML XScale
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337700"
---
# <a name="vml-xscale-attribute"></a>Атрибут VML XScale

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли использоваться прямой текстпас вместо пути к фигуре. Read/write. **Вгтристате**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "XScale: *Expression* " >

**Синтаксис сценария**

*element* . Style. XScale = "*выражение*"

*выражение* = *элемент*. Style. XScale

**Замечания**

Если **значение равно true**, текст выполняется вдоль АПАС слева направо вдоль значения x нижней границы фигуры. Значение по умолчанию равно **False**.

*Стандартный атрибут VML*

**Пример**

Текст будет выглядеть так, будто он был нарисован на горизонтальной линии, даже если контур фигуры является диагональным.


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 