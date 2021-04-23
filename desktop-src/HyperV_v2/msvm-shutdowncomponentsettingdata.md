---
description: Представляет настроенное состояние службы завершения работы.
ms.assetid: 434DE26A-E78A-403A-AFAB-2F9272426A16
title: Класс Msvm_ShutdownComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponentSettingData
- Msvm_ShutdownComponentSettingData.InstanceID
- Msvm_ShutdownComponentSettingData.Caption
- Msvm_ShutdownComponentSettingData.Description
- Msvm_ShutdownComponentSettingData.ElementName
- Msvm_ShutdownComponentSettingData.ResourceType
- Msvm_ShutdownComponentSettingData.OtherResourceType
- Msvm_ShutdownComponentSettingData.ResourceSubType
- Msvm_ShutdownComponentSettingData.PoolID
- Msvm_ShutdownComponentSettingData.ConsumerVisibility
- Msvm_ShutdownComponentSettingData.HostResource
- Msvm_ShutdownComponentSettingData.AllocationUnits
- Msvm_ShutdownComponentSettingData.VirtualQuantity
- Msvm_ShutdownComponentSettingData.Reservation
- Msvm_ShutdownComponentSettingData.Limit
- Msvm_ShutdownComponentSettingData.Weight
- Msvm_ShutdownComponentSettingData.AutomaticAllocation
- Msvm_ShutdownComponentSettingData.AutomaticDeallocation
- Msvm_ShutdownComponentSettingData.Parent
- Msvm_ShutdownComponentSettingData.Connection
- Msvm_ShutdownComponentSettingData.Address
- Msvm_ShutdownComponentSettingData.MappingBehavior
- Msvm_ShutdownComponentSettingData.AddressOnParent
- Msvm_ShutdownComponentSettingData.VirtualQuantityUnits
- Msvm_ShutdownComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8ee2fcb910dc788b01a58544bbfe6a06ba215585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263609"
---
# <a name="msvm_shutdowncomponentsettingdata-class"></a><span data-ttu-id="fc149-103">\_Класс мсвм шутдовнкомпонентсеттингдата</span><span class="sxs-lookup"><span data-stu-id="fc149-103">Msvm\_ShutdownComponentSettingData class</span></span>

<span data-ttu-id="fc149-104">Представляет настроенное состояние службы завершения работы.</span><span class="sxs-lookup"><span data-stu-id="fc149-104">Represents the configured state of the shutdown service.</span></span>

<span data-ttu-id="fc149-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fc149-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc149-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc149-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Shutdown";
  string  Description = "Microsoft Shutdown Service Setting Data";
  string  ElementName = "Shutdown";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Shutdown Component";
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

## <a name="members"></a><span data-ttu-id="fc149-107">Члены</span><span class="sxs-lookup"><span data-stu-id="fc149-107">Members</span></span>

<span data-ttu-id="fc149-108">Класс **мсвм \_ шутдовнкомпонентсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fc149-108">The **Msvm\_ShutdownComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fc149-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="fc149-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc149-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fc149-110">Properties</span></span>

<span data-ttu-id="fc149-111">Класс **мсвм \_ шутдовнкомпонентсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fc149-111">The **Msvm\_ShutdownComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc149-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="fc149-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc149-115">The address of the resource.</span></span> <span data-ttu-id="fc149-116">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-117">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="fc149-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-120">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="fc149-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="fc149-121">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="fc149-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="fc149-122">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-123">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="fc149-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-126">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="fc149-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="fc149-127">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-128">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="fc149-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fc149-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-131">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="fc149-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="fc149-132">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-133">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="fc149-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="fc149-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-136">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="fc149-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="fc149-137">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="fc149-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-141">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="fc149-141">A short description of the object.</span></span> <span data-ttu-id="fc149-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Shutdown".</span><span class="sxs-lookup"><span data-stu-id="fc149-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Shutdown".</span></span>

</dd> <dt>

