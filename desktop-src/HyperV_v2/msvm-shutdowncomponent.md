---
description: Представляет состояние службы завершения работы, которое предоставляет механизм для завершения работы операционной системы виртуальной машины из интерфейсов управления в системе узла.
ms.assetid: E9BBB08C-A3FE-4226-A2CF-458706E759D6
title: Класс Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent
- Msvm_ShutdownComponent.EnableDevice
- Msvm_ShutdownComponent.OnlineDevice
- Msvm_ShutdownComponent.QuiesceDevice
- Msvm_ShutdownComponent.RestoreProperties
- Msvm_ShutdownComponent.SaveProperties
- Msvm_ShutdownComponent.SetPowerState
- Msvm_ShutdownComponent.InstanceID
- Msvm_ShutdownComponent.Caption
- Msvm_ShutdownComponent.Description
- Msvm_ShutdownComponent.ElementName
- Msvm_ShutdownComponent.InstallDate
- Msvm_ShutdownComponent.Name
- Msvm_ShutdownComponent.OperationalStatus
- Msvm_ShutdownComponent.StatusDescriptions
- Msvm_ShutdownComponent.Status
- Msvm_ShutdownComponent.HealthState
- Msvm_ShutdownComponent.CommunicationStatus
- Msvm_ShutdownComponent.DetailedStatus
- Msvm_ShutdownComponent.OperatingStatus
- Msvm_ShutdownComponent.PrimaryStatus
- Msvm_ShutdownComponent.EnabledState
- Msvm_ShutdownComponent.OtherEnabledState
- Msvm_ShutdownComponent.RequestedState
- Msvm_ShutdownComponent.EnabledDefault
- Msvm_ShutdownComponent.TimeOfLastStateChange
- Msvm_ShutdownComponent.AvailableRequestedStates
- Msvm_ShutdownComponent.TransitioningToState
- Msvm_ShutdownComponent.SystemCreationClassName
- Msvm_ShutdownComponent.SystemName
- Msvm_ShutdownComponent.CreationClassName
- Msvm_ShutdownComponent.DeviceID
- Msvm_ShutdownComponent.PowerManagementSupported
- Msvm_ShutdownComponent.PowerManagementCapabilities
- Msvm_ShutdownComponent.Availability
- Msvm_ShutdownComponent.StatusInfo
- Msvm_ShutdownComponent.LastErrorCode
- Msvm_ShutdownComponent.ErrorDescription
- Msvm_ShutdownComponent.ErrorCleared
- Msvm_ShutdownComponent.OtherIdentifyingInfo
- Msvm_ShutdownComponent.PowerOnHours
- Msvm_ShutdownComponent.TotalPowerOnHours
- Msvm_ShutdownComponent.IdentifyingDescriptions
- Msvm_ShutdownComponent.AdditionalAvailability
- Msvm_ShutdownComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 49729568a1625b3df723b1b5b88cc1044b41e715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080478"
---
# <a name="msvm_shutdowncomponent-class"></a><span data-ttu-id="a9b1d-103">\_Класс мсвм шутдовнкомпонент</span><span class="sxs-lookup"><span data-stu-id="a9b1d-103">Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="a9b1d-104">Представляет состояние службы завершения работы, которое предоставляет механизм для завершения работы операционной системы виртуальной машины из интерфейсов управления в системе узла.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-104">Represents the state of the shutdown service, which provides a mechanism to shut down the operating system of the virtual machine from the management interfaces on the host system.</span></span>

<span data-ttu-id="a9b1d-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b1d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9b1d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Shutdown";
  string   Description = "Microsoft Shutdown Service";
  string   ElementName = "Shutdown";
  datetime InstallDate;
  string   Name = "Shutdown";
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_ShutdownComponent";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
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

## <a name="members"></a><span data-ttu-id="a9b1d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a9b1d-107">Members</span></span>

<span data-ttu-id="a9b1d-108">Класс **мсвм \_ шутдовнкомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a9b1d-108">The **Msvm\_ShutdownComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a9b1d-109">Методы</span><span class="sxs-lookup"><span data-stu-id="a9b1d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a9b1d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a9b1d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a9b1d-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a9b1d-111">Methods</span></span>

