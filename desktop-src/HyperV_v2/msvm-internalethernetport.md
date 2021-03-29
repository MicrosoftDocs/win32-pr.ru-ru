---
description: Представляет внутренний порт Ethernet (сетевой адаптер).
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Класс Msvm_InternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810426"
---
# <a name="msvm_internalethernetport-class"></a><span data-ttu-id="be8c0-103">\_Класс мсвм интерналесернетпорт</span><span class="sxs-lookup"><span data-stu-id="be8c0-103">Msvm\_InternalEthernetPort class</span></span>

<span data-ttu-id="be8c0-104">Представляет внутренний порт Ethernet (сетевой адаптер).</span><span class="sxs-lookup"><span data-stu-id="be8c0-104">Represents an internal Ethernet port (network adapter).</span></span> <span data-ttu-id="be8c0-105">Этот тип порта Ethernet предоставляет виртуальным машинам доступ к серверу виртуализации, на котором работает сетевое программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="be8c0-105">This type of Ethernet port gives virtual machines access to the virtualization server running the networking software.</span></span> <span data-ttu-id="be8c0-106">Внутренние сетевые адаптеры позволяют маршрутизировать или фильтровать сетевой трафик виртуальных машин до выхода из физической системы.</span><span class="sxs-lookup"><span data-stu-id="be8c0-106">The internal network adapters allow the virtual machines network traffic to be routed or filtered before leaving the physical system.</span></span>

<span data-ttu-id="be8c0-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="be8c0-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8c0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be8c0-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_InternalEthernetPort";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="be8c0-109">Члены</span><span class="sxs-lookup"><span data-stu-id="be8c0-109">Members</span></span>

<span data-ttu-id="be8c0-110">Класс **мсвм \_ интерналесернетпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be8c0-110">The **Msvm\_InternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="be8c0-111">Методы</span><span class="sxs-lookup"><span data-stu-id="be8c0-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="be8c0-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="be8c0-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="be8c0-113">Методы</span><span class="sxs-lookup"><span data-stu-id="be8c0-113">Methods</span></span>

<span data-ttu-id="be8c0-114">Класс **мсвм \_ интерналесернетпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="be8c0-114">The **Msvm\_InternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="be8c0-115">Метод</span><span class="sxs-lookup"><span data-stu-id="be8c0-115">Method</span></span>                                                                     | <span data-ttu-id="be8c0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="be8c0-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="be8c0-117">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="be8c0-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="be8c0-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="be8c0-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="be8c0-119">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="be8c0-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="be8c0-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="be8c0-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="be8c0-121">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="be8c0-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="be8c0-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="be8c0-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="be8c0-123">**Равен**</span><span class="sxs-lookup"><span data-stu-id="be8c0-123">**RequestStateChange**</span></span>](msvm-internalethernetport-requeststatechange.md) | <span data-ttu-id="be8c0-124">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="be8c0-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="be8c0-125">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="be8c0-125">**Reset**</span></span>](msvm-internalethernetport-reset.md)                           | <span data-ttu-id="be8c0-126">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="be8c0-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="be8c0-127">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="be8c0-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="be8c0-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="be8c0-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="be8c0-129">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="be8c0-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="be8c0-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="be8c0-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="be8c0-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="be8c0-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="be8c0-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="be8c0-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="be8c0-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="be8c0-133">Properties</span></span>

