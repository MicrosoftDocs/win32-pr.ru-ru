---
description: Объект Controller
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Объект Controller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104568598"
---
# <a name="controller-object"></a><span data-ttu-id="fb5db-103">Объект Controller</span><span class="sxs-lookup"><span data-stu-id="fb5db-103">Controller Object</span></span>

<span data-ttu-id="fb5db-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fb5db-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="fb5db-105">Объект контроллера моделирует контроллер в подсистеме.</span><span class="sxs-lookup"><span data-stu-id="fb5db-105">A controller object models a controller in a subsystem.</span></span> <span data-ttu-id="fb5db-106">Контроллеры содержатся в подсистемах, и каждый контроллер имеет один или несколько портов контроллера, через которые главный компьютер может выполнять запись и чтение из LUN.</span><span class="sxs-lookup"><span data-stu-id="fb5db-106">Controllers are contained by subsystems, and each controller has one or more controller ports through which the host computer can write to and read from LUNs.</span></span> <span data-ttu-id="fb5db-107">Один контроллер может быть одновременно установлен в состояние "активный" для одного LUN и неактивен для других.</span><span class="sxs-lookup"><span data-stu-id="fb5db-107">A single controller can be simultaneously set to active for one LUN and inactive for others.</span></span> <span data-ttu-id="fb5db-108">Контроллер, активный для указанного LUN, несет ответственность за обработку входных данных и их вывод из LUN.</span><span class="sxs-lookup"><span data-stu-id="fb5db-108">A controller that is active for a specified LUN carries the responsibility for handling input to and output from the LUN.</span></span> <span data-ttu-id="fb5db-109">Эта идея показана на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="fb5db-109">The following figure illustrates this idea.</span></span>

![На схеме показан контроллер с активным LUN слева и два активных LUN справа.](images/vdscontroller.png)

<span data-ttu-id="fb5db-111">**VDS 1,0:** Каждому контроллеру подсистемы присваивается значение активно или неактивно по отношению к каждому из LUN, которые являются областями подсистемы.</span><span class="sxs-lookup"><span data-stu-id="fb5db-111">**VDS 1.0:** Each of a subsystem's controllers is set to either active or inactive in relation to each of the LUNs the subsystem surfaces.</span></span>

<span data-ttu-id="fb5db-112">Приложения VDS используют метод [**ивдссубсистем:: куериконтроллерс**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) для определения контроллеров, содержащихся в определенной подсистеме.</span><span class="sxs-lookup"><span data-stu-id="fb5db-112">VDS applications use the [**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) method to determine the controllers that are contained by a specific subsystem.</span></span> <span data-ttu-id="fb5db-113">Вызывающие объекты могут получить указатель на конкретный контроллер, выбрав нужный объект контроллера из перечисления, возвращаемого методом **куериконтроллерс** .</span><span class="sxs-lookup"><span data-stu-id="fb5db-113">Callers can get a pointer to a specific controller by selecting the desired controller object from the enumeration that is returned by the **QueryControllers** method.</span></span> <span data-ttu-id="fb5db-114">С помощью объекта контроллера вызывающий объект может установить состояние контроллера, запросить связанные с ним LUN, запросить его порты контроллера, а также очистить кэш и сделать его недействительным.</span><span class="sxs-lookup"><span data-stu-id="fb5db-114">With a controller object, a caller can set the controller status, query for its associated LUNs, query for its controller ports, and flush and invalidate the cache.</span></span>

<span data-ttu-id="fb5db-115">В дополнение к идентификатору объекта, имени и серийному номеру свойства объекта контроллера включают состояние контроллера и работоспособность, а также количество портов.</span><span class="sxs-lookup"><span data-stu-id="fb5db-115">In addition to an object identifier, a name, and a serial number, controller object properties include the controller status and health, and a count of the ports.</span></span>

<span data-ttu-id="fb5db-116">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="fb5db-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="fb5db-117">Тип</span><span class="sxs-lookup"><span data-stu-id="fb5db-117">Type</span></span>                                                                                              | <span data-ttu-id="fb5db-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="fb5db-118">Element</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb5db-119">Интерфейсы, которые всегда предоставляются этим объектом</span><span class="sxs-lookup"><span data-stu-id="fb5db-119">Interfaces that are always exposed by this object</span></span>                                                 | [<span data-ttu-id="fb5db-120">**ивдсконтроллер**</span><span class="sxs-lookup"><span data-stu-id="fb5db-120">**IVdsController**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| <span data-ttu-id="fb5db-121">Интерфейсы, которые всегда предоставляются этим объектом в службе VDS 1,1 и 2,0 Fibre Channel только поставщики</span><span class="sxs-lookup"><span data-stu-id="fb5db-121">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 Fibre Channel providers only</span></span> | [<span data-ttu-id="fb5db-122">**ивдсконтроллерконтроллерпорт**</span><span class="sxs-lookup"><span data-stu-id="fb5db-122">**IVdsControllerControllerPort**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| <span data-ttu-id="fb5db-123">Интерфейсы, которые могут предоставляться этим объектом</span><span class="sxs-lookup"><span data-stu-id="fb5db-123">Interfaces that may be exposed by this object</span></span>                                                     | [<span data-ttu-id="fb5db-124">**ивдсмаинтенанце**</span><span class="sxs-lookup"><span data-stu-id="fb5db-124">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| <span data-ttu-id="fb5db-125">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="fb5db-125">Associated enumerations</span></span>                                                                           | <span data-ttu-id="fb5db-126">Служба [**VDS \_ \_состояние контроллера**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span><span class="sxs-lookup"><span data-stu-id="fb5db-126">[**VDS\_CONTROLLER\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).</span></span>                                                                      |
| <span data-ttu-id="fb5db-127">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="fb5db-127">Associated structures</span></span>                                                                             | <span data-ttu-id="fb5db-128">Служба [**VDS \_ Уведомления \_ контроллера**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) и [**\_ \_ контроллера VDS**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span><span class="sxs-lookup"><span data-stu-id="fb5db-128">[**VDS\_CONTROLLER\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) and [**VDS\_CONTROLLER\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fb5db-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fb5db-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb5db-130">Объекты поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="fb5db-130">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="fb5db-131">**Ивдссубсистем:: Куериконтроллерс**</span><span class="sxs-lookup"><span data-stu-id="fb5db-131">**IVdsSubSystem::QueryControllers**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
