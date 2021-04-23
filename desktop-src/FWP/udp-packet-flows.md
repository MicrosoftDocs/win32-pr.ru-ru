---
title: Потоки UDP-пакетов
description: Порядок, в котором уровни обработчика фильтра платформы фильтрации Windows (WFP) проходят во время типичного сеанса UDP.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331307"
---
# <a name="udp-packet-flows"></a><span data-ttu-id="b9b36-103">Потоки UDP-пакетов</span><span class="sxs-lookup"><span data-stu-id="b9b36-103">UDP Packet Flows</span></span>

<span data-ttu-id="b9b36-104">В этом разделе описывается порядок, в котором уровни обработчика фильтра платформы фильтрации Windows (WFP) проходят во время типичного сеанса UDP.</span><span class="sxs-lookup"><span data-stu-id="b9b36-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical UDP session.</span></span>

> [!Note]  
> <span data-ttu-id="b9b36-105">Потоки пакетов UDP для IPv6 следуют той же схеме, что и для IPv4.</span><span class="sxs-lookup"><span data-stu-id="b9b36-105">UDP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="b9b36-106">Все потоки пакетов, отличных от TCP, следуют той же схеме, что и пакеты UDP.</span><span class="sxs-lookup"><span data-stu-id="b9b36-106">All non-TCP packet flows follow the same pattern as UDP packet flows.</span></span>

 

## <a name="udp-connection-establishment"></a><span data-ttu-id="b9b36-107">Установка подключения UDP</span><span class="sxs-lookup"><span data-stu-id="b9b36-107">UDP Connection Establishment</span></span>

