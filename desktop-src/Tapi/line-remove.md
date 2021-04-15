---
description: '\_Сообщение Удаление линии TAPI отправляется для информирования приложения об удалении (об удалении из системы) линейного устройства.'
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: Сообщение LINE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675677"
---
# <a name="line_remove-message"></a><span data-ttu-id="dae78-103">\_Сообщение об удалении строки</span><span class="sxs-lookup"><span data-stu-id="dae78-103">LINE\_REMOVE message</span></span>

<span data-ttu-id="dae78-104">Сообщение **\_ Удаление линии** TAPI отправляется для информирования приложения об удалении (об удалении из системы) линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="dae78-104">The TAPI **LINE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a line device.</span></span> <span data-ttu-id="dae78-105">Как правило, это не используется для временных удалений, например для извлечения устройств PCMCIA, но только для постоянных удалений, в которых устройство больше не будет сообщено поставщиком услуг при повторной инициализации TAPI.</span><span class="sxs-lookup"><span data-stu-id="dae78-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="dae78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dae78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae78-107">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="dae78-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="dae78-108">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="dae78-108">Reserved.</span></span> <span data-ttu-id="dae78-109">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="dae78-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="dae78-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="dae78-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="dae78-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="dae78-111">Reserved.</span></span> <span data-ttu-id="dae78-112">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="dae78-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="dae78-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="dae78-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="dae78-114">Идентификатор удаленного устройства, которое было удалено.</span><span class="sxs-lookup"><span data-stu-id="dae78-114">Identifier of the line device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="dae78-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="dae78-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="dae78-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="dae78-116">Reserved.</span></span> <span data-ttu-id="dae78-117">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="dae78-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="dae78-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="dae78-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="dae78-119">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="dae78-119">Reserved.</span></span> <span data-ttu-id="dae78-120">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="dae78-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae78-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dae78-121">Return value</span></span>

<span data-ttu-id="dae78-122">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="dae78-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dae78-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dae78-123">Remarks</span></span>

<span data-ttu-id="dae78-124">Приложения, поддерживающие TAPI версии 2,0 или более поздней, отправляют сообщение об **\_ удалении строки** .</span><span class="sxs-lookup"><span data-stu-id="dae78-124">Applications supporting TAPI version 2.0 or later are sent a **LINE\_REMOVE** message.</span></span> <span data-ttu-id="dae78-125">Это информирует, что устройство было удалено из системы.</span><span class="sxs-lookup"><span data-stu-id="dae78-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="dae78-126">Тексту сообщения об **\_ удалении строки** предшествует строка с сообщением о [**\_ закрытии строки**](line-close.md) для каждого маркера строки, если в приложении была открыта строка.</span><span class="sxs-lookup"><span data-stu-id="dae78-126">The **LINE\_REMOVE** message is preceded by a [**LINE\_CLOSE**](line-close.md) message on each line handle, if the application had the line open.</span></span> <span data-ttu-id="dae78-127">Это сообщение отправляется во все приложения, поддерживающие TAPI версии 2,0 или более поздней, которые назывались [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), включая те, которые не имеют устройств линий, открытых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="dae78-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

<span data-ttu-id="dae78-128">Более старые приложения отправляют сообщение [**Line \_ линедевстате**](line-linedevstate.md) с указанием линедевстате \_ removed, за которым следует \_ сообщение о закрытии строки.</span><span class="sxs-lookup"><span data-stu-id="dae78-128">Older applications are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REMOVED, followed by a LINE\_CLOSE message.</span></span> <span data-ttu-id="dae78-129">Однако, в отличие от сообщения об **\_ удалении** , эти старые приложения могут получить эти сообщения, только если при их удалении строка была открыта.</span><span class="sxs-lookup"><span data-stu-id="dae78-129">Unlike the **LINE\_REMOVE** message, however, these older applications can receive these messages only if they have the line open when it is removed.</span></span> <span data-ttu-id="dae78-130">Если у них нет открытой строки, то указание на то, что устройство было удалено, получит ошибку ЛИНИРР \_ при попытке доступа к устройству.</span><span class="sxs-lookup"><span data-stu-id="dae78-130">If they do not have the line open, their only indication that the device was removed would be receiving a LINEERR\_NODEVICE error when they attempt to access the device.</span></span>

<span data-ttu-id="dae78-131">После удаления устройства любая попытка получить доступ к устройству по его идентификатору приводит к \_ ошибке линирр-устройства.</span><span class="sxs-lookup"><span data-stu-id="dae78-131">After a device has been removed, any attempt to access the device by its device identifier results in a LINEERR\_NODEVICE error.</span></span> <span data-ttu-id="dae78-132">После завершения работы всех приложений TAPI для перезапуска TAPI, а также при повторной инициализации TAPI удаленное устройство больше не будет занимать идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="dae78-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="dae78-133">Реализация: это TAPI, возвращающий это ЛИНИРР \_ устройство. После получения сообщения об **\_ удалении строки** от поставщика услуг дальнейшие обращения к этому поставщику службы с помощью идентификатора устройства этой линии не выполняются.</span><span class="sxs-lookup"><span data-stu-id="dae78-133">Implementation: it is TAPI that returns this LINEERR\_NODEVICE; after a **LINE\_REMOVE** message is received from a service provider; no further calls are made to that service provider using that line device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dae78-134">Требования</span><span class="sxs-lookup"><span data-stu-id="dae78-134">Requirements</span></span>



| <span data-ttu-id="dae78-135">Требование</span><span class="sxs-lookup"><span data-stu-id="dae78-135">Requirement</span></span> | <span data-ttu-id="dae78-136">Значение</span><span class="sxs-lookup"><span data-stu-id="dae78-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dae78-137">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="dae78-137">TAPI version</span></span><br/> | <span data-ttu-id="dae78-138">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="dae78-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="dae78-139">Header</span><span class="sxs-lookup"><span data-stu-id="dae78-139">Header</span></span><br/>       | <dl> <span data-ttu-id="dae78-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="dae78-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae78-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dae78-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae78-142">**\_закрыть строку**</span><span class="sxs-lookup"><span data-stu-id="dae78-142">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="dae78-143">**Строка \_ линедевстате**</span><span class="sxs-lookup"><span data-stu-id="dae78-143">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="dae78-144">**линеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="dae78-144">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




