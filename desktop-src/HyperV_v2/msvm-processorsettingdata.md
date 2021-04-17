---
description: Представляет параметры виртуального процессора для виртуальной машины.
ms.assetid: 2B299793-E1CD-49D4-898C-AE60B49F44F5
title: Класс Msvm_ProcessorSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorSettingData
- Msvm_ProcessorSettingData.InstanceID
- Msvm_ProcessorSettingData.Caption
- Msvm_ProcessorSettingData.Description
- Msvm_ProcessorSettingData.ElementName
- Msvm_ProcessorSettingData.ResourceType
- Msvm_ProcessorSettingData.OtherResourceType
- Msvm_ProcessorSettingData.ResourceSubType
- Msvm_ProcessorSettingData.PoolID
- Msvm_ProcessorSettingData.ConsumerVisibility
- Msvm_ProcessorSettingData.HostResource
- Msvm_ProcessorSettingData.AllocationUnits
- Msvm_ProcessorSettingData.VirtualQuantity
- Msvm_ProcessorSettingData.Reservation
- Msvm_ProcessorSettingData.Limit
- Msvm_ProcessorSettingData.Weight
- Msvm_ProcessorSettingData.AutomaticAllocation
- Msvm_ProcessorSettingData.AutomaticDeallocation
- Msvm_ProcessorSettingData.Parent
- Msvm_ProcessorSettingData.Connection
- Msvm_ProcessorSettingData.Address
- Msvm_ProcessorSettingData.MappingBehavior
- Msvm_ProcessorSettingData.AddressOnParent
- Msvm_ProcessorSettingData.VirtualQuantityUnits
- Msvm_ProcessorSettingData.LimitCPUID
- Msvm_ProcessorSettingData.HwThreadsPerCore
- Msvm_ProcessorSettingData.LimitProcessorFeatures
- Msvm_ProcessorSettingData.MaxProcessorsPerNumaNode
- Msvm_ProcessorSettingData.MaxNumaNodesPerSocket
- Msvm_ProcessorSettingData.EnableHostResourceProtection
- Msvm_ProcessorSettingData.CpuGroupId
- Msvm_ProcessorSettingData.HideHypervisorPresent
- Msvm_ProcessorSettingData.ExposeVirtualizationExtensions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5154105c4deab13f93bb65078a5c9527283620e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663465"
---
# <a name="msvm_processorsettingdata-class"></a><span data-ttu-id="89c9f-103">\_Класс мсвм процессорсеттингдата</span><span class="sxs-lookup"><span data-stu-id="89c9f-103">Msvm\_ProcessorSettingData class</span></span>

<span data-ttu-id="89c9f-104">Представляет параметры виртуального процессора для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="89c9f-104">Represents the virtual processor settings for a virtual machine.</span></span>

