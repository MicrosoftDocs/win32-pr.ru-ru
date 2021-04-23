---
description: Представляет эмулированного Ethernet адаптер.
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Класс Msvm_EmulatedEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ec13ae369f6d5e3d884f74c96d7df27c2f5fa97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662717"
---
# <a name="msvm_emulatedethernetport-class"></a><span data-ttu-id="c5245-103">\_Класс мсвм емулатедесернетпорт</span><span class="sxs-lookup"><span data-stu-id="c5245-103">Msvm\_EmulatedEthernetPort class</span></span>

<span data-ttu-id="c5245-104">Представляет эмулированного Ethernet адаптер.</span><span class="sxs-lookup"><span data-stu-id="c5245-104">Represents an emulated Ethernet adapter.</span></span> <span data-ttu-id="c5245-105">Этот адаптер используется, если виртуальная машина не может запустить искусственный порт Ethernet, если в гостевой системе не установлены интегрированные цепи.</span><span class="sxs-lookup"><span data-stu-id="c5245-105">This adapter is used when a virtual machine is not capable of running the synthetic Ethernet port when no integrated circuits are installed in the guest.</span></span>

> [!Note]  
> <span data-ttu-id="c5245-106">Этот класс недоступен для виртуальных машин поколения 2.</span><span class="sxs-lookup"><span data-stu-id="c5245-106">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="c5245-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c5245-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5245-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5245-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
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
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="c5245-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c5245-109">Members</span></span>

<span data-ttu-id="c5245-110">Класс **мсвм \_ емулатедесернетпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c5245-110">The **Msvm\_EmulatedEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="c5245-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c5245-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c5245-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5245-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c5245-113">Методы</span><span class="sxs-lookup"><span data-stu-id="c5245-113">Methods</span></span>

<span data-ttu-id="c5245-114">Класс **мсвм \_ емулатедесернетпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c5245-114">The **Msvm\_EmulatedEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="c5245-115">Метод</span><span class="sxs-lookup"><span data-stu-id="c5245-115">Method</span></span>                                                                     | <span data-ttu-id="c5245-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c5245-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="c5245-117">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="c5245-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="c5245-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c5245-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c5245-119">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="c5245-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="c5245-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c5245-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c5245-121">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="c5245-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="c5245-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c5245-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="c5245-123">**Равен**</span><span class="sxs-lookup"><span data-stu-id="c5245-123">**RequestStateChange**</span></span>](msvm-emulatedethernetport-requeststatechange.md) | <span data-ttu-id="c5245-124">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="c5245-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="c5245-125">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="c5245-125">**Reset**</span></span>](msvm-emulatedethernetport-reset.md)                           | <span data-ttu-id="c5245-126">Выполняет сброс эмулятора устройства.</span><span class="sxs-lookup"><span data-stu-id="c5245-126">Resets the emulated device.</span></span><br/>   |
| <span data-ttu-id="c5245-127">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="c5245-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="c5245-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c5245-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c5245-129">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="c5245-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="c5245-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c5245-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c5245-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c5245-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="c5245-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c5245-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c5245-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5245-133">Properties</span></span>

