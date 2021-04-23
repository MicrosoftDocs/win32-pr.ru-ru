---
title: Уровни ALE
description: Принудительное применение уровня приложения (ALE) состоит из нескольких уровней фильтрации и многих соответствующих слоев отклонения.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336924"
---
# <a name="ale-layers"></a><span data-ttu-id="d3004-103">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="d3004-103">ALE Layers</span></span>

<span data-ttu-id="d3004-104">Принудительное применение уровня приложения (ALE) состоит из нескольких уровней фильтрации и многих соответствующих слоев отклонения.</span><span class="sxs-lookup"><span data-stu-id="d3004-104">The Application Layer Enforcement (ALE) consists of several filtering layers and many matching discard layers.</span></span> <span data-ttu-id="d3004-105">Все уровни механизма фильтрации Windows Filtering Platform (WFP), включая ALE, описаны в разделе [**Фильтрация идентификаторов слоев**](management-filtering-layer-identifiers-.md).</span><span class="sxs-lookup"><span data-stu-id="d3004-105">All the Windows Filtering Platform (WFP) filtering engine layers, including ALE, are described in [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md).</span></span> <span data-ttu-id="d3004-106">Этот раздел содержит более подробное описание слоев фильтрации, которые являются частью ALE.</span><span class="sxs-lookup"><span data-stu-id="d3004-106">This topic contains a more detailed description of the filtering layers that are part of ALE.</span></span>

## <a name="resource_assignment"></a><span data-ttu-id="d3004-107">\_Назначение ресурсов</span><span class="sxs-lookup"><span data-stu-id="d3004-107">RESOURCE\_ASSIGNMENT</span></span>

