---
description: Эти классы WMI объявляются в CimWin32. mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Поставщик WMI CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538483"
---
# <a name="cim-wmi-provider"></a><span data-ttu-id="ec3c4-103">Поставщик WMI CIM</span><span class="sxs-lookup"><span data-stu-id="ec3c4-103">CIM WMI Provider</span></span>

<span data-ttu-id="ec3c4-104">Эти классы WMI объявляются в CimWin32. mof.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-104">These WMI classes are declared in CimWin32.mof.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ec3c4-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="ec3c4-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ec3c4-106">**\_Действие CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-106">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dd>

<span data-ttu-id="ec3c4-107">Класс [**\_ действия CIM**](cim-action.md) — это операция, которая является частью процесса для создания программного элемента в следующем состоянии или для исключения программного элемента в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-107">A [**CIM\_Action**](cim-action.md) class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-108">**\_АКТИОНСЕКУЕНЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-108">**CIM\_ActionSequence**</span></span>](cim-actionsequence.md)
</dt> <dd>

<span data-ttu-id="ec3c4-109">Ассоциация [**\_ актионсекуенце CIM**](cim-actionsequence.md) определяет ряд операций, которые переходят программный элемент (на который ссылается Ассоциация [**\_ софтварилементактионс CIM**](cim-softwareelementactions.md) ) в следующее состояние или удаляет программный элемент из текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-109">The [**CIM\_ActionSequence**](cim-actionsequence.md) association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-110">**\_АКТСАССПАРЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-110">**CIM\_ActsAsSpare**</span></span>](cim-actsasspare.md)
</dt> <dd>

<span data-ttu-id="ec3c4-111">Ассоциация [**\_ актсасспаре CIM**](cim-actsasspare.md) указывает, какие элементы могут быть запасными или заменить другие агрегированные элементы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-111">The [**CIM\_ActsAsSpare**](cim-actsasspare.md) association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="ec3c4-112">Запасной элемент может действовать в режиме "горячего резервирования", как указано в отдельном элементе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-112">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-113">**\_АДЖАЦЕНТСЛОТС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-113">**CIM\_AdjacentSlots**</span></span>](cim-adjacentslots.md)
</dt> <dd>

