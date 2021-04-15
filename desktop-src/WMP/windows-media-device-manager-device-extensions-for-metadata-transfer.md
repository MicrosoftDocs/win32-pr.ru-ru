---
title: Расширения устройств Windows Media диспетчер устройств для передачи метаданных
description: Расширения устройств Windows Media диспетчер устройств для передачи метаданных
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Проигрыватель Windows Media, расширения устройств
- Проигрыватель Windows Media, расширения
- Проигрыватель Windows Media, метаданные
- Проигрыватель Windows Media, Ускоренная перенаправление метаданных
- Проигрыватель Windows Media, ускорение передачи метаданных
- метаданные, расширения устройств
- метаданные, расширения
- расширения устройств, перенос метаданных
- расширения, перенос метаданных
- Ускоренная перенаправление метаданных
- метаданные, ускорение перемещения
- расширения устройств, Ускоренная перенаправление метаданных
- расширения, Ускоренная перенаправление метаданных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486881"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a><span data-ttu-id="bbf29-116">Расширения устройств Windows Media диспетчер устройств для передачи метаданных</span><span class="sxs-lookup"><span data-stu-id="bbf29-116">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>

<span data-ttu-id="bbf29-117">Чтобы включить ускоренную пересылку метаданных, производители устройств, которые не поддерживают MTP, должны выполнить следующие действия в исходном коде:</span><span class="sxs-lookup"><span data-stu-id="bbf29-117">To enable accelerated metadata transfer, manufacturers of devices that do not support MTP must do the following in source code:</span></span>

-   <span data-ttu-id="bbf29-118">Определение **\_ \_ \_ поддержки устройств WMP вмдм**.</span><span class="sxs-lookup"><span data-stu-id="bbf29-118">Define **WMP\_WMDM\_DEVICE\_SUPPORT**.</span></span>
-   <span data-ttu-id="bbf29-119">Включите вмпдевицес. h, который устанавливается как часть пакета SDK для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bbf29-119">Include wmpdevices.h, which is installed as part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="bbf29-120">Вмпдевицес. h определяет следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="bbf29-120">Wmpdevices.h defines the following structures.</span></span>



| <span data-ttu-id="bbf29-121">Структура</span><span class="sxs-lookup"><span data-stu-id="bbf29-121">Structure</span></span>                                                                                 | <span data-ttu-id="bbf29-122">Описание</span><span class="sxs-lookup"><span data-stu-id="bbf29-122">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbf29-123">Проигрыватель \_ WMP \_ вмдм \_ цикл \_ обработки метаданных \_ PC2DEVICE</span><span class="sxs-lookup"><span data-stu-id="bbf29-123">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | <span data-ttu-id="bbf29-124">Структура, используемая проигрывателем Windows Media для запроса сведений о синхронизации метаданных с портативных устройств, которые не поддерживают MTP.</span><span class="sxs-lookup"><span data-stu-id="bbf29-124">Structure used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |
| [<span data-ttu-id="bbf29-125">Проигрыватель \_ WMP \_ вмдм \_ цикл \_ обработки метаданных \_ DEVICE2PC</span><span class="sxs-lookup"><span data-stu-id="bbf29-125">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | <span data-ttu-id="bbf29-126">Структура, используемая проигрывателем Windows Media для получения данных ускоренной синхронизации метаданных с портативных устройств, которые не поддерживают MTP.</span><span class="sxs-lookup"><span data-stu-id="bbf29-126">Structure used by Windows Media Player to receive accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |



 

<span data-ttu-id="bbf29-127">Чтобы запросить от устройства сведения об измененных метаданных, проигрыватель Windows Media 10 или более поздней версии вызывает метод Windows Media диспетчер устройств Method **IWMDMDevice3::D евицеиоконтрол**.</span><span class="sxs-lookup"><span data-stu-id="bbf29-127">To request information from the device about metadata that has changed, Windows Media Player 10 or later calls the Windows Media Device Manager method **IWMDMDevice3::DeviceIoControl**.</span></span> <span data-ttu-id="bbf29-128">При выполнении этого вызова игрок выполняет определенные действия следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bbf29-128">When making this call, the Player follows specific steps, as follows:</span></span>

-   <span data-ttu-id="bbf29-129">Первый параметр, *двиоконтролкоде*, содержит константу **\_ \_ \_ цикла \_ обработки метаданных WMP ioctl**.</span><span class="sxs-lookup"><span data-stu-id="bbf29-129">The first parameter, *dwIoControlCode*, contains the constant **IOCTL\_WMP\_METADATA\_ROUND\_TRIP**.</span></span> <span data-ttu-id="bbf29-130">Эта константа определена в вмпдевицес. h.</span><span class="sxs-lookup"><span data-stu-id="bbf29-130">This constant is defined in wmpdevices.h.</span></span>
-   <span data-ttu-id="bbf29-131">Второй параметр, *лпинбуффер*, указывает на структуру **проигрывателя WMP вмдм в виде \_ \_ \_ кругового пути \_ \_ PC2DEVICE** .</span><span class="sxs-lookup"><span data-stu-id="bbf29-131">The second parameter, *lpInBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE** structure.</span></span>
-   <span data-ttu-id="bbf29-132">Третий параметр, *нинбуфферсизе*, содержит размер входного буфера.</span><span class="sxs-lookup"><span data-stu-id="bbf29-132">The third parameter, *nInBufferSize*, contains the size of the input buffer.</span></span>
-   <span data-ttu-id="bbf29-133">Четвертый параметр, *лпаутбуффер*, указывает на структуру вмдм пути к **\_ \_ \_ циклической \_ обработки \_ метаданных проигрывателя WMP DEVICE2PC** .</span><span class="sxs-lookup"><span data-stu-id="bbf29-133">The fourth parameter, *lpOutBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC** structure.</span></span> <span data-ttu-id="bbf29-134">Устройство должно заполнить эту структуру сведениями об изменениях.</span><span class="sxs-lookup"><span data-stu-id="bbf29-134">The device must fill in this structure with information about changes.</span></span>
-   <span data-ttu-id="bbf29-135">Пятый параметр *пнаутбуфферсизе* получает размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="bbf29-135">The fifth parameter, *pnOutBufferSize*, receives the size of the output buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbf29-136">См. также</span><span class="sxs-lookup"><span data-stu-id="bbf29-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbf29-137">**Расширения устройств для ускоренной пересылки метаданных**</span><span class="sxs-lookup"><span data-stu-id="bbf29-137">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




