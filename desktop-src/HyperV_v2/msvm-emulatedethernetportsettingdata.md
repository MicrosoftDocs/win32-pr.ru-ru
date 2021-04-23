---
description: Представляет настроенное состояние эмулированного адаптера Ethernet.
ms.assetid: 8BFD69D8-65B6-4C6F-9972-BD2F3C4FB5B8
title: Класс Msvm_EmulatedEthernetPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPortSettingData
- Msvm_EmulatedEthernetPortSettingData.Caption
- Msvm_EmulatedEthernetPortSettingData.Description
- Msvm_EmulatedEthernetPortSettingData.InstanceID
- Msvm_EmulatedEthernetPortSettingData.ElementName
- Msvm_EmulatedEthernetPortSettingData.ResourceType
- Msvm_EmulatedEthernetPortSettingData.OtherResourceType
- Msvm_EmulatedEthernetPortSettingData.ResourceSubType
- Msvm_EmulatedEthernetPortSettingData.PoolID
- Msvm_EmulatedEthernetPortSettingData.ConsumerVisibility
- Msvm_EmulatedEthernetPortSettingData.HostResource
- Msvm_EmulatedEthernetPortSettingData.AllocationUnits
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantity
- Msvm_EmulatedEthernetPortSettingData.Reservation
- Msvm_EmulatedEthernetPortSettingData.Limit
- Msvm_EmulatedEthernetPortSettingData.Weight
- Msvm_EmulatedEthernetPortSettingData.AutomaticAllocation
- Msvm_EmulatedEthernetPortSettingData.AutomaticDeallocation
- Msvm_EmulatedEthernetPortSettingData.Parent
- Msvm_EmulatedEthernetPortSettingData.Connection
- Msvm_EmulatedEthernetPortSettingData.Address
- Msvm_EmulatedEthernetPortSettingData.MappingBehavior
- Msvm_EmulatedEthernetPortSettingData.AddressOnParent
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantityUnits
- Msvm_EmulatedEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_EmulatedEthernetPortSettingData.OtherEndpointMode
- Msvm_EmulatedEthernetPortSettingData.StaticMacAddress
- Msvm_EmulatedEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f80a1f14f7a5bd388aec747f19ef84ecf0a32b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898646"
---
# <a name="msvm_emulatedethernetportsettingdata-class"></a><span data-ttu-id="a2224-103">\_Класс мсвм емулатедесернетпортсеттингдата</span><span class="sxs-lookup"><span data-stu-id="a2224-103">Msvm\_EmulatedEthernetPortSettingData class</span></span>

<span data-ttu-id="a2224-104">Представляет настроенное состояние эмулированного адаптера Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a2224-104">Represents the configured state of an emulated Ethernet adapter.</span></span>

<span data-ttu-id="a2224-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a2224-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2224-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2224-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  Caption = "Ethernet Port";
  string  Description = "Settings for the Microsoft Emulated Ethernet Port";
  string  InstanceID = "Microsoft:VMID\VDID\device-specific-data";
  string  ElementName = "Ethernet Port";
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft Emulated Ethernet Port";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Ports";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  boolean StaticMacAddress = TRUE;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="a2224-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a2224-107">Members</span></span>

<span data-ttu-id="a2224-108">Класс **мсвм \_ емулатедесернетпортсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a2224-108">The **Msvm\_EmulatedEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a2224-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2224-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2224-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2224-110">Properties</span></span>

<span data-ttu-id="a2224-111">Класс **мсвм \_ емулатедесернетпортсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a2224-111">The **Msvm\_EmulatedEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2224-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="a2224-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="a2224-115">The address of the resource.</span></span> <span data-ttu-id="a2224-116">Например, MAC-адрес порта Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a2224-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="a2224-117">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a2224-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="a2224-118">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a2224-118">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-119">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="a2224-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-122">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="a2224-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="a2224-123">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="a2224-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="a2224-124">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a2224-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a2224-125">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="a2224-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-128">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="a2224-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="a2224-129">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение "Ports".</span><span class="sxs-lookup"><span data-stu-id="a2224-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Ports".</span></span>

</dd> <dt>

