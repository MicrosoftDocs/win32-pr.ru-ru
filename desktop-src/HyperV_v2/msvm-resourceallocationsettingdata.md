---
description: Представляет текущее и записанное состояние выделения виртуального ресурса.
ms.assetid: 5C180933-2013-4E16-A9BD-653D5426F468
title: Класс Msvm_ResourceAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationSettingData
- Msvm_ResourceAllocationSettingData.InstanceID
- Msvm_ResourceAllocationSettingData.Caption
- Msvm_ResourceAllocationSettingData.Description
- Msvm_ResourceAllocationSettingData.ElementName
- Msvm_ResourceAllocationSettingData.ResourceType
- Msvm_ResourceAllocationSettingData.OtherResourceType
- Msvm_ResourceAllocationSettingData.ResourceSubType
- Msvm_ResourceAllocationSettingData.PoolID
- Msvm_ResourceAllocationSettingData.ConsumerVisibility
- Msvm_ResourceAllocationSettingData.HostResource
- Msvm_ResourceAllocationSettingData.AllocationUnits
- Msvm_ResourceAllocationSettingData.VirtualQuantity
- Msvm_ResourceAllocationSettingData.Reservation
- Msvm_ResourceAllocationSettingData.Limit
- Msvm_ResourceAllocationSettingData.Weight
- Msvm_ResourceAllocationSettingData.AutomaticAllocation
- Msvm_ResourceAllocationSettingData.AutomaticDeallocation
- Msvm_ResourceAllocationSettingData.Parent
- Msvm_ResourceAllocationSettingData.Connection
- Msvm_ResourceAllocationSettingData.Address
- Msvm_ResourceAllocationSettingData.MappingBehavior
- Msvm_ResourceAllocationSettingData.AddressOnParent
- Msvm_ResourceAllocationSettingData.VirtualQuantityUnits
- Msvm_ResourceAllocationSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6d1cb2f97dcb3fa144db5cf27c1a82690214b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346052"
---
# <a name="msvm_resourceallocationsettingdata-class"></a><span data-ttu-id="0ad59-103">\_Класс мсвм ресаурцеаллокатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="0ad59-103">Msvm\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="0ad59-104">Представляет текущее и записанное состояние выделения виртуального ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ad59-104">Represents the current and recorded allocation states of a virtual resource.</span></span>