<span data-ttu-id="a9b1d-112">Класс **мсвм \_ шутдовнкомпонент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-112">The **Msvm\_ShutdownComponent** class has these methods.</span></span>



| <span data-ttu-id="a9b1d-113">Метод</span><span class="sxs-lookup"><span data-stu-id="a9b1d-113">Method</span></span>                                                                  | <span data-ttu-id="a9b1d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a9b1d-114">Description</span></span>                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b1d-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="a9b1d-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-116">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="a9b1d-117">**инитиатеребут**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-117">**InitiateReboot**</span></span>](msvm-shutdowncomponent-initiatereboot.md)         | <span data-ttu-id="a9b1d-118">Инициирует операцию перезагрузки операционной системы для связанной дочерней виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-118">Initiates an operating system reboot operation on the associated child virtual machine.</span></span><br/> |
| [<span data-ttu-id="a9b1d-119">**инитиатешутдовн**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-119">**InitiateShutdown**</span></span>](msvm-shutdowncomponent-initiateshutdown.md)     | <span data-ttu-id="a9b1d-120">Инициирует операцию завершения работы операционной системы на связанной дочерней виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-120">Initiates an operating system shutdown operation on associated child virtual machine.</span></span><br/>   |
| <span data-ttu-id="a9b1d-121">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-121">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="a9b1d-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-122">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="a9b1d-123">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-123">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="a9b1d-124">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-124">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="a9b1d-125">**Равен**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-125">**RequestStateChange**</span></span>](msvm-shutdowncomponent-requeststatechange.md) | <span data-ttu-id="a9b1d-126">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-126">Requests a state change.</span></span><br/>                                                                |
| [<span data-ttu-id="a9b1d-127">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-127">**Reset**</span></span>](msvm-shutdowncomponent-reset.md)                           | <span data-ttu-id="a9b1d-128">Сбрасывает компонент.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-128">Resets the component.</span></span><br/>                                                                   |
| <span data-ttu-id="a9b1d-129">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-129">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="a9b1d-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-130">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="a9b1d-131">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-131">**SaveProperties**</span></span>                                                      | <span data-ttu-id="a9b1d-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-132">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="a9b1d-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-133">**SetPowerState**</span></span>                                                       | <span data-ttu-id="a9b1d-134">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-134">This method is not supported.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="a9b1d-135">Свойства</span><span class="sxs-lookup"><span data-stu-id="a9b1d-135">Properties</span></span>

<span data-ttu-id="a9b1d-136">Класс **мсвм \_ шутдовнкомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-136">The **Msvm\_ShutdownComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9b1d-137">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-138">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a9b1d-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-140">Дополнительные доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-140">Additional availability and status of the device.</span></span> <span data-ttu-id="a9b1d-141">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="a9b1d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-142">Value</span></span>                                                                        | <span data-ttu-id="a9b1d-143">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-143">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a9b1d-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-144"><dt>6</dt></span></span> </dl> | <span data-ttu-id="a9b1d-145">Не применимо</span><span class="sxs-lookup"><span data-stu-id="a9b1d-145">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9b1d-146">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-147">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-149">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-149">The primary availability and status of the device.</span></span> <span data-ttu-id="a9b1d-150">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-150">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>



| <span data-ttu-id="a9b1d-151">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-151">Value</span></span>                                                                        | <span data-ttu-id="a9b1d-152">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-152">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a9b1d-153"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-153"><dt>6</dt></span></span> </dl> | <span data-ttu-id="a9b1d-154">Не применимо</span><span class="sxs-lookup"><span data-stu-id="a9b1d-154">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9b1d-155">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-156">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a9b1d-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-158">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a9b1d-158">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a9b1d-159">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-160">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-163">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-163">A short description of the object.</span></span> <span data-ttu-id="a9b1d-164">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-165">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-166">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-168">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a9b1d-169">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9b1d-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a9b1d-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a9b1d-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a9b1d-178">)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a9b1d-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-182">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-182">The scoping system's creation class name.</span></span> <span data-ttu-id="a9b1d-183">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-183">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-184">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-187">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-187">A description of the object.</span></span> <span data-ttu-id="a9b1d-188">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-190">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-192">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a9b1d-193">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9b1d-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a9b1d-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a9b1d-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a9b1d-203">)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a9b1d-204">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-204">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-207">Адрес или другие идентифицирующие сведения для уникального имени объекта.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-207">An address or other identifying information to uniquely name the LogicalDevice.</span></span> <span data-ttu-id="a9b1d-208">Это свойство наследуется от CIM-класса и всегда имеет значение "Microsoft:*VMGUID* [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) \\ *GUID*", где *VMGUID* — свойство **Name** экземпляра [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , связанного с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-209">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-209">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-212">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-212">A display name for the object.</span></span> <span data-ttu-id="a9b1d-213">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-213">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-214">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-214">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-215">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-217">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-217">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a9b1d-218">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-218">Value</span></span>                                                                        | <span data-ttu-id="a9b1d-219">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-219">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="a9b1d-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-220"><dt>7</dt></span></span> </dl> | <span data-ttu-id="a9b1d-221">Нет значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a9b1d-221">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9b1d-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-223">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-225">Включенное состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-225">The enabled state of the element.</span></span> <span data-ttu-id="a9b1d-226">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и либо равно 2 (включено), либо 3 (отключено).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-226">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="a9b1d-227">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-227">Value</span></span>                                                                        | <span data-ttu-id="a9b1d-228">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-228">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="a9b1d-229"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-229"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a9b1d-230">Активировано</span><span class="sxs-lookup"><span data-stu-id="a9b1d-230">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="a9b1d-231"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-231"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a9b1d-232">Выключено</span><span class="sxs-lookup"><span data-stu-id="a9b1d-232">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9b1d-233">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-233">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-234">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-236">Указывает, что сообщение об ошибке в свойстве **ластерроркоде** теперь отключено.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-236">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="a9b1d-237">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-238">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-238">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-239">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-241">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-241">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="a9b1d-242">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-243">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-243">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-244">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-246">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-246">The current health of the element.</span></span> <span data-ttu-id="a9b1d-247">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-247">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a9b1d-248">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-249">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-249">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-250">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-250">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-252">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="a9b1d-252">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="a9b1d-253">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-254">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-254">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-255">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-255">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-257">Дата и время установки службы интеграции в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-257">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="a9b1d-258">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-259">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-259">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-260">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-262">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-262">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-263">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-263">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a9b1d-264">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-264">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-265">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-265">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-266">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-268">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-268">The last error code reported by the logical device.</span></span> <span data-ttu-id="a9b1d-269">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-269">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-270">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-270">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-271">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-273">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-273">This property has been deprecated.</span></span> <span data-ttu-id="a9b1d-274">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-275">**Name**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-275">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-278">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-278">The label by which the object is known.</span></span> <span data-ttu-id="a9b1d-279">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-280">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-280">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-281">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-283">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a9b1d-283">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a9b1d-284">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9b1d-285">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a9b1d-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a9b1d-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a9b1d-305">)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-305">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a9b1d-306">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-306">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-307">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a9b1d-307">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-309">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-309">The current status of the element.</span></span> <span data-ttu-id="a9b1d-310">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="a9b1d-311">Ниже приведены возможные значения для  \[ \] значения свойства OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-311">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="a9b1d-312">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-312">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="a9b1d-313">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-313">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="a9b1d-314"><dt>**ОК**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-314"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="a9b1d-315">Служба работает нормально.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-315">The service is operating normally.</span></span> <span data-ttu-id="a9b1d-316"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="a9b1d-317"><dt>**Снижение уровня работоспособности**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-317"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="a9b1d-318">Служба работает нормально, но Гостевая служба согласовала совместимую версию протокола связи.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-318">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="a9b1d-319"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="a9b1d-320"><dt>**Неустранимая ошибка**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-320"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="a9b1d-321">Гостевая версия не поддерживает совместимую версию протокола.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-321">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="a9b1d-322"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="a9b1d-323"><dt>**Нет контакта**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-323"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="a9b1d-324">Гостевая служба не установлена или еще не подключена.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-324">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="a9b1d-325"><dt>**Потеря связи**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-325"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="a9b1d-326">Гостевая служба больше не отвечает в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-326">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="a9b1d-327">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-327">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-330">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-330">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a9b1d-331">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-331">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="a9b1d-332">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-333">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-333">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-334">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-334">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-336">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-336">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="a9b1d-337">Это свойство наследуется от CIM с параметром и всегда имеет значение **null**. [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-337">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-338">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-339">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a9b1d-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-341">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-341">The power management capabilities of the device.</span></span> <span data-ttu-id="a9b1d-342">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-342">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-343">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-344">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-346">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-346">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="a9b1d-347">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-347">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-348">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-348">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-349">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-349">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-351">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-351">The number of consecutive hours that this Device has been powered on since its last power cycle.</span></span> <span data-ttu-id="a9b1d-352">Это свойство наследуется от [**CIM \_ , но**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-353">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-354">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-356">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-356">Provides high level status information.</span></span> <span data-ttu-id="a9b1d-357">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a9b1d-358">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a9b1d-359">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a9b1d-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-361"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a9b1d-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a9b1d-366">)</span><span class="sxs-lookup"><span data-stu-id="a9b1d-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a9b1d-367">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-367">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-368">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-370">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-370">The last requested or desired state for the element.</span></span> <span data-ttu-id="a9b1d-371">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-371">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="a9b1d-372">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-372">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="a9b1d-373">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="a9b1d-374">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-374">Value</span></span>                                                                         | <span data-ttu-id="a9b1d-375">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a9b1d-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a9b1d-377">Не применимо</span><span class="sxs-lookup"><span data-stu-id="a9b1d-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9b1d-378">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-381">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-381">The current status of the object.</span></span> <span data-ttu-id="a9b1d-382">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-383">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-384">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-386">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a9b1d-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a9b1d-387">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-389">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-391">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-391">The current state of the logical device.</span></span> <span data-ttu-id="a9b1d-392">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-393">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-394">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-396">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-396">The scoping system's creation class name.</span></span> <span data-ttu-id="a9b1d-397">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-399">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-401">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-401">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="a9b1d-402">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-403">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-404">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-406">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a9b1d-407">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-408">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-409">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-411">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="a9b1d-412">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9b1d-413">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9b1d-414">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9b1d-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9b1d-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9b1d-416">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a9b1d-417">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9b1d-418">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9b1d-418">Remarks</span></span>

<span data-ttu-id="a9b1d-419">Доступ к классу **\_ шутдовнкомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="a9b1d-419">Access to the **Msvm\_ShutdownComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a9b1d-420">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a9b1d-420">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b1d-421">Требования</span><span class="sxs-lookup"><span data-stu-id="a9b1d-421">Requirements</span></span>



| <span data-ttu-id="a9b1d-422">Требование</span><span class="sxs-lookup"><span data-stu-id="a9b1d-422">Requirement</span></span> | <span data-ttu-id="a9b1d-423">Значение</span><span class="sxs-lookup"><span data-stu-id="a9b1d-423">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b1d-424">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9b1d-424">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b1d-425">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a9b1d-425">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a9b1d-426">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9b1d-426">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b1d-427">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a9b1d-427">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9b1d-428">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a9b1d-428">Namespace</span></span><br/>                | <span data-ttu-id="a9b1d-429">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a9b1d-429">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a9b1d-430">MOF</span><span class="sxs-lookup"><span data-stu-id="a9b1d-430">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9b1d-431"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-431"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9b1d-432">DLL</span><span class="sxs-lookup"><span data-stu-id="a9b1d-432">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9b1d-433"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9b1d-433"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9b1d-434">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9b1d-434">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b1d-435">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-435">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="a9b1d-436">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="a9b1d-436">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

