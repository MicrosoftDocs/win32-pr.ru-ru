---
description: Проблемы размера пакетов носителей, обсуждаемые в разделе о размере пакета носителей, по-разному влияют на различные \_ протоколы IPX PF.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Влияние размера пакета на протоколы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343505"
---
# <a name="how-packet-size-affects-protocols"></a><span data-ttu-id="57fc0-103">Влияние размера пакета на протоколы</span><span class="sxs-lookup"><span data-stu-id="57fc0-103">How Packet Size Affects Protocols</span></span>

<span data-ttu-id="57fc0-104">Проблемы размера пакетов носителей, обсуждаемые в разделе [о размере пакета носителей](about-media-packet-size-2.md), по-разному влияют на различные \_ протоколы IPX PF.</span><span class="sxs-lookup"><span data-stu-id="57fc0-104">Media packet size issues discussed in the topic, [About Media Packet Size](about-media-packet-size-2.md), affect the various PF\_IPX protocols differently.</span></span> <span data-ttu-id="57fc0-105">Распространенной стратегией для обработки различных ограничений на размеры маршрутизатора и носителя является использование полного размера носителя, если номер сети удаленной станции соответствует локальной станции и в противном случае возвращается к минимальному размеру пакета.</span><span class="sxs-lookup"><span data-stu-id="57fc0-105">A common strategy for handling various router and media size constraints is to use the full media size when the remote station's network number matches the local station, and fall back to the minimum packet size otherwise.</span></span>

## <a name="parameters"></a><span data-ttu-id="57fc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57fc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57fc0-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>НСПРОТО \_ IPX</span><span class="sxs-lookup"><span data-stu-id="57fc0-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO\_IPX</span></span>
</dt> <dd>

<span data-ttu-id="57fc0-108">Предоставляет службу датаграммы; Каждая датаграмма должна находиться в пределах максимального размера пакета.</span><span class="sxs-lookup"><span data-stu-id="57fc0-108">Provides a datagram service; each datagram must reside within the maximum packet size.</span></span> <span data-ttu-id="57fc0-109">Winsock устанавливает максимальный размер пакета датаграммы на локальный размер пакета носителей минус заголовок IPX.</span><span class="sxs-lookup"><span data-stu-id="57fc0-109">Winsock sets the maximum datagram packet size to the local media packet size minus the IPX header.</span></span> <span data-ttu-id="57fc0-110">Однако помните, что если пакет направляется, он может попасть в ограничения маршрутизатора En Route.</span><span class="sxs-lookup"><span data-stu-id="57fc0-110">Keep in mind, however, that if the packet is routed, it may hit router restrictions en route.</span></span> <span data-ttu-id="57fc0-111">Убедитесь, что приложение может переноситься обратно в 546-байтовые датаграммы.</span><span class="sxs-lookup"><span data-stu-id="57fc0-111">Make sure your application can fall back to 546-byte datagrams.</span></span>

</dd> <dt>

<span data-ttu-id="57fc0-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>НСПРОТО \_ SPX</span><span class="sxs-lookup"><span data-stu-id="57fc0-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO\_SPX</span></span>
</dt> <dd>

