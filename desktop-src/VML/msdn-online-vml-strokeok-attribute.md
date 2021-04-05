---
title: Атрибут Строкеок VML
description: Атрибут Строкеок VML
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a2875e3e6e8374238340ff2a596852e5ebce7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987720"
---
# <a name="vml-strokeok-attribute"></a>Атрибут Строкеок VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли отображаться штрих. Read/write. **Вгтристате**.

**Применимо к**:

[Путь](msdn-online-vml-path-element.md)

**Синтаксис тега**

<v: *element* строкеок = " *выражение* " >

**Синтаксис сценария**

*element* . строкеок = "*выражение*"

*выражение* = *element*. строкеок

**Замечания**

Если **значение равно false**, то контур не может быть обводкой. Значение по умолчанию равно **True**. Этот атрибут переопределяет все остальные атрибуты Stroke в родительском элементе или элементе **Stroke** .

*Стандартный атрибут VML*

**Пример**

Этот путь не будет обводкой.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 