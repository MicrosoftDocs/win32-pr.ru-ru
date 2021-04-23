---
description: '\_Константы побитового флага линедисконнектмоде описывают различные причины для удаленного запроса на отключение. Режим отключения становится доступным в качестве состояния вызова приложения после перехода состояния вызова в состояние DISCONNECTED (отключено).'
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: Константы LINEDISCONNECTMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689226"
---
# <a name="linedisconnectmode_-constants"></a><span data-ttu-id="8d694-104">\_Константы линедисконнектмоде</span><span class="sxs-lookup"><span data-stu-id="8d694-104">LINEDISCONNECTMODE\_ Constants</span></span>

<span data-ttu-id="8d694-105">Константы побитового флага **линедисконнектмоде \_** описывают различные причины для удаленного запроса на отключение.</span><span class="sxs-lookup"><span data-stu-id="8d694-105">The **LINEDISCONNECTMODE\_** bit-flag constants describe different reasons for a remote disconnect request.</span></span> <span data-ttu-id="8d694-106">Режим отключения становится доступным в качестве состояния вызова приложения после перехода состояния вызова в состояние DISCONNECTED (отключено).</span><span class="sxs-lookup"><span data-stu-id="8d694-106">A disconnect mode is available as call status to the application after the call state transitions to disconnected.</span></span>

<dl> <dt>

