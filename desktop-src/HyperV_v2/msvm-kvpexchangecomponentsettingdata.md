---
description: Представляет настроенное состояние службы обмена ключами и значением.
ms.assetid: B7ED1091-E49A-4C38-9794-E074E6B9EF48
title: Класс Msvm_KvpExchangeComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponentSettingData
- Msvm_KvpExchangeComponentSettingData.DisableHostKVPItems
- Msvm_KvpExchangeComponentSettingData.InstanceID
- Msvm_KvpExchangeComponentSettingData.Caption
- Msvm_KvpExchangeComponentSettingData.Description
- Msvm_KvpExchangeComponentSettingData.ElementName
- Msvm_KvpExchangeComponentSettingData.ResourceType
- Msvm_KvpExchangeComponentSettingData.OtherResourceType
- Msvm_KvpExchangeComponentSettingData.ResourceSubType
- Msvm_KvpExchangeComponentSettingData.PoolID
- Msvm_KvpExchangeComponentSettingData.ConsumerVisibility
- Msvm_KvpExchangeComponentSettingData.HostResource
- Msvm_KvpExchangeComponentSettingData.AllocationUnits
- Msvm_KvpExchangeComponentSettingData.VirtualQuantity
- Msvm_KvpExchangeComponentSettingData.Reservation
- Msvm_KvpExchangeComponentSettingData.Limit
- Msvm_KvpExchangeComponentSettingData.Weight
- Msvm_KvpExchangeComponentSettingData.AutomaticAllocation
- Msvm_KvpExchangeComponentSettingData.AutomaticDeallocation
- Msvm_KvpExchangeComponentSettingData.Parent
- Msvm_KvpExchangeComponentSettingData.Connection
- Msvm_KvpExchangeComponentSettingData.Address
- Msvm_KvpExchangeComponentSettingData.MappingBehavior
- Msvm_KvpExchangeComponentSettingData.AddressOnParent
- Msvm_KvpExchangeComponentSettingData.VirtualQuantityUnits
- Msvm_KvpExchangeComponentSettingData.EnabledState
- Msvm_KvpExchangeComponentSettingData.HostExchangeItems
- Msvm_KvpExchangeComponentSettingData.HostOnlyItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fe2ef128d3212ba2dfd47a3d71f713c26ba2435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663080"
---
# <a name="msvm_kvpexchangecomponentsettingdata-class"></a><span data-ttu-id="2a4e7-103">\_Класс мсвм квпексчанжекомпонентсеттингдата</span><span class="sxs-lookup"><span data-stu-id="2a4e7-103">Msvm\_KvpExchangeComponentSettingData class</span></span>

<span data-ttu-id="2a4e7-104">Представляет настроенное состояние службы обмена ключами и значением.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-104">Represents the configured state of the key/value pair exchange service.</span></span>

