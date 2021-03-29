---
title: Атрибут Инвкс VML
description: Атрибут Инвкс VML
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792205"
---
# <a name="vml-invx-attribute"></a>Атрибут Инвкс VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, инвертирована ли Координата x маркера. Read/write. **Вгтристате**.

**Применимо к**:

[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))

**Синтаксис тега**

<v: *element* инвкс = " *выражение* " >

**Замечания**

Если **значение равно true**, то Координата x для маркера инвертирована путем вычитания значения x из значения x **курдоригин** , добавленного к значению x объекта **курдсизе**. Значение по умолчанию равно **False**.

Этот атрибут эквивалентен

курдоригин. x + курдсизе. x-h. позиционирование. x

*Стандартный атрибут VML*

 

 