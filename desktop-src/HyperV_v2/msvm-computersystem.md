---
description: Представляет физическую систему компьютера или виртуальную машину.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Класс Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556877"
---
# <a name="msvm_computersystem-class"></a><span data-ttu-id="ac90e-103">\_Класс мсвм ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="ac90e-103">Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="ac90e-104">Представляет физическую систему компьютера или виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac90e-104">Represents a physical computer system or virtual machine.</span></span>

<span data-ttu-id="ac90e-105">Чтобы получить сведения для VMMS, используйте класс [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ac90e-105">To retrieve information for the VMMS, use the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="ac90e-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ac90e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac90e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac90e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a><span data-ttu-id="ac90e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ac90e-108">Members</span></span>

<span data-ttu-id="ac90e-109">Класс **мсвм \_ ComputerSystem** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ac90e-109">The **Msvm\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="ac90e-110">Методы</span><span class="sxs-lookup"><span data-stu-id="ac90e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ac90e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac90e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ac90e-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ac90e-112">Methods</span></span>

<span data-ttu-id="ac90e-113">Класс **мсвм \_ ComputerSystem** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ac90e-113">The **Msvm\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="ac90e-114">Метод</span><span class="sxs-lookup"><span data-stu-id="ac90e-114">Method</span></span>                                                                                         | <span data-ttu-id="ac90e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ac90e-115">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac90e-116">**инжектнонмаскаблеинтеррупт**</span><span class="sxs-lookup"><span data-stu-id="ac90e-116">**InjectNonMaskableInterrupt**</span></span>](injectnonmaskableinterrupt-msvm-computersystem.md)           | <span data-ttu-id="ac90e-117">Внедряет немаскируемое прерывание в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac90e-117">Injects a non-maskable interrupt into the virtual machine.</span></span> <span data-ttu-id="ac90e-118">Этот метод поддерживается только для экземпляров класса **\_ ComputerSystem мсвм** , представляющих виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac90e-118">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="ac90e-119">**Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ac90e-119">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                    |
| [<span data-ttu-id="ac90e-120">**рекуестрепликатионстатечанже**</span><span class="sxs-lookup"><span data-stu-id="ac90e-120">**RequestReplicationStateChange**</span></span>](msvm-computersystem-requestreplicationstatechange.md)     | <span data-ttu-id="ac90e-121">Запрашивает изменение состояния репликации виртуальной машины на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="ac90e-121">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="ac90e-122">Этот метод поддерживается только для экземпляров класса **\_ ComputerSystem мсвм** , представляющих виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac90e-122">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="ac90e-123">**рекуестрепликатионстатечанжеекс**</span><span class="sxs-lookup"><span data-stu-id="ac90e-123">**RequestReplicationStateChangeEx**</span></span>](msvm-requestreplicationstatechangeex-computersystem.md) | <span data-ttu-id="ac90e-124">Запрашивает изменение состояния репликации виртуальной машины на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="ac90e-124">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="ac90e-125">Этот метод поддерживается только для экземпляров класса **\_ ComputerSystem мсвм** , представляющих виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac90e-125">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="ac90e-126">**Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ac90e-126">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="ac90e-127">**Равен**</span><span class="sxs-lookup"><span data-stu-id="ac90e-127">**RequestStateChange**</span></span>](requeststatechange-msvm-computersystem.md)                           | <span data-ttu-id="ac90e-128">Запрашивает изменение состояния виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-128">Requests that the state of the virtual machine be changed.</span></span> <span data-ttu-id="ac90e-129">Этот метод поддерживается только для экземпляров класса **\_ ComputerSystem мсвм** , представляющих виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac90e-129">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="ac90e-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ac90e-130">**SetPowerState**</span></span>                                                                              | <span data-ttu-id="ac90e-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ac90e-131">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="ac90e-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac90e-132">Properties</span></span>

<span data-ttu-id="ac90e-133">Класс **мсвм \_ ComputerSystem** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ac90e-133">The **Msvm\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac90e-134">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="ac90e-134">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-135">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ac90e-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-137">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="ac90e-137">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="ac90e-138">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ac90e-138">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="ac90e-139">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="ac90e-139">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="ac90e-140">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="ac90e-140">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="ac90e-141">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac90e-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="ac90e-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="ac90e-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="ac90e-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="ac90e-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="ac90e-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="ac90e-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="ac90e-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="ac90e-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="ac90e-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="ac90e-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="ac90e-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="ac90e-152">)</span><span class="sxs-lookup"><span data-stu-id="ac90e-152">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac90e-153">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ac90e-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-156">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ac90e-156">A short description of the object.</span></span> <span data-ttu-id="ac90e-157">Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и будет содержать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ac90e-157">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it will contain one of the following values.</span></span>



