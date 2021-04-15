---
description: Представляет запрос на выделение для статического или динамического порта коммутатора или представляет активную конфигурацию выделенного в данный момент статического или динамического порта коммутатора.
ms.assetid: ef70b72f-75a0-448e-a648-6a28c12f0da1
title: Класс Msvm_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortAllocationSettingData
- Msvm_EthernetPortAllocationSettingData.InstanceID
- Msvm_EthernetPortAllocationSettingData.Caption
- Msvm_EthernetPortAllocationSettingData.Description
- Msvm_EthernetPortAllocationSettingData.ElementName
- Msvm_EthernetPortAllocationSettingData.ResourceType
- Msvm_EthernetPortAllocationSettingData.OtherResourceType
- Msvm_EthernetPortAllocationSettingData.ResourceSubType
- Msvm_EthernetPortAllocationSettingData.PoolID
- Msvm_EthernetPortAllocationSettingData.ConsumerVisibility
- Msvm_EthernetPortAllocationSettingData.HostResource
- Msvm_EthernetPortAllocationSettingData.AllocationUnits
- Msvm_EthernetPortAllocationSettingData.VirtualQuantity
- Msvm_EthernetPortAllocationSettingData.Reservation
- Msvm_EthernetPortAllocationSettingData.Limit
- Msvm_EthernetPortAllocationSettingData.Weight
- Msvm_EthernetPortAllocationSettingData.AutomaticAllocation
- Msvm_EthernetPortAllocationSettingData.AutomaticDeallocation
- Msvm_EthernetPortAllocationSettingData.Parent
- Msvm_EthernetPortAllocationSettingData.Connection
- Msvm_EthernetPortAllocationSettingData.Address
- Msvm_EthernetPortAllocationSettingData.MappingBehavior
- Msvm_EthernetPortAllocationSettingData.AddressOnParent
- Msvm_EthernetPortAllocationSettingData.VirtualQuantityUnits
- Msvm_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- Msvm_EthernetPortAllocationSettingData.OtherEndpointMode
- Msvm_EthernetPortAllocationSettingData.EnabledState
- Msvm_EthernetPortAllocationSettingData.LastKnownSwitchName
- Msvm_EthernetPortAllocationSettingData.RequiredFeatures
- Msvm_EthernetPortAllocationSettingData.RequiredFeatureHints
- Msvm_EthernetPortAllocationSettingData.TestReplicaPoolID
- Msvm_EthernetPortAllocationSettingData.TestReplicaSwitchName
- Msvm_EthernetPortAllocationSettingData.CompartmentGuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a310daf30127aec5069efcf7ca4fd5ead9277e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683552"
---
# <a name="msvm_ethernetportallocationsettingdata-class"></a><span data-ttu-id="8a5e1-103">\_Класс мсвм есернетпорталлокатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="8a5e1-103">Msvm\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="8a5e1-104">Представляет запрос на выделение для статического или динамического порта коммутатора или представляет активную конфигурацию выделенного в данный момент статического или динамического порта коммутатора.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-104">Represents an allocation request for a static or dynamic switch port, or represents the active configuration of a currently allocated static or dynamic switch port.</span></span> <span data-ttu-id="8a5e1-105">Запрос на выделение порта динамического коммутатора также называется запросом на соединение.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-105">An allocation request for a dynamic switch port is also known as a connection request.</span></span>

