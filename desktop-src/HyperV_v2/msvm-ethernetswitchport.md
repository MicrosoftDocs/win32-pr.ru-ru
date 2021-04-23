---
description: Представляет порт в коммутаторе.
ms.assetid: a2637e53-6b28-41ad-bef9-d3a14b6cf727
title: Класс Msvm_EthernetSwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPort
- Msvm_EthernetSwitchPort.SetPowerState
- Msvm_EthernetSwitchPort.EnableDevice
- Msvm_EthernetSwitchPort.OnlineDevice
- Msvm_EthernetSwitchPort.QuiesceDevice
- Msvm_EthernetSwitchPort.SaveProperties
- Msvm_EthernetSwitchPort.RestoreProperties
- Msvm_EthernetSwitchPort.InstanceID
- Msvm_EthernetSwitchPort.Caption
- Msvm_EthernetSwitchPort.Description
- Msvm_EthernetSwitchPort.ElementName
- Msvm_EthernetSwitchPort.InstallDate
- Msvm_EthernetSwitchPort.Name
- Msvm_EthernetSwitchPort.OperationalStatus
- Msvm_EthernetSwitchPort.StatusDescriptions
- Msvm_EthernetSwitchPort.Status
- Msvm_EthernetSwitchPort.HealthState
- Msvm_EthernetSwitchPort.CommunicationStatus
- Msvm_EthernetSwitchPort.DetailedStatus
- Msvm_EthernetSwitchPort.OperatingStatus
- Msvm_EthernetSwitchPort.PrimaryStatus
- Msvm_EthernetSwitchPort.EnabledState
- Msvm_EthernetSwitchPort.OtherEnabledState
- Msvm_EthernetSwitchPort.RequestedState
- Msvm_EthernetSwitchPort.EnabledDefault
- Msvm_EthernetSwitchPort.TimeOfLastStateChange
- Msvm_EthernetSwitchPort.AvailableRequestedStates
- Msvm_EthernetSwitchPort.TransitioningToState
- Msvm_EthernetSwitchPort.SystemCreationClassName
- Msvm_EthernetSwitchPort.SystemName
- Msvm_EthernetSwitchPort.CreationClassName
- Msvm_EthernetSwitchPort.DeviceID
- Msvm_EthernetSwitchPort.PowerManagementSupported
- Msvm_EthernetSwitchPort.PowerManagementCapabilities
- Msvm_EthernetSwitchPort.Availability
- Msvm_EthernetSwitchPort.StatusInfo
- Msvm_EthernetSwitchPort.LastErrorCode
- Msvm_EthernetSwitchPort.ErrorDescription
- Msvm_EthernetSwitchPort.ErrorCleared
- Msvm_EthernetSwitchPort.OtherIdentifyingInfo
- Msvm_EthernetSwitchPort.PowerOnHours
- Msvm_EthernetSwitchPort.TotalPowerOnHours
- Msvm_EthernetSwitchPort.IdentifyingDescriptions
- Msvm_EthernetSwitchPort.AdditionalAvailability
- Msvm_EthernetSwitchPort.MaxQuiesceTime
- Msvm_EthernetSwitchPort.Speed
- Msvm_EthernetSwitchPort.MaxSpeed
- Msvm_EthernetSwitchPort.RequestedSpeed
- Msvm_EthernetSwitchPort.UsageRestriction
- Msvm_EthernetSwitchPort.PortType
- Msvm_EthernetSwitchPort.OtherPortType
- Msvm_EthernetSwitchPort.OtherNetworkPortType
- Msvm_EthernetSwitchPort.PortNumber
- Msvm_EthernetSwitchPort.LinkTechnology
- Msvm_EthernetSwitchPort.OtherLinkTechnology
- Msvm_EthernetSwitchPort.PermanentAddress
- Msvm_EthernetSwitchPort.NetworkAddresses
- Msvm_EthernetSwitchPort.FullDuplex
- Msvm_EthernetSwitchPort.AutoSense
- Msvm_EthernetSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.MaxDataSize
- Msvm_EthernetSwitchPort.Capabilities
- Msvm_EthernetSwitchPort.CapabilityDescriptions
- Msvm_EthernetSwitchPort.EnabledCapabilities
- Msvm_EthernetSwitchPort.OtherEnabledCapabilities
- Msvm_EthernetSwitchPort.VMQOffloadUsage
- Msvm_EthernetSwitchPort.IOVOffloadUsage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76c43cbe8dd053808085346b1874781f354b20dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664767"
---
# <a name="msvm_ethernetswitchport-class"></a><span data-ttu-id="9d5b6-103">\_Класс мсвм есернетсвитчпорт</span><span class="sxs-lookup"><span data-stu-id="9d5b6-103">Msvm\_EthernetSwitchPort class</span></span>

