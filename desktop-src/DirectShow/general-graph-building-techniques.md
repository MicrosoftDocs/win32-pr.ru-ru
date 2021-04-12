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
# <a name="general-graph-building-techniques"></a><span data-ttu-id="ee4d6-103">Общие методы Graph-Building</span><span class="sxs-lookup"><span data-stu-id="ee4d6-103">General Graph-Building Techniques</span></span>

<span data-ttu-id="ee4d6-104">Каждое приложение DirectShow начинается с создания графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="ee4d6-104">Every DirectShow application starts by building a filter graph.</span></span> <span data-ttu-id="ee4d6-105">По мере ознакомления с обзорными разделами в документации по DirectShow вы узнаете, как лучше всего начать с описания того, какой тип графа фильтра вам нужен.</span><span class="sxs-lookup"><span data-stu-id="ee4d6-105">As you read the overview topics in the DirectShow documentation, you will find that most start by describing what kind of filter graph you need.</span></span> <span data-ttu-id="ee4d6-106">В некоторых случаях существует метод или вспомогательный объект, специально предназначенный для создания такого типа графа.</span><span class="sxs-lookup"><span data-stu-id="ee4d6-106">In some cases, there is a method or a helper object specifically designed for building that type of graph.</span></span> <span data-ttu-id="ee4d6-107">Например, объект " [Построитель DVD Graph](dvd-graph-builder.md) " создает графы воспроизведения DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="ee4d6-107">For example, the [DVD Graph Builder](dvd-graph-builder.md) object builds DVD playback graphs.</span></span> <span data-ttu-id="ee4d6-108">В других случаях приложение должно создать граф, добавив фильтры и соединив их.</span><span class="sxs-lookup"><span data-stu-id="ee4d6-108">In other cases, the application must construct the graph by adding filters and connecting them.</span></span>

<span data-ttu-id="ee4d6-109">В этом разделе представлены некоторые вспомогательные функции, реализующие базовые операции построения графа.</span><span class="sxs-lookup"><span data-stu-id="ee4d6-109">This section presents some helper functions that implement basic graph-building operations.</span></span> <span data-ttu-id="ee4d6-110">Они могут использоваться любым приложением DirectShow, которое должно создавать или изменять графы фильтров.</span><span class="sxs-lookup"><span data-stu-id="ee4d6-110">They can be used by any DirectShow application that needs to build or modify a filter graph.</span></span> <span data-ttu-id="ee4d6-111">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="ee4d6-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="ee4d6-112">Добавление фильтра по CLSID</span><span class="sxs-lookup"><span data-stu-id="ee4d6-112">Add a Filter by CLSID</span></span>](add-a-filter-by-clsid.md)
-   [<span data-ttu-id="ee4d6-113">Поиск неподключенного ПИН-кода в фильтре</span><span class="sxs-lookup"><span data-stu-id="ee4d6-113">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
-   [<span data-ttu-id="ee4d6-114">Соединение двух фильтров</span><span class="sxs-lookup"><span data-stu-id="ee4d6-114">Connect Two Filters</span></span>](connect-two-filters.md)
-   [<span data-ttu-id="ee4d6-115">Поиск интерфейса в фильтре или ПИН-коде</span><span class="sxs-lookup"><span data-stu-id="ee4d6-115">Find an Interface on a Filter or Pin</span></span>](find-an-interface-on-a-filter-or-pin.md)
-   [<span data-ttu-id="ee4d6-116">Поиск однорангового узла фильтра</span><span class="sxs-lookup"><span data-stu-id="ee4d6-116">Find a Filter's Peer</span></span>](find-a-filters-peer.md)
-   [<span data-ttu-id="ee4d6-117">Удаление всех фильтров в графе</span><span class="sxs-lookup"><span data-stu-id="ee4d6-117">Remove All the Filters in the Graph</span></span>](remove-all-the-filters-in-the-graph.md)
-   [<span data-ttu-id="ee4d6-118">Построение диаграмм с помощью построителя графа записи</span><span class="sxs-lookup"><span data-stu-id="ee4d6-118">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a><span data-ttu-id="ee4d6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ee4d6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee4d6-120">Основные задачи DirectShow</span><span class="sxs-lookup"><span data-stu-id="ee4d6-120">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="ee4d6-121">Перечисление устройств и фильтров</span><span class="sxs-lookup"><span data-stu-id="ee4d6-121">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="ee4d6-122">Перечисление объектов в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="ee4d6-122">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="ee4d6-123">Интеллектуальное подключение</span><span class="sxs-lookup"><span data-stu-id="ee4d6-123">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 



