---
description: Объект подсистемы
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Объект подсистемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104570906"
---
# <a name="subsystem-object"></a><span data-ttu-id="74746-103">Объект подсистемы</span><span class="sxs-lookup"><span data-stu-id="74746-103">Subsystem Object</span></span>

<span data-ttu-id="74746-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="74746-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="74746-105">Объект подсистемы моделирует подсистему хранения.</span><span class="sxs-lookup"><span data-stu-id="74746-105">A subsystem object models a storage subsystem.</span></span> <span data-ttu-id="74746-106">Подсистема — это либо RAID-корпус, либо карта PCI RAID.</span><span class="sxs-lookup"><span data-stu-id="74746-106">A subsystem is either a RAID enclosure or a PCI RAID card.</span></span> <span data-ttu-id="74746-107">Один главный компьютер может быть подключен к любому количеству подсистем.</span><span class="sxs-lookup"><span data-stu-id="74746-107">A single host computer can be connected to any number of subsystems.</span></span> <span data-ttu-id="74746-108">Каждая подсистема управляется только одним поставщиком оборудования.</span><span class="sxs-lookup"><span data-stu-id="74746-108">Each subsystem is managed by exactly one hardware provider.</span></span> <span data-ttu-id="74746-109">В конфигурации сети SAN класс подсистемы представляет корпус хранилища SAN.</span><span class="sxs-lookup"><span data-stu-id="74746-109">In a SAN configuration, the subsystem class represents a SAN storage enclosure.</span></span>

<span data-ttu-id="74746-110">Подсистема может содержать любое количество контроллеров и дисков, а также может отображать (расмаску) любое количество LUN на компьютере, на котором работает поставщик оборудования.</span><span class="sxs-lookup"><span data-stu-id="74746-110">A subsystem can contain any number of controllers and drives, and can surface (unmask) any number of LUNs to the computer on which the hardware provider is running.</span></span> <span data-ttu-id="74746-111">Более высокие подсистемы могут снять маску LUN для других компьютеров в сети.</span><span class="sxs-lookup"><span data-stu-id="74746-111">Higher-end subsystems can unmask LUNs to other computers on the network.</span></span> <span data-ttu-id="74746-112">Каждый диск в подсистеме подключается к шине и занимает слот на шине.</span><span class="sxs-lookup"><span data-stu-id="74746-112">Each disk drive within a subsystem is connected to a bus and occupies a slot in the bus.</span></span> <span data-ttu-id="74746-113">Каждый контроллер в подсистеме имеет один или несколько портов контроллера.</span><span class="sxs-lookup"><span data-stu-id="74746-113">Each controller within a subsystem has one or more controller ports.</span></span>

<span data-ttu-id="74746-114">На рисунке ниже показаны физические устройства, содержащиеся в подсистеме (LUN не показаны), и связи между ними.</span><span class="sxs-lookup"><span data-stu-id="74746-114">The illustration that follows shows the physical devices contained in a subsystem (LUNs are not shown) and the relationships among them.</span></span>

![Схема, на которой показана подсистема, начинающаяся с "Ports" слева, переход на "контроллеры", а затем "шина" с "разъемами", ведущими к отдельным "дискам".](images/vdssubsystem.png)

<span data-ttu-id="74746-116">Приложения VDS используют метод [**ивдшвпровидер:: куерисубсистемс**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) для запроса подсистем, относящихся к определенному поставщику оборудования.</span><span class="sxs-lookup"><span data-stu-id="74746-116">VDS applications use the [**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) method to query the subsystems that belong to a specific hardware provider.</span></span> <span data-ttu-id="74746-117">Вызывающие объекты могут получить указатель на определенную подсистему, выбрав нужный объект подсистемы из перечисления, возвращаемого методом **куерисубсистемс** .</span><span class="sxs-lookup"><span data-stu-id="74746-117">Callers can get a pointer to a specific subsystem by selecting the desired subsystem object from the enumeration that is returned by the **QuerySubSystems** method.</span></span> <span data-ttu-id="74746-118">С помощью объекта подсистемы можно задать состояние подсистемы, создать LUN, заменить диски и запросить контроллеры, диски и LUN.</span><span class="sxs-lookup"><span data-stu-id="74746-118">With a subsystem object, you can set the subsystem status, create LUNs, replace drives, and query for controllers, drives, and LUNs.</span></span>

<span data-ttu-id="74746-119">В дополнение к идентификатору объекта, имени и серийному номеру свойства объекта подсистемы включают состояние подсистемы, работоспособность и флаги. число контроллеров, слотов и шин; и параметр приоритета перестроения.</span><span class="sxs-lookup"><span data-stu-id="74746-119">In addition to an object identifier, a name, and a serial number, subsystem object properties include the subsystem status, health, and flags; a count of the controllers, slots, and buses; and a rebuild priority setting.</span></span>

<span data-ttu-id="74746-120">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="74746-120">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="74746-121">Тип</span><span class="sxs-lookup"><span data-stu-id="74746-121">Type</span></span>                                                                                      | <span data-ttu-id="74746-122">Элемент</span><span class="sxs-lookup"><span data-stu-id="74746-122">Element</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74746-123">Интерфейсы, которые всегда предоставляются этим объектом</span><span class="sxs-lookup"><span data-stu-id="74746-123">Interfaces that are always exposed by this object</span></span>                                         | <span data-ttu-id="74746-124">[**Ивдссубсистем**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span><span class="sxs-lookup"><span data-stu-id="74746-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span></span>                                                                                          |
| <span data-ttu-id="74746-125">Интерфейсы, которые всегда предоставляются этим объектом в поставщиках iSCSI для VDS 1,1 и 2,0</span><span class="sxs-lookup"><span data-stu-id="74746-125">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="74746-126">[**Ивдссубсистемискси**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) и [**ивдссубсистемимпорттаржет**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span><span class="sxs-lookup"><span data-stu-id="74746-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) and [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span></span>             |
| <span data-ttu-id="74746-127">Интерфейсы, которые могут предоставляться этим объектом</span><span class="sxs-lookup"><span data-stu-id="74746-127">Interfaces that may be exposed by this object</span></span>                                             | <span data-ttu-id="74746-128">[**Ивдссубсистемнаминг**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) и [**ивдсмаинтенанце**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span><span class="sxs-lookup"><span data-stu-id="74746-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) and [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span></span>                               |
| <span data-ttu-id="74746-129">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="74746-129">Associated enumerations</span></span>                                                                   | <span data-ttu-id="74746-130">Служба [**VDS \_ \_ \_ Флаг подсистемы**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) и [**\_ \_ \_ состояние подсистемы VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span><span class="sxs-lookup"><span data-stu-id="74746-130">[**VDS\_SUB\_SYSTEM\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) and [**VDS\_SUB\_SYSTEM\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span></span>             |
| <span data-ttu-id="74746-131">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="74746-131">Associated structures</span></span>                                                                     | <span data-ttu-id="74746-132">Служба [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) [**\_ \_ \_ Уведомление подсистемы**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification)подсистемы Prop и VDS.</span><span class="sxs-lookup"><span data-stu-id="74746-132">[**VDS\_SUB\_SYSTEM\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) and [**VDS\_SUB\_SYSTEM\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="74746-133">См. также</span><span class="sxs-lookup"><span data-stu-id="74746-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74746-134">Объекты поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="74746-134">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="74746-135">**Ивдшвпровидер:: Куерисубсистемс**</span><span class="sxs-lookup"><span data-stu-id="74746-135">**IVdsHwProvider::QuerySubSystems**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
