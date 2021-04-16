---
description: Представляет внешний порт Ethernet (сетевой адаптер).
ms.assetid: 70901587-641D-46F5-8A35-FEA483D336DE
title: Класс Msvm_ExternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPort
- Msvm_ExternalEthernetPort.SetPowerState
- Msvm_ExternalEthernetPort.EnableDevice
- Msvm_ExternalEthernetPort.OnlineDevice
- Msvm_ExternalEthernetPort.QuiesceDevice
- Msvm_ExternalEthernetPort.SaveProperties
- Msvm_ExternalEthernetPort.RestoreProperties
- Msvm_ExternalEthernetPort.InstanceID
- Msvm_ExternalEthernetPort.Caption
- Msvm_ExternalEthernetPort.Description
- Msvm_ExternalEthernetPort.ElementName
- Msvm_ExternalEthernetPort.InstallDate
- Msvm_ExternalEthernetPort.Name
- Msvm_ExternalEthernetPort.OperationalStatus
- Msvm_ExternalEthernetPort.StatusDescriptions
- Msvm_ExternalEthernetPort.Status
- Msvm_ExternalEthernetPort.HealthState
- Msvm_ExternalEthernetPort.CommunicationStatus
- Msvm_ExternalEthernetPort.DetailedStatus
- Msvm_ExternalEthernetPort.OperatingStatus
- Msvm_ExternalEthernetPort.PrimaryStatus
- Msvm_ExternalEthernetPort.EnabledState
- Msvm_ExternalEthernetPort.OtherEnabledState
- Msvm_ExternalEthernetPort.RequestedState
- Msvm_ExternalEthernetPort.EnabledDefault
- Msvm_ExternalEthernetPort.TimeOfLastStateChange
- Msvm_ExternalEthernetPort.AvailableRequestedStates
- Msvm_ExternalEthernetPort.TransitioningToState
- Msvm_ExternalEthernetPort.SystemCreationClassName
- Msvm_ExternalEthernetPort.SystemName
- Msvm_ExternalEthernetPort.CreationClassName
- Msvm_ExternalEthernetPort.DeviceID
- Msvm_ExternalEthernetPort.PowerManagementSupported
- Msvm_ExternalEthernetPort.PowerManagementCapabilities
- Msvm_ExternalEthernetPort.Availability
- Msvm_ExternalEthernetPort.StatusInfo
- Msvm_ExternalEthernetPort.LastErrorCode
- Msvm_ExternalEthernetPort.ErrorDescription
- Msvm_ExternalEthernetPort.ErrorCleared
- Msvm_ExternalEthernetPort.OtherIdentifyingInfo
- Msvm_ExternalEthernetPort.PowerOnHours
- Msvm_ExternalEthernetPort.TotalPowerOnHours
- Msvm_ExternalEthernetPort.IdentifyingDescriptions
- Msvm_ExternalEthernetPort.AdditionalAvailability
- Msvm_ExternalEthernetPort.MaxQuiesceTime
- Msvm_ExternalEthernetPort.Speed
- Msvm_ExternalEthernetPort.MaxSpeed
- Msvm_ExternalEthernetPort.RequestedSpeed
- Msvm_ExternalEthernetPort.UsageRestriction
- Msvm_ExternalEthernetPort.PortType
- Msvm_ExternalEthernetPort.OtherPortType
- Msvm_ExternalEthernetPort.OtherNetworkPortType
- Msvm_ExternalEthernetPort.PortNumber
- Msvm_ExternalEthernetPort.LinkTechnology
- Msvm_ExternalEthernetPort.OtherLinkTechnology
- Msvm_ExternalEthernetPort.PermanentAddress
- Msvm_ExternalEthernetPort.NetworkAddresses
- Msvm_ExternalEthernetPort.FullDuplex
- Msvm_ExternalEthernetPort.AutoSense
- Msvm_ExternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.MaxDataSize
- Msvm_ExternalEthernetPort.Capabilities
- Msvm_ExternalEthernetPort.CapabilityDescriptions
- Msvm_ExternalEthernetPort.EnabledCapabilities
- Msvm_ExternalEthernetPort.OtherEnabledCapabilities
- Msvm_ExternalEthernetPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 507c2235c1fda5f43ba025172e276b30e2f0aa85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542495"
---
# <a name="msvm_externalethernetport-class"></a><span data-ttu-id="79306-103">\_Класс мсвм екстерналесернетпорт</span><span class="sxs-lookup"><span data-stu-id="79306-103">Msvm\_ExternalEthernetPort class</span></span>

