---
title: Счетчики, запросы и затенения
description: Потоковый выход и счетчики UAV работают в Direct3D 12 в аналогичном методе для Direct3D 11, хотя теперь память для счетчиков должна выделяться приложением, драйвер не выполняет его.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104549026"
---
# <a name="counters-queries-and-predication"></a><span data-ttu-id="b8715-103">Счетчики, запросы и затенения</span><span class="sxs-lookup"><span data-stu-id="b8715-103">Counters, queries, and predication</span></span>

<span data-ttu-id="b8715-104">В этом разделе рассматриваются счетчики потокового вывода, счетчики UAV, запросы и затенения.</span><span class="sxs-lookup"><span data-stu-id="b8715-104">This topic covers stream-output counters, UAV counters, queries, and predication.</span></span>

<span data-ttu-id="b8715-105">Потоковый выход и счетчики UAV работают в Direct3D 12 в аналогичном методе для Direct3D 11, хотя теперь память для счетчиков должна выделяться приложением, драйвер не выполняет его.</span><span class="sxs-lookup"><span data-stu-id="b8715-105">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="b8715-106">Запросы в Direct3D 12 более отличаются от запросов в Direct3D 11, с добавлением ограждений и другими процессами, которые изменяют потребность в некоторых типах запросов.</span><span class="sxs-lookup"><span data-stu-id="b8715-106">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b8715-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b8715-107">In this section</span></span>



| <span data-ttu-id="b8715-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="b8715-108">Topic</span></span>                                                           | <span data-ttu-id="b8715-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b8715-109">Description</span></span>                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8715-110">Счетчики потокового вывода</span><span class="sxs-lookup"><span data-stu-id="b8715-110">Stream Output Counters</span></span>](stream-output-counters.md)<br/> | <span data-ttu-id="b8715-111">Потоковая передача данных — это способность GPU записывать вершины в буфер.</span><span class="sxs-lookup"><span data-stu-id="b8715-111">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="b8715-112">Счетчики потокового вывода отслеживают ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="b8715-112">The stream output counters monitor progress.</span></span><br/>                                                               |
| [<span data-ttu-id="b8715-113">Счетчики UAV</span><span class="sxs-lookup"><span data-stu-id="b8715-113">UAV Counters</span></span>](uav-counters.md)<br/>                     | <span data-ttu-id="b8715-114">Счетчики UAV можно использовать для связывания 32-разрядного атомарного счетчика с неупорядоченным представлением доступа (UAV).</span><span class="sxs-lookup"><span data-stu-id="b8715-114">UAV counters can be used to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span><br/>                                                                                |
| [<span data-ttu-id="b8715-115">Запросы</span><span class="sxs-lookup"><span data-stu-id="b8715-115">Queries</span></span>](queries.md)<br/>                               | <span data-ttu-id="b8715-116">В Direct3D 12 запросы группируются в массивы запросов, которые называются кучами запросов.</span><span class="sxs-lookup"><span data-stu-id="b8715-116">In Direct3D 12, queries are grouped into arrays of queries called a query heap.</span></span> <span data-ttu-id="b8715-117">Куча запроса имеет тип, который определяет допустимые типы запросов, которые могут использоваться с этой кучей.</span><span class="sxs-lookup"><span data-stu-id="b8715-117">A query heap has a type which defines the valid types of queries that can be used with that heap.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b8715-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b8715-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8715-119">Измерение производительности</span><span class="sxs-lookup"><span data-stu-id="b8715-119">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>

 

 





