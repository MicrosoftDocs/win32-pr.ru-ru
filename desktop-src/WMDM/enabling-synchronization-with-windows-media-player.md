---
title: Включение синхронизации с проигрывателем Windows Media
description: Включение синхронизации с проигрывателем Windows Media
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Диспетчер устройств Windows Media, синхронизация с проигрывателем Windows Media
- Диспетчер устройств, синхронизация с проигрывателем Windows Media
- инструкции по программированию, синхронизация с проигрывателем Windows Media
- поставщики услуг, синхронизация с проигрывателем Windows Media
- Создание поставщиков услуг, синхронизация с проигрывателем Windows Media
- Синхронизация с проигрывателем Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691392"
---
# <a name="enabling-synchronization-with-windows-media-player"></a><span data-ttu-id="040d9-109">Включение синхронизации с проигрывателем Windows Media</span><span class="sxs-lookup"><span data-stu-id="040d9-109">Enabling Synchronization with Windows Media Player</span></span>

<span data-ttu-id="040d9-110">Вы можете разрешить устройству участвовать в автоматической синхронизации с помощью проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="040d9-110">You can enable a device to participate in automatic synchronization with Windows Media Player.</span></span> <span data-ttu-id="040d9-111">Автоматическая синхронизация означает, что когда назначенное пользователем Синхронизированное устройство подключается к компьютеру, проигрыватель Windows Media автоматически скачивает, обновляет или удаляет файлы с устройства, не требуя дополнительных входов пользователя.</span><span class="sxs-lookup"><span data-stu-id="040d9-111">Automatic synchronization means that when a user-designated synchronized device connects to the computer, Windows Media Player will automatically download, update, or delete files from the device without requiring any additional user input.</span></span>

<span data-ttu-id="040d9-112">По умолчанию следующие устройства синхронизируются с проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="040d9-112">By default the following devices are synchronized with Windows Media Player:</span></span>

-   <span data-ttu-id="040d9-113">Устройства MTP</span><span class="sxs-lookup"><span data-stu-id="040d9-113">MTP devices</span></span>
-   <span data-ttu-id="040d9-114">Запоминающие устройства</span><span class="sxs-lookup"><span data-stu-id="040d9-114">Mass-storage devices</span></span>
-   <span data-ttu-id="040d9-115">Устройства Windows CE (проигрыватель Windows Media 10 Mobile и более поздние версии)</span><span class="sxs-lookup"><span data-stu-id="040d9-115">Windows CE devices (Windows Media Player 10 Mobile and later)</span></span>

<span data-ttu-id="040d9-116">Для синхронизации любого другого устройства с проигрывателем Windows Media необходимо соблюдение следующих требований.</span><span class="sxs-lookup"><span data-stu-id="040d9-116">For any other device to synchronize with Windows Media Player, the following requirements must met:</span></span>

-   <span data-ttu-id="040d9-117">Устройство должно объявлять интерфейс PAP-устройства {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span><span class="sxs-lookup"><span data-stu-id="040d9-117">The device must advertise a PAP device interface that is {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span></span>
-   <span data-ttu-id="040d9-118">Объекты устройства, возвращаемые поставщиком службы, должны поддерживать интерфейс **IMDSPDevice3** .</span><span class="sxs-lookup"><span data-stu-id="040d9-118">The device objects returned by service provider must support the **IMDSPDevice3** interface.</span></span>
-   <span data-ttu-id="040d9-119">Параметру устройства Усикстендедвмдм должно быть присвоено значение **DWORD** , равное 1.</span><span class="sxs-lookup"><span data-stu-id="040d9-119">The device parameter UseExtendedWmdm must be set to a **DWORD** value of 1.</span></span> <span data-ttu-id="040d9-120">Дополнительные сведения см. в разделе [Параметры устройства](device-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="040d9-120">See [Device Parameters](device-parameters.md) for more information.</span></span>
-   <span data-ttu-id="040d9-121">Поставщик услуг должен реализовать следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="040d9-121">The service provider should implement the following interfaces:</span></span>

    [<span data-ttu-id="040d9-122">**IMDSPDevice3**</span><span class="sxs-lookup"><span data-stu-id="040d9-122">**IMDSPDevice3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [<span data-ttu-id="040d9-123">**IMDSPObject2**</span><span class="sxs-lookup"><span data-stu-id="040d9-123">**IMDSPObject2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [<span data-ttu-id="040d9-124">**IMDSPStorage4**</span><span class="sxs-lookup"><span data-stu-id="040d9-124">**IMDSPStorage4**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a><span data-ttu-id="040d9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="040d9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="040d9-126">**Создание поставщика услуг**</span><span class="sxs-lookup"><span data-stu-id="040d9-126">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="040d9-127">**Параметры устройства**</span><span class="sxs-lookup"><span data-stu-id="040d9-127">**Device Parameters**</span></span>](device-parameters.md)
</dt> </dl>

 

 




