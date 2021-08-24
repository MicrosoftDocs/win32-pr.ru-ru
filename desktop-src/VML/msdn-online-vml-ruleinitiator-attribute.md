---
title: Атрибут Рулеинитиатор VML
description: Атрибут Рулеинитиатор VML
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b015ba3742eda42fd506d955bbc8d2b9d7285999581897952dede665c9eb3361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654964"
---
# <a name="vml-ruleinitiator-attribute"></a>Атрибут Рулеинитиатор VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли использоваться обработчик правил. Read/write. **Вгтристате**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:рулеинитиатор = " *выражение* " >

**Замечания**

Значение по умолчанию равно **False**. Если значение равно **true**, используется обработчик правил.

*Microsoft Office Extensions, атрибут*

**Пример**

Фигура будет обработана обработчиком правил.


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 