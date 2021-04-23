---
description: '\_Сообщение о закрытии линии TAPI отправляется, когда указанное устройство было принудительно закрыто. Дескриптор устройства линии или любые дескрипторы вызова в строке больше не действительны после отправки сообщения.'
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: Сообщение LINE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688752"
---
# <a name="line_close-message"></a><span data-ttu-id="1bc7a-104">\_Сообщение о закрытии строки</span><span class="sxs-lookup"><span data-stu-id="1bc7a-104">LINE\_CLOSE message</span></span>

<span data-ttu-id="1bc7a-105">Сообщение о **\_ закрытии линии** TAPI отправляется, когда указанное устройство было принудительно закрыто.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-105">The TAPI **LINE\_CLOSE** message is sent when the specified line device has been forcibly closed.</span></span> <span data-ttu-id="1bc7a-106">Дескриптор устройства линии или любые дескрипторы вызова в строке больше не действительны после отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-106">The line device handle or any call handles for calls on the line are no longer valid once this message has been sent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="1bc7a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bc7a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bc7a-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="1bc7a-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc7a-109">Маркер закрытого устройства Line.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-109">A handle to the line device that was closed.</span></span> <span data-ttu-id="1bc7a-110">Этот маркер больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-110">This handle is no longer valid.</span></span>

</dd> <dt>

<span data-ttu-id="1bc7a-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="1bc7a-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc7a-112">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="1bc7a-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1bc7a-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc7a-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-114">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="1bc7a-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1bc7a-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc7a-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="1bc7a-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="1bc7a-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc7a-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bc7a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1bc7a-119">Return value</span></span>

<span data-ttu-id="1bc7a-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bc7a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1bc7a-121">Remarks</span></span>

<span data-ttu-id="1bc7a-122">Сообщение **о \_ закрытии строки** отправляется любому приложению только после того, как поставщик услуг TAPI принудительно закрыл открытую строку.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-122">The **LINE\_CLOSE** message is sent to any application only after the TAPI service provider (TSP) has forcibly closed an open line.</span></span> <span data-ttu-id="1bc7a-123">Можно ли повторно открыть строку сразу после принудительного закрытия, зависящего от устройства.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-123">Whether or not the line can be reopened immediately after a forced close is device-specific.</span></span>

<span data-ttu-id="1bc7a-124">Условие, вызывающее срабатывание, может быть существенным изменением состояния, аппаратной ошибкой, потерей соединения с сервером или даже потенциально, чтобы предотвратить слишком длинное монопольное применение устройства в одном приложении.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-124">The causing condition can be a significant change of state, a hardware error, a loss of connection to a server, or even potentially to prevent a single application from monopolizing a line device for too long.</span></span> <span data-ttu-id="1bc7a-125">Линейное устройство можно также принудительно закрыть после того, как пользователь изменял конфигурацию этой строки или ее драйвера.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-125">A line device can also be forcibly closed after the user has modified the configuration of that line or its driver.</span></span> <span data-ttu-id="1bc7a-126">Если пользователь хочет, чтобы изменения конфигурации действовали немедленно (в отличие от следующей перезагрузки системы), и они влияют на текущее представление устройства (например, на возможности устройства), то поставщик услуг может принудительно закрыть устройство линии.</span><span class="sxs-lookup"><span data-stu-id="1bc7a-126">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the line device.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc7a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1bc7a-127">Requirements</span></span>



| <span data-ttu-id="1bc7a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1bc7a-128">Requirement</span></span> | <span data-ttu-id="1bc7a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1bc7a-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1bc7a-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1bc7a-130">TAPI version</span></span><br/> | <span data-ttu-id="1bc7a-131">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1bc7a-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1bc7a-132">Header</span><span class="sxs-lookup"><span data-stu-id="1bc7a-132">Header</span></span><br/>       | <dl> <span data-ttu-id="1bc7a-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bc7a-133"><dt>Tapi.h</dt></span></span> </dl> |



 

 




