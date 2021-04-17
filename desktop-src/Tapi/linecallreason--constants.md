---
description: '\_Константы побитового флага линекаллреасон описывают причину вызова.'
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Константы LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674895"
---
# <a name="linecallreason_-constants"></a><span data-ttu-id="e3a57-103">\_Константы линекаллреасон</span><span class="sxs-lookup"><span data-stu-id="e3a57-103">LINECALLREASON\_ Constants</span></span>

<span data-ttu-id="e3a57-104">Константы побитового флага **линекаллреасон \_** описывают причину вызова.</span><span class="sxs-lookup"><span data-stu-id="e3a57-104">The **LINECALLREASON\_** bit-flag constants describe the reason for a call.</span></span>

<dl> <dt>

<span data-ttu-id="e3a57-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**ЛИНЕКАЛЛРЕАСОН \_ каллкомплетион**</span><span class="sxs-lookup"><span data-stu-id="e3a57-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON\_CALLCOMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-106">Вызов был результатом запроса на завершение вызова.</span><span class="sxs-lookup"><span data-stu-id="e3a57-106">The call was the result of a call completion request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**ЛИНЕКАЛЛРЕАСОН \_ кампедон**</span><span class="sxs-lookup"><span data-stu-id="e3a57-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON\_CAMPEDON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-108">В адресе был включен звонок.</span><span class="sxs-lookup"><span data-stu-id="e3a57-108">The call was camped on the address.</span></span> <span data-ttu-id="e3a57-109">Обычно он отображается изначально в состоянии onhold и может быть переключен на использование [**линесвафолд**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span><span class="sxs-lookup"><span data-stu-id="e3a57-109">Usually, it appears initially in the onhold state, and can be switched to using [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span></span> <span data-ttu-id="e3a57-110">Если активный вызов переходит в состояние простоя, вызов с включенным параметром "в состоянии" может измениться на "предложение", а устройство начнет звонить.</span><span class="sxs-lookup"><span data-stu-id="e3a57-110">If an active call becomes idle, the camped-on call may change to the offering state and the device start ringing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**ЛИНЕКАЛЛРЕАСОН \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="e3a57-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-112">Это прямой входящий или исходящий вызов.</span><span class="sxs-lookup"><span data-stu-id="e3a57-112">This is a direct incoming or outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**ЛИНЕКАЛЛРЕАСОН \_ фвдбуси**</span><span class="sxs-lookup"><span data-stu-id="e3a57-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON\_FWDBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-114">Этот вызов был перенаправлен от другого расширения, которое было занято во время вызова.</span><span class="sxs-lookup"><span data-stu-id="e3a57-114">This call was forwarded from another extension that was busy at the time of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**ЛИНЕКАЛЛРЕАСОН \_ фвдноансвер**</span><span class="sxs-lookup"><span data-stu-id="e3a57-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON\_FWDNOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-116">Вызов был перенаправлен от другого расширения, которое не ответило на вызов после некоторого числа колец.</span><span class="sxs-lookup"><span data-stu-id="e3a57-116">The call was forwarded from another extension that didn't answer the call after some number of rings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**ЛИНЕКАЛЛРЕАСОН \_ фвдунконд**</span><span class="sxs-lookup"><span data-stu-id="e3a57-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON\_FWDUNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-118">Вызов был перенаправлен безусловно из другого числа.</span><span class="sxs-lookup"><span data-stu-id="e3a57-118">The call was forwarded unconditionally from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**ЛИНЕКАЛЛРЕАСОН \_ атака**</span><span class="sxs-lookup"><span data-stu-id="e3a57-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-120">Вызов, появляющийся в строке с помощью действия завершения вызова, вызванного другой станцией или действием оператора.</span><span class="sxs-lookup"><span data-stu-id="e3a57-120">The call intruded onto the line, either by a call completion action invoked by another station or by operator action.</span></span> <span data-ttu-id="e3a57-121">В зависимости от реализации переключателя вызов может находиться либо в состоянии Connected, либо на Конференции с существующим активным вызовом в строке.</span><span class="sxs-lookup"><span data-stu-id="e3a57-121">Depending on switch implementation, the call may appear either in the connected state, or conferenced with an existing active call on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**ЛИНЕКАЛЛРЕАСОН \_ приостановлено**</span><span class="sxs-lookup"><span data-stu-id="e3a57-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON\_PARKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-123">Звонок был приостановлен по адресу.</span><span class="sxs-lookup"><span data-stu-id="e3a57-123">The call was parked on the address.</span></span> <span data-ttu-id="e3a57-124">Обычно он отображается изначально в состоянии onholdии.</span><span class="sxs-lookup"><span data-stu-id="e3a57-124">Usually, it appears initially in the onhold state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**\_Отправка линекаллреасон**</span><span class="sxs-lookup"><span data-stu-id="e3a57-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-126">Вызов был выбран из другого расширения.</span><span class="sxs-lookup"><span data-stu-id="e3a57-126">The call was picked up from another extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**Перенаправление ЛИНЕКАЛЛРЕАСОН \_**</span><span class="sxs-lookup"><span data-stu-id="e3a57-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**LINECALLREASON\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-128">Вызов перенаправляется на эту станцию.</span><span class="sxs-lookup"><span data-stu-id="e3a57-128">The call was redirected to this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**\_напоминание линекаллреасон**</span><span class="sxs-lookup"><span data-stu-id="e3a57-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON\_REMINDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-130">Вызов — это напоминание (или «отзыв») о том, что пользователь придерживается или удерживается (потенциально) длительное время.</span><span class="sxs-lookup"><span data-stu-id="e3a57-130">The call is a reminder (or "recall") that the user has a call parked or on hold for (potentially) a long time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**ЛИНЕКАЛЛРЕАСОН \_ раутерекуест**</span><span class="sxs-lookup"><span data-stu-id="e3a57-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON\_ROUTEREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-132">Вызов отображается по адресу, так как параметру требуются инструкции по маршрутизации из приложения.</span><span class="sxs-lookup"><span data-stu-id="e3a57-132">The call appears on the address because the switch needs routing instructions from the application.</span></span> <span data-ttu-id="e3a57-133">Приложение должно проверить элемент **калледид** в [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)и использовать функцию [**линередирект**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) для предоставления нового набора адресов для вызова.</span><span class="sxs-lookup"><span data-stu-id="e3a57-133">The application should examine the **CalledID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo), and use the [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) function to provide a new dialable address for the call.</span></span> <span data-ttu-id="e3a57-134">Если вместо этого вызов будет заблокирован, приложение может вызвать [**линедроп**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="e3a57-134">If the call is to be blocked instead, the application may call [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span></span> <span data-ttu-id="e3a57-135">Если приложению не удается выполнить действие в течение определенного времени ожидания, будет предпринято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3a57-135">If the application fails to take action within a switch-defined timeout period, a default action will be taken.</span></span> <span data-ttu-id="e3a57-136">Поставщик услуг может использовать эту константу только в том случае, если согласованная версия в строке 2,0 или выше.</span><span class="sxs-lookup"><span data-stu-id="e3a57-136">A service provider can use this constant only if the negotiated version on the line is 2.0 or higher.</span></span> <span data-ttu-id="e3a57-137">В противном случае поставщик услуг должен заменить ЛИНЕКАЛЛРЕАСОН \_ .</span><span class="sxs-lookup"><span data-stu-id="e3a57-137">Otherwise the service provider should substitute LINECALLREASON\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**\_Перенос линекаллреасон**</span><span class="sxs-lookup"><span data-stu-id="e3a57-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-139">Вызов был передан из другого числа.</span><span class="sxs-lookup"><span data-stu-id="e3a57-139">The call has been transferred from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**ЛИНЕКАЛЛРЕАСОН \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="e3a57-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-141">Причина вызова недоступна и не будет известна позже.</span><span class="sxs-lookup"><span data-stu-id="e3a57-141">The reason for the call is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**ЛИНЕКАЛЛРЕАСОН \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="e3a57-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-143">Причина вызова в настоящее время неизвестна, но может быть известна позже.</span><span class="sxs-lookup"><span data-stu-id="e3a57-143">The reason for the call is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3a57-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**\_НЕприпаркованный линекаллреасон**</span><span class="sxs-lookup"><span data-stu-id="e3a57-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3a57-145">Вызов был получен как приостановленный вызов.</span><span class="sxs-lookup"><span data-stu-id="e3a57-145">The call was retrieved as a parked call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3a57-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3a57-146">Remarks</span></span>

