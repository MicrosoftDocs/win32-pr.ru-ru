---
description: Общие методы Graph-Building
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Общие методы Graph-Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262304"
---
# <a name="general-graph-building-techniques"></a>Общие методы Graph-Building

Каждое приложение DirectShow начинается с создания графа фильтра. По мере ознакомления с обзорными разделами в документации по DirectShow вы узнаете, как лучше всего начать с описания того, какой тип графа фильтра вам нужен. В некоторых случаях существует метод или вспомогательный объект, специально предназначенный для создания такого типа графа. Например, объект " [Построитель DVD Graph](dvd-graph-builder.md) " создает графы воспроизведения DVD-дисков. В других случаях приложение должно создать граф, добавив фильтры и соединив их.

В этом разделе представлены некоторые вспомогательные функции, реализующие базовые операции построения графа. Они могут использоваться любым приложением DirectShow, которое должно создавать или изменять графы фильтров. В этом разделе рассматриваются следующие вопросы.

-   [Добавление фильтра по CLSID](add-a-filter-by-clsid.md)
-   [Поиск неподключенного ПИН-кода в фильтре](find-an-unconnected-pin-on-a-filter.md)
-   [Соединение двух фильтров](connect-two-filters.md)
-   [Поиск интерфейса в фильтре или ПИН-коде](find-an-interface-on-a-filter-or-pin.md)
-   [Поиск однорангового узла фильтра](find-a-filters-peer.md)
-   [Удаление всех фильтров в графе](remove-all-the-filters-in-the-graph.md)
-   [Построение диаграмм с помощью построителя графа записи](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные задачи DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[Перечисление устройств и фильтров](enumerating-devices-and-filters.md)
</dt> <dt>

[Перечисление объектов в графе фильтра](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Интеллектуальное подключение](intelligent-connect.md)
</dt> </dl>

 

 



