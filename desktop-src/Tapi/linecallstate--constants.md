---
description: '\_Константы побитового флага линекаллстате описывают состояния вызовов, которые могут быть в вызове.'
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: Константы LINECALLSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675675"
---
# <a name="linecallstate_-constants"></a><span data-ttu-id="38195-103">\_Константы линекаллстате</span><span class="sxs-lookup"><span data-stu-id="38195-103">LINECALLSTATE\_ Constants</span></span>

<span data-ttu-id="38195-104">Константы побитового флага **линекаллстате \_** описывают состояния вызовов, которые могут быть в вызове.</span><span class="sxs-lookup"><span data-stu-id="38195-104">The **LINECALLSTATE\_** bit-flag constants describe the call states a call can be in.</span></span>

<dl> <dt>

<span data-ttu-id="38195-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**ЛИНЕКАЛЛСТАТЕ \_ принято**</span><span class="sxs-lookup"><span data-stu-id="38195-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-106">Вызов был в состоянии предложения и принят.</span><span class="sxs-lookup"><span data-stu-id="38195-106">The call was in the offering state and has been accepted.</span></span> <span data-ttu-id="38195-107">Это означает другие (наблюдение) приложения, за которые текущее приложение-владелец запросили ответственность за ответ на вызов.</span><span class="sxs-lookup"><span data-stu-id="38195-107">This indicates to other (monitoring) applications that the current owner application has claimed responsibility for answering the call.</span></span> <span data-ttu-id="38195-108">В ISDN принятое состояние указывается, когда вызываемое оборудование отправляет на коммутатор сообщение, указывающее, что он готов представлять вызов вызываемого человека.</span><span class="sxs-lookup"><span data-stu-id="38195-108">In ISDN, the accepted state is entered when the called-party equipment sends a message to the switch indicating that it is willing to present the call to the called person.</span></span> <span data-ttu-id="38195-109">Это оказывает побочный результат (звонок) пользователям на обоих концах вызова.</span><span class="sxs-lookup"><span data-stu-id="38195-109">This has the side effect of alerting (ringing) the users at both ends of the call.</span></span> <span data-ttu-id="38195-110">На входящий вызов всегда можно ответить немедленно, без предварительного принятия по отдельности.</span><span class="sxs-lookup"><span data-stu-id="38195-110">An incoming call can always be immediately answered without first being separately accepted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**ЛИНЕКАЛЛСТАТЕ \_ занят**</span><span class="sxs-lookup"><span data-stu-id="38195-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-112">Вызов получает сигнал о занятости.</span><span class="sxs-lookup"><span data-stu-id="38195-112">The call is receiving a busy tone.</span></span> <span data-ttu-id="38195-113">Сигнал «занято» указывает на то, что звонок не может быть выполнен либо на канале (магистральном), либо на станции удаленной стороны.</span><span class="sxs-lookup"><span data-stu-id="38195-113">A busy tone indicates that the call cannot be completed either a circuit (trunk) or the remote party's station are in use.</span></span> <span data-ttu-id="38195-114">См. раздел [**\_ константы линебусимоде**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="38195-114">See [**LINEBUSYMODE\_ Constants**](linebusymode--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**ЛИНЕКАЛЛСТАТЕ \_ Конференция**</span><span class="sxs-lookup"><span data-stu-id="38195-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE\_CONFERENCED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-116">Вызов является членом Конференции и логически находится в подключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="38195-116">The call is a member of a conference call and is logically in the connected state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**ЛИНЕКАЛЛСТАТЕ \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="38195-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-118">Был установлен вызов и установлено соединение.</span><span class="sxs-lookup"><span data-stu-id="38195-118">The call has been established and the connection is made.</span></span> <span data-ttu-id="38195-119">Информация может передаваться по вызову между исходным адресом и адресом назначения.</span><span class="sxs-lookup"><span data-stu-id="38195-119">Information is able to flow over the call between the originating address and the destination address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**ЛИНЕКАЛЛСТАТЕ \_ набора**</span><span class="sxs-lookup"><span data-stu-id="38195-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE\_DIALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-121">Инициатор набирает цифры в вызове.</span><span class="sxs-lookup"><span data-stu-id="38195-121">The originator is dialing digits on the call.</span></span> <span data-ttu-id="38195-122">Номера набираемых цифр собираются параметром.</span><span class="sxs-lookup"><span data-stu-id="38195-122">The dialed digits are collected by the switch.</span></span> <span data-ttu-id="38195-123">Обратите внимание, что ни [**линеженератедигитс**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) , ни [**тспи \_ линеженератедигитс**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) не поместит строку в состояние набора.</span><span class="sxs-lookup"><span data-stu-id="38195-123">Note that neither [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) nor [**TSPI\_lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) will place the line into the dialing state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**ЛИНЕКАЛЛСТАТЕ \_ диалтоне**</span><span class="sxs-lookup"><span data-stu-id="38195-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-125">Вызов получает гудок из параметра, что означает, что коммутатор готов к получению номера телефона.</span><span class="sxs-lookup"><span data-stu-id="38195-125">The call is receiving a dial tone from the switch, which means that the switch is ready to receive a dialed number.</span></span> <span data-ttu-id="38195-126">См. раздел [**\_ константы линедиалтонемоде**](linedialtonemode--constants.md) для идентификаторов специальных тонов, например перебои сигнала обычной электронной почты.</span><span class="sxs-lookup"><span data-stu-id="38195-126">See [**LINEDIALTONEMODE\_ Constants**](linedialtonemode--constants.md) for identifiers of special dial tones, such as a stutter tone of normal voice mail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**ЛИНЕКАЛЛСТАТЕ \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="38195-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-128">Удаленная сторона отключилась от вызова.</span><span class="sxs-lookup"><span data-stu-id="38195-128">The remote party has disconnected from the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**ЛИНЕКАЛЛСТАТЕ \_ бездействие**</span><span class="sxs-lookup"><span data-stu-id="38195-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-130">Вызов существует, но не был подключен.</span><span class="sxs-lookup"><span data-stu-id="38195-130">The call exists but has not been connected.</span></span> <span data-ttu-id="38195-131">В вызове не существует действий, что означает, что ни один из вызовов в данный момент не активен.</span><span class="sxs-lookup"><span data-stu-id="38195-131">No activity exists on the call, which means that no call is currently active.</span></span> <span data-ttu-id="38195-132">Вызов никогда не может выходить из состояния простоя.</span><span class="sxs-lookup"><span data-stu-id="38195-132">A call can never transition out of the idle state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**\_предложение линекаллстате**</span><span class="sxs-lookup"><span data-stu-id="38195-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**LINECALLSTATE\_OFFERING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-134">Вызов предоставляется станции и сообщает о поступлении нового звонка.</span><span class="sxs-lookup"><span data-stu-id="38195-134">The call is being offered to the station, signaling the arrival of a new call.</span></span> <span data-ttu-id="38195-135">Состояние предложения не совпадает с вызовом телефона или компьютера для звонка.</span><span class="sxs-lookup"><span data-stu-id="38195-135">The offering state is not the same as causing a phone or computer to ring.</span></span> <span data-ttu-id="38195-136">В некоторых средах вызов в состоянии предложения не вызывает пользователя до тех пор, пока параметр не предписывает линии на звонок.</span><span class="sxs-lookup"><span data-stu-id="38195-136">In some environments, a call in the offering state does not ring the user until the switch instructs the line to ring.</span></span> <span data-ttu-id="38195-137">В качестве примера можно привести, где входящий вызов отображается в нескольких наборах станций, но только с основными кольцами адресов.</span><span class="sxs-lookup"><span data-stu-id="38195-137">An example use might be where an incoming call appears on several station sets but only the primary address rings.</span></span> <span data-ttu-id="38195-138">Инструкция для звонка не влияет на состояние вызова.</span><span class="sxs-lookup"><span data-stu-id="38195-138">The instruction to ring does not affect any call states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**ЛИНЕКАЛЛСТАТЕ \_**</span><span class="sxs-lookup"><span data-stu-id="38195-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE\_ONHOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-140">Вызов удерживается коммутатором.</span><span class="sxs-lookup"><span data-stu-id="38195-140">The call is on hold by the switch.</span></span> <span data-ttu-id="38195-141">Это освобождает физическую строку, которая позволяет другому вызову использовать строку.</span><span class="sxs-lookup"><span data-stu-id="38195-141">This frees the physical line, which allows another call to use the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**ЛИНЕКАЛЛСТАТЕ \_ онхолдпендконф**</span><span class="sxs-lookup"><span data-stu-id="38195-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE\_ONHOLDPENDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-143">Вызов сейчас удерживается, пока он добавляется на конференцию.</span><span class="sxs-lookup"><span data-stu-id="38195-143">The call is currently on hold while it is being added to a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**ЛИНЕКАЛЛСТАТЕ \_ онхолдпендтрансфер**</span><span class="sxs-lookup"><span data-stu-id="38195-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE\_ONHOLDPENDTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-145">Вызов сейчас находится в состоянии ожидания перемещения в другое число.</span><span class="sxs-lookup"><span data-stu-id="38195-145">The call is currently on hold awaiting transfer to another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**\_продолжение линекаллстате**</span><span class="sxs-lookup"><span data-stu-id="38195-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE\_PROCEEDING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-147">Набор номера завершен, и вызов проходит через коммутатор или телефонную сеть.</span><span class="sxs-lookup"><span data-stu-id="38195-147">Dialing has completed and the call is proceeding through the switch or telephone network.</span></span> <span data-ttu-id="38195-148">Это происходит после завершения набора номера и до того, как вызов достигнет вызываемой стороны, как указано в звонка, занятии или ответе.</span><span class="sxs-lookup"><span data-stu-id="38195-148">This occurs after dialing is complete and before the call reaches the dialed party, as indicated by ringback, busy, or answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**ЛИНЕКАЛЛСТАТЕ \_ звонка**</span><span class="sxs-lookup"><span data-stu-id="38195-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-150">Была достигнута вызываемая станция, а параметр назначения — генерация сигнала кольца обратно к инициатору.</span><span class="sxs-lookup"><span data-stu-id="38195-150">The station to be called has been reached, and the destination's switch is generating a ring tone back to the originator.</span></span> <span data-ttu-id="38195-151">*Звонка* означает, что адрес назначения будет оповещен о вызове.</span><span class="sxs-lookup"><span data-stu-id="38195-151">A *ringback* means that the destination address is being alerted to the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**ЛИНЕКАЛЛСТАТЕ \_ спеЦиалинфо**</span><span class="sxs-lookup"><span data-stu-id="38195-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE\_SPECIALINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-153">Вызов получает специальный информационный сигнал, который предшествует предзаписанному объявлению, указывающему, почему не удается завершить вызов.</span><span class="sxs-lookup"><span data-stu-id="38195-153">The call is receiving a special information signal, which precedes a prerecorded announcement indicating why a call cannot be completed.</span></span> <span data-ttu-id="38195-154">См. раздел [**\_ константы линеспеЦиалинфо**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="38195-154">See [**LINESPECIALINFO\_ Constants**](linespecialinfo--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="38195-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**ЛИНЕКАЛЛСТАТЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="38195-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="38195-156">Вызов существует, но его состояние в настоящее время неизвестно.</span><span class="sxs-lookup"><span data-stu-id="38195-156">The call exists, but its state is currently unknown.</span></span> <span data-ttu-id="38195-157">Это может быть результатом обнаружения неудовлетворительного состояния вызова поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="38195-157">This may be the result of poor call progress detection by the service provider.</span></span> <span data-ttu-id="38195-158">Также может быть сформировано сообщение о состоянии вызова с состоянием вызова "неизвестно", чтобы сообщить библиотеке DLL TAPI о новом вызове в момент, когда фактическое состояние вызова вызова не полностью известно.</span><span class="sxs-lookup"><span data-stu-id="38195-158">A call state message with the call state set to unknown may also be generated to inform the TAPI DLL about a new call at a time when the actual call state of the call is not exactly known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38195-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38195-159">Remarks</span></span>

