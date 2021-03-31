---
description: 'Служба VDS предоставляет два вспомогательных объекта: объект перечисления и асинхронный объект. В этом разделе описываются все эти объекты и приводятся ссылки на примеры работы вызывающих методов.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Вспомогательные объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272765"
---
# <a name="helper-objects"></a><span data-ttu-id="b2c4f-104">Вспомогательные объекты</span><span class="sxs-lookup"><span data-stu-id="b2c4f-104">Helper Objects</span></span>

<span data-ttu-id="b2c4f-105">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b2c4f-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="b2c4f-106">Служба VDS предоставляет два вспомогательных объекта: объект перечисления и асинхронный объект.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-106">VDS provides two helper objects: the enumeration object and the async object.</span></span> <span data-ttu-id="b2c4f-107">В этом разделе описываются все эти объекты и приводятся ссылки на примеры работы вызывающих методов.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-107">This topic describes each of these objects and provides links to examples of how callers work with each.</span></span>

## <a name="enumeration-object"></a><span data-ttu-id="b2c4f-108">Объект перечисления</span><span class="sxs-lookup"><span data-stu-id="b2c4f-108">Enumeration Object</span></span>

<span data-ttu-id="b2c4f-109">Объект перечисления перечисляет набор объектов VDS заданного типа.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-109">An enumeration object enumerates through a set of VDS objects of a given type.</span></span> <span data-ttu-id="b2c4f-110">Объектами могут быть поставщики, подсистемы, контроллеры, LUN, Плекс LUN, диски, пакеты дисков, диски, тома или плекса томов.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-110">Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, disk packs, disks, volumes, or volume plexes.</span></span> <span data-ttu-id="b2c4f-111">Вызывающие объекты могут получить указатель на конкретный объект, выбрав нужный объект из перечисления, возвращаемого соответствующим методом.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-111">Callers can get a pointer to a specific object by selecting the desired object from the enumeration that is returned by the appropriate method.</span></span> <span data-ttu-id="b2c4f-112">Пример кода см. в разделе [Работа с объектами перечисления](working-with-enumeration-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b2c4f-112">For a code example, see [Working with Enumeration Objects](working-with-enumeration-objects.md).</span></span>

<span data-ttu-id="b2c4f-113">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-113">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="b2c4f-114">Тип</span><span class="sxs-lookup"><span data-stu-id="b2c4f-114">Type</span></span>                                              | <span data-ttu-id="b2c4f-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="b2c4f-115">Element</span></span>                                  |
|---------------------------------------------------|------------------------------------------|
| <span data-ttu-id="b2c4f-116">Интерфейсы, которые всегда предоставляются этим объектом</span><span class="sxs-lookup"><span data-stu-id="b2c4f-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="b2c4f-117">**иенумвдсобжект**</span><span class="sxs-lookup"><span data-stu-id="b2c4f-117">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| <span data-ttu-id="b2c4f-118">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="b2c4f-118">Associated enumerations</span></span>                           | <span data-ttu-id="b2c4f-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-119">None.</span></span>                                    |
| <span data-ttu-id="b2c4f-120">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="b2c4f-120">Associated structures</span></span>                             | <span data-ttu-id="b2c4f-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-121">None.</span></span>                                    |



 

## <a name="async-object"></a><span data-ttu-id="b2c4f-122">Асинхронный объект</span><span class="sxs-lookup"><span data-stu-id="b2c4f-122">Async Object</span></span>

<span data-ttu-id="b2c4f-123">Асинхронный объект управляет асинхронными операциями.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-123">An async object manages asynchronous operations.</span></span> <span data-ttu-id="b2c4f-124">Методы, инициирующие асинхронные операции, возвращают указатель на интерфейс [**ивдсасинк**](/windows/desktop/api/Vds/nn-vds-ivdsasync) , который позволяет вызывающему объекту отменить, подождать и запросить состояние асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-124">Methods that initiate asynchronous operations return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface, which allows the caller to cancel, wait for, and query the status of the asynchronous operation.</span></span>

