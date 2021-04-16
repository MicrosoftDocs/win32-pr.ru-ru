---
description: '\_Константы линеажентстатикс описывают состояние агента по адресу.'
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Константы LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689395"
---
# <a name="lineagentstateex_-constants"></a><span data-ttu-id="054f1-103">\_Константы линеажентстатикс</span><span class="sxs-lookup"><span data-stu-id="054f1-103">LINEAGENTSTATEEX\_ Constants</span></span>

<span data-ttu-id="054f1-104">**\_ Константы линеажентстатикс** описывают состояние агента по адресу.</span><span class="sxs-lookup"><span data-stu-id="054f1-104">The **LINEAGENTSTATEEX\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="054f1-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**ЛИНЕАЖЕНТСТАТИКС \_ бусякд**</span><span class="sxs-lookup"><span data-stu-id="054f1-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="054f1-106">Агент занят обработкой вызова, направляемого из очереди ACD.</span><span class="sxs-lookup"><span data-stu-id="054f1-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="054f1-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**ЛИНЕАЖЕНТСТАТИКС \_ бусинкоминг**</span><span class="sxs-lookup"><span data-stu-id="054f1-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="054f1-108">Агент занят обработкой входящего вызова, который не был передан агенту из очереди ACD, в которой вошел агент.</span><span class="sxs-lookup"><span data-stu-id="054f1-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="054f1-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**ЛИНЕАЖЕНТСТАТИКС \_ бусйоутгоинг**</span><span class="sxs-lookup"><span data-stu-id="054f1-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX\_BUSYOUTGOING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="054f1-110">Агент занят обработкой исходящего вызова, например одного маршрута из очереди прогнозируемого набора.</span><span class="sxs-lookup"><span data-stu-id="054f1-110">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="054f1-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**ЛИНЕАЖЕНТСТАТИКС \_ NOTREADY**</span><span class="sxs-lookup"><span data-stu-id="054f1-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="054f1-112">Агент вошел в систему, но занят задачей, отличной от обслуживания вызова (например, при прерывании).</span><span class="sxs-lookup"><span data-stu-id="054f1-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="054f1-113">Никакие дополнительные вызовы не должны маршрутизироваться агенту.</span><span class="sxs-lookup"><span data-stu-id="054f1-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="054f1-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**ЛИНЕАЖЕНТСТАТИКС \_ Готово**</span><span class="sxs-lookup"><span data-stu-id="054f1-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="054f1-115">Агент готов принять вызовы.</span><span class="sxs-lookup"><span data-stu-id="054f1-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="054f1-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**ЛИНЕАЖЕНТСТАТИКС \_ выпущен**</span><span class="sxs-lookup"><span data-stu-id="054f1-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="054f1-117">Агент был выпущен, возможно, из-за того, что он вышел из системы.</span><span class="sxs-lookup"><span data-stu-id="054f1-117">The agent has been released, probably because they logged off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="054f1-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**ЛИНЕАЖЕНТСТАТИКС \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="054f1-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="054f1-119">Состояние агента неизвестно, но может быть известно позже.</span><span class="sxs-lookup"><span data-stu-id="054f1-119">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="054f1-120">Это может быть переходное состояние при первом открытии строки или адреса.</span><span class="sxs-lookup"><span data-stu-id="054f1-120">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="054f1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="054f1-121">Requirements</span></span>



| <span data-ttu-id="054f1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="054f1-122">Requirement</span></span> | <span data-ttu-id="054f1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="054f1-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="054f1-124">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="054f1-124">TAPI version</span></span><br/> | <span data-ttu-id="054f1-125">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="054f1-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="054f1-126">Header</span><span class="sxs-lookup"><span data-stu-id="054f1-126">Header</span></span><br/>       | <dl> <span data-ttu-id="054f1-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="054f1-127"><dt>Tapi.h</dt></span></span> </dl> |



 

 




