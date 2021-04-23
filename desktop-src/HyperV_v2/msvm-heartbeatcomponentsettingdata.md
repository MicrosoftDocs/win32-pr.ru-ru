---
description: Представляет настроенное состояние службы пульса.
ms.assetid: 2946FA02-A751-4576-BB8A-004C80E21E5B
title: Класс Msvm_HeartbeatComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponentSettingData
- Msvm_HeartbeatComponentSettingData.InstanceID
- Msvm_HeartbeatComponentSettingData.Caption
- Msvm_HeartbeatComponentSettingData.Description
- Msvm_HeartbeatComponentSettingData.ElementName
- Msvm_HeartbeatComponentSettingData.ResourceType
- Msvm_HeartbeatComponentSettingData.OtherResourceType
- Msvm_HeartbeatComponentSettingData.ResourceSubType
- Msvm_HeartbeatComponentSettingData.PoolID
- Msvm_HeartbeatComponentSettingData.ConsumerVisibility
- Msvm_HeartbeatComponentSettingData.HostResource
- Msvm_HeartbeatComponentSettingData.AllocationUnits
- Msvm_HeartbeatComponentSettingData.VirtualQuantity
- Msvm_HeartbeatComponentSettingData.Reservation
- Msvm_HeartbeatComponentSettingData.Limit
- Msvm_HeartbeatComponentSettingData.Weight
- Msvm_HeartbeatComponentSettingData.AutomaticAllocation
- Msvm_HeartbeatComponentSettingData.AutomaticDeallocation
- Msvm_HeartbeatComponentSettingData.Parent
- Msvm_HeartbeatComponentSettingData.Connection
- Msvm_HeartbeatComponentSettingData.Address
- Msvm_HeartbeatComponentSettingData.MappingBehavior
- Msvm_HeartbeatComponentSettingData.AddressOnParent
- Msvm_HeartbeatComponentSettingData.VirtualQuantityUnits
- Msvm_HeartbeatComponentSettingData.EnabledState
- Msvm_HeartbeatComponentSettingData.ErrorThreshold
- Msvm_HeartbeatComponentSettingData.Interval
- Msvm_HeartbeatComponentSettingData.Latency
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a36afbd8ab17a3fc2dfddb99b0a648fddbada415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682855"
---
# <a name="msvm_heartbeatcomponentsettingdata-class"></a><span data-ttu-id="34785-103">\_Класс мсвм хеартбеаткомпонентсеттингдата</span><span class="sxs-lookup"><span data-stu-id="34785-103">Msvm\_HeartbeatComponentSettingData class</span></span>

<span data-ttu-id="34785-104">Представляет настроенное состояние службы пульса.</span><span class="sxs-lookup"><span data-stu-id="34785-104">Represents the configured state of the heartbeat service.</span></span>

