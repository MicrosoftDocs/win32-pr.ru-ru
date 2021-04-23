---
description: Представляет настроенное состояние искусственного адаптера Ethernet.
ms.assetid: BE895BAF-7766-43A2-9659-3ABA97A16134
title: Класс Msvm_SyntheticEthernetPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPortSettingData
- Msvm_SyntheticEthernetPortSettingData.InstanceID
- Msvm_SyntheticEthernetPortSettingData.Caption
- Msvm_SyntheticEthernetPortSettingData.Description
- Msvm_SyntheticEthernetPortSettingData.ElementName
- Msvm_SyntheticEthernetPortSettingData.ResourceType
- Msvm_SyntheticEthernetPortSettingData.OtherResourceType
- Msvm_SyntheticEthernetPortSettingData.ResourceSubType
- Msvm_SyntheticEthernetPortSettingData.PoolID
- Msvm_SyntheticEthernetPortSettingData.ConsumerVisibility
- Msvm_SyntheticEthernetPortSettingData.HostResource
- Msvm_SyntheticEthernetPortSettingData.AllocationUnits
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantity
- Msvm_SyntheticEthernetPortSettingData.Reservation
- Msvm_SyntheticEthernetPortSettingData.Limit
- Msvm_SyntheticEthernetPortSettingData.Weight
- Msvm_SyntheticEthernetPortSettingData.AutomaticAllocation
- Msvm_SyntheticEthernetPortSettingData.AutomaticDeallocation
- Msvm_SyntheticEthernetPortSettingData.Parent
- Msvm_SyntheticEthernetPortSettingData.Connection
- Msvm_SyntheticEthernetPortSettingData.Address
- Msvm_SyntheticEthernetPortSettingData.MappingBehavior
- Msvm_SyntheticEthernetPortSettingData.AddressOnParent
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_SyntheticEthernetPortSettingData.OtherEndpointMode
- Msvm_SyntheticEthernetPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticEthernetPortSettingData.DeviceNamingEnabled
- Msvm_SyntheticEthernetPortSettingData.AllowPacketDirect
- Msvm_SyntheticEthernetPortSettingData.StaticMacAddress
- Msvm_SyntheticEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5b31b02782c0f215f70f3bb5d2767b01294c7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682516"
---
# <a name="msvm_syntheticethernetportsettingdata-class"></a><span data-ttu-id="943fb-103">\_Класс мсвм синсетицесернетпортсеттингдата</span><span class="sxs-lookup"><span data-stu-id="943fb-103">Msvm\_SyntheticEthernetPortSettingData class</span></span>

<span data-ttu-id="943fb-104">Представляет настроенное состояние искусственного адаптера Ethernet.</span><span class="sxs-lookup"><span data-stu-id="943fb-104">Represents the configured state of a synthetic Ethernet adapter.</span></span>

<span data-ttu-id="943fb-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="943fb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="943fb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="943fb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Ethernet Port Default Settings";
  string  Description = "Describes the default settings for the virtual Ethernet port resources.";
  string  ElementName;
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic Ethernet Port";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  string  VirtualSystemIdentifiers[];
  boolean DeviceNamingEnabled = FALSE;
  boolean AllowPacketDirect = FALSE;
  boolean StaticMacAddress = False;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="943fb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="943fb-107">Members</span></span>

<span data-ttu-id="943fb-108">Класс **мсвм \_ синсетицесернетпортсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="943fb-108">The **Msvm\_SyntheticEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="943fb-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="943fb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="943fb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="943fb-110">Properties</span></span>

<span data-ttu-id="943fb-111">Класс **мсвм \_ синсетицесернетпортсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="943fb-111">The **Msvm\_SyntheticEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="943fb-112">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="943fb-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-115">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="943fb-115">The address of the resource.</span></span> <span data-ttu-id="943fb-116">Например, MAC-адрес порта Ethernet.</span><span class="sxs-lookup"><span data-stu-id="943fb-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="943fb-117">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-118">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="943fb-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-121">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="943fb-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="943fb-122">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="943fb-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="943fb-123">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-124">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="943fb-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-127">Единицы распределения, используемые свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="943fb-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="943fb-128">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-129">**алловпаккетдирект**</span><span class="sxs-lookup"><span data-stu-id="943fb-129">**AllowPacketDirect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-130">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="943fb-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="943fb-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="943fb-132">Указывает, включена ли проекция PacketDirect для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="943fb-132">Indicates if PacketDirect projection is enabled for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="943fb-133">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="943fb-133">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="943fb-134">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="943fb-134">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-135">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="943fb-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-137">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="943fb-137">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="943fb-138">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-139">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="943fb-139">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-140">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="943fb-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-142">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="943fb-142">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="943fb-143">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-143">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-144">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="943fb-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-147">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="943fb-147">A short description of the object.</span></span> <span data-ttu-id="943fb-148">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="943fb-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-149">**клустермониторед**</span><span class="sxs-lookup"><span data-stu-id="943fb-149">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-150">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="943fb-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-152">Указывает, наблюдает ли этот адаптер Ethernet в кластере.</span><span class="sxs-lookup"><span data-stu-id="943fb-152">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="943fb-153">Это свойство по умолчанию имеет значение true, если не настроено.</span><span class="sxs-lookup"><span data-stu-id="943fb-153">This property defaults to true if not configured.</span></span>

