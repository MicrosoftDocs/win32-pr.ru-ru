---
title: Счетчики, запросы и измерение производительности
description: В следующих разделах описываются функции для использования при тестировании и улучшении производительности, такие как запросы, счетчики, время и затенения.
ms.assetid: C7AEF1A0-36FB-4026-9CCF-ED0206961A58
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf316978f3dd0928692f378dd8d72b8453ad0aae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105102"
---
# <a name="counters-queries-and-performance-measurement"></a><span data-ttu-id="716fc-103">Счетчики, запросы и измерение производительности</span><span class="sxs-lookup"><span data-stu-id="716fc-103">Counters, Queries and Performance Measurement</span></span>

<span data-ttu-id="716fc-104">В следующих разделах описываются функции для использования при тестировании и улучшении производительности, такие как запросы, счетчики, время и затенения.</span><span class="sxs-lookup"><span data-stu-id="716fc-104">The following sections describe features for use in performance testing and improvement, such as queries, counters, timing, and predication.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="716fc-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="716fc-105">In this section</span></span>



| <span data-ttu-id="716fc-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="716fc-106">Topic</span></span>                                                                                                 | <span data-ttu-id="716fc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="716fc-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="716fc-108">Счетчики потокового вывода, счетчики UAV, запросы и затенения</span><span class="sxs-lookup"><span data-stu-id="716fc-108">Stream-Output Counters, UAV Counters, Queries, and Predication</span></span>](counters-and-queries.md)<br/> | <span data-ttu-id="716fc-109">Потоковый выход и счетчики UAV работают в Direct3D 12 в аналогичном методе для Direct3D 11, хотя теперь память для счетчиков должна выделяться приложением, драйвер не выполняет его.</span><span class="sxs-lookup"><span data-stu-id="716fc-109">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="716fc-110">Запросы в Direct3D 12 более отличаются от запросов в Direct3D 11, с добавлением ограждений и другими процессами, которые изменяют потребность в некоторых типах запросов.</span><span class="sxs-lookup"><span data-stu-id="716fc-110">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span><br/> |
| [<span data-ttu-id="716fc-111">Временные свойства</span><span class="sxs-lookup"><span data-stu-id="716fc-111">Timing</span></span>](timing.md)<br/>                                                                       | <span data-ttu-id="716fc-112">В этом разделе рассматриваются запросы к отметкам времени и калибровка GPU и счетчиков времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="716fc-112">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="716fc-113">Затенения</span><span class="sxs-lookup"><span data-stu-id="716fc-113">Predication</span></span>](predication.md)<br/>                                                             | <span data-ttu-id="716fc-114">Затенения — это функция, которая позволяет GPU, а не ЦП определять, что не может рисовать, копировать или отправлять объект.</span><span class="sxs-lookup"><span data-stu-id="716fc-114">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span><br/>                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="716fc-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="716fc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="716fc-116">Руководство по программированию для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="716fc-116">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





