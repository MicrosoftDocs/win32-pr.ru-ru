---
title: Атрибут VML V-Text-кернинг
description: Атрибут VML V-Text-кернинг
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987719"
---
# <a name="vml-v-text-kern-attribute"></a>Атрибут VML V-Text-кернинг

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, включен ли кернинг. Read/write. **Вгтристате**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "v-Text-кернинг: *выражение* " >

**Синтаксис сценария**

*element* . Style. v-Text-кернинг = "*выражение*"

*выражение* = *element*. Style. v-Text-кернинг

**Замечания**

Если **значение равно true**, кернинг включен. По умолчанию **False**. Кернинг — это удаление пробела между определенными парами букв, чтобы компенсировать нечетные леттерформс. Например, если кернинг включен, дополнительное пространство между заглавной буквой «T» и строчной буквой «i» будет удалено.

*Стандартный атрибут VML*

**Пример**

Кернинг включен.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 