<span data-ttu-id="943fb-154">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="943fb-154">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="943fb-155">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="943fb-155">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="943fb-156">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="943fb-156">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-157">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="943fb-157">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="943fb-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-159">Объект, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="943fb-159">The thing to which this resource is connected.</span></span> <span data-ttu-id="943fb-160">Например, именованная сеть или порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="943fb-160">For example, a named network or switch port.</span></span> <span data-ttu-id="943fb-161">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-161">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-162">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="943fb-162">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="943fb-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-165">Пользователи могут видеть выделенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="943fb-165">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="943fb-166">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 3 (виртуализированное).</span><span class="sxs-lookup"><span data-stu-id="943fb-166">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-167">**Описание**</span><span class="sxs-lookup"><span data-stu-id="943fb-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-170">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="943fb-170">A description of the object.</span></span> <span data-ttu-id="943fb-171">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="943fb-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-172">**десиредвланендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="943fb-172">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-173">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="943fb-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-175">Режим требуемой конфигурации для конечной точки VLAN.</span><span class="sxs-lookup"><span data-stu-id="943fb-175">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="943fb-176">Это свойство используется для задания значения начального свойства **оператионалендпоинтмоде** в экземпляре класса [**мсвм \_ вланендпоинт**](msvm-vlanendpoint.md) , связанного с целевым портом Ethernet.</span><span class="sxs-lookup"><span data-stu-id="943fb-176">This property is used to set the initial **OperationalEndpointMode** property value in the instance of the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="943fb-177">Возможные значения см. в свойстве **оператионалендпоинтмоде** класса **мсвм \_ вланендпоинт** .</span><span class="sxs-lookup"><span data-stu-id="943fb-177">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="943fb-178">Это свойство наследуется от **CIM \_ есернетпорталлокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="943fb-178">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="943fb-179">**девиценаминженаблед**</span><span class="sxs-lookup"><span data-stu-id="943fb-179">**DeviceNamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-180">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="943fb-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-182">Указывает, поддерживает ли адаптер Ethernet именование устройств.</span><span class="sxs-lookup"><span data-stu-id="943fb-182">Indicates whether this ethernet adapter supports device naming.</span></span>

<span data-ttu-id="943fb-183">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифивиртуалсистемресаурцес**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="943fb-183">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="943fb-184">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="943fb-184">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="943fb-185">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="943fb-185">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-188">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="943fb-188">A short description of the object.</span></span> <span data-ttu-id="943fb-189">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="943fb-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-190">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="943fb-190">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-191">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="943fb-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="943fb-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-193">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="943fb-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="943fb-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="943fb-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="943fb-197">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="943fb-197">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="943fb-198">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="943fb-198">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="943fb-199">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="943fb-199">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-200">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="943fb-200">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-201">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="943fb-201">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-203">Верхняя граница или максимальный объем ресурса, который будет предоставлен для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="943fb-203">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="943fb-204">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-205">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="943fb-205">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-206">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="943fb-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-208">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="943fb-208">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="943fb-209">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-210">**осерендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="943fb-210">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-213">Строка, описывающая тип модели конечной точки VLAN, поддерживаемой этой конечной точкой VLAN.</span><span class="sxs-lookup"><span data-stu-id="943fb-213">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="943fb-214">Это свойство используется только в том случае, если свойство **десиредвланендпоинтмоде** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="943fb-214">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="943fb-215">Это свойство должно иметь значение **null** , если свойство **десиредвланендпоинтмоде** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="943fb-215">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="943fb-216">Это свойство наследуется от **CIM \_ есернетпорталлокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="943fb-216">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="943fb-217">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="943fb-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-220">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение "Other" (0).</span><span class="sxs-lookup"><span data-stu-id="943fb-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to "Other" (0).</span></span> <span data-ttu-id="943fb-221">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и не используется.</span><span class="sxs-lookup"><span data-stu-id="943fb-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="943fb-222">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="943fb-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-225">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="943fb-225">The parent of the resource.</span></span> <span data-ttu-id="943fb-226">Например, контроллер для текущего выделения.</span><span class="sxs-lookup"><span data-stu-id="943fb-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="943fb-227">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-228">**пулид**</span><span class="sxs-lookup"><span data-stu-id="943fb-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-231">Пул, из которого в данный момент выделяется ресурс, или пул, от которого будет выделяться ресурс при выделении.</span><span class="sxs-lookup"><span data-stu-id="943fb-231">The pool the resource is currently allocated from, or which pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="943fb-232">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-233">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="943fb-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-234">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="943fb-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-236">Объем ресурсов, которые гарантированно будут доступны для этого выделения.</span><span class="sxs-lookup"><span data-stu-id="943fb-236">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="943fb-237">В системах, поддерживающих чрезмерное использование ресурсов, это значение обычно используется для управления допуском, чтобы предотвратить принятие выделения.</span><span class="sxs-lookup"><span data-stu-id="943fb-237">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="943fb-238">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="943fb-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-242">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="943fb-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="943fb-243">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="943fb-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="943fb-244">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="943fb-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-246">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="943fb-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-248">Тип ресурса, к которому применяется этот параметр.</span><span class="sxs-lookup"><span data-stu-id="943fb-248">The type of resource this setting applies to.</span></span> <span data-ttu-id="943fb-249">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 10 (Ethernet Adapter).</span><span class="sxs-lookup"><span data-stu-id="943fb-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-250">**статикмакаддресс**</span><span class="sxs-lookup"><span data-stu-id="943fb-250">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-251">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="943fb-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-253">Указывает, является ли MAC-адрес статическим.</span><span class="sxs-lookup"><span data-stu-id="943fb-253">Specifies if the MAC address is static.</span></span>