<span data-ttu-id="38195-160">Старшие 8 битов могут определять подсостояние конкретного устройства для любого из предопределенных состояний при условии, что также задан один из битов ЛИНЕКАЛЛСТАТЕ, \_ определенных выше.</span><span class="sxs-lookup"><span data-stu-id="38195-160">The high-order 8 bits can define a device-specific substate of any of the predefined states, provided that one of the LINECALLSTATE\_ bits defined above is also set.</span></span> <span data-ttu-id="38195-161">Младшие 24 бита зарезервированы для предопределенных состояний.</span><span class="sxs-lookup"><span data-stu-id="38195-161">The low-order 24 bits are reserved for predefined states.</span></span>

<span data-ttu-id="38195-162">**\_ Константы линекаллстате** используются в качестве параметров в сообщении [**Line \_ каллстате**](line-callstate.md) , отправляемом в приложение.</span><span class="sxs-lookup"><span data-stu-id="38195-162">The **LINECALLSTATE\_constants** are used as parameters by the [**LINE\_CALLSTATE**](line-callstate.md) message sent to the application.</span></span> <span data-ttu-id="38195-163">Сообщение содержит новое состояние вызова, переданное вызовом.</span><span class="sxs-lookup"><span data-stu-id="38195-163">The message carries the new call state that the call transitioned to.</span></span> <span data-ttu-id="38195-164">Эти константы также используются как члены в структуре [**линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , возвращаемой функцией [**линежеткаллстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) .</span><span class="sxs-lookup"><span data-stu-id="38195-164">These constants are also used as members in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure returned by the [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="38195-165">Требования</span><span class="sxs-lookup"><span data-stu-id="38195-165">Requirements</span></span>



| <span data-ttu-id="38195-166">Требование</span><span class="sxs-lookup"><span data-stu-id="38195-166">Requirement</span></span> | <span data-ttu-id="38195-167">Значение</span><span class="sxs-lookup"><span data-stu-id="38195-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="38195-168">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="38195-168">TAPI version</span></span><br/> | <span data-ttu-id="38195-169">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="38195-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="38195-170">Header</span><span class="sxs-lookup"><span data-stu-id="38195-170">Header</span></span><br/>       | <dl> <span data-ttu-id="38195-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="38195-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38195-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38195-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38195-173">**Строка \_ каллстате**</span><span class="sxs-lookup"><span data-stu-id="38195-173">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="38195-174">**линекаллстатус**</span><span class="sxs-lookup"><span data-stu-id="38195-174">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="38195-175">**линеженератедигитс**</span><span class="sxs-lookup"><span data-stu-id="38195-175">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="38195-176">**линежеткаллстатус**</span><span class="sxs-lookup"><span data-stu-id="38195-176">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

