---
description: Представляет параметры для искусственного трехмерного контроллера экрана для виртуальной машины.
ms.assetid: 7162AEED-90CB-41C3-BD44-8B552C00F597
title: Класс Msvm_Synthetic3DDisplayControllerSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayControllerSettingData
- Msvm_Synthetic3DDisplayControllerSettingData.InstanceID
- Msvm_Synthetic3DDisplayControllerSettingData.Caption
- Msvm_Synthetic3DDisplayControllerSettingData.Description
- Msvm_Synthetic3DDisplayControllerSettingData.ElementName
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.OtherResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceSubType
- Msvm_Synthetic3DDisplayControllerSettingData.PoolID
- Msvm_Synthetic3DDisplayControllerSettingData.ConsumerVisibility
- Msvm_Synthetic3DDisplayControllerSettingData.HostResource
- Msvm_Synthetic3DDisplayControllerSettingData.AllocationUnits
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantity
- Msvm_Synthetic3DDisplayControllerSettingData.Reservation
- Msvm_Synthetic3DDisplayControllerSettingData.Limit
- Msvm_Synthetic3DDisplayControllerSettingData.Weight
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticAllocation
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticDeallocation
- Msvm_Synthetic3DDisplayControllerSettingData.Parent
- Msvm_Synthetic3DDisplayControllerSettingData.Connection
- Msvm_Synthetic3DDisplayControllerSettingData.Address
- Msvm_Synthetic3DDisplayControllerSettingData.MappingBehavior
- Msvm_Synthetic3DDisplayControllerSettingData.AddressOnParent
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantityUnits
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumScreenResolution
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumMonitors
- Msvm_Synthetic3DDisplayControllerSettingData.VRAMSizeBytes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c93bb67cd4a66c4ecc5f6820ff2de7cf3816b2b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683169"
---
# <a name="msvm_synthetic3ddisplaycontrollersettingdata-class"></a><span data-ttu-id="3f64b-103">\_Класс мсвм Synthetic3DDisplayControllerSettingData</span><span class="sxs-lookup"><span data-stu-id="3f64b-103">Msvm\_Synthetic3DDisplayControllerSettingData class</span></span>

<span data-ttu-id="3f64b-104">Представляет параметры для искусственного трехмерного контроллера экрана для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3f64b-104">Represents settings for a synthetic 3-D display controller for a virtual machine.</span></span> <span data-ttu-id="3f64b-105">Этот класс используется только с виртуальными машинами, использующими RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="3f64b-105">This class is only used with virtual machines that use RemoteFX.</span></span>

