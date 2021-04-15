---
title: Атрибут ИНВИ VML
description: Атрибут ИНВИ VML
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338009"
---
# <a name="vml-invy-attribute"></a>Атрибут ИНВИ VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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

 

 