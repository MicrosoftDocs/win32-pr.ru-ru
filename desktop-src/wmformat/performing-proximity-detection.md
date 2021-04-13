---
title: Выполнение обнаружения близлежащих устройств
description: Выполнение обнаружения близлежащих устройств
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Пакет SDK для Windows Media Format, выполнение обнаружения близлежащих устройств
- Windows Media Format SDK, обнаружение близлежащих устройств
- Расширенный системный формат (ASF), выполнение обнаружения близлежащих устройств
- ASF (Расширенный системный формат), выполнение обнаружения близлежащих устройств
- Расширенный формат систем (ASF), обнаружение близлежащих устройств
- ASF (Расширенный системный формат), обнаружение близлежащих устройств
- Управление цифровыми правами (DRM), выполнение обнаружения близлежащих устройств
- DRM (Управление цифровыми правами), выполнение обнаружения близлежащих устройств
- Управление цифровыми правами (DRM), обнаружение близлежащих устройств
- DRM (Управление цифровыми правами), обнаружение близлежащих устройств
- Обнаружение близлежащих устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412471"
---
# <a name="performing-proximity-detection"></a><span data-ttu-id="2bd7c-114">Выполнение обнаружения близлежащих устройств</span><span class="sxs-lookup"><span data-stu-id="2bd7c-114">Performing Proximity Detection</span></span>

<span data-ttu-id="2bd7c-115">Прежде чем передавать зашифрованные данные в зарегистрированное устройство в протоколе Windows Media DRM 10 для сетевых устройств, необходимо выполнить процесс, называемый обнаружением близости (также называемым проверкой).</span><span class="sxs-lookup"><span data-stu-id="2bd7c-115">Before you can stream encrypted data to a registered device in the Windows Media DRM 10 for Network Devices protocol, you must perform a process called proximity detection (also called validation).</span></span> <span data-ttu-id="2bd7c-116">Этот процесс включает отправку сообщений на устройство и получение ответов.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-116">This process involves sending messages to the device and receiving responses.</span></span> <span data-ttu-id="2bd7c-117">Время получения ответа используется для определения того, что устройство достаточно близко к компьютеру в сети для получения защищенных данных.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-117">The time it takes to receive a response is used to determine whether the device is "near" enough to the computer on the network to receive secure data.</span></span> <span data-ttu-id="2bd7c-118">Подтверждение того, что устройство физически близко к клиентскому компьютеру в сети, помогает предотвратить подмену и другие несанкционированные попытки доступа.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-118">Confirming that the device is physically close to the client computer on the network helps to prevent spoofing and other unauthorized access.</span></span>

<span data-ttu-id="2bd7c-119">Когда обнаружение близости успешно завершится, устройство считается действительным.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-119">When proximity detection is successfully completed, the device is said to be valid.</span></span> <span data-ttu-id="2bd7c-120">Проверить, является ли устройство допустимым, можно путем вызова метода [**ивмрегистереддевице:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) .</span><span class="sxs-lookup"><span data-stu-id="2bd7c-120">You can check whether a device is valid by calling the [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) method.</span></span> <span data-ttu-id="2bd7c-121">Устройства должны проверяться каждые 48 часов.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-121">Devices must be validated every 48 hours.</span></span> <span data-ttu-id="2bd7c-122">Устройство, прошедшее проверку более 48 часов до запуска программы, должно быть повторно проверено путем выполнения процесса обнаружения близости.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-122">A device that was validated more than 48 hours before your program runs must be revalidated by performing the proximity detection process again.</span></span>

<span data-ttu-id="2bd7c-123">Чтобы обнаружить близость, необходимо установить связь с устройством, а затем вызвать метод [**ивмпроксимитидетектион:: стартдетектион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) .</span><span class="sxs-lookup"><span data-stu-id="2bd7c-123">To perform proximity detection, you must establish communications with the device and then call the [**IWMProximityDetection::StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) method.</span></span> <span data-ttu-id="2bd7c-124">Процесс обнаружения асинхронно завершается внутренними компонентами DRM пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-124">The detection process is completed asynchronously by the internal DRM components of the Windows Media Format SDK.</span></span> <span data-ttu-id="2bd7c-125">Приложение должно включать реализацию интерфейса [**ивмстатускаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) для обработки сообщений обнаружения близости.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-125">Your application must include an implementation of the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface to process proximity detection messages.</span></span>

<span data-ttu-id="2bd7c-126">Процесс обнаружения близлежащих сообщений отправляет два сообщения: сообщение с результатами и сообщение о завершении.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-126">There are two messages that are sent by the proximity detection process: a result message and a completion message.</span></span>

<span data-ttu-id="2bd7c-127">\_ \_ После завершения процесса обнаружения отправляется результирующее сообщение, ВМТ близость.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-127">The result message, WMT\_PROXIMITY\_RESULT, is sent when the detection process is completed.</span></span> <span data-ttu-id="2bd7c-128">Параметр *HR* метода обратного вызова [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) указывает, было ли обнаружено, что устройство достаточно близко к клиентскому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-128">The *hr* parameter of the [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method indicates whether the device was found to be near enough to the client computer.</span></span> <span data-ttu-id="2bd7c-129">Если параметр *HR* результирующего сообщения указывает на успешное выполнение, параметр *pValue* содержит **DWORD** , указывающий измеряемую задержку на устройство в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-129">If the *hr* parameter of the result message indicates success, the *pValue* parameter contains a **DWORD** specifying the measured latency to the device in milliseconds.</span></span>

<span data-ttu-id="2bd7c-130">При завершении \_ обнаружения отправляется сообщение о завершении, ВМТ близость \_ .</span><span class="sxs-lookup"><span data-stu-id="2bd7c-130">The completion message, WMT\_PROXIMITY\_COMPLETED, is sent when the detection is finalized.</span></span> <span data-ttu-id="2bd7c-131">Интерфейс [**ивмпроксимитидетектион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) следует освобождать только после получения этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-131">You should release the [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) interface only after receiving this message.</span></span>

<span data-ttu-id="2bd7c-132">При завершении обнаружения для устройства база данных регистрации устройства обновляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-132">When proximity detection for a device succeeds, the device registration database is automatically updated.</span></span> <span data-ttu-id="2bd7c-133">Последующие вызовы [**ивмрегистереддевице:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) будут возвращать **значение true** до тех пор, пока не прошло 48 часов и необходимо будет выполнить повторную проверку устройства.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-133">Subsequent calls to [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) will return **TRUE** until 48 hours have passed and the device needs to be revalidated.</span></span>

<span data-ttu-id="2bd7c-134">**Примечание** . DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="2bd7c-134">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bd7c-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2bd7c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bd7c-136">**Использование протокола Windows Media DRM 10 для сетевых устройств**</span><span class="sxs-lookup"><span data-stu-id="2bd7c-136">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