<span data-ttu-id="57fc0-113">Предоставляет службы потоков и виртуализированных пакетов.</span><span class="sxs-lookup"><span data-stu-id="57fc0-113">Provides stream and sequenced-packet services.</span></span> <span data-ttu-id="57fc0-114">Winsock IPX/SPX позволяет потокам данных и сообщениям охватывать несколько пакетов, поэтому размер пакета не ограничивает объем данных, обрабатываемых функцией [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) и [**recv**](/windows/desktop/api/winsock/nf-winsock-recv).</span><span class="sxs-lookup"><span data-stu-id="57fc0-114">Winsock IPX/SPX lets data streams and messages span multiple packets, so packet size does not limit the amount of data handled by [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv).</span></span> <span data-ttu-id="57fc0-115">Однако базовый размер носителя должен быть задан правильно, либо первый большой пакет будет недоступен и подключение будет сброшено.</span><span class="sxs-lookup"><span data-stu-id="57fc0-115">However, the underlying media size must be set correctly or the first large packet will be undeliverable and the connection will reset.</span></span> <span data-ttu-id="57fc0-116">Если целевая станция находится в локальной сети, Winsock устанавливает размер пакета в виде пакета носителей.</span><span class="sxs-lookup"><span data-stu-id="57fc0-116">If the target station is on the local network, Winsock sets its packet size to the media packet size.</span></span> <span data-ttu-id="57fc0-117">В противном случае по умолчанию используется значение 512 байт.</span><span class="sxs-lookup"><span data-stu-id="57fc0-117">Otherwise, it defaults to 512 bytes.</span></span> <span data-ttu-id="57fc0-118">Этот размер можно изменить сразу после [**подключения**](/windows/desktop/api/Winsock2/nf-winsock2-connect) или [**приема**](/windows/desktop/api/Winsock2/nf-winsock2-accept) через [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span><span class="sxs-lookup"><span data-stu-id="57fc0-118">This size can be changed immediately after [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) or [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) through [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span>

</dd> <dt>

<span data-ttu-id="57fc0-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>НСПРОТО \_ спксии</span><span class="sxs-lookup"><span data-stu-id="57fc0-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO\_SPXII</span></span>
</dt> <dd>

<span data-ttu-id="57fc0-120">СПКСИИ использует большое согласование пакетов Интернета для поддержания оптимального размера пакетов и не требует вмешательства программиста.</span><span class="sxs-lookup"><span data-stu-id="57fc0-120">SPXII features large Internet packet negotiation to maintain a best-fit size for packets and does not require programmer intervention.</span></span> <span data-ttu-id="57fc0-121">Однако если удаленная станция не поддерживает СПКСИИ и не выполняет согласование до стандарта SPX, действуют \_ правила SPX нспрото.</span><span class="sxs-lookup"><span data-stu-id="57fc0-121">However, if the remote station does not support SPXII and negotiates down to standard SPX, the NSPROTO\_SPX rules are in effect.</span></span>



| <span data-ttu-id="57fc0-122">Протокол</span><span class="sxs-lookup"><span data-stu-id="57fc0-122">Protocol</span></span>     | <span data-ttu-id="57fc0-123">Мультимедиа</span><span class="sxs-lookup"><span data-stu-id="57fc0-123">Media</span></span>      | <span data-ttu-id="57fc0-124">Тип</span><span class="sxs-lookup"><span data-stu-id="57fc0-124">Type</span></span>        | <span data-ttu-id="57fc0-125">Размер пакета данных</span><span class="sxs-lookup"><span data-stu-id="57fc0-125">Data packet size</span></span> |
|--------------|------------|-------------|------------------|
| <span data-ttu-id="57fc0-126">НСПРОТО \_ IPX</span><span class="sxs-lookup"><span data-stu-id="57fc0-126">NSPROTO\_IPX</span></span> | <span data-ttu-id="57fc0-127">Ethernet</span><span class="sxs-lookup"><span data-stu-id="57fc0-127">Ethernet</span></span>   | <span data-ttu-id="57fc0-128">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="57fc0-128">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="57fc0-129">802.3</span><span class="sxs-lookup"><span data-stu-id="57fc0-129">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="57fc0-130">802.2</span><span class="sxs-lookup"><span data-stu-id="57fc0-130">802.2</span></span>       | <span data-ttu-id="57fc0-131">1466</span><span class="sxs-lookup"><span data-stu-id="57fc0-131">1466</span></span>             |
|              |            | <span data-ttu-id="57fc0-132">ВЯЗАТЬ</span><span class="sxs-lookup"><span data-stu-id="57fc0-132">SNAP</span></span>        |                  |
|              | <span data-ttu-id="57fc0-133">Token Ring</span><span class="sxs-lookup"><span data-stu-id="57fc0-133">Token Ring</span></span> | <span data-ttu-id="57fc0-134">4 Мбит</span><span class="sxs-lookup"><span data-stu-id="57fc0-134">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="57fc0-135">16 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="57fc0-135">16 megabit</span></span>  |                  |
| <span data-ttu-id="57fc0-136">НСПРОТО \_ SPX</span><span class="sxs-lookup"><span data-stu-id="57fc0-136">NSPROTO\_SPX</span></span> | <span data-ttu-id="57fc0-137">Ethernet</span><span class="sxs-lookup"><span data-stu-id="57fc0-137">Ethernet</span></span>   | <span data-ttu-id="57fc0-138">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="57fc0-138">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="57fc0-139">802.3</span><span class="sxs-lookup"><span data-stu-id="57fc0-139">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="57fc0-140">802.2</span><span class="sxs-lookup"><span data-stu-id="57fc0-140">802.2</span></span>       | <span data-ttu-id="57fc0-141">1454</span><span class="sxs-lookup"><span data-stu-id="57fc0-141">1454</span></span>             |
|              |            | <span data-ttu-id="57fc0-142">ВЯЗАТЬ</span><span class="sxs-lookup"><span data-stu-id="57fc0-142">SNAP</span></span>        |                  |
|              | <span data-ttu-id="57fc0-143">Token Ring</span><span class="sxs-lookup"><span data-stu-id="57fc0-143">Token Ring</span></span> | <span data-ttu-id="57fc0-144">4 Мбит</span><span class="sxs-lookup"><span data-stu-id="57fc0-144">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="57fc0-145">16 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="57fc0-145">16 megabit</span></span>  |                  |



 

</dd> </dl>

 

 



