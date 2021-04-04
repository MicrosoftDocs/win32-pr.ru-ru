---
description: Представляет настроенное состояние памяти для виртуальной машины.
ms.assetid: 4B6FEE50-1C5F-4F41-B14A-E10B40400A1B
title: Класс Msvm_MemorySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MemorySettingData
- Msvm_MemorySettingData.InstanceID
- Msvm_MemorySettingData.Caption
- Msvm_MemorySettingData.Description
- Msvm_MemorySettingData.ElementName
- Msvm_MemorySettingData.ResourceType
- Msvm_MemorySettingData.OtherResourceType
- Msvm_MemorySettingData.ResourceSubType
- Msvm_MemorySettingData.PoolID
- Msvm_MemorySettingData.ConsumerVisibility
- Msvm_MemorySettingData.HostResource
- Msvm_MemorySettingData.HugePagesEnabled
- Msvm_MemorySettingData.AllocationUnits
- Msvm_MemorySettingData.VirtualQuantity
- Msvm_MemorySettingData.Reservation
- Msvm_MemorySettingData.Limit
- Msvm_MemorySettingData.Weight
- Msvm_MemorySettingData.AutomaticAllocation
- Msvm_MemorySettingData.AutomaticDeallocation
- Msvm_MemorySettingData.Parent
- Msvm_MemorySettingData.Connection
- Msvm_MemorySettingData.Address
- Msvm_MemorySettingData.MappingBehavior
- Msvm_MemorySettingData.AddressOnParent
- Msvm_MemorySettingData.VirtualQuantityUnits
- Msvm_MemorySettingData.DynamicMemoryEnabled
- Msvm_MemorySettingData.TargetMemoryBuffer
- Msvm_MemorySettingData.IsVirtualized
- Msvm_MemorySettingData.SwapFilesInUse
- Msvm_MemorySettingData.MaxMemoryBlocksPerNumaNode
- Msvm_MemorySettingData.SgxSize
- Msvm_MemorySettingData.SgxEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47309fead7ee45936f34e1e4286ee94437823df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998436"
---
# <a name="msvm_memorysettingdata-class"></a><span data-ttu-id="cd4c1-103">\_Класс мсвм меморисеттингдата</span><span class="sxs-lookup"><span data-stu-id="cd4c1-103">Msvm\_MemorySettingData class</span></span>

<span data-ttu-id="cd4c1-104">Представляет настроенное состояние памяти для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-104">Represents the configured state of the memory for a virtual machine.</span></span>