| <span data-ttu-id="ac90e-158">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-158">Value</span></span>                                                                                                | <span data-ttu-id="ac90e-159">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-159">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="ac90e-160"><dt>"Виртуальная машина"</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-160"><dt>"Virtual Machine"</dt></span></span> </dl>         | <span data-ttu-id="ac90e-161">Экземпляр представляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac90e-161">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="ac90e-162"><dt>"Система размещения компьютера"</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-162"><dt>"Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="ac90e-163">Экземпляр представляет компьютер размещения.</span><span class="sxs-lookup"><span data-stu-id="ac90e-163">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ac90e-164">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="ac90e-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-167">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="ac90e-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ac90e-168">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ac90e-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ac90e-169">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac90e-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-170">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ac90e-170">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-173">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ac90e-173">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="ac90e-174">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="ac90e-174">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-175">**Выделенные**</span><span class="sxs-lookup"><span data-stu-id="ac90e-175">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-176">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ac90e-176">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-178">Указывает, является ли компьютерная система специальной (выделенной для конкретного использования), а не универсальной системой.</span><span class="sxs-lookup"><span data-stu-id="ac90e-178">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="ac90e-179">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение 0 (не выделено).</span><span class="sxs-lookup"><span data-stu-id="ac90e-179">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-180">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ac90e-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-183">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ac90e-183">A description of the object.</span></span> <span data-ttu-id="ac90e-184">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и будет содержать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ac90e-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it will contain one of the following values.</span></span>



| <span data-ttu-id="ac90e-185">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-185">Value</span></span>                                                                                                          | <span data-ttu-id="ac90e-186">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-186">Meaning</span></span>                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="ac90e-187"><dt>«Система виртуального компьютера Microsoft»</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-187"><dt>"Microsoft Virtual Computer System"</dt></span></span> </dl> | <span data-ttu-id="ac90e-188">Экземпляр представляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ac90e-188">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="ac90e-189"><dt>«Microsoft Hosting Computer System»</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-189"><dt>"Microsoft Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="ac90e-190">Экземпляр представляет компьютер размещения.</span><span class="sxs-lookup"><span data-stu-id="ac90e-190">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ac90e-191">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ac90e-191">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-192">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-194">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="ac90e-194">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ac90e-195">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ac90e-195">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ac90e-196">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac90e-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-197">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ac90e-197">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-200">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ac90e-200">A display name for the object.</span></span> <span data-ttu-id="ac90e-201">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда устанавливается в качестве отображаемого имени компьютера для виртуальной машины или NetBIOS-имени операционной системы управления.</span><span class="sxs-lookup"><span data-stu-id="ac90e-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to the display name of the computer for a virtual machine or the NetBIOS name of the management operating system.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-202">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="ac90e-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-203">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-205">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ac90e-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ac90e-206">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ac90e-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ac90e-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="ac90e-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="ac90e-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="ac90e-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac90e-210">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ac90e-210">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-211">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-213">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ac90e-213">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ac90e-214">Это свойство также может указывать переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="ac90e-214">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="ac90e-215">Это свойство наследуется от класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и имеет значение 2 (включено) для физического компьютера или одно из следующих значений для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-215">This property is inherited from the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class, and it is set to 2 (Enabled) for a physical computer or one of the following values for a virtual machine.</span></span> <span data-ttu-id="ac90e-216">Графическое представление этих состояний см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="ac90e-216">For a graphical view of these states, see Remarks.</span></span>



| <span data-ttu-id="ac90e-217">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-217">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="ac90e-218">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-218">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="ac90e-219"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-219"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="ac90e-220">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="ac90e-220">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="ac90e-221"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-221"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="ac90e-222"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="ac90e-223">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="ac90e-223">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="ac90e-224"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="ac90e-225">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="ac90e-225">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="ac90e-226"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-226"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="ac90e-227">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="ac90e-227">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="ac90e-228"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-228"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="ac90e-229">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="ac90e-229">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="ac90e-230"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-230"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="ac90e-231">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="ac90e-231">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="ac90e-232"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-232"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="ac90e-233">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="ac90e-233">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="ac90e-234"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-234"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="ac90e-235">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="ac90e-235">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="ac90e-236"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-236"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="ac90e-237">Элемент включен, но в режиме с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="ac90e-237">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="ac90e-238">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="ac90e-238">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="ac90e-239">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="ac90e-239">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="ac90e-240"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-240"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="ac90e-241">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="ac90e-241">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="ac90e-242">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="ac90e-242">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="ac90e-243">**енханцедсессионмодестате**</span><span class="sxs-lookup"><span data-stu-id="ac90e-243">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-244">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-246">Указывает текущее состояние режима расширенного сеанса на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ac90e-246">Specifies the current state of enhanced session mode on the virtual machine.</span></span>