<span data-ttu-id="be8c0-134">Класс **мсвм \_ интерналесернетпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be8c0-134">The **Msvm\_InternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be8c0-135">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="be8c0-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-136">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be8c0-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-138">Допустимое число активных или согласованных максимальных единиц передачи (MTU).</span><span class="sxs-lookup"><span data-stu-id="be8c0-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="be8c0-139">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-140">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="be8c0-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-141">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="be8c0-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-143">Любая дополнительная доступность и состояние устройства, кроме указанного в свойстве **Availability** .</span><span class="sxs-lookup"><span data-stu-id="be8c0-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="be8c0-144">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="be8c0-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-145">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="be8c0-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-146">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8c0-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-148">Указывает, может ли сетевой порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="be8c0-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="be8c0-149">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-150">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="be8c0-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-153">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="be8c0-153">The primary availability and status of the device.</span></span> <span data-ttu-id="be8c0-154">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-155">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="be8c0-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-156">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="be8c0-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-158">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="be8c0-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="be8c0-159">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="be8c0-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="be8c0-160">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="be8c0-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="be8c0-161">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="be8c0-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="be8c0-162">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="be8c0-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-164">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="be8c0-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-166">Возможности порта Ethernet.</span><span class="sxs-lookup"><span data-stu-id="be8c0-166">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="be8c0-167">Если в списке перечислены возможности отработки отказа или балансировки нагрузки, необходимо также определить [**CIM \_ спареграуп**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (отработку отказа) или [**CIM \_ екстракапаЦитиграуп**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (Балансировка нагрузки), чтобы полностью описать эту возможность.</span><span class="sxs-lookup"><span data-stu-id="be8c0-167">If failover or load balancing capabilities are listed, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="be8c0-168">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-168">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="be8c0-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="be8c0-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="be8c0-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Алертонлан** (2)</span><span class="sxs-lookup"><span data-stu-id="be8c0-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Вакеонлан** (3)</span><span class="sxs-lookup"><span data-stu-id="be8c0-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Отработка отказа** (4)</span><span class="sxs-lookup"><span data-stu-id="be8c0-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="be8c0-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be8c0-175">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="be8c0-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-176">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="be8c0-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-178">Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из функций порта Ethernet, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="be8c0-178">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="be8c0-179">Обратите внимание, что каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="be8c0-179">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="be8c0-180">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-181">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="be8c0-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-184">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="be8c0-184">A short description of the object.</span></span> <span data-ttu-id="be8c0-185">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-186">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="be8c0-186">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-187">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-189">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="be8c0-189">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="be8c0-190">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="be8c0-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="be8c0-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-192">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="be8c0-192">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-195">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="be8c0-195">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="be8c0-196">При использовании с другими ключевыми свойствами этого класса это свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="be8c0-196">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="be8c0-197">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="be8c0-197">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-198">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be8c0-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-201">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="be8c0-201">A description of the object.</span></span> <span data-ttu-id="be8c0-202">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-203">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="be8c0-203">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-204">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-206">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="be8c0-206">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="be8c0-207">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="be8c0-207">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="be8c0-208">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="be8c0-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-212">Адрес или другие идентифицирующие сведения, используемые для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="be8c0-212">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="be8c0-213">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение "Microsoft:*GUID* \\ ,*зависящие от устройства*".</span><span class="sxs-lookup"><span data-stu-id="be8c0-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="be8c0-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-216">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="be8c0-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-217">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="be8c0-217">A display name for the object.</span></span> <span data-ttu-id="be8c0-218">Это свойство позволяет каждому экземпляру определить отображаемое имя в дополнение к его ключевым свойствам, идентификационным данным и сведениям о описании.</span><span class="sxs-lookup"><span data-stu-id="be8c0-218">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="be8c0-219">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и создается на основе сетевого адаптера, присутствующего на узле.</span><span class="sxs-lookup"><span data-stu-id="be8c0-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) and is generated based on the NIC present in the host.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-220">**енабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="be8c0-220">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-221">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="be8c0-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-223">Указывает, какие возможности включаются в списке всех поддерживаемых, определенных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="be8c0-223">Specifies which capabilities are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="be8c0-224">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-224">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="be8c0-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="be8c0-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="be8c0-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Алертонлан** (2)</span><span class="sxs-lookup"><span data-stu-id="be8c0-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Вакеонлан** (3)</span><span class="sxs-lookup"><span data-stu-id="be8c0-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Отработка отказа** (4)</span><span class="sxs-lookup"><span data-stu-id="be8c0-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="be8c0-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be8c0-231">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="be8c0-231">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-232">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-234">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="be8c0-234">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="be8c0-235">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8c0-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="be8c0-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-237">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-239">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="be8c0-239">The enabled and disabled states of an element.</span></span> <span data-ttu-id="be8c0-240">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8c0-240">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-241">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="be8c0-241">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-242">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8c0-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-244">Указывает, что сообщение об ошибке в свойстве **ластерроркоде** теперь отключено.</span><span class="sxs-lookup"><span data-stu-id="be8c0-244">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="be8c0-245">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-246">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="be8c0-246">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-249">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="be8c0-249">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="be8c0-250">Это свойство унаследовано от [**свойства \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) property and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-251">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="be8c0-251">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-252">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8c0-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-254">Указывает, работает ли порт в режиме полного дуплекса.</span><span class="sxs-lookup"><span data-stu-id="be8c0-254">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="be8c0-255">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-255">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="be8c0-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-257">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-259">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="be8c0-259">The current health of the element.</span></span> <span data-ttu-id="be8c0-260">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="be8c0-260">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="be8c0-261">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-262">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="be8c0-262">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-263">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="be8c0-263">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-265">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="be8c0-265">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="be8c0-266">Каждая запись этого массива связана с записью в массиве свойств **осеридентифингинфо** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="be8c0-266">Each entry of this array is related to the entry in the **OtherIdentifyingInfo** property array that is located at the same index.</span></span> <span data-ttu-id="be8c0-267">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="be8c0-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-269">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be8c0-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-271">Значение **типа DateTime** , указывающее, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="be8c0-271">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="be8c0-272">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="be8c0-272">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="be8c0-273">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-274">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="be8c0-274">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-275">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-277">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="be8c0-277">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-278">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="be8c0-278">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="be8c0-279">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-279">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-280">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="be8c0-280">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-281">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be8c0-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-283">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="be8c0-283">The last error code reported by the logical device.</span></span> <span data-ttu-id="be8c0-284">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-285">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="be8c0-285">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-286">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-288">Типы ссылок.</span><span class="sxs-lookup"><span data-stu-id="be8c0-288">The types of links.</span></span> <span data-ttu-id="be8c0-289">Если задано значение 1 (другое), связанное свойство **осерлинктечнологи** содержит строковое описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="be8c0-289">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="be8c0-290">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-290">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="be8c0-291">Значение</span><span class="sxs-lookup"><span data-stu-id="be8c0-291">Value</span></span>                                                                        | <span data-ttu-id="be8c0-292">Значение</span><span class="sxs-lookup"><span data-stu-id="be8c0-292">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="be8c0-293"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="be8c0-293"><dt>2</dt></span></span> </dl> | <span data-ttu-id="be8c0-294">Ethernet</span><span class="sxs-lookup"><span data-stu-id="be8c0-294">Ethernet</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="be8c0-295">**максдатасизе**</span><span class="sxs-lookup"><span data-stu-id="be8c0-295">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-296">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be8c0-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-298">Максимальный размер поля сведений (не MAC), которое будет получено или передано.</span><span class="sxs-lookup"><span data-stu-id="be8c0-298">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="be8c0-299">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-299">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-300">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="be8c0-300">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-301">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be8c0-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-303">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-303">This property has been deprecated.</span></span> <span data-ttu-id="be8c0-304">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-305">**максспид**</span><span class="sxs-lookup"><span data-stu-id="be8c0-305">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-306">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be8c0-306">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-308">Максимальная пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="be8c0-308">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="be8c0-309">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8c0-309">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-310">**Name**</span><span class="sxs-lookup"><span data-stu-id="be8c0-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-311">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-313">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="be8c0-313">The label by which the object is known.</span></span> <span data-ttu-id="be8c0-314">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="be8c0-314">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="be8c0-315">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-316">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="be8c0-316">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-317">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="be8c0-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-319">MAC-адреса Ethernet/802.3 отформатированы как двенадцать шестнадцатеричных цифр (например, "010203040506"). Каждая пара представляет один из шести октетов MAC-адреса в каноническом порядке (бит адреса группы находится в младших битах первого символа строки). Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-319">The Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-320">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="be8c0-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-321">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-323">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="be8c0-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="be8c0-324">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="be8c0-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="be8c0-325">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="be8c0-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-327">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="be8c0-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-329">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="be8c0-329">The current statuses of the element.</span></span> <span data-ttu-id="be8c0-330">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-331">**осеренабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="be8c0-331">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-332">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="be8c0-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-334">Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из включенных возможностей, указанных как 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="be8c0-334">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="be8c0-335">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-335">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-336">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="be8c0-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-339">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое). Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="be8c0-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other.) This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="be8c0-340">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8c0-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="be8c0-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-342">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="be8c0-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-344">Любые данные в дополнение к сведениям об ИДЕНТИФИКАТОРе устройства, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="be8c0-344">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="be8c0-345">Например, это свойство можно использовать для хранения отображаемого имени операционной системы для устройства.</span><span class="sxs-lookup"><span data-stu-id="be8c0-345">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="be8c0-346">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-347">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="be8c0-347">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-348">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-350">Строковое значение, описывающее свойство **линктечнологи** , если оно имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="be8c0-350">A string value that describes the **LinkTechnology** property when it is set to 1 (Other).</span></span> <span data-ttu-id="be8c0-351">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-351">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-352">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="be8c0-352">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-355">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-355">This property is deprecated.</span></span> <span data-ttu-id="be8c0-356">Используйте свойство **portType** .</span><span class="sxs-lookup"><span data-stu-id="be8c0-356">Use the **PortType** property.</span></span> <span data-ttu-id="be8c0-357">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-357">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<span data-ttu-id="be8c0-358">Нерекомендуемое описание: тип модуля, если свойство **portType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="be8c0-358">Deprecated description: The type of module, when the **PortType** property is set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-359">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="be8c0-359">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-362">Тип модуля, если свойство **portType** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="be8c0-362">The type of module, when the **PortType** property is set to 1 (Other).</span></span> <span data-ttu-id="be8c0-363">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="be8c0-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-364">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="be8c0-364">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-365">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-367">Сетевой адрес, жестко закодированный в порт.</span><span class="sxs-lookup"><span data-stu-id="be8c0-367">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="be8c0-368">Этот адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="be8c0-368">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="be8c0-369">При внесении этого изменения поле должно быть обновлено одновременно.</span><span class="sxs-lookup"><span data-stu-id="be8c0-369">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="be8c0-370">Если для сетевого адаптера не существует жестко закодированного адреса, его следует оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="be8c0-370">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="be8c0-371">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-371">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-372">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="be8c0-372">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-373">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-375">Сетевые порты часто нумеруются относительно логического модуля или сетевого элемента.</span><span class="sxs-lookup"><span data-stu-id="be8c0-375">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="be8c0-376">Это значение равно 1 для эмулированных сетевых карт, 0 — для всех остальных.</span><span class="sxs-lookup"><span data-stu-id="be8c0-376">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="be8c0-377">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-378">**Порта**</span><span class="sxs-lookup"><span data-stu-id="be8c0-378">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-379">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-381">Конкретный режим, который в данный момент включен для порта.</span><span class="sxs-lookup"><span data-stu-id="be8c0-381">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="be8c0-382">Если задано значение 1 (другое), связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="be8c0-382">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="be8c0-383">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-383">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="be8c0-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="be8c0-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="be8c0-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 медный** (50)</span><span class="sxs-lookup"><span data-stu-id="be8c0-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BASE** (51)</span><span class="sxs-lookup"><span data-stu-id="be8c0-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BASE** (52)</span><span class="sxs-lookup"><span data-stu-id="be8c0-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BASE** (53)</span><span class="sxs-lookup"><span data-stu-id="be8c0-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="be8c0-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="be8c0-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="be8c0-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="be8c0-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="be8c0-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="be8c0-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="be8c0-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="be8c0-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="be8c0-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="be8c0-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="be8c0-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="be8c0-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-лв** (109)</span><span class="sxs-lookup"><span data-stu-id="be8c0-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="be8c0-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ать** (111)</span><span class="sxs-lookup"><span data-stu-id="be8c0-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="be8c0-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be8c0-406">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="be8c0-406">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-407">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="be8c0-407">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-409">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="be8c0-409">The power management capabilities of the device.</span></span> <span data-ttu-id="be8c0-410">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-411">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="be8c0-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-412">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="be8c0-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-414">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="be8c0-414">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="be8c0-415">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-415">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-416">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="be8c0-416">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-417">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be8c0-417">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-419">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="be8c0-419">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="be8c0-420">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-421">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="be8c0-421">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-422">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-423">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-424">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="be8c0-424">Provides high level status information.</span></span> <span data-ttu-id="be8c0-425">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="be8c0-425">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="be8c0-426">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="be8c0-426">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="be8c0-427">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-428">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="be8c0-428">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-429">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be8c0-429">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-431">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="be8c0-431">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="be8c0-432">Фактическая пропускная способность указывается в свойстве **Speed** .</span><span class="sxs-lookup"><span data-stu-id="be8c0-432">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="be8c0-433">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8c0-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-434">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="be8c0-434">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-435">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-436">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-437">Последнее запрошенное или требуемое состояние для службы управления.</span><span class="sxs-lookup"><span data-stu-id="be8c0-437">The last requested or desired state for the management service.</span></span> <span data-ttu-id="be8c0-438">Если свойство **EnabledState** имеет значение 5 (неприменимо), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="be8c0-438">When the **EnabledState** property is set to 5 (Not Applicable), then this property has no meaning.</span></span> <span data-ttu-id="be8c0-439">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8c0-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-440">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="be8c0-440">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-441">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be8c0-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-443">Квалификаторы: **Переопределение**, **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="be8c0-443">Qualifiers: **Override**, **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-444">Текущая пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="be8c0-444">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="be8c0-445">Для портов, которые зависят от пропускной способности или для тех, для которых не удается выполнить точную оценку, это свойство должно содержать номинальную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="be8c0-445">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="be8c0-446">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-446">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-447">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="be8c0-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-448">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-450">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="be8c0-450">The current status of the object.</span></span> <span data-ttu-id="be8c0-451">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-452">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="be8c0-452">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-453">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="be8c0-453">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-454">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-455">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="be8c0-455">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="be8c0-456">Записи в этом массиве сопоставляются с элементами в том же индексе массива в **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="be8c0-456">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="be8c0-457">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="be8c0-457">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="be8c0-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-459">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-461">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="be8c0-461">The state of the logical device.</span></span> <span data-ttu-id="be8c0-462">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-463">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="be8c0-463">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-464">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be8c0-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-466">Поддерживаемый максимальный размер блока передачи (MTU).</span><span class="sxs-lookup"><span data-stu-id="be8c0-466">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="be8c0-467">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="be8c0-467">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-468">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="be8c0-468">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-469">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-471">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="be8c0-471">The scoping system's creation class name.</span></span> <span data-ttu-id="be8c0-472">Это свойство унаследовано от [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-, но не поддерживается</span><span class="sxs-lookup"><span data-stu-id="be8c0-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not supported</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="be8c0-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-474">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="be8c0-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-476">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="be8c0-476">The name of the scoping system.</span></span> <span data-ttu-id="be8c0-477">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="be8c0-477">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-478">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="be8c0-478">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-479">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="be8c0-479">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-480">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-481">Дата или время последнего изменения свойства **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="be8c0-481">The date or time when the **EnabledState** property of the element last changed.</span></span> <span data-ttu-id="be8c0-482">Если состояние элемента не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала.</span><span class="sxs-lookup"><span data-stu-id="be8c0-482">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="be8c0-483">Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="be8c0-483">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="be8c0-484">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-484">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-485">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="be8c0-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-486">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-488">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="be8c0-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="be8c0-489">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-490">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="be8c0-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-491">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-492">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-493">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="be8c0-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="be8c0-494">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="be8c0-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be8c0-495">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="be8c0-495">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8c0-496">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="be8c0-496">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="be8c0-497">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be8c0-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8c0-498">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="be8c0-498">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="be8c0-499">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="be8c0-499">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="be8c0-500">Значение</span><span class="sxs-lookup"><span data-stu-id="be8c0-500">Value</span></span>                                                                        | <span data-ttu-id="be8c0-501">Значение</span><span class="sxs-lookup"><span data-stu-id="be8c0-501">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="be8c0-502"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="be8c0-502"><dt>4</dt></span></span> </dl> | <span data-ttu-id="be8c0-503">Не ограничено</span><span class="sxs-lookup"><span data-stu-id="be8c0-503">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be8c0-504">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be8c0-504">Remarks</span></span>

