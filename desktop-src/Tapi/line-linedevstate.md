---
description: '\_Сообщение ЛИНЕДЕВСТАТЕ линии TAPI отправляется при изменении состояния линейного устройства. Приложение может вызвать Линежетлинедевстатус, чтобы определить новое состояние строки.'
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: Сообщение LINE_LINEDEVSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685431"
---
# <a name="line_linedevstate-message"></a><span data-ttu-id="e6aa3-104">Строка \_ сообщения линедевстате</span><span class="sxs-lookup"><span data-stu-id="e6aa3-104">LINE\_LINEDEVSTATE message</span></span>

<span data-ttu-id="e6aa3-105">Сообщение **\_ ЛИНЕДЕВСТАТЕ линии** TAPI отправляется при изменении состояния линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-105">The TAPI **LINE\_LINEDEVSTATE** message is sent when the state of a line device has changed.</span></span> <span data-ttu-id="e6aa3-106">Приложение может вызвать [**линежетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) , чтобы определить новое состояние строки.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-106">The application can invoke [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) to determine the new status of the line.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e6aa3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6aa3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6aa3-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="e6aa3-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e6aa3-109">Маркер устройства линии.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-109">A handle to the line device.</span></span> <span data-ttu-id="e6aa3-110">Этот параметр имеет **значение NULL** , если *dwParam1* — линедевстате \_ reinit.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-110">This parameter is **NULL** when *dwParam1* is LINEDEVSTATE\_REINIT.</span></span>

</dd> <dt>

<span data-ttu-id="e6aa3-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="e6aa3-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e6aa3-112">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-112">The callback instance supplied when opening the line.</span></span> <span data-ttu-id="e6aa3-113">Если параметр *dwParam1* имеет значение ЛИНЕДЕВСТАТЕ \_ reinit, то параметр *двкаллбаккинстанце* является недопустимым и имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-113">If the *dwParam1* parameter is LINEDEVSTATE\_REINIT, the *dwCallbackInstance* parameter is not valid and is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e6aa3-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e6aa3-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e6aa3-115">Элемент состояния линейного устройства, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-115">The line device status item that has changed.</span></span> <span data-ttu-id="e6aa3-116">Параметр может быть одной или несколькими [**\_ константами линедевстате**](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="e6aa3-116">The parameter can be one or more of the [**LINEDEVSTATE\_ constants**](linedevstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6aa3-117">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e6aa3-117">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e6aa3-118">Интерпретация этого параметра зависит от значения *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-118">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="e6aa3-119">Если *dwParam1* — линедевстате \_ Ring, *dwParam2* содержит режим Ring, с помощью которого параметр указывает линии на звонок.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-119">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam2* contains the ring mode with which the switch instructs the line to ring.</span></span> <span data-ttu-id="e6aa3-120">Допустимые режимы звонка — это числа в диапазоне от 1 до **двнумрингмодес**, где **двнумрингмодес** является возможностью линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-120">Valid ring modes are numbers in the range one to **dwNumRingModes**, where **dwNumRingModes** is a line device capability.</span></span>

<span data-ttu-id="e6aa3-121">Если *dwParam1* имеет значение ЛИНЕДЕВСТАТЕ \_ reinit, и сообщение было выдано TAPI в результате перевода нового сообщения API в сообщение о повторной инициализации, *dwParam2* содержит параметр *Двмсг* исходного сообщения (например, [**строку \_ CREATE**](line-create.md) или Line \_ линедевстате).</span><span class="sxs-lookup"><span data-stu-id="e6aa3-121">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam2* contains the *dwMsg* parameter of the original message (for example, [**LINE\_CREATE**](line-create.md) or LINE\_LINEDEVSTATE).</span></span> <span data-ttu-id="e6aa3-122">Если значение *dwParam2* равно нулю, это означает, что сообщение о переинициализации является "реальным" сообщением о переинициализации, которое требует, чтобы приложение вызывало [**линешутдовн**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) на самом раннем удобство.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-122">If *dwParam2* is zero, this indicates that the REINIT message is a "real" REINIT message that requires the application to call [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) at its earliest convenience.</span></span>

</dd> <dt>

