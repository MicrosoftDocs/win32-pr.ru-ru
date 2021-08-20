---
title: Атрибут печати VML
description: Атрибут печати VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfa364e573d887da2013f946ddf23e0a974e0f63211623de3d2046b0525b2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057732"
---
# <a name="vml-print-attribute"></a>Атрибут печати VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли распечатана фигура. Read/write. [Вгтристате](msdn-online-vml-vgtristate.md).

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *элемент* Print = " *выражение* " >

**Синтаксис сценария**

*элемент* . Print = "*выражение*"

*выражение* = *элемент*. Print

**Замечания**

Позволяет указать, будут ли напечатаны фигуры. Обратите внимание, что фигура по-прежнему может отображаться на экране, даже если она не печатается в результате **ложного** этого атрибута. По умолчанию используется значение **True**.

этот атрибут используется Microsoft Office но не используется обозревателем Microsoft Internet Explorer.

*Microsoft Office Extensions, атрибут*

 

 