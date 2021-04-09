---
title: Главный атрибут VML
description: Главный атрибут VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134550"
---
# <a name="vml-master-attribute"></a>Главный атрибут VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, является ли элемент **шапетипе** главным элементом. Read/write. **Вгтристате**.

**Применимо к**:

[шапетипе](msdn-online-vml-shapetype-element.md)

**Синтаксис тега**

<v: *element* о:Мастер = " *выражение* " >

**Замечания**

Если **значение — true**, фигура **шапетипе** подготавливается к просмотру модулем визуализации. Значение по умолчанию равно **False**.

*Атрибут расширений Microsoft Office*

**Пример**

Элемент **шапетипе** является главной фигурой.


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 