<span data-ttu-id="ac90e-247">Поставщик WMI Hyper-V создает [**\_ \_ инстанцемодификатионевент**](/windows/desktop/WmiSdk/--instancemodificationevent) каждый раз при изменении **енханцедсессионмодестате** класса **\_ ComputerSystem мсвм** .</span><span class="sxs-lookup"><span data-stu-id="ac90e-247">The Hyper-V WMI provider raises an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) each time the **EnhancedSessionModeState** of the **Msvm\_ComputerSystem** class changes.</span></span> <span data-ttu-id="ac90e-248">Если активный сеанс вмконнектион получает **\_ \_ инстанцемодификатионевент**, он пытается переключиться в режим расширенного сеанса, если пользователь включил этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac90e-248">If an active vmconnection session receives an **\_\_InstanceModificationEvent**, it attempts to switch to enhanced session mode if the user enabled that setting.</span></span>

<span data-ttu-id="ac90e-249">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ac90e-249">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="ac90e-250">**Енханцедсессионмодестате** может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ac90e-250">**EnhancedSessionModeState** can be one of these values:</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="ac90e-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Разрешено и доступно** (2)</span><span class="sxs-lookup"><span data-stu-id="ac90e-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Allowed and available** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ac90e-252">Расширенный режим разрешен и доступен на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ac90e-252">Enhanced mode is allowed and available on the virtual machine.</span></span>

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="ac90e-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Не разрешено** (3)</span><span class="sxs-lookup"><span data-stu-id="ac90e-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not allowed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ac90e-254">Расширенный режим не разрешен на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ac90e-254">Enhanced mode is not allowed on the virtual machine.</span></span>

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="ac90e-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Разрешено, но недоступно** (6)</span><span class="sxs-lookup"><span data-stu-id="ac90e-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Allowed but not available** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ac90e-256">Расширенный режим разрешен и в настоящее время недоступен на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ac90e-256">Enhanced mode is allowed and but not currently available on the virtual machine.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ac90e-257">**фаиледоверрепликатионтипе**</span><span class="sxs-lookup"><span data-stu-id="ac90e-257">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-258">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-260">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Фаиледоверрепликатионтипе**")</span><span class="sxs-lookup"><span data-stu-id="ac90e-260">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-261">Тип точки данных восстановления, которая была применена во время операции отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="ac90e-261">The type of recovery data point that was applied during the failover operation.</span></span>

> [!Note]  
> <span data-ttu-id="ac90e-262">Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.</span><span class="sxs-lookup"><span data-stu-id="ac90e-262">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="ac90e-263">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ac90e-263">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ac90e-264">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="ac90e-264">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="ac90e-265">**Обычный** (1)</span><span class="sxs-lookup"><span data-stu-id="ac90e-265">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="ac90e-266">С **совместимостью приложений** (2)</span><span class="sxs-lookup"><span data-stu-id="ac90e-266">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="ac90e-267">**Запланировано** (3)</span><span class="sxs-lookup"><span data-stu-id="ac90e-267">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac90e-268">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ac90e-268">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-269">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-271">Указывает текущую работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="ac90e-271">Specifies the current health of the element.</span></span> <span data-ttu-id="ac90e-272">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="ac90e-272">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="ac90e-273">При возникновении критической ошибки просмотрите подробные сведения в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="ac90e-273">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="ac90e-274">Свойство **EnabledState** также может содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ac90e-274">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="ac90e-275">Например, если место на диске критически низкий, значение **HealthState** равно 25, виртуальная машина будет приостановлена, а параметру **EnabledState** будет присвоено значение 32768 (приостановлено).</span><span class="sxs-lookup"><span data-stu-id="ac90e-275">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="ac90e-276">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac90e-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="ac90e-277">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-277">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="ac90e-278">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-278">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="ac90e-279"><dt>**ОК**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-279"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="ac90e-280">Виртуальная машина полностью работоспособна и работает в нормальных рабочих параметрах и без ошибок.</span><span class="sxs-lookup"><span data-stu-id="ac90e-280">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="ac90e-281"><dt>**Серьезный сбой**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-281"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="ac90e-282">Произошла серьезная ошибка виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-282">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="ac90e-283">Это значение используется, когда на одном или нескольких дисках, содержащих виртуальные жесткие диски виртуальной машины, недостаточно места на диске, а виртуальная машина приостановлена.</span><span class="sxs-lookup"><span data-stu-id="ac90e-283">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="ac90e-284"><dt>**Критический сбой**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-284"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="ac90e-285">Элемент нефункциональный, и восстановление может быть невозможным.</span><span class="sxs-lookup"><span data-stu-id="ac90e-285">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="ac90e-286">Это может означать, что рабочий процесс для виртуальной машины (Vmwp.exe) не отвечает на запросы контроля или информации или что на одном или нескольких дисках, содержащих виртуальные жесткие диски виртуальной машины, недостаточно места на диске.</span><span class="sxs-lookup"><span data-stu-id="ac90e-286">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ac90e-287">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ac90e-287">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-288">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ac90e-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-290">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-290">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-291">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ac90e-291">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-292">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac90e-292">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-294">Дата и время создания конфигурации виртуальной машины для виртуальной машины или **значение NULL** для операционной системы управления.</span><span class="sxs-lookup"><span data-stu-id="ac90e-294">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="ac90e-295">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac90e-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-296">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac90e-296">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-299">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ac90e-299">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-300">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ac90e-300">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ac90e-301">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ac90e-301">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="ac90e-302">В Windows 8 существует единственный экземпляр [**репликатионсеттингдата**](msvm-replicationsettingdata.md) для каждой компьютерной системы или виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-302">In Windows 8, there is a single instance of [**ReplicationSettingData**](msvm-replicationsettingdata.md) for every computer system or virtual machine.</span></span> <span data-ttu-id="ac90e-303">Для Windows 8.1 виртуальная машина восстановления имеет два экземпляра **репликатионсеттингдата**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-303">For Windows 8.1, a recovery virtual machine has two instances of **ReplicationSettingData**.</span></span> <span data-ttu-id="ac90e-304">Это изменение отличает и связывает данные настройки с отношением репликации.</span><span class="sxs-lookup"><span data-stu-id="ac90e-304">This change differentiates and associates setting data with replication relationship.</span></span>