<span data-ttu-id="c5245-134">Класс **мсвм \_ емулатедесернетпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c5245-134">The **Msvm\_EmulatedEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5245-135">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="c5245-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-136">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c5245-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-138">Допустимое число активных или согласованных максимальных единиц передачи (MTU).</span><span class="sxs-lookup"><span data-stu-id="c5245-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="c5245-139">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)и всегда имеет значение 1500.</span><span class="sxs-lookup"><span data-stu-id="c5245-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-140">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="c5245-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-141">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c5245-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-143">Любая дополнительная доступность и состояние устройства, кроме указанного в свойстве **Availability** .</span><span class="sxs-lookup"><span data-stu-id="c5245-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="c5245-144">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="c5245-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="c5245-145">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="c5245-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-146">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c5245-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-148">Указывает, может ли сетевой порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="c5245-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="c5245-149">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c5245-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-150">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="c5245-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-153">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="c5245-153">The primary availability and status of the device.</span></span> <span data-ttu-id="c5245-154">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c5245-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-155">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="c5245-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-156">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c5245-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-158">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="c5245-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="c5245-159">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c5245-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="c5245-160">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="c5245-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="c5245-161">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="c5245-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="c5245-162">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c5245-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c5245-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="c5245-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c5245-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="c5245-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c5245-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="c5245-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c5245-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="c5245-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c5245-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="c5245-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c5245-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="c5245-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c5245-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="c5245-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c5245-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="c5245-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c5245-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="c5245-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c5245-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="c5245-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="c5245-173">)</span><span class="sxs-lookup"><span data-stu-id="c5245-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c5245-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c5245-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-175">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c5245-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-177">Возможности порта Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c5245-177">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="c5245-178">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-179">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="c5245-179">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-180">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c5245-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-182">Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из функций порта Ethernet, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="c5245-182">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="c5245-183">Обратите внимание, что каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="c5245-183">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="c5245-184">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-184">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-185">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c5245-185">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-188">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c5245-188">A short description of the object.</span></span> <span data-ttu-id="c5245-189">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "порт Ethernet".</span><span class="sxs-lookup"><span data-stu-id="c5245-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="c5245-190">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="c5245-190">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-191">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-193">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="c5245-193">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c5245-194">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c5245-194">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c5245-195">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c5245-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5245-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c5245-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-199">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c5245-199">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="c5245-200">При использовании с другими ключевыми свойствами этого класса это свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="c5245-200">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="c5245-201">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ емулатедесернетпорт".</span><span class="sxs-lookup"><span data-stu-id="c5245-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EmulatedEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="c5245-202">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5245-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-205">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c5245-205">A description of the object.</span></span> <span data-ttu-id="c5245-206">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "порт эмуляции Ethernet (Майкрософт)".</span><span class="sxs-lookup"><span data-stu-id="c5245-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="c5245-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c5245-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-210">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="c5245-210">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c5245-211">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c5245-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c5245-212">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c5245-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5245-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c5245-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-216">Адрес или другие идентифицирующие сведения, используемые для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c5245-216">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="c5245-217">Это свойство наследуется от CIM-*класса*, и ему всегда присваивается значение "Microsoft: GUID для [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) \\ *конкретного устройства*".</span><span class="sxs-lookup"><span data-stu-id="c5245-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="c5245-218">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c5245-218">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-221">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c5245-221">A display name for the object.</span></span> <span data-ttu-id="c5245-222">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "устаревший сетевой адаптер".</span><span class="sxs-lookup"><span data-stu-id="c5245-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Legacy Network Adapter".</span></span>

</dd> <dt>

<span data-ttu-id="c5245-223">**енабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="c5245-223">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-224">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c5245-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-226">Возможности, включенные из списка всех поддерживаемых, определенных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="c5245-226">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="c5245-227">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), но не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-227">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-228">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="c5245-228">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-229">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-231">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c5245-231">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c5245-232">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и всегда имеет значение 2 ("Enabled").</span><span class="sxs-lookup"><span data-stu-id="c5245-232">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 ("Enabled").</span></span>

</dd> <dt>

<span data-ttu-id="c5245-233">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c5245-233">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-234">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-236">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c5245-236">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c5245-237">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="c5245-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="c5245-238">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="c5245-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-239">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c5245-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-241">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="c5245-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="c5245-242">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c5245-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-246">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="c5245-246">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="c5245-247">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-248">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="c5245-248">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-249">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c5245-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-251">Указывает, работает ли порт в режиме полного дуплекса.</span><span class="sxs-lookup"><span data-stu-id="c5245-251">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="c5245-252">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c5245-252">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-253">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c5245-253">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-254">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-256">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="c5245-256">The current health of the element.</span></span> <span data-ttu-id="c5245-257">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c5245-257">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c5245-258">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 ("ОК").</span><span class="sxs-lookup"><span data-stu-id="c5245-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="c5245-259">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c5245-259">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-260">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c5245-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-262">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="c5245-262">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="c5245-263">Каждая запись этого массива связана с записью в **осеридентифингинфо** , расположенной в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="c5245-263">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="c5245-264">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-264">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c5245-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-266">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c5245-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-268">Значение **типа DateTime** , указывающее, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="c5245-268">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="c5245-269">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="c5245-269">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="c5245-270">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c5245-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5245-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c5245-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-272">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5245-274">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c5245-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c5245-275">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c5245-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c5245-276">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c5245-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5245-277">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="c5245-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-278">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5245-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-280">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="c5245-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="c5245-281">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-282">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="c5245-282">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-283">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-285">Типы ссылок.</span><span class="sxs-lookup"><span data-stu-id="c5245-285">The types of links.</span></span> <span data-ttu-id="c5245-286">Если задано значение 1 ("другое"), связанное свойство **осерлинктечнологи** содержит строковое описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="c5245-286">When set to 1 ("Other"), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="c5245-287">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) и всегда имеет значение 2 ("Ethernet").</span><span class="sxs-lookup"><span data-stu-id="c5245-287">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is always set to 2 ("Ethernet").</span></span>