</dd> <dt>

<span data-ttu-id="943fb-254">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="943fb-254">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-255">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="943fb-255">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-257">Количество ресурсов, представленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="943fb-257">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="943fb-258">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-259">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="943fb-259">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-260">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="943fb-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-262">Задает единицу измерения для свойства **виртуалкуантити** .</span><span class="sxs-lookup"><span data-stu-id="943fb-262">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="943fb-263">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="943fb-263">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="943fb-264">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-264">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-265">**виртуалсистемидентифиерс**</span><span class="sxs-lookup"><span data-stu-id="943fb-265">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-266">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="943fb-266">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="943fb-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="943fb-268">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="943fb-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="943fb-269">Строковый массив идентификаторов этого ресурса, представленный операционной системе виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="943fb-269">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="943fb-270">Индексы и значения для каждого индекса определяются на основе каждого ресурса (то есть для каждого перечислимого значения свойства **ResourceType** ).</span><span class="sxs-lookup"><span data-stu-id="943fb-270">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** property value).</span></span>

</dd> <dt>

<span data-ttu-id="943fb-271">**Weight**</span><span class="sxs-lookup"><span data-stu-id="943fb-271">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="943fb-272">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="943fb-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="943fb-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="943fb-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="943fb-274">Относительный приоритет для этого выделения относительно других выделений из того же пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="943fb-274">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="943fb-275">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="943fb-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="943fb-276">Комментарии</span><span class="sxs-lookup"><span data-stu-id="943fb-276">Remarks</span></span>

<span data-ttu-id="943fb-277">Доступ к классу **\_ синсетицесернетпортсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="943fb-277">Access to the **Msvm\_SyntheticEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="943fb-278">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="943fb-278">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="943fb-279">Примеры</span><span class="sxs-lookup"><span data-stu-id="943fb-279">Examples</span></span>

<span data-ttu-id="943fb-280">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="943fb-280">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="943fb-281">Требования</span><span class="sxs-lookup"><span data-stu-id="943fb-281">Requirements</span></span>



| <span data-ttu-id="943fb-282">Требование</span><span class="sxs-lookup"><span data-stu-id="943fb-282">Requirement</span></span> | <span data-ttu-id="943fb-283">Значение</span><span class="sxs-lookup"><span data-stu-id="943fb-283">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="943fb-284">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="943fb-284">Minimum supported client</span></span><br/> | <span data-ttu-id="943fb-285">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="943fb-285">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="943fb-286">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="943fb-286">Minimum supported server</span></span><br/> | <span data-ttu-id="943fb-287">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="943fb-287">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="943fb-288">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="943fb-288">Namespace</span></span><br/>                | <span data-ttu-id="943fb-289">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="943fb-289">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="943fb-290">MOF</span><span class="sxs-lookup"><span data-stu-id="943fb-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="943fb-291"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="943fb-291"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="943fb-292">DLL</span><span class="sxs-lookup"><span data-stu-id="943fb-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="943fb-293"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="943fb-293"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="943fb-294">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="943fb-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943fb-295">**\_ЕСЕРНЕТПОРТАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="943fb-295">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="943fb-296">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="943fb-296">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

