---
title: Расширения устройств для ускоренной пересылки метаданных
description: Расширения устройств для ускоренной пересылки метаданных
ms.assetid: a79b54d4-dad5-411b-aaff-b58bb549d4d1
keywords:
- Проигрыватель Windows Media, расширения устройств
- Проигрыватель Windows Media, расширения
- Проигрыватель Windows Media, Ускоренная перенаправление метаданных
- Проигрыватель Windows Media, ускорение передачи метаданных
- Ускоренная перенаправление метаданных
- метаданные, ускорение перемещения
- расширения устройств, Ускоренная перенаправление метаданных
- расширения, Ускоренная перенаправление метаданных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe661dff0750f2ad46bef96e537b0852d480db8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068225"
---
# <a name="device-extensions-for-accelerated-metadata-transfer"></a><span data-ttu-id="cb256-111">Расширения устройств для ускоренной пересылки метаданных</span><span class="sxs-lookup"><span data-stu-id="cb256-111">Device Extensions for Accelerated Metadata Transfer</span></span>

<span data-ttu-id="cb256-112">В проигрывателе Windows Media 10 появились новые и расширенные функции для синхронизации цифровых файлов мультимедиа с портативными устройствами.</span><span class="sxs-lookup"><span data-stu-id="cb256-112">Windows Media Player 10 introduced new and extended functionality for synchronizing digital media files with portable devices.</span></span> <span data-ttu-id="cb256-113">Пользователи могут подключать устройства к компьютеру, передавать содержимое на устройство, а затем отключать устройство, чтобы получить доступ к содержимому компьютера.</span><span class="sxs-lookup"><span data-stu-id="cb256-113">Users can connect a device to a computer, transfer content to the device, and then disconnect the device to enjoy content away from the computer.</span></span>

<span data-ttu-id="cb256-114">Когда пользователь повторно подключает устройство к компьютеру, возможно, что содержимое, хранящееся на устройстве, изменилось с момента предыдущего подключения.</span><span class="sxs-lookup"><span data-stu-id="cb256-114">When the user reconnects the device to the computer, it is possible that the content stored on the device changed since the previous connection.</span></span> <span data-ttu-id="cb256-115">Например, простое воспроизведение определенного файла цифрового носителя приводит к изменению счетчика воспроизведения для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="cb256-115">For example, simply playing a particular digital media file causes the play count for that item to change.</span></span> <span data-ttu-id="cb256-116">Поскольку текущие портативные устройства могут хранить большие объемы мультимедийного содержимого, процесс обнаружения изменений будет слишком длительным, если бы проигрыватель Windows Media требовал перечисления и проверки каждого элемента цифрового носителя.</span><span class="sxs-lookup"><span data-stu-id="cb256-116">Because current portable devices can store large quantities of digital media content, the process of discovering changes would be too time consuming if Windows Media Player were required to enumerate and inspect each digital media item.</span></span> <span data-ttu-id="cb256-117">Вместо этого производители портативных устройств могут реализовать специальные функции, позволяющие проигрывателю Windows Media 10 или более поздней версии эффективно получать сведения об изменениях, внесенных в содержимое, хранящееся на устройстве.</span><span class="sxs-lookup"><span data-stu-id="cb256-117">Instead, portable device manufacturers can implement special functionality to enable Windows Media Player 10 or later to efficiently retrieve information about changes made to the content stored on a device.</span></span>

<span data-ttu-id="cb256-118">В следующих разделах описываются соглашения, используемые для реализации этой функции.</span><span class="sxs-lookup"><span data-stu-id="cb256-118">The following sections describe the conventions used to implement this functionality.</span></span>

-   [<span data-ttu-id="cb256-119">Сведения о метаданных</span><span class="sxs-lookup"><span data-stu-id="cb256-119">About the Metadata</span></span>](about-the-metadata.md)
-   [<span data-ttu-id="cb256-120">Расширения устройств MTP для обмена метаданными</span><span class="sxs-lookup"><span data-stu-id="cb256-120">MTP Device Extensions for Metadata Transfer</span></span>](mtp-device-extensions-for-metadata-transfer.md)
-   [<span data-ttu-id="cb256-121">Расширения устройств Windows Media диспетчер устройств для передачи метаданных</span><span class="sxs-lookup"><span data-stu-id="cb256-121">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>](windows-media-device-manager-device-extensions-for-metadata-transfer.md)

## <a name="related-topics"></a><span data-ttu-id="cb256-122">См. также</span><span class="sxs-lookup"><span data-stu-id="cb256-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb256-123">**Проигрыватель Windows Media**</span><span class="sxs-lookup"><span data-stu-id="cb256-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