<span data-ttu-id="ec3c4-114">Ассоциация [**\_ аджацентслотс CIM**](cim-adjacentslots.md) описывает расположение слотов на плате размещения или адаптере карты.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-114">The [**CIM\_AdjacentSlots**](cim-adjacentslots.md) association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="ec3c4-115">Такие сведения, как расстояние между слотами и то, являются ли они общими (если один из них заполнен, другие слоты не могут использоваться), передаются как свойства связи.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-115">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-116">**\_АГГРЕГАТЕПЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-116">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-117">Класс [**CIM \_ аггрегатепекстент**](cim-aggregatepextent.md) предоставляет сводные сведения об адресных логических блоках, которые находятся в одной группе избыточности хранилища и расположены на одном физическом носителе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-117">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-118">**\_АГГРЕГАТЕПСЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-118">**CIM\_AggregatePSExtent**</span></span>](cim-aggregatepsextent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-119">Класс [**CIM \_ аггрегатепсекстент**](cim-aggregatepsextent.md) определяет количество адресацических логических блоков на одном запоминающем устройстве, исключая логические блоки, сопоставленные как проверочные данные.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-119">The [**CIM\_AggregatePSExtent**](cim-aggregatepsextent.md) class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="ec3c4-120">Если определены наборы томов, логические блоки содержатся в одном наборе томов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-120">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="ec3c4-121">Это альтернативный вариант группировки для [**CIM \_ протектедспацеекстент**](cim-protectedspaceextent.md), когда требуются только сводные данные или используется автоматическая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-121">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-122">**\_АГГРЕГАТЕРЕДУНДАНЦИКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-122">**CIM\_AggregateRedundancyComponent**</span></span>](cim-aggregateredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-123">Класс [**CIM \_ аггрегатередунданцикомпонент**](cim-aggregateredundancycomponent.md) описывает совокупную физическую область в группе избыточности хранилища.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-123">The [**CIM\_AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) class describes the aggregate physical extent in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-124">**\_АЛАРМДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-124">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-125">Класс [**CIM \_ алармдевице**](cim-alarmdevice.md) — это сигнальное устройство, которое отправляет звуковые или видимые события, связанные с проблемной ситуацией.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-125">The [**CIM\_AlarmDevice**](cim-alarmdevice.md) class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-126">**\_АЛЛОКАТЕДРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-126">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dd>

<span data-ttu-id="ec3c4-127">Класс [**CIM \_ аллокатедресаурце**](cim-allocatedresource.md) представляет связь между логическими устройствами и системными ресурсами и указывает, что ресурс назначен устройству.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-127">The [**CIM\_AllocatedResource**](cim-allocatedresource.md) class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-128">**\_АППЛИКАТИОНСИСТЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-128">**CIM\_ApplicationSystem**</span></span>](cim-applicationsystem.md)
</dt> <dd>

<span data-ttu-id="ec3c4-129">Класс [**CIM \_ аппликатионсистем**](cim-applicationsystem.md) представляет приложение или программную систему, поддерживающую определенную бизнес-функцию, которая может управляться как независимая единица.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-129">The [**CIM\_ApplicationSystem**](cim-applicationsystem.md) class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="ec3c4-130">Такая система может быть разложена на функциональные компоненты с помощью класса [**CIM \_ софтварефеатуре**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-130">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="ec3c4-131">Функции программного обеспечения для конкретного приложения или программной системы находятся с помощью ассоциации [**CIM \_ аппликатионсистемсофтварефеатуре**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-131">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-132">**\_АППЛИКАТИОНСИСТЕМСОФТВАРЕФЕАТУРЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-132">**CIM\_ApplicationSystemSoftwareFeature**</span></span>](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="ec3c4-133">Класс [**CIM \_ аппликатионсистемсофтварефеатуре**](cim-applicationsystemsoftwarefeature.md) представляет ассоциацию, которая определяет программные компоненты, составляющие конкретную систему приложений.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-133">The [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="ec3c4-134">Функции программного обеспечения могут включаться в различные продукты.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-134">The software features can be included in different products.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-135">**\_АССОЦИАТЕДАЛАРМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-135">**CIM\_AssociatedAlarm**</span></span>](cim-associatedalarm.md)
</dt> <dd>

<span data-ttu-id="ec3c4-136">Зависимость [**\_ ассоЦиатедаларм CIM**](cim-associatedalarm.md) связывает сигнал с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-136">The [**CIM\_AssociatedAlarm**](cim-associatedalarm.md) dependency associates an alarm with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-137">**\_АССОЦИАТЕДБАТТЕРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-137">**CIM\_AssociatedBattery**</span></span>](cim-associatedbattery.md)
</dt> <dd>

<span data-ttu-id="ec3c4-138">Зависимость [**\_ ассоЦиатедбаттери CIM**](cim-associatedbattery.md) связывает батарею с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-138">The [**CIM\_AssociatedBattery**](cim-associatedbattery.md) dependency associates a battery with a logical device.</span></span> <span data-ttu-id="ec3c4-139">Используйте эту связь для моделирования отдельных аккумуляторов, составляющих источник бесперебойного питания (ИБП).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-139">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-140">**\_АССОЦИАТЕДКУЛИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-140">**CIM\_AssociatedCooling**</span></span>](cim-associatedcooling.md)
</dt> <dd>

<span data-ttu-id="ec3c4-141">Ассоциация [**CIM \_ ассоЦиатедкулинг**](cim-associatedcooling.md) указывает, что вентиляторы или другие устройства охлаждения относятся к устройству (в отличие от блока охлаждения корпуса или шкафа).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-141">The [**CIM\_AssociatedCooling**](cim-associatedcooling.md) association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-142">**\_АССОЦИАТЕДМЕМОРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-142">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> <dd>

<span data-ttu-id="ec3c4-143">Класс [**CIM \_ ассоЦиатемемори**](cim-associatedmemory.md) связывает установленную или связанную память, например кэш-память с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-143">The [**CIM\_AssociateMemory**](cim-associatedmemory.md) class associates installed or associated memory, such as cache memory with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-144">**\_АССОЦИАТЕДПРОЦЕССОРМЕМОРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-144">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dd>

<span data-ttu-id="ec3c4-145">Класс [**CIM \_ ассоЦиатедпроцессормемори**](cim-associatedprocessormemory.md) связывает процессор и системную память или кэш процессора.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-145">The [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md) class associates the processor and system memory, or a processor's cache.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-146">**\_АССОЦИАТЕДСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-146">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-147">Класс [**CIM \_ ассоЦиатедсенсор**](cim-associatedsensor.md) связывает установленный датчик с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-147">The [**CIM\_AssociatedSensor**](cim-associatedsensor.md) class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="ec3c4-148">Датчик измеряет критические свойства ввода и вывода и может быть добавлен вместе с устройством или установлен поблизости.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-148">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-149">**\_АССОЦИАТЕДСУППЛИКУРРЕНТСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-149">**CIM\_AssociatedSupplyCurrentSensor**</span></span>](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-150">Класс [**CIM \_ ассоЦиатедсуппликуррентсенсор**](cim-associatedsupplycurrentsensor.md) связывает источник питания с датчиком тока (ампераже), который отслеживает частоту входных данных.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-150">The [**CIM\_AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-151">**\_АССОЦИАТЕДСУППЛИВОЛТАЖЕСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-151">**CIM\_AssociatedSupplyVoltageSensor**</span></span>](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-152">Связывает источник питания с датчиком напряжения, отслеживающим свое входное напряжение.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-152">Associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-153">**\_BASEDON CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-153">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> <dd>

<span data-ttu-id="ec3c4-154">Класс [**CIM \_ BasedOn**](cim-basedon.md) представляет ассоциацию, которая описывает, как можно собирать экстенты хранилища из экстентов более низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-154">The [**CIM\_BasedOn**](cim-basedon.md) class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="ec3c4-155">Например, физические экстенты включают экстенты защищенного пространства.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-155">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="ec3c4-156">Таким же набор томов собирается из одного или нескольких физических или защищенных экстентов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-156">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="ec3c4-157">Память кэша может быть определена независимо и реализована в физическом элементе или на основе энергозависимых или временных экстентов хранения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-157">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-158">**\_Аккумулятор CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-158">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dd>

<span data-ttu-id="ec3c4-159">Класс [**\_ батареи CIM**](cim-battery.md) представляет возможности и управление логическим устройством с батареей.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-159">The [**CIM\_Battery**](cim-battery.md) class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="ec3c4-160">Этот класс применяется к батареям в ноутбуках и других внутренних и внешних батареях.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-160">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-161">**\_БИНАРИСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-161">**CIM\_BinarySensor**</span></span>](cim-binarysensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-162">Класс [**CIM \_ Бинарисенсор**](cim-binarysensor.md) предоставляет логический вывод.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-162">The [**CIM\_BinarySensor**](cim-binarysensor.md) class provides a Boolean output.</span></span> <span data-ttu-id="ec3c4-163">Свойства **CurrentState** и **поссиблестатес** были добавлены для датчиков, поэтому создание подкласса **CIM \_ бинарисенсор** больше не требуется, хотя он сохраняется для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-163">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="ec3c4-164">Двоичный датчик можно создать, создав датчик с двумя возможными состояниями.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-164">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-165">**\_БИОСЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-165">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dd>

<span data-ttu-id="ec3c4-166">Класс [**CIM \_ биоселемент**](cim-bioselement.md) представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для запуска и настройки компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-166">The [**CIM\_BIOSElement**](cim-bioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-167">**\_БИОСФЕАТУРЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-167">**CIM\_BIOSFeature**</span></span>](cim-biosfeature.md)
</dt> <dd>

<span data-ttu-id="ec3c4-168">представляет возможности низкоуровневого программного обеспечения, используемого для запуска и настройки компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-168">represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-169">**\_БИОСФЕАТУРЕБИОСЕЛЕМЕНТС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-169">**CIM\_BIOSFeatureBIOSElements**</span></span>](cim-biosfeaturebioselements.md)
</dt> <dd>

<span data-ttu-id="ec3c4-170">Класс [**CIM \_ биосфеатуребиоселементс**](cim-biosfeaturebioselements.md) связывает компонент BIOS и его агрегированные элементы BIOS.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-170">The [**CIM\_BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) class associates a BIOS feature and its aggregated BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-171">**\_БИОСЛОАДЕДИННВ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-171">**CIM\_BIOSLoadedInNV**</span></span>](cim-biosloadedinnv.md)
</dt> <dd>

<span data-ttu-id="ec3c4-172">Класс [**CIM \_ биослоадединнв**](cim-biosloadedinnv.md) связывает элемент BIOS и долговременное хранилище, в котором он загружается.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-172">The [**CIM\_BIOSLoadedInNV**](cim-biosloadedinnv.md) class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-173">**\_БУТОСФРОМФС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-173">**CIM\_BootOSFromFS**</span></span>](cim-bootosfromfs.md)
</dt> <dd>

<span data-ttu-id="ec3c4-174">Класс [**CIM \_ бутосфромфс**](cim-bootosfromfs.md) связывает операционную систему и файловые системы, из которых загружается операционная система.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-174">The [**CIM\_BootOSFromFS**](cim-bootosfromfs.md) class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="ec3c4-175">Ассоциация — «многие ко многим»; Распределенная операционная система может зависеть от нескольких файловых систем для правильной и полной загрузки.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-175">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-176">**\_БУТСАП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-176">**CIM\_BootSAP**</span></span>](cim-bootsap.md)
</dt> <dd>

<span data-ttu-id="ec3c4-177">Класс [**CIM \_ бутсап**](cim-bootsap.md) представляет точки доступа службы загрузки.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-177">The [**CIM\_BootSAP**](cim-bootsap.md) class represents the access points of a boot service.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-178">**\_БУТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-178">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-179">Класс [**CIM \_ бутсервице**](cim-bootservice.md) представляет функциональные возможности, предоставляемые устройством или программным обеспечением или сетью, для загрузки операционной системы в единой компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-179">The [**CIM\_BootService**](cim-bootservice.md) class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-180">**\_БУТСЕРВИЦЕАКЦЕССБИСАП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-180">**CIM\_BootServiceAccessBySAP**</span></span>](cim-bootserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="ec3c4-181">Класс [**CIM \_ бутсервицеакцессбисап**](cim-bootserviceaccessbysap.md) связывает службу загрузки и ее точки доступа.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-181">The [**CIM\_BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) class associates a boot service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-182">**\_КАЧЕМЕМОРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-182">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dd>

<span data-ttu-id="ec3c4-183">Класс [**CIM \_ качемемори**](cim-cachememory.md) определяет возможности и управление кэшовой памятью.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-183">The [**CIM\_CacheMemory**](cim-cachememory.md) class defines the capabilities and management of cache memory.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-184">**\_Карта CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-184">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dd>

<span data-ttu-id="ec3c4-185">Класс [**\_ карты CIM**](cim-card.md) представляет тип физического контейнера, который может быть подключен к другой плате или плате размещения или сам по себе является платой или материнской картой в корпусе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-185">The [**CIM\_Card**](cim-card.md) class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="ec3c4-186">Этот класс включает любой пакет, который способен поддерживать сигналы и предоставляет точку подключения для физических компонентов, таких как микросхемы или другие физические пакеты, такие как другие карты.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-186">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-187">**\_КАРДИНСЛОТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-187">**CIM\_CardInSlot**</span></span>](cim-cardinslot.md)
</dt> <dd>

<span data-ttu-id="ec3c4-188">Класс [**CIM \_ кардинслот**](cim-cardinslot.md) связывает адаптер адаптера с контейнером, в который он вставлен.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-188">The [**CIM\_CardInSlot**](cim-cardinslot.md) class associates an adapter card with the container into which it is inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-189">**\_КАРДОНКАРД CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-189">**CIM\_CardOnCard**</span></span>](cim-cardoncard.md)
</dt> <dd>

<span data-ttu-id="ec3c4-190">Ассоциация [**CIM \_ кардонкард**](cim-cardoncard.md) описывает связи с картами, которые могут быть подключены к материнским платам, платам адаптера или картам, поддерживающим специальные модули, подобные картам.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-190">The [**CIM\_CardOnCard**](cim-cardoncard.md) association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-191">**\_КДРОМДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-191">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dd>

<span data-ttu-id="ec3c4-192">Класс [**CIM \_ кдромдриве**](cim-cdromdrive.md) представляет устройство чтения компакт-дисков на компьютере.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-192">The [**CIM\_CDROMDrive**](cim-cdromdrive.md) class represents a CD-ROM drive on the computer.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-193">**\_Корпус CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-193">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dd>

<span data-ttu-id="ec3c4-194">Класс [**\_ шасси CIM**](cim-chassis.md) представляет физические элементы, охватывающие другие элементы, и предоставляет определяемые функциональные возможности, такие как рабочий стол, обрабатывающий узел, ИБП, диск или ленточное хранилище или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-194">The [**CIM\_Chassis**](cim-chassis.md) class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-195">**\_ЧАССИСИНРАКК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-195">**CIM\_ChassisInRack**</span></span>](cim-chassisinrack.md)
</dt> <dd>

<span data-ttu-id="ec3c4-196">Ассоциация [**CIM \_ чассисинракк**](cim-chassisinrack.md) представляет собой отношение "содержит" между стойкой и содержащимся в ней шасси.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-196">The [**CIM\_ChassisInRack**](cim-chassisinrack.md) association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-197">**\_Проверка CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-197">**CIM\_Check**</span></span>](cim-check.md)
</dt> <dd>

<span data-ttu-id="ec3c4-198">Класс [**\_ проверки CIM**](cim-check.md) представляет условие или характеристику, которые должны быть истинными в среде, определенной или определяемой экземпляром класса системы [**\_ CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-198">The [**CIM\_Check**](cim-check.md) class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="ec3c4-199">Проверки, связанные с определенным программным элементом, организованы в одну из двух групп с помощью свойства **Phase** ассоциации [**CIM \_ софтварилементчеккс**](cim-softwareelementchecks.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-199">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-200">**Микросхема CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-200">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> <dd>

<span data-ttu-id="ec3c4-201">Класс [**\_ микросхем CIM**](cim-chip.md) представляет тип оборудования интегрированной цепи, включая ASIC, процессоры, микросхемы памяти и т. д.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-201">The [**CIM\_Chip**](cim-chip.md) class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-202">**\_КЛУСТЕРИНГСАП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-202">**CIM\_ClusteringSAP**</span></span>](cim-clusteringsap.md)
</dt> <dd>

<span data-ttu-id="ec3c4-203">Класс [**CIM \_ клустерингсап**](cim-clusteringsap.md) представляет точки доступа службы кластеров.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-203">The [**CIM\_ClusteringSAP**](cim-clusteringsap.md) class represents the access points of a clustering service.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-204">**\_КЛУСТЕРИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-204">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-205">Класс [**CIM \_ клустерингсервице**](cim-clusteringservice.md) представляет функциональные возможности, предоставляемые кластером.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-205">The [**CIM\_ClusteringService**](cim-clusteringservice.md) class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="ec3c4-206">Например, возможность отработки отказа может быть смоделирована как служба отказоустойчивого кластера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-206">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-207">**\_КЛУСТЕРСЕРВИЦЕАКЦЕССБИСАП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-207">**CIM\_ClusterServiceAccessBySAP**</span></span>](cim-clusterserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="ec3c4-208">Класс [**CIM \_ клустерсервицеакцессбисап**](cim-clusterserviceaccessbysap.md) представляет связь между службой кластеризации и ее точками доступа.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-208">The [**CIM\_ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) class represents the relationship between a clustering service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-209">**\_КОЛЛЕКТЕДКОЛЛЕКТИОНС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-209">**CIM\_CollectedCollections**</span></span>](cim-collectedcollections.md)
</dt> <dd>

<span data-ttu-id="ec3c4-210">Класс [**CIM \_ коллектедколлектионс**](cim-collectedcollections.md) является ассоциацией статистической обработки, представляющей коллекцию управляемых СИСТЕМНЫХ элементов (MSE), содержащихся в коллекции мсес.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-210">The [**CIM\_CollectedCollections**](cim-collectedcollections.md) class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-211">**\_КОЛЛЕКТЕДМСЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-211">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> <dd>

<span data-ttu-id="ec3c4-212">Класс сопоставления [**CIM \_ коллектедмсес**](cim-collectedmses.md) представляет члены объекта GROUPING, класса [**коллектионофмсес**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-212">The [**CIM\_CollectedMSEs**](cim-collectedmses.md) association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-213">**\_КОЛЛЕКТИОНОФМСЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-213">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> <dd>

<span data-ttu-id="ec3c4-214">Объект [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) позволяет группировать объекты [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) с целью связывания параметров и конфигураций.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-214">The [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="ec3c4-215">Он является абстрактным, чтобы требовать дальнейшего определения и семантического уточнения в подклассах.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-215">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-216">**\_КОЛЛЕКТИОНОФСЕНСОРС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-216">**CIM\_CollectionOfSensors**</span></span>](cim-collectionofsensors.md)
</dt> <dd>

<span data-ttu-id="ec3c4-217">Ассоциация [**CIM \_ коллектионофсенсорс**](cim-collectionofsensors.md) представляет двоичные датчики, составляющие датчик с многорежимным состоянием.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-217">The [**CIM\_CollectionOfSensors**](cim-collectionofsensors.md) association represents the binary sensors that make up the multistate sensor.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-218">**\_КОЛЛЕКТИОНСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-218">**CIM\_CollectionSetting**</span></span>](cim-collectionsetting.md)
</dt> <dd>

<span data-ttu-id="ec3c4-219">Класс [**CIM \_ коллектионсеттинг**](cim-collectionsetting.md) представляет ассоциацию между CIM- [**\_ коллектионофмсес**](cim-collectionofmses.md) и классом параметра, определенным для них.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-219">The [**CIM\_CollectionSetting**](cim-collectionsetting.md) class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-220">**\_КОМПАТИБЛЕПРОДУКТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-220">**CIM\_CompatibleProduct**</span></span>](cim-compatibleproduct.md)
</dt> <dd>

<span data-ttu-id="ec3c4-221">Класс [**CIM \_ компатиблепродукт**](cim-compatibleproduct.md) представляет ассоциацию между продуктами, которая указывает, взаимодействуют ли два упоминаемых продукта, например, могут ли они быть установлены вместе, а также может ли один из них быть физическим контейнером для другого и т. д.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-221">The [**CIM\_CompatibleProduct**](cim-compatibleproduct.md) class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-222">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-222">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dd>

<span data-ttu-id="ec3c4-223">Ассоциация [**\_ компонента CIM**](cim-component.md) представляет части связи между мсес.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-223">The [**CIM\_Component**](cim-component.md) association represents the parts of a relationship between MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-224">**CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-224">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dd>

<span data-ttu-id="ec3c4-225">Класс [**\_ ComputerSystem CIM**](cim-computersystem.md) представляет специальную коллекцию экземпляров [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-225">A [**CIM\_ComputerSystem**](cim-computersystem.md) class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="ec3c4-226">Эта коллекция предоставляет возможности компьютера и служит в качестве точки статистической обработки для связывания одного или нескольких следующих элементов: файловой системы, операционной системы, процессора и памяти (Энергозависимое и энергонезависимое хранилище).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-226">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="ec3c4-227">Этот класс является производным [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-227">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-228">**\_КОМПУТЕРСИСТЕМДМА CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-228">**CIM\_ComputerSystemDMA**</span></span>](cim-computersystemdma.md)
</dt> <dd>

<span data-ttu-id="ec3c4-229">Класс [**CIM \_ компутерсистемдма**](cim-computersystemdma.md) представляет связь между компьютерной системой и доступными каналами прямого доступа к памяти (DMA).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-229">The [**CIM\_ComputerSystemDMA**](cim-computersystemdma.md) class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-230">**\_КОМПУТЕРСИСТЕМИРК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-230">**CIM\_ComputerSystemIRQ**</span></span>](cim-computersystemirq.md)
</dt> <dd>

<span data-ttu-id="ec3c4-231">Класс [**CIM \_ компутерсистемирк**](cim-computersystemirq.md) представляет связь между компьютерной системой и ее доступными линиями запросов на прерывание (IRQ).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-231">The [**CIM\_ComputerSystemIRQ**](cim-computersystemirq.md) class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-232">**\_КОМПУТЕРСИСТЕММАППЕДИО CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-232">**CIM\_ComputerSystemMappedIO**</span></span>](cim-computersystemmappedio.md)
</dt> <dd>

<span data-ttu-id="ec3c4-233">Класс [**CIM \_ компутерсистеммаппедио**](cim-computersystemmappedio.md) представляет ассоциацию между компьютером и его доступными портами ввода-вывода, размещенными в памяти.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-233">The [**CIM\_ComputerSystemMappedIO**](cim-computersystemmappedio.md) class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-234">**\_КОМПУТЕРСИСТЕМПАККАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-234">**CIM\_ComputerSystemPackage**</span></span>](cim-computersystempackage.md)
</dt> <dd>

<span data-ttu-id="ec3c4-235">Класс [**CIM \_ компутерсистемпаккаже**](cim-computersystempackage.md) представляет ассоциацию, которая явно определяет связь между едиными системами компьютеров и одним или несколькими физическими пакетами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-235">The [**CIM\_ComputerSystemPackage**](cim-computersystempackage.md) class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="ec3c4-236">Ассоциация аналогична тому, как логические устройства реализуются физическими элементами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-236">The association is similar to the way that logical devices are realized by physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-237">**\_КОМПУТЕРСИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-237">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dd>

<span data-ttu-id="ec3c4-238">Класс [**CIM \_ компутерсистемресаурце**](cim-computersystemresource.md) представляет связь между компьютерной системой и ее доступными системными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-238">The [**CIM\_ComputerSystemResource**](cim-computersystemresource.md) class represents an association between a computer system and its available system resources.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-239">**\_Конфигурация CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-239">**CIM\_Configuration**</span></span>](cim-configuration.md)
</dt> <dd>

<span data-ttu-id="ec3c4-240">Объект [**\_ конфигурации CIM**](cim-configuration.md) позволяет группировать наборы параметров (определенные в объектах [**\_ параметров CIM**](cim-setting.md) ) и зависимости для одного или нескольких управляемых системных элементов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-240">The [**CIM\_Configuration**](cim-configuration.md) object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-241">**\_КОННЕКТЕДТО CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-241">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> <dd>

<span data-ttu-id="ec3c4-242">Класс [**CIM \_ коннектедто**](cim-connectedto.md) представляет ассоциацию, которая указывает, что подключены два или более физических соединителя.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-242">The [**CIM\_ConnectedTo**](cim-connectedto.md) class represents an association that indicates that two or more physical connectors are connected.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-243">**\_КОННЕКТОРОНПАККАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-243">**CIM\_ConnectorOnPackage**</span></span>](cim-connectoronpackage.md)
</dt> <dd>

<span data-ttu-id="ec3c4-244">Класс [**CIM \_ коннекторонпаккаже**](cim-connectoronpackage.md) представляет ассоциацию, которая делает явной отношение вложения между соединителями и пакетами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-244">The [**CIM\_ConnectorOnPackage**](cim-connectoronpackage.md) class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="ec3c4-245">Физические пакеты содержат соединители и другие физические элементы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-245">Physical packages contain connectors as well as other physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-246">**\_Контейнер CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-246">**CIM\_Container**</span></span>](cim-container.md)
</dt> <dd>

<span data-ttu-id="ec3c4-247">Класс [**\_ контейнера CIM**](cim-container.md) представляет связь между содержащимся и содержащимся физическим элементом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-247">The [**CIM\_Container**](cim-container.md) class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="ec3c4-248">Содержащий объект должен быть физическим пакетом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-248">A containing object must be a physical package.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-249">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-249">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dd>

<span data-ttu-id="ec3c4-250">Отношение [**CIM \_ контролледби**](cim-controlledby.md) указывает, какие устройства отправляются логическим устройством контроллера или к которым осуществляется доступ через.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-250">The [**CIM\_ControlledBy**](cim-controlledby.md) relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-251">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-251">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-252">Класс [**\_ контроллера CIM**](cim-controller.md) является родительским классом для группирования различных устройств, связанных с управлением.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-252">The [**CIM\_Controller**](cim-controller.md) class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="ec3c4-253">Примерами контроллеров являются контроллеры SCSI, USB-контроллеры и последовательные контроллеры.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-253">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-254">**\_КУЛИНГДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-254">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-255">Класс [**CIM \_ кулингдевице**](cim-coolingdevice.md) представляет возможности и управление охлаждающими устройствами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-255">The [**CIM\_CoolingDevice**](cim-coolingdevice.md) class represents the capabilities and management of cooling devices.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-256">**\_КОПИФИЛЕАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-256">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-257">Класс [**CIM \_ копифилеактион**](cim-copyfileaction.md) представляет перемещение или копирование файлов из компьютерной системы в новое место.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-257">The [**CIM\_CopyFileAction**](cim-copyfileaction.md) class represents moving or copying files from a computer system to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-258">**\_КРЕАТЕДИРЕКТОРЯКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-258">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-259">Класс [**CIM \_ креатедиректоряктион**](cim-createdirectoryaction.md) создает пустые каталоги для программных элементов, которые должны быть установлены локально.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-259">The [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class creates empty directories for software elements to be installed locally.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-260">**\_КУРРЕНТСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-260">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-261">Класс [**CIM \_ куррентсенсор**](cim-currentsensor.md) существует для обеспечения обратной совместимости с более ранними определениями схемы CIM.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-261">The [**CIM\_CurrentSensor**](cim-currentsensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-262">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-262">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dd>

<span data-ttu-id="ec3c4-263">Класс [**\_ файлов данных CIM**](cim-datafile.md) представляет именованную коллекцию или исполняемый код.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-263">The [**CIM\_DataFile**](cim-datafile.md) class represents a named collection of data or executable code.</span></span> <span data-ttu-id="ec3c4-264">Будут возвращены только экземпляры файлов на локальных жестких дисках</span><span class="sxs-lookup"><span data-stu-id="ec3c4-264">Only instances of files on local fixed disks will be returned</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-265">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-265">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dd>

<span data-ttu-id="ec3c4-266">Класс [**\_ зависимостей CIM**](cim-dependency.md) представляет ассоциацию, которая устанавливает отношения зависимости между объектами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-266">The [**CIM\_Dependency**](cim-dependency.md) class represents an association that establishes dependency relationships between objects.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-267">**\_ДЕПЕНДЕНЦИКОНТЕКСТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-267">**CIM\_DependencyContext**</span></span>](cim-dependencycontext.md)
</dt> <dd>

<span data-ttu-id="ec3c4-268">Отношение [**CIM \_ депенденциконтекст**](cim-dependencycontext.md) связывает класс [**\_ зависимостей CIM**](cim-dependency.md) с одним или несколькими объектами [**\_ конфигурации CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-268">The [**CIM\_DependencyContext**](cim-dependencycontext.md) relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="ec3c4-269">Например, зависимости компьютера могут изменяться в зависимости от сети, к которой подключена система.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-269">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-270">**\_ДЕСКТОПМОНИТОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-270">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-271">Класс [**CIM \_ десктопмонитор**](cim-desktopmonitor.md) представляет возможности и управление логическим устройством с настольным монитором (CRT).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-271">The [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-272">**\_ДЕВИЦЕАКЦЕССЕДБИФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-272">**CIM\_DeviceAccessedByFile**</span></span>](cim-deviceaccessedbyfile.md)
</dt> <dd>

<span data-ttu-id="ec3c4-273">Класс сопоставления [**CIM \_ девицеакцесседбифиле**](cim-deviceaccessedbyfile.md) указывает логическое устройство, доступ к которому осуществляется с помощью упоминаемого класса [**CIM \_ девицефиле**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-273">The [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-274">**\_ДЕВИЦЕКОННЕКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-274">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> <dd>

<span data-ttu-id="ec3c4-275">Класс сопоставления [**CIM \_ девицеконнектион**](cim-deviceconnection.md) представляет два или более подключенных устройства.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-275">The [**CIM\_DeviceConnection**](cim-deviceconnection.md) association class represents two or more connected devices.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-276">**\_ДЕВИЦЕЕРРОРКАУНТС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-276">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> <dd>

<span data-ttu-id="ec3c4-277">Класс [**CIM \_ девицеерроркаунтс**](cim-deviceerrorcounts.md) является статистическим классом, который содержит счетчики, связанные с ошибками для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-277">The [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="ec3c4-278">Типы ошибок определяются с помощью CCITT (REC X. 733) и ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-278">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-279">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-279">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> <dd>

<span data-ttu-id="ec3c4-280">Класс [**CIM \_ девицефиле**](cim-devicefile.md) представляет тип логического файла, который представляет устройство.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-280">The [**CIM\_DeviceFile**](cim-devicefile.md) class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="ec3c4-281">Это соглашение полезно для операционных систем, управляющих устройствами с помощью потоковой модели ввода-вывода в байтах.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-281">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="ec3c4-282">Логическое устройство, связанное с этим файлом, указывается с помощью отношения [**CIM \_ девицеакцесседбифиле**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-282">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-283">**\_ДЕВИЦЕСАПИМПЛЕМЕНТАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-283">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dd>

<span data-ttu-id="ec3c4-284">Класс [**CIM \_ девицесапимплементатион**](cim-devicesapimplementation.md) представляет связь между точкой доступа к службе (SAP) и ее реализацией.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-284">The [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="ec3c4-285">Если с одним SAP связано много логических устройств, они работают совместно, чтобы предоставить точку доступа.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-285">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="ec3c4-286">При наличии различных реализаций SAP каждая реализация приводит к отдельным экземплярам объекта SAP.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-286">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-287">**\_ДЕВИЦЕСЕРВИЦЕИМПЛЕМЕНТАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-287">**CIM\_DeviceServiceImplementation**</span></span>](cim-deviceserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="ec3c4-288">Класс [**CIM \_ девицесервицеимплементатион**](cim-deviceserviceimplementation.md) представляет ассоциацию между службой и ее реализацией.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-288">The [**CIM\_DeviceServiceImplementation**](cim-deviceserviceimplementation.md) class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="ec3c4-289">Если несколько устройств связаны с одной службой, эти элементы работают совместно, чтобы предоставить службу.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-289">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="ec3c4-290">При наличии различных реализаций службы каждая реализация приводит к отдельным экземплярам объекта службы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-290">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-291">**\_ДЕВИЦЕСОФТВАРЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-291">**CIM\_DeviceSoftware**</span></span>](cim-devicesoftware.md)
</dt> <dd>

<span data-ttu-id="ec3c4-292">Отношение [**CIM \_ девицесофтваре**](cim-devicesoftware.md) определяет программное обеспечение, связанное с устройством, например драйверы, конфигурацию или программное обеспечение или встроенное по.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-292">The [**CIM\_DeviceSoftware**](cim-devicesoftware.md) relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-293">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-293">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dd>

<span data-ttu-id="ec3c4-294">Класс [**\_ каталога CIM**](cim-directory.md) представляет тип файла, который логически группирует содержащиеся в нем файлы данных и предоставляет сведения о пути для сгруппированных файлов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-294">The [**CIM\_Directory**](cim-directory.md) class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-295">**\_ДИРЕКТОРЯКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-295">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-296">Абстрактный класс [**CIM \_ директоряктион**](cim-directoryaction.md) управляет каталогами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-296">The [**CIM\_DirectoryAction**](cim-directoryaction.md) abstract class manages directories.</span></span> <span data-ttu-id="ec3c4-297">Создание каталога обрабатывается классом [**\_ креатедиректоряктион CIM**](cim-createdirectoryaction.md) , а удаление каталога обрабатывается классом [**CIM \_ ремоведиректоряктион**](cim-removedirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-297">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-298">**\_ДИРЕКТОРИКОНТАИНСФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-298">**CIM\_DirectoryContainsFile**</span></span>](cim-directorycontainsfile.md)
</dt> <dd>

<span data-ttu-id="ec3c4-299">Класс [**CIM \_ директориконтаинсфиле**](cim-directorycontainsfile.md) представляет связь между каталогом и файлами, содержащимися в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-299">The [**CIM\_DirectoryContainsFile**](cim-directorycontainsfile.md) class represents an association between a directory and files contained within that directory.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-300">**\_ДИРЕКТОРИСПЕЦИФИКАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-300">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> <dd>

<span data-ttu-id="ec3c4-301">Класс [**CIM \_ директориспеЦификатион**](cim-directoryspecification.md) захватывает основную структуру каталогов программного элемента.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-301">The [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class captures the major directory structure of a software element.</span></span> <span data-ttu-id="ec3c4-302">Этот класс используется для организации файлов программного элемента в управляемые единицы, которые могут быть перемещены на компьютерную систему.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-302">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-303">**\_ДИРЕКТОРИСПЕЦИФИКАТИОНФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-303">**CIM\_DirectorySpecificationFile**</span></span>](cim-directoryspecificationfile.md)
</dt> <dd>

<span data-ttu-id="ec3c4-304">Ассоциация [**\_ директориспеЦификатионфиле CIM**](cim-directoryspecificationfile.md) представляет каталог, содержащий файл, указанный в ссылке на класс [**CIM \_ директориспеЦификатион**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-304">The [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-305">**\_ДИСКРЕТЕСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-305">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-306">Класс [**CIM \_ дискретесенсор**](cim-discretesensor.md) имеет набор допустимых строковых значений, которые он может сообщить.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-306">The [**CIM\_DiscreteSensor**](cim-discretesensor.md) class has a set of legal string values that it can report.</span></span> <span data-ttu-id="ec3c4-307">Значения перечисляются в свойстве **поссиблевалуес** датчика.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-307">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="ec3c4-308">Дискретный датчик всегда имеет текущее считывание, соответствующее одному из перечисляемых значений.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-308">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-309">**\_ДИСКДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-309">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dd>

<span data-ttu-id="ec3c4-310">Класс [**CIM \_ дискдриве**](cim-diskdrive.md) представляет физический диск, отображаемый операционной системой.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-310">The [**CIM\_DiskDrive**](cim-diskdrive.md) class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="ec3c4-311">Функции дискового накопителя соответствуют логическим характеристикам управления диска и, в некоторых случаях, могут не отражать физические характеристики устройства.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-311">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="ec3c4-312">Интерфейс к физическому диску является членом этого класса.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-312">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="ec3c4-313">Однако объект, основанный на другом логическом устройстве, не является членом этого класса.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-313">However, an object based on another logical device is not a member of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-314">**\_ДИСКЕТТЕДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-314">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dd>

<span data-ttu-id="ec3c4-315">Класс [**CIM \_ дискеттедриве**](cim-diskettedrive.md) представляет возможности и управление флоппи-дисководом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-315">The [**CIM\_DisketteDrive**](cim-diskettedrive.md) class represents the capabilities and management of a diskette drive.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-316">**\_ДИСКПАРТИТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-316">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dd>

<span data-ttu-id="ec3c4-317">Класс [**CIM \_ дискпартитион**](cim-diskpartition.md) представляет непрерывный диапазон логических блоков, идентифицируемый операционной системой посредством полей типа и подтипа секции.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-317">The [**CIM\_DiskPartition**](cim-diskpartition.md) class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="ec3c4-318">Разделы диска должны быть непосредственно реализованы физическим носителем (обозначено ассоциацией [**CIM \_ реализесдискпартитион**](cim-realizesdiskpartition.md) ) или созданы на томах хранения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-318">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-319">**\_ДИСКСПАЦЕЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-319">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> <dd>

<span data-ttu-id="ec3c4-320">Класс [**CIM \_ дискспацечекк**](cim-diskspacecheck.md) проверяет объем свободного места в системе и указывает его в свойстве **аваилабледискспаце** .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-320">The [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class checks the system's amount of available disk space and specifies it in the **AvailableDiskSpace** property.</span></span> <span data-ttu-id="ec3c4-321">Сведения сравниваются со значением свойства **аваилаблеспаце** объекта [**\_ FileSystem CIM**](cim-filesystem.md) , связанного с объектом [**CIM \_ ComputerSystem**](cim-computersystem.md) , который описывает системную среду.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-321">Details are compared with the value in the **AvailableSpace** property of the [**CIM\_FileSystem**](cim-filesystem.md) object that is associated with the [**CIM\_ComputerSystem**](cim-computersystem.md) object, which describes the system environment.</span></span> <span data-ttu-id="ec3c4-322">Если значение свойства **аваилаблеспаце** больше или равно значению, указанному в свойстве **аваилабледискспаце** , условие выполнено.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-322">When the value of the **AvailableSpace** property is greater than or equal to the value specified in the **AvailableDiskSpace** property, the condition is satisfied.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-323">**\_Отображение CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-323">**CIM\_Display**</span></span>](cim-display.md)
</dt> <dd>

<span data-ttu-id="ec3c4-324">Класс [**- \_ дисплей CIM**](cim-display.md) является родительским классом для группирования различных устройств вывода.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-324">The [**CIM\_Display**](cim-display.md) class is a parent class for grouping miscellaneous display devices.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-325">**канал передачи CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-325">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dd>

<span data-ttu-id="ec3c4-326">Класс [**CIM \_ DMA**](cim-dma.md) представляет архитектуру компьютера с прямым доступом к памяти (DMA).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-326">The [**CIM\_DMA**](cim-dma.md) class represents computer architecture direct memory access (DMA).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-327">**\_Прикрепленная CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-327">**CIM\_Docked**</span></span>](cim-docked.md)
</dt> <dd>

<span data-ttu-id="ec3c4-328">[**\_ Прикрепленная Ассоциация CIM**](cim-docked.md) представляет связь между двумя корпусами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-328">The [**CIM\_Docked**](cim-docked.md) association represents the relationship between two chassis.</span></span> <span data-ttu-id="ec3c4-329">Например, портативный компьютер (тип корпуса) можно закрепить на стыковочный станции (другой тип корпуса).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-329">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="ec3c4-330">Эта типичная связь описана явно.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-330">This typical relationship is explicitly described.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-331">**\_ЕЛЕМЕНТКАПАЦИТИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-331">**CIM\_ElementCapacity**</span></span>](cim-elementcapacity.md)
</dt> <dd>

<span data-ttu-id="ec3c4-332">Класс [**CIM \_ елементкапаЦити**](cim-elementcapacity.md) связывает объект [**CIM \_ фисикалкапаЦити**](cim-physicalcapacity.md) с одним или несколькими физическими элементами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-332">The [**CIM\_ElementCapacity**](cim-elementcapacity.md) class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="ec3c4-333">Он связывает описание минимальных и максимальных требований к оборудованию (или возможностей) с описываемыми физическими элементами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-333">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-334">**\_ЕЛЕМЕНТКОНФИГУРАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-334">**CIM\_ElementConfiguration**</span></span>](cim-elementconfiguration.md)
</dt> <dd>

<span data-ttu-id="ec3c4-335">Ассоциация [**CIM \_ елементконфигуратион**](cim-elementconfiguration.md) связывает объект [**\_ конфигурации CIM**](cim-configuration.md) с одним или несколькими управляемыми системными элементами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-335">The [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="ec3c4-336">Объект **\_ конфигурации CIM** представляет определенное поведение или требуемое функциональное состояние для связанного [**\_ манажедсистемелемент CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-336">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-337">**\_ЕЛЕМЕНТСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-337">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="ec3c4-338">Класс [**CIM \_ елементсеттинг**](cim-elementsetting.md) представляет ассоциацию между управляемыми системными элементами и определенным для них классом параметров.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-338">The [**CIM\_ElementSetting**](cim-elementsetting.md) class represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-339">**\_ЕЛЕМЕНТСЛИНКЕД CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-339">**CIM\_ElementsLinked**</span></span>](cim-elementslinked.md)
</dt> <dd>

<span data-ttu-id="ec3c4-340">Ассоциация [**CIM \_ елементслинкед**](cim-elementslinked.md) представляет физические элементы, которые соединяются физической связью.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-340">The [**CIM\_ElementsLinked**](cim-elementslinked.md) association represents physical elements that are cabled together by a physical link.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-341">**\_ЕРРОРКАУНТЕРСФОРДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-341">**CIM\_ErrorCountersForDevice**</span></span>](cim-errorcountersfordevice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-342">Класс [**CIM \_ ерроркаунтерсфордевице**](cim-errorcountersfordevice.md) связывает класс [**CIM \_ девицеерроркаунтс**](cim-deviceerrorcounts.md) с логическим устройством, к которому оно применяется.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-342">The [**CIM\_ErrorCountersForDevice**](cim-errorcountersfordevice.md) class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-343">**\_ЕКСЕКУТЕПРОГРАМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-343">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> <dd>

<span data-ttu-id="ec3c4-344">Класс [**CIM \_ ексекутепрограм**](cim-executeprogram.md) представляет файлы, которые могут быть выполнены в системе, в которой установлен программный элемент.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-344">The [**CIM\_ExecuteProgram**](cim-executeprogram.md) class represents files that can be executed on the system where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-345">**\_Экспорт CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-345">**CIM\_Export**</span></span>](cim-export.md)
</dt> <dd>

<span data-ttu-id="ec3c4-346">Класс [**\_ экспорта CIM**](cim-export.md) представляет связь между локальной файловой системой и ее каталогами, что означает, что указанные каталоги доступны для подключения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-346">The [**CIM\_Export**](cim-export.md) class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="ec3c4-347">При экспорте всей файловой системы каталог должен ссылаться на самый верхний каталог файловой системы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-347">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-348">**\_ЕКСТРАКАПАЦИТИГРАУП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-348">**CIM\_ExtraCapacityGroup**</span></span>](cim-extracapacitygroup.md)
</dt> <dd>

<span data-ttu-id="ec3c4-349">Класс [**CIM \_ екстракапаЦитиграуп**](cim-extracapacitygroup.md) является производным от группы избыточности, которая указывает, что агрегированные элементы имеют больше емкости или возможностей, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-349">The [**CIM\_ExtraCapacityGroup**](cim-extracapacitygroup.md) class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="ec3c4-350">Примером такого типа избыточности является установка N + 1 источников питания или вентиляторов в системе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-350">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-351">**\_Вентилятор CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-351">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dd>

<span data-ttu-id="ec3c4-352">Класс [**\_ вентилятора CIM**](cim-fan.md) представляет возможности и управление устройством охлаждения вентилятора.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-352">The [**CIM\_Fan**](cim-fan.md) class represents the capabilities and management of a fan cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-353">**\_ФИЛЕАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-353">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-354">Класс [**CIM \_ филеактион**](cim-fileaction.md) позволяет автору размещать файлы, уже существующие на компьютере пользователя, а затем перемещать или копировать эти файлы в новое место.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-354">The [**CIM\_FileAction**](cim-fileaction.md) class allows the author to locate files that already exist on a user's computer, and then move or copy those files to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-355">**\_ФИЛЕСПЕЦИФИКАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-355">**CIM\_FileSpecification**</span></span>](cim-filespecification.md)
</dt> <dd>

<span data-ttu-id="ec3c4-356">Класс [**CIM \_ филеспеЦификатион**](cim-filespecification.md) представляет файл, который либо включен, либо выключен в системе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-356">The [**CIM\_FileSpecification**](cim-filespecification.md) class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="ec3c4-357">Файл находится в каталоге, определенном Ассоциацией [**CIM \_ директориспеЦификатионфиле**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-357">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="ec3c4-358">Метод [**Invoke**](invoke-method-in-class-cim-filespecification.md) использует сведения для проверки существования файла.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-358">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="ec3c4-359">Обратите внимание, что свойства со значением **null** не проверяются.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-359">Note that properties with a **Null** value are not checked.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-360">**\_ФИЛЕСТОРАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-360">**CIM\_FileStorage**</span></span>](cim-filestorage.md)
</dt> <dd>

<span data-ttu-id="ec3c4-361">Ассоциация [**\_ филестораже CIM**](cim-filestorage.md) связывает файловую систему и логические файлы, адресованные через файловую систему.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-361">The [**CIM\_FileStorage**](cim-filestorage.md) association links the file system and the logical files addressed through the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-362">**\_Файловая система CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-362">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> <dd>

<span data-ttu-id="ec3c4-363">Класс [**\_ файловой системы CIM**](cim-filesystem.md) представляет собой файл или набор данных, который является локальным для компьютера или удаленно подключен с файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-363">The [**CIM\_FileSystem**](cim-filesystem.md) class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-364">**\_ФЛАТПАНЕЛ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-364">**CIM\_FlatPanel**</span></span>](cim-flatpanel.md)
</dt> <dd>

<span data-ttu-id="ec3c4-365">Класс [**CIM \_ флатпанел**](cim-flatpanel.md) представляет возможности и управление логическим устройством плоской панели.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-365">The [**CIM\_FlatPanel**](cim-flatpanel.md) class represents the capabilities and management of the flat panel logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-366">**\_ФРОМДИРЕКТОРЯКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-366">**CIM\_FromDirectoryAction**</span></span>](cim-fromdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-367">Ассоциация [**\_ фромдиректоряктион CIM**](cim-fromdirectoryaction.md) определяет исходный каталог для действия с файлом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-367">The [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="ec3c4-368">При использовании этой ассоциации предполагается, что исходный каталог был создан предыдущим действием.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-368">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="ec3c4-369">Эта ассоциация не может существовать с Ассоциацией [**CIM \_ фромдиректориспеЦификатион**](cim-fromdirectoryspecification.md) ; действие файла может содержать только один исходный каталог.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-369">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-370">**\_ФРОМДИРЕКТОРИСПЕЦИФИКАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-370">**CIM\_FromDirectorySpecification**</span></span>](cim-fromdirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="ec3c4-371">Ассоциация [**\_ фромдиректориспеЦификатион CIM**](cim-fromdirectoryspecification.md) определяет исходный каталог для действия с файлом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-371">The [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="ec3c4-372">При использовании этой ассоциации предполагается, что исходный каталог уже существует.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-372">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="ec3c4-373">Эта ассоциация не может существовать с Ассоциацией [**CIM \_ фромдиректоряктион**](cim-fromdirectoryaction.md) ; действие файла может содержать только один исходный каталог.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-373">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-374">**FRU в CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-374">**CIM\_FRU**</span></span>](cim-fru.md)
</dt> <dd>

<span data-ttu-id="ec3c4-375">Класс [**CIM \_ FRU**](cim-fru.md) представляет собой определенную поставщиком коллекцию продуктов и физических элементов, связанных с заменяемым ЭЛЕМЕНТОМ поля (FRU) для поддержки, обслуживания или обновления продукта в расположении клиента.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-375">The [**CIM\_FRU**](cim-fru.md) class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-376">**\_ФРУИНКЛУДЕСПРОДУКТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-376">**CIM\_FRUIncludesProduct**</span></span>](cim-fruincludesproduct.md)
</dt> <dd>

<span data-ttu-id="ec3c4-377">Класс [**CIM \_ фруинклудеспродукт**](cim-fruincludesproduct.md) указывает, что заменяемое поле (FRU) может состоять из других продуктов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-377">The [**CIM\_FRUIncludesProduct**](cim-fruincludesproduct.md) class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-378">**\_ФРУФИСИКАЛЕЛЕМЕНТС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-378">**CIM\_FRUPhysicalElements**</span></span>](cim-fruphysicalelements.md)
</dt> <dd>

<span data-ttu-id="ec3c4-379">Класс [**CIM \_ фруфисикалелементс**](cim-fruphysicalelements.md) представляет физические элементы, составляющие заменяемый элемент поля (FRU).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-379">The [**CIM\_FRUPhysicalElements**](cim-fruphysicalelements.md) class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-380">**\_ХЕАТПИПЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-380">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dd>

<span data-ttu-id="ec3c4-381">Класс [**CIM \_ хеатпипе**](cim-heatpipe.md) представляет возможности и управление охлаждающим устройством с теплоотводом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-381">The [**CIM\_HeatPipe**](cim-heatpipe.md) class represents the capabilities and management of a heat pipe cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-382">**\_ХОСТЕДАКЦЕССПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-382">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> <dd>

<span data-ttu-id="ec3c4-383">Класс [**CIM \_ хостедакцесспоинт**](cim-hostedaccesspoint.md) представляет связь между точкой доступа к службе (SAP) и системой, в которой она предоставляется.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-383">The [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md) class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="ec3c4-384">Каждая система может содержать много SAPs.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-384">Each system may host many SAPs.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-385">**\_ХОСТЕДБУТСАП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-385">**CIM\_HostedBootSAP**</span></span>](cim-hostedbootsap.md)
</dt> <dd>

<span data-ttu-id="ec3c4-386">Класс [**CIM \_ хостедбутсап**](cim-hostedbootsap.md) определяет размещение единой компьютерной системы для класса [**CIM \_ бутсап**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-386">The [**CIM\_HostedBootSAP**](cim-hostedbootsap.md) class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="ec3c4-387">Так как эта связь является подклассом из [**CIM \_ хостедакцесспоинт**](cim-hostedaccesspoint.md), она наследует схему определения области и именования, определенную для [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md), где точка доступа откладывается на ее систему размещения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-387">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="ec3c4-388">В этом случае **CIM \_ бутсап** должен откладываться на класс [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md) размещения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-388">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-389">**\_ХОСТЕДБУТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-389">**CIM\_HostedBootService**</span></span>](cim-hostedbootservice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-390">Класс [**CIM \_ хостедбутсервице**](cim-hostedbootservice.md) связывает систему размещения и службу загрузки.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-390">The [**CIM\_HostedBootService**](cim-hostedbootservice.md) class associates a hosting system and a boot service.</span></span> <span data-ttu-id="ec3c4-391">Так как эта связь является подклассом из [**CIM \_ HostedService**](cim-hostedservice.md), она наследует схему определения области или именования, определенную для службы, когда служба откладывается на ее систему размещения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-391">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-392">**\_ХОСТЕДФИЛЕСИСТЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-392">**CIM\_HostedFileSystem**</span></span>](cim-hostedfilesystem.md)
</dt> <dd>

<span data-ttu-id="ec3c4-393">Ассоциация [**CIM \_ хостедфилесистем**](cim-hostedfilesystem.md) представляет собой связь между компьютерной системой и файловой системой, размещенной в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-393">The [**CIM\_HostedFileSystem**](cim-hostedfilesystem.md) association represents a link between the computer system and the file system hosted on the computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-394">**\_ХОСТЕДЖОБДЕСТИНАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-394">**CIM\_HostedJobDestination**</span></span>](cim-hostedjobdestination.md)
</dt> <dd>

<span data-ttu-id="ec3c4-395">Класс [**CIM \_ хостеджобдестинатион**](cim-hostedjobdestination.md) представляет ассоциацию между назначением задания и системой, в которой оно находится.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-395">The [**CIM\_HostedJobDestination**](cim-hostedjobdestination.md) class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="ec3c4-396">В системе может размещаться много очередей заданий.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-396">A system may host many job queues.</span></span> <span data-ttu-id="ec3c4-397">Назначения заданий откладываются на систему размещения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-397">Job destinations defer to the hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-398">**CIM \_ HostedService**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-398">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-399">Класс [**CIM \_ HostedService**](cim-hostedservice.md) представляет ассоциацию между службой и системой, в которой находятся функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-399">The [**CIM\_HostedService**](cim-hostedservice.md) class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="ec3c4-400">В системе может быть размещено множество служб, которые откладываются на систему размещения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-400">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="ec3c4-401">Модель не представляет службы, размещенные в нескольких системах.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-401">The model does not represent services hosted across multiple systems.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-402">**\_ИНФРАРЕДКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-402">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-403">Класс [**CIM \_ инфраредконтроллер**](cim-infraredcontroller.md) представляет возможности и Управление контроллером инфракрасной связи.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-403">The [**CIM\_InfraredController**](cim-infraredcontroller.md) class represents the capabilities and management of an infrared controller.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-404">**\_ИНСТАЛЛЕДОС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-404">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dd>

<span data-ttu-id="ec3c4-405">Класс сопоставления [**CIM \_ инсталледос**](cim-installedos.md) представляет связь между компьютерной системой и установленной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-405">The [**CIM\_InstalledOS**](cim-installedos.md) association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="ec3c4-406">Операционная система устанавливается, когда она находится в системе хранения данных компьютера (например, копируется на диск или загружается в память).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-406">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-407">**\_ИНСТАЛЛЕДСОФТВАРИЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-407">**CIM\_InstalledSoftwareElement**</span></span>](cim-installedsoftwareelement.md)
</dt> <dd>

<span data-ttu-id="ec3c4-408">Класс [**CIM \_ инсталледсофтварилемент**](cim-installedsoftwareelement.md) связывает компьютерную систему с установленным программным элементом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-408">The [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) class associates a computer system with an installed software element.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-409">**\_IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-409">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dd>

<span data-ttu-id="ec3c4-410">Класс [**CIM \_ IRQ**](cim-irq.md) представляет линию запроса на прерывание архитектуры Intel (IRQ).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-410">The [**CIM\_IRQ**](cim-irq.md) class represents an Intel architecture interrupt request line (IRQ).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-411">**\_Задание CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-411">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dd>

<span data-ttu-id="ec3c4-412">Класс [**\_ заданий CIM**](cim-job.md) представляет собой единицу работы для системы, например задание печати.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-412">The [**CIM\_Job**](cim-job.md) class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="ec3c4-413">Задание отличается от процесса, так как задание может быть запланировано.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-413">A job is distinct from a process because a job can be scheduled.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-414">**\_ЖОБДЕСТИНАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-414">**CIM\_JobDestination**</span></span>](cim-jobdestination.md)
</dt> <dd>

