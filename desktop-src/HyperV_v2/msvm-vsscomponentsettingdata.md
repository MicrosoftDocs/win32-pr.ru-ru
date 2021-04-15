---
description: Представляет настроенное состояние службы служба теневого копирования томов (VSS).
ms.assetid: FAE8E8F7-525A-4E5A-91B3-B73343337352
title: Класс Msvm_VssComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponentSettingData
- Msvm_VssComponentSettingData.InstanceID
- Msvm_VssComponentSettingData.Caption
- Msvm_VssComponentSettingData.Description
- Msvm_VssComponentSettingData.ElementName
- Msvm_VssComponentSettingData.ResourceType
- Msvm_VssComponentSettingData.OtherResourceType
- Msvm_VssComponentSettingData.ResourceSubType
- Msvm_VssComponentSettingData.PoolID
- Msvm_VssComponentSettingData.ConsumerVisibility
- Msvm_VssComponentSettingData.HostResource
- Msvm_VssComponentSettingData.AllocationUnits
- Msvm_VssComponentSettingData.VirtualQuantity
- Msvm_VssComponentSettingData.Reservation
- Msvm_VssComponentSettingData.Limit
- Msvm_VssComponentSettingData.Weight
- Msvm_VssComponentSettingData.AutomaticAllocation
- Msvm_VssComponentSettingData.AutomaticDeallocation
- Msvm_VssComponentSettingData.Parent
- Msvm_VssComponentSettingData.Connection
- Msvm_VssComponentSettingData.Address
- Msvm_VssComponentSettingData.MappingBehavior
- Msvm_VssComponentSettingData.AddressOnParent
- Msvm_VssComponentSettingData.VirtualQuantityUnits
- Msvm_VssComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d37f46c10cc702c66a30fb484553a8c5da03d8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662216"
---
# <a name="msvm_vsscomponentsettingdata-class"></a><span data-ttu-id="56395-103">\_Класс мсвм всскомпонентсеттингдата</span><span class="sxs-lookup"><span data-stu-id="56395-103">Msvm\_VssComponentSettingData class</span></span>

<span data-ttu-id="56395-104">Представляет настроенное состояние службы служба теневого копирования томов (VSS).</span><span class="sxs-lookup"><span data-stu-id="56395-104">Represents the configured state of the Volume Shadow Copy Service (VSS) service.</span></span>

<span data-ttu-id="56395-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="56395-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="56395-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56395-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "VSS";
  string  Description = "Microsoft VSS Service Setting Data";
  string  ElementName = "VSS";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:VSS Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource;
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

## <a name="members"></a><span data-ttu-id="56395-107">Члены</span><span class="sxs-lookup"><span data-stu-id="56395-107">Members</span></span>

<span data-ttu-id="56395-108">Класс **мсвм \_ всскомпонентсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="56395-108">The **Msvm\_VssComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="56395-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="56395-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56395-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="56395-110">Properties</span></span>

<span data-ttu-id="56395-111">Класс **мсвм \_ всскомпонентсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="56395-111">The **Msvm\_VssComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56395-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="56395-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="56395-115">The address of the resource.</span></span> <span data-ttu-id="56395-116">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-117">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="56395-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-120">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="56395-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="56395-121">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="56395-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="56395-122">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-123">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="56395-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-126">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="56395-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="56395-127">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-128">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="56395-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="56395-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56395-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-131">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="56395-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="56395-132">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-133">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="56395-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="56395-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56395-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-136">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="56395-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="56395-137">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="56395-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-141">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="56395-141">A short description of the object.</span></span> <span data-ttu-id="56395-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="56395-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="56395-143">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="56395-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-144">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="56395-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="56395-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-146">Объект, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="56395-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="56395-147">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-148">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="56395-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56395-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56395-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-151">Пользователи могут видеть выделенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="56395-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="56395-152">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="56395-153">Значение</span><span class="sxs-lookup"><span data-stu-id="56395-153">Value</span></span>                                                                        | <span data-ttu-id="56395-154">Значение</span><span class="sxs-lookup"><span data-stu-id="56395-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="56395-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="56395-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="56395-156">Виртуализированных</span><span class="sxs-lookup"><span data-stu-id="56395-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="56395-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="56395-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-160">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="56395-160">A description of the object.</span></span> <span data-ttu-id="56395-161">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="56395-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="56395-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="56395-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-165">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="56395-165">A display name for the object.</span></span> <span data-ttu-id="56395-166">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="56395-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56395-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="56395-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56395-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56395-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-170">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="56395-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="56395-171">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и имеет значение по умолчанию 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="56395-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and has a default value of 2 (Enabled).</span></span>

