---
description: '\_Константы линеажентстате описывают состояние агента по адресу.'
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Константы LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679913"
---
# <a name="lineagentstate_-constants"></a><span data-ttu-id="e9674-103">\_Константы линеажентстате</span><span class="sxs-lookup"><span data-stu-id="e9674-103">LINEAGENTSTATE\_ Constants</span></span>

<span data-ttu-id="e9674-104">**\_ Константы линеажентстате** описывают состояние агента по адресу.</span><span class="sxs-lookup"><span data-stu-id="e9674-104">The **LINEAGENTSTATE\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="e9674-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**ЛИНЕАЖЕНТСТАТЕ \_ бусякд**</span><span class="sxs-lookup"><span data-stu-id="e9674-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-106">Агент занят обработкой вызова, направляемого из очереди ACD.</span><span class="sxs-lookup"><span data-stu-id="e9674-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9674-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**ЛИНЕАЖЕНТСТАТЕ \_ бусинкоминг**</span><span class="sxs-lookup"><span data-stu-id="e9674-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-108">Агент занят обработкой входящего вызова, который не был передан агенту из очереди ACD, в которой вошел агент.</span><span class="sxs-lookup"><span data-stu-id="e9674-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9674-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**ЛИНЕАЖЕНТСТАТЕ \_ бусйосер**</span><span class="sxs-lookup"><span data-stu-id="e9674-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE\_BUSYOTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-110">Агент занят обработкой другого типа вызова, например, исходящего личного звонка, не переданного агенту с помощью прогнозирующего набора.</span><span class="sxs-lookup"><span data-stu-id="e9674-110">The agent is busy handling another type of call, such as an outgoing personal call not transferred to the agent by a predictive dialer.</span></span> <span data-ttu-id="e9674-111">Это значение можно также использовать, когда агент может быть занят при вызове, но тип вызова неизвестен.</span><span class="sxs-lookup"><span data-stu-id="e9674-111">This value can also be used when the agent is known to be busy on a call but the type of call is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9674-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**ЛИНЕАЖЕНТСТАТЕ \_ бусйоутбаунд**</span><span class="sxs-lookup"><span data-stu-id="e9674-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE\_BUSYOUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-113">Агент занят обработкой исходящего вызова, например одного маршрута из очереди прогнозируемого набора.</span><span class="sxs-lookup"><span data-stu-id="e9674-113">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9674-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**ЛИНЕАЖЕНТСТАТЕ \_ логжедофф**</span><span class="sxs-lookup"><span data-stu-id="e9674-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE\_LOGGEDOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-115">В адресе не вошел агент.</span><span class="sxs-lookup"><span data-stu-id="e9674-115">No agent is logged in on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9674-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**ЛИНЕАЖЕНТСТАТЕ \_ NOTREADY**</span><span class="sxs-lookup"><span data-stu-id="e9674-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-117">Агент вошел в систему, но занят задачей, отличной от обслуживания вызова (например, при прерывании).</span><span class="sxs-lookup"><span data-stu-id="e9674-117">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="e9674-118">Никакие дополнительные вызовы не должны маршрутизироваться агенту.</span><span class="sxs-lookup"><span data-stu-id="e9674-118">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9674-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**ЛИНЕАЖЕНТСТАТЕ \_ Готово**</span><span class="sxs-lookup"><span data-stu-id="e9674-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-120">Агент готов принять вызовы.</span><span class="sxs-lookup"><span data-stu-id="e9674-120">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9674-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**ЛИНЕАЖЕНТСТАТЕ \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="e9674-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-122">Состояние агента неизвестно и никогда не станет известным.</span><span class="sxs-lookup"><span data-stu-id="e9674-122">The agent state is unknown and will never become known.</span></span> <span data-ttu-id="e9674-123">В [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)это условие также может быть представлено членом **дважентстате** , для которого задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="e9674-123">In [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), this condition can also be represented by the **dwAgentState** member being set to 0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9674-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**ЛИНЕАЖЕНТСТАТЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="e9674-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-125">Состояние агента неизвестно, но может быть известно позже.</span><span class="sxs-lookup"><span data-stu-id="e9674-125">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="e9674-126">Это может быть переходное состояние при первом открытии строки или адреса.</span><span class="sxs-lookup"><span data-stu-id="e9674-126">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9674-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**ЛИНЕАЖЕНТСТАТЕ \_ воркингафтеркалл**</span><span class="sxs-lookup"><span data-stu-id="e9674-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE\_WORKINGAFTERCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e9674-128">Агент завершил предыдущий вызов, но по-прежнему занят работой, связанным с этим вызовом.</span><span class="sxs-lookup"><span data-stu-id="e9674-128">The agent has completed the preceding call, but is still occupied with work related to that call.</span></span> <span data-ttu-id="e9674-129">Агент не должен принимать дополнительные вызовы.</span><span class="sxs-lookup"><span data-stu-id="e9674-129">The agent should not receive additional calls.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9674-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9674-130">Remarks</span></span>

<span data-ttu-id="e9674-131">Верхние 16 разрядов этого набора констант зарезервированы для расширений для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="e9674-131">The upper 16 bits of this set of constants are reserved for device-specific extensions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9674-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e9674-132">Requirements</span></span>



| <span data-ttu-id="e9674-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e9674-133">Requirement</span></span> | <span data-ttu-id="e9674-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e9674-134">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e9674-135">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e9674-135">TAPI version</span></span><br/> | <span data-ttu-id="e9674-136">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e9674-136">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e9674-137">Header</span><span class="sxs-lookup"><span data-stu-id="e9674-137">Header</span></span><br/>       | <dl> <span data-ttu-id="e9674-138"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9674-138"><dt>Tapi.h</dt></span></span> </dl> |



 

 




