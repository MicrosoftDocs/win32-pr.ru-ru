---
description: Представляет состояние службы синхронизации времени, которое отвечает за синхронизацию системного времени виртуальной машины с системным временем операционной системы, работающей в операционной системе управления.
ms.assetid: 551A81E9-E924-4A9C-965D-02FF25EE4A49
title: Класс Msvm_TimeSyncComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponent
- Msvm_TimeSyncComponent.SetPowerState
- Msvm_TimeSyncComponent.EnableDevice
- Msvm_TimeSyncComponent.OnlineDevice
- Msvm_TimeSyncComponent.QuiesceDevice
- Msvm_TimeSyncComponent.SaveProperties
- Msvm_TimeSyncComponent.RestoreProperties
- Msvm_TimeSyncComponent.InstanceID
- Msvm_TimeSyncComponent.Caption
- Msvm_TimeSyncComponent.Description
- Msvm_TimeSyncComponent.ElementName
- Msvm_TimeSyncComponent.InstallDate
- Msvm_TimeSyncComponent.Name
- Msvm_TimeSyncComponent.OperationalStatus
- Msvm_TimeSyncComponent.StatusDescriptions
- Msvm_TimeSyncComponent.Status
- Msvm_TimeSyncComponent.HealthState
- Msvm_TimeSyncComponent.CommunicationStatus
- Msvm_TimeSyncComponent.DetailedStatus
- Msvm_TimeSyncComponent.OperatingStatus
- Msvm_TimeSyncComponent.PrimaryStatus
- Msvm_TimeSyncComponent.EnabledState
- Msvm_TimeSyncComponent.OtherEnabledState
- Msvm_TimeSyncComponent.RequestedState
- Msvm_TimeSyncComponent.EnabledDefault
- Msvm_TimeSyncComponent.TimeOfLastStateChange
- Msvm_TimeSyncComponent.AvailableRequestedStates
- Msvm_TimeSyncComponent.TransitioningToState
- Msvm_TimeSyncComponent.SystemCreationClassName
- Msvm_TimeSyncComponent.SystemName
- Msvm_TimeSyncComponent.CreationClassName
- Msvm_TimeSyncComponent.DeviceID
- Msvm_TimeSyncComponent.PowerManagementSupported
- Msvm_TimeSyncComponent.PowerManagementCapabilities
- Msvm_TimeSyncComponent.Availability
- Msvm_TimeSyncComponent.StatusInfo
- Msvm_TimeSyncComponent.LastErrorCode
- Msvm_TimeSyncComponent.ErrorDescription
- Msvm_TimeSyncComponent.ErrorCleared
- Msvm_TimeSyncComponent.OtherIdentifyingInfo
- Msvm_TimeSyncComponent.PowerOnHours
- Msvm_TimeSyncComponent.TotalPowerOnHours
- Msvm_TimeSyncComponent.IdentifyingDescriptions
- Msvm_TimeSyncComponent.AdditionalAvailability
- Msvm_TimeSyncComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea9a33d665a315861d9e6c51fd529f10f07b4aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683020"
---
# <a name="msvm_timesynccomponent-class"></a><span data-ttu-id="3842e-103">\_Класс мсвм тимесинккомпонент</span><span class="sxs-lookup"><span data-stu-id="3842e-103">Msvm\_TimeSyncComponent class</span></span>

<span data-ttu-id="3842e-104">Представляет состояние службы синхронизации времени, которое отвечает за синхронизацию системного времени виртуальной машины с системным временем операционной системы, работающей в операционной системе управления.</span><span class="sxs-lookup"><span data-stu-id="3842e-104">Represents the state of the time synchronization service, which is responsible for synchronizing the system time of a virtual machine with the system time of the operating system running in the management operating system.</span></span>

<span data-ttu-id="3842e-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3842e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3842e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3842e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Time Synchronization";
  string   Description = "Microsoft Time Synchronization Service";
  string   ElementName = "Time Synchronization";
  datetime InstallDate;
  string   Name = "Time Synchronization";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {"OK"};
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TimeSyncComponent";
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
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="3842e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="3842e-107">Members</span></span>

<span data-ttu-id="3842e-108">Класс **мсвм \_ тимесинккомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3842e-108">The **Msvm\_TimeSyncComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="3842e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="3842e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3842e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3842e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3842e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="3842e-111">Methods</span></span>

