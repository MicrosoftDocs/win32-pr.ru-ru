---
description: Представляет настроенное состояние искусственного Fibre Channel порта или порта коммутатора Fibre Channel.
ms.assetid: 680badc4-8dba-47e8-859a-0ed472a15eda
title: Класс Msvm_FcPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcPortAllocationSettingData
- Msvm_FcPortAllocationSettingData.InstanceID
- Msvm_FcPortAllocationSettingData.Caption
- Msvm_FcPortAllocationSettingData.Description
- Msvm_FcPortAllocationSettingData.ElementName
- Msvm_FcPortAllocationSettingData.ResourceType
- Msvm_FcPortAllocationSettingData.OtherResourceType
- Msvm_FcPortAllocationSettingData.ResourceSubType
- Msvm_FcPortAllocationSettingData.PoolID
- Msvm_FcPortAllocationSettingData.ConsumerVisibility
- Msvm_FcPortAllocationSettingData.HostResource
- Msvm_FcPortAllocationSettingData.AllocationUnits
- Msvm_FcPortAllocationSettingData.VirtualQuantity
- Msvm_FcPortAllocationSettingData.Reservation
- Msvm_FcPortAllocationSettingData.Limit
- Msvm_FcPortAllocationSettingData.Weight
- Msvm_FcPortAllocationSettingData.AutomaticAllocation
- Msvm_FcPortAllocationSettingData.AutomaticDeallocation
- Msvm_FcPortAllocationSettingData.Parent
- Msvm_FcPortAllocationSettingData.Connection
- Msvm_FcPortAllocationSettingData.Address
- Msvm_FcPortAllocationSettingData.MappingBehavior
- Msvm_FcPortAllocationSettingData.AddressOnParent
- Msvm_FcPortAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 824f7077eeb3cb9e00ce8733cb5d2f57761716e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682863"
---
# <a name="msvm_fcportallocationsettingdata-class"></a><span data-ttu-id="5da10-103">\_Класс мсвм фкпорталлокатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="5da10-103">Msvm\_FcPortAllocationSettingData class</span></span>

<span data-ttu-id="5da10-104">Представляет настроенное состояние искусственного Fibre Channel порта или порта коммутатора Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="5da10-104">Represents the configured state of a synthetic Fibre Channel port or a Fibre Channel switch port.</span></span>