<span data-ttu-id="e3a57-147">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="e3a57-147">No extensibility.</span></span> <span data-ttu-id="e3a57-148">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="e3a57-148">All 32 bits are reserved.</span></span>

<span data-ttu-id="e3a57-149">\_Константы линекаллреасон используются в элементе **параметр dwReason** структуры данных [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="e3a57-149">The LINECALLREASON\_ constants are used in the **dwReason** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a57-150">Требования</span><span class="sxs-lookup"><span data-stu-id="e3a57-150">Requirements</span></span>



| <span data-ttu-id="e3a57-151">Требование</span><span class="sxs-lookup"><span data-stu-id="e3a57-151">Requirement</span></span> | <span data-ttu-id="e3a57-152">Значение</span><span class="sxs-lookup"><span data-stu-id="e3a57-152">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e3a57-153">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e3a57-153">TAPI version</span></span><br/> | <span data-ttu-id="e3a57-154">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e3a57-154">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e3a57-155">Header</span><span class="sxs-lookup"><span data-stu-id="e3a57-155">Header</span></span><br/>       | <dl> <span data-ttu-id="e3a57-156"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a57-156"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a57-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3a57-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a57-158">**линекаллинфо**</span><span class="sxs-lookup"><span data-stu-id="e3a57-158">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="e3a57-159">**линедроп**</span><span class="sxs-lookup"><span data-stu-id="e3a57-159">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="e3a57-160">**линередирект**</span><span class="sxs-lookup"><span data-stu-id="e3a57-160">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[<span data-ttu-id="e3a57-161">**линесвафолд**</span><span class="sxs-lookup"><span data-stu-id="e3a57-161">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




