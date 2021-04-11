---
description: Привязка томов и устройств LUN
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Привязка томов и устройств LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104273172"
---
# <a name="volume-and-lun-binding"></a><span data-ttu-id="defea-103">Привязка томов и устройств LUN</span><span class="sxs-lookup"><span data-stu-id="defea-103">Volume and LUN Binding</span></span>

<span data-ttu-id="defea-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="defea-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="defea-105">Привязка — это создание томов или LUN.</span><span class="sxs-lookup"><span data-stu-id="defea-105">Binding is the creation of volumes or LUNs.</span></span> <span data-ttu-id="defea-106">Тома состоят из дисковых областей, а LUN состоят из экстентов диска.</span><span class="sxs-lookup"><span data-stu-id="defea-106">Volumes consist of disk extents and LUNs consist of drive extents.</span></span> <span data-ttu-id="defea-107">Привязка выбирает для набора сопоставлений с физическими ресурсами и происходит в подсистеме, в пакете или в обоих случаях.</span><span class="sxs-lookup"><span data-stu-id="defea-107">Binding selects for a set of mappings to physical resources and occurs within a subsystem, within a pack, or both.</span></span> <span data-ttu-id="defea-108">Все программы поставщика поддерживают частично направленную привязку модели, в которой вызывающий объект указывает только те атрибуты привязки, которые имеют определенный интерес, и позволяет поставщику выбрать остальные.</span><span class="sxs-lookup"><span data-stu-id="defea-108">All provider programs support partially directed binding a model in which the caller specifies only those binding attributes of particular interest, and allows the provider to choose the rest.</span></span> <span data-ttu-id="defea-109">Операции в службе VDS для привязки томов и LUN похожи, но не идентичны.</span><span class="sxs-lookup"><span data-stu-id="defea-109">The operations in VDS for binding volumes and LUNs are similar but not identical.</span></span> <span data-ttu-id="defea-110">Например, поставщики оборудования могут предложить дополнительные варианты привязки.</span><span class="sxs-lookup"><span data-stu-id="defea-110">For example, hardware providers can offer additional binding options.</span></span>

<span data-ttu-id="defea-111">Служба VDS поддерживает следующие пять типов привязок томов и LUN для частично направленных конфигураций.</span><span class="sxs-lookup"><span data-stu-id="defea-111">VDS supports the following five volume and LUN binding types for partially directed configurations.</span></span> <span data-ttu-id="defea-112">(Поставщики оборудования могут и поддерживают множество других привязок.)</span><span class="sxs-lookup"><span data-stu-id="defea-112">(Hardware providers can and do support many other bindings.)</span></span>



| <span data-ttu-id="defea-113">Термин</span><span class="sxs-lookup"><span data-stu-id="defea-113">Term</span></span>                                                                                                                                             | <span data-ttu-id="defea-114">Описание</span><span class="sxs-lookup"><span data-stu-id="defea-114">Description</span></span>                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="defea-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Простого</span><span class="sxs-lookup"><span data-stu-id="defea-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple</span></span><br/>                                                     | <span data-ttu-id="defea-116">Линейное сопоставление с одним и только одним непрерывным экстентом.</span><span class="sxs-lookup"><span data-stu-id="defea-116">Linear mapping with one and only one contiguous extent.</span></span><br/>                             |
| <span data-ttu-id="defea-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Диапазон</span><span class="sxs-lookup"><span data-stu-id="defea-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Spanned</span></span><br/>                                                 | <span data-ttu-id="defea-118">Линейное сопоставление с несколькими несмежными экстентами на нескольких дисках или дисках.</span><span class="sxs-lookup"><span data-stu-id="defea-118">Linear mapping with multiple noncontiguous extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="defea-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Чередующиеся</span><span class="sxs-lookup"><span data-stu-id="defea-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Striped</span></span><br/>                                                 | <span data-ttu-id="defea-120">Сопоставление, которое обеспечивает чередование непрерывных экстентов тома на нескольких дисках или дисках.</span><span class="sxs-lookup"><span data-stu-id="defea-120">Mapping that interleaves contiguous volume extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="defea-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Зеркальной</span><span class="sxs-lookup"><span data-stu-id="defea-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Mirrored</span></span><br/>                                             | <span data-ttu-id="defea-122">Сопоставление, которое поддерживает две или более идентичные копии данных.</span><span class="sxs-lookup"><span data-stu-id="defea-122">Mapping that maintains two or more identical data copies.</span></span><br/>                           |
| <span data-ttu-id="defea-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Чередование с четностью</span><span class="sxs-lookup"><span data-stu-id="defea-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Striped with parity</span></span><br/> | <span data-ttu-id="defea-124">Сопоставление, которое распределяет данные проверки четности на нескольких дисках или дисках.</span><span class="sxs-lookup"><span data-stu-id="defea-124">Mapping that distributes parity check information across multiple disks or drives.</span></span><br/>  |



 

