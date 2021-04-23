---
description: Объект Drive
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Объект Drive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264656"
---
# <a name="drive-object"></a><span data-ttu-id="79cfe-103">Объект Drive</span><span class="sxs-lookup"><span data-stu-id="79cfe-103">Drive Object</span></span>

<span data-ttu-id="79cfe-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="79cfe-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="79cfe-105">Объект Drive моделирует физический диск, содержащийся в подсистеме.</span><span class="sxs-lookup"><span data-stu-id="79cfe-105">A drive object models a physical disk drive that is contained within a subsystem.</span></span> <span data-ttu-id="79cfe-106">Каждый диск подключается к шине, занимает слот и содержит набор экстентов диска.</span><span class="sxs-lookup"><span data-stu-id="79cfe-106">Each drive connects to a bus, occupies a slot, and contains a set of drive extents.</span></span> <span data-ttu-id="79cfe-107">Каждый диск может добавлять экстенты в любое количество LUN.</span><span class="sxs-lookup"><span data-stu-id="79cfe-107">Each drive can contribute extents to any number of LUNs.</span></span> <span data-ttu-id="79cfe-108">Диск также можно назначить горячим резервом.</span><span class="sxs-lookup"><span data-stu-id="79cfe-108">A drive can also be designated as a hot spare.</span></span>

<span data-ttu-id="79cfe-109">Используйте метод [**ивдссубсистем:: куеридривес**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) , чтобы определить диски, содержащиеся в определенной подсистеме.</span><span class="sxs-lookup"><span data-stu-id="79cfe-109">Use the [**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) method to determine the drives that are contained by a specific subsystem.</span></span> <span data-ttu-id="79cfe-110">Вызывающие объекты могут получить указатель на конкретный диск, выбрав нужный объект диска из перечисления, возвращаемого методом **куеридривес** , или вызвав метод [**ивдссубсистем::**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) GetObject и передав требуемую шину и номер слота.</span><span class="sxs-lookup"><span data-stu-id="79cfe-110">Callers can get a pointer to a specific drive by selecting the desired drive object from the enumeration that is returned by the **QueryDrives** method, or by invoking the [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) method and passing in the desired bus and slot number.</span></span> <span data-ttu-id="79cfe-111">С помощью объекта Drive можно задать состояние диска и запрос свойств диска, связанных областей диска и подсистемы, содержащей диск.</span><span class="sxs-lookup"><span data-stu-id="79cfe-111">With a drive object, you can set the drive status and query for drive properties, associated drive extents, and the subsystem containing the drive.</span></span>

<span data-ttu-id="79cfe-112">В дополнение к идентификатору объекта, имени и серийному номеру свойства объекта диска включают состояние диска, работоспособность и флаги. Размер в байтах; и номер шины и разъема.</span><span class="sxs-lookup"><span data-stu-id="79cfe-112">In addition to an object identifier, a name, and a serial number, drive object properties include the drive status, health, and flags; the size in bytes; and a bus and slot number.</span></span>

<span data-ttu-id="79cfe-113">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="79cfe-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="79cfe-114">Тип</span><span class="sxs-lookup"><span data-stu-id="79cfe-114">Type</span></span>                                              | <span data-ttu-id="79cfe-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="79cfe-115">Element</span></span>                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79cfe-116">Интерфейсы, которые всегда предоставляются этим объектом</span><span class="sxs-lookup"><span data-stu-id="79cfe-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="79cfe-117">**ивдсдриве**</span><span class="sxs-lookup"><span data-stu-id="79cfe-117">**IVdsDrive**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| <span data-ttu-id="79cfe-118">Интерфейсы, которые могут предоставляться этим объектом</span><span class="sxs-lookup"><span data-stu-id="79cfe-118">Interfaces that may be exposed by this object</span></span>     | [<span data-ttu-id="79cfe-119">**ивдсмаинтенанце**</span><span class="sxs-lookup"><span data-stu-id="79cfe-119">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| <span data-ttu-id="79cfe-120">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="79cfe-120">Associated enumerations</span></span>                           | <span data-ttu-id="79cfe-121">Служба [**VDS \_ \_Флаг диска**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ состояние диска VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)и [**\_ \_ экстент диска VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span><span class="sxs-lookup"><span data-stu-id="79cfe-121">[**VDS\_DRIVE\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**VDS\_DRIVE\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status), and [**VDS\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span></span> |
| <span data-ttu-id="79cfe-122">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="79cfe-122">Associated structures</span></span>                             | <span data-ttu-id="79cfe-123">Служба [**VDS \_ Уведомление \_ Drive**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) и [**\_ устройство VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span><span class="sxs-lookup"><span data-stu-id="79cfe-123">[**VDS\_DRIVE\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) and [**VDS\_DRIVE\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="79cfe-124">См. также</span><span class="sxs-lookup"><span data-stu-id="79cfe-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79cfe-125">Объекты поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="79cfe-125">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="79cfe-126">**Ивдссубсистем:: Куеридривес**</span><span class="sxs-lookup"><span data-stu-id="79cfe-126">**IVdsSubSystem::QueryDrives**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[<span data-ttu-id="79cfe-127">**Ивдссубсистем:: OverDrive**</span><span class="sxs-lookup"><span data-stu-id="79cfe-127">**IVdsSubSystem::GetDrive**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