<span data-ttu-id="3842e-112">Класс **мсвм \_ тимесинккомпонент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3842e-112">The **Msvm\_TimeSyncComponent** class has these methods.</span></span>



| <span data-ttu-id="3842e-113">Метод</span><span class="sxs-lookup"><span data-stu-id="3842e-113">Method</span></span>                                                                  | <span data-ttu-id="3842e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3842e-114">Description</span></span>                              |
|:------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="3842e-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="3842e-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="3842e-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3842e-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3842e-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="3842e-117">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="3842e-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3842e-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3842e-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="3842e-119">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="3842e-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3842e-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="3842e-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="3842e-121">**RequestStateChange**</span></span>](msvm-timesynccomponent-requeststatechange.md) | <span data-ttu-id="3842e-122">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="3842e-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="3842e-123">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="3842e-123">**Reset**</span></span>](msvm-timesynccomponent-reset.md)                           | <span data-ttu-id="3842e-124">Сбрасывает компонент.</span><span class="sxs-lookup"><span data-stu-id="3842e-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="3842e-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="3842e-125">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="3842e-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3842e-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3842e-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="3842e-127">**SaveProperties**</span></span>                                                      | <span data-ttu-id="3842e-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3842e-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3842e-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3842e-129">**SetPowerState**</span></span>                                                       | <span data-ttu-id="3842e-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3842e-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3842e-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="3842e-131">Properties</span></span>

