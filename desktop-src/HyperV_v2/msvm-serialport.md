---
description: Представляет последовательный порт, связанный с контроллером последовательного порта.
ms.assetid: 856823A5-7481-453A-8476-1CDAB1D84123
title: Класс Msvm_SerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPort
- Msvm_SerialPort.SetPowerState
- Msvm_SerialPort.EnableDevice
- Msvm_SerialPort.OnlineDevice
- Msvm_SerialPort.QuiesceDevice
- Msvm_SerialPort.SaveProperties
- Msvm_SerialPort.RestoreProperties
- Msvm_SerialPort.InstanceID
- Msvm_SerialPort.Caption
- Msvm_SerialPort.Description
- Msvm_SerialPort.ElementName
- Msvm_SerialPort.InstallDate
- Msvm_SerialPort.Name
- Msvm_SerialPort.OperationalStatus
- Msvm_SerialPort.StatusDescriptions
- Msvm_SerialPort.Status
- Msvm_SerialPort.HealthState
- Msvm_SerialPort.CommunicationStatus
- Msvm_SerialPort.DetailedStatus
- Msvm_SerialPort.OperatingStatus
- Msvm_SerialPort.PrimaryStatus
- Msvm_SerialPort.EnabledState
- Msvm_SerialPort.OtherEnabledState
- Msvm_SerialPort.RequestedState
- Msvm_SerialPort.EnabledDefault
- Msvm_SerialPort.TimeOfLastStateChange
- Msvm_SerialPort.AvailableRequestedStates
- Msvm_SerialPort.TransitioningToState
- Msvm_SerialPort.SystemCreationClassName
- Msvm_SerialPort.SystemName
- Msvm_SerialPort.CreationClassName
- Msvm_SerialPort.DeviceID
- Msvm_SerialPort.PowerManagementSupported
- Msvm_SerialPort.PowerManagementCapabilities
- Msvm_SerialPort.Availability
- Msvm_SerialPort.StatusInfo
- Msvm_SerialPort.LastErrorCode
- Msvm_SerialPort.ErrorDescription
- Msvm_SerialPort.ErrorCleared
- Msvm_SerialPort.OtherIdentifyingInfo
- Msvm_SerialPort.PowerOnHours
- Msvm_SerialPort.TotalPowerOnHours
- Msvm_SerialPort.IdentifyingDescriptions
- Msvm_SerialPort.AdditionalAvailability
- Msvm_SerialPort.MaxQuiesceTime
- Msvm_SerialPort.Speed
- Msvm_SerialPort.MaxSpeed
- Msvm_SerialPort.RequestedSpeed
- Msvm_SerialPort.UsageRestriction
- Msvm_SerialPort.PortType
- Msvm_SerialPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc9ff5e1ce4b0a750866a9957c0cffc4bc8501e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910132"
---
# <a name="msvm_serialport-class"></a><span data-ttu-id="7d208-103">\_Класс мсвм SerialPort</span><span class="sxs-lookup"><span data-stu-id="7d208-103">Msvm\_SerialPort class</span></span>

<span data-ttu-id="7d208-104">Представляет последовательный порт, связанный с контроллером последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="7d208-104">Represents a serial port associated with the serial controller.</span></span>

