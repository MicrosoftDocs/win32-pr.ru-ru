---
description: Объект плекса LUN
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: Объект плекса LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693654"
---
# <a name="lun-plex-object"></a><span data-ttu-id="3caeb-103">Объект плекса LUN</span><span class="sxs-lookup"><span data-stu-id="3caeb-103">LUN Plex Object</span></span>

<span data-ttu-id="3caeb-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3caeb-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="3caeb-105">Объект плекса LUN моделирует Плекс LUN, содержащийся в LUN.</span><span class="sxs-lookup"><span data-stu-id="3caeb-105">A LUN plex object models a LUN plex that is contained by a LUN.</span></span> <span data-ttu-id="3caeb-106">Только зеркальный LUN может иметь несколько плексов; все остальные типы LUN имеют один плекс.</span><span class="sxs-lookup"><span data-stu-id="3caeb-106">Only a mirrored LUN can have multiple plexes; all other LUN types have one plex.</span></span> <span data-ttu-id="3caeb-107">Каждый плекс содержит копию данных на LUN.</span><span class="sxs-lookup"><span data-stu-id="3caeb-107">Each plex contains a copy of the data on the LUN.</span></span> <span data-ttu-id="3caeb-108">Новые плекса можно добавить в LUN, и, за исключением исходного плекса, существующие плексов можно удалить.</span><span class="sxs-lookup"><span data-stu-id="3caeb-108">New plexes can be added to a LUN, and, with the exception of the original plex, existing plexes can be removed.</span></span> <span data-ttu-id="3caeb-109">VDS поддерживает четыре типа плексов LUN: простой, составной, чередующийся и чередующийся с четностью.</span><span class="sxs-lookup"><span data-stu-id="3caeb-109">VDS supports four LUN plex types: simple, spanned, striped, and striped with parity.</span></span> <span data-ttu-id="3caeb-110">Описание каждого из этих типов LUN см. в разделе [объект LUN](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="3caeb-110">For a description of each of these LUN types, see the [LUN Object](lun-object.md).</span></span>

<span data-ttu-id="3caeb-111">Используйте метод [**ивдслун:: аддплекс**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) , чтобы добавить ПЛЕКС в LUN и метод [**Ивдслун:: ремовеплекс**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) , чтобы удалить плекс.</span><span class="sxs-lookup"><span data-stu-id="3caeb-111">Use the [**IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) method to add a plex to a LUN and the [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) method to delete the plex.</span></span> <span data-ttu-id="3caeb-112">Вы можете запросить Плекс LUN, вызвав метод [**ивдслун:: куериплексес**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) .</span><span class="sxs-lookup"><span data-stu-id="3caeb-112">You can query for LUN plexes by invoking the [**IVdsLun::QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) method.</span></span> <span data-ttu-id="3caeb-113">Вы можете получить указатель на конкретный Плекс LUN, выбрав нужный объект плекса из перечисления, возвращаемого методом **куериплексес** .</span><span class="sxs-lookup"><span data-stu-id="3caeb-113">You can get a pointer to a specific LUN plex by selecting the desired plex object from the enumeration that is returned by the **QueryPlexes** method.</span></span> <span data-ttu-id="3caeb-114">С помощью объекта плекса можно запрашивать экстенты диска и подсказки для автомагическия, а также применять новые подсказки.</span><span class="sxs-lookup"><span data-stu-id="3caeb-114">With a plex object, you can query for the drive extents and automagic hints, and apply new hints.</span></span>

<span data-ttu-id="3caeb-115">В дополнение к идентификатору объекта, имени и серийному номеру свойства объекта плекса LUN включают тип плекса, размер, состояние, работоспособность, состояние перехода и флаги. расмаскирование списка и размера блока чередования; и параметр приоритета перестроения.</span><span class="sxs-lookup"><span data-stu-id="3caeb-115">In addition to an object identifier, a name, and a serial number, LUN plex object properties include the plex type, size, status, health, transition state, and flags; an unmasking list and stripe size; and a rebuild priority setting.</span></span>

<span data-ttu-id="3caeb-116">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="3caeb-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="3caeb-117">Тип</span><span class="sxs-lookup"><span data-stu-id="3caeb-117">Type</span></span>                                              | <span data-ttu-id="3caeb-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="3caeb-118">Element</span></span>                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3caeb-119">Интерфейсы, которые всегда предоставляются этим объектом</span><span class="sxs-lookup"><span data-stu-id="3caeb-119">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="3caeb-120">[**Ивдслунплекс**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span><span class="sxs-lookup"><span data-stu-id="3caeb-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span></span>                                                                                                                              |
| <span data-ttu-id="3caeb-121">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="3caeb-121">Associated enumerations</span></span>                           | <span data-ttu-id="3caeb-122">Служба [**VDS \_ \_ \_ Флаг плекса Plex**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**\_ \_ \_ состояние плекса LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)и [**\_ \_ \_ тип плекса LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span><span class="sxs-lookup"><span data-stu-id="3caeb-122">[**VDS\_LUN\_PLEX\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS\_LUN\_PLEX\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status), and [**VDS\_LUN\_PLEX\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span></span> |
| <span data-ttu-id="3caeb-123">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="3caeb-123">Associated structures</span></span>                             | <span data-ttu-id="3caeb-124">Служба [**VDS \_ " \_ \_ prop Plex**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop)".</span><span class="sxs-lookup"><span data-stu-id="3caeb-124">[**VDS\_LUN\_PLEX\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span></span>                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="3caeb-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3caeb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3caeb-126">Объекты поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="3caeb-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="3caeb-127">LUN, объект</span><span class="sxs-lookup"><span data-stu-id="3caeb-127">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

 
