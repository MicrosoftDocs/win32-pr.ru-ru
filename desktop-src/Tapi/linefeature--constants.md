---
description: '\_Константы линефеатуре список операций, которые могут быть вызваны в строке с помощью этого API.'
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Константы LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680032"
---
# <a name="linefeature_-constants"></a><span data-ttu-id="94a7d-103">\_Константы линефеатуре</span><span class="sxs-lookup"><span data-stu-id="94a7d-103">LINEFEATURE\_ Constants</span></span>

<span data-ttu-id="94a7d-104">**\_ Константы линефеатуре** список операций, которые могут быть вызваны в строке с помощью этого API.</span><span class="sxs-lookup"><span data-stu-id="94a7d-104">The **LINEFEATURE\_ constants** list the operations that can be invoked on a line using this API.</span></span>

<dl> <dt>

<span data-ttu-id="94a7d-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**ЛИНЕФЕАТУРЕ \_ девспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="94a7d-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94a7d-106">В строке можно использовать операции для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="94a7d-106">Device-specific operations can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94a7d-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**ЛИНЕФЕАТУРЕ \_ девспеЦификфеат**</span><span class="sxs-lookup"><span data-stu-id="94a7d-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE\_DEVSPECIFICFEAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94a7d-108">В строке можно использовать функции для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="94a7d-108">Device-specific features can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94a7d-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**ЛИНЕФЕАТУРЕ \_ вперед**</span><span class="sxs-lookup"><span data-stu-id="94a7d-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94a7d-110">В строке можно использовать пересылку всех адресов.</span><span class="sxs-lookup"><span data-stu-id="94a7d-110">Forwarding of all addresses can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94a7d-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**ЛИНЕФЕАТУРЕ \_ форвардднд**</span><span class="sxs-lookup"><span data-stu-id="94a7d-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94a7d-112">Функцию [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (с пустым адресом назначения) можно использовать, чтобы включить функцию "не беспокоить" для всех адресов в строке.</span><span class="sxs-lookup"><span data-stu-id="94a7d-112">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on all addresses on the line.</span></span> <span data-ttu-id="94a7d-113">\_Также будет задано перенаправление линефеатуре.</span><span class="sxs-lookup"><span data-stu-id="94a7d-113">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="94a7d-114">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="94a7d-114">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94a7d-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**ЛИНЕФЕАТУРЕ \_ форвардфвд**</span><span class="sxs-lookup"><span data-stu-id="94a7d-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94a7d-116">Функцию [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward) можно использовать для переадресации вызовов по всем адресам в строке на другие числа.</span><span class="sxs-lookup"><span data-stu-id="94a7d-116">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on all address on the line to other numbers.</span></span> <span data-ttu-id="94a7d-117">\_Также будет задано перенаправление линефеатуре.</span><span class="sxs-lookup"><span data-stu-id="94a7d-117">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="94a7d-118">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="94a7d-118">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94a7d-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**ЛИНЕФЕАТУРЕ \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="94a7d-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94a7d-120">Исходящий вызов может быть размещен в этой строке с использованием неопределенного адреса.</span><span class="sxs-lookup"><span data-stu-id="94a7d-120">An outgoing call can be placed on this line using an unspecified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94a7d-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**ЛИНЕФЕАТУРЕ \_ сетдевстатус**</span><span class="sxs-lookup"><span data-stu-id="94a7d-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE\_SETDEVSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94a7d-122">Функция [**линесетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) может быть вызвана на устройстве линии.</span><span class="sxs-lookup"><span data-stu-id="94a7d-122">The [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) function can be invoked on the line device.</span></span> <span data-ttu-id="94a7d-123">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="94a7d-123">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94a7d-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**ЛИНЕФЕАТУРЕ \_ сетмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="94a7d-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94a7d-125">В этой строке можно задать элемент управления мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="94a7d-125">Media control can be set on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94a7d-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**ЛИНЕФЕАТУРЕ \_ сеттерминал**</span><span class="sxs-lookup"><span data-stu-id="94a7d-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94a7d-127">Можно задать режимы терминала для этой строки.</span><span class="sxs-lookup"><span data-stu-id="94a7d-127">Terminal modes for this line can be set.</span></span>

> [!Note]  
> <span data-ttu-id="94a7d-128">Если в элементе **двлинефеатурес** в [**линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) не задан ни один из новых измененных бит пересылки, но установлен бит перенаправления линефеатуре \_ , то любой из режимов прямого доступа может работать; поставщик услуг просто не указал, какие из них.</span><span class="sxs-lookup"><span data-stu-id="94a7d-128">If neither of the new modified "FORWARD" bits is set in the **dwLineFeatures** member in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) but the LINEFEATURE\_FORWARD bit is set, then any of the forward modes can work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94a7d-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94a7d-129">Remarks</span></span>

<span data-ttu-id="94a7d-130">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="94a7d-130">No extensibility.</span></span> <span data-ttu-id="94a7d-131">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="94a7d-131">All 32 bits are reserved.</span></span>

<span data-ttu-id="94a7d-132">\_Константы линефеатуре используются в [**линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (возвращается [**линежетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span><span class="sxs-lookup"><span data-stu-id="94a7d-132">The LINEFEATURE\_ constants are used in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (returned by [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span></span> <span data-ttu-id="94a7d-133">[**Линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) отчеты для определенной строки, какие функции строк фактически вызываются, пока строка находится в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="94a7d-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) reports, for a given line, which line features can actually be invoked while the line is in the current state.</span></span> <span data-ttu-id="94a7d-134">Приложение сделает это определение динамически после изменения состояния строки, как правило, из-за адреса или действий, связанных с вызовами, в строке.</span><span class="sxs-lookup"><span data-stu-id="94a7d-134">An application would make this determination dynamically after line state changes, typically caused by address or call-related activities on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="94a7d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="94a7d-135">Requirements</span></span>



| <span data-ttu-id="94a7d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="94a7d-136">Requirement</span></span> | <span data-ttu-id="94a7d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="94a7d-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="94a7d-138">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="94a7d-138">TAPI version</span></span><br/> | <span data-ttu-id="94a7d-139">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="94a7d-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="94a7d-140">Header</span><span class="sxs-lookup"><span data-stu-id="94a7d-140">Header</span></span><br/>       | <dl> <span data-ttu-id="94a7d-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="94a7d-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94a7d-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94a7d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a7d-143">**линедевстатус**</span><span class="sxs-lookup"><span data-stu-id="94a7d-143">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="94a7d-144">**линефорвард**</span><span class="sxs-lookup"><span data-stu-id="94a7d-144">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="94a7d-145">**линежетлинедевстатус**</span><span class="sxs-lookup"><span data-stu-id="94a7d-145">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="94a7d-146">**линесетлинедевстатус**</span><span class="sxs-lookup"><span data-stu-id="94a7d-146">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




