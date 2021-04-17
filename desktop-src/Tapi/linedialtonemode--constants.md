---
description: '\_Константы побитового флага линедиалтонемоде описывают различные типы тонов набора. Специальный гудок обычно несет специальное значение (как в ожидании сообщения).'
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Константы LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685156"
---
# <a name="linedialtonemode_-constants"></a><span data-ttu-id="643bb-104">\_Константы линедиалтонемоде</span><span class="sxs-lookup"><span data-stu-id="643bb-104">LINEDIALTONEMODE\_ Constants</span></span>

<span data-ttu-id="643bb-105">Константы побитового флага **линедиалтонемоде \_** описывают различные типы тонов набора.</span><span class="sxs-lookup"><span data-stu-id="643bb-105">The **LINEDIALTONEMODE\_** bit-flag constants describe different types of dial tones.</span></span> <span data-ttu-id="643bb-106">Специальный гудок обычно несет специальное значение (как в ожидании сообщения).</span><span class="sxs-lookup"><span data-stu-id="643bb-106">A special dial tone typically carries a special meaning (as with message waiting).</span></span>

<dl> <dt>

<span data-ttu-id="643bb-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**ЛИНЕДИАЛТОНЕМОДЕ \_ внешний**</span><span class="sxs-lookup"><span data-stu-id="643bb-107"><span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="643bb-108">Это внешний гудок (в общедоступной сети).</span><span class="sxs-lookup"><span data-stu-id="643bb-108">This is an external (public network) dial tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="643bb-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**\_Внутренняя линедиалтонемоде**</span><span class="sxs-lookup"><span data-stu-id="643bb-109"><span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="643bb-110">Это внутренний гудок, как в УАТС.</span><span class="sxs-lookup"><span data-stu-id="643bb-110">This is an internal dial tone, as within a PBX.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="643bb-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**ЛИНЕДИАЛТОНЕМОДЕ, \_ Обычная**</span><span class="sxs-lookup"><span data-stu-id="643bb-111"><span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="643bb-112">Это стандартный гудок, который обычно является непрерывным.</span><span class="sxs-lookup"><span data-stu-id="643bb-112">This is a normal dial tone, which typically is a continuous tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="643bb-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**\_специальное линедиалтонемоде**</span><span class="sxs-lookup"><span data-stu-id="643bb-113"><span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="643bb-114">Это специальный гудок, указывающий на то, что в настоящее время действует определенное условие (известное коммутатору или сети).</span><span class="sxs-lookup"><span data-stu-id="643bb-114">This is a special dial tone indicating that a certain condition (known by the switch or network) is currently in effect.</span></span> <span data-ttu-id="643bb-115">Специальные звуки обычно используют Прерванный тон.</span><span class="sxs-lookup"><span data-stu-id="643bb-115">Special dial tones typically use an interrupted tone.</span></span> <span data-ttu-id="643bb-116">Как и при нормальном тоновом наборе, это означает, что коммутатор готов к получению номера для набора.</span><span class="sxs-lookup"><span data-stu-id="643bb-116">As with a normal dial tone, this indicates that the switch is ready to receive the number to be dialed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="643bb-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**ЛИНЕДИАЛТОНЕМОДЕ \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="643bb-117"><span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="643bb-118">Режим «гудок» недоступен и не будет известен.</span><span class="sxs-lookup"><span data-stu-id="643bb-118">The dial tone mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="643bb-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**ЛИНЕДИАЛТОНЕМОДЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="643bb-119"><span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="643bb-120">Режим «гудок» в настоящее время не известен, но может быть известен позже.</span><span class="sxs-lookup"><span data-stu-id="643bb-120">The dial tone mode is not currently known but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="643bb-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="643bb-121">Remarks</span></span>

<span data-ttu-id="643bb-122">Старшие 16 бит можно назначить для расширений для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="643bb-122">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="643bb-123">16 младших разрядов зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="643bb-123">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="643bb-124">**\_ Константы линедиалтонемоде** используются в структуре данных [**линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) для вызова в состоянии диалтоне.</span><span class="sxs-lookup"><span data-stu-id="643bb-124">The **LINEDIALTONEMODE\_constants** are used within the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) data structure for a call in the dialtone state.</span></span>

## <a name="requirements"></a><span data-ttu-id="643bb-125">Требования</span><span class="sxs-lookup"><span data-stu-id="643bb-125">Requirements</span></span>



| <span data-ttu-id="643bb-126">Требование</span><span class="sxs-lookup"><span data-stu-id="643bb-126">Requirement</span></span> | <span data-ttu-id="643bb-127">Значение</span><span class="sxs-lookup"><span data-stu-id="643bb-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="643bb-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="643bb-128">TAPI version</span></span><br/> | <span data-ttu-id="643bb-129">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="643bb-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="643bb-130">Header</span><span class="sxs-lookup"><span data-stu-id="643bb-130">Header</span></span><br/>       | <dl> <span data-ttu-id="643bb-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="643bb-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




