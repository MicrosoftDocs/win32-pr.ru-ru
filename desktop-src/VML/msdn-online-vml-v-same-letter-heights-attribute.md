---
title: Атрибут высоты VML V-and-Letter
description: Атрибут высоты VML V-and-Letter
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791971"
---
# <a name="vml-v-same-letter-heights-attribute"></a>Атрибут высоты VML V-and-Letter

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будут ли все буквы иметь одинаковую высоту независимо от начального варианта. Read/write. **Вгтристате**.

**Применимо к**:

[текстпас](msdn-online-vml-textpath-element.md)

**Синтаксис тега**

<v: Style *элемента* = "v-та же буква-высота: *выражение* " >

**Синтаксис сценария**

*element* . Style. v-та же самая буква-высота = "*выражение*"

*выражение* = Высота *элемента*. Style. v-та же буква

**Замечания**

Если **значение равно true**, буквы в нижнем регистре растягиваются до высоты прописных букв. Значение по умолчанию равно **False**.

*Стандартный атрибут VML*

**Пример**

Все буквы будут одинаковой высотой, независимо от регистра.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 