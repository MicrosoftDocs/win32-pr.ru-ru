---
title: Фильтрация с отслеживанием состояния ALE
description: Фильтры, установленные на уровнях применения уровня приложения (ALE) платформы фильтрации Windows (WFP), выполняют фильтрацию сети с отслеживанием состояния.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104070001"
---
# <a name="ale-stateful-filtering"></a><span data-ttu-id="73be1-103">Фильтрация с отслеживанием состояния ALE</span><span class="sxs-lookup"><span data-stu-id="73be1-103">ALE Stateful Filtering</span></span>

<span data-ttu-id="73be1-104">Фильтры, установленные на уровнях применения уровня приложения (ALE) платформы фильтрации Windows (WFP), выполняют фильтрацию сети с отслеживанием состояния.</span><span class="sxs-lookup"><span data-stu-id="73be1-104">Filters installed at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) perform stateful network filtering.</span></span> <span data-ttu-id="73be1-105">В качестве базиса для фильтрации с отслеживанием состояния ALE используется *поток ALE* .</span><span class="sxs-lookup"><span data-stu-id="73be1-105">An *ALE flow* is used as the basis for ALE stateful filtering.</span></span>

<span data-ttu-id="73be1-106">Поток ALE — это способ классификации сетевого трафика путем его группирования на основе IP-адреса источника, IP-адреса назначения, исходного порта, порта назначения и протокола.</span><span class="sxs-lookup"><span data-stu-id="73be1-106">An ALE flow is a way of classifying network traffic by grouping it based on a Source IP Address, a Destination IP Address, a Source Port, a Destination Port, and a Protocol.</span></span> <span data-ttu-id="73be1-107">Поток ALE может быть универсальным, то есть один или несколько дескрипторов могут сопоставлять все (или подстановочные знаки \* ).</span><span class="sxs-lookup"><span data-stu-id="73be1-107">An ALE flow could be generic, that is one or more of the descriptors could be matching everything (or wildcard \*).</span></span> <span data-ttu-id="73be1-108">Например, универсальный поток ALE UDP будет описываться как исходный IP-адрес = \* , конечный IP-адрес = \* , исходный порт = \* , порт назначения = \* и протокол UDP.</span><span class="sxs-lookup"><span data-stu-id="73be1-108">For example, a generic UDP ALE flow would be described as Source IP Address = \*, Destination IP Address = \*, Source Port = \*, Destination Port = \*, and Protocol = UDP.</span></span>

<span data-ttu-id="73be1-109">После авторизации подключения (входящие подключения разрешаются на уровне [**\_ \_ проверки подлинности на уровне фвпм уровня \_ \_ \_ \_ {4 \| 6}**](management-filtering-layer-identifiers-.md) и исходящих подключений на уровне **\_ \_ \_ проверки подлинности ALE версии \_ \_ {4 \| 6} уровня фвпм** ) создается поток Ale, что позволяет автоматически разрешать изменение политики, все пакеты, входящие и исходящие, которые принадлежат одному потоку Ale.</span><span class="sxs-lookup"><span data-stu-id="73be1-109">Once a connection is authorized (inbound connections are authorized at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and outbound connections at the **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layer), an ALE flow is created such that, barring a policy change, all packets, inbound and outbound, that belong to the same ALE flow are permitted automatically.</span></span> <span data-ttu-id="73be1-110">Так как изменение политики может потребовать блокирования ранее разрешенных подключений, потоки ALE [должны быть переработаны при изменении политики](ale-re-authorization.md) .</span><span class="sxs-lookup"><span data-stu-id="73be1-110">Because a policy change might require blocking previously allowed connections, ALE flows need to be [reauthorized](ale-re-authorization.md) when a policy change occurs.</span></span>

<span data-ttu-id="73be1-111">Фильтрация с отслеживанием состояния ALE значительно сокращает количество необходимых классификаций, классификация только первого пакета, принадлежащего потоку ALE.</span><span class="sxs-lookup"><span data-stu-id="73be1-111">ALE stateful filtering reduces drastically the number of required classifications by classifying only the first packet that belongs to an ALE flow.</span></span> <span data-ttu-id="73be1-112">При сравнении Фильтрация без отслеживания состояния требует классификации каждого пакета, который проходит по сети.</span><span class="sxs-lookup"><span data-stu-id="73be1-112">By comparison, non-stateful filtering requires classification of every packet that traverse the network.</span></span>

