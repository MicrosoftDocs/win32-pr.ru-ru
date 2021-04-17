---
title: Атрибут Лигхтпоситион VML
description: Атрибут Лигхтпоситион VML
ms.assetid: 2ac3825d-319e-4761-905d-eb8127c4d4cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c7b1e034b8755da78e4a34cf72299380ca28af4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691518"
---
# <a name="vml-lightposition-attribute"></a>Атрибут Лигхтпоситион VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Задает расположение основного освещения в сцене. Read/write. **VgVector3D**.

**Применимо к**:

[Выдавливания](msdn-online-vml-extrusion-element.md)

**Синтаксис тега**

<o: *element* лигхтпоситион = " *выражение* " >

**Синтаксис сценария**

*element* . лигхтпоситион = "*выражение*"

*выражение* = *element*. лигхтпоситион

**Замечания**

Используйте это значение для перемещения источника освещения для объема. Разные позиции будут светлее или темнее на каждой грани. Значение по умолчанию — 50000, 0, 10000.

*Атрибут расширений Microsoft Office*

 

 