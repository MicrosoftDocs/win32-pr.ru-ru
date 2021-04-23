---
description: '\_Отправляется сообщение об удалении телефона TAPI для информирования приложения об удалении (об удалении из системы) телефонного устройства.'
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: Сообщение PHONE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688822"
---
# <a name="phone_remove-message"></a><span data-ttu-id="ba380-103">\_Сообщение для удаления телефона</span><span class="sxs-lookup"><span data-stu-id="ba380-103">PHONE\_REMOVE message</span></span>

<span data-ttu-id="ba380-104">Отправляется сообщение об **\_ удалении телефона** TAPI для информирования приложения об удалении (об удалении из системы) телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="ba380-104">The TAPI **PHONE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a phone device.</span></span> <span data-ttu-id="ba380-105">Как правило, это не используется для временных удалений, например для извлечения устройств PCMCIA, но только для постоянных удалений, в которых устройство больше не будет сообщено поставщиком услуг при повторной инициализации TAPI.</span><span class="sxs-lookup"><span data-stu-id="ba380-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="ba380-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba380-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba380-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="ba380-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="ba380-108">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ba380-108">Reserved.</span></span> <span data-ttu-id="ba380-109">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ba380-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba380-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="ba380-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ba380-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ba380-111">Reserved.</span></span> <span data-ttu-id="ba380-112">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ba380-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba380-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ba380-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ba380-114">Идентификатор удаленного устройства, которое было удалено.</span><span class="sxs-lookup"><span data-stu-id="ba380-114">Identifier of the phone device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="ba380-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ba380-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ba380-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ba380-116">Reserved.</span></span> <span data-ttu-id="ba380-117">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ba380-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba380-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ba380-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ba380-119">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ba380-119">Reserved.</span></span> <span data-ttu-id="ba380-120">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ba380-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba380-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba380-121">Return value</span></span>

<span data-ttu-id="ba380-122">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ba380-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba380-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba380-123">Remarks</span></span>

<span data-ttu-id="ba380-124">Приложения TAPI версии 2,0 или более поздней отправляют сообщение об **\_ удалении телефона** .</span><span class="sxs-lookup"><span data-stu-id="ba380-124">Applications TAPI version 2.0 or later are sent a **PHONE\_REMOVE** message.</span></span> <span data-ttu-id="ba380-125">Это информирует, что устройство было удалено из системы.</span><span class="sxs-lookup"><span data-stu-id="ba380-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="ba380-126">Сообщение **об \_ удалении телефона** предшествует сообщению о [**\_ закрытии**](phone-close.md) телефона для каждого телефонного маркера, если в приложении открыт телефон.</span><span class="sxs-lookup"><span data-stu-id="ba380-126">The **PHONE\_REMOVE** message is preceded by a [**PHONE\_CLOSE**](phone-close.md) message on each phone handle, if the application had the phone open.</span></span> <span data-ttu-id="ba380-127">Это сообщение отправляется во все приложения, поддерживающие TAPI версии 2,0 или более поздней, которые назывались [**фонеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), включая те, которые не имеют открытых телефонных устройств в данный момент.</span><span class="sxs-lookup"><span data-stu-id="ba380-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), including those that do not have any phone devices open at the time.</span></span>

<span data-ttu-id="ba380-128">Более старые приложения (для которых согласовывается TAPI версии 1,4 или более ранней) отправляют сообщение о [**\_ состоянии телефона**](phone-state.md) с указанием фонестате \_ removed, за которым следует сообщение о [**\_ закрытии телефона**](phone-close.md) .</span><span class="sxs-lookup"><span data-stu-id="ba380-128">Older applications (that negotiated TAPI version 1.4 or earlier) are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REMOVED, followed by a [**PHONE\_CLOSE**](phone-close.md) message.</span></span> <span data-ttu-id="ba380-129">Однако, в отличие от сообщения об **\_ удалении телефона** , эти старые приложения могут получить эти сообщения только в том случае, если при их удалении открыт открытый телефон.</span><span class="sxs-lookup"><span data-stu-id="ba380-129">Unlike the **PHONE\_REMOVE** message, however, these older applications can receive these messages only if they have the phone open when it is removed.</span></span> <span data-ttu-id="ba380-130">Если у них нет открытого телефона, это означает, что устройство было удалено \_ при попытке доступа к устройству было получено устройство фонирр.</span><span class="sxs-lookup"><span data-stu-id="ba380-130">If they do not have the phone open, their only indication that the device was removed would be receiving a PHONEERR\_NODEVICE when they attempt to access the device.</span></span>

<span data-ttu-id="ba380-131">После удаления устройства любая попытка получить доступ к устройству по его идентификатору приводит к \_ ошибке фонирр-устройства.</span><span class="sxs-lookup"><span data-stu-id="ba380-131">After a device has been removed, any attempt to access the device by its device identifier results in a PHONEERR\_NODEVICE error.</span></span> <span data-ttu-id="ba380-132">После завершения работы всех приложений TAPI для перезапуска TAPI, а также при повторной инициализации TAPI удаленное устройство больше не будет занимать идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="ba380-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="ba380-133">Реализация: это TAPI, возвращающий это \_ сообщение фонирр после \_ получения от поставщика услуг сообщения об удалении телефона; дальнейшие вызовы этого поставщика службы с помощью этого идентификатора устройства не выполняются.</span><span class="sxs-lookup"><span data-stu-id="ba380-133">Implementation: it is TAPI that returns this PHONEERR\_NODEVICE message after a PHONE\_REMOVE message is received from a service provider; no further calls are made to that service provider using that phone device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba380-134">Требования</span><span class="sxs-lookup"><span data-stu-id="ba380-134">Requirements</span></span>



| <span data-ttu-id="ba380-135">Требование</span><span class="sxs-lookup"><span data-stu-id="ba380-135">Requirement</span></span> | <span data-ttu-id="ba380-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ba380-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ba380-137">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ba380-137">TAPI version</span></span><br/> | <span data-ttu-id="ba380-138">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ba380-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ba380-139">Header</span><span class="sxs-lookup"><span data-stu-id="ba380-139">Header</span></span><br/>       | <dl> <span data-ttu-id="ba380-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba380-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba380-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba380-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba380-142">**\_закрытие телефона**</span><span class="sxs-lookup"><span data-stu-id="ba380-142">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="ba380-143">**\_состояние телефона**</span><span class="sxs-lookup"><span data-stu-id="ba380-143">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="ba380-144">**фонеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="ba380-144">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="ba380-145">**фонеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="ba380-145">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