<span data-ttu-id="cd4c1-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd4c1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd4c1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MemorySettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Memory Default Settings";
  string  Description = "Describes the default settings for the memory resources.";
  string  ElementName;
  uint16  ResourceType = 4;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Memory";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  boolean HugePagesEnabled;
  string  AllocationUnits = "byte * 2^20";
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "byte * 2^20";
  boolean DynamicMemoryEnabled;
  uint32  TargetMemoryBuffer;
  boolean IsVirtualized = True;
  boolean SwapFilesInUse;
  uint64  MaxMemoryBlocksPerNumaNode;
  uint64  SgxSize;
  boolean SgxEnabled;
};
```

## <a name="members"></a><span data-ttu-id="cd4c1-107">Члены</span><span class="sxs-lookup"><span data-stu-id="cd4c1-107">Members</span></span>

<span data-ttu-id="cd4c1-108">Класс **мсвм \_ меморисеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cd4c1-108">The **Msvm\_MemorySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="cd4c1-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd4c1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd4c1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd4c1-110">Properties</span></span>

<span data-ttu-id="cd4c1-111">Класс **мсвм \_ меморисеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-111">The **Msvm\_MemorySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd4c1-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-115">The address of the resource.</span></span> <span data-ttu-id="cd4c1-116">Например, MAC-адрес порта Ethernet.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-116">For example, the MAC address of an Ethernet port.</span></span> <span data-ttu-id="cd4c1-117">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-118">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-121">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="cd4c1-122">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="cd4c1-123">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-124">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-127">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="cd4c1-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="cd4c1-128">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-129">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-130">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-132">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="cd4c1-133">Например, если для этого свойства задано **значение true** , а используемая виртуальная машина включена, этот ресурс будет выделен.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-133">For example, when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="cd4c1-134">Значение **false** указывает, что ресурс должен быть явно выделен.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-134">A value of **False** indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="cd4c1-135">Например, параметр может представлять съемные носители (например, компакт-диски или дискеты), где при запуске отсутствует носитель.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-135">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="cd4c1-136">Для выделения ресурса требуется явная операция.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-136">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="cd4c1-137">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-138">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-138">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-139">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-141">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-141">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="cd4c1-142">Например, если для этого свойства задано **значение true** , а используемая виртуальная машина включена, этот ресурс будет выделен.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-142">For example when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="cd4c1-143">Если это свойство имеет **значение false**, ресурс должен быть явно выделен.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-143">When this property is **False**, the resource must be explicitly allocated.</span></span> <span data-ttu-id="cd4c1-144">Например, параметр может представлять съемные носители (например, компакт-диски или дискеты), где при запуске отсутствует носитель.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-144">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="cd4c1-145">Для выделения ресурса требуется явная операция.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-145">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="cd4c1-146">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-147">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-150">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="cd4c1-150">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-151">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-151">A short description of the object.</span></span> <span data-ttu-id="cd4c1-152">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-153">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-153">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-154">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-156">Устройство, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-156">The device to which this resource is connected.</span></span> <span data-ttu-id="cd4c1-157">Например, именованная сеть или порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-157">For example, a named network or switch port.</span></span> <span data-ttu-id="cd4c1-158">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-158">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-159">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-160">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-162">Описывает видимость пользователей для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="cd4c1-163">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-164">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-167">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-167">A description of the object.</span></span> <span data-ttu-id="cd4c1-168">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-169">**DynamicMemoryEnabled**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-169">**DynamicMemoryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-170">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-172">Указывает, включена ли динамическая память для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-172">Indicates whether dynamic memory is enabled for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-176">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-176">A display name for the object.</span></span> <span data-ttu-id="cd4c1-177">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-178">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-178">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-179">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-181">Первый элемент массива содержит ссылку на базовый ресурс узла, который необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-181">The first element of this array contains a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="cd4c1-182">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-182">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but it is not used.</span></span>

</dd> <dt>
  
<span data-ttu-id="cd4c1-183">**хужепажесенаблед**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-183">**HugePagesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-186">Указывает, поддерживается ли объем памяти страницами по 1 ГБ.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-186">Whether the memory is backed by 1GB pages or not.</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-190">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-190">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-191">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-191">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="cd4c1-192">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-193">**Виртуализированный**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-193">**IsVirtualized**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-194">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-196">Указывает, является ли устройство виртуализированным или переданным через.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-196">Indicates whether this device is virtualized or passed through.</span></span> <span data-ttu-id="cd4c1-197">Если задано **значение false**, то используется базовый или главный ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-197">When set to **False**, the underlying or host resource is used.</span></span> <span data-ttu-id="cd4c1-198">В свойстве **DeviceID** должен присутствовать хотя бы один элемент.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-198">At least one item should be present in the **DeviceID** property.</span></span> <span data-ttu-id="cd4c1-199">Если задано **значение true**, ресурс является виртуализированным и может не сопоставляться напрямую с базовым ресурсом или узлом.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-199">When set to **True**, the resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="cd4c1-200">Некоторые реализации могут поддерживать определенное назначение виртуализованных ресурсов. в этом случае ресурсы узла предоставляются с помощью свойства **DeviceID** .</span><span class="sxs-lookup"><span data-stu-id="cd4c1-200">Some implementations may support specific assignment for virtualized resources, in which case the host resources are exposed by using the **DeviceID** property.</span></span> <span data-ttu-id="cd4c1-201">Это свойство всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-201">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-202">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-203">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-205">Максимальный объем памяти, который может использоваться виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-205">The maximum amount of memory that may be consumed by the virtual machine.</span></span> <span data-ttu-id="cd4c1-206">Для виртуальной машины с включенной динамической памятью представляет параметр максимального объема памяти.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-206">For a virtual machine with dynamic memory enabled, this represents the maximum memory setting.</span></span> <span data-ttu-id="cd4c1-207">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-208">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-209">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-211">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="cd4c1-212">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-213">**максмемориблоккспернуманоде**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-213">**MaxMemoryBlocksPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-214">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-216">Максимальный объем памяти, который можно наблюдать в виртуальной машине, принадлежащей одному узлу NUMA.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-216">The maximum amount of memory that can be observed within the virtual machine as belonging to a single NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-217">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-220">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение other.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="cd4c1-221">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-222">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-225">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-225">The parent of the resource.</span></span> <span data-ttu-id="cd4c1-226">Например, контроллер для текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="cd4c1-227">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-228">**пулид**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-231">Идентификатор пула ресурсов, из которого был выделен ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-231">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="cd4c1-232">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-233">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-234">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-236">Указывает объем памяти, который должен быть доступен для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-236">Specifies the amount of memory guaranteed to be available for this virtual machine.</span></span> <span data-ttu-id="cd4c1-237">Для виртуальной машины с включенной динамической памятью представляет параметр минимального объема памяти.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-237">For a virtual machine with dynamic memory enabled, this represents the minimum memory setting.</span></span> <span data-ttu-id="cd4c1-238">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-242">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="cd4c1-243">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="cd4c1-244">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-246">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-248">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-248">The type of resource that this allocation setting represents.</span></span> <span data-ttu-id="cd4c1-249">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 4 (память).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 4 (Memory).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-250">**сгксенаблед**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-250">**SgxEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-251">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-253">Указывает, включен ли SGX.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-253">Indicates if SGX is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="cd4c1-254">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-254">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd4c1-255">**сгкссизе**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-255">**SgxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-256">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-258">Объем памяти SGX, выделяемой для виртуальной машины (в МБ).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-258">The amount of SGX memory to allocate for the VM, in MB.</span></span>

> [!Note]  
> <span data-ttu-id="cd4c1-259">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-259">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd4c1-260">**свапфилесинусе**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-260">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-261">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-263">**Значение true** , если подкачка на втором уровне активна; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-263">**True** if second level paging is active; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-264">**таржетмеморибуффер**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-264">**TargetMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-265">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-267">Определяет объем дополнительной памяти, который необходимо зарезервировать для виртуальной машины в среде выполнения, в процентах от общего объема памяти, который требуется виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-267">Defines the amount of extra memory that should be reserved for a virtual machine at runtime, as a percentage of the total memory that the virtual machine is thought to need.</span></span> <span data-ttu-id="cd4c1-268">Это относится только к виртуальным машинам с включенной динамической памятью.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-268">This only applies to virtual machines with dynamic memory enabled.</span></span>

<span data-ttu-id="cd4c1-269">Это свойство может иметь значение в диапазоне от 5 до 2000.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-269">This property can be in the range of 5 to 2000.</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-270">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-270">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-271">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-273">Общий объем ОЗУ виртуальной машины, отображаемый в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-273">The total amount of RAM in the virtual machine, as seen by the guest operating system.</span></span> <span data-ttu-id="cd4c1-274">Для виртуальной машины с включенной динамической памятью это представляет собой начальную память, доступную при запуске.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-274">For a virtual machine with dynamic memory enabled, this represents the initial memory available at startup.</span></span> <span data-ttu-id="cd4c1-275">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-276">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-276">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-277">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-279">Задает единицу измерения для этого выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-279">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="cd4c1-280">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-280">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="cd4c1-281">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="cd4c1-282">**Weight**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-282">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd4c1-283">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd4c1-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd4c1-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd4c1-285">Определяет значение веса выделения памяти для каждой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-285">Defines the memory allocation weighting value for each virtual machine.</span></span> <span data-ttu-id="cd4c1-286">После того как все резервы будут выполнены, оставшийся объем памяти платформы размещения будет выделен виртуальным машинам на основе их относительного веса (не превышающих значение, заданное свойством **Limit** ).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-286">After all reserves have been met, the remaining memory of the hosting platform will be allocated to virtual machines based on their relative weights (not to exceed the value specified by the **Limit** property).</span></span> <span data-ttu-id="cd4c1-287">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-287">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd4c1-288">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd4c1-288">Remarks</span></span>

<span data-ttu-id="cd4c1-289">Доступ к классу **\_ меморисеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="cd4c1-289">Access to the **Msvm\_MemorySettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cd4c1-290">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cd4c1-290">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="cd4c1-291">Примеры</span><span class="sxs-lookup"><span data-stu-id="cd4c1-291">Examples</span></span>

```powershell
function WaitForResult
{
  param($result)
  if ($result.ReturnValue -eq 4096)
  {
    while($true)
    {
      $result.Job
      if ($result.Job -ne $null)
      {
        if ($result.Job.JobState -gt 4)
        {
          return $result.Job.ErrorCode
        }
      }
      start-sleep 1
    }
  }
  else
  {
    return $result.ReturnValue
  }
}

