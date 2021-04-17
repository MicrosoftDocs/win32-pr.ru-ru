---
title: О партнерстве
description: О партнерстве
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Проигрыватель Windows Media, партнерство
- Объектная модель проигрывателя Windows Media, партнерство
- Объектная модель, партнерство
- Элемент управления ActiveX проигрывателя Windows Media, партнерство
- Элемент управления ActiveX, партнерство
- Элемент управления ActiveX проигрывателя Windows Media Mobile, партнерство
- Проигрыватель Windows Media Mobile, партнерство
- синхронизация устройств, партнерство
- синхронизация устройств, партнерство
- партнерство между устройствами и проигрывателем Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104487284"
---
# <a name="about-partnerships"></a><span data-ttu-id="1c67b-113">О партнерстве</span><span class="sxs-lookup"><span data-stu-id="1c67b-113">About Partnerships</span></span>

<span data-ttu-id="1c67b-114">Партнерство — это специальная связь между портативным устройством и проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1c67b-114">A partnership is a special relationship between a portable device and Windows Media Player.</span></span> <span data-ttu-id="1c67b-115">Пользователи могут установить связь с определенным устройством с помощью пользовательского интерфейса проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1c67b-115">Users can establish a partnership for a particular device by using the Windows Media Player user interface.</span></span> <span data-ttu-id="1c67b-116">Можно программно управлять партнерством с помощью [ивмпсинкдевице:: креатепартнершип](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) и [Ивмпсинкдевице::d елетепартнершип](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span><span class="sxs-lookup"><span data-stu-id="1c67b-116">You can programmatically manage partnerships by using [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) and [IWMPSyncDevice::deletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span></span> <span data-ttu-id="1c67b-117">Метод **креатепартнершип** запускает асинхронный процесс, который завершается, когда событие **креатепартнершипкомплете** получено через интерфейс **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="1c67b-117">The **createPartnership** method starts an asynchronous process that ends when the **CreatePartnershipComplete** event is received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="1c67b-118">Проигрыватель Windows Media 10 или более поздней версии поддерживает создание связей с до 16 устройств.</span><span class="sxs-lookup"><span data-stu-id="1c67b-118">Windows Media Player 10 or later supports creating partnerships with up to 16 devices.</span></span> <span data-ttu-id="1c67b-119">У каждого партнерства есть связанный индекс партнерства.</span><span class="sxs-lookup"><span data-stu-id="1c67b-119">Each partnership has an associated partnership index.</span></span> <span data-ttu-id="1c67b-120">Индекс партнерства для конкретного устройства можно получить, вызвав [ивмпсинкдевице:: Get \_ партнершипиндекс](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span><span class="sxs-lookup"><span data-stu-id="1c67b-120">You can retrieve the partnership index for a particular device by calling [IWMPSyncDevice::get\_partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span></span> <span data-ttu-id="1c67b-121">Индексы партнерства нумеруются от 1 до 16.</span><span class="sxs-lookup"><span data-stu-id="1c67b-121">Partnership indices are numbered from 1 to 16.</span></span> <span data-ttu-id="1c67b-122">Если определенное устройство не имеет связи с проигрывателем Windows Media Player, **жетпартнершипиндекс** возвращает для индекса нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="1c67b-122">When a particular device does not have a partnership with Windows Media Player, **getPartnershipIndex** returns zero for the index.</span></span>

<span data-ttu-id="1c67b-123">Состояние партнерства конкретного устройства можно получить, вызвав метод [ивмпсинкдевице:: Get \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) , а затем изменив полученное значение [вмпдевицестатус](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) .</span><span class="sxs-lookup"><span data-stu-id="1c67b-123">You can retrieve the partnership status of a particular device by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="1c67b-124">Проигрыватель Windows Media поддерживает одно партнерство с библиотекой одного пользователя на одном компьютере для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="1c67b-124">Windows Media Player allows one partnership with one user's library on one computer for each device.</span></span> <span data-ttu-id="1c67b-125">Это означает, что создание новой связи приведет к удалению любой существующей связи между текущим устройством и другим компьютером.</span><span class="sxs-lookup"><span data-stu-id="1c67b-125">This means that creating a new partnership destroys any existing partnership the current device might have with another computer.</span></span> <span data-ttu-id="1c67b-126">Чтобы иметь представление об изменении состояния устройства, можно получить событие **девицестатусчанже** .</span><span class="sxs-lookup"><span data-stu-id="1c67b-126">To know when the status changes for a device, you can receive the **DeviceStatusChange** event.</span></span>

<span data-ttu-id="1c67b-127">Проигрывателю Windows Media не удается создать связь с устройством с состоянием **вмпдсмануалдевице**.</span><span class="sxs-lookup"><span data-stu-id="1c67b-127">Windows Media Player cannot create a partnership with a device having the status **wmpdsManualDevice**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c67b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1c67b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c67b-129">**Сведения о синхронизации устройств**</span><span class="sxs-lookup"><span data-stu-id="1c67b-129">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="1c67b-130">**Интерфейс IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="1c67b-130">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="1c67b-131">**Работа с портативными устройствами**</span><span class="sxs-lookup"><span data-stu-id="1c67b-131">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