<span data-ttu-id="be8c0-505">Доступ к классу **\_ интерналесернетпорт мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="be8c0-505">Access to the **Msvm\_InternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="be8c0-506">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="be8c0-506">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="be8c0-507">Примеры</span><span class="sxs-lookup"><span data-stu-id="be8c0-507">Examples</span></span>

<span data-ttu-id="be8c0-508">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="be8c0-508">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be8c0-509">Требования</span><span class="sxs-lookup"><span data-stu-id="be8c0-509">Requirements</span></span>



| <span data-ttu-id="be8c0-510">Требование</span><span class="sxs-lookup"><span data-stu-id="be8c0-510">Requirement</span></span> | <span data-ttu-id="be8c0-511">Значение</span><span class="sxs-lookup"><span data-stu-id="be8c0-511">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be8c0-512">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be8c0-512">Minimum supported client</span></span><br/> | <span data-ttu-id="be8c0-513">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="be8c0-513">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="be8c0-514">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be8c0-514">Minimum supported server</span></span><br/> | <span data-ttu-id="be8c0-515">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="be8c0-515">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="be8c0-516">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be8c0-516">Namespace</span></span><br/>                | <span data-ttu-id="be8c0-517">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="be8c0-517">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="be8c0-518">MOF</span><span class="sxs-lookup"><span data-stu-id="be8c0-518">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be8c0-519"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be8c0-519"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="be8c0-520">DLL</span><span class="sxs-lookup"><span data-stu-id="be8c0-520">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be8c0-521"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="be8c0-521"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="be8c0-522">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be8c0-522">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8c0-523">**\_ЕСЕРНЕТПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="be8c0-523">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="be8c0-524">**\_ЕСЕРНЕТПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="be8c0-524">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

