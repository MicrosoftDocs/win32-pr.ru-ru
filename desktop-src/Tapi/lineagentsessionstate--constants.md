---
description: '\_Константы линеажентсессионстате описывают различные состояния сеанса агента.'
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: Константы LINEAGENTSESSIONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675421"
---
# <a name="lineagentsessionstate_-constants"></a><span data-ttu-id="ecb27-103">\_Константы линеажентсессионстате</span><span class="sxs-lookup"><span data-stu-id="ecb27-103">LINEAGENTSESSIONSTATE\_ Constants</span></span>

<span data-ttu-id="ecb27-104">**\_ Константы линеажентсессионстате** описывают различные состояния сеанса агента.</span><span class="sxs-lookup"><span data-stu-id="ecb27-104">The **LINEAGENTSESSIONSTATE\_ constants** describe various agent session states.</span></span>

<dl> <dt>

<span data-ttu-id="ecb27-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ бусйонкалл**</span><span class="sxs-lookup"><span data-stu-id="ecb27-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE\_BUSYONCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ecb27-106">Агент занят обработкой вызова.</span><span class="sxs-lookup"><span data-stu-id="ecb27-106">The agent is busy handling a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecb27-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ бусиврапуп**</span><span class="sxs-lookup"><span data-stu-id="ecb27-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE\_BUSYWRAPUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ecb27-108">Агент занят обработкой оболочки вызова.</span><span class="sxs-lookup"><span data-stu-id="ecb27-108">The agent is busy handling the wrap-up of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecb27-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ завершено**</span><span class="sxs-lookup"><span data-stu-id="ecb27-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE\_ENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ecb27-110">Сеанс агента завершен.</span><span class="sxs-lookup"><span data-stu-id="ecb27-110">The agent session has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecb27-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ NOTREADY**</span><span class="sxs-lookup"><span data-stu-id="ecb27-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ecb27-112">Агент вошел в систему, но занят задачей, отличной от обслуживания вызова (например, при прерывании).</span><span class="sxs-lookup"><span data-stu-id="ecb27-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="ecb27-113">Никакие дополнительные вызовы не должны маршрутизироваться агенту.</span><span class="sxs-lookup"><span data-stu-id="ecb27-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecb27-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ Готово**</span><span class="sxs-lookup"><span data-stu-id="ecb27-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ecb27-115">Агент готов принять вызовы.</span><span class="sxs-lookup"><span data-stu-id="ecb27-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecb27-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ выпущен**</span><span class="sxs-lookup"><span data-stu-id="ecb27-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ecb27-117">Сеанс агента был выпущен.</span><span class="sxs-lookup"><span data-stu-id="ecb27-117">The agent session has been released.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecb27-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ecb27-118">Requirements</span></span>



| <span data-ttu-id="ecb27-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ecb27-119">Requirement</span></span> | <span data-ttu-id="ecb27-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ecb27-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ecb27-121">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ecb27-121">TAPI version</span></span><br/> | <span data-ttu-id="ecb27-122">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="ecb27-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="ecb27-123">Header</span><span class="sxs-lookup"><span data-stu-id="ecb27-123">Header</span></span><br/>       | <dl> <span data-ttu-id="ecb27-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb27-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