</dd> <dt>

<span data-ttu-id="c5245-288">**максдатасизе**</span><span class="sxs-lookup"><span data-stu-id="c5245-288">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-289">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5245-289">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-291">Максимальный размер поля сведений (не MAC), которое будет получено или передано.</span><span class="sxs-lookup"><span data-stu-id="c5245-291">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="c5245-292">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)и всегда имеет значение 1500.</span><span class="sxs-lookup"><span data-stu-id="c5245-292">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-293">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="c5245-293">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-294">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c5245-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-296">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-297">**максспид**</span><span class="sxs-lookup"><span data-stu-id="c5245-297">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-298">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c5245-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-300">Максимальная пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="c5245-300">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c5245-301">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85))и всегда имеет значение 1000000000.</span><span class="sxs-lookup"><span data-stu-id="c5245-301">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-302">**Name**</span><span class="sxs-lookup"><span data-stu-id="c5245-302">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-305">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="c5245-305">The label by which the object is known.</span></span> <span data-ttu-id="c5245-306">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="c5245-306">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="c5245-307">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "порт Ethernet".</span><span class="sxs-lookup"><span data-stu-id="c5245-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="c5245-308">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="c5245-308">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-309">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c5245-309">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-311">MAC-адреса Ethernet/802.3, отформатированные как двенадцать шестнадцатеричных цифр (например, "010203040506"), каждая пара представляет один из шести октетов MAC-адреса в каноническом порядке (бит адреса группы находится в младших битах первого символа строки).</span><span class="sxs-lookup"><span data-stu-id="c5245-311">The Ethernet/802.3 MAC addresses, formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="c5245-312">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-312">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-313">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="c5245-313">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-314">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-314">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-316">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c5245-316">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c5245-317">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c5245-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c5245-318">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c5245-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5245-319">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c5245-319">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-320">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c5245-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-322">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="c5245-322">The current statuses of the element.</span></span> <span data-ttu-id="c5245-323">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 2 ("ОК").</span><span class="sxs-lookup"><span data-stu-id="c5245-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="c5245-324">**осеренабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="c5245-324">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-325">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c5245-325">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-327">Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из включенных возможностей, указанных как "Other".</span><span class="sxs-lookup"><span data-stu-id="c5245-327">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="c5245-328">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-328">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-329">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="c5245-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-332">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="c5245-332">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="c5245-333">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="c5245-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c5245-334">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c5245-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-336">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c5245-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-338">Любые данные в дополнение к сведениям об ИДЕНТИФИКАТОРе устройства, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c5245-338">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c5245-339">Например, это свойство можно использовать для хранения отображаемого имени операционной системы для устройства.</span><span class="sxs-lookup"><span data-stu-id="c5245-339">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="c5245-340">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-341">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="c5245-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-344">Строковое значение, описывающее **линктечнологи** , если задано значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="c5245-344">A string value that describes **LinkTechnology** when it is set to 1 ("Other").</span></span> <span data-ttu-id="c5245-345">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), но не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-346">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="c5245-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-349">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c5245-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-350">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="c5245-350">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-351">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-353">Тип модуля, когда для **portType** задано значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="c5245-353">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="c5245-354">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)) и всегда имеет значение "Virtual Ethernet".</span><span class="sxs-lookup"><span data-stu-id="c5245-354">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="c5245-355">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="c5245-355">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-356">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-358">Сетевой адрес, жестко закодированный в порт.</span><span class="sxs-lookup"><span data-stu-id="c5245-358">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="c5245-359">Этот адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="c5245-359">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="c5245-360">При внесении этого изменения поле должно быть обновлено одновременно.</span><span class="sxs-lookup"><span data-stu-id="c5245-360">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="c5245-361">Если для сетевого адаптера не существует жестко закодированного адреса, его следует оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="c5245-361">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="c5245-362">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c5245-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c5245-363">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="c5245-363">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-364">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-366">Сетевые порты часто нумеруются относительно логического модуля или сетевого элемента.</span><span class="sxs-lookup"><span data-stu-id="c5245-366">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="c5245-367">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c5245-367">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="c5245-368">Значение</span><span class="sxs-lookup"><span data-stu-id="c5245-368">Value</span></span>                                                                        | <span data-ttu-id="c5245-369">Значение</span><span class="sxs-lookup"><span data-stu-id="c5245-369">Meaning</span></span>                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="c5245-370"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c5245-370"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c5245-371">Сетевая карта не эмулируется.</span><span class="sxs-lookup"><span data-stu-id="c5245-371">The NIC is not emulated.</span></span><br/> |
| <dl> <span data-ttu-id="c5245-372"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c5245-372"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c5245-373">Сетевая карта эмулируется.</span><span class="sxs-lookup"><span data-stu-id="c5245-373">The NIC is emulated.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="c5245-374">**Порта**</span><span class="sxs-lookup"><span data-stu-id="c5245-374">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-375">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-377">Конкретный режим, который в данный момент включен для порта.</span><span class="sxs-lookup"><span data-stu-id="c5245-377">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="c5245-378">Если задано значение 1 ("другое"), связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="c5245-378">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="c5245-379">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)и всегда имеет значение 1 ("Other").</span><span class="sxs-lookup"><span data-stu-id="c5245-379">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1 ("Other").</span></span>

