---
description: Объекты поставщика оборудования
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Объекты поставщика оборудования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "105693808"
---
# <a name="hardware-provider-objects"></a><span data-ttu-id="d76fa-103">Объекты поставщика оборудования</span><span class="sxs-lookup"><span data-stu-id="d76fa-103">Hardware Provider Objects</span></span>

<span data-ttu-id="d76fa-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d76fa-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="d76fa-105">Объектная модель VDS включает набор объектов для запроса и настройки сущностей поставщика оборудования.</span><span class="sxs-lookup"><span data-stu-id="d76fa-105">The VDS object model includes a set of objects to query and configure hardware provider entities.</span></span> <span data-ttu-id="d76fa-106">(Обратите внимание, что хотя служба VDS включает поставщика программного обеспечения, для использования объектов поставщика оборудования необходимо приобрести поставщик оборудования и соответствующее оборудование отдельно.) Эти объекты поставщика оборудования представляют физические устройства (такие как подсистемы, диски и контроллеры) и виртуальные устройства (например, LUN и Плекс LUN).</span><span class="sxs-lookup"><span data-stu-id="d76fa-106">(Note that while VDS includes a software provider, you must purchase a hardware provider and the associated hardware separately to take advantage of the hardware provider objects.) These hardware provider objects represent physical devices (such as subsystems, drives, and controllers) and virtual devices (such as LUNs and LUN plexes).</span></span>

<span data-ttu-id="d76fa-107">Поставщик оборудования должен создать один COM-объект для каждого физического или виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="d76fa-107">A hardware provider should create one COM object for each physical or virtual device.</span></span>

<span data-ttu-id="d76fa-108">На следующем рисунке показана связь между объектом поставщика и набором объектов поставщика оборудования, а также отношение между различными объектами поставщика оборудования.</span><span class="sxs-lookup"><span data-stu-id="d76fa-108">The illustration that follows shows the relationship between the provider object and the set of hardware provider objects, as well as the relationship between the various hardware provider objects themselves.</span></span>

![<span data-ttu-id="d76fa-109">Схема, показывающая связь между "поставщик" и "подсистема", "контроллер", "LUN", "Плекс", "диск" и "шпиндель".</span><span class="sxs-lookup"><span data-stu-id="d76fa-109">Diagram that shows the relationship between the 'Provider' and 'Subsystem', 'Controller', 'LUN', 'LUN plex', 'Drive', and 'Spindle'.</span></span> ](images/vdshwobjects.png)

<span data-ttu-id="d76fa-110">Объект поставщика может содержать любое количество подсистем.</span><span class="sxs-lookup"><span data-stu-id="d76fa-110">A provider object can contain any number of subsystems.</span></span> <span data-ttu-id="d76fa-111">Все поставщики оборудования способны управлять несколькими экземплярами одной и той же модели подсистемы.</span><span class="sxs-lookup"><span data-stu-id="d76fa-111">All hardware providers are capable of managing multiple instances of the same subsystem model.</span></span> <span data-ttu-id="d76fa-112">Многие поставщики оборудования также могут управлять несколькими экземплярами различных моделей подсистем.</span><span class="sxs-lookup"><span data-stu-id="d76fa-112">Many hardware providers are also capable of managing multiple instances of different subsystem models.</span></span> <span data-ttu-id="d76fa-113">На одном компьютере может размещаться любое количество поставщиков оборудования.</span><span class="sxs-lookup"><span data-stu-id="d76fa-113">A single computer can host any number of hardware providers.</span></span>

<span data-ttu-id="d76fa-114">Объект подсистемы может содержать любое количество контроллеров и дисков, а также может отображать любое количество LUN.</span><span class="sxs-lookup"><span data-stu-id="d76fa-114">A subsystem object can contain any number of controllers and drives, and can surface any number of LUNs.</span></span> <span data-ttu-id="d76fa-115">Объект LUN состоит по крайней мере из одного плекса LUN, и каждый Плекс LUN сопоставляется с одним или несколькими дисками в зависимости от типа плекса.</span><span class="sxs-lookup"><span data-stu-id="d76fa-115">A LUN object comprises of at least one LUN plex, and each LUN plex maps to one or more drives, depending on the plex type.</span></span> <span data-ttu-id="d76fa-116">Объекты контроллера могут управлять вводом-выводом данных для любого числа объектов LUN.</span><span class="sxs-lookup"><span data-stu-id="d76fa-116">Controller objects can manage data input/output for any number of LUN objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d76fa-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d76fa-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d76fa-118">Объектная модель VDS</span><span class="sxs-lookup"><span data-stu-id="d76fa-118">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
