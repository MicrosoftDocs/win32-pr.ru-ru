---
description: Представляет физический сетевой адаптер Wi-Fi (802,11), который можно привязать к виртуальному коммутатору для обеспечения подключения к виртуальным машинам по внешнему сетевому подключению.
ms.assetid: c6dae491-607c-4f17-aea9-162d910120c2
title: Класс Msvm_WiFiPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiPort
- Msvm_WiFiPort.RequestStateChange
- Msvm_WiFiPort.SetPowerState
- Msvm_WiFiPort.Reset
- Msvm_WiFiPort.EnableDevice
- Msvm_WiFiPort.OnlineDevice
- Msvm_WiFiPort.QuiesceDevice
- Msvm_WiFiPort.SaveProperties
- Msvm_WiFiPort.RestoreProperties
- Msvm_WiFiPort.InstanceID
- Msvm_WiFiPort.Caption
- Msvm_WiFiPort.Description
- Msvm_WiFiPort.ElementName
- Msvm_WiFiPort.InstallDate
- Msvm_WiFiPort.Name
- Msvm_WiFiPort.OperationalStatus
- Msvm_WiFiPort.StatusDescriptions
- Msvm_WiFiPort.Status
- Msvm_WiFiPort.HealthState
- Msvm_WiFiPort.CommunicationStatus
- Msvm_WiFiPort.DetailedStatus
- Msvm_WiFiPort.OperatingStatus
- Msvm_WiFiPort.PrimaryStatus
- Msvm_WiFiPort.EnabledState
- Msvm_WiFiPort.OtherEnabledState
- Msvm_WiFiPort.RequestedState
- Msvm_WiFiPort.EnabledDefault
- Msvm_WiFiPort.TimeOfLastStateChange
- Msvm_WiFiPort.AvailableRequestedStates
- Msvm_WiFiPort.TransitioningToState
- Msvm_WiFiPort.SystemCreationClassName
- Msvm_WiFiPort.SystemName
- Msvm_WiFiPort.CreationClassName
- Msvm_WiFiPort.DeviceID
- Msvm_WiFiPort.PowerManagementSupported
- Msvm_WiFiPort.PowerManagementCapabilities
- Msvm_WiFiPort.Availability
- Msvm_WiFiPort.StatusInfo
- Msvm_WiFiPort.LastErrorCode
- Msvm_WiFiPort.ErrorDescription
- Msvm_WiFiPort.ErrorCleared
- Msvm_WiFiPort.OtherIdentifyingInfo
- Msvm_WiFiPort.PowerOnHours
- Msvm_WiFiPort.TotalPowerOnHours
- Msvm_WiFiPort.IdentifyingDescriptions
- Msvm_WiFiPort.AdditionalAvailability
- Msvm_WiFiPort.MaxQuiesceTime
- Msvm_WiFiPort.Speed
- Msvm_WiFiPort.MaxSpeed
- Msvm_WiFiPort.RequestedSpeed
- Msvm_WiFiPort.UsageRestriction
- Msvm_WiFiPort.PortType
- Msvm_WiFiPort.OtherPortType
- Msvm_WiFiPort.OtherNetworkPortType
- Msvm_WiFiPort.PortNumber
- Msvm_WiFiPort.LinkTechnology
- Msvm_WiFiPort.OtherLinkTechnology
- Msvm_WiFiPort.PermanentAddress
- Msvm_WiFiPort.NetworkAddresses
- Msvm_WiFiPort.FullDuplex
- Msvm_WiFiPort.AutoSense
- Msvm_WiFiPort.SupportedMaximumTransmissionUnit
- Msvm_WiFiPort.ActiveMaximumTransmissionUnit
- Msvm_WiFiPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47ec33236c55d281755b50449a8f33a56152a07a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999692"
---
# <a name="msvm_wifiport-class"></a><span data-ttu-id="65fad-103">\_Класс мсвм вифипорт</span><span class="sxs-lookup"><span data-stu-id="65fad-103">Msvm\_WiFiPort class</span></span>

<span data-ttu-id="65fad-104">Представляет физический сетевой адаптер Wi-Fi (802,11), который можно привязать к виртуальному коммутатору для обеспечения подключения к виртуальным машинам по внешнему сетевому подключению.</span><span class="sxs-lookup"><span data-stu-id="65fad-104">Represents a physical Wi-Fi (802.11) network adapter that can be bound to a virtual switch to provide external network connectivity to virtual machines.</span></span>

