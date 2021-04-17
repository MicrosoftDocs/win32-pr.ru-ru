---
description: Объект пула носителей моделирует пул носителей в подсистеме хранения.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Объект пула носителей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674327"
---
# <a name="storage-pool-object"></a><span data-ttu-id="feeb8-103">Объект пула носителей</span><span class="sxs-lookup"><span data-stu-id="feeb8-103">Storage Pool Object</span></span>

<span data-ttu-id="feeb8-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="feeb8-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="feeb8-105">Объект пула носителей моделирует пул носителей в подсистеме хранения.</span><span class="sxs-lookup"><span data-stu-id="feeb8-105">A storage pool object models a storage pool in a storage subsystem.</span></span>

<span data-ttu-id="feeb8-106">Пул носителей содержит экстенты дисков с одного или нескольких дисков, управляемых одним и тем же поставщиком оборудования.</span><span class="sxs-lookup"><span data-stu-id="feeb8-106">A storage pool contains drive extents from one or more drives that are managed by the same hardware provider.</span></span>

<span data-ttu-id="feeb8-107">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="feeb8-107">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="feeb8-108">Тип</span><span class="sxs-lookup"><span data-stu-id="feeb8-108">Type</span></span>                                              | <span data-ttu-id="feeb8-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="feeb8-109">Element</span></span>                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feeb8-110">Интерфейсы, которые всегда предоставляются этим объектом</span><span class="sxs-lookup"><span data-stu-id="feeb8-110">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="feeb8-111">**ивдссторажепул**</span><span class="sxs-lookup"><span data-stu-id="feeb8-111">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| <span data-ttu-id="feeb8-112">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="feeb8-112">Associated enumerations</span></span>                           | <span data-ttu-id="feeb8-113">Служба [**VDS \_ \_Тип RAID**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**\_ \_ \_ Состояние пула хранилища VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)и [**\_ \_ \_ Тип пула хранилища VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span><span class="sxs-lookup"><span data-stu-id="feeb8-113">[**VDS\_RAID\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**VDS\_STORAGE\_POOL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status), and [**VDS\_STORAGE\_POOL\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span></span>                                                                                                                                  |
| <span data-ttu-id="feeb8-114">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="feeb8-114">Associated structures</span></span>                             | <span data-ttu-id="feeb8-115">Служба [**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**\_ \_ Атрибуты пула VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ настраиваемые \_ Атрибуты пула службы VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**\_ \_ \_ \_ область диска пула носителей VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)и " [**\_ \_ \_ prop" пула носителей VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span><span class="sxs-lookup"><span data-stu-id="feeb8-115">[**VDS\_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**VDS\_POOL\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**VDS\_POOL\_CUSTOM\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**VDS\_STORAGE\_POOL\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent), and [**VDS\_STORAGE\_POOL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span></span> |



 

 

 