<span data-ttu-id="a2224-130">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="a2224-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-131">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2224-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-133">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="a2224-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="a2224-134">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="a2224-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-135">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="a2224-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-136">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2224-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-138">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="a2224-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="a2224-139">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="a2224-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-140">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a2224-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-143">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a2224-143">A short description of the object.</span></span> <span data-ttu-id="a2224-144">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "порт Ethernet".</span><span class="sxs-lookup"><span data-stu-id="a2224-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="a2224-145">**клустермониторед**</span><span class="sxs-lookup"><span data-stu-id="a2224-145">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-146">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2224-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-148">Указывает, наблюдает ли этот адаптер Ethernet в кластере.</span><span class="sxs-lookup"><span data-stu-id="a2224-148">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="a2224-149">Это свойство по умолчанию имеет значение true, если не настроено.</span><span class="sxs-lookup"><span data-stu-id="a2224-149">This property defaults to true if not configured.</span></span>

<span data-ttu-id="a2224-150">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a2224-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="a2224-151">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="a2224-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-152">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="a2224-152">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-153">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a2224-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a2224-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-155">Объект, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="a2224-155">The thing to which this resource is connected.</span></span> <span data-ttu-id="a2224-156">Например, именованная сеть или порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="a2224-156">For example, a named network or switch port.</span></span> <span data-ttu-id="a2224-157">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a2224-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="a2224-158">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a2224-158">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-159">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="a2224-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-160">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2224-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-162">Описывает видимость пользователей для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="a2224-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="a2224-163">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 3 (виртуализированное).</span><span class="sxs-lookup"><span data-stu-id="a2224-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="a2224-164">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a2224-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-167">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a2224-167">A description of the object.</span></span> <span data-ttu-id="a2224-168">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Settings для порта Microsoft эмулированного Ethernet".</span><span class="sxs-lookup"><span data-stu-id="a2224-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="a2224-169">**десиредвланендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="a2224-169">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-170">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2224-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-172">Режим требуемой конфигурации для конечной точки VLAN.</span><span class="sxs-lookup"><span data-stu-id="a2224-172">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="a2224-173">Это свойство используется для установки начального значения свойства **оператионалендпоинтмоде** в экземпляре класса [**мсвм \_ вланендпоинт**](msvm-vlanendpoint.md) , связанного с целевым портом Ethernet.</span><span class="sxs-lookup"><span data-stu-id="a2224-173">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="a2224-174">Возможные значения см. в свойстве **оператионалендпоинтмоде** класса **мсвм \_ вланендпоинт** .</span><span class="sxs-lookup"><span data-stu-id="a2224-174">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="a2224-175">Это свойство наследуется от **CIM \_ есернетпорталлокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="a2224-175">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-176">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a2224-176">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-179">Настраиваемое пользователем отображаемое имя для устройства, с которым связан этот экземпляр РАСД.</span><span class="sxs-lookup"><span data-stu-id="a2224-179">The user-configurable display name for the device this RASD instance is associated with.</span></span> <span data-ttu-id="a2224-180">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и имеет значение "порт Ethernet".</span><span class="sxs-lookup"><span data-stu-id="a2224-180">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is set to "Ethernet Port".</span></span> <span data-ttu-id="a2224-181">Изменение этого свойства приведет к изменению имени элемента связанного логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a2224-181">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="a2224-182">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a2224-182">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-183">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="a2224-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-184">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a2224-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a2224-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-186">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a2224-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a2224-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-190">В пределах области создания экземпляра пространства имен **InstanceId** непрозрачно и уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="a2224-190">Within the scope of the instantiating namespace, **InstanceID** opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a2224-191">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение "Microsoft:*VMID* \\ *ВДИД* \\ *Device-by-Data (специфические данные)*".</span><span class="sxs-lookup"><span data-stu-id="a2224-191">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*VMID*\\*VDID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="a2224-192">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="a2224-192">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-193">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2224-193">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-195">Верхняя граница или максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="a2224-195">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="a2224-196">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="a2224-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-197">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="a2224-197">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2224-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-200">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="a2224-200">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="a2224-201">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="a2224-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-202">**осерендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="a2224-202">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-205">Строка, описывающая тип модели конечной точки VLAN, поддерживаемой этой конечной точкой VLAN.</span><span class="sxs-lookup"><span data-stu-id="a2224-205">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="a2224-206">Это свойство используется только в том случае, если свойство **десиредвланендпоинтмоде** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="a2224-206">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="a2224-207">Это свойство должно иметь значение **null** , если свойство **десиредвланендпоинтмоде** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="a2224-207">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="a2224-208">Это свойство наследуется от **CIM \_ есернетпорталлокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="a2224-208">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-209">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="a2224-209">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-212">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а ResourceType имеет значение 0 ("Other").</span><span class="sxs-lookup"><span data-stu-id="a2224-212">A string that describes the resource type when a well-defined value is not available and ResourceType is set to 0 ("Other").</span></span> <span data-ttu-id="a2224-213">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и не используется.</span><span class="sxs-lookup"><span data-stu-id="a2224-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-214">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="a2224-214">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-217">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="a2224-217">The parent of the resource.</span></span> <span data-ttu-id="a2224-218">Например, контроллер для текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="a2224-218">For example, a controller for the current allocation.</span></span> <span data-ttu-id="a2224-219">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a2224-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a2224-220">**пулид**</span><span class="sxs-lookup"><span data-stu-id="a2224-220">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-223">Пул, из которого в данный момент выделяется ресурс, или пул, от которого будет выделяться ресурс при выделении.</span><span class="sxs-lookup"><span data-stu-id="a2224-223">The pool the resource is currently allocated from, or the pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="a2224-224">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a2224-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a2224-225">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="a2224-225">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-226">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2224-226">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-228">Объем ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="a2224-228">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="a2224-229">В системах, поддерживающих чрезмерное использование ресурсов, это значение обычно используется для управления допуском, чтобы предотвратить принятие выделения.</span><span class="sxs-lookup"><span data-stu-id="a2224-229">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="a2224-230">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="a2224-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-231">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="a2224-231">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-234">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="a2224-234">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="a2224-235">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2224-235">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="a2224-236">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение "порт эмуляции Ethernet (Майкрософт)".</span><span class="sxs-lookup"><span data-stu-id="a2224-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="a2224-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="a2224-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-238">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2224-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-240">Тип ресурса, к которому применяется этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a2224-240">The type of resource this setting applies to.</span></span> <span data-ttu-id="a2224-241">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 10 (Ethernet Adapter).</span><span class="sxs-lookup"><span data-stu-id="a2224-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="a2224-242">**статикмакаддресс**</span><span class="sxs-lookup"><span data-stu-id="a2224-242">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-243">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2224-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-245">Указывает, следует ли использовать статический MAC-адрес.</span><span class="sxs-lookup"><span data-stu-id="a2224-245">Indicates whether to use a static MAC address.</span></span>

