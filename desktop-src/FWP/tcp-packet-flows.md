---
title: Потоки TCP-пакетов
description: Порядок, в котором уровни обработчика фильтра платформы фильтрации Windows (WFP) проходят во время обычного сеанса TCP.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986647"
---
# <a name="tcp-packet-flows"></a><span data-ttu-id="ef74e-103">Потоки TCP-пакетов</span><span class="sxs-lookup"><span data-stu-id="ef74e-103">TCP Packet Flows</span></span>

<span data-ttu-id="ef74e-104">В этом разделе описывается порядок, в котором уровни обработчика фильтра платформы фильтрации Windows (WFP) проходят во время типичного сеанса TCP.</span><span class="sxs-lookup"><span data-stu-id="ef74e-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical TCP session.</span></span>

> [!Note]  
> <span data-ttu-id="ef74e-105">Пакеты TCP-пакетов для IPv6 следуют той же схеме, что и для IPv4.</span><span class="sxs-lookup"><span data-stu-id="ef74e-105">TCP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="ef74e-106">Потоки пакетов, не относящиеся к TCP, следуют тому же шаблону, что и [пакеты UDP](udp-packet-flows.md).</span><span class="sxs-lookup"><span data-stu-id="ef74e-106">Non-TCP packet flows follow the same pattern as [UDP packet flows](udp-packet-flows.md).</span></span>

 

## <a name="tcp-connection-establishment"></a><span data-ttu-id="ef74e-107">Установка подключения TCP</span><span class="sxs-lookup"><span data-stu-id="ef74e-107">TCP Connection Establishment</span></span>

