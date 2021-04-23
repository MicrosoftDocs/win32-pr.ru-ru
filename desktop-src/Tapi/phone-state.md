---
description: TAPI отправляет \_ сообщение о состоянии телефона приложению при каждом изменении состояния телефонного устройства.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Сообщение PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674811"
---
# <a name="phone_state-message"></a><span data-ttu-id="8512f-103">\_Сообщение о состоянии телефона</span><span class="sxs-lookup"><span data-stu-id="8512f-103">PHONE\_STATE message</span></span>

<span data-ttu-id="8512f-104">TAPI отправляет сообщение **о \_ состоянии телефона** приложению при каждом изменении состояния телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="8512f-104">TAPI sends the **PHONE\_STATE** message to an application whenever the status of a phone device changes.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8512f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="8512f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8512f-106">*хфоне*</span><span class="sxs-lookup"><span data-stu-id="8512f-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="8512f-107">Маркер телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="8512f-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="8512f-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="8512f-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8512f-109">Экземпляр обратного вызова приложения, предоставленный при открытии телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="8512f-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="8512f-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8512f-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8512f-111">Состояние телефона, которое было изменено.</span><span class="sxs-lookup"><span data-stu-id="8512f-111">The phone state that has changed.</span></span> <span data-ttu-id="8512f-112">Этот параметр использует одну из [**\_ констант фонестате**](phonestate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8512f-112">This parameter uses one of the [**PHONESTATE\_ constants**](phonestate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8512f-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8512f-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8512f-114">Сведения об изменении состояния, зависящие от состояния телефона.</span><span class="sxs-lookup"><span data-stu-id="8512f-114">Phone state-dependent information detailing the status change.</span></span> <span data-ttu-id="8512f-115">Этот параметр не используется, если в *dwParam1* задано несколько флагов, так как изменилось несколько элементов состояния.</span><span class="sxs-lookup"><span data-stu-id="8512f-115">This parameter is not used if multiple flags are set in *dwParam1*, because multiple status items have changed.</span></span> <span data-ttu-id="8512f-116">Приложение должно вызвать [**фонежетстатус**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) для получения полного набора сведений.</span><span class="sxs-lookup"><span data-stu-id="8512f-116">The application should invoke [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) to obtain a complete set of information.</span></span>

<span data-ttu-id="8512f-117">Если *dwParam1* является фонестате \_ owner, *dwParam2* содержит новое число владельцев.</span><span class="sxs-lookup"><span data-stu-id="8512f-117">If *dwParam1* is PHONESTATE\_OWNER, *dwParam2* contains the new number of owners.</span></span>

<span data-ttu-id="8512f-118">Если *dwParam1* — \_ мониторы фонестате *, dwParam2* содержит новое число мониторов.</span><span class="sxs-lookup"><span data-stu-id="8512f-118">If *dwParam1* is PHONESTATE\_MONITORS, *dwParam2* contains the new number of monitors.</span></span>

<span data-ttu-id="8512f-119">Если *dwParam1* — фонестате \_ лампа, *dwParam2* содержит идентификатор кнопки или лампы измененной лампы.</span><span class="sxs-lookup"><span data-stu-id="8512f-119">If *dwParam1* is PHONESTATE\_LAMP, *dwParam2* contains the button/lamp identifier of the lamp that has changed.</span></span>

<span data-ttu-id="8512f-120">Если *dwParam1* имеет значение фонестате \_ рингмоде, *dwParam2* содержит новый режим кольца.</span><span class="sxs-lookup"><span data-stu-id="8512f-120">If *dwParam1* is PHONESTATE\_RINGMODE, *dwParam2* contains the new ring mode.</span></span>

<span data-ttu-id="8512f-121">Если *dwParam1* — фонестатеная \_ трубка, докладчик или гарнитура, *dwParam2* содержит новый режим хуксвитч для устройства хуксвитч.</span><span class="sxs-lookup"><span data-stu-id="8512f-121">If *dwParam1* is PHONESTATE\_HANDSET, SPEAKER or HEADSET, *dwParam2* contains the new hookswitch mode of that hookswitch device.</span></span> <span data-ttu-id="8512f-122">Этот параметр использует одну из [**\_ констант фонехуксвитчмоде**](phonehookswitchmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8512f-122">This parameter uses one of the [**PHONEHOOKSWITCHMODE\_ constants**](phonehookswitchmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8512f-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8512f-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8512f-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8512f-124">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8512f-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8512f-125">Return value</span></span>

<span data-ttu-id="8512f-126">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8512f-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8512f-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8512f-127">Remarks</span></span>

<span data-ttu-id="8512f-128">Отправка сообщения **о \_ состоянии телефона** приложению можно контролировать и запрашивать с помощью [**фонесетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) и [**фонежетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="8512f-128">Sending the **PHONE\_STATE** message to the application can be controlled and queried using [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) and [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span></span> <span data-ttu-id="8512f-129">По умолчанию это сообщение отключено для всех изменений состояния, за исключением ФОНЕСТАТЕ \_ reinit, который нельзя отключить.</span><span class="sxs-lookup"><span data-stu-id="8512f-129">By default, this message is disabled for all state changes except for PHONESTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="8512f-130">Это сообщение отправляется во все приложения, имеющие маркер для телефона, включая те, которые вызвали [**фонеопен**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) с параметром *двпривилежес* , настроенным на фонепривилеже \_ owner или фонепривилеже \_ Monitor.</span><span class="sxs-lookup"><span data-stu-id="8512f-130">This message is sent to all applications that have a handle to the phone, including those that called [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) with the *dwPrivileges* parameter set to PHONEPRIVILEGE\_OWNER or PHONEPRIVILEGE\_MONITOR.</span></span>

<span data-ttu-id="8512f-131">Сообщение **о \_ состоянии телефона** с указанием владельцев и (или) мониторов отправляется в приложения, у которых уже есть маркер для телефона.</span><span class="sxs-lookup"><span data-stu-id="8512f-131">A **PHONE\_STATE** message with an Owners and/or Monitors indication is sent to applications that already have a handle for the phone.</span></span> <span data-ttu-id="8512f-132">Это может быть результатом другого приложения, изменяющего владение или мониторингом телефонного устройства с помощью [**фонеопен**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**фонеклосе**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) или [**фонешутдовн**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span><span class="sxs-lookup"><span data-stu-id="8512f-132">This can be the result of another application changing ownership or monitorship of the phone device with [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) or [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span></span>

## <a name="requirements"></a><span data-ttu-id="8512f-133">Требования</span><span class="sxs-lookup"><span data-stu-id="8512f-133">Requirements</span></span>



| <span data-ttu-id="8512f-134">Требование</span><span class="sxs-lookup"><span data-stu-id="8512f-134">Requirement</span></span> | <span data-ttu-id="8512f-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8512f-135">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8512f-136">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8512f-136">TAPI version</span></span><br/> | <span data-ttu-id="8512f-137">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8512f-137">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8512f-138">Header</span><span class="sxs-lookup"><span data-stu-id="8512f-138">Header</span></span><br/>       | <dl> <span data-ttu-id="8512f-139"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8512f-139"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8512f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8512f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8512f-141">**\_закрытие телефона**</span><span class="sxs-lookup"><span data-stu-id="8512f-141">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="8512f-142">**фонекапс**</span><span class="sxs-lookup"><span data-stu-id="8512f-142">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="8512f-143">**фонеклосе**</span><span class="sxs-lookup"><span data-stu-id="8512f-143">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[<span data-ttu-id="8512f-144">**фонежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="8512f-144">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[<span data-ttu-id="8512f-145">**фонежетстатус**</span><span class="sxs-lookup"><span data-stu-id="8512f-145">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[<span data-ttu-id="8512f-146">**фонежетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="8512f-146">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="8512f-147">**фонеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="8512f-147">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="8512f-148">**фонеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="8512f-148">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="8512f-149">**фонеопен**</span><span class="sxs-lookup"><span data-stu-id="8512f-149">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="8512f-150">**фонесетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="8512f-150">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="8512f-151">**фонешутдовн**</span><span class="sxs-lookup"><span data-stu-id="8512f-151">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