if ($($args.count) -ne 2)
{
  Write-Host "EnableHugePages.ps1 VMName SizeInMB"
  return
}

$vmName = $args[0]
$sizeInMB = $args[1]
 
$namespace = "root\virtualization\v2"
$vm = Get-WmiObject -class MSVM_ComputerSystem -filter "ElementName='$vmName'" -namespace $namespace
$settings = Get-WmiObject -query "Associators of {$vm} where ResultClass = Msvm_VirtualSystemSettingData" -namespace $namespace
$vmSettings = $settings | ? VirtualSystemType -eq "Microsoft:Hyper-V:System:Realized"
$memorySettings = Get-WmiObject -query "Associators of {$vmSettings} where ResultClass = Msvm_MemorySettingData" -namespace $namespace

$memorySettings.MaxMemoryBlocksPerNumaNode = $sizeInMB
$memorySettings.Reservation = $sizeInMB
$memorySettings.Limit = $sizeInMB
$memorySettings.VirtualQuantity = $sizeInMB
$memorySettings.HugePagesEnabled = $True

$vmSvc = Get-WmiObject -class Msvm_VirtualSystemManagementService -namespace $namespace
$res = $vmSvc.ModifyResourceSettings($memorySettings.GetText(2))
if (WaitForResult($res) -ne 0)
{
  Write-Host "Failed."
}
```

## <a name="requirements"></a><span data-ttu-id="cd4c1-292">Требования</span><span class="sxs-lookup"><span data-stu-id="cd4c1-292">Requirements</span></span>



| <span data-ttu-id="cd4c1-293">Требование</span><span class="sxs-lookup"><span data-stu-id="cd4c1-293">Requirement</span></span> | <span data-ttu-id="cd4c1-294">Значение</span><span class="sxs-lookup"><span data-stu-id="cd4c1-294">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd4c1-295">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd4c1-295">Minimum supported client</span></span><br/> | <span data-ttu-id="cd4c1-296">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cd4c1-296">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cd4c1-297">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd4c1-297">Minimum supported server</span></span><br/> | <span data-ttu-id="cd4c1-298">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cd4c1-298">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd4c1-299">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cd4c1-299">Namespace</span></span><br/>                | <span data-ttu-id="cd4c1-300">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="cd4c1-300">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cd4c1-301">MOF</span><span class="sxs-lookup"><span data-stu-id="cd4c1-301">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd4c1-302"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd4c1-302"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd4c1-303">DLL</span><span class="sxs-lookup"><span data-stu-id="cd4c1-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd4c1-304"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd4c1-304"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd4c1-305">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd4c1-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd4c1-306">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-306">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="cd4c1-307">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="cd4c1-307">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="cd4c1-308">Классы памяти</span><span class="sxs-lookup"><span data-stu-id="cd4c1-308">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

