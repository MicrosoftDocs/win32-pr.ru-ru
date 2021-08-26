---
title: Атрибут Рулепрокси VML
description: Атрибут Рулепрокси VML
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fe97afee190d87b5e6f8b74d942a72d3bf11914373931e32cbb9459915b7d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099134"
---
# <a name="vml-ruleproxy-attribute"></a>Атрибут Рулепрокси VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли использоваться прокси-сервер для обработчика правил. Read/write. **Вгтристате**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *element* рулепрокси = " *выражение* " >

**Замечания**

Значение по умолчанию равно **False**. Если задано **значение true**, используется прокси-сервер.

*Microsoft Office Extensions, атрибут*

**Пример**

Для обработки фигуры используется прокси-сервер.


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 