<span data-ttu-id="defea-125">Службы VDS создают зеркальные, чередующиеся и чередующиеся привязки с использованием привязок четности более чем от одного члена.</span><span class="sxs-lookup"><span data-stu-id="defea-125">VDS constructs mirrored, striped, and striped with parity bindings from more than one member.</span></span> <span data-ttu-id="defea-126">Например, двустороннее зеркало имеет два члена.</span><span class="sxs-lookup"><span data-stu-id="defea-126">For example, a two-way mirror has two members.</span></span> <span data-ttu-id="defea-127">Каждый элемент может занимать экстенты на нескольких дисках или дисках.</span><span class="sxs-lookup"><span data-stu-id="defea-127">Each member can occupy extents on more than one disk or drive.</span></span> <span data-ttu-id="defea-128">Служба VDS объединяет экстенты для формирования члена, а затем привязывает том или LUN к членам.</span><span class="sxs-lookup"><span data-stu-id="defea-128">VDS concatenates the extents to form the member and then binds the volume or LUN on the members.</span></span> <span data-ttu-id="defea-129">Поставщик может поддерживать все типы привязок или любое подмножество.</span><span class="sxs-lookup"><span data-stu-id="defea-129">A provider can support all binding types, or any subset.</span></span> <span data-ttu-id="defea-130">В объектной модели VDS каждый член зеркала является независимым объектом, называемым плексом.</span><span class="sxs-lookup"><span data-stu-id="defea-130">In the VDS object model, each member of a mirror is an independent object called a plex.</span></span>