<span data-ttu-id="3f64b-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3f64b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f64b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f64b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "3D Display Controller Default Settings";
  string  Description = "Describes the default settings for the 3D video controller resource pool.";
  string  ElementName;
  uint16  ResourceType = 24;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint8   MaximumScreenResolution;
  uint8   MaximumMonitors;
  uint64  VRAMSizeBytes;
};
```

## <a name="members"></a><span data-ttu-id="3f64b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3f64b-108">Members</span></span>

<span data-ttu-id="3f64b-109">Класс **мсвм \_ Synthetic3DDisplayControllerSettingData** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3f64b-109">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3f64b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f64b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f64b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f64b-111">Properties</span></span>

<span data-ttu-id="3f64b-112">Класс **мсвм \_ Synthetic3DDisplayControllerSettingData** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3f64b-112">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f64b-113">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="3f64b-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-116">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="3f64b-116">The address of the resource.</span></span> <span data-ttu-id="3f64b-117">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3f64b-118">Это свойство доступно только для чтения, но если свойство **ResourceType** имеет значение 20 (графический контроллер), его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3f64b-118">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-119">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="3f64b-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-122">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="3f64b-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="3f64b-123">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="3f64b-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="3f64b-124">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-125">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="3f64b-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-128">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="3f64b-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="3f64b-129">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-130">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="3f64b-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-131">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3f64b-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-133">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="3f64b-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="3f64b-134">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-135">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="3f64b-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-136">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3f64b-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-138">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="3f64b-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="3f64b-139">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-140">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3f64b-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-143">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="3f64b-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-144">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3f64b-144">A short description of the object.</span></span> <span data-ttu-id="3f64b-145">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3f64b-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-146">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="3f64b-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-147">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3f64b-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-149">Устройство, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="3f64b-149">The device to which this resource is connected.</span></span> <span data-ttu-id="3f64b-150">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3f64b-151">Это свойство доступно только для чтения, но если значение равно 1), свойство **ResourceType** имеет значение 17 (последовательный порт) или 2), свойство **ResourceType** равно 21 (экстент хранения), а свойство **Ресаурцесубтипе** — "Microsoft Virtual жесткий диск", затем его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3f64b-151">This is a read-only property, but if either 1) the **ResourceType** property is 17 (Serial port), or 2) the **ResourceType** property is 21 (Storage Extent) and the **ResourceSubType** property is "Microsoft Virtual Hard Disk", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-152">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="3f64b-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-153">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f64b-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-155">Видимость потребителя для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="3f64b-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="3f64b-156">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3f64b-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-160">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3f64b-160">A description of the object.</span></span> <span data-ttu-id="3f64b-161">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3f64b-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3f64b-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-165">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="3f64b-165">A display name for the object.</span></span> <span data-ttu-id="3f64b-166">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f64b-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="3f64b-167">Изменение этого свойства приведет к изменению имени элемента связанного логического устройства.</span><span class="sxs-lookup"><span data-stu-id="3f64b-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-168">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="3f64b-168">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-169">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3f64b-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-171">Каждому устройству на виртуальной машине можно назначить только один ресурс узла, поэтому можно установить только первый элемент этого массива.</span><span class="sxs-lookup"><span data-stu-id="3f64b-171">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="3f64b-172">Для устройств, поддерживающих эту функцию, установите первый элемент массива **хостресаурце** , чтобы он содержал ссылку на базовый ресурс узла, который будет назначен.</span><span class="sxs-lookup"><span data-stu-id="3f64b-172">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource that is to be assigned.</span></span> <span data-ttu-id="3f64b-173">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-173">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-174">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3f64b-174">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-177">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="3f64b-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3f64b-178">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3f64b-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-179">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="3f64b-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-180">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f64b-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-182">Максимальный объем соответствующих ресурсов узла, которые могут использоваться виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="3f64b-182">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="3f64b-183">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-184">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="3f64b-184">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-185">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f64b-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-187">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="3f64b-187">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="3f64b-188">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-189">**максимуммониторс**</span><span class="sxs-lookup"><span data-stu-id="3f64b-189">**MaximumMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-190">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3f64b-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-191">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3f64b-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-192">Максимальное число мониторов, доступных для трехмерного контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="3f64b-192">The maximum number of monitors available to the 3-D display controller.</span></span> <span data-ttu-id="3f64b-193">Минимальное число мониторов равно 1, а максимальное значение зависит от максимального разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="3f64b-193">The minimum number of monitors is 1 and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="3f64b-194">В следующей таблице определяется максимальное число мониторов, разрешенных для различных способов разрешения.</span><span class="sxs-lookup"><span data-stu-id="3f64b-194">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="3f64b-195">Решение</span><span class="sxs-lookup"><span data-stu-id="3f64b-195">Resolution</span></span>            | <span data-ttu-id="3f64b-196">Максимальное число мониторов</span><span class="sxs-lookup"><span data-stu-id="3f64b-196">Maximum monitors</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="3f64b-197">1024 768</span><span class="sxs-lookup"><span data-stu-id="3f64b-197">1024  768</span></span><br/>  | <span data-ttu-id="3f64b-198">4</span><span class="sxs-lookup"><span data-stu-id="3f64b-198">4</span></span><br/>     |
| <span data-ttu-id="3f64b-199">1280 1024</span><span class="sxs-lookup"><span data-stu-id="3f64b-199">1280  1024</span></span><br/> | <span data-ttu-id="3f64b-200">4</span><span class="sxs-lookup"><span data-stu-id="3f64b-200">4</span></span><br/>     |
| <span data-ttu-id="3f64b-201">1600 1200</span><span class="sxs-lookup"><span data-stu-id="3f64b-201">1600  1200</span></span><br/> | <span data-ttu-id="3f64b-202">3</span><span class="sxs-lookup"><span data-stu-id="3f64b-202">3</span></span><br/>     |
| <span data-ttu-id="3f64b-203">1920 1200</span><span class="sxs-lookup"><span data-stu-id="3f64b-203">1920  1200</span></span><br/> | <span data-ttu-id="3f64b-204">2</span><span class="sxs-lookup"><span data-stu-id="3f64b-204">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="3f64b-205">**максимумскринресолутион**</span><span class="sxs-lookup"><span data-stu-id="3f64b-205">**MaximumScreenResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-206">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3f64b-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-208">Задает максимальное разрешение экрана для трехмерного контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="3f64b-208">Specifies the maximum screen resolution for the 3-D display controller.</span></span> <span data-ttu-id="3f64b-209">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3f64b-209">This must be one of the following values.</span></span>

<dt>

<span id="1024___768"></span>

<span data-ttu-id="3f64b-210"><span id="1024___768"></span>**1024 \* 768** (0)</span><span class="sxs-lookup"><span data-stu-id="3f64b-210"><span id="1024___768"></span>**1024 \* 768** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3f64b-211">Максимальное разрешение составляет 1024 768.</span><span class="sxs-lookup"><span data-stu-id="3f64b-211">The maximum resolution is 1024   768.</span></span>

</dd> <dt>

<span id="1280___1024"></span>

<span data-ttu-id="3f64b-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span><span class="sxs-lookup"><span data-stu-id="3f64b-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3f64b-213">Максимальное разрешение составляет 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="3f64b-213">The maximum resolution is 1280   1024.</span></span>

</dd> <dt>

<span id="1600___1200"></span>

<span data-ttu-id="3f64b-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span><span class="sxs-lookup"><span data-stu-id="3f64b-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3f64b-215">Максимальное разрешение составляет 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="3f64b-215">The maximum resolution is 1600   1200.</span></span>

</dd> <dt>

<span id="1920___1200"></span>

<span data-ttu-id="3f64b-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span><span class="sxs-lookup"><span data-stu-id="3f64b-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3f64b-217">Максимальное разрешение составляет 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="3f64b-217">The maximum resolution is 1920   1200.</span></span>

</dd> <dt>

<span id="2560___1600"></span>

<span data-ttu-id="3f64b-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span><span class="sxs-lookup"><span data-stu-id="3f64b-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3f64b-219">Максимальное разрешение составляет 2650 1600.</span><span class="sxs-lookup"><span data-stu-id="3f64b-219">The maximum resolution is 2650   1600.</span></span>

</dd> <dt>

<span id="3840___2160"></span>

<span data-ttu-id="3f64b-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span><span class="sxs-lookup"><span data-stu-id="3f64b-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3f64b-221">Максимальное разрешение составляет 3840 2160.</span><span class="sxs-lookup"><span data-stu-id="3f64b-221">The maximum resolution is 3840   2160.</span></span>

> [!Note]  
> <span data-ttu-id="3f64b-222">Добавлено в Windows 10 и Windows Server 2016. мсвм \_ синте</span><span class="sxs-lookup"><span data-stu-id="3f64b-222">Added in Windows 10 and Windows Server 2016.msvm\_synte</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3f64b-223">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="3f64b-223">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-226">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а [**ResourceType**](msvm-processorsettingdata.md) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="3f64b-226">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="3f64b-227">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-228">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="3f64b-228">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-231">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="3f64b-231">The parent of the resource.</span></span> <span data-ttu-id="3f64b-232">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-233">**пулид**</span><span class="sxs-lookup"><span data-stu-id="3f64b-233">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-236">Идентификатор пула ресурсов, из которого был выделен ресурс.</span><span class="sxs-lookup"><span data-stu-id="3f64b-236">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="3f64b-237">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-238">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="3f64b-238">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-239">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f64b-239">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-241">Объем ресурсов ЦП, зарезервированных для использования виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="3f64b-241">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="3f64b-242">Эти ресурсы гарантированно доступны для использования виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="3f64b-242">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="3f64b-243">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-244">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="3f64b-244">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-245">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-247">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="3f64b-247">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="3f64b-248">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f64b-248">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="3f64b-249">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-250">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3f64b-250">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-251">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f64b-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-253">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="3f64b-253">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="3f64b-254">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-255">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="3f64b-255">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-256">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f64b-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-258">Общее число ядер в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="3f64b-258">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="3f64b-259">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-260">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="3f64b-260">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f64b-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-263">Задает единицу измерения для свойства **виртуалкуантити** .</span><span class="sxs-lookup"><span data-stu-id="3f64b-263">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="3f64b-264">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3f64b-264">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="3f64b-265">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-265">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3f64b-266">**врамсизебитес**</span><span class="sxs-lookup"><span data-stu-id="3f64b-266">**VRAMSizeBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-267">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3f64b-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-268">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3f64b-268">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-269">Размер видеопамяти для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3f64b-269">The video memory size for the Virtual Machine.</span></span>

> [!Note]  
> <span data-ttu-id="3f64b-270">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="3f64b-270">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>



 <span data-ttu-id="3f64b-271">(67108864)</span><span class="sxs-lookup"><span data-stu-id="3f64b-271">(67108864)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3f64b-272">(134217728)</span><span class="sxs-lookup"><span data-stu-id="3f64b-272">(134217728)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3f64b-273">(268435456)</span><span class="sxs-lookup"><span data-stu-id="3f64b-273">(268435456)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3f64b-274">(536870912)</span><span class="sxs-lookup"><span data-stu-id="3f64b-274">(536870912)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3f64b-275">(1073741824)</span><span class="sxs-lookup"><span data-stu-id="3f64b-275">(1073741824)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f64b-276">**Weight**</span><span class="sxs-lookup"><span data-stu-id="3f64b-276">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f64b-277">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3f64b-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3f64b-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f64b-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f64b-279">Целое число, определяющее вес каждого процессора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3f64b-279">An integer that defines the weight for each virtual machine processor.</span></span> <span data-ttu-id="3f64b-280">После выполнения всех резервов оставшийся объем физического процессора платформы размещения будет выделен виртуальным машинам на основе их относительного веса.</span><span class="sxs-lookup"><span data-stu-id="3f64b-280">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="3f64b-281">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3f64b-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="3f64b-282">0</span><span class="sxs-lookup"><span data-stu-id="3f64b-282">0</span></span>

<span data-ttu-id="3f64b-283">Диапазон: 0 1000</span><span class="sxs-lookup"><span data-stu-id="3f64b-283">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f64b-284">Требования</span><span class="sxs-lookup"><span data-stu-id="3f64b-284">Requirements</span></span>



| <span data-ttu-id="3f64b-285">Требование</span><span class="sxs-lookup"><span data-stu-id="3f64b-285">Requirement</span></span> | <span data-ttu-id="3f64b-286">Значение</span><span class="sxs-lookup"><span data-stu-id="3f64b-286">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f64b-287">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f64b-287">Minimum supported client</span></span><br/> | <span data-ttu-id="3f64b-288">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3f64b-288">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3f64b-289">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f64b-289">Minimum supported server</span></span><br/> | <span data-ttu-id="3f64b-290">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3f64b-290">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f64b-291">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3f64b-291">Namespace</span></span><br/>                | <span data-ttu-id="3f64b-292">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3f64b-292">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3f64b-293">MOF</span><span class="sxs-lookup"><span data-stu-id="3f64b-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f64b-294"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f64b-294"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f64b-295">DLL</span><span class="sxs-lookup"><span data-stu-id="3f64b-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f64b-296"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f64b-296"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

