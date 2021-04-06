---
description: Представляет настроенное состояние службы синхронизации времени.
ms.assetid: AACEDE11-3F5B-42AB-A16F-0474FA98D3FD
title: Класс Msvm_TimeSyncComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponentSettingData
- Msvm_TimeSyncComponentSettingData.InstanceID
- Msvm_TimeSyncComponentSettingData.Caption
- Msvm_TimeSyncComponentSettingData.Description
- Msvm_TimeSyncComponentSettingData.ElementName
- Msvm_TimeSyncComponentSettingData.ResourceType
- Msvm_TimeSyncComponentSettingData.OtherResourceType
- Msvm_TimeSyncComponentSettingData.ResourceSubType
- Msvm_TimeSyncComponentSettingData.PoolID
- Msvm_TimeSyncComponentSettingData.ConsumerVisibility
- Msvm_TimeSyncComponentSettingData.HostResource
- Msvm_TimeSyncComponentSettingData.AllocationUnits
- Msvm_TimeSyncComponentSettingData.VirtualQuantity
- Msvm_TimeSyncComponentSettingData.Reservation
- Msvm_TimeSyncComponentSettingData.Limit
- Msvm_TimeSyncComponentSettingData.Weight
- Msvm_TimeSyncComponentSettingData.AutomaticAllocation
- Msvm_TimeSyncComponentSettingData.AutomaticDeallocation
- Msvm_TimeSyncComponentSettingData.Parent
- Msvm_TimeSyncComponentSettingData.Connection
- Msvm_TimeSyncComponentSettingData.Address
- Msvm_TimeSyncComponentSettingData.MappingBehavior
- Msvm_TimeSyncComponentSettingData.AddressOnParent
- Msvm_TimeSyncComponentSettingData.VirtualQuantityUnits
- Msvm_TimeSyncComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 063c0f7904976d50d7c1914f810e71ff84f740b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991376"
---
# <a name="msvm_timesynccomponentsettingdata-class"></a><span data-ttu-id="06a4a-103">\_Класс мсвм тимесинккомпонентсеттингдата</span><span class="sxs-lookup"><span data-stu-id="06a4a-103">Msvm\_TimeSyncComponentSettingData class</span></span>

<span data-ttu-id="06a4a-104">Представляет настроенное состояние службы синхронизации времени.</span><span class="sxs-lookup"><span data-stu-id="06a4a-104">Represents the configured state of the time synchronization service.</span></span>

<span data-ttu-id="06a4a-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="06a4a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a4a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06a4a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Time Synchronization";
  string  Description = "Microsoft Time Synchronization Service Setting Data";
  string  ElementName = "Time Synchronization";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Time Synchronization Component";
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

## <a name="members"></a><span data-ttu-id="06a4a-107">Члены</span><span class="sxs-lookup"><span data-stu-id="06a4a-107">Members</span></span>

<span data-ttu-id="06a4a-108">Класс **мсвм \_ тимесинккомпонентсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="06a4a-108">The **Msvm\_TimeSyncComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="06a4a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="06a4a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06a4a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="06a4a-110">Properties</span></span>

<span data-ttu-id="06a4a-111">Класс **мсвм \_ тимесинккомпонентсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="06a4a-111">The **Msvm\_TimeSyncComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06a4a-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="06a4a-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="06a4a-115">The address of the resource.</span></span> <span data-ttu-id="06a4a-116">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-117">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="06a4a-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-120">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="06a4a-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="06a4a-121">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="06a4a-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="06a4a-122">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-123">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="06a4a-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-126">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="06a4a-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="06a4a-127">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-128">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="06a4a-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="06a4a-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-131">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="06a4a-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="06a4a-132">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-133">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="06a4a-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="06a4a-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-136">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="06a4a-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="06a4a-137">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="06a4a-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-141">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="06a4a-141">A short description of the object.</span></span> <span data-ttu-id="06a4a-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="06a4a-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-143">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="06a4a-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-144">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="06a4a-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-146">Объект, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="06a4a-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="06a4a-147">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-148">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="06a4a-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a4a-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-151">Пользователи могут видеть выделенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="06a4a-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="06a4a-152">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="06a4a-153">Значение</span><span class="sxs-lookup"><span data-stu-id="06a4a-153">Value</span></span>                                                                        | <span data-ttu-id="06a4a-154">Значение</span><span class="sxs-lookup"><span data-stu-id="06a4a-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="06a4a-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="06a4a-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="06a4a-156">Виртуализированных</span><span class="sxs-lookup"><span data-stu-id="06a4a-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="06a4a-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="06a4a-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-160">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="06a4a-160">A description of the object.</span></span> <span data-ttu-id="06a4a-161">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="06a4a-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="06a4a-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-165">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="06a4a-165">A display name for the object.</span></span> <span data-ttu-id="06a4a-166">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="06a4a-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="06a4a-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a4a-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-170">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="06a4a-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="06a4a-171">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="06a4a-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span></span>