<span data-ttu-id="d3004-108">Фильтр на уровне [**\_ \_ \_ назначения ресурсов ALE \_ \_ V {4 \| 6 для слоя фвпм**](management-filtering-layer-identifiers-.md) соответствует операциям сетевой привязки, явному или неявному.</span><span class="sxs-lookup"><span data-stu-id="d3004-108">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for network bind operations, explicit or implicit.</span></span>

<span data-ttu-id="d3004-109">Если фильтр на этом уровне совпадает с разрешающим созданием необработанного сокета, [**флаг условия FWP будет иметь значение \_ \_ \_ \_ необработанный флаг \_ конечной точки**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="d3004-109">If a filter at this layer is matched to authorize raw socket creation, the [**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**](filtering-condition-flags-.md) flag will be set.</span></span>

<span data-ttu-id="d3004-110">Если фильтр на этом уровне соответствует запросу на получение неизбирательного режима, в поле [**\_ \_ \_ неизбирательного \_ режима FWP условия**](filtering-condition-identifiers-.md) будет установлено значение SIO \_ рквалл.</span><span class="sxs-lookup"><span data-stu-id="d3004-110">If a filter at this layer is matched to authorize promiscuous mode receiving, the [**FWP\_CONDITION\_ALE\_PROMISCUOUS\_MODE**](filtering-condition-identifiers-.md) field will be set to SIO\_RCVALL.</span></span> <span data-ttu-id="d3004-111">Описание \_ РКВАЛЛ SIO см. в разделе [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span><span class="sxs-lookup"><span data-stu-id="d3004-111">For a description of SIO\_RCVALL, see [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span></span>

> [!Note]  
> <span data-ttu-id="d3004-112">Это единственный слой, в котором можно фильтровать неизбирательный режим.</span><span class="sxs-lookup"><span data-stu-id="d3004-112">This is the only layer where promiscuous mode can be filtered.</span></span>

 

<span data-ttu-id="d3004-113">Если во время **привязки ()** порт не указан, то есть для параметра Port задано значение 0 (ноль), то стек TCP/IP выберет порт из диапазона динамических портов (19152 – 65535).</span><span class="sxs-lookup"><span data-stu-id="d3004-113">If no port is specified during **bind()**, that is, port is set to 0 (zero), then the TCP/IP stack will select a port from the dynamic port range (19152–65535).</span></span> <span data-ttu-id="d3004-114">Выбранный порт будет классифицироваться в этом слое вместе с [**\_ флагом условия FWP \_ — флагом \_ \_ \_ привязки с подстановочным знаком**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="d3004-114">The selected port will be classified at this layer along with the [**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**](filtering-condition-flags-.md) flag.</span></span>

<span data-ttu-id="d3004-115">Если локальный адрес не указан в вызове [**BIND ()**](/windows/desktop/api/winsock/nf-winsock-bind) , в поле Локальный адрес устанавливается значение [**FWP \_ Empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="d3004-115">If the local address is not specified in the [**bind()**](/windows/desktop/api/winsock/nf-winsock-bind) call, the local address field is set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span>

## <a name="auth_listen"></a><span data-ttu-id="d3004-116">прослушивание проверки подлинности \_</span><span class="sxs-lookup"><span data-stu-id="d3004-116">AUTH\_LISTEN</span></span>

<span data-ttu-id="d3004-117">Фильтр на уровне [**фвпм \_ \_ \_ проверки подлинности ALE уровня \_ \_ {4 \| 6}**](management-filtering-layer-identifiers-.md) соответствует фильтру для вызовов [**Listen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen) TCP.</span><span class="sxs-lookup"><span data-stu-id="d3004-117">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen) calls.</span></span>

## <a name="auth_recv_accept"></a><span data-ttu-id="d3004-118">АВТОРИЗАЦИя \_ recv \_ Accept</span><span class="sxs-lookup"><span data-stu-id="d3004-118">AUTH\_RECV\_ACCEPT</span></span>

<span data-ttu-id="d3004-119">Фильтр на уровне [**фвпм \_ \_ \_ проверки подлинности \_ recv \_ Accept \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) сопоставлен с вызовами протокола TCP [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) , для первых UDP-пакетов (одноадресной рассылки) из уникального удаленного адреса или кортежа порта, а также для первых входящих сообщений ICMP, не являющихся ошибками (одноадресная рассылка) с уникальным типом ICMP, кодом и идентификатором.</span><span class="sxs-lookup"><span data-stu-id="d3004-119">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) calls, for first UDP packets (unicast) from a unique remote address/port tuple, and for first inbound non-error ICMP messages (unicast) with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="d3004-120">Протоколы, не являющиеся TCP или ICMP, обрабатываются как UDP.</span><span class="sxs-lookup"><span data-stu-id="d3004-120">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="d3004-121">TCP-пакеты, полученные необработанными сокетами, обрабатываются аналогично UDP-трафику.</span><span class="sxs-lookup"><span data-stu-id="d3004-121">TCP packets received by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="d3004-122">То есть фильтруется только первая отправка по протоколу TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-send) и первый протокол TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) через необработанные сокеты.</span><span class="sxs-lookup"><span data-stu-id="d3004-122">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="auth_connect"></a><span data-ttu-id="d3004-123">Проверка подлинности \_ подключения</span><span class="sxs-lookup"><span data-stu-id="d3004-123">AUTH\_CONNECT</span></span>

<span data-ttu-id="d3004-124">Фильтр на уровне [**\_ \_ \_ подключения к проверке подлинности фвпм уровня \_ \_ {4 \| 6}**](management-filtering-layer-identifiers-.md) сопоставляется с вызовами TCP [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) для первых UDP-пакетов, отправленных на уникальный удаленный адрес и кортеж портов, а также для первых исходящих ICMP-сообщений с уникальным типом ICMP, кодом и идентификатором.</span><span class="sxs-lookup"><span data-stu-id="d3004-124">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) calls, for first UDP packets sent to a unique remote address and port tuple, and for first outbound non-error ICMP messages with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="d3004-125">Протоколы, не являющиеся TCP или ICMP, обрабатываются как UDP.</span><span class="sxs-lookup"><span data-stu-id="d3004-125">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="d3004-126">TCP-пакеты, отправляемые необработанными сокетами, обрабатываются аналогично UDP-трафику.</span><span class="sxs-lookup"><span data-stu-id="d3004-126">TCP packets sent by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="d3004-127">То есть фильтруется только первая отправка по протоколу TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-send) и первый протокол TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) через необработанные сокеты.</span><span class="sxs-lookup"><span data-stu-id="d3004-127">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="flow_established"></a><span data-ttu-id="d3004-128">\_установленный поток</span><span class="sxs-lookup"><span data-stu-id="d3004-128">FLOW\_ESTABLISHED</span></span>

