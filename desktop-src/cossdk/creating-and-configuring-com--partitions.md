---
description: Администраторы могут использовать COM+ для программного создания и настройки разделов COM+.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Создание и Настройка разделов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538822"
---
# <a name="creating-and-configuring-com-partitions"></a><span data-ttu-id="a2edb-103">Создание и Настройка разделов COM+</span><span class="sxs-lookup"><span data-stu-id="a2edb-103">Creating and Configuring COM+ Partitions</span></span>

<span data-ttu-id="a2edb-104">Администраторы могут использовать COM+ для программного создания и настройки разделов COM+.</span><span class="sxs-lookup"><span data-stu-id="a2edb-104">Administrators can use COM+ to programmatically create and configure COM+ partitions.</span></span> <span data-ttu-id="a2edb-105">На самом деле, все задачи создания и настройки, которые администратор может выполнять из служб компонентов или Active Directory средства администрирования пользователей и компьютеров, можно выполнять с помощью коллекций COM+, объектов и интерфейсов, а также с помощью интерфейса системы Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="a2edb-105">In fact, all creation and configuration tasks that an administrator can do from the Component Services or the Active Directory Users and Computers administrative tools can be done by using COM+ collections, objects, and interfaces or through the Active Directory System Interface (ADSI).</span></span>

<span data-ttu-id="a2edb-106">**Windows XP:** Возможность создания, настройки или делегирования разделов COM+ недоступна.</span><span class="sxs-lookup"><span data-stu-id="a2edb-106">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="a2edb-107">Глобальный раздел является единственным доступным разделом COM+.</span><span class="sxs-lookup"><span data-stu-id="a2edb-107">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="a2edb-108">\* \* Windows 2000: \* \* служба разделов COM+ недоступна в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a2edb-108">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

> [!Note]  
> <span data-ttu-id="a2edb-109">Служба "разделы COM+" не включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2edb-109">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="a2edb-110">Чтобы использовать службу "разделы COM+", необходимо включить ее с помощью средства администрирования служб компонентов или путем изменения свойства Партитионсенаблед в коллекции [**локалкомпутер**](localcomputer.md) на true.</span><span class="sxs-lookup"><span data-stu-id="a2edb-110">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="a2edb-111">Для выполнения задач, связанных с секциями, COM+ предоставляет следующие программные элементы:</span><span class="sxs-lookup"><span data-stu-id="a2edb-111">To accomplish partition-related tasks, COM+ provides the following programming elements:</span></span>