<dt>



 <span data-ttu-id="06a4a-172">(2)</span><span class="sxs-lookup"><span data-stu-id="06a4a-172">(2)</span></span>


</dt> <dd>

<span data-ttu-id="06a4a-173">Активировано</span><span class="sxs-lookup"><span data-stu-id="06a4a-173">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-174">3</span><span class="sxs-lookup"><span data-stu-id="06a4a-174">3</span></span>
</dt> <dd>

<span data-ttu-id="06a4a-175">Выключено</span><span class="sxs-lookup"><span data-stu-id="06a4a-175">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="06a4a-176">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="06a4a-176">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-177">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="06a4a-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-179">Предоставляет определенное назначение для размещения или базовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06a4a-179">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="06a4a-180">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="06a4a-180">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-181">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="06a4a-181">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-184">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="06a4a-184">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-185">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="06a4a-185">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="06a4a-186">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="06a4a-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-187">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="06a4a-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-188">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06a4a-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-190">Верхняя граница или максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="06a4a-190">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="06a4a-191">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-192">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="06a4a-192">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-193">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a4a-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-195">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="06a4a-195">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="06a4a-196">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-197">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="06a4a-197">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-200">Тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение other.</span><span class="sxs-lookup"><span data-stu-id="06a4a-200">The resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="06a4a-201">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-202">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="06a4a-202">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-205">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="06a4a-205">The parent of the resource.</span></span> <span data-ttu-id="06a4a-206">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-207">**пулид**</span><span class="sxs-lookup"><span data-stu-id="06a4a-207">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-210">Идентификатор пула ресурсов, из которого выделяется ресурс.</span><span class="sxs-lookup"><span data-stu-id="06a4a-210">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="06a4a-211">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-212">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="06a4a-212">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-213">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06a4a-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-215">Объем ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="06a4a-215">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="06a4a-216">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-217">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="06a4a-217">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-220">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="06a4a-220">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="06a4a-221">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="06a4a-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="06a4a-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-223">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a4a-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-225">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="06a4a-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="06a4a-226">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="06a4a-227">Значение</span><span class="sxs-lookup"><span data-stu-id="06a4a-227">Value</span></span>                                                                        | <span data-ttu-id="06a4a-228">Значение</span><span class="sxs-lookup"><span data-stu-id="06a4a-228">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="06a4a-229"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="06a4a-229"><dt>1</dt></span></span> </dl> | <span data-ttu-id="06a4a-230">Другое</span><span class="sxs-lookup"><span data-stu-id="06a4a-230">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="06a4a-231">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="06a4a-231">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-232">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06a4a-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-234">Количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="06a4a-234">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="06a4a-235">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-236">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="06a4a-236">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="06a4a-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-239">Задает единицу измерения для этого выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06a4a-239">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="06a4a-240">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="06a4a-240">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="06a4a-241">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06a4a-242">**Weight**</span><span class="sxs-lookup"><span data-stu-id="06a4a-242">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a4a-243">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06a4a-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06a4a-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="06a4a-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a4a-245">Относительный приоритет для этого выделения относительно других выделений из того же пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06a4a-245">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="06a4a-246">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06a4a-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06a4a-247">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06a4a-247">Remarks</span></span>

<span data-ttu-id="06a4a-248">Доступ к классу **\_ тимесинккомпонентсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="06a4a-248">Access to the **Msvm\_TimeSyncComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="06a4a-249">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="06a4a-249">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="06a4a-250">Требования</span><span class="sxs-lookup"><span data-stu-id="06a4a-250">Requirements</span></span>



| <span data-ttu-id="06a4a-251">Требование</span><span class="sxs-lookup"><span data-stu-id="06a4a-251">Requirement</span></span> | <span data-ttu-id="06a4a-252">Значение</span><span class="sxs-lookup"><span data-stu-id="06a4a-252">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a4a-253">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06a4a-253">Minimum supported client</span></span><br/> | <span data-ttu-id="06a4a-254">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="06a4a-254">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="06a4a-255">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06a4a-255">Minimum supported server</span></span><br/> | <span data-ttu-id="06a4a-256">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="06a4a-256">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06a4a-257">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="06a4a-257">Namespace</span></span><br/>                | <span data-ttu-id="06a4a-258">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="06a4a-258">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="06a4a-259">MOF</span><span class="sxs-lookup"><span data-stu-id="06a4a-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06a4a-260"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06a4a-260"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06a4a-261">DLL</span><span class="sxs-lookup"><span data-stu-id="06a4a-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06a4a-262"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06a4a-262"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06a4a-263">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06a4a-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a4a-264">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="06a4a-264">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="06a4a-265">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="06a4a-265">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

