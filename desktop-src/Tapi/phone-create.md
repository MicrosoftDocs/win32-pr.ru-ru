---
description: '\_Отправляется сообщение о создании телефона TAPI для информирования приложений о создании нового телефонного устройства.'
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: Сообщение PHONE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674966"
---
# <a name="phone_create-message"></a><span data-ttu-id="4e7b4-103">\_Сообщение о создании телефона</span><span class="sxs-lookup"><span data-stu-id="4e7b4-103">PHONE\_CREATE message</span></span>

<span data-ttu-id="4e7b4-104">Отправляется сообщение о **\_ создании телефона** TAPI для информирования приложений о создании нового телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-104">The TAPI **PHONE\_CREATE** message is sent to inform applications of the creation of a new phone device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="4e7b4-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e7b4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e7b4-106">*хфоне*</span><span class="sxs-lookup"><span data-stu-id="4e7b4-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7b4-107">Не используется.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b4-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="4e7b4-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7b4-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b4-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4e7b4-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7b4-111">*Хдевицеид* созданного устройства.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b4-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4e7b4-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7b4-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b4-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="4e7b4-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7b4-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e7b4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e7b4-116">Return value</span></span>

<span data-ttu-id="4e7b4-117">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e7b4-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e7b4-118">Remarks</span></span>

<span data-ttu-id="4e7b4-119">Приложения, которые согласовали API версии 1,3, отправляют сообщение о [**\_ состоянии телефона**](phone-state.md) с указанием фонестате \_ reinit, что требует от них завершить использование API и вызвать [**фонеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) еще раз, чтобы получить новое число устройств.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-119">Applications that negotiated API version 1.3 are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REINIT, which requires them to shut down their use of the API and call [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="4e7b4-120">Однако TAPI версии 1,4 и выше не требует завершения работы всех приложений, прежде чем разрешить повторную инициализацию приложений. Повторная инициализация может выполняться немедленно при создании нового устройства.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-120">However, TAPI version 1.4 and above do not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created.</span></span>

<span data-ttu-id="4e7b4-121">Приложения, поддерживающие TAPI версии 1,4 или более поздней, отправляют сообщение о **\_ создании телефона** .</span><span class="sxs-lookup"><span data-stu-id="4e7b4-121">Applications supporting TAPI version 1.4 or later are sent a **PHONE\_CREATE** message.</span></span> <span data-ttu-id="4e7b4-122">Это информирует их о существовании нового устройства и нового идентификатора устройства.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="4e7b4-123">Затем приложение может выбрать, следует ли попытаться работать с новым устройством в свободное время.</span><span class="sxs-lookup"><span data-stu-id="4e7b4-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e7b4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4e7b4-124">Requirements</span></span>



| <span data-ttu-id="4e7b4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4e7b4-125">Requirement</span></span> | <span data-ttu-id="4e7b4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4e7b4-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4e7b4-127">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="4e7b4-127">TAPI version</span></span><br/> | <span data-ttu-id="4e7b4-128">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4e7b4-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4e7b4-129">Header</span><span class="sxs-lookup"><span data-stu-id="4e7b4-129">Header</span></span><br/>       | <dl> <span data-ttu-id="4e7b4-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e7b4-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e7b4-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e7b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7b4-132">**\_состояние телефона**</span><span class="sxs-lookup"><span data-stu-id="4e7b4-132">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="4e7b4-133">**фонеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="4e7b4-133">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="4e7b4-134">**фонеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="4e7b4-134">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