<span data-ttu-id="8d694-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ бададдресс**</span><span class="sxs-lookup"><span data-stu-id="8d694-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE\_BADADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-108">Недопустимый адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="8d694-108">The destination address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ заблокирована**</span><span class="sxs-lookup"><span data-stu-id="8d694-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-110">Не удалось подключить вызов, так как вызовы с адреса источника не принимаются по адресу назначения.</span><span class="sxs-lookup"><span data-stu-id="8d694-110">The call could not be connected because calls from the origination address are not being accepted at the destination address.</span></span> <span data-ttu-id="8d694-111">Это отличается от ЛИНЕДИСКОННЕКТМОДЕ \_ отклонения в этой блокировке, реализованной в сети (пассивный отклонный), а отклонение реализовано в целевом оборудовании (активное отклонение).</span><span class="sxs-lookup"><span data-stu-id="8d694-111">This differs from LINEDISCONNECTMODE\_REJECT in that blocking is implemented in the network (a passive reject) while a rejection is implemented in the destination equipment (an active reject).</span></span> <span data-ttu-id="8d694-112">Блокировка может быть вызвана конкретным исключением адреса происхождения или тем, что назначение принимает вызовы только из выбранного набора адресов происхождения (закрытая группа пользователей).</span><span class="sxs-lookup"><span data-stu-id="8d694-112">The blocking can be due to a specific exclusion of the origination address, or because the destination accepts calls from only a selected set of origination address (closed user group).</span></span> <span data-ttu-id="8d694-113">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="8d694-113">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="8d694-114">\_Заблокированный линедисконнектмоде подходит как ответ добавлен.</span><span class="sxs-lookup"><span data-stu-id="8d694-114">LINEDISCONNECTMODE\_BLOCKED is appropriate as a blocklisted response.</span></span> <span data-ttu-id="8d694-115">Например, модем получил ответ, пропустил более шести секунд без обнаружения звонка, не смог подключиться определенное количество раз, определяет, что номер телефона не является допустимым для вызова, и выдает ответ "добавлен".</span><span class="sxs-lookup"><span data-stu-id="8d694-115">For example, a modem has received an answer, gone more than six seconds without detecting Ringback, failed to connect a defined number of times, determines that the phone number is not valid to call, and issues a 'blocklisted' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ занят**</span><span class="sxs-lookup"><span data-stu-id="8d694-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-117">Станция удаленного пользователя занята.</span><span class="sxs-lookup"><span data-stu-id="8d694-117">The remote user's station is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ отменена**</span><span class="sxs-lookup"><span data-stu-id="8d694-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-119">Вызов отменен.</span><span class="sxs-lookup"><span data-stu-id="8d694-119">The call was cancelled.</span></span> <span data-ttu-id="8d694-120">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="8d694-120">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**\_перегрузка линедисконнектмоде**</span><span class="sxs-lookup"><span data-stu-id="8d694-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**LINEDISCONNECTMODE\_CONGESTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-122">Сеть перегружена.</span><span class="sxs-lookup"><span data-stu-id="8d694-122">The network is congested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ донотдистурб**</span><span class="sxs-lookup"><span data-stu-id="8d694-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE\_DONOTDISTURB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-124">Не удалось подключить вызов, так как в назначении вызвана функция "не беспокоить".</span><span class="sxs-lookup"><span data-stu-id="8d694-124">The call could not be connected because the destination has invoked the Do Not Disturb feature.</span></span> <span data-ttu-id="8d694-125">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="8d694-125">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ перенаправлено**</span><span class="sxs-lookup"><span data-stu-id="8d694-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-127">Вызов перенаправлен параметром.</span><span class="sxs-lookup"><span data-stu-id="8d694-127">The call was forwarded by the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**\_несовместимые линедисконнектмоде**</span><span class="sxs-lookup"><span data-stu-id="8d694-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-129">Оборудование устройства удаленного пользователя несовместимо с типом запрошенного вызова.</span><span class="sxs-lookup"><span data-stu-id="8d694-129">The remote user's station equipment is incompatible with the type of call requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**\_ответ линедисконнектмоде**</span><span class="sxs-lookup"><span data-stu-id="8d694-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE\_NOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-131">Станция удаленного пользователя не отвечает.</span><span class="sxs-lookup"><span data-stu-id="8d694-131">The remote user's station does not answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ нодиалтоне**</span><span class="sxs-lookup"><span data-stu-id="8d694-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE\_NODIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-133">В течение времени ожидания, заданного поставщиком услуг, не был обнаружен гудок в момент, когда ожидается, что он ожидался (например, "W" в строке с возможностью набора номера).</span><span class="sxs-lookup"><span data-stu-id="8d694-133">A dial tone was not detected within a service-provider defined timeout, at a point during dialing when one was expected (such as at a "W" in the dialable string).</span></span> <span data-ttu-id="8d694-134">Это также может произойти без времени ожидания, определенного поставщиком услуг, или без значения, указанного в элементе **двваитфордиалтоне** структуры [**линедиалпарамс**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) .</span><span class="sxs-lookup"><span data-stu-id="8d694-134">This can also occur without a service-provider-defined timeout period or without a value specified in the **dwWaitForDialTone** member of the [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) structure.</span></span> <span data-ttu-id="8d694-135">(TAPI версии 1,4 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="8d694-135">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**ЛИНЕДИСКОННЕКТМОДЕ, \_ Обычная**</span><span class="sxs-lookup"><span data-stu-id="8d694-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-137">Это Стандартный запрос на отключение от удаленной стороны.</span><span class="sxs-lookup"><span data-stu-id="8d694-137">This is a normal disconnect request by the remote party.</span></span> <span data-ttu-id="8d694-138">Вызов был прерван обычным образом.</span><span class="sxs-lookup"><span data-stu-id="8d694-138">The call was terminated normally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ нумберчанжед**</span><span class="sxs-lookup"><span data-stu-id="8d694-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE\_NUMBERCHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-140">Не удалось подключить вызов, так как номер назначения был изменен, но автоматическое перенаправление на новый номер не предоставлено.</span><span class="sxs-lookup"><span data-stu-id="8d694-140">The call could not be connected because the destination number has been changed, but automatic redirection to the new number is not provided.</span></span> <span data-ttu-id="8d694-141">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="8d694-141">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ аутофордер**</span><span class="sxs-lookup"><span data-stu-id="8d694-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE\_OUTOFORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-143">Вызов не может быть подключен или был отключен, так как конечное устройство не находится в порядке (сбой оборудования).</span><span class="sxs-lookup"><span data-stu-id="8d694-143">The call could not be connected or was disconnected because the destination device is out of order (hardware failure).</span></span> <span data-ttu-id="8d694-144">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="8d694-144">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**\_Отправка линедисконнектмоде**</span><span class="sxs-lookup"><span data-stu-id="8d694-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-146">Вызов был получен из другого места.</span><span class="sxs-lookup"><span data-stu-id="8d694-146">The call was picked up from elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ косунаваил**</span><span class="sxs-lookup"><span data-stu-id="8d694-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE\_QOSUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-148">Вызов не может быть подключен или был отключен, так как не удалось получить или поддерживать минимальное качество обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8d694-148">The call could not be connected or was disconnected because the minimum quality of service could not be obtained or sustained.</span></span> <span data-ttu-id="8d694-149">Это отличается от ЛИНЕДИСКОННЕКТМОДЕ \_ несовместимым в том, что недостаток ресурсов может быть временным условием в назначении.</span><span class="sxs-lookup"><span data-stu-id="8d694-149">This differs from LINEDISCONNECTMODE\_INCOMPATIBLE in that the lack of resources may be a temporary condition at the destination.</span></span> <span data-ttu-id="8d694-150">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="8d694-150">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**\_отклонить линедисконнектмоде**</span><span class="sxs-lookup"><span data-stu-id="8d694-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE\_REJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-152">Удаленный пользователь отклонил вызов.</span><span class="sxs-lookup"><span data-stu-id="8d694-152">The remote user has rejected the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ темпфаилуре**</span><span class="sxs-lookup"><span data-stu-id="8d694-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE\_TEMPFAILURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-154">Вызов не может быть подключен или был отключен из-за временной ошибки в сети; вызов может быть повторен позже, и в конечном итоге ожидается завершение.</span><span class="sxs-lookup"><span data-stu-id="8d694-154">The call could not be connected or was disconnected because of a temporary failure in the network; the call can be reattempted later and is expected to eventually complete.</span></span> <span data-ttu-id="8d694-155">(TAPI версии 2,0 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="8d694-155">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="8d694-156">ЛИНЕДИСКОННЕКТМОДЕ \_ темпфаилуре подходит как отложенный ответ.</span><span class="sxs-lookup"><span data-stu-id="8d694-156">LINEDISCONNECTMODE\_TEMPFAILURE is appropriate as a delayed response.</span></span> <span data-ttu-id="8d694-157">Например, модем, получивший сигнал занятости или эквивалентный ему слишком много раз за определенный период времени, завершает, что номер не должен вызываться повторно, пока не истечет определенное время и не выдаст ответ "DELAYED".</span><span class="sxs-lookup"><span data-stu-id="8d694-157">For example, a modem getting a busy signal or equivalent too many times in a particular time period concludes that the number should not be called again until a defined time has elapsed and issues a 'delayed' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="8d694-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-159">Причина отключения недоступна и не будет известна позже.</span><span class="sxs-lookup"><span data-stu-id="8d694-159">The reason for the disconnect is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="8d694-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-161">Причина запроса на отключение неизвестна, но может быть известна позже.</span><span class="sxs-lookup"><span data-stu-id="8d694-161">The reason for the disconnect request is unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8d694-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**ЛИНЕДИСКОННЕКТМОДЕ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="8d694-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8d694-163">Не удалось подключиться к удаленному пользователю.</span><span class="sxs-lookup"><span data-stu-id="8d694-163">The remote user could not be reached.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d694-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d694-164">Remarks</span></span>

<span data-ttu-id="8d694-165">Старшие 16 бит можно назначить для расширений для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="8d694-165">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="8d694-166">16 младших разрядов зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="8d694-166">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="8d694-167">Удаленный запрос на отключение для данного вызова приводит к переходу состояния вызова в состояние DISCONNECTED, а сообщение [**Line \_ каллстате**](line-callstate.md) отправляется в приложение.</span><span class="sxs-lookup"><span data-stu-id="8d694-167">A remote disconnect request for a given call results in the call state transitioning to the disconnected state and a [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="8d694-168">Сведения о ЛИНЕДИСКОННЕКТМОДЕ \_ содержат сведения об удаленном запросе на отключение.</span><span class="sxs-lookup"><span data-stu-id="8d694-168">The LINEDISCONNECTMODE\_ information provides details about the remote disconnect request.</span></span> <span data-ttu-id="8d694-169">Он доступен в структуре [**линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) вызова, когда вызов находится в отключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="8d694-169">It is available in the call's [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure when the call is in the disconnected state.</span></span> <span data-ttu-id="8d694-170">Пока вызов находится в этом состоянии, приложению по-прежнему разрешено запрашивать сведения о вызове и его состояние.</span><span class="sxs-lookup"><span data-stu-id="8d694-170">While a call is in this state, the application is still allowed to query the call's information and status.</span></span> <span data-ttu-id="8d694-171">Например, доступна информация о пользователях, получаемая как часть удаленного отключения.</span><span class="sxs-lookup"><span data-stu-id="8d694-171">For example, user-user information that is received as part of the remote disconnect is available then.</span></span> <span data-ttu-id="8d694-172">Приложение может очистить отключенный вызов, удалив вызов.</span><span class="sxs-lookup"><span data-stu-id="8d694-172">The application can clear a disconnected call by dropping the call.</span></span>

<span data-ttu-id="8d694-173">Для обеспечения обратной совместимости поставщик услуг должен проверить согласованную версию API в строке и не использовать это значение ЛИНЕДИСКОННЕКТМОДЕ, \_ если оно не поддерживается в согласованной версии ( \_ \_ вместо этого можно использовать линедисконнектмоде "Обычная" или "Неизвестная").</span><span class="sxs-lookup"><span data-stu-id="8d694-173">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEDISCONNECTMODE\_ value if it is not supported on the negotiated version (LINEDISCONNECTMODE\_NORMAL or \_UNKNOWN could be used instead).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d694-174">Требования</span><span class="sxs-lookup"><span data-stu-id="8d694-174">Requirements</span></span>



| <span data-ttu-id="8d694-175">Требование</span><span class="sxs-lookup"><span data-stu-id="8d694-175">Requirement</span></span> | <span data-ttu-id="8d694-176">Значение</span><span class="sxs-lookup"><span data-stu-id="8d694-176">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8d694-177">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8d694-177">TAPI version</span></span><br/> | <span data-ttu-id="8d694-178">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8d694-178">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8d694-179">Header</span><span class="sxs-lookup"><span data-stu-id="8d694-179">Header</span></span><br/>       | <dl> <span data-ttu-id="8d694-180"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d694-180"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d694-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d694-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d694-182">**Строка \_ каллстате**</span><span class="sxs-lookup"><span data-stu-id="8d694-182">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="8d694-183">**линекаллстатус**</span><span class="sxs-lookup"><span data-stu-id="8d694-183">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="8d694-184">**линедиалпарамс**</span><span class="sxs-lookup"><span data-stu-id="8d694-184">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