<span data-ttu-id="9d5b6-104">Представляет порт в коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-104">Represents a port on the switch.</span></span>

<span data-ttu-id="9d5b6-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5b6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d5b6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Switch Port";
  string   Description = "Microsoft Virtual Ethernet Switch Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchPort";
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
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint32   MaxDataSize;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
  uint32   VMQOffloadUsage;
  uint32   IOVOffloadUsage;
};
```

## <a name="members"></a><span data-ttu-id="9d5b6-107">Члены</span><span class="sxs-lookup"><span data-stu-id="9d5b6-107">Members</span></span>

<span data-ttu-id="9d5b6-108">Класс **мсвм \_ есернетсвитчпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9d5b6-108">The **Msvm\_EthernetSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="9d5b6-109">Методы</span><span class="sxs-lookup"><span data-stu-id="9d5b6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9d5b6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d5b6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9d5b6-111">Методы</span><span class="sxs-lookup"><span data-stu-id="9d5b6-111">Methods</span></span>

<span data-ttu-id="9d5b6-112">Класс **мсвм \_ есернетсвитчпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-112">The **Msvm\_EthernetSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="9d5b6-113">Метод</span><span class="sxs-lookup"><span data-stu-id="9d5b6-113">Method</span></span>                                                                   | <span data-ttu-id="9d5b6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9d5b6-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="9d5b6-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="9d5b6-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9d5b6-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="9d5b6-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9d5b6-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="9d5b6-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9d5b6-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-121">**RequestStateChange**</span></span>](msvm-ethernetswitchport-requeststatechange.md) | <span data-ttu-id="9d5b6-122">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="9d5b6-123">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-123">**Reset**</span></span>](msvm-ethernetswitchport-reset.md)                           | <span data-ttu-id="9d5b6-124">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="9d5b6-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="9d5b6-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9d5b6-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="9d5b6-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9d5b6-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="9d5b6-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9d5b6-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d5b6-131">Properties</span></span>

<span data-ttu-id="9d5b6-132">Класс **мсвм \_ есернетсвитчпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-132">The **Msvm\_EthernetSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d5b6-133">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-134">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-136">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="9d5b6-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-137">Количество активных или согласованных максимальных единиц передачи (MTU), которые могут поддерживаться в байтах.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="9d5b6-138">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-139">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-140">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9d5b6-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-142">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="9d5b6-143">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-144">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-145">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-147">Указывает, может ли порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="9d5b6-148">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-149">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-150">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-152">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-152">The primary availability and status of the device.</span></span> <span data-ttu-id="9d5b6-153">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-154">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-155">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9d5b6-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-157">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="9d5b6-158">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="9d5b6-159">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="9d5b6-160">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="9d5b6-161">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9d5b6-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="9d5b6-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="9d5b6-172">)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d5b6-173">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-173">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-174">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9d5b6-174">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-176">Массив, указывающий возможности порта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-176">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="9d5b6-177">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-177">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="9d5b6-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Алертонлан** (2)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Вакеонлан** (3)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Отработка отказа** (4)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d5b6-184">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-185">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-187">Массив строк произвольной формы, содержащий более подробные пояснения к функциям порта, содержащимся в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="9d5b6-187">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="9d5b6-188">Каждая запись этого массива связана с соответствующей записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-188">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="9d5b6-189">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-189">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-190">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-193">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-193">A short description of the object.</span></span> <span data-ttu-id="9d5b6-194">Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и всегда имеет значение "порт коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="9d5b6-194">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it is always set to "Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-195">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-195">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-196">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-198">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-198">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9d5b6-199">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-199">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9d5b6-200">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-201">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-201">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-204">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-204">The scoping system's creation class name.</span></span> <span data-ttu-id="9d5b6-205">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ есернетсвитчпорт".</span><span class="sxs-lookup"><span data-stu-id="9d5b6-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-206">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-209">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-209">A description of the object.</span></span> <span data-ttu-id="9d5b6-210">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "порт виртуального коммутатора Microsoft Virtual Ethernet".</span><span class="sxs-lookup"><span data-stu-id="9d5b6-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-212">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-214">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-214">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9d5b6-215">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9d5b6-216">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-217">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-217">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-220">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-220">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="9d5b6-221">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-225">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-225">A display name for the object.</span></span> <span data-ttu-id="9d5b6-226">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-227">**енабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-227">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-228">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9d5b6-228">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-230">Указывает, какие возможности включены из списка всех поддерживаемых возможностей в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="9d5b6-230">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="9d5b6-231">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-231">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="9d5b6-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Алертонлан** (2)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Вакеонлан** (3)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Отработка отказа** (4)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d5b6-238">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-239">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-241">Конфигурация по умолчанию или запуск администратора для свойства **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-241">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="9d5b6-242">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-244">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-246">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9d5b6-247">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="9d5b6-248">Значение</span><span class="sxs-lookup"><span data-stu-id="9d5b6-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="9d5b6-249">Значение</span><span class="sxs-lookup"><span data-stu-id="9d5b6-249">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="9d5b6-250"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9d5b6-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="9d5b6-251">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-251">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="9d5b6-252"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9d5b6-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="9d5b6-253">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-253">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d5b6-254">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-255">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-257">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="9d5b6-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="9d5b6-258">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-260">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-262">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="9d5b6-263">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-264">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-264">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-265">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-267">Указывает, работает ли порт в режиме полного дуплекса.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-267">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="9d5b6-268">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-268">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-269">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-269">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-270">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-270">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-272">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-272">The current health of the element.</span></span> <span data-ttu-id="9d5b6-273">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-274">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-274">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-275">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-275">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-277">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="9d5b6-277">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="9d5b6-278">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-280">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-282">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-282">The date and time when the object was installed.</span></span> <span data-ttu-id="9d5b6-283">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-283">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="9d5b6-284">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-285">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-285">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-288">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-288">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-289">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-289">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9d5b6-290">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-290">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-291">**иовоффлоадусаже**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-291">**IOVOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-292">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-294">Текущий уровень использования виртуализации ввода-вывода (IOV) для этого порта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-294">The current I/O virtualization (IOV) offload usage on this port.</span></span> <span data-ttu-id="9d5b6-295">Использование — это объем используемых в порте ресурсов IOV.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-295">The usage is the amount of IOV resources in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-296">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-296">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-297">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-299">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-299">The last error code reported by the logical device.</span></span> <span data-ttu-id="9d5b6-300">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-301">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-301">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-302">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-304">Указывает тип технологии ссылок для порта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-304">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="9d5b6-305">Если задано значение 1 (другое), свойство **осерлинктечнологи** содержит строковое описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-305">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="9d5b6-306">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-306">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="9d5b6-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-310"><span id="IB"></span><span id="ib"></span>**ГЕО(3** )</span><span class="sxs-lookup"><span data-stu-id="9d5b6-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Инфракрасная связь** (9)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Беспроводная локальная сеть** (11)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d5b6-319">**максдатасизе**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-319">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-320">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-322">Максимальный размер поля сведений (не MAC), которое будет получено или передано.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-322">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="9d5b6-323">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)и всегда имеет значение 1500.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-323">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-324">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-324">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-325">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-327">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-327">This property has been deprecated.</span></span> <span data-ttu-id="9d5b6-328">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-329">**максспид**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-329">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-330">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-332">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="9d5b6-332">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-333">Максимальная пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-333">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9d5b6-334">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-334">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-335">**Name**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-335">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-338">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-338">The label by which the object is known.</span></span> <span data-ttu-id="9d5b6-339">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-340">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-340">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-341">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-343">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-343">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-344">Массив строк, содержащих MAC-адреса для порта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-344">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="9d5b6-345">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-346">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-346">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-347">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-349">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9d5b6-349">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9d5b6-350">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9d5b6-351">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-352">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-352">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-353">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9d5b6-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-355">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-355">The current statuses of the object.</span></span> <span data-ttu-id="9d5b6-356">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-357">**осеренабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-357">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-358">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-360">Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из включенных возможностей, указанных как 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-360">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="9d5b6-361">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-361">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-362">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-363">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-365">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-365">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9d5b6-366">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-366">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="9d5b6-367">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-369">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-371">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="9d5b6-372">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-373">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-373">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-376">Строковое значение, описывающее **линктечнологи** , если оно имеет значение 1, (другое).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-376">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="9d5b6-377">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-378">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-378">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-381">Использование этого свойства не рекомендуется использовать вместо свойства **portType** .</span><span class="sxs-lookup"><span data-stu-id="9d5b6-381">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="9d5b6-382">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-382">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-383">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-383">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-384">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-386">Описывает тип модуля, когда для **portType** задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-386">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="9d5b6-387">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-387">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-388">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-388">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-389">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-391">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-391">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-392">Сетевой адрес, жестко закодированный в порт.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-392">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="9d5b6-393">Этот жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-393">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="9d5b6-394">При внесении этого изменения поле должно быть обновлено одновременно.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-394">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="9d5b6-395">Это свойство должно иметь **значение NULL** , если для сетевого адаптера не существует жестко закодированного адреса.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-395">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="9d5b6-396">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-396">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-397">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-397">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-398">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-400">номер порта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-400">The port number.</span></span> <span data-ttu-id="9d5b6-401">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-401">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-402">**Порта**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-402">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-403">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-405">Конкретный режим, который в данный момент включен для порта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-405">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="9d5b6-406">Если задано значение 1 (другое), связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-406">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="9d5b6-407">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9d5b6-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 медный** (50)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BASE** (51)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BASE** (52)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BASE** (53)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-лв** (109)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ать** (111)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d5b6-430">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-431">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9d5b6-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-433">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-433">The power management capabilities of the device.</span></span> <span data-ttu-id="9d5b6-434">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-435">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-436">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-438">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-438">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="9d5b6-439">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-440">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-440">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-441">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-443">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-443">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="9d5b6-444">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-445">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-445">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-446">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-448">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-448">Provides high level status information.</span></span> <span data-ttu-id="9d5b6-449">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-449">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="9d5b6-450">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-450">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9d5b6-451">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-452">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-452">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-453">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-453">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-454">Тип доступа: только для записи</span><span class="sxs-lookup"><span data-stu-id="9d5b6-454">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-455">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="9d5b6-455">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-456">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-456">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9d5b6-457">Фактическая пропускная способность указывается в свойстве **Speed** .</span><span class="sxs-lookup"><span data-stu-id="9d5b6-457">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="9d5b6-458">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-458">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-459">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-459">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-460">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-460">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-461">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-462">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-462">The last requested or desired state for the element.</span></span> <span data-ttu-id="9d5b6-463">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-463">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-464">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-464">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-465">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-465">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-466">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-467">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="9d5b6-467">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-468">Пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-468">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9d5b6-469">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-469">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-470">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-470">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-471">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-473">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-473">The current status of the object.</span></span> <span data-ttu-id="9d5b6-474">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-474">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-475">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-475">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-476">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-478">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9d5b6-478">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9d5b6-479">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-480">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-480">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-481">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-481">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-483">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-483">The current state of the logical device.</span></span> <span data-ttu-id="9d5b6-484">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-485">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-485">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-486">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-488">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="9d5b6-488">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-489">Максимальный поддерживаемый размер блока передачи (MTU) в байтах.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-489">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="9d5b6-490">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-490">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-491">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-492">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-493">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-494">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-494">The scoping system's creation class name.</span></span> <span data-ttu-id="9d5b6-495">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ виртуалесернетсвитч".</span><span class="sxs-lookup"><span data-stu-id="9d5b6-495">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-496">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-496">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-497">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-497">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-498">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-499">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-499">The scoping system's name.</span></span> <span data-ttu-id="9d5b6-500">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-500">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-501">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-501">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-502">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-502">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-503">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-504">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-504">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9d5b6-505">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-505">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-506">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-506">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-507">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-507">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-508">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-509">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-509">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="9d5b6-510">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-510">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-511">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-511">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-512">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-512">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-513">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-514">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-514">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9d5b6-515">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-515">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5b6-516">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-516">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-517">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-517">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-518">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-519">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-519">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="9d5b6-520">В качестве примера такой ситуации можно привести массив хранения данных, который может иметь серверные порты для взаимодействия с дисками и интерфейсными портами для взаимодействия с узлами.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-520">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="9d5b6-521">При отсутствии ограничений на использование порта значение должно быть равно 4 (не ограничено).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-521">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="9d5b6-522">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d5b6-522">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9d5b6-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Только внешний** интерфейс (2)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Только серверная** части (3)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Не ограничено** (4)</span><span class="sxs-lookup"><span data-stu-id="9d5b6-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d5b6-527">**вмкоффлоадусаже**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-527">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d5b6-528">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d5b6-528">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d5b6-529">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d5b6-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d5b6-530">Текущее использование разгрузки очереди виртуальных машин (VMQ) на этом порту.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-530">The current virtual machine queue (VMQ) offloading usage on this port.</span></span> <span data-ttu-id="9d5b6-531">Использование — это объем ресурсов VMQ, используемых в порте.</span><span class="sxs-lookup"><span data-stu-id="9d5b6-531">The usage is the amount of VMQ resources in use on the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d5b6-532">Требования</span><span class="sxs-lookup"><span data-stu-id="9d5b6-532">Requirements</span></span>



| <span data-ttu-id="9d5b6-533">Требование</span><span class="sxs-lookup"><span data-stu-id="9d5b6-533">Requirement</span></span> | <span data-ttu-id="9d5b6-534">Значение</span><span class="sxs-lookup"><span data-stu-id="9d5b6-534">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5b6-535">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d5b6-535">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5b6-536">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9d5b6-536">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9d5b6-537">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d5b6-537">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5b6-538">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9d5b6-538">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d5b6-539">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9d5b6-539">Namespace</span></span><br/>                | <span data-ttu-id="9d5b6-540">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9d5b6-540">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9d5b6-541">MOF</span><span class="sxs-lookup"><span data-stu-id="9d5b6-541">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d5b6-542"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d5b6-542"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d5b6-543">DLL</span><span class="sxs-lookup"><span data-stu-id="9d5b6-543">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d5b6-544"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d5b6-544"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