<span data-ttu-id="ec3c4-415">Класс [**CIM \_ жобдестинатион**](cim-jobdestination.md) представляет место отправки задания для обработки.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-415">The [**CIM\_JobDestination**](cim-jobdestination.md) class represents where a job is submitted for processing.</span></span> <span data-ttu-id="ec3c4-416">Он может ссылаться на очередь, содержащую ноль или более заданий, например очередь печати, содержащую задания печати.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-416">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="ec3c4-417">Назначения заданий размещаются на системах, аналогично тому, как службы размещаются на системах.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-417">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-418">**\_ЖОБДЕСТИНАТИОНЖОБС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-418">**CIM\_JobDestinationJobs**</span></span>](cim-jobdestinationjobs.md)
</dt> <dd>

<span data-ttu-id="ec3c4-419">Ассоциация [**\_ жобдестинатионжобс CIM**](cim-jobdestinationjobs.md) описывает место отправки задания для обработки (то есть назначение задания).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-419">The [**CIM\_JobDestinationJobs**](cim-jobdestinationjobs.md) association describes where a job is submitted for processing (that is, to which job destination).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-420">**\_Клавиатура CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-420">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> <dd>

<span data-ttu-id="ec3c4-421">Класс [**\_ клавиатуры CIM**](cim-keyboard.md) представляет возможности и управление логическим устройством с клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-421">The [**CIM\_Keyboard**](cim-keyboard.md) class represents the capabilities and management of the keyboard logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-422">**\_ЛИНКХАСКОННЕКТОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-422">**CIM\_LinkHasConnector**</span></span>](cim-linkhasconnector.md)
</dt> <dd>

