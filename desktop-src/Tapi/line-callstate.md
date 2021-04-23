---
description: '\_Сообщение КАЛЛСТАТЕ линии TAPI отправляется при изменении состояния указанного вызова.'
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: Сообщение LINE_CALLSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675397"
---
# <a name="line_callstate-message"></a><span data-ttu-id="9a689-103">Строка \_ сообщения каллстате</span><span class="sxs-lookup"><span data-stu-id="9a689-103">LINE\_CALLSTATE message</span></span>

<span data-ttu-id="9a689-104">Сообщение **\_ КАЛЛСТАТЕ линии** TAPI отправляется при изменении состояния указанного вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-104">The TAPI **LINE\_CALLSTATE** message is sent when the status of the specified call has changed.</span></span> <span data-ttu-id="9a689-105">Как правило, несколько таких сообщений получаются в течение времени существования вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-105">Typically, several such messages are received during the lifetime of a call.</span></span> <span data-ttu-id="9a689-106">Приложения получают уведомления о новых входящих вызовах с помощью этого сообщения; новый вызов находится в состоянии *предложения* .</span><span class="sxs-lookup"><span data-stu-id="9a689-106">Applications are notified of new incoming calls with this message; the new call is in the *offering* state.</span></span> <span data-ttu-id="9a689-107">Приложение может использовать [**линежеткаллстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) для получения более подробных сведений о текущем состоянии вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-107">The application can use [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) to retrieve more detailed information about the current status of the call.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="9a689-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a689-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a689-109">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="9a689-109">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9a689-110">Маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-110">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="9a689-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="9a689-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="9a689-112">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-112">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="9a689-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="9a689-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="9a689-114">Новое состояние вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-114">The new call state.</span></span> <span data-ttu-id="9a689-115">Этот параметр должен быть одной и только одной из следующих [**\_ констант линекаллстате**](linecallstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-115">This parameter must be one and only one of the following [**LINECALLSTATE\_ constants**](linecallstate--constants.md).</span></span>



