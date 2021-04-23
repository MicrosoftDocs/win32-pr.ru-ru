---
description: Представляет настроенное состояние искусственного Fibre Channel порта.
ms.assetid: 5d47dd80-de34-4ae4-a300-c16da1cd4974
title: Класс Msvm_SyntheticFcPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPortSettingData
- Msvm_SyntheticFcPortSettingData.InstanceID
- Msvm_SyntheticFcPortSettingData.Caption
- Msvm_SyntheticFcPortSettingData.Description
- Msvm_SyntheticFcPortSettingData.ElementName
- Msvm_SyntheticFcPortSettingData.ResourceType
- Msvm_SyntheticFcPortSettingData.OtherResourceType
- Msvm_SyntheticFcPortSettingData.ResourceSubType
- Msvm_SyntheticFcPortSettingData.PoolID
- Msvm_SyntheticFcPortSettingData.ConsumerVisibility
- Msvm_SyntheticFcPortSettingData.HostResource
- Msvm_SyntheticFcPortSettingData.AllocationUnits
- Msvm_SyntheticFcPortSettingData.VirtualQuantity
- Msvm_SyntheticFcPortSettingData.Reservation
- Msvm_SyntheticFcPortSettingData.Limit
- Msvm_SyntheticFcPortSettingData.Weight
- Msvm_SyntheticFcPortSettingData.AutomaticAllocation
- Msvm_SyntheticFcPortSettingData.AutomaticDeallocation
- Msvm_SyntheticFcPortSettingData.Parent
- Msvm_SyntheticFcPortSettingData.Connection
- Msvm_SyntheticFcPortSettingData.Address
- Msvm_SyntheticFcPortSettingData.MappingBehavior
- Msvm_SyntheticFcPortSettingData.AddressOnParent
- Msvm_SyntheticFcPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticFcPortSettingData.VirtualPortWWPN
- Msvm_SyntheticFcPortSettingData.VirtualPortWWNN
- Msvm_SyntheticFcPortSettingData.SecondaryWWPN
- Msvm_SyntheticFcPortSettingData.SecondaryWWNN
- Msvm_SyntheticFcPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticFcPortSettingData.ChapEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdd0342f5429f5314f5c744a3a760101dbaa043b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808800"
---
# <a name="msvm_syntheticfcportsettingdata-class"></a><span data-ttu-id="ab672-103">\_Класс мсвм синсетикфкпортсеттингдата</span><span class="sxs-lookup"><span data-stu-id="ab672-103">Msvm\_SyntheticFcPortSettingData class</span></span>