<span data-ttu-id="ec3c4-423">Класс [**CIM \_ линкхасконнектор**](cim-linkhasconnector.md) связывает Кабели и ссылки, используемые в качестве физических соединителей, которые соединяют физические элементы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-423">The [**CIM\_LinkHasConnector**](cim-linkhasconnector.md) class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="ec3c4-424">Эта ассоциация явно определяет связь соединителей для [**CIM \_ фисикаллинк**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-424">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-425">**\_ЛОКАЛФИЛЕСИСТЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-425">**CIM\_LocalFileSystem**</span></span>](cim-localfilesystem.md)
</dt> <dd>

<span data-ttu-id="ec3c4-426">Класс [**CIM \_ локалфилесистем**](cim-localfilesystem.md) представляет хранилище файлов, контролируемое компьютерной системой с помощью локальных средств (например, прямой доступ к драйверу устройства).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-426">The [**CIM\_LocalFileSystem**](cim-localfilesystem.md) class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="ec3c4-427">Хранилище файлов может управляться непосредственно компьютерной системой без необходимости использовать другой компьютер в качестве файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-427">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="ec3c4-428">Однако для кластерной файловой системы файловая система является локальной и, следовательно, откладывается на кластер.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-428">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-429">**\_Расположение CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-429">**CIM\_Location**</span></span>](cim-location.md)
</dt> <dd>

<span data-ttu-id="ec3c4-430">Класс [**\_ расположения CIM**](cim-location.md) представляет позицию и адрес физического элемента.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-430">The [**CIM\_Location**](cim-location.md) class represents the position and address of a physical element.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-431">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-431">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-432">Класс [**CIM \_**](cim-logicaldevice.md) -класса представляет собой аппаратную сущность, которая может быть или не реализована в физическом оборудовании.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-432">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-433">**Логический диск CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-433">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dd>

<span data-ttu-id="ec3c4-434">Класс [**CIM \_ LogicalDisk**](cim-logicaldisk.md) представляет непрерывный диапазон логических блоков, идентифицируемый файловой системой с помощью поля **DeviceID** (ключ) диска.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-434">The [**CIM\_LogicalDisk**](cim-logicaldisk.md) class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="ec3c4-435">Например, в среде Windows поле **DeviceID** содержит букву диска; в среде UNIX она содержит путь доступа. и в среде NetWare он содержит имя тома.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-435">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-436">**\_ЛОГИКАЛДИСКБАСЕДОНПАРТИТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-436">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

<span data-ttu-id="ec3c4-437">Класс [**CIM \_ логикалдискбаседонпартитион**](cim-logicaldiskbasedonpartition.md) связывает логический диск с разделом диска, на котором он находится.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-437">The [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) class associates a logical disk with the disk partition on which it resides.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-438">**\_ЛОГИКАЛДИСКБАСЕДОНВОЛУМЕСЕТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-438">**CIM\_LogicalDiskBasedOnVolumeSet**</span></span>](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