<span data-ttu-id="fc149-143">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="fc149-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-144">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="fc149-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc149-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-146">Объект, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="fc149-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="fc149-147">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-148">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="fc149-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc149-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-151">Пользователи могут видеть выделенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="fc149-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="fc149-152">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="fc149-153">Значение</span><span class="sxs-lookup"><span data-stu-id="fc149-153">Value</span></span>                                                                        | <span data-ttu-id="fc149-154">Значение</span><span class="sxs-lookup"><span data-stu-id="fc149-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="fc149-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="fc149-156">Виртуализированных</span><span class="sxs-lookup"><span data-stu-id="fc149-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fc149-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc149-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-160">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="fc149-160">A description of the object.</span></span> <span data-ttu-id="fc149-161">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc149-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fc149-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-165">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="fc149-165">A display name for the object.</span></span> <span data-ttu-id="fc149-166">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc149-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fc149-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc149-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-170">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="fc149-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="fc149-171">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc149-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fc149-172">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="fc149-172">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fc149-173">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="fc149-173">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc149-174">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="fc149-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-175">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="fc149-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc149-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-177">Предоставляет определенное назначение для размещения или базовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc149-177">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="fc149-178">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-178">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-179">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fc149-179">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc149-182">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="fc149-182">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fc149-183">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="fc149-183">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fc149-184">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc149-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-185">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="fc149-185">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-186">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc149-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-188">Верхняя граница или максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="fc149-188">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="fc149-189">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-190">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="fc149-190">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-191">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc149-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-193">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="fc149-193">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="fc149-194">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-195">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="fc149-195">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-198">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="fc149-198">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="fc149-199">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-200">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="fc149-200">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-203">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc149-203">The parent of the resource.</span></span> <span data-ttu-id="fc149-204">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-205">**пулид**</span><span class="sxs-lookup"><span data-stu-id="fc149-205">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-208">Идентификатор пула ресурсов, из которого выделяется ресурс.</span><span class="sxs-lookup"><span data-stu-id="fc149-208">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="fc149-209">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-210">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="fc149-210">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-211">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc149-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-213">Объем ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="fc149-213">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="fc149-214">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-214">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-215">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="fc149-215">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-218">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc149-218">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="fc149-219">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="fc149-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-221">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc149-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-223">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="fc149-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="fc149-224">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="fc149-225">Значение</span><span class="sxs-lookup"><span data-stu-id="fc149-225">Value</span></span>                                                                        | <span data-ttu-id="fc149-226">Значение</span><span class="sxs-lookup"><span data-stu-id="fc149-226">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="fc149-227"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-227"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fc149-228">Другое</span><span class="sxs-lookup"><span data-stu-id="fc149-228">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fc149-229">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="fc149-229">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-230">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc149-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-232">Количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="fc149-232">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="fc149-233">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-233">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-234">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="fc149-234">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc149-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-237">Задает единицу измерения для этого выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc149-237">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="fc149-238">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fc149-238">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="fc149-239">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-239">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fc149-240">**Weight**</span><span class="sxs-lookup"><span data-stu-id="fc149-240">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc149-241">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc149-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc149-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc149-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc149-243">Относительный приоритет для этого выделения относительно других выделений из того же пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc149-243">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="fc149-244">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fc149-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc149-245">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc149-245">Remarks</span></span>

<span data-ttu-id="fc149-246">Доступ к классу **\_ шутдовнкомпонентсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="fc149-246">Access to the **Msvm\_ShutdownComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fc149-247">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fc149-247">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc149-248">Требования</span><span class="sxs-lookup"><span data-stu-id="fc149-248">Requirements</span></span>



| <span data-ttu-id="fc149-249">Требование</span><span class="sxs-lookup"><span data-stu-id="fc149-249">Requirement</span></span> | <span data-ttu-id="fc149-250">Значение</span><span class="sxs-lookup"><span data-stu-id="fc149-250">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc149-251">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc149-251">Minimum supported client</span></span><br/> | <span data-ttu-id="fc149-252">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fc149-252">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fc149-253">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc149-253">Minimum supported server</span></span><br/> | <span data-ttu-id="fc149-254">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fc149-254">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc149-255">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fc149-255">Namespace</span></span><br/>                | <span data-ttu-id="fc149-256">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fc149-256">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fc149-257">MOF</span><span class="sxs-lookup"><span data-stu-id="fc149-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc149-258"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-258"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc149-259">DLL</span><span class="sxs-lookup"><span data-stu-id="fc149-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc149-260"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc149-260"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc149-261">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc149-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc149-262">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="fc149-262">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="fc149-263">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="fc149-263">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