| <span data-ttu-id="ac90e-305">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="ac90e-305">Property name</span></span>  | <span data-ttu-id="ac90e-306">Значение Windows 8</span><span class="sxs-lookup"><span data-stu-id="ac90e-306">Windows 8 value</span></span>               | <span data-ttu-id="ac90e-307">Windows 8.1 значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-307">Windows 8.1 value</span></span>                          |
|----------------|-------------------------------|--------------------------------------------|
| <span data-ttu-id="ac90e-308">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac90e-308">**InstanceID**</span></span> | <span data-ttu-id="ac90e-309">Microsoft: <vmguid> \\ HVR</span><span class="sxs-lookup"><span data-stu-id="ac90e-309">Microsoft:<vmguid>\\HVR</span></span> | <span data-ttu-id="ac90e-310">Microsoft: <vmguid> \\ HVR \\<0/1></span><span class="sxs-lookup"><span data-stu-id="ac90e-310">Microsoft:<vmguid>\\HVR\\<0/1></span></span> |



 

<span data-ttu-id="ac90e-311">В Windows 8.1 значение 0 указывает на первичный, а 1 — на расширенную репликацию.</span><span class="sxs-lookup"><span data-stu-id="ac90e-311">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="ac90e-312">Дополнительные сведения о расширенной репликации см. в разделе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="ac90e-312">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-313">**ластаппликатионконсистентрепликатионтиме**</span><span class="sxs-lookup"><span data-stu-id="ac90e-313">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-314">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac90e-314">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-316">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Ластаппликатионконсистентрепликатионтиме**")</span><span class="sxs-lookup"><span data-stu-id="ac90e-316">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-317">Время получения последней репликации, соответствующей приложению, для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-317">The time at which the last application-consistent replication was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="ac90e-318">Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.</span><span class="sxs-lookup"><span data-stu-id="ac90e-318">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="ac90e-319">**ластрепликатионтиме**</span><span class="sxs-lookup"><span data-stu-id="ac90e-319">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-320">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac90e-320">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-322">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Ластрепликатионтиме**")</span><span class="sxs-lookup"><span data-stu-id="ac90e-322">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-323">Время, когда при восстановлении виртуальной машины получается Последняя репликация.</span><span class="sxs-lookup"><span data-stu-id="ac90e-323">The time at which the last replication is received on recovery for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="ac90e-324">Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.</span><span class="sxs-lookup"><span data-stu-id="ac90e-324">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="ac90e-325">**ластрепликатионтипе**</span><span class="sxs-lookup"><span data-stu-id="ac90e-325">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-326">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-328">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Ластрепликатионтипе**")</span><span class="sxs-lookup"><span data-stu-id="ac90e-328">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-329">Тип последней репликации, полученной для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-329">The type of the last replication that was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="ac90e-330">Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.</span><span class="sxs-lookup"><span data-stu-id="ac90e-330">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="ac90e-331">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ac90e-331">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ac90e-332">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="ac90e-332">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="ac90e-333">**Обычный** (1)</span><span class="sxs-lookup"><span data-stu-id="ac90e-333">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="ac90e-334">С **совместимостью приложений** (2)</span><span class="sxs-lookup"><span data-stu-id="ac90e-334">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="ac90e-335">**Запланировано** (3)</span><span class="sxs-lookup"><span data-stu-id="ac90e-335">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac90e-336">**ластсукцессфулбаккуптиме**</span><span class="sxs-lookup"><span data-stu-id="ac90e-336">**LastSuccessfulBackupTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-337">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac90e-337">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-339">Время, когда последняя успешная архивация была завершена для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-339">The time at which the last successful backup has completed for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-340">**Name**</span><span class="sxs-lookup"><span data-stu-id="ac90e-340">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-341">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-343">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="ac90e-343">The label by which the object is known.</span></span> <span data-ttu-id="ac90e-344">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="ac90e-344">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-345">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="ac90e-345">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-348">Строка, которая определяет, как было создано системное имя с использованием эвристики подкласса.</span><span class="sxs-lookup"><span data-stu-id="ac90e-348">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="ac90e-349">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-349">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-350">**NumberOfNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="ac90e-350">**NumberOfNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-351">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-353">Количество узлов (NUMA) неоднородным доступом системы.</span><span class="sxs-lookup"><span data-stu-id="ac90e-353">The number of nonuniform memory access (NUMA) nodes of the computer system.</span></span> <span data-ttu-id="ac90e-354">Если **мсвм \_ ComputerSystem** представляет компьютер размещения, это свойство содержит количество физических узлов NUMA.</span><span class="sxs-lookup"><span data-stu-id="ac90e-354">When **Msvm\_ComputerSystem** represents the hosting computer system, this property contains the count of physical NUMA nodes.</span></span> <span data-ttu-id="ac90e-355">Когда **мсвм \_ ComputerSystem** представляет виртуальную машину, это свойство содержит число виртуальных узлов NUMA, которые представлены в гостевой операционной системе с помощью таблицы СОПОСТАВЛЕНИЯ системных ресурсов ACPI (СРАТ).</span><span class="sxs-lookup"><span data-stu-id="ac90e-355">When **Msvm\_ComputerSystem** represents a virtual machine, this property contains the number of virtual NUMA nodes that are presented to the guest operating system through the ACPI System Resource Affinity Table (SRAT).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-356">**онтимеинмиллисекондс**</span><span class="sxs-lookup"><span data-stu-id="ac90e-356">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-357">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ac90e-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-359">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="ac90e-359">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-360">Для виртуальной машины это свойство указывает время в миллисекундах, прошедшее с момента последнего включения, сброса или восстановления компьютера.</span><span class="sxs-lookup"><span data-stu-id="ac90e-360">For the virtual machine, this property indicates the time, in milliseconds, since the machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="ac90e-361">В этот раз исключается время, в течение которого виртуальная машина находилась в приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ac90e-361">This time excludes the time the virtual machine was in the paused state.</span></span> <span data-ttu-id="ac90e-362">Для операционной системы управления это свойство имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-362">For the management operating system, this property is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-363">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="ac90e-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-364">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-366">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ac90e-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ac90e-367">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ac90e-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ac90e-368">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac90e-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ac90e-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-370">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ac90e-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-372">Массив, содержащий текущие состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="ac90e-372">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="ac90e-373">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac90e-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="ac90e-374">Значение с нулевым индексом (0) является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ac90e-374">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="ac90e-375">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-375">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="ac90e-376">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-376">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="ac90e-377"><dt>**ОК**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-377"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="ac90e-378">Виртуальная машина работоспособна и работает нормально.</span><span class="sxs-lookup"><span data-stu-id="ac90e-378">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="ac90e-379"><dt>**Снижение уровня работоспособности**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-379"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="ac90e-380">Виртуальная машина работает только частично.</span><span class="sxs-lookup"><span data-stu-id="ac90e-380">The virtual machine is only partially functional.</span></span> <span data-ttu-id="ac90e-381">Это означает, что хранилище, которое содержит конфигурацию, недоступно.</span><span class="sxs-lookup"><span data-stu-id="ac90e-381">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="ac90e-382">Виртуальную машину в этом состоянии можно отключить или удалить.</span><span class="sxs-lookup"><span data-stu-id="ac90e-382">A virtual machine in this state can only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="ac90e-383"><dt>**Прогнозный сбой**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-383"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="ac90e-384">Виртуальная машина работоспособна, но может завершиться с ошибкой в будущем.</span><span class="sxs-lookup"><span data-stu-id="ac90e-384">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="ac90e-385">Это означает, что недостаточно свободного места в хранилище, содержащем виртуальный жесткий диск виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-385">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="ac90e-386">Виртуальная машина будет приостановлена, если свободное место на диске не станет доступным.</span><span class="sxs-lookup"><span data-stu-id="ac90e-386">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="ac90e-387"><dt>**Остановлено**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-387"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="ac90e-388">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ac90e-388">This value is not supported.</span></span> <span data-ttu-id="ac90e-389">Если виртуальная машина остановлена, свойство **EnabledState** будет иметь значение 3 (отключено).</span><span class="sxs-lookup"><span data-stu-id="ac90e-389">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="ac90e-390"><dt>**В службе**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-390"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="ac90e-391">Виртуальная машина обрабатывает запрос.</span><span class="sxs-lookup"><span data-stu-id="ac90e-391">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="ac90e-392"><dt>**Неактивность**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-392"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="ac90e-393">Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ac90e-393">This value is not supported.</span></span> <span data-ttu-id="ac90e-394">Если виртуальная машина приостановлена или приостановлена, свойство **EnabledState** будет иметь значение 32769 (приостановлено) или 32768 (приостановлено).</span><span class="sxs-lookup"><span data-stu-id="ac90e-394">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="ac90e-395">Значение с индексом 1 является необязательным и содержит дополнительные сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="ac90e-395">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="ac90e-396">Клиент должен использовать первичное состояние из нулевого индекса (0), чтобы определить, может ли новый запрос выдаться виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ac90e-396">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="ac90e-397">Если значение **OperationalStatus** \[ 0 \] равно 2 (ОК), операция, указанная в **OperationalStatus** \[ 1, \] может быть прервана.</span><span class="sxs-lookup"><span data-stu-id="ac90e-397">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="ac90e-398">Значение в **OperationalStatus** \[ 1 \] имеет одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ac90e-398">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="ac90e-399">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-399">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="ac90e-400">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-400">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="ac90e-401"><dt>**Создание моментального снимка**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-401"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="ac90e-402">Моментальный снимок находится в процессе создания для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-402">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="ac90e-403"><dt>**Применение моментального снимка**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-403"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="ac90e-404">Моментальный снимок находится в процессе применения к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ac90e-404">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="ac90e-405"><dt>**Удаление моментального снимка**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-405"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="ac90e-406">Моментальный снимок находится в процессе удаления из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-406">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="ac90e-407"><dt>**Ожидание запуска**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-407"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="ac90e-408">Виртуальная машина будет запущена после истечения интервала автоматической загрузки.</span><span class="sxs-lookup"><span data-stu-id="ac90e-408">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="ac90e-409"><dt>**Слияние дисков**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-409"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="ac90e-410">Выполняется слияние виртуальных жестких дисков из ранее удаленных моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="ac90e-410">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="ac90e-411"><dt>**Экспорт виртуальной машины**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-411"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="ac90e-412">Выполняется экспорт виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-412">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="ac90e-413"><dt>**Миграция виртуальной машины**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-413"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="ac90e-414">Виртуальная машина переносится с одного физического компьютера на другой.</span><span class="sxs-lookup"><span data-stu-id="ac90e-414">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="ac90e-415">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ac90e-415">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-416">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ac90e-416">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-418">Строка, описывающая, как или почему система выделяется, когда **выделенный** массив включает значение 2 (другое).</span><span class="sxs-lookup"><span data-stu-id="ac90e-418">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="ac90e-419">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-419">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-420">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="ac90e-420">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-423">Состояние виртуальной машины (включено или отключено), если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="ac90e-423">The enabled or disabled state of the virtual machine when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ac90e-424">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="ac90e-424">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="ac90e-425">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-425">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-426">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ac90e-426">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-427">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ac90e-427">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-429">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-429">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-430">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ac90e-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-431">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ac90e-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-433">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), но не используется.</span><span class="sxs-lookup"><span data-stu-id="ac90e-433">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-434">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="ac90e-434">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-435">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-435">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-436">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-437">Строка, которая указывает, как можно достичь основного владельца системы (например, номер телефона или адрес электронной почты).</span><span class="sxs-lookup"><span data-stu-id="ac90e-437">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="ac90e-438">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-438">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-439">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="ac90e-439">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-440">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-442">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="ac90e-442">The name of the primary system owner.</span></span> <span data-ttu-id="ac90e-443">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-443">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-444">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="ac90e-444">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-445">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-445">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-447">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="ac90e-447">Provides high level status information.</span></span> <span data-ttu-id="ac90e-448">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="ac90e-448">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="ac90e-449">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ac90e-449">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ac90e-450">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac90e-450">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-451">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="ac90e-451">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-452">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac90e-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-454">Идентификатор процесса, в котором выполняется эта виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="ac90e-454">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="ac90e-455">Это значение можно использовать для уникальной идентификации экземпляра Vmwp.exe в системе, где работает виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="ac90e-455">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-456">**репликатионхеалс**</span><span class="sxs-lookup"><span data-stu-id="ac90e-456">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-457">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-459">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**Репликатионхеалс**")</span><span class="sxs-lookup"><span data-stu-id="ac90e-459">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-460">Работоспособность репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-460">The replication health for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="ac90e-461">Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.</span><span class="sxs-lookup"><span data-stu-id="ac90e-461">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="ac90e-462">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ac90e-462">Possible values are:</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ac90e-463">**Неприменимо** (0)</span><span class="sxs-lookup"><span data-stu-id="ac90e-463">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="ac90e-464">**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="ac90e-464">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ac90e-465">**Предупреждение** (2)</span><span class="sxs-lookup"><span data-stu-id="ac90e-465">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="ac90e-466">**Критическая** (3)</span><span class="sxs-lookup"><span data-stu-id="ac90e-466">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac90e-467">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="ac90e-467">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-468">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-468">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-470">Указывает режим репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-470">Specifies the replication mode for the virtual machine.</span></span> <span data-ttu-id="ac90e-471">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ac90e-471">This will be one of the following values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ac90e-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="ac90e-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="ac90e-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Основной** (1)</span><span class="sxs-lookup"><span data-stu-id="ac90e-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="ac90e-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Реплика** (2)</span><span class="sxs-lookup"><span data-stu-id="ac90e-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replica** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ac90e-475">Восстановление</span><span class="sxs-lookup"><span data-stu-id="ac90e-475">Recovery</span></span>

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="ac90e-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Тестовая реплика** (3)</span><span class="sxs-lookup"><span data-stu-id="ac90e-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Test Replica** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ac90e-477">Реплика</span><span class="sxs-lookup"><span data-stu-id="ac90e-477">Replica</span></span>

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="ac90e-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Расширенная реплика** (4)</span><span class="sxs-lookup"><span data-stu-id="ac90e-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac90e-479">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="ac90e-479">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-480">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-482">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md).**ReplicationState**")</span><span class="sxs-lookup"><span data-stu-id="ac90e-482">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-483">Состояние репликации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-483">The replication state for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="ac90e-484">Это свойство является устаревшим, начиная с Windows 8.1; Вместо этого используйте свойство с тем же именем в классе [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) , чтобы получить значение для первичной или расширенной связи.</span><span class="sxs-lookup"><span data-stu-id="ac90e-484">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="ac90e-485">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ac90e-485">Possible values are:</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ac90e-486">**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="ac90e-486">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="ac90e-487">**Готово к репликации** (1)</span><span class="sxs-lookup"><span data-stu-id="ac90e-487">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="ac90e-488">**Ожидание завершения начальной репликации** (2)</span><span class="sxs-lookup"><span data-stu-id="ac90e-488">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="ac90e-489">**Репликация** (3)</span><span class="sxs-lookup"><span data-stu-id="ac90e-489">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="ac90e-490">**Синхронизированная репликация завершена** (4)</span><span class="sxs-lookup"><span data-stu-id="ac90e-490">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="ac90e-491">**Восстановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="ac90e-491">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="ac90e-492">**Зафиксировано** (6)</span><span class="sxs-lookup"><span data-stu-id="ac90e-492">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="ac90e-493">**Приостановлено** (7)</span><span class="sxs-lookup"><span data-stu-id="ac90e-493">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="ac90e-494">**Критическая** (8)</span><span class="sxs-lookup"><span data-stu-id="ac90e-494">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="ac90e-495">**Ожидание запуска повторной синхронизации** (9)</span><span class="sxs-lookup"><span data-stu-id="ac90e-495">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="ac90e-496">Повторная **Синхронизация** (10)</span><span class="sxs-lookup"><span data-stu-id="ac90e-496">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="ac90e-497">**Повторная синхронизация приостановлена** (11)</span><span class="sxs-lookup"><span data-stu-id="ac90e-497">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="ac90e-498">**Выполняется отработка отказа** (12)</span><span class="sxs-lookup"><span data-stu-id="ac90e-498">**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="ac90e-499">**Выполняется восстановление размещения** (13)</span><span class="sxs-lookup"><span data-stu-id="ac90e-499">**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="ac90e-500">**Восстановление размещения завершено** (14)</span><span class="sxs-lookup"><span data-stu-id="ac90e-500">**Failback complete** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac90e-501">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ac90e-501">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-502">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-503">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-504">Последнее запрошенное или требуемое состояние виртуальной машины, переданное методу [**RequestStateChange**](requeststatechange-msvm-computersystem.md) , или 12 (неприменимо), если изменение состояния не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac90e-504">The last requested or desired state for the virtual machine as passed to the [**RequestStateChange**](requeststatechange-msvm-computersystem.md) method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="ac90e-505">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-505">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="ac90e-506">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="ac90e-506">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="ac90e-507">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac90e-507">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-508">**ресеткапабилити**</span><span class="sxs-lookup"><span data-stu-id="ac90e-508">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-509">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-510">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-511">Это свойство наследуется от [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)и всегда имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="ac90e-511">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-512">**Роли**</span><span class="sxs-lookup"><span data-stu-id="ac90e-512">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-513">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ac90e-513">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-514">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-515">Массив строк, описывающих роли, которые система играет в среде информационных технологий.</span><span class="sxs-lookup"><span data-stu-id="ac90e-515">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="ac90e-516">Это свойство наследуется [**от \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ac90e-516">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-517">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ac90e-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-518">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac90e-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-520">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="ac90e-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-521">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="ac90e-521">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-522">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ac90e-522">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-523">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-524">Квалификаторы: **arrayType** ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="ac90e-524">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-525">Массив, содержащий строки, описывающие соответствующие значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ac90e-525">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="ac90e-526">Например, если 11 (в службе) — значение, назначенное для **OperationalStatus** \[ 0 \] , то **статусдескриптионс** \[ 0 \] может содержать объяснение, почему виртуальная машина обрабатывает запрос.</span><span class="sxs-lookup"><span data-stu-id="ac90e-526">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="ac90e-527">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ac90e-527">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-528">**тимеофластконфигуратиончанже**</span><span class="sxs-lookup"><span data-stu-id="ac90e-528">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-529">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac90e-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-530">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-531">Дата и время последнего изменения файла конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac90e-531">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="ac90e-532">Файл конфигурации изменяется во время определенных операций виртуальной машины, а также при добавлении, изменении или удалении любой из параметров виртуальной машины или устройства.</span><span class="sxs-lookup"><span data-stu-id="ac90e-532">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-533">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="ac90e-533">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-534">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac90e-534">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-535">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-536">Дата и время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ac90e-536">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ac90e-537">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac90e-537">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ac90e-538">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="ac90e-538">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac90e-539">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac90e-539">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac90e-540">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac90e-540">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac90e-541">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="ac90e-541">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ac90e-542">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="ac90e-542">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac90e-543">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac90e-543">Remarks</span></span>

