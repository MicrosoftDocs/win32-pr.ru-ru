---
description: Объекты поставщика программного обеспечения
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Объекты поставщика программного обеспечения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "103913952"
---
# <a name="software-provider-objects"></a><span data-ttu-id="d78c2-103">Объекты поставщика программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="d78c2-103">Software Provider Objects</span></span>

<span data-ttu-id="d78c2-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d78c2-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="d78c2-105">Объекты поставщика программного обеспечения моделируют физические устройства, такие как диски IDE и компакт-диски, а также виртуальные элементы, такие как пакеты, тома и плексов томов.</span><span class="sxs-lookup"><span data-stu-id="d78c2-105">Software provider objects model physical devices, such as IDE disks and CD-ROMs, and virtual elements like packs, volumes, and volume plexes.</span></span> <span data-ttu-id="d78c2-106">На следующем рисунке показана связь между объектом поставщика и набором объектов поставщика программного обеспечения, а также отношение между различными объектами поставщика программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="d78c2-106">The following illustration shows the relationship between the provider object and the set of software provider objects, as well as the relationship between the various software provider objects themselves.</span></span>

![Схема, показывающая связь между поставщиком и объектами поставщика программного обеспечения, такими как "Pack" и "том".](images/vdsswobjects.png)

<span data-ttu-id="d78c2-108">Объект поставщика может содержать ноль или более пакетов.</span><span class="sxs-lookup"><span data-stu-id="d78c2-108">A provider object can contain zero or more packs.</span></span> <span data-ttu-id="d78c2-109">Объект Pack может содержать ноль или более дисков и томов.</span><span class="sxs-lookup"><span data-stu-id="d78c2-109">A pack object can contain zero or more disks and volumes.</span></span> <span data-ttu-id="d78c2-110">Том состоит по крайней мере из одного плекса тома, и каждый Плекс тома может сопоставляться с одним или несколькими дисками в зависимости от типа плекса.</span><span class="sxs-lookup"><span data-stu-id="d78c2-110">A volume comprises of at least one volume plex and each volume plex can map to one or more disks, depending on the plex type.</span></span> <span data-ttu-id="d78c2-111">Служба VDS управляет нераспределенными дисками напрямую без контейнера пакета.</span><span class="sxs-lookup"><span data-stu-id="d78c2-111">VDS manages unallocated disks directly, without a pack container.</span></span> <span data-ttu-id="d78c2-112">В остальных разделах этого раздела описываются объекты типа "пакет", "диск", "том" и "Плекс".</span><span class="sxs-lookup"><span data-stu-id="d78c2-112">The remaining topics of this section describe the pack, disk, volume, and volume plex objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d78c2-113">См. также</span><span class="sxs-lookup"><span data-stu-id="d78c2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d78c2-114">Объектная модель VDS</span><span class="sxs-lookup"><span data-stu-id="d78c2-114">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
