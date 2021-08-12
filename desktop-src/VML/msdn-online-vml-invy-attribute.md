---
title: Атрибут ИНВИ VML
description: Атрибут ИНВИ VML
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d012e8ac6afe0e7808236c36d8dd3088ce9fa3552b4b7efa0542ea8612e4d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599872"
---
# <a name="vml-invy-attribute"></a>Атрибут ИНВИ VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, инвертирована ли координата y маркера. Read/write. **Вгтристате**.

**Применимо к**:

[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))

**Синтаксис тега**

<v: *element* ИНВИ = " *выражение* " >

**Замечания**

Если **значение равно true**, то y-координата маркера инвертирована путем вычитания значения y из значения y **курдоригин** , добавленного к значению y **курдсизе**. Значение по умолчанию равно **False**.

Этот атрибут эквивалентен


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*Стандартный атрибут VML*

 

 