<span data-ttu-id="7d208-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7d208-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d208-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d208-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPort : CIM_LogicalPort
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual Serial Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
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
  string   CreationClassName = "Msvm_SerialPort";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint64   Speed = 115200;
  uint32   MaxSpeed = 115200;
  uint64   RequestedSpeed = 115200;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Serial Port";
};
```

## <a name="members"></a><span data-ttu-id="7d208-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7d208-107">Members</span></span>

<span data-ttu-id="7d208-108">Класс **мсвм \_ SerialPort** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7d208-108">The **Msvm\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="7d208-109">Методы</span><span class="sxs-lookup"><span data-stu-id="7d208-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7d208-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d208-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7d208-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7d208-111">Methods</span></span>

<span data-ttu-id="7d208-112">Класс **мсвм \_ SerialPort** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7d208-112">The **Msvm\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="7d208-113">Метод</span><span class="sxs-lookup"><span data-stu-id="7d208-113">Method</span></span>                                                           | <span data-ttu-id="7d208-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7d208-114">Description</span></span>                              |
|:-----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="7d208-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="7d208-115">**EnableDevice**</span></span>                                                 | <span data-ttu-id="7d208-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d208-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7d208-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="7d208-117">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="7d208-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d208-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7d208-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="7d208-119">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="7d208-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d208-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="7d208-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="7d208-121">**RequestStateChange**</span></span>](msvm-serialport-requeststatechange.md) | <span data-ttu-id="7d208-122">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="7d208-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="7d208-123">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="7d208-123">**Reset**</span></span>](msvm-serialport-reset.md)                           | <span data-ttu-id="7d208-124">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="7d208-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="7d208-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="7d208-125">**RestoreProperties**</span></span>                                            | <span data-ttu-id="7d208-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d208-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7d208-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="7d208-127">**SaveProperties**</span></span>                                               | <span data-ttu-id="7d208-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d208-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7d208-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7d208-129">**SetPowerState**</span></span>                                                | <span data-ttu-id="7d208-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d208-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7d208-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d208-131">Properties</span></span>

<span data-ttu-id="7d208-132">Класс **мсвм \_ SerialPort** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7d208-132">The **Msvm\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d208-133">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="7d208-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7d208-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7d208-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-136">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="7d208-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="7d208-137">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d208-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="7d208-138">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-138">Value</span></span>                                                                            | <span data-ttu-id="7d208-139">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7d208-140"><dt>1-6</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="7d208-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="7d208-142">Не применимо</span><span class="sxs-lookup"><span data-stu-id="7d208-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d208-143">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="7d208-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-146">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="7d208-146">The primary availability and status of the device.</span></span> <span data-ttu-id="7d208-147">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d208-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="7d208-148">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-148">Value</span></span>                                                                        | <span data-ttu-id="7d208-149">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7d208-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="7d208-151">Не применимо</span><span class="sxs-lookup"><span data-stu-id="7d208-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d208-152">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="7d208-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-153">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7d208-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7d208-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-155">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="7d208-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="7d208-156">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-157">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7d208-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-160">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7d208-160">A short description of the object.</span></span> <span data-ttu-id="7d208-161">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-162">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="7d208-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-165">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="7d208-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7d208-166">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="7d208-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7d208-167">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7d208-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7d208-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="7d208-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="7d208-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="7d208-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="7d208-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7d208-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7d208-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7d208-175">)</span><span class="sxs-lookup"><span data-stu-id="7d208-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d208-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7d208-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-179">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7d208-179">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7d208-180">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d208-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-181">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7d208-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-184">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7d208-184">A description of the object.</span></span> <span data-ttu-id="7d208-185">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7d208-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-187">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-189">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="7d208-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7d208-190">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="7d208-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7d208-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7d208-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="7d208-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="7d208-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="7d208-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="7d208-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="7d208-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="7d208-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7d208-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7d208-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7d208-200">)</span><span class="sxs-lookup"><span data-stu-id="7d208-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d208-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7d208-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-204">Это свойство наследуется от CIM-класса, и ему присваивается значение "Microsoft:*GUID* устройства — [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) \\ *специфические данные*", где *данные, относящиеся к устройству* , являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="7d208-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*", where *device-specific-data* is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7d208-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-208">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="7d208-208">A display name for the object.</span></span> <span data-ttu-id="7d208-209">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-210">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="7d208-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-211">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-213">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="7d208-213">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="7d208-214">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="7d208-215">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-215">Value</span></span>                                                                        | <span data-ttu-id="7d208-216">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-216">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="7d208-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7d208-218">Активировано</span><span class="sxs-lookup"><span data-stu-id="7d208-218">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d208-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7d208-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-220">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-222">Включенное состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="7d208-222">The enabled state of the element.</span></span> <span data-ttu-id="7d208-223">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="7d208-223">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="7d208-224">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-224">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="7d208-225">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-225">Value</span></span>                                                                        | <span data-ttu-id="7d208-226">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-226">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7d208-227"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-227"><dt>5</dt></span></span> </dl> | <span data-ttu-id="7d208-228">Не применимо</span><span class="sxs-lookup"><span data-stu-id="7d208-228">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d208-229">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="7d208-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-230">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7d208-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-232">Указывает, что сообщение об ошибке в свойстве **ластерроркоде** теперь отключено.</span><span class="sxs-lookup"><span data-stu-id="7d208-232">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="7d208-233">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7d208-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-237">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="7d208-237">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="7d208-238">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7d208-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-240">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-242">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="7d208-242">The current health of the element.</span></span> <span data-ttu-id="7d208-243">Это выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="7d208-243">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="7d208-244">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="7d208-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="7d208-245">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7d208-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-247">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="7d208-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7d208-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-249">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="7d208-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="7d208-250">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7d208-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7d208-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-252">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7d208-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-254">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7d208-254">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="7d208-255">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-256">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7d208-256">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d208-259">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="7d208-259">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7d208-260">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="7d208-260">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7d208-261">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-261">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-262">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="7d208-262">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-263">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7d208-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-265">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="7d208-265">The last error code reported by the logical device.</span></span> <span data-ttu-id="7d208-266">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-266">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-267">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="7d208-267">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-268">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7d208-268">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-270">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7d208-270">This property has been deprecated.</span></span> <span data-ttu-id="7d208-271">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d208-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-272">**максспид**</span><span class="sxs-lookup"><span data-stu-id="7d208-272">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-273">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7d208-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-275">Максимальная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="7d208-275">The maximum bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="7d208-276">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-276">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-277">**Name**</span><span class="sxs-lookup"><span data-stu-id="7d208-277">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-280">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="7d208-280">The label by which the object is known.</span></span> <span data-ttu-id="7d208-281">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="7d208-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-282">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="7d208-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-283">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-285">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="7d208-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7d208-286">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="7d208-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7d208-287">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7d208-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7d208-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="7d208-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="7d208-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="7d208-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="7d208-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="7d208-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="7d208-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="7d208-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="7d208-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="7d208-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="7d208-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="7d208-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="7d208-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="7d208-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="7d208-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="7d208-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="7d208-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7d208-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7d208-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7d208-307">)</span><span class="sxs-lookup"><span data-stu-id="7d208-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d208-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7d208-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-309">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7d208-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7d208-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-311">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="7d208-311">The current statuses of the object.</span></span> <span data-ttu-id="7d208-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-313">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="7d208-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-314">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-316">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="7d208-316">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="7d208-317">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="7d208-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="7d208-318">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="7d208-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-320">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="7d208-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7d208-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-322">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7d208-322">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="7d208-323">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7d208-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-324">**осерпорттипе**</span><span class="sxs-lookup"><span data-stu-id="7d208-324">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-327">Тип модуля, когда для **portType** задано значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="7d208-327">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="7d208-328">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-328">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-329">**Порта**</span><span class="sxs-lookup"><span data-stu-id="7d208-329">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-330">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-332">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-332">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="7d208-333">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-333">Value</span></span>                                                                        | <span data-ttu-id="7d208-334">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-334">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="7d208-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-335"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7d208-336">Другое</span><span class="sxs-lookup"><span data-stu-id="7d208-336">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d208-337">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="7d208-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-338">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7d208-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7d208-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-340">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="7d208-340">The power management capabilities of the device.</span></span> <span data-ttu-id="7d208-341">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-341">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-342">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="7d208-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-343">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7d208-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-345">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="7d208-345">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="7d208-346">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-347">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="7d208-347">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-348">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7d208-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-350">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="7d208-350">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="7d208-351">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-351">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-352">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="7d208-352">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-353">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-353">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-355">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="7d208-355">Provides high level status information.</span></span> <span data-ttu-id="7d208-356">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="7d208-356">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="7d208-357">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="7d208-357">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7d208-358">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-358">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7d208-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7d208-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-360"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="7d208-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="7d208-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="7d208-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="7d208-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7d208-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="7d208-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7d208-365">)</span><span class="sxs-lookup"><span data-stu-id="7d208-365">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d208-366">**рекуестедспид**</span><span class="sxs-lookup"><span data-stu-id="7d208-366">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-367">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7d208-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-369">Запрошенная пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="7d208-369">The requested bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="7d208-370">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-370">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-371">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="7d208-371">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-372">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-374">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="7d208-374">The last requested or desired state for the element.</span></span> <span data-ttu-id="7d208-375">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="7d208-375">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="7d208-376">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="7d208-376">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="7d208-377">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="7d208-378">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-378">Value</span></span>                                                                         | <span data-ttu-id="7d208-379">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7d208-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="7d208-381">Не применимо</span><span class="sxs-lookup"><span data-stu-id="7d208-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d208-382">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="7d208-382">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-383">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7d208-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-385">Пропускная способность порта в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="7d208-385">The bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="7d208-386">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-386">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-387">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="7d208-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-388">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-390">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="7d208-390">The current status of the object.</span></span> <span data-ttu-id="7d208-391">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-392">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="7d208-392">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-393">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="7d208-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7d208-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-395">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="7d208-395">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7d208-396">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7d208-396">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-397">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7d208-397">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-398">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-400">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7d208-400">The current state of the logical device.</span></span> <span data-ttu-id="7d208-401">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-402">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="7d208-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-405">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="7d208-405">The scoping system's creation class name.</span></span> <span data-ttu-id="7d208-406">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d208-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7d208-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-408">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d208-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-410">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7d208-410">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="7d208-411">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d208-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7d208-412">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="7d208-412">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-413">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7d208-413">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-415">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="7d208-415">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="7d208-416">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7d208-416">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-417">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="7d208-417">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-418">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7d208-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-420">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="7d208-420">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="7d208-421">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-422">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="7d208-422">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-423">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-425">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="7d208-425">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="7d208-426">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="7d208-426">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d208-427">**усажерестриктион**</span><span class="sxs-lookup"><span data-stu-id="7d208-427">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d208-428">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d208-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d208-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d208-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d208-430">В некоторых случаях логический порт может идентифицироваться как интерфейсный или серверный порт.</span><span class="sxs-lookup"><span data-stu-id="7d208-430">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="7d208-431">В качестве примера такой ситуации можно привести массив хранения данных, который может иметь серверные порты для взаимодействия с дисками и интерфейсными портами для взаимодействия с узлами.</span><span class="sxs-lookup"><span data-stu-id="7d208-431">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="7d208-432">При отсутствии ограничений на использование порта значение должно быть равно 4 (не ограничено).</span><span class="sxs-lookup"><span data-stu-id="7d208-432">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="7d208-433">Это свойство наследуется от [**CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7d208-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="7d208-434">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-434">Value</span></span>                                                                        | <span data-ttu-id="7d208-435">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-435">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="7d208-436"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-436"><dt>4</dt></span></span> </dl> | <span data-ttu-id="7d208-437">Не ограничено</span><span class="sxs-lookup"><span data-stu-id="7d208-437">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d208-438">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d208-438">Remarks</span></span>

<span data-ttu-id="7d208-439">Доступ к классу **мсвм \_ SerialPort** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7d208-439">Access to the **Msvm\_SerialPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7d208-440">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7d208-440">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d208-441">Требования</span><span class="sxs-lookup"><span data-stu-id="7d208-441">Requirements</span></span>



| <span data-ttu-id="7d208-442">Требование</span><span class="sxs-lookup"><span data-stu-id="7d208-442">Requirement</span></span> | <span data-ttu-id="7d208-443">Значение</span><span class="sxs-lookup"><span data-stu-id="7d208-443">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d208-444">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d208-444">Minimum supported client</span></span><br/> | <span data-ttu-id="7d208-445">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7d208-445">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7d208-446">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d208-446">Minimum supported server</span></span><br/> | <span data-ttu-id="7d208-447">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7d208-447">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d208-448">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7d208-448">Namespace</span></span><br/>                | <span data-ttu-id="7d208-449">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7d208-449">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7d208-450">MOF</span><span class="sxs-lookup"><span data-stu-id="7d208-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d208-451"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-451"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d208-452">DLL</span><span class="sxs-lookup"><span data-stu-id="7d208-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d208-453"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d208-453"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d208-454">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d208-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d208-455">**\_ЛОГИКАЛПОРТ CIM**</span><span class="sxs-lookup"><span data-stu-id="7d208-455">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> <dt>

<span data-ttu-id="7d208-456">[**\_ЛОГИКАЛПОРТ CIM**](/previous-versions//cc136869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7d208-456">[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7d208-457">Классы последовательных устройств</span><span class="sxs-lookup"><span data-stu-id="7d208-457">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