<span data-ttu-id="73be1-113">Поток ALE имеет связанное направление, которое является направлением первого пакета потока.</span><span class="sxs-lookup"><span data-stu-id="73be1-113">An ALE flow has an associated direction, which is the direction of the first packet of the flow.</span></span> <span data-ttu-id="73be1-114">Это позволяет более гибким политикам, разрешая входящим подключениям, имеющим различные политики от исходящих инициированных подключений.</span><span class="sxs-lookup"><span data-stu-id="73be1-114">This allows for more flexible policies, by permitting inbound initiated connections to have different policies from outbound initiated connections.</span></span>

## <a name="tcp-ale-flow"></a><span data-ttu-id="73be1-115">Поток ALE TCP</span><span class="sxs-lookup"><span data-stu-id="73be1-115">TCP ALE Flow</span></span>

<span data-ttu-id="73be1-116">Поток ALE для трафика TCP определяется пятью кортежами TCP/IP (исходный IP-адрес, IP-адрес назначения, исходный порт, порт назначения и протокол).</span><span class="sxs-lookup"><span data-stu-id="73be1-116">An ALE flow for TCP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="73be1-117">Поток ALE TCP имеет такое же время существования, как и подключенный TCP-сокет.</span><span class="sxs-lookup"><span data-stu-id="73be1-117">A TCP ALE flow has the same lifetime as a connected TCP socket.</span></span> <span data-ttu-id="73be1-118">Подключенный TCP-сокет может быть либо сокетом, созданным с помощью [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) , либо сокетом, созданным в результате вызова [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) .</span><span class="sxs-lookup"><span data-stu-id="73be1-118">A connected TCP socket could be either a socket created using [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) or a socket created as a result of an [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) call.</span></span>

<span data-ttu-id="73be1-119">ALE поддерживает связь "один к одному" между потоком TCP ALE и управляющим блоком TCP (TCB).</span><span class="sxs-lookup"><span data-stu-id="73be1-119">ALE maintains a one-to-one relationship between a TCP ALE flow and a TCP Control Block (TCB).</span></span>

## <a name="udp-ale-flow"></a><span data-ttu-id="73be1-120">Поток ALE UDP</span><span class="sxs-lookup"><span data-stu-id="73be1-120">UDP ALE Flow</span></span>

> [!Note]  
> <span data-ttu-id="73be1-121">Протоколы, не являющиеся TCP или ICMP, обрабатываются как UDP.</span><span class="sxs-lookup"><span data-stu-id="73be1-121">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="73be1-122">Поток ALE для UDP-трафика определяется пятью кортежами TCP/IP (исходный IP-адрес, IP-адрес назначения, исходный порт, порт назначения и протокол).</span><span class="sxs-lookup"><span data-stu-id="73be1-122">An ALE flow for UDP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="73be1-123">Поток ALE UDP создается на основе сокета UDP и представляет удаленный одноранговый узел, с которым взаимодействует приложение.</span><span class="sxs-lookup"><span data-stu-id="73be1-123">A UDP ALE flow is created based on a UDP socket and it represents the remote peer that the application is communicating with.</span></span> <span data-ttu-id="73be1-124">Удаленный узел определяется кортежем (IP-адрес назначения и порт назначения).</span><span class="sxs-lookup"><span data-stu-id="73be1-124">A remote peer is identified by a (Destination IP Address and Destination Port) tuple.</span></span>

<span data-ttu-id="73be1-125">Между сокетом UDP и удаленными одноранговыми узлами, к которым он обращается, существует связь «один ко многим».</span><span class="sxs-lookup"><span data-stu-id="73be1-125">There is a one-to-many relationship between a UDP socket and the remote peers that it talks to.</span></span>

