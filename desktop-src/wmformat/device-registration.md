---
title: Регистрация устройства
description: Регистрация устройства
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media Format SDK, регистрация устройств
- Windows Media Format SDK, регистрация устройств
- Расширенный формат систем (ASF), регистрация устройств
- ASF (Расширенный системный формат), регистрация устройства
- Расширенный формат систем (ASF), регистрация устройств
- ASF (Расширенный системный формат), регистрация устройств
- Управление цифровыми правами (DRM), регистрация устройств
- DRM (Управление цифровыми правами), регистрация устройства
- Управление цифровыми правами (DRM), регистрация устройств
- DRM (Управление цифровыми правами), регистрация устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069566"
---
# <a name="device-registration"></a><span data-ttu-id="ed977-113">Регистрация устройства</span><span class="sxs-lookup"><span data-stu-id="ed977-113">Device Registration</span></span>

<span data-ttu-id="ed977-114">Пакет SDK для формата Windows Media предоставляет доступ к базе данных регистрации устройств.</span><span class="sxs-lookup"><span data-stu-id="ed977-114">The Windows Media Format SDK provides access to the device registration database.</span></span> <span data-ttu-id="ed977-115">Эта база данных защищена на клиентском компьютере и используется для регистрации устройств, поддерживающих Windows Media DRM 10 для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="ed977-115">This database is secured on the client computer and is used to register devices that support Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="ed977-116">При добавлении устройства в сеть, к которой подключен клиентский компьютер, устройство пытается связаться с приложением передатчика Windows Media DRM 10 для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="ed977-116">When a device is added to a network to which the client computer is connected, the device attempts to contact a Windows Media DRM 10 for Network Devices transmitter application.</span></span> <span data-ttu-id="ed977-117">После установления связи устройство отправляет сообщение с запросом на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="ed977-117">After establishing communications, the device sends a registration request message.</span></span>

<span data-ttu-id="ed977-118">При получении сообщения с запросом на регистрацию приложение должно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ed977-118">Your application should perform the following steps when it receives a registration request message:</span></span>