<span data-ttu-id="34785-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="34785-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="34785-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34785-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Heartbeat";
  string  Description = "Microsoft Heartbeat Service Setting Data";
  string  ElementName = "Heartbeat";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft Heartbeat Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Integration Components";
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
  uint32  ErrorThreshold = 2;
  uint32  Interval = 2000;
  uint32  Latency = 1000;
};
```

## <a name="members"></a><span data-ttu-id="34785-107">Члены</span><span class="sxs-lookup"><span data-stu-id="34785-107">Members</span></span>

<span data-ttu-id="34785-108">Класс **мсвм \_ хеартбеаткомпонентсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="34785-108">The **Msvm\_HeartbeatComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="34785-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="34785-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34785-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="34785-110">Properties</span></span>

<span data-ttu-id="34785-111">Класс **мсвм \_ хеартбеаткомпонентсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="34785-111">The **Msvm\_HeartbeatComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34785-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="34785-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="34785-115">The address of the resource.</span></span> <span data-ttu-id="34785-116">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="34785-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34785-117">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="34785-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-120">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="34785-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="34785-121">Свойства **родительского** / **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="34785-121">The **Parent**/**AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="34785-122">Например, если родительским объектом является контроллер PCI, в этом свойстве будет указан слот PCI этого дочернего устройства.</span><span class="sxs-lookup"><span data-stu-id="34785-122">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span> <span data-ttu-id="34785-123">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="34785-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34785-124">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="34785-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-127">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="34785-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="34785-128">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение "интеграционные компоненты".</span><span class="sxs-lookup"><span data-stu-id="34785-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Integration Components".</span></span>

</dd> <dt>

<span data-ttu-id="34785-129">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="34785-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-130">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="34785-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34785-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-132">Указывает, выделяется ли ресурс автоматически.</span><span class="sxs-lookup"><span data-stu-id="34785-132">Indicates whether the resource is automatically allocated.</span></span> <span data-ttu-id="34785-133">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="34785-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="34785-134">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="34785-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-135">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="34785-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34785-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-137">Указывает, освобождается ли ресурс автоматически.</span><span class="sxs-lookup"><span data-stu-id="34785-137">Indicates whether the resource is automatically de-allocated.</span></span> <span data-ttu-id="34785-138">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="34785-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="34785-139">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="34785-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-142">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="34785-142">A short description of the object.</span></span> <span data-ttu-id="34785-143">Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и всегда имеет значение "Пульс".</span><span class="sxs-lookup"><span data-stu-id="34785-143">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="34785-144">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="34785-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-145">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="34785-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="34785-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-147">Объект, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="34785-147">The thing to which this resource is connected.</span></span> <span data-ttu-id="34785-148">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="34785-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34785-149">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="34785-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-150">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34785-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34785-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-152">Описание видимости потребителей для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="34785-152">Describes the consumers' visibility to the allocated resource.</span></span> <span data-ttu-id="34785-153">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение 3 (виртуализированное).</span><span class="sxs-lookup"><span data-stu-id="34785-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="34785-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="34785-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-157">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="34785-157">A description of the object.</span></span> <span data-ttu-id="34785-158">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "данные параметра службы пульса Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="34785-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="34785-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="34785-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-162">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="34785-162">A display name for the object.</span></span> <span data-ttu-id="34785-163">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение "Пульс".</span><span class="sxs-lookup"><span data-stu-id="34785-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Heartbeat".</span></span> <span data-ttu-id="34785-164">Изменение этого свойства приведет к изменению свойства **ElementName** связанного производного класса [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .</span><span class="sxs-lookup"><span data-stu-id="34785-164">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="34785-165">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="34785-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="34785-166">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="34785-166">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34785-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34785-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-169">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="34785-169">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="34785-170">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="34785-170">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="34785-171">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="34785-171">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="34785-172">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="34785-172">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34785-173">**еррорсрешолд**</span><span class="sxs-lookup"><span data-stu-id="34785-173">**ErrorThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-174">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34785-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34785-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-176">Конфигурация запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="34785-176">An administrator's startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="34785-177">Это свойство всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="34785-177">This property is always set to 2 (Enabled).</span></span>

<span data-ttu-id="34785-178">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="34785-178">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="34785-179">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="34785-179">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-180">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="34785-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="34785-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-182">Предоставляет определенное назначение для размещения или базовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34785-182">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="34785-183">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="34785-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34785-184">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="34785-184">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34785-187">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="34785-187">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="34785-188">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="34785-188">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="34785-189">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)) и всегда имеет значение "Microsoft:*GUID* \\ *девицеспеЦификдата*".</span><span class="sxs-lookup"><span data-stu-id="34785-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="34785-190">**Интервал**</span><span class="sxs-lookup"><span data-stu-id="34785-190">**Interval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-191">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34785-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34785-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-193">Интервал (в миллисекундах) между попытками проверки связи.</span><span class="sxs-lookup"><span data-stu-id="34785-193">The interval, in milliseconds, between ping attempts.</span></span> <span data-ttu-id="34785-194">Всегда имеет значение 2000.</span><span class="sxs-lookup"><span data-stu-id="34785-194">This is always set to 2000.</span></span>

<span data-ttu-id="34785-195">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="34785-195">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="34785-196">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="34785-196">**Latency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-197">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34785-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34785-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-199">Максимальная ожидаемая задержка (в миллисекундах) между запросом проверки связи и ответом до того, как данный запрос считается удаленным.</span><span class="sxs-lookup"><span data-stu-id="34785-199">The maximum expected latency, in milliseconds, between a request ping and a response before a given request is considered dropped.</span></span> <span data-ttu-id="34785-200">Это свойство всегда имеет значение 1000.</span><span class="sxs-lookup"><span data-stu-id="34785-200">This property is always set to 1000.</span></span>

<span data-ttu-id="34785-201">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="34785-201">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="34785-202">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="34785-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-203">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34785-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34785-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-205">Верхняя граница или максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="34785-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="34785-206">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="34785-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="34785-207">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="34785-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34785-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34785-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-210">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="34785-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="34785-211">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="34785-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34785-212">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="34785-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-215">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а свойство **ResourceType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="34785-215">A string that describes the resource type when a well-defined value is not available and the **ResourceType** property has the value 1 (Other).</span></span> <span data-ttu-id="34785-216">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение "компонент пульса Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="34785-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Microsoft Heartbeat Component".</span></span>

</dd> <dt>

<span data-ttu-id="34785-217">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="34785-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-220">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="34785-220">The parent of the resource.</span></span> <span data-ttu-id="34785-221">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="34785-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34785-222">**пулид**</span><span class="sxs-lookup"><span data-stu-id="34785-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-225">Идентификатор пула ресурсов, из которого выделяется ресурс.</span><span class="sxs-lookup"><span data-stu-id="34785-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="34785-226">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="34785-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="34785-227">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="34785-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-228">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34785-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34785-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-230">Объем ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="34785-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="34785-231">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="34785-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="34785-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="34785-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-233">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-235">Конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="34785-235">An implementation specific subtype for this resource.</span></span> <span data-ttu-id="34785-236">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="34785-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="34785-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="34785-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-238">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34785-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34785-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-240">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="34785-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="34785-241">Это свойство наследуется от класса [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="34785-241">This property is inherited from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class and is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="34785-242">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="34785-242">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-243">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34785-243">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34785-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-245">Количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="34785-245">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="34785-246">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="34785-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="34785-247">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="34785-247">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="34785-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34785-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-250">Указывает единицы, используемые свойством **виртуалкуантити** .</span><span class="sxs-lookup"><span data-stu-id="34785-250">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="34785-251">Например, если ResourceType = Processor, значение свойства **виртуалкуантитюнитс** может быть равно "Count", что означает, что значение свойства **виртуалкуантити** выражается как число.</span><span class="sxs-lookup"><span data-stu-id="34785-251">For example, if ResourceType=Processor, the value of the **VirtualQuantityUnits** property can be set to "count", indicating that the value of the **VirtualQuantity** property is expressed as a count.</span></span> <span data-ttu-id="34785-252">Если ResourceType = Memory, значение свойства **виртуалкуантитюнитс** может быть равно "bytes \* 10 ^ 3", что означает, что значение свойства **виртуалкуантити** выражается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="34785-252">If ResourceType=Memory, the value of the **VirtualQuantityUnits** property can be set to "bytes\*10^3", indicating that the value of the **VirtualQuantity** property is expressed in kilobytes.</span></span> <span data-ttu-id="34785-253">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение "Count".</span><span class="sxs-lookup"><span data-stu-id="34785-253">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "count".</span></span>

</dd> <dt>

<span data-ttu-id="34785-254">**Weight**</span><span class="sxs-lookup"><span data-stu-id="34785-254">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34785-255">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34785-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34785-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="34785-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34785-257">Относительный приоритет для этого выделения относительно других выделений из того же пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34785-257">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="34785-258">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="34785-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34785-259">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34785-259">Remarks</span></span>

<span data-ttu-id="34785-260">Доступ к классу **\_ хеартбеаткомпонентсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="34785-260">Access to the **Msvm\_HeartbeatComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="34785-261">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="34785-261">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="34785-262">Требования</span><span class="sxs-lookup"><span data-stu-id="34785-262">Requirements</span></span>



| <span data-ttu-id="34785-263">Требование</span><span class="sxs-lookup"><span data-stu-id="34785-263">Requirement</span></span> | <span data-ttu-id="34785-264">Значение</span><span class="sxs-lookup"><span data-stu-id="34785-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34785-265">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34785-265">Minimum supported client</span></span><br/> | <span data-ttu-id="34785-266">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="34785-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="34785-267">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34785-267">Minimum supported server</span></span><br/> | <span data-ttu-id="34785-268">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="34785-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34785-269">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="34785-269">Namespace</span></span><br/>                | <span data-ttu-id="34785-270">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="34785-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="34785-271">MOF</span><span class="sxs-lookup"><span data-stu-id="34785-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34785-272"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34785-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34785-273">DLL</span><span class="sxs-lookup"><span data-stu-id="34785-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34785-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34785-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="34785-275">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34785-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34785-276">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="34785-276">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="34785-277">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="34785-277">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="34785-278">**Мсвм \_ хеартбеаткомпонентсеттингдата**</span><span class="sxs-lookup"><span data-stu-id="34785-278">**Msvm\_HeartbeatComponentSettingData**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponentsettingdata)
</dt> </dl>

 

