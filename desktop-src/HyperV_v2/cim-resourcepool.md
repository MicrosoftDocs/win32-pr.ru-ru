---
description: Представляет пул ресурсов, который является логической сущностью, предоставляемой хост-системой для выделения и назначения ресурсов.
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: Класс CIM_ResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11a073f817da27dbbd45be26a008486a776470cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154539"
---
# <a name="cim_resourcepool-class"></a><span data-ttu-id="bb4d5-103">\_Класс CIM ResourcePool</span><span class="sxs-lookup"><span data-stu-id="bb4d5-103">CIM\_ResourcePool class</span></span>

<span data-ttu-id="bb4d5-104">Представляет пул ресурсов, который является логической сущностью, предоставляемой хост-системой для выделения и назначения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-104">Represents a resource pool, which is a logical entity provided by the host system to allocate and assign resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb4d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb4d5-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="bb4d5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="bb4d5-106">Members</span></span>

<span data-ttu-id="bb4d5-107">Класс **CIM \_ ResourcePool** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bb4d5-107">The **CIM\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="bb4d5-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb4d5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb4d5-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb4d5-109">Properties</span></span>

<span data-ttu-id="bb4d5-110">Класс **CIM \_ ResourcePool** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-110">The **CIM\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb4d5-111">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-111">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-114">Квалификаторы: **испунит**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-114">Qualifiers: **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-115">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="bb4d5-115">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="bb4d5-116">Например, если для **ResourceType** задано значение "процессор", **аллокатионунитс** может иметь значение "Герц \* 10 ^ 6" или "Percent".</span><span class="sxs-lookup"><span data-stu-id="bb4d5-116">For example, when **ResourceType** is set to "Processor", **AllocationUnits** may be set to "hertz\*10^6" or "percent".</span></span> <span data-ttu-id="bb4d5-117">Значение этого свойства должно быть допустимым значением квалификатора программных единиц из приложения C. 1 *DSP0004 v 2.4* или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-117">The value of this property should be a legal value of the Programmatic Units qualifier from Appendix C.1 of *DSP0004 V2.4* or later.</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-118">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-118">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-119">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-121">Максимальное количество резервирований, которое может поддерживать пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-121">The maximum amount of reservations that the resource pool can support.</span></span> <span data-ttu-id="bb4d5-122">Свойство **аллокатионунитс** указывает тип единицы.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-122">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-123">**консумедресаурцеунитс**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-123">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-126">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**Максконсумаблересаурце**","**CIM \_ ResourcePool**.**Куррентликонсумедресаурце**"), **испунит**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-126">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**MaxConsumableResource**", "**CIM\_ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-127">Единицы измерения для **максконсумабле** и **использованных** свойств.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-127">The units for the **MaxConsumable** and the **Consumed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-128">**куррентликонсумедресаурце**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-128">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-129">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-131">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**Консумедресаурцеунитс**")</span><span class="sxs-lookup"><span data-stu-id="bb4d5-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-132">Объем ресурса, который в настоящее время представлен пулом ресурсов для потребителей ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-132">The amount of resource that the resource pool currently presents to resource consumers.</span></span> <span data-ttu-id="bb4d5-133">Это свойство отличается от **зарезервированного** свойства, так как оно описывает представление объекта "потребители" ресурса, а **зарезервированное** свойство описывает представление "производители" ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-133">This property is different from the **Reserved** property because it describes the consumers view of the resource while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-137">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="bb4d5-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-138">Уникально идентифицирует экземпляр этого класса в области содержащего его пространства имен.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-138">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="bb4d5-139">Чтобы обеспечить уникальность в пространстве имен, значение свойства **InstanceId** должно быть создано в следующем шаблоне: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="bb4d5-139">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="bb4d5-140">*OrgID* должен включать уникальное имя, присвоенное товару или иным способом, которое принадлежит бизнес-сущности, определяющей свойство **InstanceId** , или быть зарегистрированным идентификатором, назначенным распознанным глобальным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-140">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="bb4d5-141">*OrgID* не должно содержать двоеточие.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-141">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="bb4d5-142">Первое двоеточие в **InstanceId** должно находиться между *OrgID* и *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-142">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="bb4d5-143">*LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых реальных элементов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-143">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="bb4d5-144">Если приведенный выше шаблон не используется, определяющая сущность должна гарантировать, что результирующее значение **InstanceId** не будет повторно использоваться во всех свойствах **InstanceId** , созданных этим поставщиком или другими поставщиками для этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-144">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="bb4d5-145">Для экземпляров, определенных DMTF, шаблон должен использоваться с *OrgID* , для которого задано значение "CIM".</span><span class="sxs-lookup"><span data-stu-id="bb4d5-145">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> <dt>

