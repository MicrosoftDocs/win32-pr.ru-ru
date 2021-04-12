---
title: Атрибут Филлок VML
description: Атрибут Филлок VML
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667524be103b7c641643a52a85368a82a1289e5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339177"
---
# <a name="vml-fillok-attribute"></a>Атрибут Филлок VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли отображаться заливка. Read/write. **Вгтристате**.

**Применимо к**:

[Путь](msdn-online-vml-path-element.md)

**Синтаксис тега**

<v: *element* филлок = " *выражение* " >

**Синтаксис сценария**

*element* . филлок = "*выражение*"

*выражение* = *element*. филлок

**Замечания**

Если **значение равно false**, то путь не может быть заполнен. Значение по умолчанию равно **True**. Этот атрибут переопределяет все остальные атрибуты заливки в родительском элементе или элементе **Fill** .

*Стандартный атрибут VML*

**Пример**

Путь не будет заполнен.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 