</dd> <dt>

<span data-ttu-id="c5245-380">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="c5245-380">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-381">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c5245-381">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-383">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="c5245-383">The power management capabilities of the device.</span></span> <span data-ttu-id="c5245-384">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-385">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="c5245-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-386">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c5245-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-388">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="c5245-388">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="c5245-389">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-390">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="c5245-390">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-391">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c5245-391">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-393">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="c5245-393">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="c5245-394">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-395">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="c5245-395">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-396">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-398">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="c5245-398">Provides high level status information.</span></span> <span data-ttu-id="c5245-399">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c5245-399">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="c5245-400">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c5245-400">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c5245-401">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c5245-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c5245-402">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="c5245-402">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-403">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c5245-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-405">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="c5245-405">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c5245-406">Фактическая пропускная способность указывается в Логикалпорт. Speed.</span><span class="sxs-lookup"><span data-stu-id="c5245-406">The actual bandwidth is reported in LogicalPort.Speed.</span></span> <span data-ttu-id="c5245-407">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85))и всегда имеет значение 1000000000.</span><span class="sxs-lookup"><span data-stu-id="c5245-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-408">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c5245-408">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-409">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-411">Последнее запрошенное или требуемое состояние для службы управления.</span><span class="sxs-lookup"><span data-stu-id="c5245-411">The last requested or desired state for the management service.</span></span> <span data-ttu-id="c5245-412">Если параметр **EnabledState** имеет значение 5 ("неприменимо"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="c5245-412">When **EnabledState** is set to 5 ("Not Applicable"), then this property has no meaning.</span></span> <span data-ttu-id="c5245-413">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="c5245-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="c5245-414">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="c5245-414">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-415">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c5245-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-417">Текущая пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="c5245-417">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c5245-418">Для портов, которые зависят от пропускной способности или для тех, для которых не удается выполнить точную оценку, это свойство должно содержать номинальную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="c5245-418">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="c5245-419">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)и всегда имеет значение 1000000000.</span><span class="sxs-lookup"><span data-stu-id="c5245-419">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-420">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c5245-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-423">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-424">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="c5245-424">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-425">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c5245-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5245-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-427">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c5245-427">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c5245-428">Записи в этом массиве сопоставляются с элементами в том же индексе массива в **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="c5245-428">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="c5245-429">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="c5245-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c5245-430">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c5245-430">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-431">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-433">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c5245-433">The state of the logical device.</span></span> <span data-ttu-id="c5245-434">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-435">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="c5245-435">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5245-438">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="c5245-438">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c5245-439">Максимальный поддерживаемый размер блока передачи (MTU) в байтах.</span><span class="sxs-lookup"><span data-stu-id="c5245-439">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="c5245-440">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)и всегда имеет значение 1500.</span><span class="sxs-lookup"><span data-stu-id="c5245-440">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-441">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c5245-441">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-442">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-444">Имя класса создания для системы области.</span><span class="sxs-lookup"><span data-stu-id="c5245-444">The creation class name of the scoping system.</span></span> <span data-ttu-id="c5245-445">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="c5245-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="c5245-446">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c5245-446">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-447">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c5245-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-448">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-449">ИДЕНТИФИКАТОР виртуальной машины в виде **идентификатора GUID** .</span><span class="sxs-lookup"><span data-stu-id="c5245-449">The virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="c5245-450">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c5245-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c5245-451">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="c5245-451">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-452">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c5245-452">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-454">Дата или время последнего изменения **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="c5245-454">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="c5245-455">Если состояние элемента не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала.</span><span class="sxs-lookup"><span data-stu-id="c5245-455">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="c5245-456">Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="c5245-456">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="c5245-457">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-458">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="c5245-458">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-459">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-461">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="c5245-461">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="c5245-462">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-463">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="c5245-463">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-464">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-466">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c5245-466">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c5245-467">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="c5245-467">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5245-468">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="c5245-468">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5245-469">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5245-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5245-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c5245-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5245-471">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="c5245-471">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="c5245-472">При отсутствии ограничений на использование порта значение должно быть равно 4 ("не ограничено").</span><span class="sxs-lookup"><span data-stu-id="c5245-472">If there is no restriction on the use of the port, then the value should be set to 4 ("Not Restricted").</span></span> <span data-ttu-id="c5245-473">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)) и всегда имеет значение 4 ("не ограничено").</span><span class="sxs-lookup"><span data-stu-id="c5245-473">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to 4 ("Not Restricted").</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5245-474">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5245-474">Remarks</span></span>

