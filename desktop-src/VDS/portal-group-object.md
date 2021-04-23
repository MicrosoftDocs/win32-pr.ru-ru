---
description: Объект группы портала
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Объект группы портала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c915e76debac959a1dc7684d87c9770033b4aa34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546895"
---
# <a name="portal-group-object"></a><span data-ttu-id="cd72d-103">Объект группы портала</span><span class="sxs-lookup"><span data-stu-id="cd72d-103">Portal Group Object</span></span>

<span data-ttu-id="cd72d-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cd72d-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="cd72d-105">Объект группы портала моделирует группу порталов iSCSI, содержащуюся в целевом объекте iSCSI.</span><span class="sxs-lookup"><span data-stu-id="cd72d-105">A portal group object models an iSCSI portal group that is contained within an iSCSI target.</span></span>

<span data-ttu-id="cd72d-106">Используйте метод [**ивдсискситаржет:: куерипорталграупс**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) , чтобы определить группы порталов, содержащиеся в определенном целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="cd72d-106">Use the [**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) method to determine the portal groups that are contained by a specific target.</span></span> <span data-ttu-id="cd72d-107">Используйте метод [**ивдсисксипортал:: куеряссоЦиатедпорталграупс**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) , чтобы определить группы порталов, связанные с указанным порталом.</span><span class="sxs-lookup"><span data-stu-id="cd72d-107">Use the [**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) method to determine the portal groups that are associated with a specified portal.</span></span> <span data-ttu-id="cd72d-108">Вызывающие объекты могут получить указатель на определенную группу портала, выбрав нужный объект группы портала из перечисления, возвращаемого методом **куерипорталграупс** или методом **куеряссоЦиатедпорталграупс** .</span><span class="sxs-lookup"><span data-stu-id="cd72d-108">Callers can get a pointer to a specific portal group by selecting the desired portal group object from the enumeration that is returned by the **QueryPortalGroups** method or the **QueryAssociatedPortalGroups** method.</span></span> <span data-ttu-id="cd72d-109">С помощью объекта группы портал можно добавлять или удалять порталы и запросы к свойствам групп порталов, связанным порталам и целевым объектам, содержащим группу порталов.</span><span class="sxs-lookup"><span data-stu-id="cd72d-109">With a portal group object, you can add or remove portals and query for portal group properties, associated portals, and the target that contains the portal group.</span></span>

<span data-ttu-id="cd72d-110">Свойства объекта группы портала включают [идентификатор объекта](vds-data-types.md) и тег группы портала.</span><span class="sxs-lookup"><span data-stu-id="cd72d-110">Portal group object properties include an [object identifier](vds-data-types.md) and the portal group tag.</span></span> <span data-ttu-id="cd72d-111">Дополнительные сведения о тегах группы порталов см. в спецификации iSCSI по адресу <https://go.microsoft.com/fwlink/p/?linkid=158752> .</span><span class="sxs-lookup"><span data-stu-id="cd72d-111">For more information about portal group tags, see the iSCSI specification at <https://go.microsoft.com/fwlink/p/?linkid=158752>.</span></span>

<span data-ttu-id="cd72d-112">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="cd72d-112">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="cd72d-113">Тип</span><span class="sxs-lookup"><span data-stu-id="cd72d-113">Type</span></span>                                                                                      | <span data-ttu-id="cd72d-114">Элемент</span><span class="sxs-lookup"><span data-stu-id="cd72d-114">Element</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd72d-115">Интерфейсы, которые всегда предоставляются этим объектом в поставщиках iSCSI для VDS 1,1 и 2,0</span><span class="sxs-lookup"><span data-stu-id="cd72d-115">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="cd72d-116">[**Ивдсисксипорталграуп**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span><span class="sxs-lookup"><span data-stu-id="cd72d-116">[**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).</span></span>                                                                                              |
| <span data-ttu-id="cd72d-117">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="cd72d-117">Associated enumerations</span></span>                                                                   | <span data-ttu-id="cd72d-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="cd72d-118">None.</span></span>                                                                                                                                              |
| <span data-ttu-id="cd72d-119">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="cd72d-119">Associated structures</span></span>                                                                     | <span data-ttu-id="cd72d-120">Служба [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) [**\_ \_ \_ Уведомление группы**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification)порталграуп iSCSI и портала VDS.</span><span class="sxs-lookup"><span data-stu-id="cd72d-120">[**VDS\_ISCSI\_PORTALGROUP\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) and [**VDS\_PORTAL\_GROUP\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cd72d-121">См. также</span><span class="sxs-lookup"><span data-stu-id="cd72d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd72d-122">Объекты поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="cd72d-122">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="cd72d-123">**Ивдсисксипортал:: КуеряссоЦиатедпорталграупс**</span><span class="sxs-lookup"><span data-stu-id="cd72d-123">**IVdsIscsiPortal::QueryAssociatedPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[<span data-ttu-id="cd72d-124">**Ивдсискситаржет:: Куерипорталграупс**</span><span class="sxs-lookup"><span data-stu-id="cd72d-124">**IVdsIscsiTarget::QueryPortalGroups**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