<span data-ttu-id="3842e-132">Класс **мсвм \_ тимесинккомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3842e-132">The **Msvm\_TimeSyncComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3842e-133">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="3842e-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3842e-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3842e-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-136">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="3842e-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="3842e-137">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="3842e-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="3842e-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-141">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="3842e-141">The primary availability and status of the device.</span></span> <span data-ttu-id="3842e-142">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3842e-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="3842e-143">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-143">Value</span></span>                                                                        | <span data-ttu-id="3842e-144">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3842e-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="3842e-146">Не применимо</span><span class="sxs-lookup"><span data-stu-id="3842e-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3842e-147">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="3842e-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-148">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3842e-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3842e-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-150">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="3842e-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="3842e-151">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3842e-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-152">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3842e-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-155">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3842e-155">A short description of the object.</span></span> <span data-ttu-id="3842e-156">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-157">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="3842e-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-158">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-160">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="3842e-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3842e-161">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="3842e-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3842e-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3842e-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3842e-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="3842e-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="3842e-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="3842e-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="3842e-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3842e-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3842e-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3842e-170">)</span><span class="sxs-lookup"><span data-stu-id="3842e-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3842e-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3842e-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-174">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="3842e-174">The scoping system's creation class name.</span></span> <span data-ttu-id="3842e-175">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3842e-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-176">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3842e-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-179">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3842e-179">A description of the object.</span></span> <span data-ttu-id="3842e-180">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3842e-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-182">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-184">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="3842e-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3842e-185">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="3842e-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3842e-186">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3842e-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="3842e-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="3842e-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="3842e-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="3842e-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="3842e-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="3842e-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3842e-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3842e-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3842e-195">)</span><span class="sxs-lookup"><span data-stu-id="3842e-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3842e-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3842e-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-199">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="3842e-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="3842e-200">Это свойство наследуется от CIM-класса и всегда имеет значение "Microsoft:*VMGUID* [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) \\ *GUID*", где *VMGUID* — свойство **Name** экземпляра [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , связанного с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="3842e-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3842e-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-204">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="3842e-204">A display name for the object.</span></span> <span data-ttu-id="3842e-205">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-206">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="3842e-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-207">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-209">Конфигурация по умолчанию или запуск администратора для элемента **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3842e-209">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="3842e-210">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3842e-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3842e-211">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-211">Value</span></span>                                                                        | <span data-ttu-id="3842e-212">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-212">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="3842e-213"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-213"><dt>7</dt></span></span> </dl> | <span data-ttu-id="3842e-214">Нет значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3842e-214">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3842e-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3842e-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-216">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-218">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="3842e-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3842e-219">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и либо равно 2 (включено), либо 3 (отключено).</span><span class="sxs-lookup"><span data-stu-id="3842e-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="3842e-220">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-220">Value</span></span>                                                                        | <span data-ttu-id="3842e-221">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-221">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="3842e-222"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-222"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3842e-223">Активировано</span><span class="sxs-lookup"><span data-stu-id="3842e-223">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="3842e-224"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-224"><dt>3</dt></span></span> </dl> | <span data-ttu-id="3842e-225">Выключено</span><span class="sxs-lookup"><span data-stu-id="3842e-225">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3842e-226">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="3842e-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-227">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3842e-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-229">Указывает, что сообщение об ошибке в свойстве **ластерроркоде** теперь отключено.</span><span class="sxs-lookup"><span data-stu-id="3842e-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="3842e-230">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3842e-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-234">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="3842e-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="3842e-235">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-236">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3842e-236">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-237">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-239">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="3842e-239">The current health of the element.</span></span> <span data-ttu-id="3842e-240">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="3842e-241">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-241">Value</span></span>                                                                        | <span data-ttu-id="3842e-242">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-242">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="3842e-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-243"><dt>5</dt></span></span> </dl> | <span data-ttu-id="3842e-244">ОК</span><span class="sxs-lookup"><span data-stu-id="3842e-244">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3842e-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3842e-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-246">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3842e-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3842e-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-248">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="3842e-248">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="3842e-249">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-250">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3842e-250">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-251">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3842e-251">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-253">Дата и время установки службы интеграции в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3842e-253">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="3842e-254">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-255">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3842e-255">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-256">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3842e-258">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="3842e-258">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3842e-259">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="3842e-259">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3842e-260">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-261">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="3842e-261">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-262">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3842e-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-264">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="3842e-264">The last error code reported by the logical device.</span></span> <span data-ttu-id="3842e-265">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-266">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="3842e-266">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-267">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3842e-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-269">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="3842e-269">This property has been deprecated.</span></span> <span data-ttu-id="3842e-270">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3842e-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-271">**Name**</span><span class="sxs-lookup"><span data-stu-id="3842e-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-272">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-274">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="3842e-274">The label by which the object is known.</span></span> <span data-ttu-id="3842e-275">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-275">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-276">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="3842e-276">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-277">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-279">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3842e-279">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3842e-280">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="3842e-280">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3842e-281">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3842e-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3842e-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="3842e-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="3842e-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="3842e-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="3842e-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="3842e-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="3842e-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="3842e-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="3842e-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="3842e-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="3842e-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="3842e-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="3842e-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="3842e-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="3842e-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="3842e-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="3842e-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3842e-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3842e-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3842e-301">)</span><span class="sxs-lookup"><span data-stu-id="3842e-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3842e-302">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3842e-302">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-303">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3842e-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3842e-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-305">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="3842e-305">The current status of the element.</span></span> <span data-ttu-id="3842e-306">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-306">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="3842e-307">Ниже приведены возможные значения для  \[ \] значения свойства OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="3842e-307">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="3842e-308">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-308">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="3842e-309">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-309">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3842e-310"><dt>открыт</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-310"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="3842e-311"><dt>**ОК**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-311"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="3842e-312">Служба работает нормально.</span><span class="sxs-lookup"><span data-stu-id="3842e-312">The service is operating normally.</span></span> <span data-ttu-id="3842e-313"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3842e-313">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="3842e-314"><dt>**Снижение уровня работоспособности**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-314"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="3842e-315">Служба работает нормально, но Гостевая служба согласовала совместимую версию протокола связи.</span><span class="sxs-lookup"><span data-stu-id="3842e-315">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="3842e-316"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3842e-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="3842e-317"><dt>**Неустранимая ошибка**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-317"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="3842e-318">Гостевая версия не поддерживает совместимую версию протокола.</span><span class="sxs-lookup"><span data-stu-id="3842e-318">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="3842e-319"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3842e-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="3842e-320"><dt>**Нет контакта**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-320"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="3842e-321">Гостевая служба не установлена или еще не подключена.</span><span class="sxs-lookup"><span data-stu-id="3842e-321">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="3842e-322"><dt>**Потеря связи**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-322"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="3842e-323">Гостевая служба больше не отвечает в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="3842e-323">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="3842e-324">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="3842e-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-327">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="3842e-327">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="3842e-328">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="3842e-328">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="3842e-329">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3842e-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3842e-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-331">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3842e-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3842e-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-333">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="3842e-333">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="3842e-334">Это свойство наследуется от CIM с параметром и всегда имеет значение **null**. [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)</span><span class="sxs-lookup"><span data-stu-id="3842e-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-335">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="3842e-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-336">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3842e-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3842e-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-338">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="3842e-338">The power management capabilities of the device.</span></span> <span data-ttu-id="3842e-339">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-340">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="3842e-340">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-341">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3842e-341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-343">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="3842e-343">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="3842e-344">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-345">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="3842e-345">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-346">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3842e-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-348">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="3842e-348">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="3842e-349">Это свойство наследуется от [**CIM \_ , но**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-350">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="3842e-350">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-351">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-353">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="3842e-353">Provides high level status information.</span></span> <span data-ttu-id="3842e-354">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="3842e-354">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3842e-355">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="3842e-355">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3842e-356">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3842e-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3842e-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-358"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="3842e-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="3842e-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="3842e-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3842e-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3842e-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="3842e-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3842e-363">)</span><span class="sxs-lookup"><span data-stu-id="3842e-363">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3842e-364">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3842e-364">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-365">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-367">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="3842e-367">The last requested or desired state for the element.</span></span> <span data-ttu-id="3842e-368">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3842e-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3842e-369">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-369">Value</span></span>                                                                         | <span data-ttu-id="3842e-370">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-370">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3842e-371"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-371"><dt>12</dt></span></span> </dl> | <span data-ttu-id="3842e-372">Не применимо</span><span class="sxs-lookup"><span data-stu-id="3842e-372">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3842e-373">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="3842e-373">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-376">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="3842e-376">A string that specifies the current status of the object.</span></span> <span data-ttu-id="3842e-377">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , но не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-378">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="3842e-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-379">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3842e-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3842e-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-381">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="3842e-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3842e-382">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3842e-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3842e-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-384">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-386">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="3842e-386">The current state of the logical device.</span></span> <span data-ttu-id="3842e-387">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-387">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-388">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="3842e-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-389">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-391">Имя класса создания для системы области.</span><span class="sxs-lookup"><span data-stu-id="3842e-391">The creation class name of the scoping system.</span></span> <span data-ttu-id="3842e-392">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3842e-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-393">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3842e-393">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-394">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3842e-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-396">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="3842e-396">The name of the scoping system.</span></span> <span data-ttu-id="3842e-397">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3842e-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3842e-398">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="3842e-398">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-399">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3842e-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-401">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="3842e-401">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3842e-402">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3842e-402">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-403">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="3842e-403">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-404">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3842e-404">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-406">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="3842e-406">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="3842e-407">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="3842e-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3842e-408">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="3842e-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3842e-409">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3842e-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3842e-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3842e-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3842e-411">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="3842e-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3842e-412">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3842e-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3842e-413">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-413">Value</span></span>                                                                         | <span data-ttu-id="3842e-414">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-414">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3842e-415"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-415"><dt>12</dt></span></span> </dl> | <span data-ttu-id="3842e-416">Не применимо</span><span class="sxs-lookup"><span data-stu-id="3842e-416">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3842e-417">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3842e-417">Remarks</span></span>