<span data-ttu-id="d3004-129">После успешного завершения 3-стороннего подтверждения TCP-порта для [**\_ потока ALE уровня фвпм, \_ установленного на уровне \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , сопоставляется с фильтром.</span><span class="sxs-lookup"><span data-stu-id="d3004-129">A filter at the [**FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after a TCP three-way handshake has successfully completed.</span></span> <span data-ttu-id="d3004-130">Для трафика, отличного от TCP, фильтр сопоставляется немедленно после того, как будут сопоставлены уровни **проверки подлинности \_ \_ Accept** или Authentication **\_ Connect** .</span><span class="sxs-lookup"><span data-stu-id="d3004-130">For non-TCP traffic, the filter is matched immediately after filters from **AUTH\_RECV\_ACCEPT** or **AUTH\_CONNECT** layers are matched.</span></span>

<span data-ttu-id="d3004-131">Фильтр на этом уровне не должен возвращать блок или разрешить.</span><span class="sxs-lookup"><span data-stu-id="d3004-131">A filter at this layer should not return Block or Permit.</span></span>

<span data-ttu-id="d3004-132">Этот уровень используется драйверами выноски для отслеживания состояния подключения, подробно описанных в документации к [пакету драйверов Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="d3004-132">This layer is used by callout drivers to track connection state, described in detail in the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) documentation.</span></span>

## <a name="resource_release"></a><span data-ttu-id="d3004-133">\_Выпуск ресурсов</span><span class="sxs-lookup"><span data-stu-id="d3004-133">RESOURCE\_RELEASE</span></span>

<span data-ttu-id="d3004-134">После освобождения ресурсов, выделенных с помощью **\_ назначения ресурсов** , фильтр на уровне [**\_ \_ \_ ресурсов \_ Release \_ V {4 \| 6 для уровня фвпм**](management-filtering-layer-identifiers-.md) будет сопоставлен.</span><span class="sxs-lookup"><span data-stu-id="d3004-134">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_RELEASE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after resources that were allocated via **RESOURCE\_ASSIGNMENT** have been freed.</span></span>

## <a name="endpoint_closure"></a><span data-ttu-id="d3004-135">\_замыкание КОНЕЧНОЙ точки</span><span class="sxs-lookup"><span data-stu-id="d3004-135">ENDPOINT\_CLOSURE</span></span>

<span data-ttu-id="d3004-136">Фильтр на уровне [**\_ \_ \_ замыкания конечной точки ALE уровня фвпм \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) сопоставляется при закрытии ПОДКЛЮЧЕНной конечной точки TCP-потока или UDP-сокетов.</span><span class="sxs-lookup"><span data-stu-id="d3004-136">A filter at the [**FWPM\_LAYER\_ALE\_ENDPOINT\_CLOSURE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched when a connected TCP flow or UDP sockets endpoint is closed.</span></span>

## <a name="connect_redirect"></a><span data-ttu-id="d3004-137">Перенаправление подключений \_</span><span class="sxs-lookup"><span data-stu-id="d3004-137">CONNECT\_REDIRECT</span></span>

<span data-ttu-id="d3004-138">Фильтр на уровне [**фвпм " \_ \_ \_ Connect \_ redirect \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) " позволяет изменять удаленные адреса и порты.</span><span class="sxs-lookup"><span data-stu-id="d3004-138">A filter at the [**FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of remote addresses and ports.</span></span> <span data-ttu-id="d3004-139">Исходящее подключение будет перенаправляться на время этого соединения.</span><span class="sxs-lookup"><span data-stu-id="d3004-139">The outbound connection will be redirected for the duration of that connection.</span></span>

## <a name="bind_redirect"></a><span data-ttu-id="d3004-140">Перенаправление привязки \_</span><span class="sxs-lookup"><span data-stu-id="d3004-140">BIND\_REDIRECT</span></span>

<span data-ttu-id="d3004-141">Фильтр на уровне [**фвпм \_ BIND версии \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) позволяет изменять локальный адрес и порты базового сокета.</span><span class="sxs-lookup"><span data-stu-id="d3004-141">A filter at the [**FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of the underlying socket's local address and ports.</span></span> <span data-ttu-id="d3004-142">Локальный сокет будет перенаправлен на время существования сокета</span><span class="sxs-lookup"><span data-stu-id="d3004-142">The local socket will be redirected for the lifetime of the socket</span></span>

## <a name="ale-discard-layers"></a><span data-ttu-id="d3004-143">Слои отклонения ALE</span><span class="sxs-lookup"><span data-stu-id="d3004-143">ALE DISCARD Layers</span></span>

<span data-ttu-id="d3004-144">Для каждого из уровней ALE, описанных выше, модуль фильтрации содержит соответствующий слой отклонения.</span><span class="sxs-lookup"><span data-stu-id="d3004-144">For each of the ALE layers described above the filtering engine contains a matching discard layer.</span></span> <span data-ttu-id="d3004-145">Уровни отклонения ALE используются в целях ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="d3004-145">The ALE discard layers are used by callouts for logging purposes.</span></span> <span data-ttu-id="d3004-146">Пакеты и указания, которые были отклонены на одном из уровней фильтрации ALE, обозначаются соответствующим уровнем отклонения ALE.</span><span class="sxs-lookup"><span data-stu-id="d3004-146">Packets and indications that have been discarded at one of the ALE filtering layers are indicated to the matching ALE discard layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3004-147">См. также</span><span class="sxs-lookup"><span data-stu-id="d3004-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3004-148">Принудительное применение уровня приложения (ALE)</span><span class="sxs-lookup"><span data-stu-id="d3004-148">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="d3004-149">Фильтрация с отслеживанием состояния ALE</span><span class="sxs-lookup"><span data-stu-id="d3004-149">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="d3004-150">Многоадресный или широковещательный трафик ALE</span><span class="sxs-lookup"><span data-stu-id="d3004-150">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="d3004-151">Повторная авторизация ALE</span><span class="sxs-lookup"><span data-stu-id="d3004-151">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="d3004-152">Настройка потока ALE</span><span class="sxs-lookup"><span data-stu-id="d3004-152">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="d3004-153">Потоки TCP-пакетов</span><span class="sxs-lookup"><span data-stu-id="d3004-153">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="d3004-154">Потоки UDP-пакетов</span><span class="sxs-lookup"><span data-stu-id="d3004-154">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="d3004-155">Функции Winsock</span><span class="sxs-lookup"><span data-stu-id="d3004-155">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[<span data-ttu-id="d3004-156">**Флаги условия фильтрации**</span><span class="sxs-lookup"><span data-stu-id="d3004-156">**Filtering Condition Flags**</span></span>](filtering-condition-flags-.md)
</dt> <dt>

[<span data-ttu-id="d3004-157">**Условия фильтрации, доступные на каждом слое фильтрации**</span><span class="sxs-lookup"><span data-stu-id="d3004-157">**Filtering Conditions Available At Each Filtering Layer**</span></span>](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 