<span data-ttu-id="defea-131">Опять же, тома и типы LUN похожи, но не являются точными.</span><span class="sxs-lookup"><span data-stu-id="defea-131">Again, volume and LUN types are similar, but not exact.</span></span> <span data-ttu-id="defea-132">Описание типов томов см. в разделе [объект тома](volume-object.md). сведения о типах LUN см. в разделе [объект LUN](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="defea-132">For a description of volume types, see the [Volume Object](volume-object.md); for LUN types, see the [LUN Object](lun-object.md).</span></span> <span data-ttu-id="defea-133">Типы привязки не могут быть отказоустойчивыми или отказоустойчивыми.</span><span class="sxs-lookup"><span data-stu-id="defea-133">Binding types are either non-fault tolerant or fault tolerant.</span></span>

### <a name="non-fault-tolerant-binding"></a><span data-ttu-id="defea-134">Неотказоустойчивая привязка</span><span class="sxs-lookup"><span data-stu-id="defea-134">Non-Fault Tolerant Binding</span></span>

<span data-ttu-id="defea-135">Тома без отказоустойчивости и LUN не обеспечивают аварийное восстановление.</span><span class="sxs-lookup"><span data-stu-id="defea-135">Non-fault tolerant volumes and LUNs do not offer disaster recovery.</span></span> <span data-ttu-id="defea-136">Если один из дисков, входящих в состав неотказоустойчивого тома или LUN, завершается сбоем, происходит сбой всего тома или LUN.</span><span class="sxs-lookup"><span data-stu-id="defea-136">If one of the spindles that contributes to a non-fault tolerant volume or LUN fails, the entire volume or LUN fails.</span></span> <span data-ttu-id="defea-137">В Exchange, чтобы получить риск для данных, неотказоустойчивые тома и LUN предлагают производительность ввода-вывода, которая обычно является предпочтительной для отказоустойчивых томов и LUN.</span><span class="sxs-lookup"><span data-stu-id="defea-137">In exchange for the risk to data, non-fault tolerant volumes and LUNs offer input/output performance that is generally superior to that of fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="defea-138">Служба VDS поддерживает следующие три неотказоустойчивых типа: простой, составной и чередующийся.</span><span class="sxs-lookup"><span data-stu-id="defea-138">VDS supports the following three non-fault tolerant types: simple, spanned, and striped.</span></span>

<span data-ttu-id="defea-139">Простота</span><span class="sxs-lookup"><span data-stu-id="defea-139">Simple</span></span>

![Схема, на которой показан простой неотказоустойчивый тип с 2 пакетами и 2 подсистемами.](images/vdssimplelunvol.png)

<span data-ttu-id="defea-141">Развернутый</span><span class="sxs-lookup"><span data-stu-id="defea-141">Spanned</span></span>

![Схема, на которой показан составной неотказоустойчивый тип с 1 пакетом и 1 подсистемой.](images/vdsspanlunvol.png)

<span data-ttu-id="defea-143">Чередующиеся</span><span class="sxs-lookup"><span data-stu-id="defea-143">Striped</span></span>

![Схема, на которой показан чередующийся неотказоустойчивый тип с 1 пакетом и 1 подсистемой.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a><span data-ttu-id="defea-145">Отказоустойчивая привязка</span><span class="sxs-lookup"><span data-stu-id="defea-145">Fault Tolerant Binding</span></span>

<span data-ttu-id="defea-146">Следующие отказоустойчивые тома и LUN обеспечивают аварийное восстановление.</span><span class="sxs-lookup"><span data-stu-id="defea-146">The following fault tolerant volumes and LUNs offer disaster recovery.</span></span> <span data-ttu-id="defea-147">Если один из дисков, влияющих на отказоустойчивый том или LUN, завершается сбоем, данные могут быть восстановлены.</span><span class="sxs-lookup"><span data-stu-id="defea-147">If one of the spindles that contributes to a fault tolerant volume or LUN fails, the data can be recovered.</span></span> <span data-ttu-id="defea-148">В Exchange для обеспечения безопасности данных производительность ввода-вывода отказоустойчивых томов и LUN обычно ограничена неотказоустойчивыми томами и LUN.</span><span class="sxs-lookup"><span data-stu-id="defea-148">In exchange for data security, the input/output performance of fault tolerant volumes and LUNs is generally inferior to that of non-fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="defea-149">Служба VDS поддерживает два типа отказоустойчивости: зеркальный и чередующийся с четностью.</span><span class="sxs-lookup"><span data-stu-id="defea-149">VDS supports two fault tolerant types: mirrored and striped with parity.</span></span>

<span data-ttu-id="defea-150">Зеркальное отражение (трехстороннее зеркало)</span><span class="sxs-lookup"><span data-stu-id="defea-150">Mirrored (three-way mirror)</span></span>

![Схема, на которой показан отказоустойчивый тип зеркального отображения (3-сторонний).](images/vdsmirrorlunvol.png)

<span data-ttu-id="defea-152">Чередование с четностью</span><span class="sxs-lookup"><span data-stu-id="defea-152">Striped with parity</span></span>

![Схема, на которой показан чередующийся тип с нечувствительным к сбоям контролем четности.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a><span data-ttu-id="defea-154">См. также</span><span class="sxs-lookup"><span data-stu-id="defea-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="defea-155">Обзор конфигурации</span><span class="sxs-lookup"><span data-stu-id="defea-155">Configuration Overview</span></span>](configuration.md)
</dt> <dt>

[<span data-ttu-id="defea-156">Объект Volume</span><span class="sxs-lookup"><span data-stu-id="defea-156">Volume Object</span></span>](volume-object.md)
</dt> <dt>

[<span data-ttu-id="defea-157">LUN, объект</span><span class="sxs-lookup"><span data-stu-id="defea-157">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