<span data-ttu-id="ec3c4-439">Ассоциация [**\_ логикалдискбаседонволумесет CIM**](cim-logicaldiskbasedonvolumeset.md) связывает логические диски с томом, на котором они находятся.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-439">The [**CIM\_LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="ec3c4-440">Логические диски могут быть основаны на одном томе (например, предоставленном диспетчером программных томов) или в разделе диска.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-440">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-441">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-441">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="ec3c4-442">Класс [**CIM \_ логикалелемент**](cim-logicalelement.md) является базовым классом для всех системных компонентов, представляющих абстрактные системные компоненты, такие как профили, процессы или возможности системы, в форме логических устройств.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-442">The [**CIM\_LogicalElement**](cim-logicalelement.md) class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-443">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-443">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dd>

<span data-ttu-id="ec3c4-444">Класс [**CIM \_ LogicalFile**](cim-logicalfile.md) представляет именованную коллекцию данных, которая может быть исполняемым кодом, расположенным в файловой системе в экстенте хранения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-444">The [**CIM\_LogicalFile**](cim-logicalfile.md) class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-445">**\_ЛОГИКАЛИДЕНТИТИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-445">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dd>

<span data-ttu-id="ec3c4-446">Класс [**CIM \_ логикалидентити**](cim-logicalidentity.md) — это абстрактная и универсальная ассоциация, которая указывает, что два логических элемента представляют различные аспекты одной и той же базовой сущности.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-446">The [**CIM\_LogicalIdentity**](cim-logicalidentity.md) class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-447">**\_МАГНЕТУПТИКАЛДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-447">**CIM\_MagnetoOpticalDrive**</span></span>](cim-magnetoopticaldrive.md)
</dt> <dd>

<span data-ttu-id="ec3c4-448">Класс [**CIM \_ магнетуптикалдриве**](cim-magnetoopticaldrive.md) представляет возможности и управление дисководом для магнитооптических дисков, подтипом устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-448">The [**CIM\_MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-449">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-449">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="ec3c4-450">Класс [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) является базовым классом для иерархии системных элементов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-450">The [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="ec3c4-451">Любой различимый системный компонент является кандидатом для включения в этот класс.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-451">Any distinguishable system component is a candidate for inclusion in this class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-452">**\_МАНАЖЕМЕНТКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-452">**CIM\_ManagementController**</span></span>](cim-managementcontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-453">Класс [**CIM \_ манажементконтроллер**](cim-managementcontroller.md) относится к возможностям и управлению контроллером управления.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-453">The [**CIM\_ManagementController**](cim-managementcontroller.md) class relates to the capabilities and management of a management controller.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-454">**\_МЕДИААКЦЕССДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-454">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-455">Класс [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md) представляет возможность доступа к одному или нескольким носителям, а затем использует носитель для хранения и извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-455">The [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-456">**\_МЕДИАПРЕСЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-456">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-457">Ассоциация [**\_ медиапресент CIM**](cim-mediapresent.md) описывает связь, в которой доступ к экстенту хранения должен осуществляться через устройство доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-457">The [**CIM\_MediaPresent**](cim-mediapresent.md) association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-458">**\_Память CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-458">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dd>

<span data-ttu-id="ec3c4-459">Класс [**\_ памяти CIM**](cim-memory.md) представляет возможности и управление логическими устройствами, связанными с памятью.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-459">The [**CIM\_Memory**](cim-memory.md) class represents the capabilities and management of memory-related logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-460">**\_МЕМОРИКАПАЦИТИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-460">**CIM\_MemoryCapacity**</span></span>](cim-memorycapacity.md)
</dt> <dd>

<span data-ttu-id="ec3c4-461">Класс [**CIM \_ меморикапаЦити**](cim-memorycapacity.md) представляет память, которую можно установить на физическом элементе и его минимальной и максимальной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-461">The [**CIM\_MemoryCapacity**](cim-memorycapacity.md) class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="ec3c4-462">Сведения о текущей установленной памяти, а также минимальные и максимальные требования к элементу находятся в экземплярах класса [**CIM \_ фисикалмемори**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-462">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-463">**\_МЕМОРИЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-463">**CIM\_MemoryCheck**</span></span>](cim-memorycheck.md)
</dt> <dd>

<span data-ttu-id="ec3c4-464">Класс [**CIM \_ меморичекк**](cim-memorycheck.md) указывает условие для минимального объема памяти, который должен быть доступен в системе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-464">The [**CIM\_MemoryCheck**](cim-memorycheck.md) class specifies a condition for the minimum amount of memory that must be available on a system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-465">**\_МЕМОРИМАППЕДИО CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-465">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dd>

<span data-ttu-id="ec3c4-466">Класс [**CIM \_ меморимаппедио**](cim-memorymappedio.md) представляет сопоставленный в памяти ввод-вывод архитектуры компьютера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-466">The [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="ec3c4-467">Этот класс предназначен для адресации ресурсов памяти и портов ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-467">This class addresses memory and port I/O resources.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-468">**\_МЕМОРЙОНКАРД CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-468">**CIM\_MemoryOnCard**</span></span>](cim-memoryoncard.md)
</dt> <dd>

<span data-ttu-id="ec3c4-469">Класс [**CIM \_ меморйонкард**](cim-memoryoncard.md) связывает физическую память, размещенную на досках размещения, платах адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-469">The [**CIM\_MemoryOnCard**](cim-memoryoncard.md) class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="ec3c4-470">Эта ассоциация явно определяет связь памяти с картами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-470">This association explicitly defines the relationship of memory to cards.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-471">**\_МЕМОРИВИСМЕДИА CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-471">**CIM\_MemoryWithMedia**</span></span>](cim-memorywithmedia.md)
</dt> <dd>

<span data-ttu-id="ec3c4-472">Класс [**CIM \_ меморивисмедиа**](cim-memorywithmedia.md) связывает физическую память с физическим носителем и его картриджем.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-472">The [**CIM\_MemoryWithMedia**](cim-memorywithmedia.md) class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="ec3c4-473">Память обеспечивает идентификацию носителя и сохраняет данные, относящиеся к пользователю.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-473">The memory provides media identification and stores user-specific data.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-474">**\_МОДИФИСЕТТИНГАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-474">**CIM\_ModifySettingAction**</span></span>](cim-modifysettingaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-475">Класс [**CIM \_ модифисеттингактион**](cim-modifysettingaction.md) представляет сведения для изменения определенного файла параметров для конкретной записи с указанным значением.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-475">The [**CIM\_ModifySettingAction**](cim-modifysettingaction.md) class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-476">**\_MONITORRESOLUTION CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-476">**CIM\_MonitorResolution**</span></span>](cim-monitorresolution.md)
</dt> <dd>

<span data-ttu-id="ec3c4-477">Класс [**CIM \_ MonitorResolution**](cim-monitorresolution.md) представляет связь между горизонтальным и вертикальным разрешением, а также частотой обновления и режимом сканирования для настольного монитора.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-477">The [**CIM\_MonitorResolution**](cim-monitorresolution.md) class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="ec3c4-478">Значения указываются в объекте контроллера видео.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-478">Values are specified in the video controller object.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-479">**\_МОНИТОРСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-479">**CIM\_MonitorSetting**</span></span>](cim-monitorsetting.md)
</dt> <dd>

<span data-ttu-id="ec3c4-480">Класс [**CIM \_ мониторсеттинг**](cim-monitorsetting.md) связывает разрешение монитора с монитором рабочего стола, к которому он применяется.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-480">The [**CIM\_MonitorSetting**](cim-monitorsetting.md) class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-481">**\_Подключение CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-481">**CIM\_Mount**</span></span>](cim-mount.md)
</dt> <dd>

<span data-ttu-id="ec3c4-482">Класс [**\_ подключения CIM**](cim-mount.md) представляет связь между файловой системой и каталогом, к которому она присоединена.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-482">The [**CIM\_Mount**](cim-mount.md) class represents an association between a file system and a directory to which it is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-483">**\_МУЛТИСТАТЕСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-483">**CIM\_MultiStateSensor**</span></span>](cim-multistatesensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-484">Класс [**CIM \_ мултистатесенсор**](cim-multistatesensor.md) представляет набор из нескольких элементов двоичных датчиков, каждый двоичный датчик которого сообщает о логическом результате.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-484">The [**CIM\_MultiStateSensor**](cim-multistatesensor.md) class represents a multi-member set of binary sensors where each binary sensor reports a Boolean result.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-485">**\_Сетевого адаптера CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-485">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dd>

<span data-ttu-id="ec3c4-486">Класс [**CIM \_ сетевого адаптера**](cim-networkadapter.md) является абстрактным классом, который определяет основные понятия сетевого оборудования (например, постоянный адрес или скорость работы).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-486">The [**CIM\_NetworkAdapter**](cim-networkadapter.md) class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="ec3c4-487">Сведения передаются с помощью ассоциации [**CIM \_ девицесапимплементатион**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-487">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-488">**CIM \_ NFS**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-488">**CIM\_NFS**</span></span>](cim-nfs.md)
</dt> <dd>

<span data-ttu-id="ec3c4-489">Класс [**\_ NFS CIM**](cim-nfs.md) представляет удаленную файловую систему, подключенную с помощью протокола NFS, из компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-489">The [**CIM\_NFS**](cim-nfs.md) class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-490">**\_НОНВОЛАТИЛЕСТОРАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-490">**CIM\_NonVolatileStorage**</span></span>](cim-nonvolatilestorage.md)
</dt> <dd>

<span data-ttu-id="ec3c4-491">Класс [**CIM \_ нонволатилестораже**](cim-nonvolatilestorage.md) представляет возможности и управление энергонезависимым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-491">The [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="ec3c4-492">В энергонезависимой памяти предусмотрено встроенное хранилище Flash и ПЗУ.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-492">Nonvolatile memory natively includes flash and ROM storage.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-493">**CIM \_ NumericSensor**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-493">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-494">Класс [**CIM \_ NumericSensor**](cim-numericsensor.md) представляет числовой датчик, который возвращает числовые показания и при необходимости поддерживает параметры пороговых значений.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-494">The [**CIM\_NumericSensor**](cim-numericsensor.md) class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-495">**Операционная система CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-495">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dd>

<span data-ttu-id="ec3c4-496">Класс [**системы \_ CIM**](cim-operatingsystem.md) представляет собой операционную систему компьютера, которая состоит из программного обеспечения и микропрограммы, которые позволяют использовать оборудование компьютера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-496">The [**CIM\_OperatingSystem**](cim-operatingsystem.md) class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-497">**\_ОПЕРАТИНГСИСТЕМСОФТВАРЕФЕАТУРЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-497">**CIM\_OperatingSystemSoftwareFeature**</span></span>](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="ec3c4-498">Класс [**CIM \_ оператингсистемсофтварефеатуре**](cim-operatingsystemsoftwarefeature.md) представляет программные функции, составляющие операционную систему.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-498">The [**CIM\_OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) class represents the software features that make up the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-499">**\_ОСПРОЦЕСС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-499">**CIM\_OSProcess**</span></span>](cim-osprocess.md)
</dt> <dd>

<span data-ttu-id="ec3c4-500">Класс [**CIM \_ оспроцесс**](cim-osprocess.md) связывает операционную систему и один или несколько процессов, выполняющихся в контексте операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-500">The [**CIM\_OSProcess**](cim-osprocess.md) class associates the operating system and one or more processes running in the context of the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-501">**\_ОСВЕРСИОНЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-501">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> <dd>

<span data-ttu-id="ec3c4-502">Класс [**CIM \_ осверсиончекк**](cim-osversioncheck.md) указывает версии операционной системы, которые могут поддерживать программный элемент.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-502">The [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class specifies the versions of the operating system that can support a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-503">**\_ПАККАЖЕАЛАРМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-503">**CIM\_PackageAlarm**</span></span>](cim-packagealarm.md)
</dt> <dd>

<span data-ttu-id="ec3c4-504">Ассоциация [**\_ паккажеаларм CIM**](/windows/desktop/SecCrypto/extendedproperties-newenum) представляет связь, в которой устанавливается сигнальное устройство в составе пакета.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-504">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="ec3c4-505">Установка указывает на проблемы в среде пакета — состояние безопасности или его общую работоспособность.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-505">The installation indicates issues with the package's environment—its security state or its overall health.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-506">**\_ПАККАЖЕКУЛИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-506">**CIM\_PackageCooling**</span></span>](cim-packagecooling.md)
</dt> <dd>

<span data-ttu-id="ec3c4-507">Ассоциация [**CIM \_ паккажекулинг**](cim-packagecooling.md) представляет собой связь, в которой устройство охлаждения устанавливается в пакете, таком как шасси или стойка, для помощи с охлаждением пакета.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-507">The [**CIM\_PackageCooling**](cim-packagecooling.md) association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-508">**\_ПАККАЖЕДКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-508">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-509">Ассоциация [**CIM \_ паккажедкомпонент**](cim-packagedcomponent.md) представляет собой явную связь, в которой компонент обычно содержится в физическом пакете, таком как шасси или плата.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-509">The [**CIM\_PackagedComponent**](cim-packagedcomponent.md) association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-510">**\_ПАККАЖЕИНЧАССИС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-510">**CIM\_PackageInChassis**</span></span>](cim-packageinchassis.md)
</dt> <dd>

<span data-ttu-id="ec3c4-511">Ассоциация [**CIM \_ паккажеинчассис**](cim-packageinchassis.md) представляет собой связь, в которой шасси может содержать другие пакеты, такие как другие шасси и платы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-511">The [**CIM\_PackageInChassis**](cim-packageinchassis.md) association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-512">**\_ПАККАЖЕИНСЛОТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-512">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> <dd>

<span data-ttu-id="ec3c4-513">Ассоциация [**CIM \_ паккажеинслот**](cim-packageinslot.md) представляет связь между картами устройств и шасси, в котором они подключены.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-513">The [**CIM\_PackageInSlot**](cim-packageinslot.md) association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-514">**\_ПАККАЖЕТЕМПСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-514">**CIM\_PackageTempSensor**</span></span>](cim-packagetempsensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-515">Ассоциация [**\_ паккажетемпсенсор CIM**](cim-packagetempsensor.md) представляет связь, в которой датчик температуры часто устанавливается в пакете, например в шасси или стойке, для мониторинга среды пакета.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-515">The [**CIM\_PackageTempSensor**](cim-packagetempsensor.md) association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-516">**\_ПАРАЛЛЕЛКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-516">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-517">Ассоциация [**CIM \_ параллелконтроллер**](cim-parallelcontroller.md) относится к возможностям и управлению логическим устройством параллельного порта.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-517">The [**CIM\_ParallelController**](cim-parallelcontroller.md) association relates to the capabilities and management of the parallel port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-518">**\_ПАРТИЦИПАТЕСИНСЕТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-518">**CIM\_ParticipatesInSet**</span></span>](cim-participatesinset.md)
</dt> <dd>

