---
description: Представляет виртуальный процессор в виртуальной машине.
ms.assetid: 4BA91C44-0F85-42D1-A8B5-147E1D532FB5
title: Класс Msvm_Processor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor
- Msvm_Processor.SetPowerState
- Msvm_Processor.EnableDevice
- Msvm_Processor.OnlineDevice
- Msvm_Processor.QuiesceDevice
- Msvm_Processor.SaveProperties
- Msvm_Processor.RestoreProperties
- Msvm_Processor.InstanceID
- Msvm_Processor.Caption
- Msvm_Processor.Description
- Msvm_Processor.ElementName
- Msvm_Processor.InstallDate
- Msvm_Processor.Name
- Msvm_Processor.OperationalStatus
- Msvm_Processor.StatusDescriptions
- Msvm_Processor.Status
- Msvm_Processor.HealthState
- Msvm_Processor.CommunicationStatus
- Msvm_Processor.DetailedStatus
- Msvm_Processor.OperatingStatus
- Msvm_Processor.PrimaryStatus
- Msvm_Processor.EnabledState
- Msvm_Processor.OtherEnabledState
- Msvm_Processor.RequestedState
- Msvm_Processor.EnabledDefault
- Msvm_Processor.TimeOfLastStateChange
- Msvm_Processor.AvailableRequestedStates
- Msvm_Processor.TransitioningToState
- Msvm_Processor.SystemCreationClassName
- Msvm_Processor.SystemName
- Msvm_Processor.CreationClassName
- Msvm_Processor.DeviceID
- Msvm_Processor.PowerManagementSupported
- Msvm_Processor.PowerManagementCapabilities
- Msvm_Processor.Availability
- Msvm_Processor.StatusInfo
- Msvm_Processor.LastErrorCode
- Msvm_Processor.ErrorDescription
- Msvm_Processor.ErrorCleared
- Msvm_Processor.OtherIdentifyingInfo
- Msvm_Processor.PowerOnHours
- Msvm_Processor.TotalPowerOnHours
- Msvm_Processor.IdentifyingDescriptions
- Msvm_Processor.AdditionalAvailability
- Msvm_Processor.MaxQuiesceTime
- Msvm_Processor.Role
- Msvm_Processor.Family
- Msvm_Processor.OtherFamilyDescription
- Msvm_Processor.UpgradeMethod
- Msvm_Processor.MaxClockSpeed
- Msvm_Processor.CurrentClockSpeed
- Msvm_Processor.DataWidth
- Msvm_Processor.AddressWidth
- Msvm_Processor.LoadPercentage
- Msvm_Processor.Stepping
- Msvm_Processor.UniqueID
- Msvm_Processor.CPUStatus
- Msvm_Processor.ExternalBusClockSpeed
- Msvm_Processor.LoadPercentageHistory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 14ed1e2bbb9e15f89376234da8981faffb1a6809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910147"
---
# <a name="msvm_processor-class"></a><span data-ttu-id="e711e-103">\_Класс процессора мсвм</span><span class="sxs-lookup"><span data-stu-id="e711e-103">Msvm\_Processor class</span></span>

<span data-ttu-id="e711e-104">Представляет виртуальный процессор в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e711e-104">Represents the virtual processor in a virtual machine.</span></span>

