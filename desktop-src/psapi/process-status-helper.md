---
title: API состояния процесса
description: Получение сведений о процессах, модулях (исполняемых файлах или библиотеках DLL) и драйверах устройств. Получение данных об использовании памяти. Сделайте моментальные снимки объема памяти, физически сопоставленного с контекстом процесса.
ms.assetid: 512c3f0f-b1b5-43a0-9460-eb668315d6f4
keywords:
- API состояния процесса
- вспомогательное приложение состояния процесса
- PSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a2234ee53acda22df6b6be6267815ba68090be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070477"
---
# <a name="process-status-api"></a><span data-ttu-id="cdfc0-108">API состояния процесса</span><span class="sxs-lookup"><span data-stu-id="cdfc0-108">Process Status API</span></span>

<span data-ttu-id="cdfc0-109">Программный интерфейс "состояние процесса" (PSAPI) — это вспомогательная библиотека, которая упрощает получение сведений о процессах и драйверах устройств.</span><span class="sxs-lookup"><span data-stu-id="cdfc0-109">The process status application programming interface (PSAPI) is a helper library that makes it easier for you to obtain information about processes and device drivers.</span></span> <span data-ttu-id="cdfc0-110">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="cdfc0-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="cdfc0-111">О PSAPI</span><span class="sxs-lookup"><span data-stu-id="cdfc0-111">About PSAPI</span></span>](about-psapi.md)
-   [<span data-ttu-id="cdfc0-112">Использование PSAPI</span><span class="sxs-lookup"><span data-stu-id="cdfc0-112">Using PSAPI</span></span>](using-psapi.md)
-   [<span data-ttu-id="cdfc0-113">Справочник по PSAPI</span><span class="sxs-lookup"><span data-stu-id="cdfc0-113">PSAPI Reference</span></span>](psapi-reference.md)

<span data-ttu-id="cdfc0-114">Эти функции доступны в Psapi.dll.</span><span class="sxs-lookup"><span data-stu-id="cdfc0-114">These functions are available in Psapi.dll.</span></span>

<span data-ttu-id="cdfc0-115">Одни и те же сведения доступны через данные о производительности в реестре.</span><span class="sxs-lookup"><span data-stu-id="cdfc0-115">The same information is generally available through the performance data in the registry.</span></span> <span data-ttu-id="cdfc0-116">Дополнительные сведения см. в статье [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="cdfc0-116">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

 

 