<span data-ttu-id="65fad-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="65fad-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="65fad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65fad-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiPort : CIM_WiFiPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="65fad-107">Члены</span><span class="sxs-lookup"><span data-stu-id="65fad-107">Members</span></span>

<span data-ttu-id="65fad-108">Класс **мсвм \_ вифипорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="65fad-108">The **Msvm\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="65fad-109">Методы</span><span class="sxs-lookup"><span data-stu-id="65fad-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="65fad-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="65fad-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="65fad-111">Методы</span><span class="sxs-lookup"><span data-stu-id="65fad-111">Methods</span></span>

<span data-ttu-id="65fad-112">Класс **мсвм \_ вифипорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="65fad-112">The **Msvm\_WiFiPort** class has these methods.</span></span>



| <span data-ttu-id="65fad-113">Метод</span><span class="sxs-lookup"><span data-stu-id="65fad-113">Method</span></span>                 | <span data-ttu-id="65fad-114">Описание</span><span class="sxs-lookup"><span data-stu-id="65fad-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="65fad-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="65fad-115">**EnableDevice**</span></span>       | <span data-ttu-id="65fad-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="65fad-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="65fad-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="65fad-117">**OnlineDevice**</span></span>       | <span data-ttu-id="65fad-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="65fad-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="65fad-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="65fad-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="65fad-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="65fad-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="65fad-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="65fad-121">**RequestStateChange**</span></span> | <span data-ttu-id="65fad-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="65fad-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="65fad-123">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="65fad-123">**Reset**</span></span>              | <span data-ttu-id="65fad-124">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="65fad-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="65fad-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="65fad-125">**RestoreProperties**</span></span>  | <span data-ttu-id="65fad-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="65fad-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="65fad-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="65fad-127">**SaveProperties**</span></span>     | <span data-ttu-id="65fad-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="65fad-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="65fad-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="65fad-129">**SetPowerState**</span></span>      | <span data-ttu-id="65fad-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="65fad-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="65fad-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="65fad-131">Properties</span></span>

<span data-ttu-id="65fad-132">Класс **мсвм \_ вифипорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="65fad-132">The **Msvm\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65fad-133">**активемаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="65fad-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-134">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65fad-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65fad-136">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="65fad-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="65fad-137">Количество активных или согласованных максимальных единиц передачи (MTU), которые могут поддерживаться в байтах.</span><span class="sxs-lookup"><span data-stu-id="65fad-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="65fad-138">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-139">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="65fad-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-140">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="65fad-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="65fad-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-142">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="65fad-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="65fad-143">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-144">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="65fad-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-145">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65fad-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-147">Указывает, может ли порт автоматически определять скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="65fad-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="65fad-148">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-149">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="65fad-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-150">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-152">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="65fad-152">The primary availability and status of the device.</span></span> <span data-ttu-id="65fad-153">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-154">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="65fad-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-155">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="65fad-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="65fad-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-157">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="65fad-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="65fad-158">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="65fad-159">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="65fad-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="65fad-160">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="65fad-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="65fad-161">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="65fad-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="65fad-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="65fad-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="65fad-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="65fad-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="65fad-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="65fad-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="65fad-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="65fad-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="65fad-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="65fad-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="65fad-172">)</span><span class="sxs-lookup"><span data-stu-id="65fad-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="65fad-173">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="65fad-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-176">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="65fad-176">A short description of the object.</span></span> <span data-ttu-id="65fad-177">Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="65fad-177">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="65fad-178">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="65fad-178">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-181">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="65fad-181">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="65fad-182">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="65fad-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="65fad-183">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="65fad-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-187">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="65fad-187">The scoping system's creation class name.</span></span> <span data-ttu-id="65fad-188">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-189">**Описание**</span><span class="sxs-lookup"><span data-stu-id="65fad-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-192">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="65fad-192">A description of the object.</span></span> <span data-ttu-id="65fad-193">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="65fad-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-195">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-197">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="65fad-197">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="65fad-198">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="65fad-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="65fad-199">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-200">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="65fad-200">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-203">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="65fad-203">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="65fad-204">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="65fad-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-208">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="65fad-208">A display name for the object.</span></span> <span data-ttu-id="65fad-209">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-210">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="65fad-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-211">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-213">Конфигурация по умолчанию или запуск администратора для свойства **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="65fad-213">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="65fad-214">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="65fad-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-216">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-218">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="65fad-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="65fad-219">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="65fad-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="65fad-220">Значение</span><span class="sxs-lookup"><span data-stu-id="65fad-220">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="65fad-221">Значение</span><span class="sxs-lookup"><span data-stu-id="65fad-221">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="65fad-222"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="65fad-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="65fad-223">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="65fad-223">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="65fad-224"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="65fad-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="65fad-225">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="65fad-225">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="65fad-226">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="65fad-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-227">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65fad-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-229">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="65fad-229">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="65fad-230">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="65fad-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-234">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="65fad-234">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="65fad-235">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-236">**фуллдуплекс**</span><span class="sxs-lookup"><span data-stu-id="65fad-236">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-237">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65fad-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-239">Указывает, работает ли порт в режиме полного дуплекса.</span><span class="sxs-lookup"><span data-stu-id="65fad-239">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="65fad-240">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-240">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-241">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="65fad-241">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-242">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-244">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="65fad-244">The current health of the element.</span></span> <span data-ttu-id="65fad-245">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="65fad-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-247">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="65fad-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65fad-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-249">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="65fad-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="65fad-250">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="65fad-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-252">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65fad-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-254">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="65fad-254">The date and time when the object was installed.</span></span> <span data-ttu-id="65fad-255">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="65fad-255">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="65fad-256">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="65fad-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65fad-260">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="65fad-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="65fad-261">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="65fad-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="65fad-262">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-263">**С привязкой**</span><span class="sxs-lookup"><span data-stu-id="65fad-263">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-264">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65fad-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-266">Указывает, привязан ли порт Wi-Fi к сетевой архитектуре виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65fad-266">Specifies if the Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <span data-ttu-id="65fad-267">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="65fad-267">This will be one of the following values.</span></span>



