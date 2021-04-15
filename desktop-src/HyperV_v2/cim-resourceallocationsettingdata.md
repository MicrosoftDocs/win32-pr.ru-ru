---
description: Представляет параметры для выделенного ресурса, которые выходят за пределы области класса CIM, обычно используемые для представления самого ресурса.
ms.assetid: 6261bab9-aa51-479e-bd6a-43c4a9b294a6
title: Класс CIM_ResourceAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationSettingData
- CIM_ResourceAllocationSettingData.ResourceType
- CIM_ResourceAllocationSettingData.OtherResourceType
- CIM_ResourceAllocationSettingData.ResourceSubType
- CIM_ResourceAllocationSettingData.PoolID
- CIM_ResourceAllocationSettingData.ConsumerVisibility
- CIM_ResourceAllocationSettingData.HostResource
- CIM_ResourceAllocationSettingData.AllocationUnits
- CIM_ResourceAllocationSettingData.VirtualQuantity
- CIM_ResourceAllocationSettingData.Reservation
- CIM_ResourceAllocationSettingData.Limit
- CIM_ResourceAllocationSettingData.Weight
- CIM_ResourceAllocationSettingData.AutomaticAllocation
- CIM_ResourceAllocationSettingData.AutomaticDeallocation
- CIM_ResourceAllocationSettingData.Parent
- CIM_ResourceAllocationSettingData.Connection
- CIM_ResourceAllocationSettingData.Address
- CIM_ResourceAllocationSettingData.MappingBehavior
- CIM_ResourceAllocationSettingData.AddressOnParent
- CIM_ResourceAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22289511f454e0d3b128d0e73d32687924c7a7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683430"
---
# <a name="cim_resourceallocationsettingdata-class"></a><span data-ttu-id="1530c-103">\_Класс CIM ресаурцеаллокатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="1530c-103">CIM\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="1530c-104">Представляет параметры для выделенного ресурса, которые выходят за пределы области класса CIM, обычно используемые для представления самого ресурса.</span><span class="sxs-lookup"><span data-stu-id="1530c-104">Represents settings for an allocated resource that are outside the scope of the CIM class typically used to represent the resource itself.</span></span> <span data-ttu-id="1530c-105">Эти параметры включают сведения, относящиеся к выделению, которые могут быть не видны потребителю ресурса.</span><span class="sxs-lookup"><span data-stu-id="1530c-105">These settings include information specific to the allocation that may not be visible to the consumer of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="1530c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1530c-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourceAllocationSettingData : CIM_SettingData
{
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
};
```

## <a name="members"></a><span data-ttu-id="1530c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1530c-107">Members</span></span>

<span data-ttu-id="1530c-108">Класс **CIM \_ ресаурцеаллокатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1530c-108">The **CIM\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1530c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="1530c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1530c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="1530c-110">Properties</span></span>

<span data-ttu-id="1530c-111">Класс **CIM \_ ресаурцеаллокатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1530c-111">The **CIM\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1530c-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="1530c-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1530c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1530c-115">Адрес ресурса, например MAC-адрес порта Ethernet.</span><span class="sxs-lookup"><span data-stu-id="1530c-115">The address of the resource, for example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-116">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="1530c-116">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1530c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1530c-119">Адрес этого ресурса из контекста родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="1530c-119">The address of this resource from the context of the parent.</span></span> <span data-ttu-id="1530c-120">Это свойство используется для описания отношения контроллера и порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="1530c-120">This property is used to describe a controller relationship and the ordering of devices on a controller.</span></span> <span data-ttu-id="1530c-121">Например, если родительским объектом является контроллер PCI, в этом свойстве будет указан слот PCI этого дочернего устройства.</span><span class="sxs-lookup"><span data-stu-id="1530c-121">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-122">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="1530c-122">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1530c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-125">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ресаурцеаллокатионсеттингдата**.**Резервирование**","**CIM \_ ресаурцеаллокатионсеттингдата**.**Limit**"), **испунит**</span><span class="sxs-lookup"><span data-stu-id="1530c-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**Reservation**", "**CIM\_ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="1530c-126">Единицы распределения, используемые свойствами " **резервирование** " и " **ограничение** ".</span><span class="sxs-lookup"><span data-stu-id="1530c-126">The allocation units used by the **Reservation** and **Limit** properties.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-127">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="1530c-127">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1530c-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1530c-130">**значение true** , чтобы автоматически выделить ресурс; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1530c-130">**true** to automatically allocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-131">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="1530c-131">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-132">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1530c-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1530c-134">**значение true** , чтобы автоматически освободить ресурс; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1530c-134">**true** to automatically deallocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-135">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="1530c-135">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-136">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1530c-136">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1530c-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1530c-138">Массив, указывающий объекты, подключенные к ресурсу, такие как именованная сеть или порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="1530c-138">An array that indicates the objects connected to the resource, such as a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-139">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="1530c-139">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1530c-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1530c-142">Пользователи могут видеть выделенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="1530c-142">The consumers visibility to the allocated resource.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1530c-143">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1530c-143">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>

<span data-ttu-id="1530c-144">**Пройдено** (2)</span><span class="sxs-lookup"><span data-stu-id="1530c-144">**Passed-Through** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>

<span data-ttu-id="1530c-145">**Виртуализированный** (3)</span><span class="sxs-lookup"><span data-stu-id="1530c-145">**Virtualized** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>

<span data-ttu-id="1530c-146">**Не представлено** (4)</span><span class="sxs-lookup"><span data-stu-id="1530c-146">**Not represented** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1530c-147">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1530c-147">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1530c-148">**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1530c-148">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1530c-149">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="1530c-149">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-150">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="1530c-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1530c-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-152">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ресаурцеаллокатионсеттингдата**.**Консумервисибилити**","**CIM \_ ресаурцеаллокатионсеттингдата**.**Маппингбехавиор**")</span><span class="sxs-lookup"><span data-stu-id="1530c-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ConsumerVisibility**", "**CIM\_ResourceAllocationSettingData**.**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="1530c-153">Массив, содержащий назначение выделенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1530c-153">An array that contains the assignment of the allocated resources.</span></span> <span data-ttu-id="1530c-154">Каждое значение этого свойства, отличное от NULL, должно быть отформатировано как универсальный код ресурса (URI) на основе RFC3986.</span><span class="sxs-lookup"><span data-stu-id="1530c-154">Each non-null value of this property must be formated as an RFC3986 based URI.</span></span> <span data-ttu-id="1530c-155">Если ресурс моделируется, значение должно быть URI WBEM.</span><span class="sxs-lookup"><span data-stu-id="1530c-155">If the resource is modeled, then the value should be a WBEM URI.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-156">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="1530c-156">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-157">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1530c-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-159">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ресаурцеаллокатионсеттингдата**.**Аллокатионунитс**")</span><span class="sxs-lookup"><span data-stu-id="1530c-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="1530c-160">Максимальный объем ресурса, который необходимо предоставить выделению.</span><span class="sxs-lookup"><span data-stu-id="1530c-160">The maximum amount of resource to grant to the allocation.</span></span> <span data-ttu-id="1530c-161">Тип единицы этого свойства задается свойством **аллокатионунитс** .</span><span class="sxs-lookup"><span data-stu-id="1530c-161">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-162">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="1530c-162">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1530c-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1530c-165">Указывает, как ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="1530c-165">Indicates how the resource maps to underlying resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1530c-166">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1530c-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1530c-167">**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="1530c-167">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="1530c-168">**Выделенный** (3)</span><span class="sxs-lookup"><span data-stu-id="1530c-168">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="1530c-169">**Мягкое сходство** (4)</span><span class="sxs-lookup"><span data-stu-id="1530c-169">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="1530c-170">**Жесткое сходство** (5)</span><span class="sxs-lookup"><span data-stu-id="1530c-170">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1530c-171">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1530c-171">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1530c-172">**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1530c-172">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1530c-173">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="1530c-173">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1530c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-176">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ресаурцеаллокатионсеттингдата**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="1530c-176">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="1530c-177">Описание типа ресурса, если свойство **ResourceType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="1530c-177">A description of the resource type when the **ResourceType** property is set to 1 (other).</span></span>

</dd> <dt>

<span data-ttu-id="1530c-178">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="1530c-178">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1530c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1530c-181">Родительский объект ресурса, например контроллер для текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="1530c-181">The parent of the resource, for example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-182">**пулид**</span><span class="sxs-lookup"><span data-stu-id="1530c-182">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1530c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-185">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**Пулид**")</span><span class="sxs-lookup"><span data-stu-id="1530c-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="1530c-186">Идентификатор пула ресурсов, создавшего ресурс.</span><span class="sxs-lookup"><span data-stu-id="1530c-186">The ID of the resource pool that generated the resource.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-187">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="1530c-187">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-188">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1530c-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-190">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ресаурцеаллокатионсеттингдата**.**Аллокатионунитс**")</span><span class="sxs-lookup"><span data-stu-id="1530c-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="1530c-191">Число ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="1530c-191">The number of resource that are guaranteed to be available for this allocation.</span></span> <span data-ttu-id="1530c-192">В системах, поддерживающих чрезмерное использование ресурсов, это значение обычно используется для управления доступом.</span><span class="sxs-lookup"><span data-stu-id="1530c-192">On systems that support over-commitment of resources, this value is typically used for admission control.</span></span>

<span data-ttu-id="1530c-193">Тип единицы этого свойства задается свойством **аллокатионунитс** .</span><span class="sxs-lookup"><span data-stu-id="1530c-193">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-194">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="1530c-194">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1530c-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-197">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ресаурцеаллокатионсеттингдата**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="1530c-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="1530c-198">Конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="1530c-198">An implementation specific sub-type for this resource.</span></span> <span data-ttu-id="1530c-199">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1530c-199">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-200">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="1530c-200">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-201">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1530c-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-203">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ресаурцеаллокатионсеттингдата**.**Осерресаурцетипе**","**CIM \_ ресаурцеаллокатионсеттингдата**.**Ресаурцесубтипе**")</span><span class="sxs-lookup"><span data-stu-id="1530c-203">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**OtherResourceType**", "**CIM\_ResourceAllocationSettingData**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="1530c-204">Тип ресурса, представленный параметрами выделения.</span><span class="sxs-lookup"><span data-stu-id="1530c-204">The type of resource that is represented by the allocation settings.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1530c-205">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1530c-205">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="1530c-206">**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="1530c-206">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="1530c-207">**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="1530c-207">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="1530c-208">**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="1530c-208">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="1530c-209">**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="1530c-209">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="1530c-210">**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="1530c-210">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="1530c-211">**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="1530c-211">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="1530c-212">**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="1530c-212">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="1530c-213">**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="1530c-213">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="1530c-214">**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="1530c-214">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="1530c-215">**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="1530c-215">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="1530c-216">**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="1530c-216">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="1530c-217">**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="1530c-217">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="1530c-218">Дисковод **гибких дисков** (14)</span><span class="sxs-lookup"><span data-stu-id="1530c-218">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="1530c-219">**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="1530c-219">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="1530c-220">**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="1530c-220">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="1530c-221">**Диск** (17)</span><span class="sxs-lookup"><span data-stu-id="1530c-221">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="1530c-222">**Ленточный накопитель** (18)</span><span class="sxs-lookup"><span data-stu-id="1530c-222">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="1530c-223">**Область хранения** (19)</span><span class="sxs-lookup"><span data-stu-id="1530c-223">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="1530c-224">**Другое запоминающее устройство** (20)</span><span class="sxs-lookup"><span data-stu-id="1530c-224">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="1530c-225">**Последовательный порт** (21)</span><span class="sxs-lookup"><span data-stu-id="1530c-225">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="1530c-226">**Параллельный порт** (22)</span><span class="sxs-lookup"><span data-stu-id="1530c-226">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="1530c-227">**Контроллер USB** (23)</span><span class="sxs-lookup"><span data-stu-id="1530c-227">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="1530c-228">**Графический контроллер** (24)</span><span class="sxs-lookup"><span data-stu-id="1530c-228">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="1530c-229">**Контроллер IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="1530c-229">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="1530c-230">**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="1530c-230">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="1530c-231">**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="1530c-231">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="1530c-232">**Мощность** (28)</span><span class="sxs-lookup"><span data-stu-id="1530c-232">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="1530c-233">**Емкость системы охлаждения** (29)</span><span class="sxs-lookup"><span data-stu-id="1530c-233">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="1530c-234">**Порт коммутатора Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="1530c-234">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="1530c-235">**Логический диск** (31)</span><span class="sxs-lookup"><span data-stu-id="1530c-235">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="1530c-236">**Том хранилища** (32)</span><span class="sxs-lookup"><span data-stu-id="1530c-236">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="1530c-237">**Ethernet-подключение** (33)</span><span class="sxs-lookup"><span data-stu-id="1530c-237">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1530c-238">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1530c-238">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1530c-239">**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="1530c-239">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1530c-240">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="1530c-240">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-241">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1530c-241">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-243">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ресаурцеаллокатионсеттингдата**.**Виртуалкуантитюнитс**")</span><span class="sxs-lookup"><span data-stu-id="1530c-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="1530c-244">Число ресурсов, представленных потребителю ресурса.</span><span class="sxs-lookup"><span data-stu-id="1530c-244">The number of resources presented to the consumer of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-245">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="1530c-245">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1530c-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1530c-248">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ресаурцеаллокатионсеттингдата**.**Виртуалкуантити**"), **испунит**</span><span class="sxs-lookup"><span data-stu-id="1530c-248">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="1530c-249">Единицы, используемые свойством **виртуалкуантити** .</span><span class="sxs-lookup"><span data-stu-id="1530c-249">The units used by the **VirtualQuantity** property.</span></span>

</dd> <dt>

<span data-ttu-id="1530c-250">**Weight**</span><span class="sxs-lookup"><span data-stu-id="1530c-250">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1530c-251">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1530c-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1530c-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1530c-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1530c-253">Относительный приоритет для этого выделения относительно других выделений из того же пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1530c-253">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1530c-254">Требования</span><span class="sxs-lookup"><span data-stu-id="1530c-254">Requirements</span></span>



| <span data-ttu-id="1530c-255">Требование</span><span class="sxs-lookup"><span data-stu-id="1530c-255">Requirement</span></span> | <span data-ttu-id="1530c-256">Значение</span><span class="sxs-lookup"><span data-stu-id="1530c-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1530c-257">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1530c-257">Minimum supported client</span></span><br/> | <span data-ttu-id="1530c-258">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1530c-258">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1530c-259">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1530c-259">Minimum supported server</span></span><br/> | <span data-ttu-id="1530c-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1530c-260">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1530c-261">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1530c-261">Namespace</span></span><br/>                | <span data-ttu-id="1530c-262">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1530c-262">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1530c-263">MOF</span><span class="sxs-lookup"><span data-stu-id="1530c-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1530c-264"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1530c-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1530c-265">DLL</span><span class="sxs-lookup"><span data-stu-id="1530c-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1530c-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1530c-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1530c-267">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1530c-267">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1530c-268">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="1530c-268">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