<span data-ttu-id="e711e-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e711e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e711e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e711e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Processor : CIM_Processor
{
  string   InstanceID;
  string   Caption = "Processor";
  string   Description = " A logical processor of the hypervisor running on the host computer system.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 2;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Processor";
  string   DeviceID = "Microsoft:GUID\device specific data";
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
  string   Role = "Central Processor";
  uint16   Family;
  string   OtherFamilyDescription;
  uint16   UpgradeMethod;
  uint32   MaxClockSpeed;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  uint16   AddressWidth;
  uint16   LoadPercentage;
  string   Stepping;
  string   UniqueID;
  uint16   CPUStatus;
  uint32   ExternalBusClockSpeed;
  uint16   LoadPercentageHistory[];
};
```

## <a name="members"></a><span data-ttu-id="e711e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e711e-107">Members</span></span>

<span data-ttu-id="e711e-108">Класс **\_ процессора мсвм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e711e-108">The **Msvm\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="e711e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="e711e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e711e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e711e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e711e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e711e-111">Methods</span></span>

<span data-ttu-id="e711e-112">Класс **\_ процессора мсвм** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e711e-112">The **Msvm\_Processor** class has these methods.</span></span>



| <span data-ttu-id="e711e-113">Метод</span><span class="sxs-lookup"><span data-stu-id="e711e-113">Method</span></span>                                                          | <span data-ttu-id="e711e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e711e-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e711e-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="e711e-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="e711e-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e711e-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e711e-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="e711e-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="e711e-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e711e-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e711e-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="e711e-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="e711e-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e711e-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e711e-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="e711e-121">**RequestStateChange**</span></span>](msvm-processor-requeststatechange.md) | <span data-ttu-id="e711e-122">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="e711e-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e711e-123">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="e711e-123">**Reset**</span></span>](msvm-processor-reset.md)                           | <span data-ttu-id="e711e-124">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="e711e-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="e711e-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="e711e-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="e711e-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e711e-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e711e-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="e711e-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="e711e-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e711e-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e711e-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e711e-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="e711e-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e711e-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e711e-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="e711e-131">Properties</span></span>

<span data-ttu-id="e711e-132">Класс **\_ процессора мсвм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e711e-132">The **Msvm\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e711e-133">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="e711e-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e711e-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e711e-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-136">Любая дополнительная доступность и состояние устройства, кроме указанного в свойстве **Availability** .</span><span class="sxs-lookup"><span data-stu-id="e711e-136">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="e711e-137">Свойство **Availability** указывает основное состояние и доступность устройства.</span><span class="sxs-lookup"><span data-stu-id="e711e-137">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="e711e-138">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e711e-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-139">**аддрессвидс**</span><span class="sxs-lookup"><span data-stu-id="e711e-139">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-142">Ширина адреса процессора в битах.</span><span class="sxs-lookup"><span data-stu-id="e711e-142">The processor address width, in bits.</span></span> <span data-ttu-id="e711e-143">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor), а значение — 32 или 64, в зависимости от характеристик виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e711e-143">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-144">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="e711e-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-145">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-147">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="e711e-147">The primary availability and status of the device.</span></span> <span data-ttu-id="e711e-148">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-149">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="e711e-149">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-150">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e711e-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e711e-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-152">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e711e-152">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e711e-153">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e711e-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-154">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e711e-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e711e-157">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e711e-157">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="e711e-158">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e711e-158">A short description of the object.</span></span> <span data-ttu-id="e711e-159">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-160">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="e711e-160">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-161">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-163">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="e711e-163">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e711e-164">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e711e-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e711e-165">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e711e-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e711e-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="e711e-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="e711e-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="e711e-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="e711e-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e711e-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e711e-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e711e-173">)</span><span class="sxs-lookup"><span data-stu-id="e711e-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e711e-174">**кпустатус**</span><span class="sxs-lookup"><span data-stu-id="e711e-174">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-175">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-177">Текущее состояние процессора.</span><span class="sxs-lookup"><span data-stu-id="e711e-177">The current status of the processor.</span></span> <span data-ttu-id="e711e-178">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="e711e-178">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e711e-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e711e-182">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e711e-182">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e711e-183">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e711e-183">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e711e-184">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="e711e-184">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="e711e-185">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e711e-185">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-186">**куррентклоккспид**</span><span class="sxs-lookup"><span data-stu-id="e711e-186">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-187">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e711e-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-189">Максимальная скорость физического процессора, учитывающая емкость виртуального процессора.</span><span class="sxs-lookup"><span data-stu-id="e711e-189">The maximum speed of the physical processor, taking into account the capacity for the virtual processor.</span></span> <span data-ttu-id="e711e-190">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="e711e-190">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-191">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="e711e-191">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-192">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-194">Ширина данных процессора в битах.</span><span class="sxs-lookup"><span data-stu-id="e711e-194">The processor data width, in bits.</span></span> <span data-ttu-id="e711e-195">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor), а значение — 32 или 64, в зависимости от характеристик виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e711e-195">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-196">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e711e-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-199">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e711e-199">A description of the object.</span></span> <span data-ttu-id="e711e-200">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e711e-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-202">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-204">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="e711e-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e711e-205">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e711e-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e711e-206">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e711e-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="e711e-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="e711e-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="e711e-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="e711e-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="e711e-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="e711e-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e711e-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e711e-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e711e-215">)</span><span class="sxs-lookup"><span data-stu-id="e711e-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e711e-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e711e-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-219">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e711e-219">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="e711e-220">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-*класса*, и ему всегда присваивается значение "Майкрософт: \\ *данные, относящиеся к устройству*".</span><span class="sxs-lookup"><span data-stu-id="e711e-220">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="e711e-221">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e711e-221">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-224">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e711e-224">A display name for the object.</span></span> <span data-ttu-id="e711e-225">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-226">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="e711e-226">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-227">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-229">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e711e-229">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="e711e-230">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e711e-230">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-231">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e711e-231">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-232">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-234">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e711e-234">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e711e-235">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e711e-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-236">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="e711e-236">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-237">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e711e-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-239">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="e711e-239">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="e711e-240">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-241">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e711e-241">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-244">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="e711e-244">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="e711e-245">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-246">**екстерналбусклоккспид**</span><span class="sxs-lookup"><span data-stu-id="e711e-246">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-247">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e711e-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-249">Тактовая частота внешней шины на базовом физическом процессоре.</span><span class="sxs-lookup"><span data-stu-id="e711e-249">The external bus clock speed of the underlying physical processor.</span></span> <span data-ttu-id="e711e-250">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="e711e-250">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-251">**Семейство**</span><span class="sxs-lookup"><span data-stu-id="e711e-251">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-252">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-254">Семейство процессоров базового физического процессора.</span><span class="sxs-lookup"><span data-stu-id="e711e-254">The processor family of the underlying physical processor.</span></span> <span data-ttu-id="e711e-255">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="e711e-255">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e711e-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-257">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-259">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="e711e-259">The current health of the element.</span></span> <span data-ttu-id="e711e-260">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e711e-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-262">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e711e-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e711e-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-264">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве [**осеридентифингинфо**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="e711e-264">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="e711e-265">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e711e-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e711e-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-267">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e711e-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-269">Дата и время создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e711e-269">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="e711e-270">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e711e-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-272">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e711e-274">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e711e-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e711e-275">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="e711e-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e711e-276">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-277">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="e711e-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-278">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e711e-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-280">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="e711e-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="e711e-281">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-282">**лоадперцентаже**</span><span class="sxs-lookup"><span data-stu-id="e711e-282">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-283">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-285">Текущий процент от общей вычислительной мощности, потребляемой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="e711e-285">The current percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="e711e-286">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="e711e-286">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-287">**лоадперцентажехистори**</span><span class="sxs-lookup"><span data-stu-id="e711e-287">**LoadPercentageHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-288">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e711e-288">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e711e-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e711e-290">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="e711e-290">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e711e-291">Записанный журнал в процентах от общей вычислительной мощности, потребляемой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="e711e-291">The recorded history of percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="e711e-292">Это массив, содержащий примеры.</span><span class="sxs-lookup"><span data-stu-id="e711e-292">This is an array containing samples.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-293">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="e711e-293">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-294">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e711e-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-296">Максимальная тактовая частота виртуального процессора (в мегагерцах).</span><span class="sxs-lookup"><span data-stu-id="e711e-296">The maximum clock speed, in megahertz, of the virtual processor.</span></span> <span data-ttu-id="e711e-297">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="e711e-297">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-298">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="e711e-298">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-299">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e711e-299">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-301">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e711e-301">This property has been deprecated.</span></span> <span data-ttu-id="e711e-302">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-303">**Name**</span><span class="sxs-lookup"><span data-stu-id="e711e-303">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e711e-306">Квалификаторы: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="e711e-306">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="e711e-307">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="e711e-307">The label by which the object is known.</span></span> <span data-ttu-id="e711e-308">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="e711e-308">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="e711e-309">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-310">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="e711e-310">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-311">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-311">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-313">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e711e-313">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e711e-314">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e711e-314">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e711e-315">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e711e-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e711e-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="e711e-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="e711e-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="e711e-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="e711e-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="e711e-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="e711e-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="e711e-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="e711e-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="e711e-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="e711e-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="e711e-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="e711e-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="e711e-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="e711e-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="e711e-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="e711e-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e711e-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e711e-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e711e-335">)</span><span class="sxs-lookup"><span data-stu-id="e711e-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e711e-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e711e-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-337">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e711e-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e711e-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-339">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="e711e-339">The current status of the element.</span></span> <span data-ttu-id="e711e-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-341">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="e711e-341">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-344">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e711e-344">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e711e-345">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="e711e-345">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e711e-346">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e711e-346">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-347">**осерфамилидескриптион**</span><span class="sxs-lookup"><span data-stu-id="e711e-347">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-348">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-350">Описание типа семейства процессоров.</span><span class="sxs-lookup"><span data-stu-id="e711e-350">A description of the processor family type.</span></span> <span data-ttu-id="e711e-351">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e711e-351">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-352">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e711e-352">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-353">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e711e-353">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e711e-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-355">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e711e-355">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="e711e-356">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e711e-356">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-357">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="e711e-357">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-358">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e711e-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e711e-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-360">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="e711e-360">The power management capabilities of the device.</span></span> <span data-ttu-id="e711e-361">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-362">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="e711e-362">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-363">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e711e-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-365">Указывает, поддерживается ли на устройстве управление питанием.</span><span class="sxs-lookup"><span data-stu-id="e711e-365">Indicates whether power management is supported on the device.</span></span> <span data-ttu-id="e711e-366">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-367">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="e711e-367">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-368">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e711e-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-370">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="e711e-370">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="e711e-371">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-371">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-372">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="e711e-372">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-373">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-375">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="e711e-375">Provides high level status information.</span></span> <span data-ttu-id="e711e-376">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="e711e-376">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e711e-377">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e711e-377">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e711e-378">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-378">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e711e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e711e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-380"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="e711e-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="e711e-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="e711e-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e711e-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e711e-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e711e-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e711e-385">)</span><span class="sxs-lookup"><span data-stu-id="e711e-385">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e711e-386">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e711e-386">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-387">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-389">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="e711e-389">The last requested or desired state for the element.</span></span> <span data-ttu-id="e711e-390">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e711e-390">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-391">**Роль**</span><span class="sxs-lookup"><span data-stu-id="e711e-391">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-392">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-394">Строка, описывающая роль процессора.</span><span class="sxs-lookup"><span data-stu-id="e711e-394">A string that describes the role of the processor.</span></span> <span data-ttu-id="e711e-395">Например, "Центральный процессор" или "математический процессор".</span><span class="sxs-lookup"><span data-stu-id="e711e-395">For example, "Central Processor" or "Math Processor".</span></span> <span data-ttu-id="e711e-396">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="e711e-396">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-397">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e711e-397">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-398">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-400">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e711e-400">The current status of the object.</span></span> <span data-ttu-id="e711e-401">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-402">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="e711e-402">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-403">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e711e-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e711e-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-405">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e711e-405">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e711e-406">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e711e-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-407">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e711e-407">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-408">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-410">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e711e-410">The current state of the logical device.</span></span> <span data-ttu-id="e711e-411">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-412">**Отладка по шагам**</span><span class="sxs-lookup"><span data-stu-id="e711e-412">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-413">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-415">Уровень редакции процессора в семействе процессоров базового физического процессора.</span><span class="sxs-lookup"><span data-stu-id="e711e-415">The revision level of the processor within the processor family of the underlying physical processor.</span></span> <span data-ttu-id="e711e-416">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="e711e-416">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-417">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="e711e-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-418">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e711e-420">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e711e-420">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e711e-421">Имя класса создания для системы области.</span><span class="sxs-lookup"><span data-stu-id="e711e-421">The creation class name of the scoping system.</span></span> <span data-ttu-id="e711e-422">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e711e-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e711e-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e711e-426">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e711e-426">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="e711e-427">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="e711e-427">The name of the scoping system.</span></span> <span data-ttu-id="e711e-428">Это значение соответствует значению свойства [**Name**](msvm-computersystem.md) класса **мсвм \_ ComputerSystem** для виртуальной машины с областями.</span><span class="sxs-lookup"><span data-stu-id="e711e-428">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="e711e-429">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e711e-429">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-430">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="e711e-430">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-431">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e711e-431">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-433">Дата или время изменения состояния виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e711e-433">The date or time at which the virtual machine's state was changed.</span></span> <span data-ttu-id="e711e-434">Если состояние элемента не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала.</span><span class="sxs-lookup"><span data-stu-id="e711e-434">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="e711e-435">Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="e711e-435">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="e711e-436">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e711e-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e711e-437">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="e711e-437">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-438">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e711e-438">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-439">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-440">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="e711e-440">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="e711e-441">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-442">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="e711e-442">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-443">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-445">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e711e-445">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e711e-446">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e711e-446">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-447">**UniqueID**</span><span class="sxs-lookup"><span data-stu-id="e711e-447">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-448">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e711e-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-450">Глобальный уникальный идентификатор процессора.</span><span class="sxs-lookup"><span data-stu-id="e711e-450">A globally unique identifier for the processor.</span></span> <span data-ttu-id="e711e-451">Этот идентификатор может быть уникальным только в пределах семейства процессоров.</span><span class="sxs-lookup"><span data-stu-id="e711e-451">This identifier can only be unique within a processor family.</span></span> <span data-ttu-id="e711e-452">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e711e-452">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e711e-453">**упградемесод**</span><span class="sxs-lookup"><span data-stu-id="e711e-453">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e711e-454">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e711e-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e711e-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e711e-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e711e-456">Сведения о сокете ЦП, включая данные о том, как обновить процессор (если обновления поддерживаются).</span><span class="sxs-lookup"><span data-stu-id="e711e-456">The CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span> <span data-ttu-id="e711e-457">Это свойство наследуется [**от \_ процессора CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="e711e-457">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e711e-458">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e711e-458">Remarks</span></span>

<span data-ttu-id="e711e-459">Доступ к классу **\_ процессора мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e711e-459">Access to the **Msvm\_Processor** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e711e-460">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e711e-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e711e-461">Требования</span><span class="sxs-lookup"><span data-stu-id="e711e-461">Requirements</span></span>



| <span data-ttu-id="e711e-462">Требование</span><span class="sxs-lookup"><span data-stu-id="e711e-462">Requirement</span></span> | <span data-ttu-id="e711e-463">Значение</span><span class="sxs-lookup"><span data-stu-id="e711e-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e711e-464">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e711e-464">Minimum supported client</span></span><br/> | <span data-ttu-id="e711e-465">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e711e-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e711e-466">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e711e-466">Minimum supported server</span></span><br/> | <span data-ttu-id="e711e-467">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e711e-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e711e-468">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e711e-468">Namespace</span></span><br/>                | <span data-ttu-id="e711e-469">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e711e-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e711e-470">MOF</span><span class="sxs-lookup"><span data-stu-id="e711e-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e711e-471"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e711e-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e711e-472">DLL</span><span class="sxs-lookup"><span data-stu-id="e711e-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e711e-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e711e-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e711e-474">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e711e-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e711e-475">**\_Процессор CIM**</span><span class="sxs-lookup"><span data-stu-id="e711e-475">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dt>

[<span data-ttu-id="e711e-476">**\_Процессор CIM**</span><span class="sxs-lookup"><span data-stu-id="e711e-476">**CIM\_Processor**</span></span>](/windows/desktop/CIMWin32Prov/cim-processor)
</dt> <dt>

[<span data-ttu-id="e711e-477">Классы процессоров</span><span class="sxs-lookup"><span data-stu-id="e711e-477">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

