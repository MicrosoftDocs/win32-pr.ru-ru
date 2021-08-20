---
title: Главный атрибут VML
description: Главный атрибут VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d126b9d02144bbc8831d7be9e73a3e5896c2ceccca71cfcbc8161d5ccc8112f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999114"
---
# <a name="vml-master-attribute"></a>Главный атрибут VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, является ли элемент **шапетипе** главным элементом. Read/write. **Вгтристате**.

**Применимо к**:

[шапетипе](msdn-online-vml-shapetype-element.md)

**Синтаксис тега**

<v: *element* о:Мастер = " *выражение* " >

**Замечания**

Если **значение — true**, фигура **шапетипе** подготавливается к просмотру модулем визуализации. Значение по умолчанию равно **False**.

*Microsoft Office Extensions, атрибут*

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



 

 