<span data-ttu-id="a2224-246">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a2224-246">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-247">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="a2224-247">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-248">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a2224-248">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-250">Количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="a2224-250">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="a2224-251">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="a2224-251">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="a2224-252">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="a2224-252">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-253">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2224-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-255">Задает единицу измерения для этого выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2224-255">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="a2224-256">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a2224-256">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="a2224-257">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="a2224-257">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a2224-258">**Weight**</span><span class="sxs-lookup"><span data-stu-id="a2224-258">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2224-259">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2224-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2224-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2224-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2224-261">Относительный приоритет для этого выделения относительно других выделений из того же ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="a2224-261">A relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="a2224-262">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="a2224-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2224-263">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2224-263">Remarks</span></span>

<span data-ttu-id="a2224-264">Доступ к классу **\_ емулатедесернетпортсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="a2224-264">Access to the **Msvm\_EmulatedEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a2224-265">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a2224-265">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="a2224-266">Примеры</span><span class="sxs-lookup"><span data-stu-id="a2224-266">Examples</span></span>

<span data-ttu-id="a2224-267">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a2224-267">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2224-268">Требования</span><span class="sxs-lookup"><span data-stu-id="a2224-268">Requirements</span></span>



| <span data-ttu-id="a2224-269">Требование</span><span class="sxs-lookup"><span data-stu-id="a2224-269">Requirement</span></span> | <span data-ttu-id="a2224-270">Значение</span><span class="sxs-lookup"><span data-stu-id="a2224-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2224-271">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2224-271">Minimum supported client</span></span><br/> | <span data-ttu-id="a2224-272">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a2224-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a2224-273">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2224-273">Minimum supported server</span></span><br/> | <span data-ttu-id="a2224-274">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a2224-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2224-275">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a2224-275">Namespace</span></span><br/>                | <span data-ttu-id="a2224-276">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a2224-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a2224-277">MOF</span><span class="sxs-lookup"><span data-stu-id="a2224-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2224-278"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2224-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2224-279">DLL</span><span class="sxs-lookup"><span data-stu-id="a2224-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2224-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2224-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2224-281">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2224-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2224-282">**\_ЕСЕРНЕТПОРТАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="a2224-282">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="a2224-283">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="a2224-283">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