<dl> <span data-ttu-id="b9b36-108">Сервер (получатель) выполняет пассивное открытие</span><span class="sxs-lookup"><span data-stu-id="b9b36-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="b9b36-109">BIND: \_ \_ Перенаправление привязки ALE уровня фвпм для \_ \_ \_ версии 4 (только для windows 7 или Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="b9b36-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="b9b36-110">привязка: \_ \_ \_ назначение ресурса ALE уровня \_ фвпм \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>

  
<span data-ttu-id="b9b36-111">Клиент (отправитель) выполняет активное открытие</span><span class="sxs-lookup"><span data-stu-id="b9b36-111">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="b9b36-112">BIND: \_ \_ Перенаправление привязки ALE уровня фвпм для \_ \_ \_ версии 4 (только для windows 7 или Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="b9b36-112">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="b9b36-113">привязка: \_ \_ \_ назначение ресурса ALE уровня \_ фвпм \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-113">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="b9b36-114">SendTo: ФВПМ \_ \_ \_ \_ Перенаправление подключения ALE \_ версии 4 (только windows 7 или Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="b9b36-114">sendto: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="b9b36-115">SendTo: \_ \_ \_ Проверка подлинности фвпм уровня ALE \_ \_ v4 Connect</span><span class="sxs-lookup"><span data-stu-id="b9b36-115">sendto: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="b9b36-116">\_ \_ \_ Установленный поток ALE уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-116">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="b9b36-117">данные: \_ данные о \_ датаграмме уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-117">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>
-   <span data-ttu-id="b9b36-118">Сообщение UDP: \_ \_ исходящий транспорт фвпм Layer \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-118">UDP message: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="b9b36-119">IP-датаграммы: ФВПМ \_ уровень \_ исходящего трафика \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-119">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="b9b36-120">Сервер</span><span class="sxs-lookup"><span data-stu-id="b9b36-120">Server</span></span>

-   <span data-ttu-id="b9b36-121">IP-датаграммы: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-121">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="b9b36-122">UDP-сообщение: \_ \_ транспорт фвпм входящего \_ транспорта \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-122">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="b9b36-123">UDP-сообщение: \_ \_ \_ Проверка подлинности приема на уровне фвпм для проверки \_ \_ принятия \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-123">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="b9b36-124">\_ \_ \_ Установленный поток ALE уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-124">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="b9b36-125">данные: \_ данные о \_ датаграмме уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-125">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="b9b36-126">Получено сообщение UDP без одного прослушивания порта или протокола</span><span class="sxs-lookup"><span data-stu-id="b9b36-126">UDP Message Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="b9b36-127">Сервер (получатель)</span><span class="sxs-lookup"><span data-stu-id="b9b36-127">Server (receiver)</span></span>

-   <span data-ttu-id="b9b36-128">IP-датаграммы: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-128">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="b9b36-129">IP-датаграммы: ФВПМ \_ уровень \_ входящего трафика \_ иппаккет \_ v4 \_</span><span class="sxs-lookup"><span data-stu-id="b9b36-129">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4\_DISCARD</span></span>
-   <span data-ttu-id="b9b36-130">Недостижимый адрес ICMP: \_ \_ Исходящая \_ Ошибка ICMP уровня фвпм \_ \_ IPv4</span><span class="sxs-lookup"><span data-stu-id="b9b36-130">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V4</span></span>
-   <span data-ttu-id="b9b36-131">Недостижимый адрес ICMP: \_ \_ исходящий транспорт фвпм Layer \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-131">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="b9b36-132">Недостижимый адрес ICMP: \_ \_ исходящий уровень фвпм \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-132">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="b9b36-133">UDP без конечной точки указывается в ИППАККЕТ Discard с конкретным условием ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9b36-133">UDP with no endpoint is indicated at IPPACKET discard with a specific error condition.</span></span> <span data-ttu-id="b9b36-134">Блокировать этот пакет в ИППАККЕТ Discard, чтобы стек не отправлял соответствующее событие (ошибка ICMP).</span><span class="sxs-lookup"><span data-stu-id="b9b36-134">Block this packet at IPPACKET discard to cause the stack not to send the corresponding event (ICMP error).</span></span>

 

## <a name="successful-reauthorization-of-a-udp-packet"></a><span data-ttu-id="b9b36-135">Успешная повторная авторизация пакета UDP</span><span class="sxs-lookup"><span data-stu-id="b9b36-135">Successful Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="b9b36-136">Сервер (получатель)</span><span class="sxs-lookup"><span data-stu-id="b9b36-136">Server (receiver)</span></span>

-   <span data-ttu-id="b9b36-137">IP-датаграммы: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-137">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="b9b36-138">UDP-сообщение: \_ \_ транспорт фвпм входящего \_ транспорта \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-138">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="b9b36-139">UDP-сообщение: \_ \_ \_ Проверка подлинности приема на уровне фвпм для проверки \_ \_ принятия \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-139">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="b9b36-140">UDP-сообщение: \_ фвпм \_ Layer \_ Data \_ 4 (входящий трафик)</span><span class="sxs-lookup"><span data-stu-id="b9b36-140">UDP message: FWPM\_LAYER\_DATAGRAM\_DATA\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-udp-packet"></a><span data-ttu-id="b9b36-141">Сбой при пересоздании пакета UDP</span><span class="sxs-lookup"><span data-stu-id="b9b36-141">Failed Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="b9b36-142">Сервер (получатель)</span><span class="sxs-lookup"><span data-stu-id="b9b36-142">Server (receiver)</span></span>

-   <span data-ttu-id="b9b36-143">IP-датаграммы: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-143">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="b9b36-144">UDP-сообщение: \_ \_ транспорт фвпм входящего \_ транспорта \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-144">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="b9b36-145">UDP-сообщение: \_ \_ \_ Проверка подлинности приема на уровне фвпм для проверки \_ \_ принятия \_ v4</span><span class="sxs-lookup"><span data-stu-id="b9b36-145">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="b9b36-146">UDP-сообщение: \_ \_ \_ Проверка подлинности recv фвпм уровня проверки \_ \_ приема \_ входящего трафика v4 \_</span><span class="sxs-lookup"><span data-stu-id="b9b36-146">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="udp-connection-termination"></a><span data-ttu-id="b9b36-147">Завершение подключения UDP</span><span class="sxs-lookup"><span data-stu-id="b9b36-147">UDP Connection Termination</span></span>

<span data-ttu-id="b9b36-148">Завершение подключения UDP не указано ни на одном уровне WFP.</span><span class="sxs-lookup"><span data-stu-id="b9b36-148">UDP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9b36-149">См. также</span><span class="sxs-lookup"><span data-stu-id="b9b36-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9b36-150">Повторная авторизация ALE</span><span class="sxs-lookup"><span data-stu-id="b9b36-150">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="b9b36-151">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="b9b36-151">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




