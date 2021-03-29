---
description: Представляет искусственный Ethernet-адаптер.
ms.assetid: B5CB86A9-015B-42E8-ADF4-2F61970D8437
title: Класс Msvm_SyntheticEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort
- Msvm_SyntheticEthernetPort.SetPowerState
- Msvm_SyntheticEthernetPort.EnableDevice
- Msvm_SyntheticEthernetPort.OnlineDevice
- Msvm_SyntheticEthernetPort.QuiesceDevice
- Msvm_SyntheticEthernetPort.SaveProperties
- Msvm_SyntheticEthernetPort.RestoreProperties
- Msvm_SyntheticEthernetPort.InstanceID
- Msvm_SyntheticEthernetPort.Caption
- Msvm_SyntheticEthernetPort.Description
- Msvm_SyntheticEthernetPort.ElementName
- Msvm_SyntheticEthernetPort.InstallDate
- Msvm_SyntheticEthernetPort.Name
- Msvm_SyntheticEthernetPort.OperationalStatus
- Msvm_SyntheticEthernetPort.StatusDescriptions
- Msvm_SyntheticEthernetPort.Status
- Msvm_SyntheticEthernetPort.HealthState
- Msvm_SyntheticEthernetPort.CommunicationStatus
- Msvm_SyntheticEthernetPort.DetailedStatus
- Msvm_SyntheticEthernetPort.OperatingStatus
- Msvm_SyntheticEthernetPort.PrimaryStatus
- Msvm_SyntheticEthernetPort.EnabledState
- Msvm_SyntheticEthernetPort.OtherEnabledState
- Msvm_SyntheticEthernetPort.RequestedState
- Msvm_SyntheticEthernetPort.EnabledDefault
- Msvm_SyntheticEthernetPort.TimeOfLastStateChange
- Msvm_SyntheticEthernetPort.AvailableRequestedStates
- Msvm_SyntheticEthernetPort.TransitioningToState
- Msvm_SyntheticEthernetPort.SystemCreationClassName
- Msvm_SyntheticEthernetPort.SystemName
- Msvm_SyntheticEthernetPort.CreationClassName
- Msvm_SyntheticEthernetPort.DeviceID
- Msvm_SyntheticEthernetPort.PowerManagementSupported
- Msvm_SyntheticEthernetPort.PowerManagementCapabilities
- Msvm_SyntheticEthernetPort.Availability
- Msvm_SyntheticEthernetPort.StatusInfo
- Msvm_SyntheticEthernetPort.LastErrorCode
- Msvm_SyntheticEthernetPort.ErrorDescription
- Msvm_SyntheticEthernetPort.ErrorCleared
- Msvm_SyntheticEthernetPort.OtherIdentifyingInfo
- Msvm_SyntheticEthernetPort.PowerOnHours
- Msvm_SyntheticEthernetPort.TotalPowerOnHours
- Msvm_SyntheticEthernetPort.IdentifyingDescriptions
- Msvm_SyntheticEthernetPort.AdditionalAvailability
- Msvm_SyntheticEthernetPort.MaxQuiesceTime
- Msvm_SyntheticEthernetPort.Speed
- Msvm_SyntheticEthernetPort.MaxSpeed
- Msvm_SyntheticEthernetPort.RequestedSpeed
- Msvm_SyntheticEthernetPort.UsageRestriction
- Msvm_SyntheticEthernetPort.PortType
- Msvm_SyntheticEthernetPort.OtherPortType
- Msvm_SyntheticEthernetPort.OtherNetworkPortType
- Msvm_SyntheticEthernetPort.PortNumber
- Msvm_SyntheticEthernetPort.LinkTechnology
- Msvm_SyntheticEthernetPort.OtherLinkTechnology
- Msvm_SyntheticEthernetPort.PermanentAddress
- Msvm_SyntheticEthernetPort.NetworkAddresses
- Msvm_SyntheticEthernetPort.FullDuplex
- Msvm_SyntheticEthernetPort.AutoSense
- Msvm_SyntheticEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.MaxDataSize
- Msvm_SyntheticEthernetPort.Capabilities
- Msvm_SyntheticEthernetPort.CapabilityDescriptions
- Msvm_SyntheticEthernetPort.EnabledCapabilities
- Msvm_SyntheticEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8e2a8c2207e410878a4f5c498ea71a1ce67cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898642"
---
# <a name="msvm_syntheticethernetport-class"></a><span data-ttu-id="38ae0-103">\_Класс мсвм синсетицесернетпорт</span><span class="sxs-lookup"><span data-stu-id="38ae0-103">Msvm\_SyntheticEthernetPort class</span></span>