<span data-ttu-id="56395-172">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="56395-172">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>



 <span data-ttu-id="56395-173">(2)</span><span class="sxs-lookup"><span data-stu-id="56395-173">(2)</span></span>


</dt> <dd>

<span data-ttu-id="56395-174">Активировано</span><span class="sxs-lookup"><span data-stu-id="56395-174">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="56395-175">3</span><span class="sxs-lookup"><span data-stu-id="56395-175">3</span></span>
</dt> <dd>

<span data-ttu-id="56395-176">Выключено</span><span class="sxs-lookup"><span data-stu-id="56395-176">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56395-177">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="56395-177">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-180">Предоставляет определенное назначение для размещения или базовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56395-180">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="56395-181">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="56395-181">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="56395-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="56395-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56395-185">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="56395-185">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="56395-186">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="56395-186">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="56395-187">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="56395-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="56395-188">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="56395-188">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-189">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="56395-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="56395-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-191">Верхняя граница или максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="56395-191">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="56395-192">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-193">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="56395-193">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-194">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56395-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56395-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-196">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="56395-196">Indicates how this resource maps to underlying resources.</span></span> <span data-ttu-id="56395-197">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-197">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-198">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="56395-198">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-201">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="56395-201">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="56395-202">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-202">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-203">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="56395-203">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-206">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="56395-206">The parent of the resource.</span></span> <span data-ttu-id="56395-207">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-208">**пулид**</span><span class="sxs-lookup"><span data-stu-id="56395-208">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-211">Идентификатор пула ресурсов, из которого выделяется ресурс.</span><span class="sxs-lookup"><span data-stu-id="56395-211">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="56395-212">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-213">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="56395-213">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-214">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="56395-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="56395-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-216">Объем ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="56395-216">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="56395-217">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="56395-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-221">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="56395-221">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="56395-222">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="56395-222">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="56395-223">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="56395-223">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-224">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56395-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56395-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-226">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="56395-226">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="56395-227">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="56395-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1 (Other).</span></span>



| <span data-ttu-id="56395-228">Значение</span><span class="sxs-lookup"><span data-stu-id="56395-228">Value</span></span>                                                                        | <span data-ttu-id="56395-229">Значение</span><span class="sxs-lookup"><span data-stu-id="56395-229">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="56395-230"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="56395-230"><dt>1</dt></span></span> </dl> | <span data-ttu-id="56395-231">Другое</span><span class="sxs-lookup"><span data-stu-id="56395-231">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="56395-232">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="56395-232">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-233">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="56395-233">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="56395-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-235">Количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="56395-235">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="56395-236">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-237">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="56395-237">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-238">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="56395-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56395-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-240">Задает единицу измерения для этого выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56395-240">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="56395-241">Значение этого свойства является допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="56395-241">The value of this property is a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="56395-242">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="56395-243">**Weight**</span><span class="sxs-lookup"><span data-stu-id="56395-243">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56395-244">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56395-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56395-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="56395-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56395-246">Относительный приоритет для этого выделения относительно других выделений из того же пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56395-246">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="56395-247">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="56395-247">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56395-248">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56395-248">Remarks</span></span>

<span data-ttu-id="56395-249">Доступ к классу **\_ всскомпонентсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="56395-249">Access to the **Msvm\_VssComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="56395-250">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="56395-250">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="56395-251">Требования</span><span class="sxs-lookup"><span data-stu-id="56395-251">Requirements</span></span>



| <span data-ttu-id="56395-252">Требование</span><span class="sxs-lookup"><span data-stu-id="56395-252">Requirement</span></span> | <span data-ttu-id="56395-253">Значение</span><span class="sxs-lookup"><span data-stu-id="56395-253">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56395-254">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56395-254">Minimum supported client</span></span><br/> | <span data-ttu-id="56395-255">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="56395-255">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="56395-256">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56395-256">Minimum supported server</span></span><br/> | <span data-ttu-id="56395-257">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="56395-257">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56395-258">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="56395-258">Namespace</span></span><br/>                | <span data-ttu-id="56395-259">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="56395-259">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="56395-260">MOF</span><span class="sxs-lookup"><span data-stu-id="56395-260">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56395-261"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56395-261"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56395-262">DLL</span><span class="sxs-lookup"><span data-stu-id="56395-262">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56395-263"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56395-263"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56395-264">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56395-264">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56395-265">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="56395-265">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="56395-266">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="56395-266">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