<span data-ttu-id="2a4e7-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a4e7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a4e7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponentSettingData : CIM_ResourceAllocationSettingData
{
  boolean DisableHostKVPItems;
  string  InstanceID;
  string  Caption = "Key-Value Pair Exchange";
  string  Description = "Microsoft Key-Value Pair Exchange Service Setting Data";
  string  ElementName = "Key-Value Pair Exchange";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Key-Value Pair Exchange Component";
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
  String  HostExchangeItems[];
  String  HostOnlyItems[];
};
```

## <a name="members"></a><span data-ttu-id="2a4e7-107">Члены</span><span class="sxs-lookup"><span data-stu-id="2a4e7-107">Members</span></span>

<span data-ttu-id="2a4e7-108">Класс **мсвм \_ квпексчанжекомпонентсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2a4e7-108">The **Msvm\_KvpExchangeComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2a4e7-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a4e7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a4e7-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a4e7-110">Properties</span></span>

<span data-ttu-id="2a4e7-111">Класс **мсвм \_ квпексчанжекомпонентсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-111">The **Msvm\_KvpExchangeComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a4e7-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-115">The address of the resource.</span></span> <span data-ttu-id="2a4e7-116">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-117">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-120">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="2a4e7-121">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="2a4e7-122">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-123">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-126">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="2a4e7-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="2a4e7-127">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-128">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-131">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="2a4e7-132">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-133">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-136">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="2a4e7-137">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-141">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-141">A short description of the object.</span></span> <span data-ttu-id="2a4e7-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-143">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-144">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-146">Объект, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="2a4e7-147">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-148">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-151">Пользователи могут видеть выделенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="2a4e7-152">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="2a4e7-153">Значение</span><span class="sxs-lookup"><span data-stu-id="2a4e7-153">Value</span></span>                                                                        | <span data-ttu-id="2a4e7-154">Значение</span><span class="sxs-lookup"><span data-stu-id="2a4e7-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="2a4e7-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2a4e7-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2a4e7-156">Виртуализированных</span><span class="sxs-lookup"><span data-stu-id="2a4e7-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2a4e7-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-160">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-160">A description of the object.</span></span> <span data-ttu-id="2a4e7-161">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-162">**дисаблехостквпитемс**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-162">**DisableHostKVPItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-163">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2a4e7-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-165">Это свойство отключает узел от автоматически популатингхост имя и сведения о ОС в гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-165">This property disables the host from automatically populatinghost name and OS information inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="2a4e7-166">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-166">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="2a4e7-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-170">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-170">A display name for the object.</span></span> <span data-ttu-id="2a4e7-171">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-172">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-172">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-173">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-175">Включенное состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-175">The enabled state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2a4e7-176">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="2a4e7-176">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2a4e7-177">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="2a4e7-177">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a4e7-178">**хостексчанжеитемс**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-178">**HostExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-179">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-179">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-181">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), **Хипервембеддединстанце** ("мсвм \_ квпексчанжедатаитем")</span><span class="sxs-lookup"><span data-stu-id="2a4e7-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-182">Массив внедренных экземпляров [**мсвм \_ квпексчанжедатаитем**](msvm-kvpexchangedataitem.md) , представляющих пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="2a4e7-182">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances that represent the key/value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-183">**хостонлитемс**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-183">**HostOnlyItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-184">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-184">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-186">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), **Хипервембеддединстанце** ("мсвм \_ квпексчанжедатаитем")</span><span class="sxs-lookup"><span data-stu-id="2a4e7-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-187">Массив экземпляров [**мсвм \_ квпексчанжедатаитем**](msvm-kvpexchangedataitem.md) , содержащих пары "ключ-значение", которые хранятся в файле конфигурации, но не обмениваются данными с гостевой операционной системой.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-187">An array of [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances containing the key/value pairs that are stored in the configuration file but not exchanged with the guest operating system.</span></span> <span data-ttu-id="2a4e7-188">Это позволяет приложениям хранить данные, относящиеся к виртуальной машине, которые не должны быть видимыми для гостевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-188">This allows applications to store virtual machine-specific data that does not need to be visible to the guest operating system.</span></span> <span data-ttu-id="2a4e7-189">Элементы форматируются так же, как элементы в свойстве **хостексчанжеитемс** , за исключением того, что свойство **Source** экземпляра **мсвм \_ квпексчанжедатаитем** имеет значение 4.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-189">The items are formatted the same as the items in the **HostExchangeItems** property except the **Source** property of the **Msvm\_KvpExchangeDataItem** instance is set to 4.</span></span> <span data-ttu-id="2a4e7-190">Каждый файл конфигурации ограничен 128 парами "ключ-значение", где каждое поле значения может иметь размер до 16 КБ, а ключевое поле может содержать до 512 байт.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-190">Each configuration file is limited to 128 key/value pairs, where each value field is allowed to be up to 16 KB in size and the key field is allowed to be up to 512 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-191">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-191">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-192">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-192">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-194">Предоставляет определенное назначение для размещения или базовых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-194">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="2a4e7-195">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-196">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-196">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-199">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-199">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-200">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-200">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2a4e7-201">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-202">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-203">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-205">Верхняя граница или максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="2a4e7-206">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-207">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-210">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="2a4e7-211">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-212">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-215">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-215">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="2a4e7-216">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-217">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-220">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-220">The parent of the resource.</span></span> <span data-ttu-id="2a4e7-221">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-222">**пулид**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-225">Идентификатор пула ресурсов, из которого выделяется ресурс.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="2a4e7-226">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-227">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-228">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-230">Объем ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="2a4e7-231">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-232">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-233">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-235">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-235">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="2a4e7-236">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-238">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-240">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="2a4e7-241">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="2a4e7-242">Значение</span><span class="sxs-lookup"><span data-stu-id="2a4e7-242">Value</span></span>                                                                        | <span data-ttu-id="2a4e7-243">Значение</span><span class="sxs-lookup"><span data-stu-id="2a4e7-243">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="2a4e7-244"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2a4e7-244"><dt>1</dt></span></span> </dl> | <span data-ttu-id="2a4e7-245">Другое</span><span class="sxs-lookup"><span data-stu-id="2a4e7-245">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2a4e7-246">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-246">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-247">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-247">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-249">Количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-249">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="2a4e7-250">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-250">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-251">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-251">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-254">Задает единицу измерения для этого выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-254">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="2a4e7-255">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-255">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="2a4e7-256">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-256">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2a4e7-257">**Weight**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-257">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a4e7-258">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a4e7-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a4e7-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a4e7-260">Относительный приоритет для этого выделения относительно других выделений из того же пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-260">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="2a4e7-261">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a4e7-262">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a4e7-262">Remarks</span></span>

<span data-ttu-id="2a4e7-263">Доступ к классу **\_ квпексчанжекомпонентсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="2a4e7-263">Access to the **Msvm\_KvpExchangeComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2a4e7-264">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2a4e7-264">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a4e7-265">Требования</span><span class="sxs-lookup"><span data-stu-id="2a4e7-265">Requirements</span></span>



| <span data-ttu-id="2a4e7-266">Требование</span><span class="sxs-lookup"><span data-stu-id="2a4e7-266">Requirement</span></span> | <span data-ttu-id="2a4e7-267">Значение</span><span class="sxs-lookup"><span data-stu-id="2a4e7-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4e7-268">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a4e7-268">Minimum supported client</span></span><br/> | <span data-ttu-id="2a4e7-269">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2a4e7-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2a4e7-270">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a4e7-270">Minimum supported server</span></span><br/> | <span data-ttu-id="2a4e7-271">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2a4e7-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a4e7-272">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2a4e7-272">Namespace</span></span><br/>                | <span data-ttu-id="2a4e7-273">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="2a4e7-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2a4e7-274">MOF</span><span class="sxs-lookup"><span data-stu-id="2a4e7-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a4e7-275"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a4e7-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a4e7-276">DLL</span><span class="sxs-lookup"><span data-stu-id="2a4e7-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a4e7-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a4e7-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a4e7-278">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a4e7-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a4e7-279">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-279">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="2a4e7-280">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="2a4e7-280">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

