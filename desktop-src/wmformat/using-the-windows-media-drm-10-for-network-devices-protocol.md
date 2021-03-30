---
title: Использование протокола Windows Media DRM 10 для сетевых устройств
description: Использование протокола Windows Media DRM 10 для сетевых устройств
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media Format SDK, Windows Media DRM 10 для сетевых устройств
- Windows Media Format SDK, DRM 10 для сетевых устройств
- Расширенный формат систем (ASF), Windows Media DRM 10 для сетевых устройств
- ASF (Расширенный системный формат), Windows Media DRM 10 для сетевых устройств
- Расширенный формат систем (ASF), DRM 10 для сетевых устройств
- ASF (Расширенный системный формат), DRM 10 для сетевых устройств
- Управление цифровыми правами (DRM), Windows Media DRM 10 для сетевых устройств
- DRM (Управление цифровыми правами), Windows Media DRM 10 для сетевых устройств
- Управление цифровыми правами (DRM), DRM 10 для сетевых устройств
- DRM (Управление цифровыми правами), DRM 10 для сетевых устройств
- Windows Media DRM 10 для сетевых устройств, протоколы
- DRM 10 для сетевых устройств, протоколов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329691"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a><span data-ttu-id="19627-115">Использование протокола Windows Media DRM 10 для сетевых устройств</span><span class="sxs-lookup"><span data-stu-id="19627-115">Using the Windows Media DRM 10 for Network Devices Protocol</span></span>

<span data-ttu-id="19627-116">Пакет Windows Media Format SDK предоставляет некоторые функции для поддержки протокола защищенных сетевых устройств, Windows Media DRM 10 для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="19627-116">The Windows Media Format SDK provides some features to support the secure network device protocol, Windows Media DRM 10 for Network Devices.</span></span> <span data-ttu-id="19627-117">Этот протокол определяет сообщения, которые передаются между устройством воспроизведения цифрового носителя, например видеопроигрывателем Set-Top, и компьютером, который обслуживает данные на устройстве.</span><span class="sxs-lookup"><span data-stu-id="19627-117">This protocol defines the messages sent between a digital media playback device, such as a set-top video player, and the computer that serves data to the device.</span></span> <span data-ttu-id="19627-118">Данные мультимедиа, передаваемые между сервером и устройством, шифруются для защиты от перехвата.</span><span class="sxs-lookup"><span data-stu-id="19627-118">The media data sent between server and device is encrypted to protect it from interception.</span></span>

<span data-ttu-id="19627-119">Взаимодействие между приложением и устройствами, поддерживающими Windows Media DRM 10 для сетевых устройств, может использовать любой предпочтительный сетевой протокол.</span><span class="sxs-lookup"><span data-stu-id="19627-119">The communication between your application and devices that support Windows Media DRM 10 for Network Devices can use whatever networking protocols you prefer.</span></span> <span data-ttu-id="19627-120">Пакет SDK для формата Windows Media не предоставляет никаких объектов, которые выполняют сетевую связь.</span><span class="sxs-lookup"><span data-stu-id="19627-120">The Windows Media Format SDK does not provide any objects that perform the network communications for you.</span></span> <span data-ttu-id="19627-121">Вместо этого объекты этого пакета SDK обрабатывают некоторые сообщения Windows Media DRM 10 для сетевых устройств после их получения приложением.</span><span class="sxs-lookup"><span data-stu-id="19627-121">Instead, the objects of this SDK process some Windows Media DRM 10 for Network Devices messages after your application has received them.</span></span>

<span data-ttu-id="19627-122">Функции, поддерживающие Windows Media DRM 10 для сетевых устройств, — это регистрация устройств, обнаружение с учетом расположения и преобразование файлов, защищенных с помощью DRM.</span><span class="sxs-lookup"><span data-stu-id="19627-122">The features that support Windows Media DRM 10 for Network Devices are device registration, proximity detection, and converting DRM-protected files.</span></span> <span data-ttu-id="19627-123">Эти функции описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="19627-123">These features are described in the following sections.</span></span>



| <span data-ttu-id="19627-124">Section</span><span class="sxs-lookup"><span data-stu-id="19627-124">Section</span></span>                                                                                                                                                                          | <span data-ttu-id="19627-125">Описание</span><span class="sxs-lookup"><span data-stu-id="19627-125">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19627-126">Регистрация устройства</span><span class="sxs-lookup"><span data-stu-id="19627-126">Device Registration</span></span>](device-registration.md)                                                                                                                                   | <span data-ttu-id="19627-127">Описание процесса обработки сообщений о запросах регистрации с устройств.</span><span class="sxs-lookup"><span data-stu-id="19627-127">Describes how to process registration request messages from devices.</span></span>                                                                       |
| [<span data-ttu-id="19627-128">Выполнение обнаружения близлежащих устройств</span><span class="sxs-lookup"><span data-stu-id="19627-128">Performing Proximity Detection</span></span>](performing-proximity-detection.md)                                                                                                             | <span data-ttu-id="19627-129">Описывает процесс обнаружения близлежащих устройств.</span><span class="sxs-lookup"><span data-stu-id="19627-129">Describes the proximity detection process.</span></span>                                                                                                 |
| [<span data-ttu-id="19627-130">Преобразование файла DRM-Protected в поток Windows Media DRM 10 для сетевых устройств</span><span class="sxs-lookup"><span data-stu-id="19627-130">Converting a DRM-Protected File to a Windows Media DRM 10 for Network Devices Stream</span></span>](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | <span data-ttu-id="19627-131">Описывает, как преобразовать защищенный DRM файл в поток, который можно отправить на устройство, использующее Windows Media DRM 10 для сетевых устройств.</span><span class="sxs-lookup"><span data-stu-id="19627-131">Describes how to convert a DRM-protected file to a stream that can be sent to a device that uses Windows Media DRM 10 for Network Devices.</span></span> |



 

> [!Note]  
> <span data-ttu-id="19627-132">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="19627-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="19627-133">См. также</span><span class="sxs-lookup"><span data-stu-id="19627-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19627-134">**Включение поддержки DRM**</span><span class="sxs-lookup"><span data-stu-id="19627-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




