---
description: Перечисление и обновление
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Перечисление и обновление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693167"
---
# <a name="reenumerating-and-refreshing"></a><span data-ttu-id="27470-103">Перечисление и обновление</span><span class="sxs-lookup"><span data-stu-id="27470-103">Reenumerating and Refreshing</span></span>

<span data-ttu-id="27470-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="27470-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="27470-105">Операция переперечисления находит только что подключенные и вновь Отключенные устройства.</span><span class="sxs-lookup"><span data-stu-id="27470-105">The reenumeration operation discovers newly connected and newly disconnected devices.</span></span> <span data-ttu-id="27470-106">Операция обновления обновляет сведения о конфигурации существующих устройств.</span><span class="sxs-lookup"><span data-stu-id="27470-106">The refresh operation updates the configuration information of existing devices.</span></span>

<span data-ttu-id="27470-107">**Перечисление объектов поставщика программного обеспечения**</span><span class="sxs-lookup"><span data-stu-id="27470-107">**To reenumerate software provider objects**</span></span>

-   <span data-ttu-id="27470-108">Вызовите метод [**ивдссервице:: reenumerat**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="27470-108">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method.</span></span> <span data-ttu-id="27470-109">Этот метод обнаруживает все подключенные и отключенные диски и дисководы компакт-дисков, а также гарантирует, что все диски имеют соответствующего владельца.</span><span class="sxs-lookup"><span data-stu-id="27470-109">This method discovers all newly connected and disconnected disks and CD-ROM drives, and ensures that all disks have the proper owner.</span></span> <span data-ttu-id="27470-110">Служба VDS владеет необработанными дисками или дисками с ошибками; базовый поставщик владеет базовыми дисками; и динамический поставщик владеет динамическими дисками.</span><span class="sxs-lookup"><span data-stu-id="27470-110">VDS owns raw disks or disks with failures; the basic provider owns basic disks; and the dynamic provider owns dynamic disks.</span></span> <span data-ttu-id="27470-111">Эта операция может содержать проверку внутренних шин подсистем и Ожидание истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="27470-111">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="27470-112">**Перечисление и обновление объектов поставщика программного обеспечения**</span><span class="sxs-lookup"><span data-stu-id="27470-112">**To reenumerate and refresh software provider objects**</span></span>

-   <span data-ttu-id="27470-113">Вызовите метод [**ивдссервице:: reenumerat**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) , а затем вызовите метод [**Ивдссервице:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) .</span><span class="sxs-lookup"><span data-stu-id="27470-113">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method and then call the [**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) method.</span></span> <span data-ttu-id="27470-114">Помимо обнаружения новых подключенных и отключенных дисков и дисководов компакт-дисков, такое сочетание методов обновляет все сведения о диске, Томе и плекса в кэше VDS для дисков, которые не были недавно подключены или отключены.</span><span class="sxs-lookup"><span data-stu-id="27470-114">In addition to discovering newly connected and disconnected disks and CD-ROM drives, this combination of methods updates all disk, volume, and plex information in the VDS cache for disks that have not been recently connected or disconnected.</span></span> <span data-ttu-id="27470-115">Вызовите метод **Refresh** только для обновления сведений о свойствах существующих объектов в кэше.</span><span class="sxs-lookup"><span data-stu-id="27470-115">Call **Refresh** alone to refresh the property information of existing objects in the cache.</span></span> <span data-ttu-id="27470-116">Эта операция может содержать проверку внутренних шин подсистем и Ожидание истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="27470-116">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span> <span data-ttu-id="27470-117">Обратите внимание, что служба VDS автоматически обновляет кэш всякий раз, когда происходит изменение, запускающее уведомление.</span><span class="sxs-lookup"><span data-stu-id="27470-117">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="27470-118">Кроме того, вызов **обновления** в ответ на уведомление VDS может привести к отправке бесконечного цикла уведомлений.</span><span class="sxs-lookup"><span data-stu-id="27470-118">Also, calling **Refresh** in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="27470-119">По этим причинам **Обновление** следует вызывать только в том случае, если кажется, что кэш не обновляется должным образом.</span><span class="sxs-lookup"><span data-stu-id="27470-119">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

<span data-ttu-id="27470-120">**Перечисление аппаратных подсистем**</span><span class="sxs-lookup"><span data-stu-id="27470-120">**To reenumerate hardware subsystems**</span></span>

-   <span data-ttu-id="27470-121">Вызовите метод [**ивдшвпровидер:: reenumerat**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="27470-121">Call the [**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) method.</span></span> <span data-ttu-id="27470-122">В зависимости от поставщика эта операция может задействовать отправку сетевых пакетов и Ожидание истечения времени ожидания, повторное сканирование шин SCSI и Ожидание истечения времени ожидания и т. д.</span><span class="sxs-lookup"><span data-stu-id="27470-122">Depending on the provider, this operation can involve sending network packets and waiting for time-outs, rescanning SCSI buses and waiting for time-outs, and so on.</span></span>

<span data-ttu-id="27470-123">**Перечисление объектов аппаратной подсистемы**</span><span class="sxs-lookup"><span data-stu-id="27470-123">**To reenumerate hardware subsystem objects**</span></span>

-   <span data-ttu-id="27470-124">Вызовите метод [**ивдссубсистем:: reenumerat**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) для инвентаризации объектов (обычно накопителей) в подсистеме.</span><span class="sxs-lookup"><span data-stu-id="27470-124">Call the [**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) method to inventory the objects (typically drives) in the subsystem.</span></span> <span data-ttu-id="27470-125">В зависимости от подсистемы эта операция может содержать проверку внутренних шин подсистем и Ожидание истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="27470-125">Depending on the subsystem, this operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="27470-126">**Обновление подсистем оборудования и объектов подсистемы**</span><span class="sxs-lookup"><span data-stu-id="27470-126">**To refresh hardware subsystems and subsystem objects**</span></span>

-   <span data-ttu-id="27470-127">Вызовите метод [**ивдшвпровидер:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) , чтобы обновить кэш VDS сведений о существующих подсистемах, управляемых поставщиками оборудования VDS.</span><span class="sxs-lookup"><span data-stu-id="27470-127">Call the [**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) method to refresh the VDS cache of information about existing subsystems that are managed by VDS hardware providers.</span></span> <span data-ttu-id="27470-128">Обратите внимание, что служба VDS автоматически обновляет кэш всякий раз, когда происходит изменение, запускающее уведомление.</span><span class="sxs-lookup"><span data-stu-id="27470-128">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="27470-129">Кроме того, вызов [**обновления**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) в ответ на уведомление VDS может привести к отправке бесконечного цикла уведомлений.</span><span class="sxs-lookup"><span data-stu-id="27470-129">Also, calling [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="27470-130">По этим причинам **Обновление** следует вызывать только в том случае, если кажется, что кэш не обновляется должным образом.</span><span class="sxs-lookup"><span data-stu-id="27470-130">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27470-131">См. также</span><span class="sxs-lookup"><span data-stu-id="27470-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27470-132">Использование VDS</span><span class="sxs-lookup"><span data-stu-id="27470-132">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="27470-133">**Ивдссервице:: перечисление**</span><span class="sxs-lookup"><span data-stu-id="27470-133">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="27470-134">**Ивдссервице:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="27470-134">**IVdsService::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[<span data-ttu-id="27470-135">**Ивдшвпровидер:: перечисление**</span><span class="sxs-lookup"><span data-stu-id="27470-135">**IVdsHwProvider::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[<span data-ttu-id="27470-136">**Ивдссубсистем:: перечисление**</span><span class="sxs-lookup"><span data-stu-id="27470-136">**IVdsSubSystem::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[<span data-ttu-id="27470-137">**Ивдшвпровидер:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="27470-137">**IVdsHwProvider::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
