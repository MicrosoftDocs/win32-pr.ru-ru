---
description: Представляет состояние службы пульса, которое отвечает за наблюдение за состоянием виртуальной машины с помощью регулярного сообщения о пульсе.
ms.assetid: 72DB3CD9-B083-4483-BCCD-DC8C140DDBF4
title: Класс Msvm_HeartbeatComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponent
- Msvm_HeartbeatComponent.SetPowerState
- Msvm_HeartbeatComponent.EnableDevice
- Msvm_HeartbeatComponent.OnlineDevice
- Msvm_HeartbeatComponent.QuiesceDevice
- Msvm_HeartbeatComponent.SaveProperties
- Msvm_HeartbeatComponent.RestoreProperties
- Msvm_HeartbeatComponent.InstanceID
- Msvm_HeartbeatComponent.Caption
- Msvm_HeartbeatComponent.Description
- Msvm_HeartbeatComponent.ElementName
- Msvm_HeartbeatComponent.InstallDate
- Msvm_HeartbeatComponent.Name
- Msvm_HeartbeatComponent.OperationalStatus
- Msvm_HeartbeatComponent.StatusDescriptions
- Msvm_HeartbeatComponent.Status
- Msvm_HeartbeatComponent.HealthState
- Msvm_HeartbeatComponent.CommunicationStatus
- Msvm_HeartbeatComponent.DetailedStatus
- Msvm_HeartbeatComponent.OperatingStatus
- Msvm_HeartbeatComponent.PrimaryStatus
- Msvm_HeartbeatComponent.EnabledState
- Msvm_HeartbeatComponent.OtherEnabledState
- Msvm_HeartbeatComponent.RequestedState
- Msvm_HeartbeatComponent.EnabledDefault
- Msvm_HeartbeatComponent.TimeOfLastStateChange
- Msvm_HeartbeatComponent.AvailableRequestedStates
- Msvm_HeartbeatComponent.TransitioningToState
- Msvm_HeartbeatComponent.SystemCreationClassName
- Msvm_HeartbeatComponent.SystemName
- Msvm_HeartbeatComponent.CreationClassName
- Msvm_HeartbeatComponent.DeviceID
- Msvm_HeartbeatComponent.PowerManagementSupported
- Msvm_HeartbeatComponent.PowerManagementCapabilities
- Msvm_HeartbeatComponent.Availability
- Msvm_HeartbeatComponent.StatusInfo
- Msvm_HeartbeatComponent.LastErrorCode
- Msvm_HeartbeatComponent.ErrorDescription
- Msvm_HeartbeatComponent.ErrorCleared
- Msvm_HeartbeatComponent.OtherIdentifyingInfo
- Msvm_HeartbeatComponent.PowerOnHours
- Msvm_HeartbeatComponent.TotalPowerOnHours
- Msvm_HeartbeatComponent.IdentifyingDescriptions
- Msvm_HeartbeatComponent.AdditionalAvailability
- Msvm_HeartbeatComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 61a3efaba52c2e592f405e1b95f1c62568a59229
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540330"
---
# <a name="msvm_heartbeatcomponent-class"></a><span data-ttu-id="00806-103">\_Класс мсвм хеартбеаткомпонент</span><span class="sxs-lookup"><span data-stu-id="00806-103">Msvm\_HeartbeatComponent class</span></span>

<span data-ttu-id="00806-104">Представляет состояние службы пульса, которое отвечает за наблюдение за состоянием виртуальной машины с помощью регулярного сообщения о пульсе.</span><span class="sxs-lookup"><span data-stu-id="00806-104">Represents the state of the heartbeat service, which is responsible for monitoring the state of a virtual machine by reporting a heartbeat at regular intervals.</span></span>

