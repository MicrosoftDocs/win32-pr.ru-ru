---
description: В этом разделе описываются структуры НПП, используемые методами НПП.
ms.assetid: f0729dc5-6b5f-4f24-85d6-47c45f1bf9be
title: Структуры НПП
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b514bded37450f6a7c33a016b231bb38f0c1812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682903"
---
# <a name="npp-structures"></a><span data-ttu-id="13a77-103">Структуры НПП</span><span class="sxs-lookup"><span data-stu-id="13a77-103">NPP Structures</span></span>

<span data-ttu-id="13a77-104">В этом разделе описываются структуры НПП, используемые методами НПП.</span><span class="sxs-lookup"><span data-stu-id="13a77-104">This section describes the NPP structures used by NPP methods.</span></span> <span data-ttu-id="13a77-105">Эти структуры используются для получения статистики, предоставления состояния системы и статистических данных и указания компьютеров, на которых выполняется сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="13a77-105">These structures are used to retrieve statistics, provide system status and statistical information, and indicate which computers are running Network Monitor.</span></span> <span data-ttu-id="13a77-106">Эти структуры описаны в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="13a77-106">The following tables describes these structures.</span></span>



| <span data-ttu-id="13a77-107">Структуры НПП</span><span class="sxs-lookup"><span data-stu-id="13a77-107">NPP Structures</span></span>                     | <span data-ttu-id="13a77-108">Описание</span><span class="sxs-lookup"><span data-stu-id="13a77-108">Description</span></span>                                                                                                                      |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13a77-109">сессионстатс</span><span class="sxs-lookup"><span data-stu-id="13a77-109">SESSIONSTATS</span></span>](sessionstats.md)   | <span data-ttu-id="13a77-110">Предоставляет сведения о сеансе при извлечении статистики диалога.</span><span class="sxs-lookup"><span data-stu-id="13a77-110">Provides session information when conversation statistics are retrieved.</span></span>                                                         |
| [<span data-ttu-id="13a77-111">статионстатс</span><span class="sxs-lookup"><span data-stu-id="13a77-111">STATIONSTATS</span></span>](stationstats.md)   | <span data-ttu-id="13a77-112">Предоставляет статистику о конкретной [*станции*](s.md).</span><span class="sxs-lookup"><span data-stu-id="13a77-112">Provides statistics about a specific [*station*](s.md).</span></span>                                                     |
| [<span data-ttu-id="13a77-113">STATISTICS</span><span class="sxs-lookup"><span data-stu-id="13a77-113">STATISTICS</span></span>](statistics.md)       | <span data-ttu-id="13a77-114">Предоставляет статистику сети при получении всей статистики и о том, что текущая запись приостановлена или остановлена.</span><span class="sxs-lookup"><span data-stu-id="13a77-114">Provides network statistics when total statistics are retrieved and when the current capture has paused or stopped.</span></span>              |
| [<span data-ttu-id="13a77-115">куеритабле</span><span class="sxs-lookup"><span data-stu-id="13a77-115">QUERYTABLE</span></span>](querytable.md)       | <span data-ttu-id="13a77-116">Указывает, какие компьютеры используют сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="13a77-116">Indicates which computers are using Network Monitor.</span></span>                                                                             |
| [<span data-ttu-id="13a77-117">статионкуери</span><span class="sxs-lookup"><span data-stu-id="13a77-117">STATIONQUERY</span></span>](stationquery.md)   | <span data-ttu-id="13a77-118">Предоставляет сведения о компьютере, использующем сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="13a77-118">Provides information about a computer that is using Network Monitor.</span></span> <span data-ttu-id="13a77-119">Эта структура используется структурой **КУЕРИТАБЛЕ** НПП.</span><span class="sxs-lookup"><span data-stu-id="13a77-119">This structure is used by the NPP **QUERYTABLE** structure.</span></span> |
| [<span data-ttu-id="13a77-120">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="13a77-120">NETWORKSTATUS</span></span>](networkstatus.md) | <span data-ttu-id="13a77-121">Предоставляет текущее состояние сети с точки зрения состояния системы.</span><span class="sxs-lookup"><span data-stu-id="13a77-121">Provides current network status in terms of system state.</span></span>                                                                        |



 

 

 