<span data-ttu-id="79306-104">Представляет внешний порт Ethernet (сетевой адаптер).</span><span class="sxs-lookup"><span data-stu-id="79306-104">Represents an external Ethernet port (network adapter).</span></span> <span data-ttu-id="79306-105">Эти типы портов Ethernet предоставляют виртуальным машинам доступ к внешней сети.</span><span class="sxs-lookup"><span data-stu-id="79306-105">These types of Ethernet ports give virtual machines access to the external network.</span></span>

<span data-ttu-id="79306-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="79306-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79306-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79306-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft External Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
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
  string   CreationClassName = "Msvm_ExternalEthernetPort";
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
  string   AdditionalAvailability[];
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="79306-108">Члены</span><span class="sxs-lookup"><span data-stu-id="79306-108">Members</span></span>

<span data-ttu-id="79306-109">Класс **мсвм \_ екстерналесернетпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="79306-109">The **Msvm\_ExternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="79306-110">Методы</span><span class="sxs-lookup"><span data-stu-id="79306-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="79306-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="79306-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="79306-112">Методы</span><span class="sxs-lookup"><span data-stu-id="79306-112">Methods</span></span>

<span data-ttu-id="79306-113">Класс **мсвм \_ екстерналесернетпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="79306-113">The **Msvm\_ExternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="79306-114">Метод</span><span class="sxs-lookup"><span data-stu-id="79306-114">Method</span></span>                                                                     | <span data-ttu-id="79306-115">Описание</span><span class="sxs-lookup"><span data-stu-id="79306-115">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="79306-116">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="79306-116">**EnableDevice**</span></span>                                                           | <span data-ttu-id="79306-117">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="79306-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="79306-118">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="79306-118">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="79306-119">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="79306-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="79306-120">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="79306-120">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="79306-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="79306-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="79306-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="79306-122">**RequestStateChange**</span></span>](msvm-externalethernetport-requeststatechange.md) | <span data-ttu-id="79306-123">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="79306-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="79306-124">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="79306-124">**Reset**</span></span>](msvm-externalethernetport-reset.md)                           | <span data-ttu-id="79306-125">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="79306-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="79306-126">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="79306-126">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="79306-127">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="79306-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="79306-128">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="79306-128">**SaveProperties**</span></span>                                                         | <span data-ttu-id="79306-129">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="79306-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="79306-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="79306-130">**SetPowerState**</span></span>                                                          | <span data-ttu-id="79306-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="79306-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="79306-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="79306-132">Properties</span></span>