<span data-ttu-id="73be1-126">При закрытии локального UDP-сокета все связанные с ним потоки ALE будут удалены.</span><span class="sxs-lookup"><span data-stu-id="73be1-126">When the local UDP socket is closed, all the ALE flows associated with it will be deleted.</span></span>

<span data-ttu-id="73be1-127">При отсутствии замыканий сокетов одноадресные потоки ALE UDP имеют [настраиваемое](ale-flow-customization.md) время ожидания простоя, которое по умолчанию составляет 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="73be1-127">In the absence of socket closures, UDP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="73be1-128">Если в этом окне не отправляются или не принимаются пакеты, поток ALE будет удален.</span><span class="sxs-lookup"><span data-stu-id="73be1-128">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="73be1-129">Это время ожидания по умолчанию постепенно сокращается, когда количество потоков ALE уровня системы достигает определенного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="73be1-129">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

## <a name="icmp-ale-flow"></a><span data-ttu-id="73be1-130">Поток ALE ICMP</span><span class="sxs-lookup"><span data-stu-id="73be1-130">ICMP ALE Flow</span></span>

<span data-ttu-id="73be1-131">Поток ALE для ICMP-трафика определяется шестью кортежами (исходным IP-адресом, IP-адресом назначения, типом ICMP, кодом ICMP, протоколом и ИДЕНТИФИКАТОРом ICMP).</span><span class="sxs-lookup"><span data-stu-id="73be1-131">An ALE flow for ICMP traffic is identified by the six-tuple (Source IP Address, Destination IP Address, ICMP type, ICMP code, Protocol, and ICMP ID).</span></span> <span data-ttu-id="73be1-132">Идентификатор ICMP является частью потока ALE только для трафика эхо/Reply ICMP.</span><span class="sxs-lookup"><span data-stu-id="73be1-132">The ICMP ID is part of the ALE flow only for ICMP echo/reply traffic.</span></span>

<span data-ttu-id="73be1-133">В случае отсутствия замыканий сокета потоки одноадресных ALE ICMP имеют [настраиваемое](ale-flow-customization.md) время ожидания простоя, которое по умолчанию составляет 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="73be1-133">In the absence of socket closures, ICMP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="73be1-134">Если в этом окне не отправляются или не принимаются пакеты, поток ALE будет удален.</span><span class="sxs-lookup"><span data-stu-id="73be1-134">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="73be1-135">Это время ожидания по умолчанию постепенно сокращается, когда количество потоков ALE уровня системы достигает определенного порогового значения.</span><span class="sxs-lookup"><span data-stu-id="73be1-135">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

<span data-ttu-id="73be1-136">На уровни ALE выводятся только сообщения ICMP без ошибок.</span><span class="sxs-lookup"><span data-stu-id="73be1-136">Only ICMP non-error messages are indicated to ALE layers.</span></span> <span data-ttu-id="73be1-137">Сообщения об ошибках ICMP можно проверить на \_ уровнях ошибок ICMP.</span><span class="sxs-lookup"><span data-stu-id="73be1-137">ICMP error messages can be inspected at ICMP\_ERROR layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73be1-138">См. также</span><span class="sxs-lookup"><span data-stu-id="73be1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73be1-139">Принудительное применение уровня приложения (ALE)</span><span class="sxs-lookup"><span data-stu-id="73be1-139">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="73be1-140">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="73be1-140">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="73be1-141">Многоадресный или широковещательный трафик ALE</span><span class="sxs-lookup"><span data-stu-id="73be1-141">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="73be1-142">Повторная авторизация ALE</span><span class="sxs-lookup"><span data-stu-id="73be1-142">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="73be1-143">Настройка потока ALE</span><span class="sxs-lookup"><span data-stu-id="73be1-143">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="73be1-144">Потоки TCP-пакетов</span><span class="sxs-lookup"><span data-stu-id="73be1-144">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="73be1-145">Потоки UDP-пакетов</span><span class="sxs-lookup"><span data-stu-id="73be1-145">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="73be1-146">Функции Winsock</span><span class="sxs-lookup"><span data-stu-id="73be1-146">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 