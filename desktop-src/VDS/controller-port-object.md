---
description: Объект порта контроллера
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Объект порта контроллера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692218"
---
# <a name="controller-port-object"></a><span data-ttu-id="35437-103">Объект порта контроллера</span><span class="sxs-lookup"><span data-stu-id="35437-103">Controller Port Object</span></span>

<span data-ttu-id="35437-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="35437-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="35437-105">Объект порта контроллера моделирует порт контроллера в подсистеме.</span><span class="sxs-lookup"><span data-stu-id="35437-105">A controller port object models a controller port in a subsystem.</span></span> <span data-ttu-id="35437-106">Ведущие компьютеры могут записывать и считывать LUN через порты контроллера.</span><span class="sxs-lookup"><span data-stu-id="35437-106">Host computers can write to and read from LUNs through controller ports.</span></span> <span data-ttu-id="35437-107">Порты контроллера содержатся в подсистеме контроллеры.</span><span class="sxs-lookup"><span data-stu-id="35437-107">Controller ports are contained by controllers in a subsystem.</span></span> <span data-ttu-id="35437-108">В службе VDS 1,1 и VDS 2.0 каждому из портов контроллера подсистемы присваивается значение активно или неактивно по отношению к каждому из LUN, которые являются областями подсистемы.</span><span class="sxs-lookup"><span data-stu-id="35437-108">In VDS 1.1 and VDS2.0, each of a subsystem's controller ports is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span> <span data-ttu-id="35437-109">После этого один порт контроллера может быть одновременно задан как активный для одного LUN и неактивен для других.</span><span class="sxs-lookup"><span data-stu-id="35437-109">A single controller port, then, can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="35437-110">Порт контроллера, активный для данного LUN, несет ответственность за обработку входных данных и их вывод из LUN.</span><span class="sxs-lookup"><span data-stu-id="35437-110">A controller port that is active for a given LUN carries responsibility for handling input to and output from the LUN.</span></span>

<span data-ttu-id="35437-111">Активные порты контроллера служат в качестве одной из конечных точек путей MPIO в Fibre Channel поставщиков оборудования, на которых могут быть наложены политики балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="35437-111">Active controller ports serve as one of the endpoints of MPIO paths in Fibre Channel hardware providers, upon which load balancing policies can be imposed.</span></span>

<span data-ttu-id="35437-112">Используйте метод [**ивдсконтроллерконтроллерпорт:: куериконтроллерпортс**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) , чтобы определить порты контроллера, содержащиеся в определенном контроллере.</span><span class="sxs-lookup"><span data-stu-id="35437-112">Use the [**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) method to determine the controller ports that are contained by a specific controller.</span></span> <span data-ttu-id="35437-113">Вызывающие объекты могут получить указатель на конкретный порт контроллера, выбрав нужный объект порта контроллера из перечисления, возвращаемого методом **куериконтроллерпортс** .</span><span class="sxs-lookup"><span data-stu-id="35437-113">Callers can get a pointer to a specific controller port by selecting the desired controller port object from the enumeration that is returned by the **QueryControllerPorts** method.</span></span> <span data-ttu-id="35437-114">С помощью объекта контроллера вызывающий объект может установить состояние порта контроллера и запросить связанные с ним LUN.</span><span class="sxs-lookup"><span data-stu-id="35437-114">With a controller object, a caller can set the controller port status and query for its associated LUNs.</span></span>

<span data-ttu-id="35437-115">Свойства объекта контроллера включают в себя идентификатор объекта, имя, серийный номер и состояние порта контроллера.</span><span class="sxs-lookup"><span data-stu-id="35437-115">Controller object properties include an object identifier, a name, a serial number, and the controller port status.</span></span>

<span data-ttu-id="35437-116">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="35437-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="35437-117">Тип</span><span class="sxs-lookup"><span data-stu-id="35437-117">Type</span></span>                                                                                              | <span data-ttu-id="35437-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="35437-118">Element</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35437-119">Интерфейсы, которые всегда предоставляются этим объектом в службе VDS 1,1 и 2,0 Fibre Channel только поставщики</span><span class="sxs-lookup"><span data-stu-id="35437-119">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="35437-120">**ивдсконтроллерпорт**</span><span class="sxs-lookup"><span data-stu-id="35437-120">**IVdsControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| <span data-ttu-id="35437-121">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="35437-121">Associated enumerations</span></span>                                                                           | [<span data-ttu-id="35437-122">**\_состояние порта \_ VDS**</span><span class="sxs-lookup"><span data-stu-id="35437-122">**VDS\_PORT\_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| <span data-ttu-id="35437-123">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="35437-123">Associated structures</span></span>                                                                             | <span data-ttu-id="35437-124">Служба [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) [ **\_ \_ Уведомление о портах** Prop и VDS](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span><span class="sxs-lookup"><span data-stu-id="35437-124">[**VDS\_PORT\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) and [**VDS\_PORT\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="35437-125">См. также</span><span class="sxs-lookup"><span data-stu-id="35437-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35437-126">Объекты поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="35437-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="35437-127">**Ивдсконтроллерконтроллерпорт:: Куериконтроллерпортс**</span><span class="sxs-lookup"><span data-stu-id="35437-127">**IVdsControllerControllerPort::QueryControllerPorts**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
