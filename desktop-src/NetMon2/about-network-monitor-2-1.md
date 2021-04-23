---
description: Сетевой монитор является компонентом Microsoft Systems Management Server (SMS), который используется для обнаружения и устранения неполадок в локальных сетях, глобальных сетях и последовательных связях с сервером Microsoft Remote Access Server (RAS).
ms.assetid: bd273439-daa2-4263-8f12-28ec988beea0
title: Сведения о сетевой монитор 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447f4763e0c73dc0dcac4cf719a0bad4b61f073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080756"
---
# <a name="about-network-monitor-21"></a><span data-ttu-id="c23f0-103">Сведения о сетевой монитор 2,1</span><span class="sxs-lookup"><span data-stu-id="c23f0-103">About Network Monitor 2.1</span></span>

<span data-ttu-id="c23f0-104">Сетевой монитор является компонентом Microsoft Systems Management Server (SMS), который используется для обнаружения и устранения неполадок в локальных сетях, глобальных сетях и последовательных связях с сервером Microsoft Remote Access Server (RAS).</span><span class="sxs-lookup"><span data-stu-id="c23f0-104">Network Monitor is a component of Microsoft Systems Management Server (SMS) used to detect and troubleshoot problems on LANs, WANs, and serial links running Microsoft Remote Access Server (RAS).</span></span> <span data-ttu-id="c23f0-105">Сетевой монитор обеспечивает анализ данных по сети после записи.</span><span class="sxs-lookup"><span data-stu-id="c23f0-105">Network Monitor provides post-capture network data analysis.</span></span>

<span data-ttu-id="c23f0-106">В ходе анализа после захвата сетевой трафик сохраняется в собственном файле записи, чтобы захваченные данные можно было проанализировать позже.</span><span class="sxs-lookup"><span data-stu-id="c23f0-106">In post-capture analysis, network traffic is saved in a proprietary capture file, so that the captured data can be analyzed later.</span></span> <span data-ttu-id="c23f0-107">В этом случае анализ может быть указан в форме [*парсеров*](p.md) протоколов, которые выводят определенные типы кадров сети и отображают данные кадра в пользовательском интерфейсе сетевой монитор. или анализ может быть в виде [*экспертов*](e.md) , изучающих сетевые данные и отображая отчет (эксперты также могут управлять сетевыми данными).</span><span class="sxs-lookup"><span data-stu-id="c23f0-107">In this case, analysis can be in the form of protocol [*parsers*](p.md) picking out specific network frame types and displaying the frame data in the Network Monitor UI; or analysis can be in the form of [*experts*](e.md) examining the network data and displaying a report (experts may also manipulate the network data).</span></span>

<span data-ttu-id="c23f0-108">Сетевой монитор предоставляет следующие типы функциональных возможностей:</span><span class="sxs-lookup"><span data-stu-id="c23f0-108">Network Monitor provides the following types of functionality:</span></span>

-   <span data-ttu-id="c23f0-109">Записывает сетевые данные в режиме реального времени или отложенного режима.</span><span class="sxs-lookup"><span data-stu-id="c23f0-109">Captures network data in real-time or delayed mode.</span></span>
-   <span data-ttu-id="c23f0-110">Предоставляет возможности фильтрации при сборе данных.</span><span class="sxs-lookup"><span data-stu-id="c23f0-110">Provides filtering capabilities when capturing data.</span></span>
-   <span data-ttu-id="c23f0-111">Использует экспертов и анализаторы для подробного анализа после записи.</span><span class="sxs-lookup"><span data-stu-id="c23f0-111">Uses experts and parsers for detailed post-capture analysis.</span></span>

<span data-ttu-id="c23f0-112">Дополнительные сведения о сетевой монитор компонентах см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="c23f0-112">For more information about Network Monitor features, see:</span></span>

-   [<span data-ttu-id="c23f0-113">Архитектура эксперта и анализатора</span><span class="sxs-lookup"><span data-stu-id="c23f0-113">Expert and Parser Architecture</span></span>](expert-and-parser-architecture.md)
-   [<span data-ttu-id="c23f0-114">Эксперты</span><span class="sxs-lookup"><span data-stu-id="c23f0-114">Experts</span></span>](experts.md)
-   [<span data-ttu-id="c23f0-115">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="c23f0-115">Parsers</span></span>](parsers.md)
-   [<span data-ttu-id="c23f0-116">Поставщики сетевых пакетов</span><span class="sxs-lookup"><span data-stu-id="c23f0-116">Network Packet Providers</span></span>](network-packet-providers.md)
-   [<span data-ttu-id="c23f0-117">сетевой монитор большие двоичные объекты</span><span class="sxs-lookup"><span data-stu-id="c23f0-117">Network Monitor BLOBs</span></span>](network-monitor-blobs.md)
-   [<span data-ttu-id="c23f0-118">Страница ссылки на событие</span><span class="sxs-lookup"><span data-stu-id="c23f0-118">Event Reference Page</span></span>](event-reference-page.md)
-   [<span data-ttu-id="c23f0-119">Фильтры записи</span><span class="sxs-lookup"><span data-stu-id="c23f0-119">Capture Filters</span></span>](capture-filters.md)

<span data-ttu-id="c23f0-120">**Windows Vista:** На этой платформе не поддерживаются сетевой монитор 2,1 и более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="c23f0-120">**Windows Vista:** Network Monitor 2.1 and earlier are not supported on this platform.</span></span>

 

 