<span data-ttu-id="ec3c4-519">Класс [**CIM \_ партиЦипатесинсет**](cim-participatesinset.md) определяет физические элементы, которые должны быть заменены вместе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-519">The [**CIM\_ParticipatesInSet**](cim-participatesinset.md) class identifies physical elements that should be replaced together.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-520">**\_ПЦИКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-520">**CIM\_PCIController**</span></span>](cim-pcicontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-521">Класс [**CIM \_ пЦиконтроллер**](cim-pcicontroller.md) представляет свойства и Управление контроллером PCI.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-521">The [**CIM\_PCIController**](cim-pcicontroller.md) class represents the properties and management of a PCI controller.</span></span> <span data-ttu-id="ec3c4-522">Свойства в этом классе и его подклассах определены в различных спецификациях PCI, опубликованных в SIG PCI.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-522">The properties in this class and its subclasses are defined in the various PCI specifications published by the PCI SIG.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-523">**\_ПКМЦИАКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-523">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-524">Класс [**CIM \_ пкмЦиаконтроллер**](cim-pcmciacontroller.md) представляет возможности и Управление контроллером международной связи с картой памяти персональных компьютеров (PCMCIA).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-524">The [**CIM\_PCMCIAController**](cim-pcmciacontroller.md) class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-525">**\_ПКВИДЕОКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-525">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-526">[**CIM \_ пквидеоконтроллер**](cim-pcvideocontroller.md) представляет возможности и управление видеоконтроллером персональных компьютеров, подтипом видеоконтроллера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-526">The [**CIM\_PCVideoController**](cim-pcvideocontroller.md) represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-527">**\_ПЕКСТЕНТРЕДУНДАНЦИКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-527">**CIM\_PExtentRedundancyComponent**</span></span>](cim-pextentredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-528">Класс [**CIM \_ пекстентредунданцикомпонент**](cim-pextentredundancycomponent.md) представляет физические экстенты, участвующие в группе избыточности хранилища.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-528">The [**CIM\_PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) class represents the physical extents that participate in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-529">**\_ФИСИКАЛКАПАЦИТИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-529">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> <dd>

<span data-ttu-id="ec3c4-530">Класс [**CIM \_ фисикалкапаЦити**](cim-physicalcapacity.md) является абстрактным классом, который представляет минимальные и максимальные требования физического элемента и его способность поддерживать различные типы оборудования.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-530">The [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="ec3c4-531">Например, минимальные и максимальные требования к памяти можно моделировать как подкласс **CIM \_ фисикалкапаЦити**.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-531">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-532">**\_ФИСИКАЛКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-532">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-533">Класс [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md) представляет компонент нижнего или базового уровня в пакете.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-533">The [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="ec3c4-534">Физический элемент, не являющийся ссылкой, соединителем или пакетом, является потомком (или членом) этого класса.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-534">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-535">**\_ФИСИКАЛКОННЕКТОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-535">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dd>

<span data-ttu-id="ec3c4-536">Класс [**CIM \_ фисикалконнектор**](cim-physicalconnector.md) представляет любой физический элемент, используемый для подключения к другим элементам.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-536">The [**CIM\_PhysicalConnector**](cim-physicalconnector.md) class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="ec3c4-537">Любой объект, который может подключаться и передавать сигналы или мощь между двумя или более физическими элементами, является потомком (или членом) этого класса.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-537">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-538">**\_ФИСИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-538">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> <dd>

<span data-ttu-id="ec3c4-539">Подклассы [**CIM \_ фисикалелемент**](cim-physicalelement.md) определяют любой компонент системы, имеющий уникальное физическое удостоверение.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-539">The [**CIM\_PhysicalElement**](cim-physicalelement.md) subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="ec3c4-540">Экземпляры этого класса могут быть определены в терминах меток, которые могут быть физически присоединены к объекту.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-540">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-541">**\_ФИСИКАЛЕЛЕМЕНТЛОКАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-541">**CIM\_PhysicalElementLocation**</span></span>](cim-physicalelementlocation.md)
</dt> <dd>

<span data-ttu-id="ec3c4-542">Класс [**CIM \_ фисикалелементлокатион**](cim-physicalelementlocation.md) связывает физический элемент с объектом [**\_ расположения CIM**](cim-location.md) для целей инвентаризации или замены.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-542">The [**CIM\_PhysicalElementLocation**](cim-physicalelementlocation.md) class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-543">**\_ФИСИКАЛЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-543">**CIM\_PhysicalExtent**</span></span>](cim-physicalextent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-544">Класс [**CIM \_ фисикалекстент**](cim-physicalextent.md) представляет реализацию SCC RAID.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-544">The [**CIM\_PhysicalExtent**](cim-physicalextent.md) class represents an SCC RAID implementation.</span></span> <span data-ttu-id="ec3c4-545">Он определяет последовательные адреса блочных адресов на одном запоминающем устройстве, которые обрабатываются как единая область хранения в одном классе [**CIM \_ сторажередунданциграуп**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-545">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="ec3c4-546">Альтернативой, при использовании автоматической конфигурации, является создание экземпляра или расширение класса [**CIM \_ аггрегатепекстент**](cim-aggregatepextent.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-546">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-547">**\_ФИСИКАЛФРАМЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-547">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> <dd>

<span data-ttu-id="ec3c4-548">Класс [**CIM \_ фисикалфраме**](cim-physicalframe.md) является родительским классом стойки, корпуса и других корпусов, так как они определены в классах расширения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-548">The [**CIM\_PhysicalFrame**](cim-physicalframe.md) class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="ec3c4-549">Такие свойства, как **висиблеаларм** и **аудиблеаларм**, и данные, связанные с нарушениями безопасности, включены в этот родительский класс.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-549">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-550">**\_ФИСИКАЛЛИНК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-550">**CIM\_PhysicalLink**</span></span>](cim-physicallink.md)
</dt> <dd>

<span data-ttu-id="ec3c4-551">Класс [**CIM \_ фисикаллинк**](cim-physicallink.md) представляет кабель физических элементов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-551">The [**CIM\_PhysicalLink**](cim-physicallink.md) class represents the cabling of physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-552">**\_ФИСИКАЛМЕДИА CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-552">**CIM\_PhysicalMedia**</span></span>](cim-physicalmedia.md)
</dt> <dd>

<span data-ttu-id="ec3c4-553">Класс [**CIM \_ фисикалмедиа**](cim-physicalmedia.md) представляет типы документации и среды хранения, такие как ленты, компакт-диски и т. д.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-553">The [**CIM\_PhysicalMedia**](cim-physicalmedia.md) class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-554">**\_ФИСИКАЛМЕМОРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-554">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dd>

<span data-ttu-id="ec3c4-555">Класс [**CIM \_ фисикалмемори**](cim-physicalmemory.md) представляет устройства памяти низкого уровня, такие как SIMM, модули DIMM, микросхемы памяти и т. д.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-555">The [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-556">**\_ФИСИКАЛПАККАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-556">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dd>

<span data-ttu-id="ec3c4-557">Класс [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md) представляет физические элементы, содержащие или ведущие другие компоненты.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-557">The [**CIM\_PhysicalPackage**](cim-physicalpackage.md) class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="ec3c4-558">Примерами являются корпус стойки или плата адаптера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-558">Examples are a rack enclosure or an adapter card.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-559">**\_ПОИНТИНГДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-559">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-560">Класс [**CIM \_ поинтингдевице**](cim-pointingdevice.md) представляет устройство, которое указывает на регионы на дисплее.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-560">The [**CIM\_PointingDevice**](cim-pointingdevice.md) class represents a device that points to regions on the display.</span></span> <span data-ttu-id="ec3c4-561">Все устройства, управляющие указателем или указывающие на регионы на визуальном дисплее, являются членом этого класса.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-561">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="ec3c4-562">Например, мышь, перо, Сенсорная панель или планшет.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-562">For example, a mouse, stylus, touch pad, or tablet.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-563">**\_ПОТСМОДЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-563">**CIM\_POTSModem**</span></span>](cim-potsmodem.md)
</dt> <dd>

<span data-ttu-id="ec3c4-564">Класс [**CIM \_ потсмодем**](cim-potsmodem.md) представляет устройство, которое преобразует двоичные данные в звуковые модуляции для передачи на основе звука, подключаясь к сети "Обычная старая телефонная система" (POTS).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-564">The [**CIM\_POTSModem**](cim-potsmodem.md) class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-565">**Источник \_ питания CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-565">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> <dd>

<span data-ttu-id="ec3c4-566">Класс [**\_ источника CIM**](cim-powersupply.md) представляет возможности и управление логическим устройством источника питания.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-566">The [**CIM\_PowerSupply**](cim-powersupply.md) class represents the capabilities and management of the power supply logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-567">**\_Принтер CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-567">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dd>

<span data-ttu-id="ec3c4-568">Класс [**\_ Printer CIM**](cim-printer.md) представляет возможности и управление логическим устройством принтера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-568">The [**CIM\_Printer**](cim-printer.md) class represents the capabilities and management of the printer logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-569">**\_Процесс CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-569">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dd>

<span data-ttu-id="ec3c4-570">Класс [**\_ процессов CIM**](cim-process.md) представляет отдельный экземпляр выполняющейся программы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-570">The [**CIM\_Process**](cim-process.md) class represents a single instance of a running program.</span></span> <span data-ttu-id="ec3c4-571">Пользователь обычно видит процесс как приложение или задачу.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-571">A user typically sees a process as an application or task.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-572">**\_ПРОЦЕССЕКСЕКУТАБЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-572">**CIM\_ProcessExecutable**</span></span>](cim-processexecutable.md)
</dt> <dd>

<span data-ttu-id="ec3c4-573">Класс [**CIM \_ процессексекутабле**](cim-processexecutable.md) представляет связь между процессом и файлом данных и указывает, что файл участвует в выполнении процесса.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-573">The [**CIM\_ProcessExecutable**](cim-processexecutable.md) class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-574">**\_Процессор CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-574">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-575">Класс [**\_ процессора CIM**](cim-processor.md) представляет возможности и управление логическим устройством процессора.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-575">The [**CIM\_Processor**](cim-processor.md) class represents the capabilities and management of the processor logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-576">**\_ПРОЦЕСССРЕАД CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-576">**CIM\_ProcessThread**</span></span>](cim-processthread.md)
</dt> <dd>

<span data-ttu-id="ec3c4-577">Класс [**CIM \_ процесссреад**](cim-processthread.md) представляет связь между процессом и потоками, выполняемыми в контексте процесса.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-577">The [**CIM\_ProcessThread**](cim-processthread.md) class represents a link between a process and the threads running in the context of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-578">**\_Продукт CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-578">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dd>

<span data-ttu-id="ec3c4-579">Класс [**\_ продукта CIM**](cim-product.md) является конкретным классом, представляющим коллекцию физических элементов, программных функций и других продуктов, приобретенных как единое целое.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-579">The [**CIM\_Product**](cim-product.md) class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="ec3c4-580">Приобретение подразумевает соглашение между поставщиком и потребителем, что может повлиять на лицензирование, поддержку и гарантию продукта.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-580">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-581">**\_ПРОДУКТФРУ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-581">**CIM\_ProductFRU**</span></span>](cim-productfru.md)
</dt> <dd>

<span data-ttu-id="ec3c4-582">Класс [**CIM \_ продуктфру**](cim-productfru.md) представляет связь между продуктом и заменяемым ЭЛЕМЕНТОМ поля (FRU), который предоставляет сведения о компонентах продукта, которые были или заменяются.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-582">The [**CIM\_ProductFRU**](cim-productfru.md) class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-583">**\_ПРОДУКТПАРЕНТЧИЛД CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-583">**CIM\_ProductParentChild**</span></span>](cim-productparentchild.md)
</dt> <dd>

<span data-ttu-id="ec3c4-584">Ассоциация [**\_ продуктпарентчилд CIM**](cim-productparentchild.md) определяет иерархию "родители-потомки" между продуктами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-584">The [**CIM\_ProductParentChild**](cim-productparentchild.md) association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="ec3c4-585">Например, продукт может быть объединен с другими продуктами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-585">For example, a product can come bundled with other products.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-586">**\_ПРОДУКТФИСИКАЛЕЛЕМЕНТС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-586">**CIM\_ProductPhysicalElements**</span></span>](cim-productphysicalelements.md)
</dt> <dd>

<span data-ttu-id="ec3c4-587">Класс [**CIM \_ продуктфисикалелементс**](cim-productphysicalelements.md) представляет физические элементы, составляющие продукт.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-587">The [**CIM\_ProductPhysicalElements**](cim-productphysicalelements.md) class represents the physical elements that make up a product.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-588">**\_ПРОДУКТПРОДУКТДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-588">**CIM\_ProductProductDependency**</span></span>](cim-productproductdependency.md)
</dt> <dd>

<span data-ttu-id="ec3c4-589">Класс [**CIM \_ продуктпродуктдепенденци**](cim-productproductdependency.md) представляет ассоциацию между двумя продуктами, которая указывает, что один из них должен быть установлен или отсутствовать для работы другого.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-589">The [**CIM\_ProductProductDependency**](cim-productproductdependency.md) class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="ec3c4-590">Это концептуально эквивалентно ассоциации [**CIM \_ сервицесервицедепенденци**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-590">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-591">**\_ПРОДУКТСОФТВАРЕФЕАТУРЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-591">**CIM\_ProductSoftwareFeatures**</span></span>](cim-productsoftwarefeatures.md)
</dt> <dd>

<span data-ttu-id="ec3c4-592">Ассоциация [**\_ продуктсофтварефеатурес CIM**](cim-productsoftwarefeatures.md) определяет функции программного обеспечения для конкретного продукта.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-592">The [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association identifies the software features for a particular product.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-593">**\_ПРОДУКТСУППОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-593">**CIM\_ProductSupport**</span></span>](cim-productsupport.md)
</dt> <dd>

