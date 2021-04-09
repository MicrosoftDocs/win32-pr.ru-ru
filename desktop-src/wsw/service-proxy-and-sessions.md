---
title: Прокси-сервер службы и сеансы
description: Прокси-сервер службы имеет особые характеристики для привязок каналов сеанса и не на основе сеанса.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Прокси службы и сеансы веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070875"
---
# <a name="service-proxy-and-sessions"></a><span data-ttu-id="cd5c3-106">Прокси-сервер службы и сеансы</span><span class="sxs-lookup"><span data-stu-id="cd5c3-106">Service Proxy and Sessions</span></span>

<span data-ttu-id="cd5c3-107">[Прокси-сервер службы](service-proxy.md) имеет особые характеристики для привязок каналов сеанса и не на основе сеанса.</span><span class="sxs-lookup"><span data-stu-id="cd5c3-107">The [service proxy](service-proxy.md) has special behaviors for session and non-session-based channel bindings.</span></span> <span data-ttu-id="cd5c3-108">Прокси-сервер службы предоставляет семантику на основе сеанса, если базовая привязка канала основана на сеансе.</span><span class="sxs-lookup"><span data-stu-id="cd5c3-108">The service proxy provides session based semantics if the underlying channel binding is session based.</span></span> <span data-ttu-id="cd5c3-109">В этом случае для вызовов служб используется один канал.</span><span class="sxs-lookup"><span data-stu-id="cd5c3-109">In this case a single channel is used to service calls.</span></span> <span data-ttu-id="cd5c3-110">Однако если привязка канала не основана на сеансе, прокси службы создает отдельный канал для каждого вызова.</span><span class="sxs-lookup"><span data-stu-id="cd5c3-110">However, if the channel binding is not session based, the service proxy creates a separate channel for each call.</span></span> <span data-ttu-id="cd5c3-111">Однако обратите внимание, что каналы, не являющиеся каналами на основе сеансов, помещаются в пул и, возможно, используются повторно.</span><span class="sxs-lookup"><span data-stu-id="cd5c3-111">Note, though, that non-session-based channels are pooled and maybe reused.</span></span> <span data-ttu-id="cd5c3-112">При повторном использовании канала прокси-сервер службы сохраняет канал открытым, если базовый канал не исправен или вызов по каналу привел к сбою канала в прокси-сервере службы.</span><span class="sxs-lookup"><span data-stu-id="cd5c3-112">In reusing a channel, the service proxy keeps the channel open if the underlying channel has not faulted or the call on a channel has resulted in the service proxy's faulting the channel.</span></span> <span data-ttu-id="cd5c3-113">Обратите внимание, что.</span><span class="sxs-lookup"><span data-stu-id="cd5c3-113">Note that.</span></span> <span data-ttu-id="cd5c3-114">за исключением случая сбоя, после открытия канала он остается открытым, пока прокси-сервер службы открыт и закрыт только при закрытии прокси-сервера службы.</span><span class="sxs-lookup"><span data-stu-id="cd5c3-114">except in the event of a fault, once a channel is opened it is kept open as long as the service proxy is open and is closed only when the service proxy is closed.</span></span>


<span data-ttu-id="cd5c3-115">Если привязка канала основана на сеансе и в случае сбоя базового канала, конечный автомат прокси-сервера службы перейдет в состояние [**\_ \_ \_ \_ сбоя прокси-службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="cd5c3-115">If the channel binding is session based and if the underlying channel faults, the service proxy state machine will transition into the [**WS\_SERVICE\_PROXY\_STATE\_FAULTED**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) state.</span></span> <span data-ttu-id="cd5c3-116">В случае привязки канала, не основанного на сеансе, ошибка в базовом канале не приводит к переходу прокси-сервера в состояние **\_ \_ \_ \_ сбоя прокси-сервера службы WS** .</span><span class="sxs-lookup"><span data-stu-id="cd5c3-116">In the case of non-session based channel binding, a fault in the underlying channel does not cause the proxy to transition into **WS\_SERVICE\_PROXY\_STATE\_FAULTED** state.</span></span>

<span data-ttu-id="cd5c3-117">Дополнительные сведения о прокси-сервере службы и его связи с состоянием см. в разделе " [прокси-сервер службы](service-proxy.md) ".</span><span class="sxs-lookup"><span data-stu-id="cd5c3-117">For more information on the service proxy and its relation to state, see the [Service Proxy](service-proxy.md) topic.</span></span> <span data-ttu-id="cd5c3-118">Примеры различных привязок каналов см. в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="cd5c3-118">For examples of different channel bindings see the following examples:</span></span>

-   <span data-ttu-id="cd5c3-119">Привязка канала без сеанса, [хттпкалкулаторклиентексампле](httpcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="cd5c3-119">non-session channel binding, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span></span>
-   <span data-ttu-id="cd5c3-120">Привязка канала на основе сеанса, [сессионфуллкалкулаторклиентексампле](sessionfullcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="cd5c3-120">session-based channel binding, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span></span>

 

 