<span data-ttu-id="89c9f-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="89c9f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c9f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89c9f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Processor";
  string  Description = "A logical processor of the hypervisor running on the host computer system.";
  string  ElementName;
  uint16  ResourceType = 3;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Processor";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits = "percent / 1000";
  uint64  VirtualQuantity = "count";
  uint64  Reservation = 0;
  uint64  Limit = 100000;
  uint32  Weight = 100;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  boolean LimitCPUID;
  uint64  HwThreadsPerCore;
  boolean LimitProcessorFeatures;
  uint64  MaxProcessorsPerNumaNode;
  uint64  MaxNumaNodesPerSocket;
  boolean EnableHostResourceProtection;
  string  CpuGroupId;
  boolean HideHypervisorPresent;
  boolean ExposeVirtualizationExtensions;
};
```

## <a name="members"></a><span data-ttu-id="89c9f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="89c9f-107">Members</span></span>

<span data-ttu-id="89c9f-108">Класс **мсвм \_ процессорсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="89c9f-108">The **Msvm\_ProcessorSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="89c9f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="89c9f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89c9f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="89c9f-110">Properties</span></span>

<span data-ttu-id="89c9f-111">Класс **мсвм \_ процессорсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="89c9f-111">The **Msvm\_ProcessorSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89c9f-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="89c9f-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="89c9f-115">The address of the resource.</span></span> <span data-ttu-id="89c9f-116">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-117">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="89c9f-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-120">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="89c9f-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="89c9f-121">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="89c9f-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="89c9f-122">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-123">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="89c9f-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-126">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="89c9f-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="89c9f-127">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-128">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="89c9f-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="89c9f-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-131">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="89c9f-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="89c9f-132">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-133">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="89c9f-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="89c9f-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-136">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="89c9f-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="89c9f-137">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="89c9f-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-141">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="89c9f-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-142">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="89c9f-142">A short description of the object.</span></span> <span data-ttu-id="89c9f-143">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="89c9f-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-144">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="89c9f-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-145">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="89c9f-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-147">Устройство, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="89c9f-147">The device to which this resource is connected.</span></span> <span data-ttu-id="89c9f-148">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-149">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="89c9f-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-150">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89c9f-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-152">Описывает видимость потребителя для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="89c9f-152">Describes the consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="89c9f-153">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-154">**кпуграупид**</span><span class="sxs-lookup"><span data-stu-id="89c9f-154">**CpuGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-157">Идентификатор группы ЦП, к которой привязана эта виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="89c9f-157">The Cpu Group Id this VM is bound to.</span></span> <span data-ttu-id="89c9f-158">Если значение равно 0, это означает, что не привязан к определенной группе ЦП.</span><span class="sxs-lookup"><span data-stu-id="89c9f-158">When value is 0 it means is not bound to a specific CPU group.</span></span>

> [!Note]  
> <span data-ttu-id="89c9f-159">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="89c9f-159">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="89c9f-160">**Описание**</span><span class="sxs-lookup"><span data-stu-id="89c9f-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-163">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="89c9f-163">A description of the object.</span></span> <span data-ttu-id="89c9f-164">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="89c9f-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-165">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="89c9f-165">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-168">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="89c9f-168">A display name for the object.</span></span> <span data-ttu-id="89c9f-169">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="89c9f-169">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="89c9f-170">Изменение этого свойства приведет к изменению **ElementName** связанного логического устройства, производного от.</span><span class="sxs-lookup"><span data-stu-id="89c9f-170">Changing this property will change the **ElementName** of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-171">**енаблехостресаурцепротектион**</span><span class="sxs-lookup"><span data-stu-id="89c9f-171">**EnableHostResourceProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-172">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="89c9f-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-174">Указывает, должна ли виртуальная машина включать функции, повышающие защиту ресурсов узла, от рабочей нагрузки, выполняемой на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="89c9f-174">Indicates whether the VM should enable features that increase the protection of host resources from workload running in the VM.</span></span>

> [!Note]  
> <span data-ttu-id="89c9f-175">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="89c9f-175">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="89c9f-176">**експосевиртуализатионекстенсионс**</span><span class="sxs-lookup"><span data-stu-id="89c9f-176">**ExposeVirtualizationExtensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-177">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="89c9f-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-179">Указывает, следует ли Hyper-V предоставлять виртуальным МАШИНАм аппаратные модули виртуализации.</span><span class="sxs-lookup"><span data-stu-id="89c9f-179">Indicates whether Hyper-V should expose virtualized hardware virtualization extensions to the VM.</span></span>

> [!Note]  
> <span data-ttu-id="89c9f-180">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="89c9f-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="89c9f-181">**хидехипервисорпресент**</span><span class="sxs-lookup"><span data-stu-id="89c9f-181">**HideHypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-182">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="89c9f-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-184">Указывает, должна ли Hyper-V сообщать о наличии гипервизора для вложенного гостя.</span><span class="sxs-lookup"><span data-stu-id="89c9f-184">Indicates whether Hyper-V should report that a hypervisor is present to the nested guest.</span></span>

> [!Note]  
> <span data-ttu-id="89c9f-185">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="89c9f-185">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="89c9f-186">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="89c9f-186">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-187">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="89c9f-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-189">Предоставляет определенное назначение для размещения или базовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89c9f-189">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="89c9f-190">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="89c9f-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-191">**хвсреадсперкоре**</span><span class="sxs-lookup"><span data-stu-id="89c9f-191">**HwThreadsPerCore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-192">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89c9f-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-194">Указывает количество SMT потоков на ядро, сообщаемое гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="89c9f-194">Indicates the number of SMT threads per core reported to the guest.</span></span> <span data-ttu-id="89c9f-195">Эти отчеты не зависят от наличия оборудования для SMT.</span><span class="sxs-lookup"><span data-stu-id="89c9f-195">This reporting is independent of whether the hardware for SMT is present.</span></span>

> [!Note]  
> <span data-ttu-id="89c9f-196">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="89c9f-196">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="89c9f-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="89c9f-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-200">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="89c9f-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-201">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="89c9f-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="89c9f-202">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="89c9f-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-203">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="89c9f-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-204">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89c9f-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-206">Максимальный объем ресурсов ЦП, которые может использовать виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="89c9f-206">The maximum amount of CPU resources that may be consumed by the virtual machine.</span></span> <span data-ttu-id="89c9f-207">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="89c9f-208">100 000</span><span class="sxs-lookup"><span data-stu-id="89c9f-208">100000</span></span>

<span data-ttu-id="89c9f-209">Диапазон: 0 100000</span><span class="sxs-lookup"><span data-stu-id="89c9f-209">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-210">**лимиткпуид**</span><span class="sxs-lookup"><span data-stu-id="89c9f-210">**LimitCPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-211">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="89c9f-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-213">Указывает, должна ли виртуальная машина понизить Идентификатор ЦП.</span><span class="sxs-lookup"><span data-stu-id="89c9f-213">Indicates whether the virtual machine should lower the CPU identifier.</span></span> <span data-ttu-id="89c9f-214">Некоторым старым операционным системам может потребоваться ограничить функциональность процессора таким образом, чтобы их можно было запустить.</span><span class="sxs-lookup"><span data-stu-id="89c9f-214">Some older operating systems may require you to limit processor functionality in this way in order to run.</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-215">**лимитпроцессорфеатурес**</span><span class="sxs-lookup"><span data-stu-id="89c9f-215">**LimitProcessorFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-216">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="89c9f-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-218">Указывает, должна ли виртуальная машина ограничивать функции ЦП, предоставляемые операционной системе.</span><span class="sxs-lookup"><span data-stu-id="89c9f-218">Indicates whether the virtual machine should limit the CPU features exposed to the operating system.</span></span> <span data-ttu-id="89c9f-219">Ограничение функций процессора позволяет выполнять миграцию виртуальной машины на разные компьютеры с разными процессорами.</span><span class="sxs-lookup"><span data-stu-id="89c9f-219">Limiting the processor features enables the virtual machine to be migrated to different host computer systems with different processors.</span></span> <span data-ttu-id="89c9f-220">Миграция виртуальных машин между компьютерами с процессорами разных поставщиков не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="89c9f-220">Migrating virtual machines between computers with processors from different vendors is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-221">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="89c9f-221">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-222">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89c9f-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-224">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="89c9f-224">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="89c9f-225">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-226">**макснуманодесперсоккет**</span><span class="sxs-lookup"><span data-stu-id="89c9f-226">**MaxNumaNodesPerSocket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-227">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89c9f-227">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-229">Максимальное количество узлов NUMA, которые можно наблюдать внутри виртуальной машины, принадлежащих одному сокету процессора.</span><span class="sxs-lookup"><span data-stu-id="89c9f-229">The maximum number of NUMA nodes that can be observed within the virtual machine as belonging to a single processor socket.</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-230">**макспроцессорспернуманоде**</span><span class="sxs-lookup"><span data-stu-id="89c9f-230">**MaxProcessorsPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-231">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89c9f-231">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-233">Максимальное число виртуальных процессоров, которые можно наблюдать внутри виртуальной машины, принадлежащих одному виртуальному узлу NUMA.</span><span class="sxs-lookup"><span data-stu-id="89c9f-233">The maximum number of virtual processors that can be observed within the virtual machine as belonging to a single virtual NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-234">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="89c9f-234">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-237">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="89c9f-237">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="89c9f-238">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-239">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="89c9f-239">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-242">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="89c9f-242">The parent of the resource.</span></span> <span data-ttu-id="89c9f-243">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-244">**пулид**</span><span class="sxs-lookup"><span data-stu-id="89c9f-244">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-245">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-247">Идентификатор пула ресурсов, из которого был выделен ресурс.</span><span class="sxs-lookup"><span data-stu-id="89c9f-247">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="89c9f-248">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-249">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="89c9f-249">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-250">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89c9f-250">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-252">Объем ресурсов ЦП, зарезервированных для использования виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="89c9f-252">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="89c9f-253">Эти ресурсы гарантированно доступны для использования виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="89c9f-253">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="89c9f-254">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="89c9f-255">0</span><span class="sxs-lookup"><span data-stu-id="89c9f-255">0</span></span>

<span data-ttu-id="89c9f-256">Диапазон: 0 100000</span><span class="sxs-lookup"><span data-stu-id="89c9f-256">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-257">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="89c9f-257">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-260">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="89c9f-260">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="89c9f-261">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89c9f-261">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="89c9f-262">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-263">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="89c9f-263">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-264">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="89c9f-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-266">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="89c9f-266">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="89c9f-267">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="89c9f-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-269">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89c9f-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-271">Общее число ядер в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="89c9f-271">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="89c9f-272">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-273">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="89c9f-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="89c9f-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-276">Задает единицу измерения для этого выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89c9f-276">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="89c9f-277">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="89c9f-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="89c9f-278">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="89c9f-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="89c9f-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c9f-280">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89c9f-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89c9f-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c9f-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c9f-282">Вес для каждого процессора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="89c9f-282">The weight for each virtual machine processor.</span></span> <span data-ttu-id="89c9f-283">После выполнения всех резервов оставшийся объем физического процессора платформы размещения будет выделен виртуальным машинам на основе их относительного веса.</span><span class="sxs-lookup"><span data-stu-id="89c9f-283">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="89c9f-284">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="89c9f-284">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="89c9f-285">100</span><span class="sxs-lookup"><span data-stu-id="89c9f-285">100</span></span>

<span data-ttu-id="89c9f-286">Диапазон: 0 10000</span><span class="sxs-lookup"><span data-stu-id="89c9f-286">Range: 0 10000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89c9f-287">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89c9f-287">Remarks</span></span>

<span data-ttu-id="89c9f-288">Доступ к классу **\_ процессорсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="89c9f-288">Access to the **Msvm\_ProcessorSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="89c9f-289">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="89c9f-289">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="89c9f-290">Требования</span><span class="sxs-lookup"><span data-stu-id="89c9f-290">Requirements</span></span>



| <span data-ttu-id="89c9f-291">Требование</span><span class="sxs-lookup"><span data-stu-id="89c9f-291">Requirement</span></span> | <span data-ttu-id="89c9f-292">Значение</span><span class="sxs-lookup"><span data-stu-id="89c9f-292">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c9f-293">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89c9f-293">Minimum supported client</span></span><br/> | <span data-ttu-id="89c9f-294">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="89c9f-294">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="89c9f-295">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89c9f-295">Minimum supported server</span></span><br/> | <span data-ttu-id="89c9f-296">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="89c9f-296">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89c9f-297">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="89c9f-297">Namespace</span></span><br/>                | <span data-ttu-id="89c9f-298">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="89c9f-298">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="89c9f-299">MOF</span><span class="sxs-lookup"><span data-stu-id="89c9f-299">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89c9f-300"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89c9f-300"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89c9f-301">DLL</span><span class="sxs-lookup"><span data-stu-id="89c9f-301">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89c9f-302"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89c9f-302"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="89c9f-303">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89c9f-303">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c9f-304">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="89c9f-304">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="89c9f-305">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="89c9f-305">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="89c9f-306">Классы процессоров</span><span class="sxs-lookup"><span data-stu-id="89c9f-306">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

