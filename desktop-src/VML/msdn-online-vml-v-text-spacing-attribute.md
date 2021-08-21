---
title: Атрибут расстояния по тексту VML V
description: Атрибут расстояния по тексту VML V
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0b699e70cd235bf7d0f7530f75a8fc5eaef52974180cc8d36a10a69c9197f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057682"
---
# <a name="vml-v-text-spacing-attribute"></a>Атрибут расстояния по тексту VML V

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет величину интервала для текста. Read/write. **Вгнумбер**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "v-Text-просвет: *Expression* " >

**Синтаксис сценария**

*element* . Style. v-Text-просвет = "*выражение*"

*выражение* = Text *. Style. v*-текстовые отступы

**Замечания**

По умолчанию используется значение 100. Дополнительные сведения о межтекстовых шагах см. в разделе атрибут [V-text-mode](msdn-online-vml-v-text-spacing-mode-attribute.md) .

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



 

 