| <span data-ttu-id="9a689-116">dwParam1</span><span class="sxs-lookup"><span data-stu-id="9a689-116">dwParam1</span></span>                                                                                                                                                                                             | <span data-ttu-id="9a689-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9a689-117">Meaning</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <span data-ttu-id="9a689-118"><dt>**ЛИНЕКАЛЛСТАТЕ \_ занят**</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-118"><dt>**LINECALLSTATE\_BUSY**</dt></span></span> </dl>                         | <span data-ttu-id="9a689-119">*dwParam2* содержит сведения о режиме занятости.</span><span class="sxs-lookup"><span data-stu-id="9a689-119">*dwParam2* contains details about the busy mode.</span></span> <span data-ttu-id="9a689-120">Этот параметр использует одну из [**\_ констант линебусимоде**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-120">This parameter uses one of the [**LINEBUSYMODE\_ constants**](linebusymode--constants.md).</span></span><br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <span data-ttu-id="9a689-121"><dt>**ЛИНЕКАЛЛСТАТЕ \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-121"><dt>**LINECALLSTATE\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="9a689-122">*dwParam2* содержит сведения о режиме подключения.</span><span class="sxs-lookup"><span data-stu-id="9a689-122">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="9a689-123">Этот параметр использует одну из [**\_ констант линеконнектедмоде**](lineconnectedmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-123">This parameter uses one of the [**LINECONNECTEDMODE\_ constants**](lineconnectedmode--constants.md).</span></span><br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <span data-ttu-id="9a689-124"><dt>**ЛИНЕКАЛЛСТАТЕ \_ диалтоне**</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-124"><dt>**LINECALLSTATE\_DIALTONE**</dt></span></span> </dl>             | <span data-ttu-id="9a689-125">*dwParam2* содержит сведения о тоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="9a689-125">*dwParam2* contains details about the dial tone mode.</span></span> <span data-ttu-id="9a689-126">Этот параметр использует одну из [**\_ констант линедиалтонемоде**](linedialtonemode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-126">This parameter uses one of the [**LINEDIALTONEMODE\_ constants**](linedialtonemode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <span data-ttu-id="9a689-127"><dt>**\_предложение линекаллстате**</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-127"><dt>**LINECALLSTATE\_OFFERING**</dt></span></span> </dl>             | <span data-ttu-id="9a689-128">*dwParam2* содержит сведения о режиме подключения.</span><span class="sxs-lookup"><span data-stu-id="9a689-128">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="9a689-129">Этот параметр использует одну из [**\_ констант линеофферингмоде**](lineofferingmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-129">This parameter uses one of the [**LINEOFFERINGMODE\_ constants**](lineofferingmode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <span data-ttu-id="9a689-130"><dt>**ЛИНЕКАЛЛСТАТЕ \_ спеЦиалинфо**</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-130"><dt>**LINECALLSTATE\_SPECIALINFO**</dt></span></span> </dl>    | <span data-ttu-id="9a689-131">*dwParam2* содержит сведения о режиме специальных сведений.</span><span class="sxs-lookup"><span data-stu-id="9a689-131">*dwParam2* contains the details about the special information mode.</span></span> <span data-ttu-id="9a689-132">Этот параметр использует одну из [**\_ констант линеспеЦиалинфо**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-132">This parameter uses one of the [**LINESPECIALINFO\_ constants**](linespecialinfo--constants.md).</span></span><br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <span data-ttu-id="9a689-133"><dt>**ЛИНЕКАЛЛСТАТЕ \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-133"><dt>**LINECALLSTATE\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9a689-134">*dwParam2* содержит сведения о режиме отключения.</span><span class="sxs-lookup"><span data-stu-id="9a689-134">*dwParam2* contains details about the disconnect mode.</span></span> <span data-ttu-id="9a689-135">Этот параметр использует одну из [**\_ констант линедисконнектмоде**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-135">This parameter uses one of the [**LINEDISCONNECTMODE\_ constants**](linedisconnectmode--constants.md).</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="9a689-136">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9a689-136">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="9a689-137">Сведения, зависящие от состояния вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-137">Call-state-dependent information.</span></span> <span data-ttu-id="9a689-138">См. *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="9a689-138">See *dwParam1*.</span></span>

> [!Note]  
> <span data-ttu-id="9a689-139">В случаях, когда подходит *отложенный* ответ, используйте линедисконнектмоде \_ темпфаилуре.</span><span class="sxs-lookup"><span data-stu-id="9a689-139">In circumstances where a *delayed* response is appropriate, use LINEDISCONNECTMODE\_TEMPFAILURE.</span></span> <span data-ttu-id="9a689-140">Если подходит ответ *добавлен* , используйте линедисконнект \_ blocked.</span><span class="sxs-lookup"><span data-stu-id="9a689-140">Where a *blocklisted* response is appropriate, use LINEDISCONNECT\_BLOCKED.</span></span> <span data-ttu-id="9a689-141">Дополнительные сведения см. в [**разделе \_ константы линедисконнектмоде**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-141">For further information, see [**LINEDISCONNECTMODE\_ Constants**](linedisconnectmode--constants.md).</span></span>

 

<span data-ttu-id="9a689-142">Если *dwParam1* является Линекаллстате \_ , *dwParam2* содержит параметр *хконфкалл* родительского вызова конференции, участником которой является субъект *хкалл* .</span><span class="sxs-lookup"><span data-stu-id="9a689-142">If *dwParam1* is LINECALLSTATE\_CONFERENCED, *dwParam2* contains the *hConfCall* parameter of the parent call of the conference of which the subject *hCall* is a member.</span></span> <span data-ttu-id="9a689-143">Если вызов, указанный в *dwParam2* , ранее не рассматривался приложением как родительский вызов конференции (*хконфкалл*, приложение должно сделать это в результате этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9a689-143">If the call specified in *dwParam2* was not previously considered by the application to be a parent conference call (*hConfCall*, the application must do so as a result of this message.</span></span> <span data-ttu-id="9a689-144">Если приложение не имеет маркера для родительского вызова конференции (так как ранее он назывался [**линедеаллокатекалл**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) на этом маркере), *DwParam2* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9a689-144">If the application does not have a handle to the parent call of the conference (because it has previously called [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) on that handle) *dwParam2* is set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9a689-145">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="9a689-145">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="9a689-146">Если значение равно нулю, этот параметр указывает на отсутствие изменений в привилегии приложения для вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-146">If zero, this parameter indicates that there has been no change in the application's privilege for the call.</span></span>

<span data-ttu-id="9a689-147">Если не равен нулю, он указывает привилегию приложения для вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-147">If nonzero, it specifies the application's privilege for the call.</span></span> <span data-ttu-id="9a689-148">Это происходит в следующих ситуациях: (1) при первом присвоении приложению маркера этого вызова; (2), если приложение является целью перенаправления вызова (даже если приложение уже было владельцем вызова).</span><span class="sxs-lookup"><span data-stu-id="9a689-148">This occurs in the following situations: (1) The first time that the application is given a handle to this call; (2) When the application is the target of a call handoff (even if the application already was an owner of the call).</span></span> <span data-ttu-id="9a689-149">Этот параметр использует одну из следующих [**\_ констант линекаллпривилеже**](linecallprivilege--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9a689-149">This parameter uses one of the following [**LINECALLPRIVILEGE\_ constants**](linecallprivilege--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a689-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a689-150">Return value</span></span>

<span data-ttu-id="9a689-151">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="9a689-151">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a689-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a689-152">Remarks</span></span>

<span data-ttu-id="9a689-153">Это сообщение отправляется в любое приложение, которое имеет обработчик для вызова.</span><span class="sxs-lookup"><span data-stu-id="9a689-153">This message is sent to any application that has a handle for the call.</span></span> <span data-ttu-id="9a689-154">Сообщение **Line \_ каллстате** также уведомляет приложения, которые отслеживают вызовы в строке о существовании и состоянии исходящих вызовов, установленных другими приложениями, или вручную (например, на подключенном телефонном устройстве).</span><span class="sxs-lookup"><span data-stu-id="9a689-154">The **LINE\_CALLSTATE** message also notifies applications that monitor calls on a line about the existence and state of outbound calls established by other applications or manually by the user (for example, on an attached phone device).</span></span> <span data-ttu-id="9a689-155">Состояние вызова таких вызовов отражает фактическое состояние вызова, которое не является *предложением*.</span><span class="sxs-lookup"><span data-stu-id="9a689-155">The call state of such calls reflects the actual state of the call, which is not *offering*.</span></span> <span data-ttu-id="9a689-156">Изучив состояние вызова, приложение может определить, является ли вызов входящим вызовом, на который необходимо ответить.</span><span class="sxs-lookup"><span data-stu-id="9a689-156">By examining the call state, the application can determine whether the call is an inbound call that needs to be answered or not.</span></span>

<span data-ttu-id="9a689-157">Сообщение **\_ каллстате строки** с неизвестным состоянием вызова может быть отправлено в приложение мониторинга в результате успешного выполнения [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**линефорвард**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**Линеунпарк**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**линесетуптрансфер**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**линесетупконференце**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)или [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) , которые были запрошены другим приложением.</span><span class="sxs-lookup"><span data-stu-id="9a689-157">A **LINE\_CALLSTATE** message with an unknown call state can be sent to a monitoring application as the result of a successful [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference), or [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) that has been requested by another application.</span></span> <span data-ttu-id="9a689-158">В то же время, когда запрашивающее приложение отправило [**\_ ответ строки**](line-reply.md) (успешно) для запрошенной операции, все приложения мониторинга в строке отправляют сообщение **Line \_ каллстате** (неизвестное).</span><span class="sxs-lookup"><span data-stu-id="9a689-158">At the same time that the requesting application is sent a [**LINE\_REPLY**](line-reply.md) (success) for the requested operation, any monitoring applications on the line are sent the **LINE\_CALLSTATE** (unknown) message.</span></span> <span data-ttu-id="9a689-159">В ближайшее время отправляется сообщение **\_ каллстате** , указывающее на фактическое состояние вызова вновь созданного вызова (с использованием сведений, предоставленных поставщиком услуг).</span><span class="sxs-lookup"><span data-stu-id="9a689-159">A **LINE\_CALLSTATE** message indicating the "real" call state of the newly generated call is sent (using information provided by the service provider) to the requesting and monitoring applications shortly thereafter.</span></span>

<span data-ttu-id="9a689-160">**Строка \_ каллстате** (неизвестная) отправляется в мониторинг приложений только в том случае, если [**линекомплететрансфер**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) приводит к тому, что вызовы разрешаются в трехстороннее конференцию.</span><span class="sxs-lookup"><span data-stu-id="9a689-160">A **LINE\_CALLSTATE** (unknown) message is sent to monitoring applications only if [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causes calls to be resolved into a three-way conference.</span></span>

<span data-ttu-id="9a689-161">Для обеспечения обратной совместимости более старые приложения не ожидают какого-либо конкретного значения в *dwParam2* \_ сообщения линекаллстате.</span><span class="sxs-lookup"><span data-stu-id="9a689-161">For backward compatibility, older applications are not expecting any particular value in *dwParam2* of a LINECALLSTATE\_CONFERENCED message.</span></span> <span data-ttu-id="9a689-162">Таким образом, TAPI передает родительский вызов *хконфкалл* в *dwParam2* независимо от версии API приложения, получающего сообщение.</span><span class="sxs-lookup"><span data-stu-id="9a689-162">TAPI therefore passes the parent call *hConfCall* in *dwParam2* regardless of the API version of the application receiving the message.</span></span> <span data-ttu-id="9a689-163">В случае вызова конференции, инициированного поставщиком услуг, старое приложение не знает о том, что родительский вызов стал вызовом конференции, если только не проверит другие сведения (например, вызвать [**линежетконфрелатедкаллс**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span><span class="sxs-lookup"><span data-stu-id="9a689-163">In the case of a conference call initiated by the service provider, the older application is not aware that the parent call has become a conference call unless it happens to spontaneously examine other information (for example, call [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span></span>

<span data-ttu-id="9a689-164">Невозможно отключить это сообщение.</span><span class="sxs-lookup"><span data-stu-id="9a689-164">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a689-165">Требования</span><span class="sxs-lookup"><span data-stu-id="9a689-165">Requirements</span></span>



| <span data-ttu-id="9a689-166">Требование</span><span class="sxs-lookup"><span data-stu-id="9a689-166">Requirement</span></span> | <span data-ttu-id="9a689-167">Значение</span><span class="sxs-lookup"><span data-stu-id="9a689-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9a689-168">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="9a689-168">TAPI version</span></span><br/> | <span data-ttu-id="9a689-169">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9a689-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9a689-170">Header</span><span class="sxs-lookup"><span data-stu-id="9a689-170">Header</span></span><br/>       | <dl> <span data-ttu-id="9a689-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a689-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a689-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a689-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a689-173">**\_ответ строки**</span><span class="sxs-lookup"><span data-stu-id="9a689-173">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="9a689-174">**линекомплететрансфер**</span><span class="sxs-lookup"><span data-stu-id="9a689-174">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="9a689-175">**линедеаллокатекалл**</span><span class="sxs-lookup"><span data-stu-id="9a689-175">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="9a689-176">**линедиалпарамс**</span><span class="sxs-lookup"><span data-stu-id="9a689-176">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[<span data-ttu-id="9a689-177">**линефорвард**</span><span class="sxs-lookup"><span data-stu-id="9a689-177">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="9a689-178">**линеженератедигитс**</span><span class="sxs-lookup"><span data-stu-id="9a689-178">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="9a689-179">**линежеткаллстатус**</span><span class="sxs-lookup"><span data-stu-id="9a689-179">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[<span data-ttu-id="9a689-180">**линежетконфрелатедкаллс**</span><span class="sxs-lookup"><span data-stu-id="9a689-180">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="9a689-181">**линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="9a689-181">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="9a689-182">**линепиккуп**</span><span class="sxs-lookup"><span data-stu-id="9a689-182">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[<span data-ttu-id="9a689-183">**линепрепареаддтоконференце**</span><span class="sxs-lookup"><span data-stu-id="9a689-183">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="9a689-184">**линесетуптрансфер**</span><span class="sxs-lookup"><span data-stu-id="9a689-184">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[<span data-ttu-id="9a689-185">**линеунпарк**</span><span class="sxs-lookup"><span data-stu-id="9a689-185">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