<span data-ttu-id="79306-133">Класс **мсвм \_ екстерналесернетпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="79306-133">The **Msvm\_ExternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79306-134">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="79306-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-135">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79306-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79306-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79306-137">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="79306-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="79306-138">Количество активных или согласованных максимальных единиц передачи (MTU), которые могут поддерживаться в байтах.</span><span class="sxs-lookup"><span data-stu-id="79306-138">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="79306-139">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-140">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="79306-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-141">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="79306-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-143">Любая дополнительная доступность и состояние устройства, кроме указанного в свойстве **Availability** .</span><span class="sxs-lookup"><span data-stu-id="79306-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="79306-144">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-145">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="79306-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-146">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="79306-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79306-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-148">Указывает, может ли сетевой порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="79306-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="79306-149">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-150">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="79306-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-153">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="79306-153">The primary availability and status of the device.</span></span> <span data-ttu-id="79306-154">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-155">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="79306-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-156">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="79306-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-158">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="79306-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="79306-159">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="79306-160">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="79306-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="79306-161">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="79306-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="79306-162">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="79306-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="79306-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79306-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="79306-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79306-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="79306-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79306-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="79306-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="79306-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="79306-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="79306-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="79306-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="79306-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="79306-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="79306-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="79306-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="79306-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="79306-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="79306-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="79306-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="79306-173">)</span><span class="sxs-lookup"><span data-stu-id="79306-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79306-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="79306-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-175">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="79306-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-177">Массив, указывающий возможности порта.</span><span class="sxs-lookup"><span data-stu-id="79306-177">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="79306-178">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="79306-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="79306-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="79306-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79306-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="79306-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79306-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Алертонлан** (2)</span><span class="sxs-lookup"><span data-stu-id="79306-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79306-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Вакеонлан** (3)</span><span class="sxs-lookup"><span data-stu-id="79306-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79306-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Отработка отказа** (4)</span><span class="sxs-lookup"><span data-stu-id="79306-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79306-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="79306-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79306-185">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="79306-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-186">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="79306-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-188">Массив строк произвольной формы, содержащий более подробные пояснения к функциям порта, содержащимся в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="79306-188">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="79306-189">Каждая запись этого массива связана с соответствующей записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="79306-189">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="79306-190">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="79306-190">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-191">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="79306-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79306-194">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="79306-194">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="79306-195">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="79306-195">A short description of the object.</span></span> <span data-ttu-id="79306-196">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "порт Ethernet".</span><span class="sxs-lookup"><span data-stu-id="79306-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="79306-197">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="79306-197">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-200">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="79306-200">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="79306-201">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="79306-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="79306-202">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79306-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="79306-203">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79306-203">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-206">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="79306-206">The scoping system's creation class name.</span></span> <span data-ttu-id="79306-207">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ екстерналесернетпорт".</span><span class="sxs-lookup"><span data-stu-id="79306-207">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ExternalEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="79306-208">**Описание**</span><span class="sxs-lookup"><span data-stu-id="79306-208">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-211">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="79306-211">A description of the object.</span></span> <span data-ttu-id="79306-212">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "внешний порт Ethernet Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="79306-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="79306-213">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="79306-213">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-214">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-216">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="79306-216">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="79306-217">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="79306-217">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="79306-218">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79306-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="79306-219">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="79306-219">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-220">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-222">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="79306-222">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="79306-223">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="79306-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="79306-224">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="79306-224">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-227">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="79306-227">A display name for the object.</span></span> <span data-ttu-id="79306-228">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="79306-228">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="79306-229">**енабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="79306-229">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-230">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="79306-230">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-232">Указывает, какие возможности включены из списка всех поддерживаемых возможностей в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="79306-232">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="79306-233">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="79306-233">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="79306-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="79306-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79306-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="79306-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79306-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**Алертонлан** (2)</span><span class="sxs-lookup"><span data-stu-id="79306-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79306-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Вакеонлан** (3)</span><span class="sxs-lookup"><span data-stu-id="79306-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79306-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Отработка отказа** (4)</span><span class="sxs-lookup"><span data-stu-id="79306-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79306-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="79306-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79306-240">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="79306-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-241">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-243">Конфигурация по умолчанию или запуск администратора для свойства **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="79306-243">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="79306-244">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="79306-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="79306-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="79306-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-246">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-248">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="79306-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="79306-249">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="79306-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="79306-250">Например, завершение работы (4) и запуск (10) являются временными состояниями между включенным и отключенным.</span><span class="sxs-lookup"><span data-stu-id="79306-250">For example, shutting down (4) and starting (10) are transient states between enabled and disabled.</span></span> <span data-ttu-id="79306-251">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-251">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="79306-252">Значение</span><span class="sxs-lookup"><span data-stu-id="79306-252">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="79306-253">Значение</span><span class="sxs-lookup"><span data-stu-id="79306-253">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="79306-254"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="79306-254"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="79306-255"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="79306-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="79306-256"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="79306-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="79306-257">Элемент или может выполнять команды, обрабатывает все команды в очереди и помещает новые запросы в очередь.</span><span class="sxs-lookup"><span data-stu-id="79306-257">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="79306-258"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="79306-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="79306-259">Элемент не будет выполнять команды и удалит все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="79306-259">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="79306-260"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="79306-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="79306-261">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="79306-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="79306-262"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="79306-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="79306-263">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="79306-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="79306-264"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="79306-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="79306-265">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="79306-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="79306-266"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="79306-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="79306-267">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="79306-267">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="79306-268"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="79306-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="79306-269">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="79306-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="79306-270"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="79306-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="79306-271">Элемент включен, но в режиме с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="79306-271">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="79306-272">Поведение элемента аналогично включенному состоянию, но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="79306-272">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="79306-273">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="79306-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="79306-274"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="79306-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="79306-275">Элемент находится в процессе перехода в состояние Enabled.</span><span class="sxs-lookup"><span data-stu-id="79306-275">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="79306-276">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="79306-276">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="79306-277"><dt>**Зарезервировано**</dt> <dt>11 32767</dt> в формате DMTF</span><span class="sxs-lookup"><span data-stu-id="79306-277"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="79306-278">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="79306-278">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="79306-279"><dt>**Поставщик Зарезервированный**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="79306-279"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="79306-280">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="79306-280">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="79306-281">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="79306-281">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-282">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="79306-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79306-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-284">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="79306-284">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="79306-285">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-285">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-286">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="79306-286">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-289">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="79306-289">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="79306-290">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-290">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-291">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="79306-291">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-292">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="79306-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79306-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-294">Указывает, работает ли порт в режиме полного дуплекса.</span><span class="sxs-lookup"><span data-stu-id="79306-294">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="79306-295">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-295">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-296">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="79306-296">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-297">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-299">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="79306-299">The current health of the element.</span></span> <span data-ttu-id="79306-300">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="79306-300">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="79306-301">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="79306-301">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="79306-302">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="79306-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="79306-303">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="79306-303">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-304">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="79306-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-306">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="79306-306">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="79306-307">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="79306-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-309">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79306-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79306-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-311">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="79306-311">The date and time when the object was installed.</span></span> <span data-ttu-id="79306-312">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="79306-312">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="79306-313">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79306-313">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="79306-314">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="79306-314">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79306-317">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="79306-317">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="79306-318">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="79306-318">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="79306-319">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="79306-319">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="79306-320">**С привязкой**</span><span class="sxs-lookup"><span data-stu-id="79306-320">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-321">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="79306-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79306-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-323">Если это свойство имеет **значение true**, то этот порт Ethernet может быть подключен к коммутаторам и тем самым может обеспечить подключение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="79306-323">If this property is **True**, then this Ethernet port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="79306-324">Если это свойство имеет **значение false**, то этот порт Ethernet не используется сетевой архитектурой виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="79306-324">If this property is **False**, then this Ethernet port is not being used by the virtual machine networking architecture.</span></span>