<span data-ttu-id="ec3c4-594">Класс [**CIM \_ продуктсуппорт**](cim-productsupport.md) представляет связь между продуктом и поддержкой доступа, которая передает сведения о получении поддержки для продукта.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-594">The [**CIM\_ProductSupport**](cim-productsupport.md) class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="ec3c4-595">Для продукта доступны различные типы поддержки. один и тот же объект поддержки может предоставить помощь для нескольких продуктов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-595">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-596">**\_ПРОТЕКТЕДСПАЦЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-596">**CIM\_ProtectedSpaceExtent**</span></span>](cim-protectedspaceextent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-597">Класс [**CIM \_ протектедспацеекстент**](cim-protectedspaceextent.md) представляет адреса адресации логических блоков, которые рассматриваются как один экстент хранения, но находятся в одном физическом экстенте.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-597">The [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) class represents addressable logical-block addresses, which are treated as a single storage extent, but are located on a single physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-598">**\_ПСЕКСТЕНТБАСЕДОНПЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-598">**CIM\_PSExtentBasedOnPExtent**</span></span>](cim-psextentbasedonpextent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-599">Класс [**CIM \_ псекстентбаседонпекстент**](cim-psextentbasedonpextent.md) связывает экстенты защищенного пространства, основанные на физическом экстенте.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-599">The [**CIM\_PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) class associates protected space extents that are based on a physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-600">**\_Стойка CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-600">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> <dd>

<span data-ttu-id="ec3c4-601">Класс [**\_ стойки CIM**](cim-rack.md) представляет стойку (физическую рамку или корпус), в котором хранятся шасси.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-601">The [**CIM\_Rack**](cim-rack.md) class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="ec3c4-602">Как правило, стойка представляет корпус; все действующие компоненты упаковываются в корпус.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-602">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-603">**\_Реализации CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-603">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dd>

<span data-ttu-id="ec3c4-604">Класс "классы [**CIM \_**](cim-realizes.md) " представляет ассоциацию, которая определяет сопоставление между логическим устройством и физическим компонентом, реализующим устройство.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-604">The [**CIM\_Realizes**](cim-realizes.md) class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-605">**\_РЕАЛИЗЕСАГГРЕГАТЕПЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-605">**CIM\_RealizesAggregatePExtent**</span></span>](cim-realizesaggregatepextent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-606">Ассоциация [**\_ реализесаггрегатепекстент CIM**](cim-realizesaggregatepextent.md) представляет связь, в которой класс [**CIM \_ аггрегатепекстент**](cim-aggregatepextent.md) реализован на физическом носителе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-606">The [**CIM\_RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-607">**\_РЕАЛИЗЕСДИСКПАРТИТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-607">**CIM\_RealizesDiskPartition**</span></span>](cim-realizesdiskpartition.md)
</dt> <dd>

<span data-ttu-id="ec3c4-608">Класс [**CIM \_ реализесдискпартитион**](cim-realizesdiskpartition.md) представляет раздел диска на физическом носителе, который моделирует создание разделов на необработанном диске SCSI или IDE.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-608">The [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-609">**\_РЕАЛИЗЕСПЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-609">**CIM\_RealizesPExtent**</span></span>](cim-realizespextent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-610">Ассоциация [**\_ реализеспекстент CIM**](cim-realizespextent.md) представляет связь, в которой физические экстенты реализуются на физическом носителе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-610">The [**CIM\_RealizesPExtent**](cim-realizespextent.md) association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="ec3c4-611">Кроме того, указывается начальный адрес физического экстента на физическом носителе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-611">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-612">**\_РЕБУТАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-612">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-613">Класс [**CIM \_ ребутактион**](cim-rebootaction.md) вызывает перезагрузку системы, в которой установлен программный элемент.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-613">The [**CIM\_RebootAction**](cim-rebootaction.md) class causes a system reboot where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-614">**\_РЕДУНДАНЦИКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-614">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-615">Класс [**CIM \_ редунданцикомпонент**](cim-redundancycomponent.md) связывает группу избыточности, состоящую из управляемых системных элементов, и указывает, что вместе элементы обеспечивают избыточность.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-615">The [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="ec3c4-616">Все элементы, Объединенные в группу избыточности, должны быть экземплярами одного и того же класса объектов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-616">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-617">**\_РЕДУНДАНЦИГРАУП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-617">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> <dd>

<span data-ttu-id="ec3c4-618">Класс [**CIM \_ редунданциграуп**](cim-redundancygroup.md) представляет коллекцию управляемых системных элементов, которая указывает, что агрегированные компоненты вместе обеспечивают избыточность.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-618">The [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="ec3c4-619">Все элементы, Объединенные в группу избыточности, должны быть экземплярами одного и того же класса объектов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-619">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-620">**\_Холодильника CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-620">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dd>

<span data-ttu-id="ec3c4-621">Класс [**CIM \_ холодильника**](cim-refrigeration.md) представляет возможности и управление устройством охлаждения холодильника.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-621">The [**CIM\_Refrigeration**](cim-refrigeration.md) class represents the capabilities and management of a refrigeration cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-622">**\_РЕЛАТЕДСТАТИСТИКС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-622">**CIM\_RelatedStatistics**</span></span>](cim-relatedstatistics.md)
</dt> <dd>

<span data-ttu-id="ec3c4-623">Ассоциация [**\_ релатедстатистикс CIM**](cim-relatedstatistics.md) представляет иерархии и зависимости связанных классов [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3c4-623">The [**CIM\_RelatedStatistics**](cim-relatedstatistics.md) association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-624">**\_РЕМОТЕФИЛЕСИСТЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-624">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> <dd>

<span data-ttu-id="ec3c4-625">Класс [**CIM \_ ремотефилесистем**](cim-remotefilesystem.md) представляет собой удаленную файловую систему, доступ к которой осуществляется посредством сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-625">The [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md) class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="ec3c4-626">В этом случае хранилище файлов размещается на компьютере, который выступает в качестве файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-626">In this case, the file store is hosted by a computer, which acts as a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-627">**\_РЕМОВЕДИРЕКТОРЯКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-627">**CIM\_RemoveDirectoryAction**</span></span>](cim-removedirectoryaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-628">Класс [**CIM \_ ремоведиректоряктион**](cim-removedirectoryaction.md) удаляет каталоги для программных элементов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-628">The [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class removes directories for software elements.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-629">**\_РЕМОВЕФИЛЕАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-629">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-630">Класс [**CIM \_ ремовефилеактион**](cim-removefileaction.md) удаляет файлы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-630">The [**CIM\_RemoveFileAction**](cim-removefileaction.md) class uninstalls files.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-631">**\_Подстановка CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-631">**CIM\_ReplacementSet**</span></span>](cim-replacementset.md)
</dt> <dd>

<span data-ttu-id="ec3c4-632">Класс [**\_ замены CIM**](cim-replacementset.md) объединяет физические элементы, которые должны быть заменены вместе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-632">The [**CIM\_ReplacementSet**](cim-replacementset.md) class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="ec3c4-633">Например, при замене платы памяти микросхемы памяти компонента также могут быть удалены и заменены.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-633">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="ec3c4-634">Или можно использовать эту связь для замены или обновления набора микросхем памяти.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-634">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-635">**\_РЕСИДЕСОНЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-635">**CIM\_ResidesOnExtent**</span></span>](cim-residesonextent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-636">Класс [**CIM \_ ресидесонекстент**](cim-residesonextent.md) представляет ассоциацию между файловой системой и областью хранения, в которой она находится.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-636">The [**CIM\_ResidesOnExtent**](cim-residesonextent.md) class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="ec3c4-637">Как правило, файловая система находится на логическом диске.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-637">Typically, a file system resides on a logical disk.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-638">**\_РУННИНГОС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-638">**CIM\_RunningOS**</span></span>](cim-runningos.md)
</dt> <dd>

<span data-ttu-id="ec3c4-639">Класс [**CIM \_ руннингос**](cim-runningos.md) представляет выполняющуюся в данный момент операционную систему.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-639">The [**CIM\_RunningOS**](cim-runningos.md) class represents the currently executing operating system.</span></span> <span data-ttu-id="ec3c4-640">В любой момент в компьютерной системе может выполняться не более одной операционной системы; возможно, компьютерная система не загрузилась или ее операционная система неизвестна.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-640">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-641">**\_САПСАПДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-641">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> <dd>

<span data-ttu-id="ec3c4-642">Класс [**CIM \_ сапсапдепенденци**](cim-sapsapdependency.md) — это ассоциация между двумя точками доступа к службе (SAPS), которая указывает, что второй SAP необходим для подключения первой SAP к своей службе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-642">The [**CIM\_SAPSAPDependency**](cim-sapsapdependency.md) class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-643">**\_Сканер CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-643">**CIM\_Scanner**</span></span>](cim-scanner.md)
</dt> <dd>

<span data-ttu-id="ec3c4-644">[**\_ Сканер CIM**](cim-scanner.md) представляет возможности и управление логическим устройством сканера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-644">The [**CIM\_Scanner**](cim-scanner.md) represents the capabilities and management of the scanner logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-645">**\_СКСИКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-645">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-646">Класс [**CIM \_ сксиконтроллер**](cim-scsicontroller.md) представляет возможности и управление ЛОГИЧЕСКИМ устройством контроллера SCSI.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-646">The [**CIM\_SCSIController**](cim-scsicontroller.md) class represents the capabilities and management of the SCSI controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-647">**\_СКСИИНТЕРФАЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-647">**CIM\_SCSIInterface**</span></span>](cim-scsiinterface.md)
</dt> <dd>

<span data-ttu-id="ec3c4-648">представляет отношение [**CIM \_ контролледби**](cim-controlledby.md) , указывающее, к каким устройствам осуществляется доступ через контроллер SCSI и характеристики доступа.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-648">represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-649">**\_Датчик CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-649">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-650">Класс [**\_ датчика CIM**](cim-sensor.md) представляет аппаратное устройство, способное измерять характеристики физического свойства (например, характеристики температуры или напряжения в единой компьютерной системе).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-650">The [**CIM\_Sensor**](cim-sensor.md) class represents a hardware device that is capable of measuring the characteristics of a physical property (for example, the temperature or voltage characteristics of a unitary computer system).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-651">**\_СЕРИАЛКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-651">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-652">Класс [**CIM \_ сериалконтроллер**](cim-serialcontroller.md) представляет возможности и управление логическим устройством с последовательным портом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-652">The [**CIM\_SerialController**](cim-serialcontroller.md) class represents the capabilities and management of the serial port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-653">**\_СЕРИАЛИНТЕРФАЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-653">**CIM\_SerialInterface**</span></span>](cim-serialinterface.md)
</dt> <dd>

<span data-ttu-id="ec3c4-654">Класс [**CIM \_ сериалинтерфаце**](cim-serialinterface.md) представляет отношение [**CIM \_ контролледби**](cim-controlledby.md) , указывающее, к каким устройствам осуществляется доступ через последовательный контроллер и характеристики доступа.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-654">The [**CIM\_SerialInterface**](cim-serialinterface.md) class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-655">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-655">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dd>

<span data-ttu-id="ec3c4-656">Класс [**\_ службы CIM**](cim-service.md) представляет логический элемент, который содержит сведения для представления функциональных возможностей, предоставляемых устройством или программным обеспечением, и управления ими.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-656">The [**CIM\_Service**](cim-service.md) class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="ec3c4-657">Служба — это объект общего назначения для настройки и управления реализацией функциональности; Это не сама функциональность.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-657">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-658">**\_СЕРВИЦЕАКЦЕССБИСАП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-658">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="ec3c4-659">Класс сопоставления [**CIM \_ сервицеакцессбисап**](cim-serviceaccessbysap.md) представляет точки доступа для службы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-659">The [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md) association class represents the access points for a service.</span></span> <span data-ttu-id="ec3c4-660">Например, доступ к принтеру можно получить из NetWare, Macintosh или точек доступа к службам Windows (SAPs), которые могут размещаться в разных системах.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-660">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-661">**\_СЕРВИЦЕАКЦЕССПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-661">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dd>

<span data-ttu-id="ec3c4-662">Класс [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md) представляет возможность использования или вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-662">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="ec3c4-663">Точки доступа представляют службы, доступные для использования другими сущностями.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-663">Access points represent services that are available for use by other entities.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-664">**\_СЕРВИЦЕСАПДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-664">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> <dd>

<span data-ttu-id="ec3c4-665">Класс [**CIM \_ сервицесапдепенденци**](cim-servicesapdependency.md) представляет ассоциацию между службой и точкой доступа к службе (SAP), которая указывает на то, что служба SAP используется службой для обеспечения ее функциональности.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-665">The [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-666">**\_СЕРВИЦЕСЕРВИЦЕДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-666">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dd>

<span data-ttu-id="ec3c4-667">Класс [**CIM \_ сервицесервицедепенденци**](cim-serviceservicedependency.md) представляет ассоциацию между двумя службами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-667">The [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) class represents an association between two services.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-668">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-668">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="ec3c4-669">Класс [**\_ параметров CIM**](cim-setting.md) представляет связанные с конфигурацией и операционные параметры для одного или нескольких управляемых системных элементов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-669">The [**CIM\_Setting**](cim-setting.md) class represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-670">**\_СЕТТИНГЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-670">**CIM\_SettingCheck**</span></span>](cim-settingcheck.md)
</dt> <dd>

<span data-ttu-id="ec3c4-671">Класс [**CIM \_ сеттингчекк**](cim-settingcheck.md) определяет сведения, необходимые для проверки конкретного файла параметров для конкретной записи, которая содержит значение, равное указанному значению.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-671">The [**CIM\_SettingCheck**](cim-settingcheck.md) class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="ec3c4-672">Предполагается, что все сравнения не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-672">All comparisons are assumed to be case insensitive.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-673">**\_СЕТТИНГКОНТЕКСТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-673">**CIM\_SettingContext**</span></span>](cim-settingcontext.md)
</dt> <dd>

<span data-ttu-id="ec3c4-674">Класс [**CIM \_ сеттингконтекст**](cim-settingcontext.md) связывает объекты конфигурации с объектами Setting.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-674">The [**CIM\_SettingContext**](cim-settingcontext.md) class associates configuration objects with setting objects.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-675">**\_Слот CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-675">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dd>

<span data-ttu-id="ec3c4-676">Класс [**\_ слота CIM**](cim-slot.md) представляет соединители, в которые вставляются пакеты.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-676">The [**CIM\_Slot**](cim-slot.md) class represents connectors into which packages are inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-677">**\_СЛОТИНСЛОТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-677">**CIM\_SlotInSlot**</span></span>](cim-slotinslot.md)
</dt> <dd>

<span data-ttu-id="ec3c4-678">Отношение [**CIM \_ слотинслот**](cim-slotinslot.md) представляет возможность специального адаптера расширить существующую структуру слота, чтобы обеспечить подключение несовместимых карт в кадр или на доску размещения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-678">The [**CIM\_SlotInSlot**](cim-slotinslot.md) relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-679">**\_СОФТВАРИЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-679">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> <dd>

<span data-ttu-id="ec3c4-680">Класс [**CIM \_ софтварилемент**](cim-softwareelement.md) разбивает объект [**CIM \_ софтварефеатуре**](cim-softwarefeature.md) на набор отдельных управляемых или развертываемых частей для конкретной платформы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-680">The [**CIM\_SoftwareElement**](cim-softwareelement.md) class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="ec3c4-681">Платформа программного элемента уникально определяется базовой архитектурой оборудования и операционной системой.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-681">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-682">**\_СОФТВАРИЛЕМЕНТАКТИОНС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-682">**CIM\_SoftwareElementActions**</span></span>](cim-softwareelementactions.md)
</dt> <dd>

<span data-ttu-id="ec3c4-683">Ассоциация [**\_ софтварилементактионс CIM**](cim-softwareelementactions.md) определяет действия для программного элемента.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-683">The [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association identifies the actions for a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-684">**\_СОФТВАРИЛЕМЕНТЧЕККС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-684">**CIM\_SoftwareElementChecks**</span></span>](cim-softwareelementchecks.md)
</dt> <dd>

<span data-ttu-id="ec3c4-685">Класс сопоставления [**CIM \_ софтварилементчеккс**](cim-softwareelementchecks.md) связывает программный элемент с условием или сведениями о расположении, которые может потребоваться компоненту.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-685">The [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association class relates a software element with condition or location information that a feature may require.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-686">**\_СОФТВАРИЛЕМЕНТВЕРСИОНЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-686">**CIM\_SoftwareElementVersionCheck**</span></span>](cim-softwareelementversioncheck.md)
</dt> <dd>

<span data-ttu-id="ec3c4-687">Класс [**CIM \_ софтварилементверсиончекк**](cim-softwareelementversioncheck.md) представляет тип программного элемента, который должен существовать в среде.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-687">The [**CIM\_SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) class represents a type of software element that must exist in the environment.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-688">**\_СОФТВАРЕФЕАТУРЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-688">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> <dd>

<span data-ttu-id="ec3c4-689">Класс [**CIM \_ софтварефеатуре**](cim-softwarefeature.md) представляет определенную функцию или возможность продукта или системы приложений.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-689">The [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class represents a particular function or capability of a product or application system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-690">**\_СОФТВАРЕФЕАТУРЕСАПИМПЛЕМЕНТАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-690">**CIM\_SoftwareFeatureSAPImplementation**</span></span>](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

<span data-ttu-id="ec3c4-691">Класс [**CIM \_ софтварефеатуресапимплементатион**](cim-softwarefeaturesapimplementation.md) представляет связь между точкой доступа к службе (SAP) и ее реализацией в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-691">The [**CIM\_SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-692">**\_СОФТВАРЕФЕАТУРЕСЕРВИЦЕИМПЛЕМЕНТАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-692">**CIM\_SoftwareFeatureServiceImplementation**</span></span>](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="ec3c4-693">Класс [**CIM \_ софтварефеатуресервицеимплементатион**](cim-softwarefeatureserviceimplementation.md) представляет ассоциацию между службой и ее реализацией в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-693">The [**CIM\_SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) class represents an association between a service and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-694">**\_СОФТВАРЕФЕАТУРЕСОФТВАРИЛЕМЕНТС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-694">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

