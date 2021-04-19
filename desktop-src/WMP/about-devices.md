---
title: Сведения об устройствах
description: Сведения об устройствах
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Проигрыватель Windows Media, синхронизация устройств
- Объектная модель проигрывателя Windows Media, синхронизация устройств
- Объектная модель, синхронизация устройств
- Элемент управления ActiveX проигрывателя Windows Media, синхронизация устройств
- Элемент управления ActiveX, синхронизация устройств
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, синхронизация устройств
- Проигрыватель Windows Media Mobile, синхронизация устройств
- синхронизация устройств, сведения
- синхронизация устройств, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691432"
---
# <a name="about-devices"></a><span data-ttu-id="575a3-112">Сведения об устройствах</span><span class="sxs-lookup"><span data-stu-id="575a3-112">About Devices</span></span>

<span data-ttu-id="575a3-113">Портативные устройства — это аппаратные устройства, которые пользователи могут использовать для воспроизведения мультимедийного содержимого, когда они находятся за пределами компьютера.</span><span class="sxs-lookup"><span data-stu-id="575a3-113">Portable devices are hardware devices that users carry to enjoy digital media content when they are away from their computer.</span></span> <span data-ttu-id="575a3-114">Обычно портативные устройства работают от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="575a3-114">Typically, portable devices are battery operated.</span></span> <span data-ttu-id="575a3-115">Некоторые устройства могут играть только музыку.</span><span class="sxs-lookup"><span data-stu-id="575a3-115">Some devices can play music only.</span></span> <span data-ttu-id="575a3-116">Другие устройства могут играть видео и музыку.</span><span class="sxs-lookup"><span data-stu-id="575a3-116">Other devices can play video and music.</span></span>

<span data-ttu-id="575a3-117">Некоторые устройства поддерживают автоматическую синхронизацию цифрового мультимедийного содержимого с проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="575a3-117">Some devices support automatic synchronization of digital media content with Windows Media Player.</span></span> <span data-ttu-id="575a3-118">Другие устройства поддерживают только перенос вручную.</span><span class="sxs-lookup"><span data-stu-id="575a3-118">Other devices support only manual transfer.</span></span> <span data-ttu-id="575a3-119">Можно определить, поддерживает ли определенное устройство автоматическую синхронизацию, вызвав метод [ивмпсинкдевице:: Get \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) , а затем изменив полученное значение [вмпдевицестатус](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) .</span><span class="sxs-lookup"><span data-stu-id="575a3-119">You can determine whether a particular device supports automatic synchronization by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="575a3-120">Если полученное значение — **вмпдсмануалдевице**, устройство не поддерживает автоматическую синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="575a3-120">If the retrieved value is **wmpdsManualDevice**, the device does not support automatic synchronization.</span></span>

<span data-ttu-id="575a3-121">Вы можете перечислить устройства, подключенные к компьютеру пользователя.</span><span class="sxs-lookup"><span data-stu-id="575a3-121">You can enumerate the devices connected to the user's computer.</span></span> <span data-ttu-id="575a3-122">Для этого сначала используйте [ивмпсинксервицес:: Get \_ девицекаунт](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) , чтобы получить количество устройств.</span><span class="sxs-lookup"><span data-stu-id="575a3-122">To do this, first use [IWMPSyncServices::get\_deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) to retrieve the count of devices.</span></span> <span data-ttu-id="575a3-123">Затем в цикле вызовите [ивмпсинксервицес::-Device](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), передавая соответствующее значение индекса каждый раз.</span><span class="sxs-lookup"><span data-stu-id="575a3-123">Then, in a loop, call [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passing the appropriate index value each time.</span></span> <span data-ttu-id="575a3-124">Вы можете использовать [ивмпсинкдевице:: Get \_ Connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) , чтобы определить, подключено ли в настоящее время конкретное устройство.</span><span class="sxs-lookup"><span data-stu-id="575a3-124">You can use [IWMPSyncDevice::get\_connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) to evaluate whether a particular device is currently connected.</span></span>

<span data-ttu-id="575a3-125">Чтобы выяснить, когда устройства подключаются или отключаются, можно получить события **DeviceConnect** и **девицедисконнект** .</span><span class="sxs-lookup"><span data-stu-id="575a3-125">To know when devices connect or disconnect, you can receive the **DeviceConnect** and **DeviceDisconnect** events.</span></span> <span data-ttu-id="575a3-126">Эти события получаются через интерфейс **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="575a3-126">These events are received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="575a3-127">Интерфейс **ивмпсинкдевице** предоставляет дополнительные методы, позволяющие получать или задавать сведения об устройстве.</span><span class="sxs-lookup"><span data-stu-id="575a3-127">The **IWMPSyncDevice** interface provides additional methods to enable you to get or set information about a device.</span></span> <span data-ttu-id="575a3-128">Пример:</span><span class="sxs-lookup"><span data-stu-id="575a3-128">For example:</span></span>

-   <span data-ttu-id="575a3-129">Методы **Get \_ FriendlyName** и **\_ FriendlyName** позволяют извлекать и указывать определяемое пользователем имя устройства.</span><span class="sxs-lookup"><span data-stu-id="575a3-129">The **get\_FriendlyName** and **put\_FriendlyName** methods enable you to retrieve and specify the user-defined device name.</span></span>
-   <span data-ttu-id="575a3-130">Метод **Get \_ DeviceName** позволяет получить имя устройства, которое пользователи видят в оболочке Windows XP.</span><span class="sxs-lookup"><span data-stu-id="575a3-130">The **get\_deviceName** method enables you to retrieve the device name that users see in the Windows XP shell.</span></span>
-   <span data-ttu-id="575a3-131">Метод **getItemInfo** позволяет получать метаданные с устройств.</span><span class="sxs-lookup"><span data-stu-id="575a3-131">The **getItemInfo** method enables you to retrieve metadata from devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="575a3-132">См. также</span><span class="sxs-lookup"><span data-stu-id="575a3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="575a3-133">**Сведения о синхронизации устройств**</span><span class="sxs-lookup"><span data-stu-id="575a3-133">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="575a3-134">**Интерфейс IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="575a3-134">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="575a3-135">**Интерфейс Ивмпсинкдевице**</span><span class="sxs-lookup"><span data-stu-id="575a3-135">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="575a3-136">**Работа с портативными устройствами**</span><span class="sxs-lookup"><span data-stu-id="575a3-136">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