<span data-ttu-id="00806-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="00806-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00806-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00806-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Heartbeat";
  string   Description = "Microsoft Heartbeat Service";
  string   ElementName = "Heartbeat";
  datetime InstallDate;
  string   Name;
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_HeartbeatComponent";
  string   DeviceID = "Microsoft:VMGUID\GUID";
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
};
```

## <a name="members"></a><span data-ttu-id="00806-107">Члены</span><span class="sxs-lookup"><span data-stu-id="00806-107">Members</span></span>

<span data-ttu-id="00806-108">Класс **мсвм \_ хеартбеаткомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="00806-108">The **Msvm\_HeartbeatComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="00806-109">Методы</span><span class="sxs-lookup"><span data-stu-id="00806-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="00806-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="00806-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="00806-111">Методы</span><span class="sxs-lookup"><span data-stu-id="00806-111">Methods</span></span>

<span data-ttu-id="00806-112">Класс **мсвм \_ хеартбеаткомпонент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="00806-112">The **Msvm\_HeartbeatComponent** class has these methods.</span></span>



| <span data-ttu-id="00806-113">Метод</span><span class="sxs-lookup"><span data-stu-id="00806-113">Method</span></span>                                                                   | <span data-ttu-id="00806-114">Описание</span><span class="sxs-lookup"><span data-stu-id="00806-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="00806-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="00806-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="00806-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="00806-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="00806-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="00806-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="00806-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="00806-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="00806-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="00806-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="00806-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="00806-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="00806-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="00806-121">**RequestStateChange**</span></span>](msvm-heartbeatcomponent-requeststatechange.md) | <span data-ttu-id="00806-122">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="00806-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="00806-123">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="00806-123">**Reset**</span></span>](msvm-heartbeatcomponent-reset.md)                           | <span data-ttu-id="00806-124">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="00806-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="00806-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="00806-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="00806-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="00806-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="00806-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="00806-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="00806-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="00806-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="00806-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="00806-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="00806-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="00806-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="00806-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="00806-131">Properties</span></span>

<span data-ttu-id="00806-132">Класс **мсвм \_ хеартбеаткомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="00806-132">The **Msvm\_HeartbeatComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00806-133">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="00806-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="00806-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="00806-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-136">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="00806-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="00806-137">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="00806-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="00806-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="00806-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-141">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="00806-141">The primary availability and status of the device.</span></span> <span data-ttu-id="00806-142">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-143">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="00806-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-144">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="00806-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="00806-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-146">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="00806-146">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="00806-147">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния CIM- [**\_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00806-147">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="00806-148">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="00806-148">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="00806-149">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="00806-149">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="00806-150">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00806-150">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="00806-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="00806-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="00806-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="00806-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="00806-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="00806-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="00806-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="00806-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="00806-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="00806-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="00806-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="00806-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="00806-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="00806-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="00806-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="00806-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="00806-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="00806-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="00806-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="00806-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="00806-161">)</span><span class="sxs-lookup"><span data-stu-id="00806-161">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00806-162">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="00806-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-165">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="00806-165">A short description of the object.</span></span> <span data-ttu-id="00806-166">Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и всегда имеет значение "Пульс".</span><span class="sxs-lookup"><span data-stu-id="00806-166">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="00806-167">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="00806-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-170">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="00806-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="00806-171">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="00806-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="00806-172">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00806-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="00806-173">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="00806-173">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-176">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="00806-176">The scoping system's creation class name.</span></span> <span data-ttu-id="00806-177">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ хеартбеаткомпонент".</span><span class="sxs-lookup"><span data-stu-id="00806-177">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_HeartbeatComponent".</span></span>

</dd> <dt>

<span data-ttu-id="00806-178">**Описание**</span><span class="sxs-lookup"><span data-stu-id="00806-178">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-181">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="00806-181">A description of the object.</span></span> <span data-ttu-id="00806-182">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба пульса Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="00806-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service".</span></span>

</dd> <dt>

<span data-ttu-id="00806-183">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="00806-183">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-184">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-186">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="00806-186">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="00806-187">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="00806-187">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="00806-188">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00806-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="00806-189">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="00806-189">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-192">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="00806-192">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="00806-193">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)"унаследовано" и всегда имеет значение "Microsoft:*VMGUID* \\ *GUID*", где *VMGUID* — это свойство **Name** объекта [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , связанного с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="00806-193">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="00806-194">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="00806-194">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-197">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="00806-197">A display name for the object.</span></span> <span data-ttu-id="00806-198">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Пульс".</span><span class="sxs-lookup"><span data-stu-id="00806-198">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="00806-199">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="00806-199">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-200">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-202">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 7 (нет значения по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="00806-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>

</dd> <dt>

<span data-ttu-id="00806-203">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="00806-203">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-204">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-206">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="00806-206">The enabled and disabled states of an element.</span></span> <span data-ttu-id="00806-207">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="00806-207">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>



| <span data-ttu-id="00806-208">Значение</span><span class="sxs-lookup"><span data-stu-id="00806-208">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="00806-209">Значение</span><span class="sxs-lookup"><span data-stu-id="00806-209">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="00806-210"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="00806-210"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="00806-211">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="00806-211">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="00806-212"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="00806-212"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="00806-213">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="00806-213">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="00806-214">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="00806-214">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-215">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="00806-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00806-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-217">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="00806-217">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="00806-218">Это свойство наследуется от [**CIM \_ , но**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-219">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="00806-219">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-220">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-222">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="00806-222">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="00806-223">Это свойство наследуется от [**CIM \_ , но**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="00806-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-225">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-227">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="00806-227">The current health of the element.</span></span> <span data-ttu-id="00806-228">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="00806-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="00806-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="00806-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-230">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="00806-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="00806-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-232">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="00806-232">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="00806-233">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="00806-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-235">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="00806-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="00806-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-237">Дата и время установки службы интеграции в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="00806-237">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="00806-238">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00806-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="00806-239">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="00806-239">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00806-242">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="00806-242">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="00806-243">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="00806-243">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="00806-244">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="00806-244">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="00806-245">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="00806-245">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-246">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00806-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00806-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-248">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="00806-248">The last error code reported by the logical device.</span></span> <span data-ttu-id="00806-249">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-250">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="00806-250">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-251">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00806-251">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00806-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-253">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="00806-253">This property has been deprecated.</span></span> <span data-ttu-id="00806-254">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-255">**Name**</span><span class="sxs-lookup"><span data-stu-id="00806-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-256">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-258">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="00806-258">The label by which the object is known.</span></span> <span data-ttu-id="00806-259">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00806-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="00806-260">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="00806-260">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-261">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-263">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="00806-263">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="00806-264">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="00806-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="00806-265">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00806-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="00806-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="00806-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-267">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="00806-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="00806-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00806-269">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="00806-269">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="00806-270">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="00806-270">The current status of the element.</span></span> <span data-ttu-id="00806-271">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00806-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="00806-272">Ниже приведены возможные значения для  \[ \] значения свойства OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="00806-272">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="00806-273"><span id="OK"></span><span id="ok"></span>**ОК** (2)</span><span class="sxs-lookup"><span data-stu-id="00806-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="00806-274">Служба работает нормально.</span><span class="sxs-lookup"><span data-stu-id="00806-274">The service is operating normally.</span></span> <span data-ttu-id="00806-275"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="00806-275">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="00806-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (3)</span><span class="sxs-lookup"><span data-stu-id="00806-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd>

<span data-ttu-id="00806-277">Служба работает нормально, но Гостевая служба согласовала совместимую версию протокола связи.</span><span class="sxs-lookup"><span data-stu-id="00806-277">The service is operating normally, but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="00806-278"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="00806-278">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="00806-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (7)</span><span class="sxs-lookup"><span data-stu-id="00806-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="00806-280">Гостевая версия не поддерживает совместимую версию протокола.</span><span class="sxs-lookup"><span data-stu-id="00806-280">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="00806-281"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="00806-281">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="00806-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (12)</span><span class="sxs-lookup"><span data-stu-id="00806-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="00806-283">Гостевая служба не установлена или еще не подключена.</span><span class="sxs-lookup"><span data-stu-id="00806-283">The guest service is not installed or has not yet been contacted.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="00806-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (13)</span><span class="sxs-lookup"><span data-stu-id="00806-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="00806-285">Гостевая служба больше не отвечает в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="00806-285">The guest service is no longer responding normally.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="00806-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (15)</span><span class="sxs-lookup"><span data-stu-id="00806-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (15)</span></span>


</dt> <dd>

<span data-ttu-id="00806-287">Виртуальная машина приостановлена.</span><span class="sxs-lookup"><span data-stu-id="00806-287">The virtual machine is paused.</span></span>

</dd> </dl>

<span data-ttu-id="00806-288"> \[ Значение свойства OperationalStatus 1 \] показывает объединенные значения состояния приложения.</span><span class="sxs-lookup"><span data-stu-id="00806-288">The **OperationalStatus**\[1\] property value indicates the coalesced application state values.</span></span> <span data-ttu-id="00806-289">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="00806-289">This will be one of the following values.</span></span>

> [!Note]  
> <span data-ttu-id="00806-290">Состояние приложения задается на виртуальной машине с помощью метода [**сетаппликатионстате**](ivmapplicationhealthmonitor-setapplicationstate.md) .</span><span class="sxs-lookup"><span data-stu-id="00806-290">The state for an application is set on the virtual machine by using the [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) method.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="00806-291"><span id="OK"></span><span id="ok"></span>**ОК** (2)</span><span class="sxs-lookup"><span data-stu-id="00806-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="00806-292">Приложения, работающие в виртуальной машине, работают нормально.</span><span class="sxs-lookup"><span data-stu-id="00806-292">The applications running inside the virtual machine are operating normally.</span></span>

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="00806-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Несоответствие протоколов** (32775)</span><span class="sxs-lookup"><span data-stu-id="00806-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd>

<span data-ttu-id="00806-294">Гостевая служба и компоненты узла используют разные версии протокола.</span><span class="sxs-lookup"><span data-stu-id="00806-294">The guest and the host components are running different protocol versions.</span></span>

</dd> <dt>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>

<span data-ttu-id="00806-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Критическое состояние приложения** (32782)</span><span class="sxs-lookup"><span data-stu-id="00806-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Application Critical State** (32782)</span></span>


</dt> <dd>

<span data-ttu-id="00806-296">Одно или несколько приложений в виртуальной машине находятся в критическом состоянии.</span><span class="sxs-lookup"><span data-stu-id="00806-296">One or more of the applications inside the virtual machine are in a critical state.</span></span>

</dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="00806-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Истекло время ожидания связи** (32783)</span><span class="sxs-lookup"><span data-stu-id="00806-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

<span data-ttu-id="00806-298">Истекло время ожидания ответа от гостевого компонента.</span><span class="sxs-lookup"><span data-stu-id="00806-298">Timed out waiting for a response from the guest component.</span></span>

</dd> <dt>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>

<span data-ttu-id="00806-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Сбой связи** (32784)</span><span class="sxs-lookup"><span data-stu-id="00806-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Communication Failed** (32784)</span></span>


</dt> <dd>

<span data-ttu-id="00806-300">Не удалось связаться с гостевым компонентом.</span><span class="sxs-lookup"><span data-stu-id="00806-300">Failed to communicate with the guest component.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="00806-301">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="00806-301">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-302">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-304">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="00806-304">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="00806-305">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="00806-305">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="00806-306">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="00806-306">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="00806-307">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="00806-307">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-308">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="00806-308">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="00806-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-310">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="00806-310">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="00806-311">Это свойство наследуется от CIM с параметром и всегда имеет значение **null**. [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)</span><span class="sxs-lookup"><span data-stu-id="00806-311">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="00806-312">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="00806-312">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-313">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="00806-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="00806-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-315">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="00806-315">The power management capabilities of the device.</span></span> <span data-ttu-id="00806-316">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-317">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="00806-317">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-318">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="00806-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00806-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-320">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="00806-320">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="00806-321">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-322">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="00806-322">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-323">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00806-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00806-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-325">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="00806-325">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="00806-326">Это свойство наследуется от [**CIM \_ , но**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-327">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="00806-327">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-328">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-328">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-330">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="00806-330">Provides high level status information.</span></span> <span data-ttu-id="00806-331">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="00806-331">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="00806-332">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="00806-332">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="00806-333">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00806-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="00806-334">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="00806-334">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-335">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-337">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="00806-337">The last requested or desired state for the element.</span></span> <span data-ttu-id="00806-338">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="00806-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="00806-339">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="00806-339">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-342">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="00806-342">The current status of the object.</span></span> <span data-ttu-id="00806-343">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-344">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="00806-344">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-345">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="00806-345">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="00806-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-347">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="00806-347">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="00806-348">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="00806-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="00806-349">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="00806-349">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-350">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-350">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-352">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="00806-352">The current state of the logical device.</span></span> <span data-ttu-id="00806-353">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-354">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="00806-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-357">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="00806-357">The scoping system's creation class name.</span></span> <span data-ttu-id="00806-358">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение "мсвм \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="00806-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="00806-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="00806-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00806-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00806-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-362">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="00806-362">The scoping system's name.</span></span> <span data-ttu-id="00806-363">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -унаследованного типа и представляет собой имя [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , связанное с этой службой пульса.</span><span class="sxs-lookup"><span data-stu-id="00806-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is the name of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) that is associated with this heartbeat service.</span></span>

</dd> <dt>

<span data-ttu-id="00806-364">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="00806-364">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-365">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="00806-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="00806-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-367">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="00806-367">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="00806-368">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="00806-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="00806-369">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="00806-369">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-370">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="00806-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="00806-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-372">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="00806-372">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="00806-373">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-373">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="00806-374">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="00806-374">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00806-375">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="00806-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="00806-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00806-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00806-377">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="00806-377">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="00806-378">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="00806-378">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00806-379">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00806-379">Remarks</span></span>

<span data-ttu-id="00806-380">Доступ к классу **\_ хеартбеаткомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="00806-380">Access to the **Msvm\_HeartbeatComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="00806-381">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="00806-381">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="00806-382">Примеры</span><span class="sxs-lookup"><span data-stu-id="00806-382">Examples</span></span>

<span data-ttu-id="00806-383">Следующий пример на C# получает состояние работоспособности приложения для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="00806-383">The following C# sample obtains the application health status of a virtual machine.</span></span> <span data-ttu-id="00806-384">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="00806-384">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00806-385">Для правильной работы приведенный ниже код должен выполняться с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="00806-385">To function correctly, the following code must be run with Administrator privileges.</span></span>

 


```CSharp
private UInt16 OperationalStatusOk = 2;
private UInt16 OperationalStatusApplicationCriticalState = 32782;