<dl> <span data-ttu-id="ef74e-108">Сервер (получатель) выполняет пассивное открытие</span><span class="sxs-lookup"><span data-stu-id="ef74e-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="ef74e-109">BIND: \_ \_ Перенаправление привязки ALE уровня фвпм для \_ \_ \_ версии 4 (только для windows 7 или Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="ef74e-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="ef74e-110">привязка: \_ \_ \_ назначение ресурса ALE уровня \_ фвпм \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="ef74e-111">прослушивание: \_ \_ \_ прослушивание проверки подлинности ALE уровня фвпм ( \_ \_ v4)</span><span class="sxs-lookup"><span data-stu-id="ef74e-111">listen: FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V4</span></span>

  
<span data-ttu-id="ef74e-112">Клиент (отправитель) выполняет активное открытие</span><span class="sxs-lookup"><span data-stu-id="ef74e-112">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="ef74e-113">BIND: \_ \_ Перенаправление привязки ALE уровня фвпм для \_ \_ \_ версии 4 (только для windows 7 или Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="ef74e-113">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="ef74e-114">привязка: \_ \_ \_ назначение ресурса ALE уровня \_ фвпм \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-114">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="ef74e-115">Подключение: ФВПМ \_ \_ \_ \_ Перенаправление подключения ALE \_ версии 4 (только windows 7 или Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="ef74e-115">connect: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="ef74e-116">Подключение: \_ \_ \_ Проверка подлинности фвпм уровня ALE для \_ подключения \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-116">connect: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="ef74e-117">SYN: \_ \_ исходящий транспорт уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-117">SYN: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-118">SYN: \_ \_ исходящий уровень фвпм \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-118">SYN: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="ef74e-119">Сервер</span><span class="sxs-lookup"><span data-stu-id="ef74e-119">Server</span></span>

-   <span data-ttu-id="ef74e-120">SYN: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-120">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ef74e-121">SYN: \_ входящий транспорт с уровнем фвпм \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-121">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-122">SYN: \_ \_ \_ Проверка подлинности recv для уровня фвпм, \_ \_ принимаемая до \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-122">SYN: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="ef74e-123">SYN-ACK: \_ \_ исходящий транспорт уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-123">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-124">SYN-ACK: ФВПМ \_ уровень \_ исходящего трафика \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-124">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="ef74e-125">Клиент</span><span class="sxs-lookup"><span data-stu-id="ef74e-125">Client</span></span>

-   <span data-ttu-id="ef74e-126">SYN-ACK: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-126">SYN-ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ef74e-127">SYN-ACK: \_ входящий транспорт на уровне фвпм \_ \_ \_ версии 4</span><span class="sxs-lookup"><span data-stu-id="ef74e-127">SYN-ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-128">\_ \_ \_ Установленный поток ALE уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-128">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="ef74e-129">ACK: \_ \_ исходящий транспорт уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-129">ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-130">ПОДТВЕРЖДЕНИЕ: ФВПМ \_ уровня \_ исходящего трафика \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-130">ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="ef74e-131">Сервер</span><span class="sxs-lookup"><span data-stu-id="ef74e-131">Server</span></span>

-   <span data-ttu-id="ef74e-132">ACK: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-132">ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ef74e-133">ACK: \_ входящий транспорт уровня фвпм для \_ \_ транспорта \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-133">ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-134">\_ \_ \_ Установленный поток ALE уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-134">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="ef74e-135">Прослушивание завершается.</span><span class="sxs-lookup"><span data-stu-id="ef74e-135">Listen completes.</span></span> <span data-ttu-id="ef74e-136">Сервер может выполнить принятие.</span><span class="sxs-lookup"><span data-stu-id="ef74e-136">Server can perform an accept.</span></span>

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="ef74e-137">Получен TCP SYN без одного прослушивания порта или протокола</span><span class="sxs-lookup"><span data-stu-id="ef74e-137">TCP SYN Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="ef74e-138">Сервер (получатель)</span><span class="sxs-lookup"><span data-stu-id="ef74e-138">Server (receiver)</span></span>

-   <span data-ttu-id="ef74e-139">SYN: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-139">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ef74e-140">SYN: \_ \_ \_ удален транспорт входящего транспорта \_ версии 4 \_ (фвпм)</span><span class="sxs-lookup"><span data-stu-id="ef74e-140">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4\_DISCARD</span></span>
-   <span data-ttu-id="ef74e-141">RST: \_ \_ исходящий транспорт уровня фвпм \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-141">RST: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-142">RST: \_ \_ исходящий уровень фвпм \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-142">RST: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="ef74e-143">TCP SYN без конечной точки указывается при отклонениях от транспорта с определенной ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ef74e-143">TCP SYN with no endpoint is indicated at TRANSPORT discard with a specific error condition.</span></span> <span data-ttu-id="ef74e-144">Блокировать этот пакет при отправке отказа, чтобы стек не отправлял соответствующее событие (RST).</span><span class="sxs-lookup"><span data-stu-id="ef74e-144">Block this packet at TRANSPORT discard to cause the stack not to send the corresponding event (RST).</span></span> <span data-ttu-id="ef74e-145">Пример фильтрации в скрытом режиме см. в разделе [запрет сканирования портов](preventing-port-scanning.md).</span><span class="sxs-lookup"><span data-stu-id="ef74e-145">For an example of stealth-mode filtering, see [Preventing Port Scanning](preventing-port-scanning.md).</span></span>

 

## <a name="data-transmitted-over-a-tcp-connection"></a><span data-ttu-id="ef74e-146">Данные, передаваемые через TCP-подключение</span><span class="sxs-lookup"><span data-stu-id="ef74e-146">Data Transmitted Over a TCP Connection</span></span>

<dl> <span data-ttu-id="ef74e-147">Клиент (отправитель)</span><span class="sxs-lookup"><span data-stu-id="ef74e-147">Client (sender)</span></span>

-   <span data-ttu-id="ef74e-148">Отправить</span><span class="sxs-lookup"><span data-stu-id="ef74e-148">send</span></span>
-   <span data-ttu-id="ef74e-149">данные: \_ поток уровня \_ фвпм \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-149">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="ef74e-150">TCP-сегменты: \_ \_ исходящий \_ транспорт уровня фвпм \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-150">TCP segments: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-151">IP-датаграммы: ФВПМ \_ уровень \_ исходящего трафика \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-151">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="ef74e-152">Сервер (получатель)</span><span class="sxs-lookup"><span data-stu-id="ef74e-152">Server (receiver)</span></span>

-   <span data-ttu-id="ef74e-153">IP-датаграммы: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-153">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ef74e-154">Сегменты TCP: \_ входящий транспорт уровня фвпм для \_ входящего \_ транспорта \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-154">TCP segments: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-155">данные: \_ поток уровня \_ фвпм \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-155">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="ef74e-156">Данные доступны для чтения.</span><span class="sxs-lookup"><span data-stu-id="ef74e-156">Data is available to read.</span></span>

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="ef74e-157">Успешная повторная авторизация пакета TCP</span><span class="sxs-lookup"><span data-stu-id="ef74e-157">Successful Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="ef74e-158">Сервер (получатель)</span><span class="sxs-lookup"><span data-stu-id="ef74e-158">Server (receiver)</span></span>

-   <span data-ttu-id="ef74e-159">IP-датаграммы: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-159">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ef74e-160">Сегмент TCP: \_ \_ \_ транспорт входящего транспорта \_ версии 4 фвпм</span><span class="sxs-lookup"><span data-stu-id="ef74e-160">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-161">Сегмент TCP: \_ \_ \_ Проверка подлинности фвпм уровня ALE \_ recv \_ Accept \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-161">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="ef74e-162">данные: \_ поток уровня \_ фвпм \_ v4 (входящий трафик)</span><span class="sxs-lookup"><span data-stu-id="ef74e-162">data: FWPM\_LAYER\_STREAM\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="ef74e-163">Не удалось выполнить повторную авторизацию пакета TCP</span><span class="sxs-lookup"><span data-stu-id="ef74e-163">Failed Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="ef74e-164">Сервер (получатель)</span><span class="sxs-lookup"><span data-stu-id="ef74e-164">Server (receiver)</span></span>

-   <span data-ttu-id="ef74e-165">IP-датаграммы: ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-165">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="ef74e-166">Сегмент TCP: \_ \_ \_ транспорт входящего транспорта \_ версии 4 фвпм</span><span class="sxs-lookup"><span data-stu-id="ef74e-166">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="ef74e-167">Сегмент TCP: \_ \_ \_ Проверка подлинности фвпм уровня ALE \_ recv \_ Accept \_ v4</span><span class="sxs-lookup"><span data-stu-id="ef74e-167">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="ef74e-168">Сегмент TCP: \_ \_ \_ Проверка подлинности \_ recv \_ Accept \_ \_ для фвпм слоя</span><span class="sxs-lookup"><span data-stu-id="ef74e-168">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="tcp-connection-termination"></a><span data-ttu-id="ef74e-169">Завершение TCP-подключения</span><span class="sxs-lookup"><span data-stu-id="ef74e-169">TCP Connection Termination</span></span>

<span data-ttu-id="ef74e-170">Завершение TCP-подключения не указано ни на одном уровне WFP.</span><span class="sxs-lookup"><span data-stu-id="ef74e-170">TCP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef74e-171">См. также</span><span class="sxs-lookup"><span data-stu-id="ef74e-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef74e-172">Повторная авторизация ALE</span><span class="sxs-lookup"><span data-stu-id="ef74e-172">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="ef74e-173">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="ef74e-173">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