<span data-ttu-id="ac90e-544">На следующем рисунке показаны значения **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ac90e-544">The following illustration shows the **EnabledState** values.</span></span>

![Схема состояний для значений enabledstate для Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

<span data-ttu-id="ac90e-546">При изменении свойства класса **\_ ComputerSystem мсвм** поставщик WMI указывает на событие [**\_ \_ инстанцемодификатионевент**](/windows/desktop/WmiSdk/--instancemodificationevent) , описывающее изменения.</span><span class="sxs-lookup"><span data-stu-id="ac90e-546">When a property of the **Msvm\_ComputerSystem** class changes, the WMI provider indicates an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) event that describes the changes.</span></span> <span data-ttu-id="ac90e-547">Предыдущее состояние содержится в свойстве **PreviousInstance** , а новое состояние содержится в свойстве **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="ac90e-547">The previous state is contained in the **PreviousInstance** property, and the new state is contained in the **TargetInstance** property.</span></span> <span data-ttu-id="ac90e-548">Это событие является асинхронным; к моменту обработки события **\_ \_ инстанцемодификатионевент** свойство **TargetInstance** может не отражать текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="ac90e-548">This event is asynchronous; by the time the **\_\_InstanceModificationEvent** event is processed, the **TargetInstance** property may not reflect the current state.</span></span>