/// <summary>
/// Gets the applications status in the VM.
/// </summary>
/// <param name="hostMachine">The hostname of the machine on which
/// the VM is running.</param>
/// <param name="vmName">The VM name.</param>
public
void
GetAppHealthStatus(
    string hostMachine,
    string vmName
    )
{
    ManagementScope scope = new ManagementScope(
        @"\\" + hostMachine + @"\root\virtualization\v2", null);

    ManagementObject heartBeatComponent = null;

    // Get the VM object and its heart beat component.
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
    using (ManagementObjectCollection heartBeatCollection =
        vm.GetRelated("Msvm_HeartbeatComponent", "Msvm_SystemDevice",
            null, null, null, null, false, null))
    {
        foreach (ManagementObject element in heartBeatCollection)
        {
            heartBeatComponent = element;
            break;
        }
    }

    if (heartBeatComponent == null)
    {
        Console.WriteLine("The VM is not running.");
        return;
    }

    using (heartBeatComponent)
    {
        UInt16[] operationalStatus = (UInt16[])heartBeatComponent["OperationalStatus"];
        UInt16 vmStatus = operationalStatus[0];

        if (vmStatus != OperationalStatusOk)
        {
            Console.WriteLine("The VM heartbeat status is not OK");
            return;
        }

        if (operationalStatus.Length != 2)
        {
            Console.WriteLine("The required Integration Components are not running " +
                "or not installed.");
            return;
        }

        UInt16 appStatus = operationalStatus[1];
        if (appStatus == OperationalStatusOk)
        {
            Console.WriteLine("The VM applications health status: OK");
        }
        else if (appStatus == OperationalStatusApplicationCriticalState)
        {
            Console.WriteLine("The VM applications health status: Critical");
        }
        else
        {
            throw new ManagementException("Unknown application health status");
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="00806-386">Требования</span><span class="sxs-lookup"><span data-stu-id="00806-386">Requirements</span></span>



| <span data-ttu-id="00806-387">Требование</span><span class="sxs-lookup"><span data-stu-id="00806-387">Requirement</span></span> | <span data-ttu-id="00806-388">Значение</span><span class="sxs-lookup"><span data-stu-id="00806-388">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00806-389">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00806-389">Minimum supported client</span></span><br/> | <span data-ttu-id="00806-390">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="00806-390">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="00806-391">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00806-391">Minimum supported server</span></span><br/> | <span data-ttu-id="00806-392">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="00806-392">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00806-393">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="00806-393">Namespace</span></span><br/>                | <span data-ttu-id="00806-394">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="00806-394">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="00806-395">MOF</span><span class="sxs-lookup"><span data-stu-id="00806-395">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00806-396"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00806-396"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="00806-397">DLL</span><span class="sxs-lookup"><span data-stu-id="00806-397">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00806-398"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00806-398"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="00806-399">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00806-399">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00806-400">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="00806-400">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="00806-401">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="00806-401">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> <dt>

[<span data-ttu-id="00806-402">**Мсвм \_ хеартбеаткомпонент**</span><span class="sxs-lookup"><span data-stu-id="00806-402">**Msvm\_HeartbeatComponent**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponent)
</dt> </dl>

 

