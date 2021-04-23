---
description: Целевой объект
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Целевой объект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693593"
---
# <a name="target-object"></a><span data-ttu-id="7f69f-103">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="7f69f-103">Target Object</span></span>

<span data-ttu-id="7f69f-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7f69f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="7f69f-105">Целевой объект моделирует цель iSCSI, содержащуюся в подсистеме iSCSI.</span><span class="sxs-lookup"><span data-stu-id="7f69f-105">A target object models an iSCSI target that is contained within an iSCSI subsystem.</span></span>

<span data-ttu-id="7f69f-106">Используйте метод [**ивдссубсистемискси:: куеритаржетс**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) , чтобы определить целевые объекты iSCSI для подсистемы.</span><span class="sxs-lookup"><span data-stu-id="7f69f-106">Use the [**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) method to determine the iSCSI targets of the subsystem.</span></span> <span data-ttu-id="7f69f-107">Вызывающие объекты могут получить указатель на конкретный целевой объект путем выбора требуемого целевого объекта из перечисления, возвращаемого методом **куеритаржетс** .</span><span class="sxs-lookup"><span data-stu-id="7f69f-107">Callers can get a pointer to a specific target by selecting the desired target object from the enumeration that is returned by the **QueryTargets** method.</span></span> <span data-ttu-id="7f69f-108">С целевым объектом можно задать понятное имя целевого объекта и запрос для целевых свойств, связанных LUN и подсистемы, содержащей целевой объект.</span><span class="sxs-lookup"><span data-stu-id="7f69f-108">With a target object, you can set the target's friendly name and query for target properties, associated LUNs, and the subsystem that contains the target.</span></span>

<span data-ttu-id="7f69f-109">Узлы должны входить в систему на целевых объектах для доступа к связанным с ними LUN.</span><span class="sxs-lookup"><span data-stu-id="7f69f-109">Host computers must log on to targets to access their associated LUNs.</span></span> <span data-ttu-id="7f69f-110">Чтобы выполнить вход в целевой объект, на целевом объекте должен быть хотя бы один связанный портал в одной из групп портала.</span><span class="sxs-lookup"><span data-stu-id="7f69f-110">To perform a logon to a target, the target must have at least one associated portal in one of its portal groups.</span></span> <span data-ttu-id="7f69f-111">Входные и выходные данные связанных LUN обрабатываются через этот сеанс входа.</span><span class="sxs-lookup"><span data-stu-id="7f69f-111">Input to and output from associated LUNs is handled through this logon session.</span></span>

<span data-ttu-id="7f69f-112">Свойства целевого объекта включают в себя идентификатор объекта, имя iSCSI, понятное имя и флаг с поддержкой CHAP.</span><span class="sxs-lookup"><span data-stu-id="7f69f-112">Target object properties include an object identifier, an iSCSI name, a friendly name, and a CHAP-enabled flag.</span></span>

<span data-ttu-id="7f69f-113">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="7f69f-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="7f69f-114">Тип</span><span class="sxs-lookup"><span data-stu-id="7f69f-114">Type</span></span>                                                                                      | <span data-ttu-id="7f69f-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="7f69f-115">Element</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f69f-116">Интерфейсы, которые всегда предоставляются этим объектом в поставщиках iSCSI для VDS 1,1 и 2,0</span><span class="sxs-lookup"><span data-stu-id="7f69f-116">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="7f69f-117">[**Ивдсискситаржет**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span><span class="sxs-lookup"><span data-stu-id="7f69f-117">[**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).</span></span>                                                                                 |
| <span data-ttu-id="7f69f-118">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="7f69f-118">Associated enumerations</span></span>                                                                   | <span data-ttu-id="7f69f-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="7f69f-119">None.</span></span>                                                                                                                       |
| <span data-ttu-id="7f69f-120">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="7f69f-120">Associated structures</span></span>                                                                     | <span data-ttu-id="7f69f-121">Служба [**VDS \_ Уведомление \_ целевого \_ объекта iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) и [**\_ целевого \_ объекта VDS**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span><span class="sxs-lookup"><span data-stu-id="7f69f-121">[**VDS\_ISCSI\_TARGET\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) and [**VDS\_TARGET\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_target_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7f69f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7f69f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f69f-123">Объекты поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="7f69f-123">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="7f69f-124">**Ивдссубсистемискси:: Куеритаржетс**</span><span class="sxs-lookup"><span data-stu-id="7f69f-124">**IVdsSubSystemIscsi::QueryTargets**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