<span data-ttu-id="3842e-418">Доступ к классу **\_ тимесинккомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="3842e-418">Access to the **Msvm\_TimeSyncComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3842e-419">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3842e-419">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3842e-420">Требования</span><span class="sxs-lookup"><span data-stu-id="3842e-420">Requirements</span></span>



| <span data-ttu-id="3842e-421">Требование</span><span class="sxs-lookup"><span data-stu-id="3842e-421">Requirement</span></span> | <span data-ttu-id="3842e-422">Значение</span><span class="sxs-lookup"><span data-stu-id="3842e-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3842e-423">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3842e-423">Minimum supported client</span></span><br/> | <span data-ttu-id="3842e-424">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3842e-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3842e-425">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3842e-425">Minimum supported server</span></span><br/> | <span data-ttu-id="3842e-426">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3842e-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3842e-427">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3842e-427">Namespace</span></span><br/>                | <span data-ttu-id="3842e-428">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3842e-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3842e-429">MOF</span><span class="sxs-lookup"><span data-stu-id="3842e-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3842e-430"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3842e-431">DLL</span><span class="sxs-lookup"><span data-stu-id="3842e-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3842e-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3842e-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3842e-433">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3842e-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3842e-434">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="3842e-434">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="3842e-435">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="3842e-435">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