<span data-ttu-id="38ae0-104">Представляет искусственный Ethernet-адаптер.</span><span class="sxs-lookup"><span data-stu-id="38ae0-104">Represents a synthetic Ethernet adapter.</span></span> <span data-ttu-id="38ae0-105">Этот адаптер является предпочтительным сетевым адаптером из-за его производительности, поэтому изменения могут вступить в силу сразу же, пока он используется (горячая Настройка).</span><span class="sxs-lookup"><span data-stu-id="38ae0-105">This adapter is the preferred network adapter because of its performance and because changes to it can take effect right away, while it is in use (hot configurability).</span></span>

<span data-ttu-id="38ae0-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="38ae0-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ae0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38ae0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  uint16   AdditionalAvailability[] = 6;
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
};
```

## <a name="members"></a><span data-ttu-id="38ae0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="38ae0-108">Members</span></span>

<span data-ttu-id="38ae0-109">Класс **мсвм \_ синсетицесернетпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="38ae0-109">The **Msvm\_SyntheticEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="38ae0-110">Методы</span><span class="sxs-lookup"><span data-stu-id="38ae0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="38ae0-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="38ae0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="38ae0-112">Методы</span><span class="sxs-lookup"><span data-stu-id="38ae0-112">Methods</span></span>

<span data-ttu-id="38ae0-113">Класс **мсвм \_ синсетицесернетпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="38ae0-113">The **Msvm\_SyntheticEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="38ae0-114">Метод</span><span class="sxs-lookup"><span data-stu-id="38ae0-114">Method</span></span>                                                                      | <span data-ttu-id="38ae0-115">Описание</span><span class="sxs-lookup"><span data-stu-id="38ae0-115">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="38ae0-116">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="38ae0-116">**EnableDevice**</span></span>                                                            | <span data-ttu-id="38ae0-117">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="38ae0-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="38ae0-118">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="38ae0-118">**OnlineDevice**</span></span>                                                            | <span data-ttu-id="38ae0-119">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="38ae0-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="38ae0-120">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="38ae0-120">**QuiesceDevice**</span></span>                                                           | <span data-ttu-id="38ae0-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="38ae0-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="38ae0-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="38ae0-122">**RequestStateChange**</span></span>](msvm-syntheticethernetport-requeststatechange.md) | <span data-ttu-id="38ae0-123">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="38ae0-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="38ae0-124">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="38ae0-124">**Reset**</span></span>](msvm-syntheticethernetport-reset.md)                           | <span data-ttu-id="38ae0-125">Выполняет сброс устройства.</span><span class="sxs-lookup"><span data-stu-id="38ae0-125">Resets the device.</span></span><br/>            |
| <span data-ttu-id="38ae0-126">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="38ae0-126">**RestoreProperties**</span></span>                                                       | <span data-ttu-id="38ae0-127">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="38ae0-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="38ae0-128">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="38ae0-128">**SaveProperties**</span></span>                                                          | <span data-ttu-id="38ae0-129">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="38ae0-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="38ae0-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="38ae0-130">**SetPowerState**</span></span>                                                           | <span data-ttu-id="38ae0-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="38ae0-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="38ae0-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="38ae0-132">Properties</span></span>

<span data-ttu-id="38ae0-133">Класс **мсвм \_ синсетицесернетпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="38ae0-133">The **Msvm\_SyntheticEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38ae0-134">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="38ae0-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-135">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38ae0-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-137">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="38ae0-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-138">Допустимое число активных или согласованных максимальных единиц передачи (MTU).</span><span class="sxs-lookup"><span data-stu-id="38ae0-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="38ae0-139">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-140">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="38ae0-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-141">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="38ae0-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-143">Дополнительные доступность и состояние устройства, кроме указанного в свойстве **Availability** .</span><span class="sxs-lookup"><span data-stu-id="38ae0-143">Additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="38ae0-144">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="38ae0-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-145">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="38ae0-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-146">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="38ae0-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-148">Указывает, может ли сетевой порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="38ae0-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="38ae0-149">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-150">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="38ae0-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-153">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="38ae0-153">The primary availability and status of the device.</span></span> <span data-ttu-id="38ae0-154">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="38ae0-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-155">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="38ae0-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-156">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="38ae0-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-158">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="38ae0-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="38ae0-159">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="38ae0-160">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="38ae0-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="38ae0-161">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="38ae0-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="38ae0-162">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="38ae0-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="38ae0-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="38ae0-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="38ae0-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="38ae0-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="38ae0-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="38ae0-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="38ae0-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="38ae0-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="38ae0-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="38ae0-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="38ae0-173">)</span><span class="sxs-lookup"><span data-stu-id="38ae0-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="38ae0-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="38ae0-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-175">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="38ae0-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-177">Возможности порта Ethernet.</span><span class="sxs-lookup"><span data-stu-id="38ae0-177">The capabilities of the Ethernet port.</span></span> <span data-ttu-id="38ae0-178">Например, устройство может поддерживать Алертонлан, Вакеонлан, балансировку нагрузки или отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="38ae0-178">For example, the device might support AlertOnLan, WakeOnLan, Load Balancing, or FailOver.</span></span> <span data-ttu-id="38ae0-179">Если в списке перечислены возможности отработки отказа или балансировки нагрузки, необходимо также определить Спареграуп (отработку отказа) или ЕкстракапаЦитиграуп (Балансировка нагрузки), чтобы полностью описать эту возможность.</span><span class="sxs-lookup"><span data-stu-id="38ae0-179">If failover or load balancing capabilities are listed, a SpareGroup (failover) or ExtraCapacityGroup (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="38ae0-180">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) и не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-181">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="38ae0-181">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-182">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="38ae0-182">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-184">Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из функций Есернетпорт, указанных в массиве свойств **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="38ae0-184">An array of free-form strings that provides more detailed explanations for any of the EthernetPort features that are indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="38ae0-185">Обратите внимание, что каждая запись этого массива связана с записью в массиве свойств **capabilities** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="38ae0-185">Note, each entry of this array is related to the entry in the **Capabilities** property array that is located at the same index.</span></span> <span data-ttu-id="38ae0-186">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) и не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-186">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-187">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="38ae0-187">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-190">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="38ae0-190">A short description of the object.</span></span> <span data-ttu-id="38ae0-191">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-191">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-192">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="38ae0-192">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-193">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-195">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="38ae0-195">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="38ae0-196">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="38ae0-196">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="38ae0-197">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-198">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="38ae0-198">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-201">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="38ae0-201">The name of the class or the subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="38ae0-202">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="38ae0-202">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-203">**Описание**</span><span class="sxs-lookup"><span data-stu-id="38ae0-203">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-206">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="38ae0-206">A description of the object.</span></span> <span data-ttu-id="38ae0-207">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-207">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-208">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="38ae0-208">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-209">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-211">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="38ae0-211">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="38ae0-212">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="38ae0-212">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="38ae0-213">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-214">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="38ae0-214">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-217">Адрес или другие идентифицирующие сведения, используемые для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="38ae0-217">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="38ae0-218">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="38ae0-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-219">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="38ae0-219">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-220">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-222">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="38ae0-222">A display name for the object.</span></span> <span data-ttu-id="38ae0-223">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-223">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-224">**енабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="38ae0-224">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-225">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="38ae0-225">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-227">Возможности, включенные из списка всех поддерживаемых, определенных в массиве свойств **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="38ae0-227">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** property array.</span></span> <span data-ttu-id="38ae0-228">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-228">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-229">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="38ae0-229">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-230">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-232">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="38ae0-232">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="38ae0-233">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="38ae0-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-235">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-237">Включенные и отключенные состояния этого элемента.</span><span class="sxs-lookup"><span data-stu-id="38ae0-237">The enabled and disabled states of this element.</span></span> <span data-ttu-id="38ae0-238">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-238">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-239">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="38ae0-239">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-240">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="38ae0-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-242">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="38ae0-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-246">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-247">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="38ae0-247">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-248">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="38ae0-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-250">Указывает, работает ли порт в режиме полного дуплекса.</span><span class="sxs-lookup"><span data-stu-id="38ae0-250">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="38ae0-251">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-251">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="38ae0-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-253">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-255">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="38ae0-255">The current health of the element.</span></span> <span data-ttu-id="38ae0-256">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="38ae0-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-258">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="38ae0-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-260">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="38ae0-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="38ae0-261">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="38ae0-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-263">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="38ae0-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-265">Дата добавления порта Ethernet в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="38ae0-265">The date the Ethernet port was added to the virtual machine.</span></span> <span data-ttu-id="38ae0-266">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-267">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="38ae0-267">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-268">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-270">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="38ae0-270">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-271">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="38ae0-271">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="38ae0-272">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-272">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-273">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="38ae0-273">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-274">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38ae0-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-276">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-276">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-277">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="38ae0-277">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-278">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-280">Перечисление типов ссылок.</span><span class="sxs-lookup"><span data-stu-id="38ae0-280">An enumeration of the types of links.</span></span> <span data-ttu-id="38ae0-281">Если задано значение 1 (другое), связанное свойство **осерлинктечнологи** содержит строковое описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="38ae0-281">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="38ae0-282">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-282">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="38ae0-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="38ae0-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="38ae0-284">**максдатасизе**</span><span class="sxs-lookup"><span data-stu-id="38ae0-284">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-285">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38ae0-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-287">Максимальный размер поля сведений (не MAC), которое будет получено или передано.</span><span class="sxs-lookup"><span data-stu-id="38ae0-287">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="38ae0-288">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-288">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-289">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="38ae0-289">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-290">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38ae0-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-292">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-293">**максспид**</span><span class="sxs-lookup"><span data-stu-id="38ae0-293">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-294">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38ae0-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-296">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="38ae0-296">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-297">Максимальная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="38ae0-297">The maximum bandwidth of the port in bits per second.</span></span> <span data-ttu-id="38ae0-298">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-298">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-299">**Name**</span><span class="sxs-lookup"><span data-stu-id="38ae0-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-302">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="38ae0-302">A display name for the object.</span></span> <span data-ttu-id="38ae0-303">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-303">This property is inherited from [**CIM\_ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-304">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="38ae0-304">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-305">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="38ae0-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-307">MAC-адреса Ethernet/802.3 отформатированы как двенадцать шестнадцатеричных цифр (например, "010203040506"). Каждая пара представляет один из шести октетов MAC-адреса в каноническом порядке (бит адреса группы находится в младших битах первого символа строки).</span><span class="sxs-lookup"><span data-stu-id="38ae0-307">Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="38ae0-308">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)и не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-308">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-309">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="38ae0-309">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-310">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-312">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="38ae0-312">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="38ae0-313">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="38ae0-313">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="38ae0-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="38ae0-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-316">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="38ae0-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-318">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="38ae0-318">The current status of the element.</span></span> <span data-ttu-id="38ae0-319">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="38ae0-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-320">**осеренабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="38ae0-320">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-321">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="38ae0-321">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-323">Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из включенных возможностей, указанных как "Other".</span><span class="sxs-lookup"><span data-stu-id="38ae0-323">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="38ae0-324">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) и не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-324">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-325">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="38ae0-325">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-328">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="38ae0-328">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="38ae0-329">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="38ae0-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-331">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="38ae0-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-333">Любые данные в дополнение к сведениям об ИДЕНТИФИКАТОРе устройства, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="38ae0-333">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="38ae0-334">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованной модели и не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-335">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="38ae0-335">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-338">Строковое значение, описывающее **линктечнологи** , если оно имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="38ae0-338">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="38ae0-339">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-339">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-340">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="38ae0-340">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-341">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-343">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="38ae0-343">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-344">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="38ae0-344">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-347">Тип модуля, когда для **portType** задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="38ae0-347">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="38ae0-348">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-348">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-349">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="38ae0-349">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-350">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-352">Сетевой адрес, который жестко закодирован в порт.</span><span class="sxs-lookup"><span data-stu-id="38ae0-352">The network address that is hardcoded into the port.</span></span> <span data-ttu-id="38ae0-353">Этот жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="38ae0-353">This hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="38ae0-354">При внесении этого изменения поле должно быть обновлено одновременно.</span><span class="sxs-lookup"><span data-stu-id="38ae0-354">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="38ae0-355">Если для сетевого адаптера не существует жестко закодированного адреса, свойство **перманентаддресс** должно оставаться пустым.</span><span class="sxs-lookup"><span data-stu-id="38ae0-355">The **PermanentAddress** property should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="38ae0-356">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-356">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-357">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="38ae0-357">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-358">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-360">Сетевые порты часто нумеруются относительно логического модуля или сетевого элемента.</span><span class="sxs-lookup"><span data-stu-id="38ae0-360">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="38ae0-361">Это значение равно 1 для эмулированных сетевых карт, 0 — для всех остальных.</span><span class="sxs-lookup"><span data-stu-id="38ae0-361">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="38ae0-362">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-363">**Порта**</span><span class="sxs-lookup"><span data-stu-id="38ae0-363">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-364">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-366">Конкретный режим, который в данный момент включен для порта.</span><span class="sxs-lookup"><span data-stu-id="38ae0-366">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="38ae0-367">Если задано значение 1 (другое), связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="38ae0-367">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="38ae0-368">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-368">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-369">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="38ae0-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-370">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="38ae0-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-372">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-373">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="38ae0-373">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-374">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="38ae0-374">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-376">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-376">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-377">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="38ae0-377">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-378">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38ae0-378">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-379">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-380">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-381">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="38ae0-381">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-382">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-384">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="38ae0-384">Provides high level status information.</span></span> <span data-ttu-id="38ae0-385">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="38ae0-385">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="38ae0-386">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="38ae0-386">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="38ae0-387">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-388">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="38ae0-388">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-389">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38ae0-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-391">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="38ae0-391">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-392">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="38ae0-392">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="38ae0-393">Фактическая пропускная способность указывается в свойстве **Speed** .</span><span class="sxs-lookup"><span data-stu-id="38ae0-393">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="38ae0-394">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-394">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="38ae0-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-396">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-398">Последнее запрошенное или требуемое состояние для службы управления.</span><span class="sxs-lookup"><span data-stu-id="38ae0-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="38ae0-399">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-400">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="38ae0-400">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-401">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38ae0-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-403">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="38ae0-403">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-404">Текущая пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="38ae0-404">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="38ae0-405">Для портов, которые зависят от пропускной способности или для тех, для которых не удается выполнить точную оценку, это свойство должно содержать номинальную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="38ae0-405">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="38ae0-406">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-406">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-407">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="38ae0-407">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-408">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-410">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="38ae0-410">The current status of the element.</span></span> <span data-ttu-id="38ae0-411">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-412">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="38ae0-412">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-413">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="38ae0-413">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-415">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="38ae0-415">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="38ae0-416">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="38ae0-416">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-417">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="38ae0-417">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-418">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-420">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-421">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="38ae0-421">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-422">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38ae0-422">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-423">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-424">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="38ae0-424">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-425">Поддерживаемый максимальный размер блока передачи (MTU).</span><span class="sxs-lookup"><span data-stu-id="38ae0-425">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="38ae0-426">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="38ae0-426">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-427">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="38ae0-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-428">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-430">Имя класса создания для системы области.</span><span class="sxs-lookup"><span data-stu-id="38ae0-430">The creation class name of the scoping system.</span></span> <span data-ttu-id="38ae0-431">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="38ae0-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-432">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="38ae0-432">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-433">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="38ae0-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-435">NetBIOS-имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="38ae0-435">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="38ae0-436">Это свойство будет содержать идентификатор виртуальной машины в виде **идентификатора GUID** .</span><span class="sxs-lookup"><span data-stu-id="38ae0-436">This property will contain the virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="38ae0-437">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="38ae0-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-438">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="38ae0-438">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-439">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="38ae0-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-441">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="38ae0-441">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="38ae0-442">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-443">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="38ae0-443">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-444">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38ae0-444">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-445">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-446">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="38ae0-446">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-447">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="38ae0-447">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-448">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-450">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="38ae0-450">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="38ae0-451">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-451">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="38ae0-452">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="38ae0-452">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38ae0-453">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38ae0-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38ae0-454">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38ae0-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38ae0-455">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="38ae0-455">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="38ae0-456">При отсутствии ограничений на использование порта значение должно быть равно 4 (не ограничено).</span><span class="sxs-lookup"><span data-stu-id="38ae0-456">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="38ae0-457">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="38ae0-457">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38ae0-458">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38ae0-458">Remarks</span></span>

<span data-ttu-id="38ae0-459">Доступ к классу **\_ синсетицесернетпорт мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="38ae0-459">Access to the **Msvm\_SyntheticEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="38ae0-460">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="38ae0-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="38ae0-461">Примеры</span><span class="sxs-lookup"><span data-stu-id="38ae0-461">Examples</span></span>

<span data-ttu-id="38ae0-462">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="38ae0-462">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38ae0-463">Требования</span><span class="sxs-lookup"><span data-stu-id="38ae0-463">Requirements</span></span>



| <span data-ttu-id="38ae0-464">Требование</span><span class="sxs-lookup"><span data-stu-id="38ae0-464">Requirement</span></span> | <span data-ttu-id="38ae0-465">Значение</span><span class="sxs-lookup"><span data-stu-id="38ae0-465">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38ae0-466">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38ae0-466">Minimum supported client</span></span><br/> | <span data-ttu-id="38ae0-467">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="38ae0-467">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="38ae0-468">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38ae0-468">Minimum supported server</span></span><br/> | <span data-ttu-id="38ae0-469">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="38ae0-469">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38ae0-470">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38ae0-470">Namespace</span></span><br/>                | <span data-ttu-id="38ae0-471">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="38ae0-471">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="38ae0-472">MOF</span><span class="sxs-lookup"><span data-stu-id="38ae0-472">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38ae0-473"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38ae0-473"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38ae0-474">DLL</span><span class="sxs-lookup"><span data-stu-id="38ae0-474">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38ae0-475"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38ae0-475"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38ae0-476">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38ae0-476">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ae0-477">**\_ЕСЕРНЕТПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="38ae0-477">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="38ae0-478">**\_ЕСЕРНЕТПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="38ae0-478">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

