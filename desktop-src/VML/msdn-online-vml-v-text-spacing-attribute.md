---
title: Атрибут расстояния по тексту VML V
description: Атрибут расстояния по тексту VML V
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413312"
---
# <a name="vml-v-text-spacing-attribute"></a>Атрибут расстояния по тексту VML V

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет величину интервала для текста. Read/write. **Вгнумбер**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "v-Text-просвет: *Expression* " >

**Синтаксис сценария**

*element* . Style. v-Text-просвет = "*выражение*"

*выражение* = Text *. Style. v*-текстовые отступы

**Замечания**

Значение по умолчанию — 100. Дополнительные сведения о межтекстовых шагах см. в разделе атрибут [V-text-mode](msdn-online-vml-v-text-spacing-mode-attribute.md) .

*Стандартный атрибут VML*

**Пример**

ЛеттерспаЦинг между каждой буквой заменяется на 200 единиц.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 