</dd> <dt>

<span data-ttu-id="79306-325">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="79306-325">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-326">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79306-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79306-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-328">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="79306-328">The last error code reported by the logical device.</span></span> <span data-ttu-id="79306-329">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-329">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-330">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="79306-330">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-331">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-333">Указывает тип технологии ссылок для порта.</span><span class="sxs-lookup"><span data-stu-id="79306-333">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="79306-334">Если задано значение 1 (другое), свойство **осерлинктечнологи** содержит строковое описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="79306-334">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="79306-335">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-335">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="79306-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="79306-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79306-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="79306-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79306-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="79306-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79306-339"><span id="IB"></span><span id="ib"></span>**ГЕО(3** )</span><span class="sxs-lookup"><span data-stu-id="79306-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79306-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="79306-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79306-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="79306-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="79306-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="79306-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="79306-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="79306-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="79306-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="79306-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="79306-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Инфракрасная связь** (9)</span><span class="sxs-lookup"><span data-stu-id="79306-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="79306-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="79306-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="79306-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Беспроводная локальная сеть** (11)</span><span class="sxs-lookup"><span data-stu-id="79306-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Wireless LAN** (11)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79306-348">**максдатасизе**</span><span class="sxs-lookup"><span data-stu-id="79306-348">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-349">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79306-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79306-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-351">Максимальный размер поля сведений (не MAC), которое будет получено или передано.</span><span class="sxs-lookup"><span data-stu-id="79306-351">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="79306-352">Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)и всегда имеет значение 1500.</span><span class="sxs-lookup"><span data-stu-id="79306-352">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="79306-353">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="79306-353">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-354">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79306-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79306-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-356">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="79306-356">This property has been deprecated.</span></span> <span data-ttu-id="79306-357">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-357">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-358">**максспид**</span><span class="sxs-lookup"><span data-stu-id="79306-358">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-359">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79306-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79306-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79306-361">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="79306-361">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="79306-362">Максимальная пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="79306-362">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="79306-363">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79306-364">**Name**</span><span class="sxs-lookup"><span data-stu-id="79306-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-365">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-367">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="79306-367">The label by which the object is known.</span></span> <span data-ttu-id="79306-368">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79306-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="79306-369">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="79306-369">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-370">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="79306-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79306-372">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="79306-372">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="79306-373">Массив строк, содержащих MAC-адреса для порта.</span><span class="sxs-lookup"><span data-stu-id="79306-373">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="79306-374">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-374">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-375">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="79306-375">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-376">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-378">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="79306-378">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="79306-379">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="79306-379">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="79306-380">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79306-380">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="79306-381">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="79306-381">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-382">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="79306-382">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-384">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="79306-384">The current statuses of the object.</span></span> <span data-ttu-id="79306-385">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="79306-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="79306-386">**осеренабледкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="79306-386">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-387">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="79306-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-389">Массив строк произвольной формы, предоставляющий более подробные объяснения для любой из включенных возможностей, указанных как 1 (другой). Это свойство наследуется от [**CIM \_ есернетпорт**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="79306-389">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-390">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="79306-390">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-391">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-393">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="79306-393">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="79306-394">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="79306-394">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="79306-395">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79306-396">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="79306-396">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-397">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="79306-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-398">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-399">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="79306-399">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="79306-400">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-401">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="79306-401">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-402">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-404">Строковое значение, описывающее **линктечнологи** , если оно имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="79306-404">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="79306-405">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-405">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-406">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="79306-406">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-407">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-409">Использование этого свойства не рекомендуется использовать вместо свойства **portType** .</span><span class="sxs-lookup"><span data-stu-id="79306-409">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="79306-410">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-410">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-411">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="79306-411">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-412">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-414">Тип модуля, когда для **portType** задано значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="79306-414">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="79306-415">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-415">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79306-416">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="79306-416">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-417">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79306-419">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="79306-419">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="79306-420">Сетевой адрес, жестко закодированный в порт.</span><span class="sxs-lookup"><span data-stu-id="79306-420">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="79306-421">Этот жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="79306-421">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="79306-422">При внесении этого изменения поле должно быть обновлено одновременно.</span><span class="sxs-lookup"><span data-stu-id="79306-422">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="79306-423">Это свойство должно иметь **значение NULL** , если для сетевого адаптера не существует жестко закодированного адреса.</span><span class="sxs-lookup"><span data-stu-id="79306-423">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="79306-424">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-424">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-425">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="79306-425">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-426">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-427">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-428">номер порта.</span><span class="sxs-lookup"><span data-stu-id="79306-428">The port number.</span></span> <span data-ttu-id="79306-429">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-429">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-430">**Порта**</span><span class="sxs-lookup"><span data-stu-id="79306-430">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-431">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-433">Конкретный режим, который в данный момент включен для порта.</span><span class="sxs-lookup"><span data-stu-id="79306-433">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="79306-434">Если задано значение 1 ("другое"), связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="79306-434">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="79306-435">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="79306-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="79306-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79306-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="79306-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79306-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 медный** (50)</span><span class="sxs-lookup"><span data-stu-id="79306-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="79306-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BASE** (51)</span><span class="sxs-lookup"><span data-stu-id="79306-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="79306-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BASE** (52)</span><span class="sxs-lookup"><span data-stu-id="79306-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="79306-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BASE** (53)</span><span class="sxs-lookup"><span data-stu-id="79306-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="79306-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="79306-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="79306-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="79306-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="79306-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="79306-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="79306-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="79306-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="79306-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="79306-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="79306-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="79306-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="79306-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="79306-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="79306-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="79306-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="79306-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="79306-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="79306-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="79306-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="79306-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="79306-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="79306-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="79306-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="79306-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-лв** (109)</span><span class="sxs-lookup"><span data-stu-id="79306-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="79306-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="79306-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="79306-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ать** (111)</span><span class="sxs-lookup"><span data-stu-id="79306-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="79306-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="79306-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79306-458">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="79306-458">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-459">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="79306-459">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-461">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="79306-461">The power management capabilities of the device.</span></span> <span data-ttu-id="79306-462">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-463">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="79306-463">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-464">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="79306-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79306-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-466">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="79306-466">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="79306-467">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-468">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="79306-468">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-469">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79306-469">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79306-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-471">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="79306-471">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="79306-472">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-473">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="79306-473">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-474">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-474">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-476">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="79306-476">Provides high level status information.</span></span> <span data-ttu-id="79306-477">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="79306-477">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="79306-478">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="79306-478">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="79306-479">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79306-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="79306-480">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="79306-480">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-481">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79306-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79306-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79306-483">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="79306-483">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="79306-484">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="79306-484">The requested bandwidth of the port in bits per second.</span></span> <span data-ttu-id="79306-485">Фактическая пропускная способность указывается в свойстве **Speed** .</span><span class="sxs-lookup"><span data-stu-id="79306-485">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="79306-486">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-486">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79306-487">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="79306-487">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-488">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-489">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-490">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="79306-490">The last requested or desired state for the element.</span></span> <span data-ttu-id="79306-491">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="79306-491">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="79306-492">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="79306-492">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-493">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79306-493">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79306-494">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79306-495">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="79306-495">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="79306-496">Пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="79306-496">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="79306-497">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-497">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79306-498">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="79306-498">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-499">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-500">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-501">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="79306-501">The current status of the object.</span></span> <span data-ttu-id="79306-502">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79306-502">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="79306-503">'</span><span class="sxs-lookup"><span data-stu-id="79306-503">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="79306-504"><span id="OK"></span><span id="ok"></span>**Хорошо**</span><span class="sxs-lookup"><span data-stu-id="79306-504"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="79306-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**План**</span><span class="sxs-lookup"><span data-stu-id="79306-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="79306-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Пониженной функциональности**</span><span class="sxs-lookup"><span data-stu-id="79306-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="79306-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестный**</span><span class="sxs-lookup"><span data-stu-id="79306-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="79306-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Пред — сбой**</span><span class="sxs-lookup"><span data-stu-id="79306-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="79306-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Start**</span><span class="sxs-lookup"><span data-stu-id="79306-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="79306-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Идет**</span><span class="sxs-lookup"><span data-stu-id="79306-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="79306-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служеб**</span><span class="sxs-lookup"><span data-stu-id="79306-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="79306-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Груз**</span><span class="sxs-lookup"><span data-stu-id="79306-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="79306-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Невосстановление**</span><span class="sxs-lookup"><span data-stu-id="79306-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="79306-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта**</span><span class="sxs-lookup"><span data-stu-id="79306-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="79306-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Потеря связи**</span><span class="sxs-lookup"><span data-stu-id="79306-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79306-516">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="79306-516">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-517">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="79306-517">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79306-518">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-519">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="79306-519">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="79306-520">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="79306-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="79306-521">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="79306-521">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-522">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-522">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-523">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-524">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="79306-524">The current state of the logical device.</span></span> <span data-ttu-id="79306-525">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-525">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-526">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="79306-526">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-527">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79306-527">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79306-528">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79306-529">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="79306-529">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="79306-530">Максимальный поддерживаемый размер блока передачи (MTU) в байтах.</span><span class="sxs-lookup"><span data-stu-id="79306-530">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="79306-531">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="79306-531">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="79306-532">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="79306-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-533">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-534">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-535">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="79306-535">The scoping system's creation class name.</span></span> <span data-ttu-id="79306-536">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="79306-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="79306-537">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="79306-537">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-538">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79306-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79306-539">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-540">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="79306-540">The name of the scoping system.</span></span> <span data-ttu-id="79306-541">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="79306-541">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="79306-542">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="79306-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-543">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79306-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79306-544">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-545">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="79306-545">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="79306-546">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="79306-546">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="79306-547">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="79306-547">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-548">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79306-548">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79306-549">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-550">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="79306-550">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="79306-551">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-551">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-552">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="79306-552">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-553">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-553">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-554">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-554">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-555">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="79306-555">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="79306-556">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="79306-556">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79306-557">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="79306-557">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79306-558">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79306-558">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79306-559">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79306-559">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79306-560">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="79306-560">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="79306-561">В качестве примера такой ситуации можно привести массив хранения данных, который может иметь серверные порты для взаимодействия с дисками и интерфейсными портами для взаимодействия с узлами.</span><span class="sxs-lookup"><span data-stu-id="79306-561">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="79306-562">При отсутствии ограничений на использование порта значение должно быть равно "не ограничено".</span><span class="sxs-lookup"><span data-stu-id="79306-562">If there is no restriction on the use of the port, then the value should be set to "Not restricted".</span></span> <span data-ttu-id="79306-563">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79306-563">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="79306-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="79306-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79306-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Только внешний** интерфейс (2)</span><span class="sxs-lookup"><span data-stu-id="79306-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79306-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Только серверная** части (3)</span><span class="sxs-lookup"><span data-stu-id="79306-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79306-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Не ограничено** (4)</span><span class="sxs-lookup"><span data-stu-id="79306-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Not restricted** (4)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79306-568">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79306-568">Remarks</span></span>

<span data-ttu-id="79306-569">Доступ к классу **\_ екстерналесернетпорт мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="79306-569">Access to the **Msvm\_ExternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="79306-570">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="79306-570">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="79306-571">Примеры</span><span class="sxs-lookup"><span data-stu-id="79306-571">Examples</span></span>

<span data-ttu-id="79306-572">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="79306-572">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79306-573">Требования</span><span class="sxs-lookup"><span data-stu-id="79306-573">Requirements</span></span>



| <span data-ttu-id="79306-574">Требование</span><span class="sxs-lookup"><span data-stu-id="79306-574">Requirement</span></span> | <span data-ttu-id="79306-575">Значение</span><span class="sxs-lookup"><span data-stu-id="79306-575">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79306-576">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79306-576">Minimum supported client</span></span><br/> | <span data-ttu-id="79306-577">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="79306-577">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="79306-578">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79306-578">Minimum supported server</span></span><br/> | <span data-ttu-id="79306-579">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="79306-579">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79306-580">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="79306-580">Namespace</span></span><br/>                | <span data-ttu-id="79306-581">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="79306-581">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="79306-582">MOF</span><span class="sxs-lookup"><span data-stu-id="79306-582">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79306-583"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79306-583"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79306-584">DLL</span><span class="sxs-lookup"><span data-stu-id="79306-584">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79306-585"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79306-585"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79306-586">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79306-586">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79306-587">**\_ЕСЕРНЕТПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="79306-587">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="79306-588">**\_ЕСЕРНЕТПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="79306-588">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

