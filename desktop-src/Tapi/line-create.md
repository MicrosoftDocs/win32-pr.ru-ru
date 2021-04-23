---
description: '\_Отправляется сообщение о создании линии TAPI для информирования приложения о создании устройства нового типа Line.'
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: Сообщение LINE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688836"
---
# <a name="line_create-message"></a><span data-ttu-id="8980f-103">\_Сообщение о создании строки</span><span class="sxs-lookup"><span data-stu-id="8980f-103">LINE\_CREATE message</span></span>

<span data-ttu-id="8980f-104">Отправляется сообщение о **\_ создании линии** TAPI для информирования приложения о создании устройства нового типа Line.</span><span class="sxs-lookup"><span data-stu-id="8980f-104">The TAPI **LINE\_CREATE** message is sent to inform the application of the creation of a new line device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8980f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="8980f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8980f-106">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="8980f-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8980f-107">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8980f-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8980f-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="8980f-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8980f-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8980f-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8980f-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8980f-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8980f-111">*Хдевицеид* созданного устройства.</span><span class="sxs-lookup"><span data-stu-id="8980f-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="8980f-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8980f-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8980f-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8980f-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8980f-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8980f-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8980f-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8980f-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8980f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8980f-116">Return value</span></span>

<span data-ttu-id="8980f-117">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8980f-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8980f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8980f-118">Remarks</span></span>

<span data-ttu-id="8980f-119">Более старые приложения (для согласованного интерфейса TAPI версии 1,3) отправляют сообщение [**Line \_ линедевстате**](line-linedevstate.md) с указанием линедевстате \_ reinit, что требует от них завершить использование API и вызвать [**линеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) еще раз, чтобы получить новое число устройств.</span><span class="sxs-lookup"><span data-stu-id="8980f-119">Older applications (that negotiated TAPI version 1.3) are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REINIT, which requires them to shut down their use of the API and call [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="8980f-120">Однако в отличие от предыдущих версий TAPI, эта версия не требует завершения работы всех приложений перед повторной инициализацией приложений. Повторная инициализация может выполняться немедленно при создании нового устройства (завершение работы по-прежнему требуется при удалении поставщика услуг из системы).</span><span class="sxs-lookup"><span data-stu-id="8980f-120">Unlike previous versions of TAPI, however, this version does not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created (complete shutdown is still required when a service provider is removed from the system).</span></span>

<span data-ttu-id="8980f-121">Приложения, поддерживающие TAPI версии 1,4 или более поздней, отправляют сообщение о **\_ создании строки** .</span><span class="sxs-lookup"><span data-stu-id="8980f-121">Applications supporting TAPI version 1.4 or later are sent a **LINE\_CREATE** message.</span></span> <span data-ttu-id="8980f-122">Это информирует их о существовании нового устройства и нового идентификатора устройства.</span><span class="sxs-lookup"><span data-stu-id="8980f-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="8980f-123">Затем приложение может выбрать, следует ли попытаться работать с новым устройством в свободное время.</span><span class="sxs-lookup"><span data-stu-id="8980f-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span> <span data-ttu-id="8980f-124">Это сообщение отправляется во все приложения, поддерживающие эту или последующие версии API, которые назывались [**линеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) или [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), включая те, которые не имеют устройств линий, открытых в данный момент.</span><span class="sxs-lookup"><span data-stu-id="8980f-124">This message is sent to all applications supporting this or subsequent versions of the API that have called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

## <a name="requirements"></a><span data-ttu-id="8980f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8980f-125">Requirements</span></span>



| <span data-ttu-id="8980f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8980f-126">Requirement</span></span> | <span data-ttu-id="8980f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8980f-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8980f-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8980f-128">TAPI version</span></span><br/> | <span data-ttu-id="8980f-129">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8980f-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8980f-130">Header</span><span class="sxs-lookup"><span data-stu-id="8980f-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8980f-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8980f-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8980f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8980f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8980f-133">**Строка \_ линедевстате**</span><span class="sxs-lookup"><span data-stu-id="8980f-133">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="8980f-134">**линеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="8980f-134">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="8980f-135">**линеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="8980f-135">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