-   <span data-ttu-id="a2edb-112">Методы и свойства интерфейса [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) в классе [**комадминкаталог**](comadmincatalog.md) :</span><span class="sxs-lookup"><span data-stu-id="a2edb-112">Methods and properties of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface on the [**COMAdminCatalog**](comadmincatalog.md) class:</span></span>
    -   <span data-ttu-id="a2edb-113">Свойство [**куррентпартитион**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-113">[**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) property.</span></span>
    -   <span data-ttu-id="a2edb-114">Свойство [**куррентпартитионид**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-114">[**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) property.</span></span>
    -   <span data-ttu-id="a2edb-115">Свойство [**куррентпартитионнаме**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-115">[**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) property.</span></span>
    -   <span data-ttu-id="a2edb-116">Метод [**флушпартитионкаче**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-116">[**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) method.</span></span>
    -   <span data-ttu-id="a2edb-117">Метод [**жетпартитионид**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-117">[**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) method.</span></span>
    -   <span data-ttu-id="a2edb-118">Метод [**жетпартитионнаме**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-118">[**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) method.</span></span>
    -   <span data-ttu-id="a2edb-119">Свойство [**глобалпартитионид**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-119">[**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) property.</span></span>
-   <span data-ttu-id="a2edb-120">Набор объектов COM+ для создания секций и управления ими в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2edb-120">A set of COM+ objects for creating and managing partitions in Active Directory.</span></span>
-   <span data-ttu-id="a2edb-121">Раздел реестра COM+, **партитионкаче**, для изменения размера кэша раздела.</span><span class="sxs-lookup"><span data-stu-id="a2edb-121">A COM+ registry key, **PartitionCache**, for changing the partition cache size.</span></span>
-   <span data-ttu-id="a2edb-122">Набор связанных с секциями [коллекций администрирования com+](com--administration-collections.md):</span><span class="sxs-lookup"><span data-stu-id="a2edb-122">A set of partitions-related [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="a2edb-123">Коллекция [**partitions**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-123">[**Partitions**](partitions.md) collection.</span></span>
    -   <span data-ttu-id="a2edb-124">Коллекция [**партитионусерс**](partitionusers.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-124">[**PartitionUsers**](partitionusers.md) collection.</span></span>
    -   <span data-ttu-id="a2edb-125">Коллекция [**ролесфорпартитион**](rolesforpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-125">[**RolesForPartition**](rolesforpartition.md) collection.</span></span>
    -   <span data-ttu-id="a2edb-126">Коллекция [**усерсинпартитионроле**](usersinpartitionrole.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-126">[**UsersInPartitionRole**](usersinpartitionrole.md) collection.</span></span>
-   <span data-ttu-id="a2edb-127">Свойства других [коллекций администрирования com+](com--administration-collections.md):</span><span class="sxs-lookup"><span data-stu-id="a2edb-127">Properties of other [COM+ Administration Collections](com--administration-collections.md):</span></span>
    -   <span data-ttu-id="a2edb-128">Свойство PartitionID в коллекции [**аппликатионинстанцес**](applicationinstances.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-128">PartitionID property on the [**ApplicationInstances**](applicationinstances.md) collection.</span></span>
    -   <span data-ttu-id="a2edb-129">Свойство Апппартитионид коллекции [**приложений**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-129">AppPartitionID property on the [**Applications**](applications.md) collection.</span></span>
    -   <span data-ttu-id="a2edb-130">Свойства Партитиондескриптион, PartitionID и PartitionName в коллекции [**филесфоримпорт**](filesforimport.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-130">PartitionDescription, PartitionID, and PartitionName properties on the [**FilesForImport**](filesforimport.md) collection.</span></span>
    -   <span data-ttu-id="a2edb-131">Свойства Дспартитионлукупенаблед, Локалпартитионлукупенаблед и Партитионсенаблед коллекции [**локалкомпутер**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-131">DSPartitionLookupEnabled, LocalPartitionLookupEnabled, and PartitionsEnabled properties on the [**LocalComputer**](localcomputer.md) collection.</span></span>
    -   <span data-ttu-id="a2edb-132">Свойства Евенткласспартитионид и Субскриберпартитионид в коллекции [**субскриптионсфоркомпонент**](subscriptionsforcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-132">EventClassPartitionID and SubscriberPartitionID properties on the [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>
    -   <span data-ttu-id="a2edb-133">Свойства Евенткласспартитионид и Субскриберпартитионид в коллекции [**трансиентсубскриптионс**](transientsubscriptions.md) .</span><span class="sxs-lookup"><span data-stu-id="a2edb-133">EventClassPartitionID and SubscriberPartitionID properties on the [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2edb-134">См. также</span><span class="sxs-lookup"><span data-stu-id="a2edb-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2edb-135">Сбор метрик секции</span><span class="sxs-lookup"><span data-stu-id="a2edb-135">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="a2edb-136">Настройка кэша секций</span><span class="sxs-lookup"><span data-stu-id="a2edb-136">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="a2edb-137">Группирование приложений в секции</span><span class="sxs-lookup"><span data-stu-id="a2edb-137">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="a2edb-138">Управление локальными секциями</span><span class="sxs-lookup"><span data-stu-id="a2edb-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="a2edb-139">Управление секциями в Active Directory</span><span class="sxs-lookup"><span data-stu-id="a2edb-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="a2edb-140">Установка прав администратора для секции</span><span class="sxs-lookup"><span data-stu-id="a2edb-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