<span data-ttu-id="5da10-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5da10-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da10-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5da10-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel VDev Default Settings";
  string  Description = "The default settings for the virtual Fibre Channel connection pool.";
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
};
```

## <a name="members"></a><span data-ttu-id="5da10-107">Члены</span><span class="sxs-lookup"><span data-stu-id="5da10-107">Members</span></span>

<span data-ttu-id="5da10-108">Класс **мсвм \_ фкпорталлокатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5da10-108">The **Msvm\_FcPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5da10-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="5da10-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5da10-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5da10-110">Properties</span></span>

<span data-ttu-id="5da10-111">Класс **мсвм \_ фкпорталлокатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5da10-111">The **Msvm\_FcPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5da10-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="5da10-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="5da10-115">The address of the resource.</span></span> <span data-ttu-id="5da10-116">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-117">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="5da10-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-120">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="5da10-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="5da10-121">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="5da10-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="5da10-122">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-123">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="5da10-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-126">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="5da10-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="5da10-127">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-128">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="5da10-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5da10-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-131">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="5da10-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="5da10-132">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-133">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="5da10-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5da10-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-136">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="5da10-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="5da10-137">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="5da10-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5da10-141">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="5da10-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="5da10-142">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5da10-142">A short description of the object.</span></span> <span data-ttu-id="5da10-143">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5da10-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-144">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="5da10-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-145">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="5da10-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5da10-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-147">Устройство, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="5da10-147">The device to which this resource is connected.</span></span> <span data-ttu-id="5da10-148">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-149">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="5da10-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-150">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5da10-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-152">Видимость потребителя для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="5da10-152">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="5da10-153">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5da10-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-157">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5da10-157">A description of the object.</span></span> <span data-ttu-id="5da10-158">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5da10-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5da10-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-162">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="5da10-162">A display name for the object.</span></span> <span data-ttu-id="5da10-163">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5da10-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="5da10-164">Изменение этого свойства приведет к изменению имени элемента связанного логического устройства.</span><span class="sxs-lookup"><span data-stu-id="5da10-164">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="5da10-165">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5da10-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="5da10-166">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="5da10-166">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-167">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="5da10-167">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5da10-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-169">Каждому устройству на виртуальной машине можно назначить только один ресурс узла, поэтому можно установить только первый элемент этого массива.</span><span class="sxs-lookup"><span data-stu-id="5da10-169">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="5da10-170">Для устройств, поддерживающих эту функцию, установите первый элемент массива **хостресаурце** , чтобы он содержал ссылку на базовый ресурс узла, который нужно назначить.</span><span class="sxs-lookup"><span data-stu-id="5da10-170">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="5da10-171">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-171">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="5da10-172">Это свойство только для чтения, но если свойство **ResourceType** имеет значение 22 (диск), а свойство **ресаурцесубтипе** имеет значение "физический диск (Майкрософт)", то его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5da10-172">This is a read-only property, but if the **ResourceType** property is 22 (Disk) and the **ResourceSubType** property is "Microsoft Physical Disk Drive", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="5da10-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5da10-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5da10-176">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="5da10-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5da10-177">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="5da10-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5da10-178">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5da10-178">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-179">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="5da10-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-180">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5da10-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-182">Максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="5da10-182">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="5da10-183">Единица измерения для этого свойства задается свойством **виртуалкуантитюнитс** .</span><span class="sxs-lookup"><span data-stu-id="5da10-183">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="5da10-184">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-184">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-185">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="5da10-185">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-186">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5da10-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-188">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="5da10-188">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="5da10-189">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-190">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="5da10-190">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-193">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а [**ResourceType**](msvm-processorsettingdata.md) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="5da10-193">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="5da10-194">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-195">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="5da10-195">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-198">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="5da10-198">The parent of the resource.</span></span> <span data-ttu-id="5da10-199">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-200">**пулид**</span><span class="sxs-lookup"><span data-stu-id="5da10-200">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-203">Идентификатор пула ресурсов, из которого был выделен ресурс.</span><span class="sxs-lookup"><span data-stu-id="5da10-203">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="5da10-204">Для экземпляров, связанных с виртуальной машиной, это будет «Microsoft:*GUID* \\ *-данные устройства*».</span><span class="sxs-lookup"><span data-stu-id="5da10-204">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="5da10-205">Для экземпляров, определяющих потенциальные параметры виртуальной машины, это будет "Microsoft: определение \\  \\ *типа* GUID", где *тип* может быть одним из значений: "максимум", "минимум", "default" или "Increment".</span><span class="sxs-lookup"><span data-stu-id="5da10-205">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="5da10-206">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-207">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="5da10-207">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-208">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5da10-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-210">Объем ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="5da10-210">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="5da10-211">Единица измерения для этого свойства задается свойством **виртуалкуантитюнитс** .</span><span class="sxs-lookup"><span data-stu-id="5da10-211">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="5da10-212">Эти ресурсы гарантированно доступны для использования виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="5da10-212">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="5da10-213">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="5da10-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-217">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="5da10-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="5da10-218">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5da10-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="5da10-219">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="5da10-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-221">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5da10-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-223">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="5da10-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="5da10-224">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="5da10-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="5da10-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Компьютерная система** (2)</span><span class="sxs-lookup"><span data-stu-id="5da10-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Процессор** (3)</span><span class="sxs-lookup"><span data-stu-id="5da10-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Память** (4)</span><span class="sxs-lookup"><span data-stu-id="5da10-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-контроллер** (5)</span><span class="sxs-lookup"><span data-stu-id="5da10-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Параллельный SCSI HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="5da10-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**Адаптер шины FC** (7)</span><span class="sxs-lookup"><span data-stu-id="5da10-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**адаптер шины iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="5da10-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**Геохка** (9)</span><span class="sxs-lookup"><span data-stu-id="5da10-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-адаптер** (10)</span><span class="sxs-lookup"><span data-stu-id="5da10-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Другой сетевой адаптер** (11)</span><span class="sxs-lookup"><span data-stu-id="5da10-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Разъем ввода-вывода** (12)</span><span class="sxs-lookup"><span data-stu-id="5da10-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Устройство ввода-вывода** (13)</span><span class="sxs-lookup"><span data-stu-id="5da10-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>Дисковод **гибких дисков** (14)</span><span class="sxs-lookup"><span data-stu-id="5da10-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Дисковод компакт-дисков** (15)</span><span class="sxs-lookup"><span data-stu-id="5da10-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-дисковод** (16)</span><span class="sxs-lookup"><span data-stu-id="5da10-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Последовательный порт** (17)</span><span class="sxs-lookup"><span data-stu-id="5da10-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Параллельный порт** (18)</span><span class="sxs-lookup"><span data-stu-id="5da10-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-контроллер** (19)</span><span class="sxs-lookup"><span data-stu-id="5da10-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Графический контроллер** (20)</span><span class="sxs-lookup"><span data-stu-id="5da10-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Область хранения** (21)</span><span class="sxs-lookup"><span data-stu-id="5da10-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Диск** (22)</span><span class="sxs-lookup"><span data-stu-id="5da10-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Лента** (23)</span><span class="sxs-lookup"><span data-stu-id="5da10-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Другое запоминающее устройство** (24)</span><span class="sxs-lookup"><span data-stu-id="5da10-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Контроллер FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="5da10-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Единица секционирования** (26)</span><span class="sxs-lookup"><span data-stu-id="5da10-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Базовая единица секционирования** (27)</span><span class="sxs-lookup"><span data-stu-id="5da10-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Источник питания** (28)</span><span class="sxs-lookup"><span data-stu-id="5da10-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Охлаждающее устройство** (29)</span><span class="sxs-lookup"><span data-stu-id="5da10-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="5da10-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="5da10-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="5da10-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5da10-256">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="5da10-256">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-257">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5da10-257">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-259">Указывает количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="5da10-259">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="5da10-260">Единица измерения для этого свойства задается свойством **виртуалкуантитюнитс** .</span><span class="sxs-lookup"><span data-stu-id="5da10-260">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="5da10-261">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-262">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="5da10-262">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5da10-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-265">Задает единицу измерения для этого выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5da10-265">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="5da10-266">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5da10-266">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="5da10-267">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5da10-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5da10-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5da10-269">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5da10-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5da10-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5da10-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5da10-271">Целое число, определяющее относительный вес для каждого процессора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5da10-271">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="5da10-272">После выполнения всех резервов оставшийся объем физического процессора платформы размещения будет выделен виртуальным машинам на основе их относительного веса.</span><span class="sxs-lookup"><span data-stu-id="5da10-272">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="5da10-273">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="5da10-273">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="5da10-274">Диапазон: 0 1000</span><span class="sxs-lookup"><span data-stu-id="5da10-274">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5da10-275">Требования</span><span class="sxs-lookup"><span data-stu-id="5da10-275">Requirements</span></span>



| <span data-ttu-id="5da10-276">Требование</span><span class="sxs-lookup"><span data-stu-id="5da10-276">Requirement</span></span> | <span data-ttu-id="5da10-277">Значение</span><span class="sxs-lookup"><span data-stu-id="5da10-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da10-278">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5da10-278">Minimum supported client</span></span><br/> | <span data-ttu-id="5da10-279">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5da10-279">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5da10-280">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5da10-280">Minimum supported server</span></span><br/> | <span data-ttu-id="5da10-281">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5da10-281">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5da10-282">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5da10-282">Namespace</span></span><br/>                | <span data-ttu-id="5da10-283">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5da10-283">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5da10-284">MOF</span><span class="sxs-lookup"><span data-stu-id="5da10-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5da10-285"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5da10-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5da10-286">DLL</span><span class="sxs-lookup"><span data-stu-id="5da10-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5da10-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5da10-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

