---
description: Метрики используются для измерения аспектов производительности сети и протокола.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Терминология сети (сокеты Windows 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809713"
---
# <a name="network-terminology-windows-sockets-2"></a><span data-ttu-id="3dd67-103">Терминология сети (сокеты Windows 2)</span><span class="sxs-lookup"><span data-stu-id="3dd67-103">Network Terminology (Windows Sockets 2)</span></span>

<span data-ttu-id="3dd67-104">Метрики используются для измерения аспектов производительности сети и протокола.</span><span class="sxs-lookup"><span data-stu-id="3dd67-104">Metrics are used to measure aspects of network and protocol performance.</span></span> <span data-ttu-id="3dd67-105">Значения для таких метрик в различных сценариях указывают на уровень производительности сетевого приложения.</span><span class="sxs-lookup"><span data-stu-id="3dd67-105">The values for such metrics in various scenarios indicate the level of performance of a network application.</span></span> <span data-ttu-id="3dd67-106">В этом разделе определяются термины и метрики, используемые во всей отрасли для измерения производительности сетевых приложений.</span><span class="sxs-lookup"><span data-stu-id="3dd67-106">This section defines terms and metrics used industry-wide for measuring network application performance.</span></span> <span data-ttu-id="3dd67-107">Эти термины используются в оставшейся части этого руководств.</span><span class="sxs-lookup"><span data-stu-id="3dd67-107">These terms are used throughout the rest of this guide.</span></span>

-   <span data-ttu-id="3dd67-108">Время кругового пути (RTT)</span><span class="sxs-lookup"><span data-stu-id="3dd67-108">Round Trip Time (RTT)</span></span>

    <span data-ttu-id="3dd67-109">Время (в миллисекундах), в течение которого запрос на перепоездку с исходного компьютера на конечный компьютер и обратно.</span><span class="sxs-lookup"><span data-stu-id="3dd67-109">Time, in milliseconds, for a request to make a trip from a source computer to a destination computer, and back again.</span></span> <span data-ttu-id="3dd67-110">Более низкие значения указывают на более высокую производительность.</span><span class="sxs-lookup"><span data-stu-id="3dd67-110">Lower values indicate better performance.</span></span> <span data-ttu-id="3dd67-111">Значения времени пути пересылки и возврата не обязательно равны.</span><span class="sxs-lookup"><span data-stu-id="3dd67-111">Forward and return path times are not necessarily equal.</span></span>

    <span data-ttu-id="3dd67-112">На значения RTT влияют сетевая инфраструктура, расстояние между узлами, сетевые условия и размер пакета.</span><span class="sxs-lookup"><span data-stu-id="3dd67-112">RTT values are affected by network infrastructure, distance between nodes, network conditions, and packet size.</span></span> <span data-ttu-id="3dd67-113">Размер пакета, перегрузка и полезные данные сжимаемости влияют на время приема-передачи, измеряемое в медленных каналах, таких как коммутируемые подключения.</span><span class="sxs-lookup"><span data-stu-id="3dd67-113">Packet size, congestion and payload compressibility impact RTT when measured on slow links, such as dial-up connections.</span></span> <span data-ttu-id="3dd67-114">Другие факторы влияют на RTT, включая исправление ошибок переадресации и сжатие данных, что приводит к появлению буферов и очередей, которые увеличивают время приема на работу и, следовательно, снижают производительность.</span><span class="sxs-lookup"><span data-stu-id="3dd67-114">Other factors affect RTT, including forward error correction and data compression, which introduce buffers and queues that increase RTT, and therefore decrease performance.</span></span>

-   <span data-ttu-id="3dd67-115">гудпут</span><span class="sxs-lookup"><span data-stu-id="3dd67-115">Goodput</span></span>

    <span data-ttu-id="3dd67-116">Мера полезных данных приложений, успешно обрабатываемых получателем, в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="3dd67-116">Measure of useful application data successfully processed by the receiver, in bits-per-second.</span></span> <span data-ttu-id="3dd67-117">Гудпут включает измерение эффективной или полезной пропускной способности и включает только данные приложения. заголовки пакетов, протоколов и носителей рассматриваются как издержки и не являются частью гудпут.</span><span class="sxs-lookup"><span data-stu-id="3dd67-117">Goodput enables the measurement of effective or useful throughput and includes only application data; packet, protocol, and media headers are considered overhead, and are not part of goodput.</span></span>

-   <span data-ttu-id="3dd67-118">Издержки протокола</span><span class="sxs-lookup"><span data-stu-id="3dd67-118">Protocol Overhead</span></span>

    <span data-ttu-id="3dd67-119">Неприложения (байты), в том числе протокол и мультимедийные данные, разделенные на общее число переданных байтов.</span><span class="sxs-lookup"><span data-stu-id="3dd67-119">Nonapplication bytes, including protocol and media framing, divided by the total number of bytes transmitted.</span></span> <span data-ttu-id="3dd67-120">Значение выражается в процентах.</span><span class="sxs-lookup"><span data-stu-id="3dd67-120">The value is expressed as a percentage.</span></span> <span data-ttu-id="3dd67-121">Более высокие значения указывают на низкую производительность.</span><span class="sxs-lookup"><span data-stu-id="3dd67-121">Higher values indicate poorer performance.</span></span>

    <span data-ttu-id="3dd67-122">Накладные расходы рассчитываются для обоих направлений в этом пошаговом руководству, но могут рассчитываться отдельно для каждого направления.</span><span class="sxs-lookup"><span data-stu-id="3dd67-122">Overhead is calculated for both directions in this guide, but can be calculated for each direction separately.</span></span>

-   <span data-ttu-id="3dd67-123">Bandwidth-Delay продукт</span><span class="sxs-lookup"><span data-stu-id="3dd67-123">Bandwidth-Delay Product</span></span>

    <span data-ttu-id="3dd67-124">Объем пропускной способности сети в секунду и время приема-передачи (в секундах).</span><span class="sxs-lookup"><span data-stu-id="3dd67-124">Product of the bits-per-second bandwidth of the network, and the RTT (in seconds).</span></span> <span data-ttu-id="3dd67-125">Это значение соответствует количеству битов, требуемых для заполнения доступной пропускной способности сети.</span><span class="sxs-lookup"><span data-stu-id="3dd67-125">This value equates to the number of bits it takes to fill available network bandwidth.</span></span> <span data-ttu-id="3dd67-126">Если значение для продукта задержки пропускной способности велико, стек TCP/IP должен работать с большими объемами неподтвержденных данных, чтобы обеспечить заполнение конвейера.</span><span class="sxs-lookup"><span data-stu-id="3dd67-126">When the value for bandwidth-delay product is high, the TCP/IP stack must handle large amounts of unacknowledged data in order to keep the pipeline full.</span></span> <span data-ttu-id="3dd67-127">«Пропускная способность-задержка» — это основная комплексная метрика для потоковой передачи приложений.</span><span class="sxs-lookup"><span data-stu-id="3dd67-127">Bandwidth-delay product is a key end-to-end metric for streaming applications.</span></span>

 

 



