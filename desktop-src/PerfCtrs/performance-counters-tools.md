---
description: В следующей таблице перечислены
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Средства счетчиков производительности
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998508"
---
# <a name="performance-counters-tools"></a><span data-ttu-id="15968-103">Средства счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="15968-103">Performance Counters Tools</span></span>

## <a name="data-collection-tools"></a><span data-ttu-id="15968-104">Средства сбора данных</span><span class="sxs-lookup"><span data-stu-id="15968-104">Data collection tools</span></span>

<span data-ttu-id="15968-105">Следующие средства полезны при использовании данных счетчика производительности Windows или управлении ими.</span><span class="sxs-lookup"><span data-stu-id="15968-105">The following tools are useful when consuming or manipulating Windows Performance Counter data.</span></span>

|<span data-ttu-id="15968-106">Средство</span><span class="sxs-lookup"><span data-stu-id="15968-106">Tool</span></span>|<span data-ttu-id="15968-107">Описание</span><span class="sxs-lookup"><span data-stu-id="15968-107">Description</span></span>
|----|-----------
| [<span data-ttu-id="15968-108">PerfMon</span><span class="sxs-lookup"><span data-stu-id="15968-108">PerfMon</span></span>](/windows-server/administration/windows-commands/perfmon) | <span data-ttu-id="15968-109">Средство графического пользовательского интерфейса для сбора и просмотра данных счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="15968-109">GUI tool for collecting and viewing Performance Counter data.</span></span> <span data-ttu-id="15968-110">`perfmon.exe` Запускает MMC с оснасткой "системный монитор", которая предоставляет доступ к монитору производительности, наборам сборщиков данных и средствам отчетов.</span><span class="sxs-lookup"><span data-stu-id="15968-110">`perfmon.exe` launches MMC with the Performance Monitor snap-in, which provides access to the Performance Monitor, Data Collector Sets, and Reports tools.</span></span>
| [<span data-ttu-id="15968-111">типеперф</span><span class="sxs-lookup"><span data-stu-id="15968-111">TypePerf</span></span>](/windows-server/administration/windows-commands/typeperf) |<span data-ttu-id="15968-112">Программа командной строки для сбора и печати данных счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="15968-112">Command-line tool for collecting and printing Performance Counter data.</span></span> <span data-ttu-id="15968-113">Можно использовать для вывода списка доступных каунтерсетс, вывода списка доступных счетчиков, вывода данных счетчиков на консоль или получения данных счетчиков в файл журнала (CSV, TDF, BLG).</span><span class="sxs-lookup"><span data-stu-id="15968-113">Can be used to list available countersets, list available counters, print counter data to the console, or collect counter data to a log file (CSV, TDF, BLG).</span></span>
| [<span data-ttu-id="15968-114">Relog</span><span class="sxs-lookup"><span data-stu-id="15968-114">Relog</span></span>](/windows-server/administration/windows-commands/relog) |<span data-ttu-id="15968-115">Программа командной строки для преобразования и слияния файлов журналов (CSV, TDF, BLG), захваченных через `typeperf.exe` или через API- `PDH.dll` интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="15968-115">Command-line tool for transforming and merging log files (CSV, TDF, BLG) captured via `typeperf.exe` or via the `PDH.dll` APIs.</span></span>
| [<span data-ttu-id="15968-116">LogMan</span><span class="sxs-lookup"><span data-stu-id="15968-116">LogMan</span></span>](/windows-server/administration/windows-commands/logman) |<span data-ttu-id="15968-117">Программа командной строки для управления наборами сборщиков данных.</span><span class="sxs-lookup"><span data-stu-id="15968-117">Command-line tool for controlling Data Collector Sets.</span></span>

## <a name="data-provider-tools"></a><span data-ttu-id="15968-118">Средства поставщика данных</span><span class="sxs-lookup"><span data-stu-id="15968-118">Data provider tools</span></span>

<span data-ttu-id="15968-119">Следующие средства полезны при публикации данных счетчика производительности Windows.</span><span class="sxs-lookup"><span data-stu-id="15968-119">The following tools are useful when publishing Windows Performance Counter data.</span></span>

|<span data-ttu-id="15968-120">Средство</span><span class="sxs-lookup"><span data-stu-id="15968-120">Tool</span></span>|<span data-ttu-id="15968-121">Описание</span><span class="sxs-lookup"><span data-stu-id="15968-121">Description</span></span>
|----|-----------
| [<span data-ttu-id="15968-122">ктрпп</span><span class="sxs-lookup"><span data-stu-id="15968-122">CtrPP</span></span>](ctrpp.md) | <span data-ttu-id="15968-123">Средство сборки командной строки из Windows SDK, которое проверяет и компилирует манифест поставщика v2 счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="15968-123">Command-line build tool from the Windows SDK that validates and compiles your Performance Counters V2 provider manifest.</span></span> <span data-ttu-id="15968-124">Это средство создает `.h` заголовки и `.rc` сценарии ресурсов, необходимые для создания поставщика v2.</span><span class="sxs-lookup"><span data-stu-id="15968-124">This tool generates the `.h` headers and `.rc` resource scripts needed to build a V2 provider.</span></span>
| [<span data-ttu-id="15968-125">LodCtr</span><span class="sxs-lookup"><span data-stu-id="15968-125">LodCtr</span></span>](/windows-server/administration/windows-commands/lodctr) | <span data-ttu-id="15968-126">Программа командной строки, используемая для установки поставщика в системе.</span><span class="sxs-lookup"><span data-stu-id="15968-126">Command-line tool used to install your provider onto a system.</span></span>
| [<span data-ttu-id="15968-127">Lodctr</span><span class="sxs-lookup"><span data-stu-id="15968-127">UnlodCtr</span></span>](/windows-server/administration/windows-commands/unlodctr_1) | <span data-ttu-id="15968-128">Программа командной строки, используемая для удаления поставщика из системы.</span><span class="sxs-lookup"><span data-stu-id="15968-128">Command-line tool used to uninstall your provider from a system.</span></span>
