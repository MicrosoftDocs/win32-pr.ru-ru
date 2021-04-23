---
description: Представляет настроенное состояние компонента удаленный рабочий стол Virtualization (RDV). Состояние по умолчанию — Enabled.
ms.assetid: 058432d7-4439-47ec-9909-82a405d69a6e
title: Класс Msvm_RdvComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponentSettingData
- Msvm_RdvComponentSettingData.InstanceID
- Msvm_RdvComponentSettingData.Caption
- Msvm_RdvComponentSettingData.Description
- Msvm_RdvComponentSettingData.ElementName
- Msvm_RdvComponentSettingData.ResourceType
- Msvm_RdvComponentSettingData.OtherResourceType
- Msvm_RdvComponentSettingData.ResourceSubType
- Msvm_RdvComponentSettingData.PoolID
- Msvm_RdvComponentSettingData.ConsumerVisibility
- Msvm_RdvComponentSettingData.HostResource
- Msvm_RdvComponentSettingData.AllocationUnits
- Msvm_RdvComponentSettingData.VirtualQuantity
- Msvm_RdvComponentSettingData.Reservation
- Msvm_RdvComponentSettingData.Limit
- Msvm_RdvComponentSettingData.Weight
- Msvm_RdvComponentSettingData.AutomaticAllocation
- Msvm_RdvComponentSettingData.AutomaticDeallocation
- Msvm_RdvComponentSettingData.Parent
- Msvm_RdvComponentSettingData.Connection
- Msvm_RdvComponentSettingData.Address
- Msvm_RdvComponentSettingData.MappingBehavior
- Msvm_RdvComponentSettingData.AddressOnParent
- Msvm_RdvComponentSettingData.VirtualQuantityUnits
- Msvm_RdvComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfc8decda2bf0c505331c9d681069d55f40687f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910144"
---
# <a name="msvm_rdvcomponentsettingdata-class"></a><span data-ttu-id="a51e1-104">\_Класс мсвм рдвкомпонентсеттингдата</span><span class="sxs-lookup"><span data-stu-id="a51e1-104">Msvm\_RdvComponentSettingData class</span></span>

<span data-ttu-id="a51e1-105">Представляет настроенное состояние компонента удаленный рабочий стол Virtualization (RDV).</span><span class="sxs-lookup"><span data-stu-id="a51e1-105">Represents the configured state of the Remote Desktop Virtualization (RDV) component.</span></span> <span data-ttu-id="a51e1-106">Состояние по умолчанию — Enabled.</span><span class="sxs-lookup"><span data-stu-id="a51e1-106">The default state is Enabled.</span></span>