<span data-ttu-id="e6aa3-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e6aa3-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e6aa3-124">Интерпретация этого параметра зависит от значения *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-124">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="e6aa3-125">Если *dwParam1* — линедевстате \_ Звонок, *dwParam3* содержит число колец для этого события кольца.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-125">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam3* contains the ring count for this ring event.</span></span> <span data-ttu-id="e6aa3-126">Число звонков начинается с нуля.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-126">The ring count starts at zero.</span></span>

<span data-ttu-id="e6aa3-127">Если *dwParam1* имеет значение ЛИНЕДЕВСТАТЕ \_ reinit, и сообщение было выдано TAPI в результате перевода нового сообщения API в сообщение о повторной инициализации, *dwParam3* содержит параметр *DWPARAM1* исходного сообщения (например, линедевстате \_ транслатечанже или другое \_ значение линедевстате, если *dwParam2* — Line \_ Линедевстате, или новый идентификатор устройства, если *dwParam2* — это [**\_ Создание строки**](line-create.md)).</span><span class="sxs-lookup"><span data-stu-id="e6aa3-127">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam3* contains the *dwParam1* parameter of the original message (for example, LINEDEVSTATE\_TRANSLATECHANGE or some other LINEDEVSTATE\_ value, if *dwParam2* is LINE\_LINEDEVSTATE, or the new device identifier, if *dwParam2* is [**LINE\_CREATE**](line-create.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6aa3-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6aa3-128">Return value</span></span>

<span data-ttu-id="e6aa3-129">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-129">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6aa3-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6aa3-130">Remarks</span></span>

<span data-ttu-id="e6aa3-131">Отправкой сообщения **Line \_ линедевстате** можно управлять с помощью [**линесетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="e6aa3-131">The sending of the **LINE\_LINEDEVSTATE** message can be controlled with [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="e6aa3-132">Приложение может указывать на изменения элементов состояния, о которых требуется получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-132">An application can indicate status item changes about which it wants to be notified.</span></span> <span data-ttu-id="e6aa3-133">По умолчанию все отчеты о состоянии отключены, за исключением ЛИНЕДЕВСТАТЕ \_ reinit, которые не могут быть отключены.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-133">By default, all status reporting is disabled except for LINEDEVSTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="e6aa3-134">Это сообщение отправляется всем приложениям, имеющим в строке маркер, включая те, которые вызвали [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) с параметром *двпривилежес* , для которого задано значение линекаллпривилеже \_ None, линекаллпривилеже \_ owner, линекаллпривилеже \_ Monitor или разрешенные сочетания.</span><span class="sxs-lookup"><span data-stu-id="e6aa3-134">This message is sent to all applications that have a handle to the line, including those that called [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) with the *dwPrivileges* parameter set to LINECALLPRIVILEGE\_NONE, LINECALLPRIVILEGE\_OWNER, LINECALLPRIVILEGE\_MONITOR, or permitted combinations of these.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6aa3-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e6aa3-135">Requirements</span></span>



| <span data-ttu-id="e6aa3-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e6aa3-136">Requirement</span></span> | <span data-ttu-id="e6aa3-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e6aa3-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e6aa3-138">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e6aa3-138">TAPI version</span></span><br/> | <span data-ttu-id="e6aa3-139">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e6aa3-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e6aa3-140">Header</span><span class="sxs-lookup"><span data-stu-id="e6aa3-140">Header</span></span><br/>       | <dl> <span data-ttu-id="e6aa3-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6aa3-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6aa3-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6aa3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6aa3-143">**\_закрыть строку**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-143">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="e6aa3-144">**\_Создание строки**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-144">**LINE\_CREATE**</span></span>](line-create.md)
</dt> <dt>

[<span data-ttu-id="e6aa3-145">**линедевкапс**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-145">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="e6aa3-146">**линежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-146">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="e6aa3-147">**линежетдевконфиг**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-147">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="e6aa3-148">**линежеттранслатекапс**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-148">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="e6aa3-149">**линеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-149">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="e6aa3-150">**линеопен**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-150">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="e6aa3-151">**линесетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-151">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="e6aa3-152">**линешутдовн**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-152">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[<span data-ttu-id="e6aa3-153">**линетранслатекапс**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-153">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="e6aa3-154">**линеункомплетекалл**</span><span class="sxs-lookup"><span data-stu-id="e6aa3-154">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