<span data-ttu-id="ab672-104">Представляет настроенное состояние искусственного Fibre Channel порта.</span><span class="sxs-lookup"><span data-stu-id="ab672-104">Represents the configured state of a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="ab672-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ab672-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab672-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab672-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPortSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel Port Default Settings";
  string  Description = "Describes the default settings for the virtual Fibre Channel port resources.";
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
  string  VirtualPortWWPN;
  string  VirtualPortWWNN;
  string  SecondaryWWPN;
  string  SecondaryWWNN;
  string  VirtualSystemIdentifiers[];
  boolean ChapEnabled;
};
```

## <a name="members"></a><span data-ttu-id="ab672-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ab672-107">Members</span></span>

<span data-ttu-id="ab672-108">Класс **мсвм \_ синсетикфкпортсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ab672-108">The **Msvm\_SyntheticFcPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ab672-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab672-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab672-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab672-110">Properties</span></span>

<span data-ttu-id="ab672-111">Класс **мсвм \_ синсетикфкпортсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ab672-111">The **Msvm\_SyntheticFcPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab672-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="ab672-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab672-115">The address of the resource.</span></span> <span data-ttu-id="ab672-116">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-117">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="ab672-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-120">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="ab672-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="ab672-121">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="ab672-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="ab672-122">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-123">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="ab672-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-126">Единица распределения, используемая свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="ab672-126">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="ab672-127">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-128">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="ab672-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ab672-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-131">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="ab672-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ab672-132">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-133">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="ab672-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ab672-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-136">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="ab672-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="ab672-137">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ab672-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab672-141">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="ab672-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ab672-142">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ab672-142">A short description of the object.</span></span> <span data-ttu-id="ab672-143">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ab672-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-144">**чапенаблед**</span><span class="sxs-lookup"><span data-stu-id="ab672-144">**ChapEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-145">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ab672-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-147">Указывает, что этот порт настроен с использованием общего секрета с помощью DH-CHAP, что позволяет Fibre Channel структуре проверить подлинность этой виртуальной машины, которая может использовать WWN-имена, назначенные этому порту.</span><span class="sxs-lookup"><span data-stu-id="ab672-147">Indicates that this port has been configured with a shared secret using DH-CHAP, which allows the Fibre Channel fabric to authenticate that this virtual machine can legitimately use the world wide names that are assigned to this port.</span></span>

</dd> <dt>

<span data-ttu-id="ab672-148">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="ab672-148">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-149">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ab672-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab672-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-151">Устройство, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="ab672-151">The device to which this resource is connected.</span></span> <span data-ttu-id="ab672-152">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-153">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="ab672-153">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab672-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-156">Видимость потребителя для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab672-156">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="ab672-157">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-158">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ab672-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-161">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ab672-161">A description of the object.</span></span> <span data-ttu-id="ab672-162">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ab672-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ab672-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-166">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ab672-166">A display name for the object.</span></span> <span data-ttu-id="ab672-167">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab672-167">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="ab672-168">Изменение этого свойства приведет к изменению имени элемента связанного логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ab672-168">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="ab672-169">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ab672-169">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ab672-170">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="ab672-170">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-171">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ab672-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab672-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-173">Каждому устройству на виртуальной машине можно назначить только один ресурс узла, поэтому можно установить только первый элемент этого массива.</span><span class="sxs-lookup"><span data-stu-id="ab672-173">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="ab672-174">Для устройств, поддерживающих эту функцию, установите первый элемент массива **хостресаурце** , чтобы он содержал ссылку на базовый ресурс узла, который нужно назначить.</span><span class="sxs-lookup"><span data-stu-id="ab672-174">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="ab672-175">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-175">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-176">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ab672-176">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab672-179">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ab672-179">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ab672-180">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ab672-180">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ab672-181">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab672-181">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-182">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="ab672-182">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-183">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab672-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-185">Максимальный объем соответствующих ресурсов узла, которые могут использоваться виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="ab672-185">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="ab672-186">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-187">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="ab672-187">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-188">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab672-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-190">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="ab672-190">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="ab672-191">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-192">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="ab672-192">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-195">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а [**ResourceType**](msvm-processorsettingdata.md) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="ab672-195">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="ab672-196">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), но не используется.</span><span class="sxs-lookup"><span data-stu-id="ab672-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab672-197">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="ab672-197">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-200">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab672-200">The parent of the resource.</span></span> <span data-ttu-id="ab672-201">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-202">**пулид**</span><span class="sxs-lookup"><span data-stu-id="ab672-202">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-205">Идентификатор пула ресурсов, из которого был выделен ресурс.</span><span class="sxs-lookup"><span data-stu-id="ab672-205">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="ab672-206">Для экземпляров, связанных с виртуальной машиной, это будет «Microsoft:*GUID* \\ *-данные устройства*».</span><span class="sxs-lookup"><span data-stu-id="ab672-206">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="ab672-207">Для экземпляров, определяющих потенциальные параметры виртуальной машины, это будет "Microsoft: определение \\  \\ *типа* GUID", где *тип* может быть одним из значений: "максимум", "минимум", "default" или "Increment".</span><span class="sxs-lookup"><span data-stu-id="ab672-207">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="ab672-208">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-209">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="ab672-209">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-210">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab672-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-212">Объем ресурсов, зарезервированных для использования виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="ab672-212">The amount of resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="ab672-213">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), но не используется.</span><span class="sxs-lookup"><span data-stu-id="ab672-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab672-214">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ab672-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-217">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab672-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="ab672-218">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab672-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="ab672-219">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ab672-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-221">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ab672-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-223">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="ab672-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="ab672-224">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="ab672-225">Значение</span><span class="sxs-lookup"><span data-stu-id="ab672-225">Value</span></span>                                                                                                                                                                                          | <span data-ttu-id="ab672-226">Значение</span><span class="sxs-lookup"><span data-stu-id="ab672-226">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC_HBA"></span><span id="fc_hba"></span><dl> <span data-ttu-id="ab672-227"><dt>**FC HBA**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ab672-227"><dt>**FC HBA**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="ab672-228">Fibre Channel,</span><span class="sxs-lookup"><span data-stu-id="ab672-228">Fibre Channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab672-229">**секондариввнн**</span><span class="sxs-lookup"><span data-stu-id="ab672-229">**SecondaryWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-232">Указывает имя узла виртуального адаптера шины, используемого во время динамической миграции виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab672-232">Indicates the world wide node name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ab672-233">**секондариввпн**</span><span class="sxs-lookup"><span data-stu-id="ab672-233">**SecondaryWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-234">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-236">Указывает WWN имя порта виртуального адаптера шины, которое будет использоваться во время динамической миграции виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab672-236">Indicates the world wide port name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ab672-237">**виртуалпортввнн**</span><span class="sxs-lookup"><span data-stu-id="ab672-237">**VirtualPortWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-238">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-240">Указывает WWN имени узла для виртуального порта HBA.</span><span class="sxs-lookup"><span data-stu-id="ab672-240">Indicates the world wide node name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="ab672-241">**виртуалпортввпн**</span><span class="sxs-lookup"><span data-stu-id="ab672-241">**VirtualPortWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-244">Указывает WWN имя порта виртуального адаптера шины.</span><span class="sxs-lookup"><span data-stu-id="ab672-244">Indicates the world wide port name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="ab672-245">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="ab672-245">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-246">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ab672-246">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-248">Указывает количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="ab672-248">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="ab672-249">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-250">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="ab672-250">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ab672-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-253">Задает единицу измерения для свойства **виртуалкуантити** .</span><span class="sxs-lookup"><span data-stu-id="ab672-253">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="ab672-254">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ab672-254">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="ab672-255">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ab672-255">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ab672-256">**виртуалсистемидентифиерс**</span><span class="sxs-lookup"><span data-stu-id="ab672-256">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-257">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ab672-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ab672-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab672-259">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ab672-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ab672-260">Строковый массив идентификаторов этого ресурса, представленный операционной системе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab672-260">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="ab672-261">Индексы и значения для каждого индекса определяются для каждого ресурса (то есть для каждого перечислимого **значения типа ресурса)** .</span><span class="sxs-lookup"><span data-stu-id="ab672-261">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="ab672-262">Это свойство не используется</span><span class="sxs-lookup"><span data-stu-id="ab672-262">This property is not used</span></span>

</dd> <dt>

<span data-ttu-id="ab672-263">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ab672-263">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab672-264">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab672-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab672-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab672-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab672-266">Целое число, определяющее относительный вес для каждого процессора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ab672-266">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="ab672-267">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), но не используется.</span><span class="sxs-lookup"><span data-stu-id="ab672-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab672-268">Требования</span><span class="sxs-lookup"><span data-stu-id="ab672-268">Requirements</span></span>



| <span data-ttu-id="ab672-269">Требование</span><span class="sxs-lookup"><span data-stu-id="ab672-269">Requirement</span></span> | <span data-ttu-id="ab672-270">Значение</span><span class="sxs-lookup"><span data-stu-id="ab672-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab672-271">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab672-271">Minimum supported client</span></span><br/> | <span data-ttu-id="ab672-272">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ab672-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ab672-273">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab672-273">Minimum supported server</span></span><br/> | <span data-ttu-id="ab672-274">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ab672-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab672-275">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ab672-275">Namespace</span></span><br/>                | <span data-ttu-id="ab672-276">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ab672-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ab672-277">MOF</span><span class="sxs-lookup"><span data-stu-id="ab672-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab672-278"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab672-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab672-279">DLL</span><span class="sxs-lookup"><span data-stu-id="ab672-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab672-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab672-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