<span data-ttu-id="ac90e-549">Доступ к классу **\_ ComputerSystem мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="ac90e-549">Access to the **Msvm\_ComputerSystem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ac90e-550">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ac90e-550">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ac90e-551">Примеры</span><span class="sxs-lookup"><span data-stu-id="ac90e-551">Examples</span></span>

<span data-ttu-id="ac90e-552">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ac90e-552">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac90e-553">Требования</span><span class="sxs-lookup"><span data-stu-id="ac90e-553">Requirements</span></span>



| <span data-ttu-id="ac90e-554">Требование</span><span class="sxs-lookup"><span data-stu-id="ac90e-554">Requirement</span></span> | <span data-ttu-id="ac90e-555">Значение</span><span class="sxs-lookup"><span data-stu-id="ac90e-555">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac90e-556">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac90e-556">Minimum supported client</span></span><br/> | <span data-ttu-id="ac90e-557">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ac90e-557">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ac90e-558">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac90e-558">Minimum supported server</span></span><br/> | <span data-ttu-id="ac90e-559">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ac90e-559">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac90e-560">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac90e-560">Namespace</span></span><br/>                | <span data-ttu-id="ac90e-561">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ac90e-561">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ac90e-562">MOF</span><span class="sxs-lookup"><span data-stu-id="ac90e-562">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac90e-563"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-563"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac90e-564">DLL</span><span class="sxs-lookup"><span data-stu-id="ac90e-564">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac90e-565"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac90e-565"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac90e-566">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac90e-566">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac90e-567">**CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="ac90e-567">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="ac90e-568">**\_\_инстанцемодификатионевент**</span><span class="sxs-lookup"><span data-stu-id="ac90e-568">**\_\_InstanceModificationEvent**</span></span>](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[<span data-ttu-id="ac90e-569">**CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="ac90e-569">**CIM\_ComputerSystem**</span></span>](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[<span data-ttu-id="ac90e-570">**Мсвм \_ ComputerSystem (v1)**</span><span class="sxs-lookup"><span data-stu-id="ac90e-570">**Msvm\_ComputerSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[<span data-ttu-id="ac90e-571">Классы виртуальных систем</span><span class="sxs-lookup"><span data-stu-id="ac90e-571">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