<span data-ttu-id="0ad59-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0ad59-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad59-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ad59-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption;
  string  Description;
  string  ElementName;
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
  string  VirtualSystemIdentifiers[] = { "GUID" };
};
```

## <a name="members"></a><span data-ttu-id="0ad59-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0ad59-107">Members</span></span>

<span data-ttu-id="0ad59-108">Класс **мсвм \_ ресаурцеаллокатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0ad59-108">The **Msvm\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0ad59-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ad59-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ad59-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ad59-110">Properties</span></span>

<span data-ttu-id="0ad59-111">Класс **мсвм \_ ресаурцеаллокатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0ad59-111">The **Msvm\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ad59-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="0ad59-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ad59-115">The address of the resource.</span></span> <span data-ttu-id="0ad59-116">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0ad59-117">Это свойство доступно только для чтения, но если свойство **ResourceType** имеет значение 20 (графический контроллер), его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad59-117">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-118">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="0ad59-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-121">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="0ad59-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="0ad59-122">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="0ad59-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="0ad59-123">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-124">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="0ad59-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-127">Единица распределения, используемая свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="0ad59-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="0ad59-128">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-129">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="0ad59-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-130">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0ad59-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-132">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="0ad59-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="0ad59-133">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-134">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="0ad59-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-135">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0ad59-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-137">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="0ad59-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="0ad59-138">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-139">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0ad59-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-142">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="0ad59-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-143">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0ad59-143">A short description of the object.</span></span> <span data-ttu-id="0ad59-144">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0ad59-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-145">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="0ad59-145">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-146">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0ad59-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-148">Устройство, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="0ad59-148">The device to which this resource is connected.</span></span> <span data-ttu-id="0ad59-149">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-149">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0ad59-150">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0ad59-150">This is a read-only property.</span></span> <span data-ttu-id="0ad59-151">Но если свойство **ResourceType** имеет значение 21 (последовательный порт), а свойство **Ресаурцесубтипе** имеет значение Microsoft: Hyper-V: последовательный порт, свойство **Connection** можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad59-151">But if the **ResourceType** property is 21 (Serial port) and the **ResourceSubType** property is "Microsoft:Hyper-V:Serial Port", the **Connection** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-152">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="0ad59-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-153">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ad59-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-155">Видимость потребителя для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ad59-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="0ad59-156">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0ad59-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-160">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0ad59-160">A description of the object.</span></span> <span data-ttu-id="0ad59-161">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0ad59-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0ad59-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-165">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0ad59-165">A display name for the object.</span></span> <span data-ttu-id="0ad59-166">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0ad59-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="0ad59-167">Изменение этого свойства приведет к изменению имени элемента связанного логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0ad59-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="0ad59-168">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad59-168">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-169">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="0ad59-169">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-170">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0ad59-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-172">Каждому устройству на виртуальной машине можно назначить только один ресурс узла, поэтому можно установить только первый элемент этого массива.</span><span class="sxs-lookup"><span data-stu-id="0ad59-172">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="0ad59-173">Для устройств, поддерживающих эту функцию, установите первый элемент массива **хостресаурце** , чтобы он содержал ссылку на базовый ресурс узла, который нужно назначить.</span><span class="sxs-lookup"><span data-stu-id="0ad59-173">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="0ad59-174">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-174">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0ad59-175">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0ad59-175">This is a read-only property.</span></span> <span data-ttu-id="0ad59-176">Но если свойство **ResourceType** имеет значение 17 (Disk), а свойство **Ресаурцесубтипе** имеет значение Microsoft: Hyper-V: физический диск, свойство **хостресаурце** можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad59-176">But if the **ResourceType** property is 17 (Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Physical Disk Drive", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0ad59-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-180">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="0ad59-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-181">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="0ad59-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0ad59-182">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение "Microsoft:*GUID* \\ *девицеспеЦификдата*".</span><span class="sxs-lookup"><span data-stu-id="0ad59-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-183">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="0ad59-183">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-184">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0ad59-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-186">Максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="0ad59-186">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="0ad59-187">Единица измерения для этого свойства задается свойством **виртуалкуантитюнитс** .</span><span class="sxs-lookup"><span data-stu-id="0ad59-187">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="0ad59-188">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-189">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="0ad59-189">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-190">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ad59-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-192">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="0ad59-192">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="0ad59-193">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-194">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="0ad59-194">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-197">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а [**ResourceType**](msvm-processorsettingdata.md) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="0ad59-197">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="0ad59-198">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-198">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-199">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="0ad59-199">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-202">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ad59-202">The parent of the resource.</span></span> <span data-ttu-id="0ad59-203">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-203">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-204">**пулид**</span><span class="sxs-lookup"><span data-stu-id="0ad59-204">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-207">Идентификатор пула ресурсов, из которого был выделен ресурс.</span><span class="sxs-lookup"><span data-stu-id="0ad59-207">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="0ad59-208">Для экземпляров, связанных с виртуальной машиной, это будет «Microsoft:*GUID* \\ *-данные устройства*».</span><span class="sxs-lookup"><span data-stu-id="0ad59-208">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="0ad59-209">Для экземпляров, определяющих потенциальные параметры виртуальной машины, это будет "Microsoft: определение \\  \\ *типа* GUID", где *тип* может быть одним из значений: "максимум", "минимум", "default" или "Increment".</span><span class="sxs-lookup"><span data-stu-id="0ad59-209">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="0ad59-210">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-211">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="0ad59-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-212">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0ad59-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-214">Объем ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="0ad59-214">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="0ad59-215">Единица измерения для этого свойства задается свойством **виртуалкуантитюнитс** .</span><span class="sxs-lookup"><span data-stu-id="0ad59-215">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="0ad59-216">Эти ресурсы гарантированно доступны для использования виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="0ad59-216">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="0ad59-217">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="0ad59-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-221">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ad59-221">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="0ad59-222">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ad59-222">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="0ad59-223">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-223">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-224">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0ad59-224">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-225">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ad59-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-227">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="0ad59-227">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="0ad59-228">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-228">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="0ad59-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0ad59-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="0ad59-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="0ad59-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="0ad59-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="0ad59-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="0ad59-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="0ad59-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="0ad59-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="0ad59-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="0ad59-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="0ad59-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="0ad59-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="0ad59-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Флоппи-дисковод** (14)</span><span class="sxs-lookup"><span data-stu-id="0ad59-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="0ad59-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="0ad59-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Диск** (17)</span><span class="sxs-lookup"><span data-stu-id="0ad59-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Ленточный накопитель** (18)</span><span class="sxs-lookup"><span data-stu-id="0ad59-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Область хранения** (19)</span><span class="sxs-lookup"><span data-stu-id="0ad59-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Другое запоминающее устройство** (20)</span><span class="sxs-lookup"><span data-stu-id="0ad59-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Последовательный порт** (21)</span><span class="sxs-lookup"><span data-stu-id="0ad59-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Параллельный порт** (22)</span><span class="sxs-lookup"><span data-stu-id="0ad59-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Контроллер USB** (23)</span><span class="sxs-lookup"><span data-stu-id="0ad59-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Графический контроллер** (24)</span><span class="sxs-lookup"><span data-stu-id="0ad59-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Контроллер IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="0ad59-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="0ad59-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="0ad59-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Источник питания** (28)</span><span class="sxs-lookup"><span data-stu-id="0ad59-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Охлаждающее устройство** (29)</span><span class="sxs-lookup"><span data-stu-id="0ad59-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Порт коммутатора Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="0ad59-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Логический диск** (31)</span><span class="sxs-lookup"><span data-stu-id="0ad59-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Том хранилища** (32)</span><span class="sxs-lookup"><span data-stu-id="0ad59-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-подключение** (33)</span><span class="sxs-lookup"><span data-stu-id="0ad59-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="0ad59-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="0ad59-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad59-264">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="0ad59-264">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-265">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0ad59-265">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-267">Указывает количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="0ad59-267">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="0ad59-268">Единица измерения для этого свойства задается свойством **виртуалкуантитюнитс** .</span><span class="sxs-lookup"><span data-stu-id="0ad59-268">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="0ad59-269">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-269">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-270">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="0ad59-270">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-271">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ad59-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-273">Задает единицу измерения для этого выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ad59-273">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="0ad59-274">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0ad59-274">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="0ad59-275">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-276">**виртуалсистемидентифиерс**</span><span class="sxs-lookup"><span data-stu-id="0ad59-276">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-277">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0ad59-277">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-279">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="0ad59-279">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-280">Строковый массив идентификаторов этого ресурса, представленный операционной системе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0ad59-280">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="0ad59-281">Эти значения используются только в том случае, если свойство **ResourceType** имеет значение 6 (Parallel SCSI HBA), а свойство **ресаурцесубтипе** имеет значение "синтетический SCSI-контроллер (Майкрософт)".</span><span class="sxs-lookup"><span data-stu-id="0ad59-281">These values are used only if the **ResourceType** property is set to 6 (Parallel SCSI HBA) and the **ResourceSubType** property is set to "Microsoft Synthetic SCSI Controller".</span></span> <span data-ttu-id="0ad59-282">Для этого свойства задано значение "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="0ad59-282">This property is set to "*GUID*".</span></span>

<span data-ttu-id="0ad59-283">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad59-283">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0ad59-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="0ad59-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad59-285">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ad59-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ad59-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ad59-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad59-287">Целое число, определяющее относительный вес для каждого процессора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0ad59-287">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="0ad59-288">После выполнения всех резервов оставшийся объем физического процессора платформы размещения будет выделен виртуальным машинам на основе их относительного веса.</span><span class="sxs-lookup"><span data-stu-id="0ad59-288">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="0ad59-289">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0ad59-289">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0ad59-290">Диапазон: 0 1000</span><span class="sxs-lookup"><span data-stu-id="0ad59-290">Range: 0 1000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ad59-291">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ad59-291">Remarks</span></span>

<span data-ttu-id="0ad59-292">Доступ к классу **\_ ресаурцеаллокатионсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="0ad59-292">Access to the **Msvm\_ResourceAllocationSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0ad59-293">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0ad59-293">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad59-294">Требования</span><span class="sxs-lookup"><span data-stu-id="0ad59-294">Requirements</span></span>



| <span data-ttu-id="0ad59-295">Требование</span><span class="sxs-lookup"><span data-stu-id="0ad59-295">Requirement</span></span> | <span data-ttu-id="0ad59-296">Значение</span><span class="sxs-lookup"><span data-stu-id="0ad59-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad59-297">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ad59-297">Minimum supported client</span></span><br/> | <span data-ttu-id="0ad59-298">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0ad59-298">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0ad59-299">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ad59-299">Minimum supported server</span></span><br/> | <span data-ttu-id="0ad59-300">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0ad59-300">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ad59-301">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0ad59-301">Namespace</span></span><br/>                | <span data-ttu-id="0ad59-302">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0ad59-302">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0ad59-303">MOF</span><span class="sxs-lookup"><span data-stu-id="0ad59-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ad59-304"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ad59-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ad59-305">DLL</span><span class="sxs-lookup"><span data-stu-id="0ad59-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ad59-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ad59-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ad59-307">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ad59-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad59-308">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="0ad59-308">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="0ad59-309">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="0ad59-309">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="0ad59-310">**Мсвм \_ ресаурцеаллокатионсеттингдата (v1)**</span><span class="sxs-lookup"><span data-stu-id="0ad59-310">**Msvm\_ResourceAllocationSettingData (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="0ad59-311">Классы управления ресурсами</span><span class="sxs-lookup"><span data-stu-id="0ad59-311">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