<span data-ttu-id="b2c4f-125">Длительные операции службы VDS обычно реализуются асинхронно.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-125">Long-running VDS operations tend to be implemented asynchronously.</span></span> <span data-ttu-id="b2c4f-126">Основные и динамические программы поставщика программного обеспечения регулярно реализуют асинхронные методы для томов, разделов и дисковых операций.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-126">The basic and dynamic software provider programs implement asynchronous methods consistently for volume, partition, and disk operations.</span></span> <span data-ttu-id="b2c4f-127">Поставщики оборудования дополнительно реализуют асинхронно связанные методы.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-127">Hardware providers optionally implement async-related methods asynchronously.</span></span> <span data-ttu-id="b2c4f-128">Независимо от того, как поставщик реализует метод, операция должна вернуть указатель на интерфейс [**ивдсасинк**](/windows/desktop/api/Vds/nn-vds-ivdsasync) к вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-128">Regardless of how the provider implements the method, the operation must return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface to the caller.</span></span> <span data-ttu-id="b2c4f-129">Пример кода см. в разделе [управление асинхронными операциями](managing-asynchronous-operations.md).</span><span class="sxs-lookup"><span data-stu-id="b2c4f-129">For a code example, see [Managing Asynchronous Operations](managing-asynchronous-operations.md).</span></span>

<span data-ttu-id="b2c4f-130">Асинхронные операции включают:</span><span class="sxs-lookup"><span data-stu-id="b2c4f-130">Asynchronous operations include:</span></span>

-   <span data-ttu-id="b2c4f-131">Создание LUN, тома или раздела.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-131">Creating a LUN, volume, or partition.</span></span>
-   <span data-ttu-id="b2c4f-132">Форматирование тома или раздела.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-132">Formatting a volume or partition.</span></span>
-   <span data-ttu-id="b2c4f-133">Добавление или удаление LUN или плекса тома.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-133">Adding or removing a LUN or volume plex.</span></span>
-   <span data-ttu-id="b2c4f-134">Разбиение плекса тома.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-134">Breaking a volume plex.</span></span>
-   <span data-ttu-id="b2c4f-135">Расширение или сжатие LUN или тома.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-135">Extending or shrinking a LUN or volume.</span></span>
-   <span data-ttu-id="b2c4f-136">Восстановление LUN или тома.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-136">Recovering a LUN or volume.</span></span>
-   <span data-ttu-id="b2c4f-137">Очистка диска.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-137">Cleaning a disk.</span></span>
-   <span data-ttu-id="b2c4f-138">Замена диска.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-138">Replacing a disk.</span></span>

<span data-ttu-id="b2c4f-139">В следующей таблице перечислены связанные интерфейсы, перечисления и структуры.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-139">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="b2c4f-140">Тип</span><span class="sxs-lookup"><span data-stu-id="b2c4f-140">Type</span></span>                                              | <span data-ttu-id="b2c4f-141">Элемент</span><span class="sxs-lookup"><span data-stu-id="b2c4f-141">Element</span></span>                        |
|---------------------------------------------------|--------------------------------|
| <span data-ttu-id="b2c4f-142">Интерфейсы, которые всегда предоставляются этим объектом</span><span class="sxs-lookup"><span data-stu-id="b2c4f-142">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="b2c4f-143">**ивдсасинк**</span><span class="sxs-lookup"><span data-stu-id="b2c4f-143">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| <span data-ttu-id="b2c4f-144">Связанные перечисления</span><span class="sxs-lookup"><span data-stu-id="b2c4f-144">Associated enumerations</span></span>                           | <span data-ttu-id="b2c4f-145">Нет.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-145">None.</span></span>                          |
| <span data-ttu-id="b2c4f-146">Связанные структуры</span><span class="sxs-lookup"><span data-stu-id="b2c4f-146">Associated structures</span></span>                             | <span data-ttu-id="b2c4f-147">Нет.</span><span class="sxs-lookup"><span data-stu-id="b2c4f-147">None.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="b2c4f-148">См. также</span><span class="sxs-lookup"><span data-stu-id="b2c4f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2c4f-149">Объектная модель VDS</span><span class="sxs-lookup"><span data-stu-id="b2c4f-149">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="b2c4f-150">**ивдсасинк**</span><span class="sxs-lookup"><span data-stu-id="b2c4f-150">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[<span data-ttu-id="b2c4f-151">Работа с объектами перечисления</span><span class="sxs-lookup"><span data-stu-id="b2c4f-151">Working with Enumeration Objects</span></span>](working-with-enumeration-objects.md)
</dt> <dt>

[<span data-ttu-id="b2c4f-152">Управление асинхронными операциями</span><span class="sxs-lookup"><span data-stu-id="b2c4f-152">Managing Asynchronous Operations</span></span>](managing-asynchronous-operations.md)
</dt> </dl>

 

 