| <span data-ttu-id="65fad-268">Значение</span><span class="sxs-lookup"><span data-stu-id="65fad-268">Value</span></span>                                                                                                                                                        | <span data-ttu-id="65fad-269">Значение</span><span class="sxs-lookup"><span data-stu-id="65fad-269">Meaning</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="True"></span><span id="true"></span><span id="TRUE"></span><dl> <span data-ttu-id="65fad-270"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="65fad-270"><dt>**True**</dt></span></span> </dl>     | <span data-ttu-id="65fad-271">Wi-Fi порт привязан к сетевой архитектуре виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65fad-271">The Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <br/>     |
| <span id="False"></span><span id="false"></span><span id="FALSE"></span><dl> <span data-ttu-id="65fad-272"><dt>**Неверно**</dt></span><span class="sxs-lookup"><span data-stu-id="65fad-272"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="65fad-273">Wi-Fi порт не привязан к сетевой архитектуре виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65fad-273">The Wi-Fi port is not bound to the virtual machine networking architecture.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="65fad-274">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="65fad-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-275">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="65fad-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-277">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="65fad-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="65fad-278">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-279">**линктечнологи**</span><span class="sxs-lookup"><span data-stu-id="65fad-279">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-280">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-282">Указывает тип технологии ссылок для порта.</span><span class="sxs-lookup"><span data-stu-id="65fad-282">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="65fad-283">Если задано значение 1 (другое), свойство **осерлинктечнологи** содержит строковое описание типа ссылки.</span><span class="sxs-lookup"><span data-stu-id="65fad-283">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="65fad-284">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-284">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="65fad-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="65fad-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="65fad-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="65fad-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-288"><span id="IB"></span><span id="ib"></span>**ГЕО(3** )</span><span class="sxs-lookup"><span data-stu-id="65fad-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="65fad-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="65fad-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="65fad-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="65fad-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="65fad-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Инфракрасная связь** (9)</span><span class="sxs-lookup"><span data-stu-id="65fad-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="65fad-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Беспроводная локальная сеть** (11)</span><span class="sxs-lookup"><span data-stu-id="65fad-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="65fad-297">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="65fad-297">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-298">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65fad-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-300">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="65fad-300">This property has been deprecated.</span></span> <span data-ttu-id="65fad-301">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-302">**максспид**</span><span class="sxs-lookup"><span data-stu-id="65fad-302">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-303">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65fad-303">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65fad-305">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="65fad-305">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="65fad-306">Максимальная пропускная способность порта (в битах в секунду).</span><span class="sxs-lookup"><span data-stu-id="65fad-306">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="65fad-307">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-307">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-308">**Name**</span><span class="sxs-lookup"><span data-stu-id="65fad-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-311">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="65fad-311">The label by which the object is known.</span></span> <span data-ttu-id="65fad-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-313">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="65fad-313">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-314">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="65fad-314">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65fad-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65fad-316">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="65fad-316">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="65fad-317">Массив строк, содержащих MAC-адреса для порта.</span><span class="sxs-lookup"><span data-stu-id="65fad-317">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="65fad-318">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-318">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-319">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="65fad-319">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-320">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-320">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-322">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="65fad-322">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="65fad-323">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="65fad-323">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="65fad-324">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-324">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-325">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="65fad-325">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-326">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="65fad-326">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="65fad-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-328">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="65fad-328">The current statuses of the object.</span></span> <span data-ttu-id="65fad-329">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-330">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="65fad-330">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-333">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="65fad-333">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="65fad-334">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="65fad-334">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="65fad-335">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-335">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-336">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="65fad-336">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-337">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="65fad-337">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65fad-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-339">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="65fad-339">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="65fad-340">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-341">**осерлинктечнологи**</span><span class="sxs-lookup"><span data-stu-id="65fad-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-344">Строковое значение, описывающее **линктечнологи** , если оно имеет значение 1, (другое).</span><span class="sxs-lookup"><span data-stu-id="65fad-344">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="65fad-345">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-346">**осернетворкпорттипе**</span><span class="sxs-lookup"><span data-stu-id="65fad-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-349">Использование этого свойства не рекомендуется использовать вместо свойства **portType** .</span><span class="sxs-lookup"><span data-stu-id="65fad-349">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="65fad-350">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-350">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-351">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="65fad-351">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-354">Описывает тип модуля, когда для **portType** задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="65fad-354">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="65fad-355">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-355">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-356">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="65fad-356">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-357">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65fad-359">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="65fad-359">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="65fad-360">Сетевой адрес, жестко закодированный в порт.</span><span class="sxs-lookup"><span data-stu-id="65fad-360">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="65fad-361">Этот жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="65fad-361">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="65fad-362">При внесении этого изменения поле должно быть обновлено одновременно.</span><span class="sxs-lookup"><span data-stu-id="65fad-362">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="65fad-363">Это свойство должно иметь **значение NULL** , если для сетевого адаптера не существует жестко закодированного адреса.</span><span class="sxs-lookup"><span data-stu-id="65fad-363">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="65fad-364">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-364">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-365">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="65fad-365">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-366">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-368">номер порта.</span><span class="sxs-lookup"><span data-stu-id="65fad-368">The port number.</span></span> <span data-ttu-id="65fad-369">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-369">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-370">**Порта**</span><span class="sxs-lookup"><span data-stu-id="65fad-370">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-371">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-373">Конкретный режим, который в данный момент включен для порта.</span><span class="sxs-lookup"><span data-stu-id="65fad-373">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="65fad-374">Если задано значение 1 (другое), связанное свойство **осерпорттипе** содержит строковое описание типа порта.</span><span class="sxs-lookup"><span data-stu-id="65fad-374">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="65fad-375">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-375">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="65fad-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="65fad-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="65fad-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 медный** (50)</span><span class="sxs-lookup"><span data-stu-id="65fad-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BASE** (51)</span><span class="sxs-lookup"><span data-stu-id="65fad-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BASE** (52)</span><span class="sxs-lookup"><span data-stu-id="65fad-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BASE** (53)</span><span class="sxs-lookup"><span data-stu-id="65fad-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="65fad-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="65fad-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="65fad-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 Fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="65fad-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="65fad-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="65fad-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="65fad-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="65fad-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="65fad-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="65fad-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="65fad-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="65fad-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-лв** (109)</span><span class="sxs-lookup"><span data-stu-id="65fad-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="65fad-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-ать** (111)</span><span class="sxs-lookup"><span data-stu-id="65fad-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="65fad-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="65fad-398">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="65fad-398">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-399">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="65fad-399">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="65fad-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-401">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="65fad-401">The power management capabilities of the device.</span></span> <span data-ttu-id="65fad-402">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-403">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="65fad-403">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-404">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="65fad-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-406">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="65fad-406">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="65fad-407">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-408">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="65fad-408">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-409">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65fad-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-411">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="65fad-411">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="65fad-412">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-413">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="65fad-413">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-414">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-416">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="65fad-416">Provides high level status information.</span></span> <span data-ttu-id="65fad-417">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="65fad-417">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="65fad-418">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="65fad-418">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="65fad-419">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-419">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-420">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="65fad-420">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-421">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65fad-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-422">Тип доступа: только для записи</span><span class="sxs-lookup"><span data-stu-id="65fad-422">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="65fad-423">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="65fad-423">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="65fad-424">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="65fad-424">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="65fad-425">Фактическая пропускная способность указывается в свойстве **Speed** .</span><span class="sxs-lookup"><span data-stu-id="65fad-425">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="65fad-426">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-426">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-427">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="65fad-427">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-428">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-430">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="65fad-430">The last requested or desired state for the element.</span></span> <span data-ttu-id="65fad-431">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-432">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="65fad-432">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-433">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65fad-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65fad-435">Квалификаторы: **единицы** ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="65fad-435">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="65fad-436">Пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="65fad-436">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="65fad-437">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-437">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-438">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="65fad-438">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-441">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="65fad-441">The current status of the object.</span></span> <span data-ttu-id="65fad-442">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-442">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-443">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="65fad-443">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-444">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="65fad-444">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65fad-445">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-446">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="65fad-446">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="65fad-447">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="65fad-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="65fad-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-449">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-451">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="65fad-451">The current state of the logical device.</span></span> <span data-ttu-id="65fad-452">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-453">**суппортедмаксимумтрансмиссионунит**</span><span class="sxs-lookup"><span data-stu-id="65fad-453">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-454">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65fad-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65fad-456">Квалификаторы: **единицы** ("байт")</span><span class="sxs-lookup"><span data-stu-id="65fad-456">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="65fad-457">Максимальный поддерживаемый размер блока передачи (MTU) в байтах.</span><span class="sxs-lookup"><span data-stu-id="65fad-457">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="65fad-458">Это свойство наследуется от [**CIM \_ нетворкпорт**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="65fad-458">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-459">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="65fad-459">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-460">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-461">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-462">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="65fad-462">The scoping system's creation class name.</span></span> <span data-ttu-id="65fad-463">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="65fad-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-465">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65fad-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-466">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-467">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="65fad-467">The scoping system's name.</span></span> <span data-ttu-id="65fad-468">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-468">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-469">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="65fad-469">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-470">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65fad-470">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-471">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-472">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="65fad-472">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="65fad-473">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-473">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-474">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="65fad-474">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-475">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65fad-475">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-476">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-477">Общее число часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="65fad-477">The total number of hours that this device has been powered on.</span></span> <span data-ttu-id="65fad-478">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="65fad-478">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="65fad-479">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="65fad-479">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-480">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-482">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="65fad-482">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="65fad-483">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="65fad-483">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="65fad-484">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="65fad-484">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65fad-485">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65fad-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65fad-486">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65fad-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65fad-487">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="65fad-487">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="65fad-488">В качестве примера такой ситуации можно привести массив хранения данных, который может иметь серверные порты для взаимодействия с дисками и интерфейсными портами для взаимодействия с узлами.</span><span class="sxs-lookup"><span data-stu-id="65fad-488">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="65fad-489">При отсутствии ограничений на использование порта значение должно быть равно 4 (не ограничено).</span><span class="sxs-lookup"><span data-stu-id="65fad-489">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="65fad-490">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="65fad-490">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="65fad-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="65fad-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Только внешний** интерфейс (2)</span><span class="sxs-lookup"><span data-stu-id="65fad-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Только серверная** части (3)</span><span class="sxs-lookup"><span data-stu-id="65fad-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="65fad-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Не ограничено** (4)</span><span class="sxs-lookup"><span data-stu-id="65fad-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65fad-495">Требования</span><span class="sxs-lookup"><span data-stu-id="65fad-495">Requirements</span></span>



| <span data-ttu-id="65fad-496">Требование</span><span class="sxs-lookup"><span data-stu-id="65fad-496">Requirement</span></span> | <span data-ttu-id="65fad-497">Значение</span><span class="sxs-lookup"><span data-stu-id="65fad-497">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65fad-498">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65fad-498">Minimum supported client</span></span><br/> | <span data-ttu-id="65fad-499">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="65fad-499">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="65fad-500">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65fad-500">Minimum supported server</span></span><br/> | <span data-ttu-id="65fad-501">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="65fad-501">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65fad-502">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="65fad-502">Namespace</span></span><br/>                | <span data-ttu-id="65fad-503">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="65fad-503">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="65fad-504">MOF</span><span class="sxs-lookup"><span data-stu-id="65fad-504">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65fad-505"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65fad-505"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="65fad-506">DLL</span><span class="sxs-lookup"><span data-stu-id="65fad-506">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65fad-507"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65fad-507"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