<span data-ttu-id="ec3c4-695">Ассоциация [**\_ софтварефеатуресофтварилементс CIM**](cim-softwarefeaturesoftwareelements.md) определяет программные элементы, составляющие определенную функцию программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-695">The [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) association identifies the software elements that make up a specific software feature.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-696">**\_СПАРЕГРАУП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-696">**CIM\_SpareGroup**</span></span>](cim-sparegroup.md)
</dt> <dd>

<span data-ttu-id="ec3c4-697">Класс [**CIM \_ спареграуп**](cim-sparegroup.md) является производным от класса [**CIM \_ редунданциграуп**](cim-redundancygroup.md) и указывает, что один или несколько агрегированных элементов могут быть запасными.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-697">The [**CIM\_SpareGroup**](cim-sparegroup.md) class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-698">**\_СТАТИСТИКАЛИНФОРМАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-698">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dd>

<span data-ttu-id="ec3c4-699">Класс [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md) является корневым классом для произвольной коллекции статистических данных или метрик, применимых к одному или нескольким управляемым системным элементам.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-699">The [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-700">**\_Статистика CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-700">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> <dd>

<span data-ttu-id="ec3c4-701">Класс [**\_ статистики CIM**](cim-statistics.md) представляет ассоциацию, которая связывает управляемые системные элементы с применяемыми к ним статистическими группами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-701">The [**CIM\_Statistics**](cim-statistics.md) class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-702">**\_СТОРАЖЕДЕФЕКТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-702">**CIM\_StorageDefect**</span></span>](cim-storagedefect.md)
</dt> <dd>

<span data-ttu-id="ec3c4-703">Агрегат [**\_ сторажедефект CIM**](cim-storagedefect.md) собирает ошибки хранилища для экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-703">The [**CIM\_StorageDefect**](cim-storagedefect.md) aggregation collects the storage errors for a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-704">**\_СТОРАЖЕЕРРОР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-704">**CIM\_StorageError**</span></span>](cim-storageerror.md)
</dt> <dd>

<span data-ttu-id="ec3c4-705">Класс [**CIM \_ сторажееррор**](cim-storageerror.md) представляет блоки мультимедиа или пространства памяти, которые сопоставлены неиспользуемыми из-за ошибок.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-705">The [**CIM\_StorageError**](cim-storageerror.md) class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="ec3c4-706">Ключ класса является свойством **стартингаддресс** объекта Bytes in Error.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-706">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-707">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-707">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-708">Класс [**CIM \_ сторажеекстент**](cim-storageextent.md) представляет возможности и управление различными носителями, которые существуют для хранения данных и позволяют получать данные.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-708">The [**CIM\_StorageExtent**](cim-storageextent.md) class represents the capabilities and management of the various media that exist to store data and allow data retrieval.</span></span> <span data-ttu-id="ec3c4-709">Этот родительский класс может представлять различные компоненты RAID (оборудование или программное обеспечение) или необработанную логическую область поверх физических носителей.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-709">This parent class can represent the various components of RAID (hardware or software) or a raw logical extent on top of physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-710">**\_СТОРАЖЕРЕДУНДАНЦИГРАУП CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-710">**CIM\_StorageRedundancyGroup**</span></span>](cim-storageredundancygroup.md)
</dt> <dd>

<span data-ttu-id="ec3c4-711">Класс [**CIM \_ сторажередунданциграуп**](cim-storageredundancygroup.md) представляет сведения о избыточности, связанные с запоминающими устройствами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-711">The [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class represents mass storage-related redundancy information.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-712">**\_СУППОРТАКЦЕСС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-712">**CIM\_SupportAccess**</span></span>](cim-supportaccess.md)
</dt> <dd>

<span data-ttu-id="ec3c4-713">Класс [**CIM \_ суппортакцесс**](cim-supportaccess.md) определяет, как получить помощь для продукта.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-713">The [**CIM\_SupportAccess**](cim-supportaccess.md) class defines how to obtain assistance for a product.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-714">**\_СВАПСПАЦЕЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-714">**CIM\_SwapSpaceCheck**</span></span>](cim-swapspacecheck.md)
</dt> <dd>

<span data-ttu-id="ec3c4-715">Класс [**CIM \_ свапспацечекк**](cim-swapspacecheck.md) определяет объем пространства подкачки, который должен быть доступен в системе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-715">The [**CIM\_SwapSpaceCheck**](cim-swapspacecheck.md) class specifies the amount of swap space that must be available on the system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-716">**\_Система CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-716">**CIM\_System**</span></span>](cim-system.md)
</dt> <dd>

<span data-ttu-id="ec3c4-717">Класс [**\_ системы CIM**](cim-system.md) выполняет статистическую обработку перечислимого набора управляемых системных элементов.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-717">The [**CIM\_System**](cim-system.md) class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="ec3c4-718">Статистическая обработка работает как единое функциональное целое.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-718">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="ec3c4-719">В любом конкретном подклассе системы имеется четко определенный список управляемых классов системных элементов, экземпляры которых должны быть агрегированы.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-719">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-720">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-720">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dd>

<span data-ttu-id="ec3c4-721">класс ассоциации модель CIM (CIM), устанавливающий связи между системой и управляемыми системными элементами, из которых она состоит.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-721">a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-722">**\_СИСТЕМДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-722">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-723">Ассоциация [**CIM \_ системдевице**](cim-systemdevice.md) представляет собой явную связь, в которой логические устройства могут быть агрегированы системой.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-723">The [**CIM\_SystemDevice**](cim-systemdevice.md) association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-724">**\_СИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-724">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dd>

<span data-ttu-id="ec3c4-725">Класс [**CIM \_ системресаурце**](cim-systemresource.md) представляет сущность, управляемую BIOS, или операционную систему, доступную для использования программным обеспечением и логическими устройствами.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-725">The [**CIM\_SystemResource**](cim-systemresource.md) class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-726">**CIM \_ тахометра**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-726">**CIM\_Tachometer**</span></span>](cim-tachometer.md)
</dt> <dd>

<span data-ttu-id="ec3c4-727">Класс [**\_ тахометра CIM**](cim-tachometer.md) существует для обратной совместимости с более ранними определениями схемы CIM.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-727">The [**CIM\_Tachometer**](cim-tachometer.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-728">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-728">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dd>

<span data-ttu-id="ec3c4-729">Класс [**CIM \_ TapeDrive**](cim-tapedrive.md) представляет ленточный накопитель в системе.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-729">The [**CIM\_TapeDrive**](cim-tapedrive.md) class represents a tape drive on the system.</span></span> <span data-ttu-id="ec3c4-730">Ленточные накопители в основном различаются тем, что доступ к ним можно получить только последовательно.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-730">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-731">**\_Датчик температуры CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-731">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-732">Класс [**CIM \_ датчик температуры**](cim-temperaturesensor.md) существует для обеспечения обратной совместимости с более ранними определениями схемы CIM.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-732">The [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-733">**\_Поток CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-733">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dd>

<span data-ttu-id="ec3c4-734">Класс [**\_ потока CIM**](cim-thread.md) представляет возможность выполнения единиц процесса или задачи в параллельном режиме.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-734">The [**CIM\_Thread**](cim-thread.md) class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="ec3c4-735">Процесс может иметь много потоков, каждый из которых является ненадежным для процесса.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-735">A process can have many threads, each of which is weak to the process.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-736">**\_ТОДИРЕКТОРЯКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-736">**CIM\_ToDirectoryAction**</span></span>](cim-todirectoryaction.md)
</dt> <dd>

<span data-ttu-id="ec3c4-737">Ассоциация [**\_ тодиректоряктион CIM**](cim-todirectoryaction.md) определяет целевой каталог для действия с файлом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-737">The [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-738">**\_ТОДИРЕКТОРИСПЕЦИФИКАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-738">**CIM\_ToDirectorySpecification**</span></span>](cim-todirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="ec3c4-739">Ассоциация [**\_ тодиректориспеЦификатион CIM**](cim-todirectoryspecification.md) определяет целевой каталог для действия с файлом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-739">The [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-740">**\_УНИНТЕРРУПТИБЛЕПОВЕРСУППЛИ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-740">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> <dd>

<span data-ttu-id="ec3c4-741">Класс [**CIM \_ унинтерруптиблеповерсуппли**](cim-uninterruptiblepowersupply.md) представляет возможности и управление источником бесперебойного питания (ИБП).</span><span class="sxs-lookup"><span data-stu-id="ec3c4-741">The [**CIM\_UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-742">**\_УНИТАРИКОМПУТЕРСИСТЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-742">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dd>

<span data-ttu-id="ec3c4-743">Класс [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md) представляет Настольный, мобильный, сетевой компьютер, сервер или другой тип одноузловой системы с одним узлом.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-743">The [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-744">**\_УСБКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-744">**CIM\_USBController**</span></span>](cim-usbcontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-745">Класс [**CIM \_ усбконтроллер**](cim-usbcontroller.md) представляет возможности и Управление контроллером USB.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-745">The [**CIM\_USBController**](cim-usbcontroller.md) class represents the capabilities and management of a USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-746">**\_УСБКОНТРОЛЛЕРХАШУБ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-746">**CIM\_USBControllerHasHub**</span></span>](cim-usbcontrollerhashub.md)
</dt> <dd>

<span data-ttu-id="ec3c4-747">Класс [**CIM \_ усбконтроллерхашуб**](cim-usbcontrollerhashub.md) определяет концентраторы, расположенные на контроллере USB.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-747">The [**CIM\_USBControllerHasHub**](cim-usbcontrollerhashub.md) class defines the hubs that are downstream of the USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-748">**\_УСБДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-748">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-749">Класс [**CIM \_ усбдевице**](cim-usbdevice.md) представляет характеристики управления USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-749">The [**CIM\_USBDevice**](cim-usbdevice.md) class represents the management characteristics of a USB device.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-750">**\_УСБХУБ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-750">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> <dd>

<span data-ttu-id="ec3c4-751">Класс [**CIM \_ усбхуб**](cim-usbhub.md) представляет возможности и управление USB-концентратором.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-751">The [**CIM\_USBHub**](cim-usbhub.md) class represents the capabilities and management of a USB hub.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-752">**\_УСЕРДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-752">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dd>

<span data-ttu-id="ec3c4-753">Класс [**CIM \_ усердевице**](cim-userdevice.md) является родительским классом, от которого другие классы, такие как [**CIM- \_ Клавиатура**](cim-keyboard.md) или [**CIM \_ десктопмонитор**](cim-desktopmonitor.md), по убыванию.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-753">The [**CIM\_UserDevice**](cim-userdevice.md) class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="ec3c4-754">Устройства пользователей — это логические устройства, позволяющие пользователю компьютерной системы вводить, просматривать или слышать данные.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-754">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-755">**\_ВЕРСИОНКОМПАТИБИЛИТИЧЕКК CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-755">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> <dd>

<span data-ttu-id="ec3c4-756">Класс [**CIM \_ версионкомпатибилитичекк**](cim-versioncompatibilitycheck.md) указывает, разрешено ли создание следующего состояния программного элемента.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-756">The [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class specifies whether it is permissible to create the next state of a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-757">**\_ВИДЕОБИОСЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-757">**CIM\_VideoBIOSElement**</span></span>](cim-videobioselement.md)
</dt> <dd>

<span data-ttu-id="ec3c4-758">Класс [**CIM \_ видеобиоселемент**](cim-videobioselement.md) представляет программное обеспечение низкого уровня, которое загружается в долговременное хранилище и используется для настройки и доступа к видеоконтроллеру и экрану системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-758">The [**CIM\_VideoBIOSElement**](cim-videobioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-759">**\_ВИДЕОБИОСФЕАТУРЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-759">**CIM\_VideoBIOSFeature**</span></span>](cim-videobiosfeature.md)
</dt> <dd>

<span data-ttu-id="ec3c4-760">Класс [**CIM \_ видеобиосфеатуре**](cim-videobiosfeature.md) представляет возможности низкоуровневого программного обеспечения, используемого для настройки и доступа к видеоконтроллеру и экрану системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-760">The [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-761">**\_ВИДЕОБИОСФЕАТУРЕВИДЕОБИОСЕЛЕМЕНТС CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-761">**CIM\_VideoBIOSFeatureVideoBIOSElements**</span></span>](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

<span data-ttu-id="ec3c4-762">Класс [**CIM \_ видеобиосфеатуревидеобиоселементс**](cim-videobiosfeaturevideobioselements.md) связывает компонент Video BIOS и его объединенные элементы Video BIOS.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-762">The [**CIM\_VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-763">**\_ВИДЕОКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-763">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> <dd>

<span data-ttu-id="ec3c4-764">Класс [**CIM \_ Видеоконтроллер**](cim-videocontroller.md) представляет возможности и управление видеоконтроллером.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-764">The [**CIM\_VideoController**](cim-videocontroller.md) class represents the capabilities and management of the video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-765">**\_ВИДЕОКОНТРОЛЛЕРРЕСОЛУТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-765">**CIM\_VideoControllerResolution**</span></span>](cim-videocontrollerresolution.md)
</dt> <dd>

<span data-ttu-id="ec3c4-766">Класс [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) представляет различные видеорежимы, которые может поддерживать контроллер видео.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-766">The [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class represents the various video modes that a video controller can support.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-767">**\_ВИДЕОСЕТТИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-767">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dd>

<span data-ttu-id="ec3c4-768">Класс [**CIM \_ видеосеттинг**](cim-videosetting.md) связывает объект параметра [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) с контроллером, к которому он применяется.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-768">The [**CIM\_VideoSetting**](cim-videosetting.md) class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-769">**\_ВОЛАТИЛЕСТОРАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-769">**CIM\_VolatileStorage**</span></span>](cim-volatilestorage.md)
</dt> <dd>

<span data-ttu-id="ec3c4-770">Класс [**CIM \_ волатилестораже**](cim-volatilestorage.md) представляет возможности и управление энергозависимым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-770">The [**CIM\_VolatileStorage**](cim-volatilestorage.md) class represents the capabilities and management of volatile storage.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-771">**\_Датчик напряжения CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-771">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dd>

<span data-ttu-id="ec3c4-772">Класс [**CIM \_ датчик напряжения**](cim-voltagesensor.md) существует для обеспечения обратной совместимости с более ранними определениями схемы CIM.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-772">The [**CIM\_VoltageSensor**](cim-voltagesensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="ec3c4-773">Благодаря дополнениям к классам [**\_ датчиков CIM**](cim-sensor.md) и [**модели cim \_ NumericSensor**](cim-numericsensor.md) в версии 2,2 больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-773">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-774">**\_Том CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-774">**CIM\_VolumeSet**</span></span>](cim-volumeset.md)
</dt> <dd>

<span data-ttu-id="ec3c4-775">Класс [**набора \_ томов CIM**](cim-volumeset.md) представляет непрерывный диапазон логических блоков, представленных в операционной среде для чтения и записи пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-775">The [**CIM\_VolumeSet**](cim-volumeset.md) class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span>

</dd> <dt>

[<span data-ttu-id="ec3c4-776">**\_ВОРМДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ec3c4-776">**CIM\_WORMDrive**</span></span>](cim-wormdrive.md)
</dt> <dd>

<span data-ttu-id="ec3c4-777">Класс [**CIM \_ вормдриве**](cim-wormdrive.md) представляет возможности и управление НАКОПИТЕЛем-червем, подтипом устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="ec3c4-777">The [**CIM\_WORMDrive**](cim-wormdrive.md) class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

</dd> </dl>

 

 