<span data-ttu-id="c5245-475">Доступ к классу **\_ емулатедесернетпорт мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c5245-475">Access to the **Msvm\_EmulatedEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c5245-476">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c5245-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="c5245-477">Примеры</span><span class="sxs-lookup"><span data-stu-id="c5245-477">Examples</span></span>

<span data-ttu-id="c5245-478">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c5245-478">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5245-479">Требования</span><span class="sxs-lookup"><span data-stu-id="c5245-479">Requirements</span></span>



| <span data-ttu-id="c5245-480">Требование</span><span class="sxs-lookup"><span data-stu-id="c5245-480">Requirement</span></span> | <span data-ttu-id="c5245-481">Значение</span><span class="sxs-lookup"><span data-stu-id="c5245-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5245-482">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5245-482">Minimum supported client</span></span><br/> | <span data-ttu-id="c5245-483">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c5245-483">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c5245-484">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5245-484">Minimum supported server</span></span><br/> | <span data-ttu-id="c5245-485">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c5245-485">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5245-486">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c5245-486">Namespace</span></span><br/>                | <span data-ttu-id="c5245-487">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c5245-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c5245-488">MOF</span><span class="sxs-lookup"><span data-stu-id="c5245-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5245-489"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5245-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5245-490">DLL</span><span class="sxs-lookup"><span data-stu-id="c5245-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5245-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5245-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5245-492">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5245-492">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5245-493">**\_ЕСЕРНЕТПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="c5245-493">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="c5245-494">**\_ЕСЕРНЕТПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="c5245-494">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