<span data-ttu-id="a51e1-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a51e1-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a51e1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a51e1-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Remote Desktop Virtualization Service Default Settings";
  string  Description = "Describes the default settings for the Remote Desktop Virtualization Service resources.";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
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
  uint16  EnabledState = 2;
};
```

## <a name="members"></a><span data-ttu-id="a51e1-109">Члены</span><span class="sxs-lookup"><span data-stu-id="a51e1-109">Members</span></span>

<span data-ttu-id="a51e1-110">Класс **мсвм \_ рдвкомпонентсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a51e1-110">The **Msvm\_RdvComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a51e1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a51e1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a51e1-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a51e1-112">Properties</span></span>

<span data-ttu-id="a51e1-113">Класс **мсвм \_ рдвкомпонентсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a51e1-113">The **Msvm\_RdvComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a51e1-114">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="a51e1-114">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-117">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="a51e1-117">The address of the resource.</span></span> <span data-ttu-id="a51e1-118">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-118">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-119">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="a51e1-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-122">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="a51e1-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="a51e1-123">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="a51e1-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="a51e1-124">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-125">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="a51e1-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-128">Единица распределения, используемая свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="a51e1-128">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="a51e1-129">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-130">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="a51e1-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-131">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a51e1-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-133">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="a51e1-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="a51e1-134">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-135">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="a51e1-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-136">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a51e1-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-138">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="a51e1-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="a51e1-139">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-140">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a51e1-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-143">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="a51e1-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-144">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a51e1-144">A short description of the object.</span></span> <span data-ttu-id="a51e1-145">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="a51e1-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-146">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="a51e1-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-147">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a51e1-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-149">Устройство, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="a51e1-149">The device to which this resource is connected.</span></span> <span data-ttu-id="a51e1-150">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-151">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="a51e1-151">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-152">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a51e1-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-154">Видимость потребителя для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="a51e1-154">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="a51e1-155">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 3 (виртуализированное).</span><span class="sxs-lookup"><span data-stu-id="a51e1-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-156">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a51e1-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-159">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a51e1-159">A description of the object.</span></span> <span data-ttu-id="a51e1-160">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="a51e1-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-161">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a51e1-161">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-164">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="a51e1-164">A display name for the object.</span></span> <span data-ttu-id="a51e1-165">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a51e1-165">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="a51e1-166">Изменение этого свойства приведет к изменению имени элемента связанного логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a51e1-166">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a51e1-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a51e1-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-170">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="a51e1-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a51e1-171">Допустимые значения: 2 (включено) и 3 (отключено).</span><span class="sxs-lookup"><span data-stu-id="a51e1-171">Valid values are 2 (enabled) and 3 (disabled).</span></span> <span data-ttu-id="a51e1-172">Значение по умолчанию — 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="a51e1-172">The default value is 2 (enabled).</span></span> <span data-ttu-id="a51e1-173">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифивиртуалсистемресаурцес**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a51e1-173">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-174">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="a51e1-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-175">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a51e1-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-177">Каждому устройству в виртуальном коммутаторе можно назначить только один ресурс узла, поэтому можно установить только первый элемент этого массива.</span><span class="sxs-lookup"><span data-stu-id="a51e1-177">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="a51e1-178">Для устройств, поддерживающих эту функцию, установите первый элемент массива **хостресаурце** , чтобы он содержал ссылку на базовый ресурс узла, который нужно назначить.</span><span class="sxs-lookup"><span data-stu-id="a51e1-178">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="a51e1-179">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-179">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a51e1-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-183">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="a51e1-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-184">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="a51e1-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a51e1-185">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a51e1-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-186">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="a51e1-186">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-187">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a51e1-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-189">Максимальный объем соответствующих ресурсов узла, которые могут использоваться виртуальным коммутатором.</span><span class="sxs-lookup"><span data-stu-id="a51e1-189">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="a51e1-190">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-191">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="a51e1-191">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-192">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a51e1-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-194">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="a51e1-194">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="a51e1-195">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-196">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="a51e1-196">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-199">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а [**ResourceType**](msvm-processorsettingdata.md) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="a51e1-199">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="a51e1-200">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и не используется.</span><span class="sxs-lookup"><span data-stu-id="a51e1-200">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-201">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="a51e1-201">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-204">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="a51e1-204">The parent of the resource.</span></span> <span data-ttu-id="a51e1-205">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-205">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-206">**пулид**</span><span class="sxs-lookup"><span data-stu-id="a51e1-206">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-209">Идентификатор пула ресурсов, из которого был выделен ресурс.</span><span class="sxs-lookup"><span data-stu-id="a51e1-209">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="a51e1-210">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-211">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="a51e1-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-212">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a51e1-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-214">Объем ресурсов, зарезервированных для использования виртуальным коммутатором.</span><span class="sxs-lookup"><span data-stu-id="a51e1-214">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="a51e1-215">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-215">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-216">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="a51e1-216">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-219">Строка, описывающая подтип для этого ресурса, зависящий от реализации.</span><span class="sxs-lookup"><span data-stu-id="a51e1-219">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="a51e1-220">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a51e1-220">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="a51e1-221">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="a51e1-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-223">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a51e1-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-225">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="a51e1-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="a51e1-226">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 33 (подключение Ethernet).</span><span class="sxs-lookup"><span data-stu-id="a51e1-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-227">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="a51e1-227">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-228">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a51e1-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-230">Общее число портов в виртуальном коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="a51e1-230">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="a51e1-231">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-232">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="a51e1-232">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-233">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a51e1-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-235">Задает единицу измерения для свойства **виртуалкуантити** .</span><span class="sxs-lookup"><span data-stu-id="a51e1-235">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="a51e1-236">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a51e1-236">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="a51e1-237">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a51e1-238">**Weight**</span><span class="sxs-lookup"><span data-stu-id="a51e1-238">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a51e1-239">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a51e1-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a51e1-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a51e1-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a51e1-241">Целое число, определяющее вес для каждого виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="a51e1-241">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="a51e1-242">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a51e1-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="a51e1-243">Диапазон: 0 1000</span><span class="sxs-lookup"><span data-stu-id="a51e1-243">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a51e1-244">Требования</span><span class="sxs-lookup"><span data-stu-id="a51e1-244">Requirements</span></span>



| <span data-ttu-id="a51e1-245">Требование</span><span class="sxs-lookup"><span data-stu-id="a51e1-245">Requirement</span></span> | <span data-ttu-id="a51e1-246">Значение</span><span class="sxs-lookup"><span data-stu-id="a51e1-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a51e1-247">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a51e1-247">Minimum supported client</span></span><br/> | <span data-ttu-id="a51e1-248">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a51e1-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a51e1-249">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a51e1-249">Minimum supported server</span></span><br/> | <span data-ttu-id="a51e1-250">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a51e1-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a51e1-251">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a51e1-251">Namespace</span></span><br/>                | <span data-ttu-id="a51e1-252">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a51e1-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a51e1-253">MOF</span><span class="sxs-lookup"><span data-stu-id="a51e1-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a51e1-254"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a51e1-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a51e1-255">DLL</span><span class="sxs-lookup"><span data-stu-id="a51e1-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a51e1-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a51e1-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