1.  <span data-ttu-id="ed977-119">Проанализируйте сообщение, вызвав метод [**ивмдрммессажепарсер::P арсерегистратионрекмсг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) .</span><span class="sxs-lookup"><span data-stu-id="ed977-119">Parse the message by calling the [**IWMDRMMessageParser::ParseRegistrationReqMsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) method.</span></span> <span data-ttu-id="ed977-120">Этот метод извлекает сертификат устройства и серийный номер устройства, которые необходимы для обнаружения устройства.</span><span class="sxs-lookup"><span data-stu-id="ed977-120">This method retrieves the device certificate and the device serial number, both of which are needed to identify the device.</span></span>
2.  <span data-ttu-id="ed977-121">Вызовите метод [**ивмдевицерегистратион:: жетрегистереддевицебид**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , передав сертификат и серийный номер устройства, полученные на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="ed977-121">Call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method, passing in the certificate and device serial number retrieved in step 1.</span></span> <span data-ttu-id="ed977-122">Если устройство найдено, оно уже зарегистрировано, и вы можете пропустить следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="ed977-122">If the device is found, it is already registered and you can skip the next step.</span></span>
3.  <span data-ttu-id="ed977-123">Вызовите метод [**ивмдевицерегистратион:: RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) , чтобы добавить устройство в базу данных регистрации устройств.</span><span class="sxs-lookup"><span data-stu-id="ed977-123">Call the [**IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) method to add the device to the device registration database.</span></span>

<span data-ttu-id="ed977-124">Вы можете получить доступ к сведениям о любом устройстве в базе данных регистрации, извлекая связанный с ним объект зарегистрированного устройства.</span><span class="sxs-lookup"><span data-stu-id="ed977-124">You can access information about any device in the registration database by retrieving the registered device object associated with it.</span></span> <span data-ttu-id="ed977-125">Существует два способа получить зарегистрированный объект устройства.</span><span class="sxs-lookup"><span data-stu-id="ed977-125">There are two ways to get a registered device object.</span></span> <span data-ttu-id="ed977-126">Если у вас есть сертификат и серийный номер устройства, можно вызвать метод [**ивмдевицерегистратион:: жетрегистереддевицебид**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) .</span><span class="sxs-lookup"><span data-stu-id="ed977-126">If you have the certificate and serial number of the device, you can call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method.</span></span> <span data-ttu-id="ed977-127">Если у вас нет сертификата и серийного номера устройства, можно перечислить все устройства в базе данных, вызвав [**ивмдевицерегистратион:: жетфирстрегистереддевице**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) , а затем повторные вызовы [**Ивмдевицерегистратион:: жетнекстрегистереддевице**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) до тех пор, пока вызов не возвратит \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="ed977-127">If you do not have the certificate and serial number of the device, you can enumerate all the devices in the database by calling [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) followed by repeated calls to [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) until a call returns S\_FALSE.</span></span>

<span data-ttu-id="ed977-128">Прежде чем приложение сможет отправить данные на устройство, необходимо убедиться, что устройство утверждено, проверено и открыто.</span><span class="sxs-lookup"><span data-stu-id="ed977-128">Before your application can send data to a device, you must ensure that the device is approved, validated, and open.</span></span>

<span data-ttu-id="ed977-129">Утверждение устройства должно затрагивать взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="ed977-129">Device approval should involve interaction with the user.</span></span> <span data-ttu-id="ed977-130">Когда устройство отправляет сообщение регистрации, оно может предложить пользователю решить, является ли устройство устройством, которое должно получить данные этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed977-130">When a device sends a registration message, your application can prompt the user to decide whether the device is one that should receive that user's data.</span></span> <span data-ttu-id="ed977-131">Затем обновите базу данных регистрации устройств, вызвав метод [**ивмрегистереддевице:: reутверждать**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) , передав **true** или **false** соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="ed977-131">Then update the device registration database by calling the [**IWMRegisteredDevice::Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) method, passing **TRUE** or **FALSE** as appropriate.</span></span>

<span data-ttu-id="ed977-132">Проверка также называется обнаружением близлежащих устройств.</span><span class="sxs-lookup"><span data-stu-id="ed977-132">Validation is also called proximity detection.</span></span> <span data-ttu-id="ed977-133">Это процесс, с помощью которого внутренние объекты DRM из пакета SDK Windows Media Format определяют, достаточно ли для компьютера, на котором работает приложение, безопасно передавать носители.</span><span class="sxs-lookup"><span data-stu-id="ed977-133">This is a process by which the internal DRM objects of the Windows Media Format SDK determine whether the device is "near" enough to the computer running your application to securely transmit media.</span></span> <span data-ttu-id="ed977-134">Близкость определяется временем, которое требуется для получения ответа на сообщение.</span><span class="sxs-lookup"><span data-stu-id="ed977-134">Nearness is determined by the time it takes to get a response to a message.</span></span> <span data-ttu-id="ed977-135">Эта функция предназначена для предотвращения доступа неавторизованных пользователей к сети и получения защищенного носителя.</span><span class="sxs-lookup"><span data-stu-id="ed977-135">This feature is intended to prevent unauthorized users from accessing your network and obtaining your secured media.</span></span> <span data-ttu-id="ed977-136">Дополнительные сведения см. в разделе [выполнение обнаружения близлежащих](performing-proximity-detection.md)устройств.</span><span class="sxs-lookup"><span data-stu-id="ed977-136">For more information, see [Performing Proximity Detection](performing-proximity-detection.md).</span></span>

<span data-ttu-id="ed977-137">Чтобы открыть устройство, вызовите [**ивмрегистереддевице:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span><span class="sxs-lookup"><span data-stu-id="ed977-137">To open a device, call [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span></span>

> [!Note]  
> <span data-ttu-id="ed977-138">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="ed977-138">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ed977-139">См. также</span><span class="sxs-lookup"><span data-stu-id="ed977-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed977-140">**ивмрегистереддевице**</span><span class="sxs-lookup"><span data-stu-id="ed977-140">**IWMRegisteredDevice**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[<span data-ttu-id="ed977-141">**Использование протокола Windows Media DRM 10 для сетевых устройств**</span><span class="sxs-lookup"><span data-stu-id="ed977-141">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