<span data-ttu-id="8a5e1-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5e1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a5e1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortAllocationSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Ethernet Switch Port Settings";
  string  Description = "Ethernet Switch Port Settings";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight = 0;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  uint16  EnabledState;
  string  LastKnownSwitchName;
  string  RequiredFeatures[];
  string  RequiredFeatureHints[];
  string  TestReplicaPoolID;
  string  TestReplicaSwitchName;
  string  CompartmentGuid;
};
```

## <a name="members"></a><span data-ttu-id="8a5e1-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8a5e1-108">Members</span></span>

<span data-ttu-id="8a5e1-109">Класс **мсвм \_ есернетпорталлокатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8a5e1-109">The **Msvm\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8a5e1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8a5e1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a5e1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="8a5e1-111">Properties</span></span>

<span data-ttu-id="8a5e1-112">Класс **мсвм \_ есернетпорталлокатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-112">The **Msvm\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a5e1-113">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-116">Адрес ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-116">The address of the resource.</span></span> <span data-ttu-id="8a5e1-117">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-118">**аддрессонпарент**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-121">Описывает адрес этого ресурса в контексте родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="8a5e1-122">Свойства **Parent** и **аддрессонпарент** используются для описания отношения контроллера, а также порядка устройств на контроллере.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="8a5e1-123">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-124">**аллокатионунитс**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-127">Единица распределения, используемая свойствами **резервирования** и **ограничения** .</span><span class="sxs-lookup"><span data-stu-id="8a5e1-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="8a5e1-128">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-129">**аутоматикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-130">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-132">Указывает, будет ли ресурс автоматически выделен.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="8a5e1-133">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-134">**аутоматикдеаллокатион**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-135">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-137">Указывает, будет ли ресурс автоматически освобожден.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="8a5e1-138">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-139">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-142">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="8a5e1-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-143">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-143">A short description of the object.</span></span> <span data-ttu-id="8a5e1-144">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="8a5e1-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-145">**компартментгуид**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-145">**CompartmentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8a5e1-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-148">Это свойство указывает целевой сегмент сети для порта.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-148">This property specifies the target network compartment for the port.</span></span> <span data-ttu-id="8a5e1-149">Поддерживается только для внутренних адаптеров.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-149">It is only supported for internal adapters.</span></span>

> [!Note]  
> <span data-ttu-id="8a5e1-150">Свойство добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-150">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="8a5e1-151">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-151">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-152">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-154">Устройство, к которому подключен этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-154">The device to which this resource is connected.</span></span> <span data-ttu-id="8a5e1-155">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-156">**консумервисибилити**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-156">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-157">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-159">Видимость потребителя для выделенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-159">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="8a5e1-160">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 3 (виртуализированное).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-160">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-161">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-164">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-164">A description of the object.</span></span> <span data-ttu-id="8a5e1-165">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="8a5e1-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-166">**десиредвланендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-166">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-169">Режим требуемой конфигурации для конечной точки VLAN.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-169">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="8a5e1-170">Это свойство используется для установки начального значения свойства **оператионалендпоинтмоде** в экземпляре класса [**мсвм \_ вланендпоинт**](msvm-vlanendpoint.md) , связанного с целевым портом Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-170">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="8a5e1-171">Возможные значения см. в свойстве **оператионалендпоинтмоде** класса **мсвм \_ вланендпоинт** .</span><span class="sxs-lookup"><span data-stu-id="8a5e1-171">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="8a5e1-172">Это свойство наследуется от **CIM \_ есернетпорталлокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-172">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-176">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-176">A display name for the object.</span></span> <span data-ttu-id="8a5e1-177">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="8a5e1-178">Изменение этого свойства приведет к изменению имени элемента связанного логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-178">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-180">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-182">Указывает, включен или отключен запрос на выделение.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-182">Indicates whether the allocation request is enabled or disabled.</span></span> <span data-ttu-id="8a5e1-183">Если запрос на выделение помечен как отключенный (3), выделение не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-183">When an allocation request is marked as Disabled (3), then the allocation is not processed.</span></span> <span data-ttu-id="8a5e1-184">Значение **EnabledState** для активной конфигурации всегда помечается как включенное (2).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-184">The **EnabledState** for an active configuration is always marked as Enabled (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8a5e1-185">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="8a5e1-185">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8a5e1-186">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="8a5e1-186">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a5e1-187">**хостресаурце**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-187">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-188">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-188">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-190">Каждому устройству в виртуальном коммутаторе можно назначить только один ресурс узла, поэтому можно установить только первый элемент этого массива.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-190">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="8a5e1-191">Для устройств, поддерживающих эту функцию, установите первый элемент массива **хостресаурце** , чтобы он содержал ссылку на базовый ресурс узла, который нужно назначить.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-191">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="8a5e1-192">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-196">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-197">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8a5e1-198">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение "Microsoft:*GUID* \\ *девицеспеЦификдата*".</span><span class="sxs-lookup"><span data-stu-id="8a5e1-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-199">**ласткновнсвитчнаме**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-199">**LastKnownSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-202">Последнее известное понятное имя коммутатора с жестким соответствием для этого порта, если таковое имеется.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-202">The last known friendly name of the switch this port had a hard affinity to, if any.</span></span>

> [!Note]  
> <span data-ttu-id="8a5e1-203">Свойство добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-203">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="8a5e1-204">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-204">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-205">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-207">Максимальный объем соответствующих ресурсов узла, которые могут использоваться виртуальным коммутатором.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-207">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="8a5e1-208">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-209">**маппингбехавиор**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-209">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-210">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-212">Указывает, как этот ресурс сопоставляется с базовыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-212">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="8a5e1-213">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-214">**осерендпоинтмоде**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-214">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-217">Строка, описывающая тип модели конечной точки VLAN, поддерживаемой этой конечной точкой VLAN.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-217">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="8a5e1-218">Это свойство используется только в том случае, если свойство **десиредвланендпоинтмоде** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-218">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="8a5e1-219">Это свойство должно иметь значение **null** , если свойство **десиредвланендпоинтмоде** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-219">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="8a5e1-220">Это свойство наследуется от **CIM \_ есернетпорталлокатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-220">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-221">**осерресаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-221">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-224">Строка, описывающая тип ресурса, если четко определенное значение недоступно, а [**ResourceType**](msvm-processorsettingdata.md) имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-224">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="8a5e1-225">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и не используется.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-226">**Родительский объект**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-226">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-229">Родительский объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-229">The parent of the resource.</span></span> <span data-ttu-id="8a5e1-230">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-231">**пулид**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-231">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-234">Идентификатор пула ресурсов, из которого был выделен ресурс.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-234">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="8a5e1-235">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-236">**рекуиредфеатурехинтс**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-236">**RequiredFeatureHints**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-237">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-239">Список отображаемых имен, соответствующих каждой записи в массиве **рекуиредфеатурес** .</span><span class="sxs-lookup"><span data-stu-id="8a5e1-239">The list of display names that correspond to each entry in the **RequiredFeatures** array.</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-240">**рекуиредфеатурес**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-240">**RequiredFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-241">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-242">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8a5e1-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-243">Список идентификаторов компонентов, которые представляют все функции, необходимые для порта.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-243">The list of feature identifiers that represent all the features that are required for a port.</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-244">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-244">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-245">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-247">Объем ресурсов, зарезервированных для использования виртуальным коммутатором.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-247">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="8a5e1-248">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-249">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-249">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-250">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-252">Строка, описывающая конкретный подтип реализации для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-252">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="8a5e1-253">Например, это можно использовать для различения разных моделей одного типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-253">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="8a5e1-254">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-255">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-255">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-256">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-258">Тип ресурса, который представляет этот параметр выделения.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-258">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="8a5e1-259">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)и всегда имеет значение 33 (подключение Ethernet).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-260">**тестрепликапулид**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-260">**TestReplicaPoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8a5e1-262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-263">Указывает пул сетевых ресурсов, из которого будет выделено подключение к системе реплики теста при ее создании.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-263">Specifies the network resource pool from which a connection will be allocated to the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-264">**тестрепликасвитчнаме**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-264">**TestReplicaSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-265">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-266">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8a5e1-266">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-267">Указывает отображаемое имя коммутатора виртуальной сети, к которому будет выделяться подключение для системы реплики теста при ее создании.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-267">Specifies the display name of the virtual network switch to which a connection will be allocated for the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-269">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-271">Общее число портов в виртуальном коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-271">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="8a5e1-272">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-273">**виртуалкуантитюнитс**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-276">Задает единицу измерения для свойства **виртуалкуантити** .</span><span class="sxs-lookup"><span data-stu-id="8a5e1-276">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="8a5e1-277">Значение этого свойства должно быть допустимым значением квалификатора программных единиц, как определено в приложении C. 1 из DSP0004 V 2.5 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="8a5e1-278">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8a5e1-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5e1-280">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a5e1-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a5e1-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8a5e1-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a5e1-282">Целое число, определяющее вес для каждого виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="8a5e1-282">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="8a5e1-283">Это свойство наследуется от [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="8a5e1-283">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="8a5e1-284">Диапазон: 0 1000</span><span class="sxs-lookup"><span data-stu-id="8a5e1-284">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a5e1-285">Требования</span><span class="sxs-lookup"><span data-stu-id="8a5e1-285">Requirements</span></span>



| <span data-ttu-id="8a5e1-286">Требование</span><span class="sxs-lookup"><span data-stu-id="8a5e1-286">Requirement</span></span> | <span data-ttu-id="8a5e1-287">Значение</span><span class="sxs-lookup"><span data-stu-id="8a5e1-287">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5e1-288">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a5e1-288">Minimum supported client</span></span><br/> | <span data-ttu-id="8a5e1-289">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8a5e1-289">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8a5e1-290">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a5e1-290">Minimum supported server</span></span><br/> | <span data-ttu-id="8a5e1-291">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8a5e1-291">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a5e1-292">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8a5e1-292">Namespace</span></span><br/>                | <span data-ttu-id="8a5e1-293">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8a5e1-293">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8a5e1-294">MOF</span><span class="sxs-lookup"><span data-stu-id="8a5e1-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a5e1-295"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a5e1-295"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a5e1-296">DLL</span><span class="sxs-lookup"><span data-stu-id="8a5e1-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a5e1-297"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a5e1-297"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

