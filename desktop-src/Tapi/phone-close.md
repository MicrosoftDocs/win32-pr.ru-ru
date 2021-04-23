---
description: '\_Сообщение закрытия телефона TAPI отправляется при принудительном закрытии открытого телефонного устройства в процессе восстановления ресурса. После отправки сообщения маркер устройства больше не действителен.'
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: Сообщение PHONE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675739"
---
# <a name="phone_close-message"></a><span data-ttu-id="27b06-104">\_Сообщение о закрытии телефона</span><span class="sxs-lookup"><span data-stu-id="27b06-104">PHONE\_CLOSE message</span></span>

<span data-ttu-id="27b06-105">Сообщение **\_ закрытия телефона** TAPI отправляется при принудительном закрытии открытого телефонного устройства в процессе восстановления ресурса.</span><span class="sxs-lookup"><span data-stu-id="27b06-105">The TAPI **PHONE\_CLOSE** message is sent when an open phone device has been forcibly closed as part of resource reclamation.</span></span> <span data-ttu-id="27b06-106">После отправки сообщения маркер устройства больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="27b06-106">The device handle is no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="27b06-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="27b06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27b06-108">*хфоне*</span><span class="sxs-lookup"><span data-stu-id="27b06-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="27b06-109">Маркер открытого телефонного устройства, который был закрыт.</span><span class="sxs-lookup"><span data-stu-id="27b06-109">A handle to the open phone device that was closed.</span></span> <span data-ttu-id="27b06-110">После отправки этого сообщения маркер больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="27b06-110">The handle is no longer valid after this message has been sent.</span></span>

</dd> <dt>

<span data-ttu-id="27b06-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="27b06-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="27b06-112">Экземпляр обратного вызова приложения, который был предоставлен при открытии телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="27b06-112">The application's callback instance that provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="27b06-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="27b06-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="27b06-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="27b06-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="27b06-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="27b06-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="27b06-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="27b06-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="27b06-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="27b06-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="27b06-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="27b06-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27b06-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27b06-119">Return value</span></span>

<span data-ttu-id="27b06-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="27b06-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27b06-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27b06-121">Remarks</span></span>

<span data-ttu-id="27b06-122">Сообщение **\_ закрытия телефона** отправляется в приложение только после принудительного закрытия открытого телефона.</span><span class="sxs-lookup"><span data-stu-id="27b06-122">The **PHONE\_CLOSE** message is only sent to an application after an open phone has been forcibly closed.</span></span> <span data-ttu-id="27b06-123">Это можно сделать, чтобы предотвратить слишком длинное монопольное применение телефонного устройства для одного приложения.</span><span class="sxs-lookup"><span data-stu-id="27b06-123">This can be done to prevent a single application from monopolizing a phone device for too long.</span></span> <span data-ttu-id="27b06-124">Можно ли повторно открыть телефон сразу после принудительного закрытия в зависимости от устройства.</span><span class="sxs-lookup"><span data-stu-id="27b06-124">Whether the phone can be reopened immediately after a forced close is device specific.</span></span>

<span data-ttu-id="27b06-125">Устройство с открытым телефоном можно также принудительно закрыть после того, как пользователь изменил конфигурацию этого телефона или его драйвера.</span><span class="sxs-lookup"><span data-stu-id="27b06-125">An open phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="27b06-126">Если пользователь хочет, чтобы изменения конфигурации вступили в силу немедленно (в отличие от следующей перезагрузки системы), и эти изменения затрагивают текущее представление устройства (например, изменение возможностей устройства), то поставщик услуг может принудительно закрыть телефонное устройство.</span><span class="sxs-lookup"><span data-stu-id="27b06-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and these changes affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b06-127">Требования</span><span class="sxs-lookup"><span data-stu-id="27b06-127">Requirements</span></span>



| <span data-ttu-id="27b06-128">Требование</span><span class="sxs-lookup"><span data-stu-id="27b06-128">Requirement</span></span> | <span data-ttu-id="27b06-129">Значение</span><span class="sxs-lookup"><span data-stu-id="27b06-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="27b06-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="27b06-130">TAPI version</span></span><br/> | <span data-ttu-id="27b06-131">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="27b06-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="27b06-132">Header</span><span class="sxs-lookup"><span data-stu-id="27b06-132">Header</span></span><br/>       | <dl> <span data-ttu-id="27b06-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="27b06-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