<span data-ttu-id="bb4d5-146">**максконсумаблересаурце**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-146">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-147">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-149">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**Консумедресаурцеунитс**")</span><span class="sxs-lookup"><span data-stu-id="bb4d5-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-150">Максимальное количество потребляемых ресурсов, которые пул ресурсов может предоставить потребителям ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-150">The maximum of amount of consumable resources that the resource pool can present to resource consumers.</span></span> <span data-ttu-id="bb4d5-151">Это свойство отличается от свойства **Capacity** , так как оно описывает представление объекта "потребители" для ресурса, а свойство **Capacity** описывает представление "производители" ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-151">This property is different from the **Capacity** property because it describes the consumers view of the resource while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-152">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-152">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-155">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="bb4d5-155">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-156">Тип ресурса, если свойство **ResourceType** имеет значение "0" (другое).</span><span class="sxs-lookup"><span data-stu-id="bb4d5-156">The resource type when the **ResourceType** property is set to "0" (other).</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-157">**пулид**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-157">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-160">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md).**Пулид**")</span><span class="sxs-lookup"><span data-stu-id="bb4d5-160">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-161">Непрозрачный идентификатор пула.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-161">An opaque identifier for the pool.</span></span> <span data-ttu-id="bb4d5-162">Это свойство используется для обеспечения корреляции при сохранении и восстановлении данных конфигурации в базовом постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-162">This property is used to provide correlation when saving and restoring configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-163">**Исходный пул**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-163">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-164">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-166">**значение true** , если пул ресурсов является первичным.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-166">**true** if the resource pool is primordial.</span></span> <span data-ttu-id="bb4d5-167">**значение false** , если пул ресурсов является конкретным пулом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-167">**false** if the resource pool is a concrete resource pool.</span></span> <span data-ttu-id="bb4d5-168">Исходный пул ресурсов — это пул ресурсов, который не создается и не удаляется потребителями ресурса.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-168">A primordial resource pool is a resource pool that is not created or deleted by consumers of the resource.</span></span> <span data-ttu-id="bb4d5-169">Конкретный пул ресурсов может быть обновлен службами выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-169">A concrete resource pool can be updated by resource allocation services.</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-170">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-170">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-171">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-173">Текущее количество резервирований, распределенное по всем активным выделениям из этого пула.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-173">The current number of reservations spread across all active allocations from this pool.</span></span> <span data-ttu-id="bb4d5-174">В иерархической конфигурации это представляет сумму всех текущих резервирований потомков.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-174">In a hierarchical configuration, this represents the sum of all current descendant reservations.</span></span> <span data-ttu-id="bb4d5-175">Свойство **аллокатионунитс** указывает тип единицы.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-175">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-179">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="bb4d5-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-180">Конкретный подтип реализации для пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-180">The implementation specific sub-type for the resource pool.</span></span> <span data-ttu-id="bb4d5-181">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-181">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="bb4d5-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb4d5-183">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb4d5-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb4d5-185">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**Осерресаурцетипе**","**CIM \_ ResourcePool**.**Ресаурцесубтипе**")</span><span class="sxs-lookup"><span data-stu-id="bb4d5-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**OtherResourceType**", "**CIM\_ResourcePool**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="bb4d5-186">Тип ресурса, выделенного пулом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb4d5-186">The type of resource allocated by the resource pool.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb4d5-187">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-187">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="bb4d5-188">**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-188">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="bb4d5-189">**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-189">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="bb4d5-190">**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-190">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="bb4d5-191">**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-191">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="bb4d5-192">**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-192">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="bb4d5-193">**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-193">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="bb4d5-194">**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-194">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="bb4d5-195">**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-195">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="bb4d5-196">**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-196">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="bb4d5-197">**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-197">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="bb4d5-198">**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-198">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="bb4d5-199">**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-199">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="bb4d5-200">Дисковод **гибких дисков** (14)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-200">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="bb4d5-201">**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-201">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="bb4d5-202">**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-202">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="bb4d5-203">**Диск** (17)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-203">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="bb4d5-204">**Ленточный накопитель** (18)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-204">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="bb4d5-205">**Область хранения** (19)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-205">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="bb4d5-206">**Другое запоминающее устройство** (20)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-206">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="bb4d5-207">**Последовательный порт** (21)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-207">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="bb4d5-208">**Параллельный порт** (22)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-208">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="bb4d5-209">**Контроллер USB** (23)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-209">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="bb4d5-210">**Графический контроллер** (24)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-210">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="bb4d5-211">**Контроллер IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-211">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="bb4d5-212">**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-212">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="bb4d5-213">**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-213">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="bb4d5-214">**Мощность** (28)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-214">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="bb4d5-215">**Емкость системы охлаждения** (29)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-215">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="bb4d5-216">**Порт коммутатора Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-216">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="bb4d5-217">**Логический диск** (31)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-217">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="bb4d5-218">**Том хранилища** (32)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-218">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="bb4d5-219">**Ethernet-подключение** (33)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-219">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="bb4d5-220">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="bb4d5-220">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="bb4d5-221">**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="bb4d5-221">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="bb4d5-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bb4d5-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bb4d5-223">Требования</span><span class="sxs-lookup"><span data-stu-id="bb4d5-223">Requirements</span></span>



| <span data-ttu-id="bb4d5-224">Требование</span><span class="sxs-lookup"><span data-stu-id="bb4d5-224">Requirement</span></span> | <span data-ttu-id="bb4d5-225">Значение</span><span class="sxs-lookup"><span data-stu-id="bb4d5-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb4d5-226">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb4d5-226">Minimum supported client</span></span><br/> | <span data-ttu-id="bb4d5-227">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bb4d5-227">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bb4d5-228">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb4d5-228">Minimum supported server</span></span><br/> | <span data-ttu-id="bb4d5-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb4d5-229">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bb4d5-230">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb4d5-230">Namespace</span></span><br/>                | <span data-ttu-id="bb4d5-231">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="bb4d5-231">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bb4d5-232">MOF</span><span class="sxs-lookup"><span data-stu-id="bb4d5-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb4d5-233"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb4d5-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb4d5-234">DLL</span><span class="sxs-lookup"><span data-stu-id="bb4d5-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb4d5-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb4d5-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb4d5-236">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb4d5-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb4d5-237">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="bb4d5-237">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

