---
description: Объект Portal
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Объект Portal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01328d8dccfe7a29c0686cde9b531df63d56e63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693653"
---
# <a name="portal-object"></a><span data-ttu-id="ff581-103">Объект Portal</span><span class="sxs-lookup"><span data-stu-id="ff581-103">Portal Object</span></span>

<span data-ttu-id="ff581-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ff581-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="ff581-105">Объект портала моделирует портал iSCSI, содержащийся в подсистеме iSCSI.</span><span class="sxs-lookup"><span data-stu-id="ff581-105">A portal object models an iSCSI portal that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="ff581-106">Чтобы определить порталы iSCSI подсистемы, используйте метод [**ивдссубсистемискси:: куерипорталс**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) .</span><span class="sxs-lookup"><span data-stu-id="ff581-106">Use the [**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) method to determine the iSCSI portals of the subsystem.</span></span> <span data-ttu-id="ff581-107">Вызывающие объекты могут получить указатель на конкретный портал, выбрав нужный объект портала из перечисления, возвращаемого методом **куерипорталс** .</span><span class="sxs-lookup"><span data-stu-id="ff581-107">Callers can get a pointer to a specific portal by selecting the desired portal object from the enumeration that is returned by the **QueryPortals** method.</span></span> <span data-ttu-id="ff581-108">С помощью объекта портала можно задать состояние портала и запрос свойств портала, связанных групп портала и подсистемы, содержащей портал.</span><span class="sxs-lookup"><span data-stu-id="ff581-108">With a portal object, you can set the portal status and query for portal properties, associated portal groups, and the subsystem that contains the portal.</span></span>

<span data-ttu-id="ff581-109">Объект портала может быть связан только с одной группой портала указанного целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ff581-109">A portal object can only be associated with at most one portal group of a specified target.</span></span>

<span data-ttu-id="ff581-110">Порталы служат одной из конечных точек путей MPIO в поставщиках оборудования iSCSI, на которых можно налагать политики балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ff581-110">Portals serve as one of the endpoints of MPIO paths in iSCSI hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="ff581-111">К свойствам объекта портала относятся идентификатор объекта, IP-адрес и порт, а также состояние портала.</span><span class="sxs-lookup"><span data-stu-id="ff581-111">Portal object properties include an object identifier, an IP address and port, and the portal status.</span></span>

<span data-ttu-id="ff581-112">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="ff581-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="ff581-113">Тип</span><span class="sxs-lookup"><span data-stu-id="ff581-113">Type</span></span>                                                                                      | <span data-ttu-id="ff581-114">Элемент</span><span class="sxs-lookup"><span data-stu-id="ff581-114">Element</span></span>                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff581-115">Интерфейсы, которые всегда предоставляются этим объектом в поставщиках iSCSI для VDS 1,1 и 2,0</span><span class="sxs-lookup"><span data-stu-id="ff581-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="ff581-116">[**Ивдсисксипортал**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span><span class="sxs-lookup"><span data-stu-id="ff581-116">[**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).</span></span>                                                                             |
| <span data-ttu-id="ff581-117">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="ff581-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="ff581-118">Служба [**VDS \_ \_ \_ состояние портала iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span><span class="sxs-lookup"><span data-stu-id="ff581-118">[**VDS\_ISCSI\_PORTAL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).</span></span>                                                          |
| <span data-ttu-id="ff581-119">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="ff581-119">Associated structures</span></span>                                                                     | <span data-ttu-id="ff581-120">Служба [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) [**\_ \_ Уведомление о портах и службе VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)портала iSCSI.</span><span class="sxs-lookup"><span data-stu-id="ff581-120">[**VDS\_ISCSI\_PORTAL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ff581-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ff581-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff581-122">Объекты поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="ff581-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="ff581-123">**Ивдссубсистемискси:: Куерипорталс**</span><span class="sxs-lookup"><span data-stu-id="ff581-123">**IVdsSubSystemIscsi::QueryPortals**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
