---
title: Атрибут печати VML
description: Атрибут печати VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672299"
---
# <a name="vml-print-attribute"></a>Атрибут печати VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли распечатана фигура. Read/write. [Вгтристате](msdn-online-vml-vgtristate.md).

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *элемент* Print = " *выражение* " >

**Синтаксис сценария**

*элемент* . Print = "*выражение*"

*выражение* = *элемент*. Print

**Замечания**

Позволяет указать, будут ли напечатаны фигуры. Обратите внимание, что фигура по-прежнему может отображаться на экране, даже если она не печатается в результате **ложного** этого атрибута. По умолчанию используется значение **True**.

Этот атрибут используется Microsoft Office но не используется обозревателем Microsoft Internet Explorer.

*Атрибут расширений Microsoft Office*

 

 