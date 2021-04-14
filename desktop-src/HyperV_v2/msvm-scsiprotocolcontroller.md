---
description: Представляет искусственный контроллер SCSI.
ms.assetid: 4ABAB4C8-F922-4AA3-8FEE-5F5AA969E8B4
title: Класс Msvm_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SCSIProtocolController
- Msvm_SCSIProtocolController.SetPowerState
- Msvm_SCSIProtocolController.EnableDevice
- Msvm_SCSIProtocolController.OnlineDevice
- Msvm_SCSIProtocolController.QuiesceDevice
- Msvm_SCSIProtocolController.SaveProperties
- Msvm_SCSIProtocolController.RestoreProperties
- Msvm_SCSIProtocolController.InstanceID
- Msvm_SCSIProtocolController.Caption
- Msvm_SCSIProtocolController.Description
- Msvm_SCSIProtocolController.ElementName
- Msvm_SCSIProtocolController.InstallDate
- Msvm_SCSIProtocolController.Name
- Msvm_SCSIProtocolController.OperationalStatus
- Msvm_SCSIProtocolController.StatusDescriptions
- Msvm_SCSIProtocolController.Status
- Msvm_SCSIProtocolController.HealthState
- Msvm_SCSIProtocolController.CommunicationStatus
- Msvm_SCSIProtocolController.DetailedStatus
- Msvm_SCSIProtocolController.OperatingStatus
- Msvm_SCSIProtocolController.PrimaryStatus
- Msvm_SCSIProtocolController.EnabledState
- Msvm_SCSIProtocolController.OtherEnabledState
- Msvm_SCSIProtocolController.RequestedState
- Msvm_SCSIProtocolController.EnabledDefault
- Msvm_SCSIProtocolController.TimeOfLastStateChange
- Msvm_SCSIProtocolController.AvailableRequestedStates
- Msvm_SCSIProtocolController.TransitioningToState
- Msvm_SCSIProtocolController.SystemCreationClassName
- Msvm_SCSIProtocolController.SystemName
- Msvm_SCSIProtocolController.CreationClassName
- Msvm_SCSIProtocolController.DeviceID
- Msvm_SCSIProtocolController.PowerManagementSupported
- Msvm_SCSIProtocolController.PowerManagementCapabilities
- Msvm_SCSIProtocolController.Availability
- Msvm_SCSIProtocolController.StatusInfo
- Msvm_SCSIProtocolController.LastErrorCode
- Msvm_SCSIProtocolController.ErrorDescription
- Msvm_SCSIProtocolController.ErrorCleared
- Msvm_SCSIProtocolController.OtherIdentifyingInfo
- Msvm_SCSIProtocolController.PowerOnHours
- Msvm_SCSIProtocolController.TotalPowerOnHours
- Msvm_SCSIProtocolController.IdentifyingDescriptions
- Msvm_SCSIProtocolController.AdditionalAvailability
- Msvm_SCSIProtocolController.MaxQuiesceTime
- Msvm_SCSIProtocolController.MaxUnitsControlled
- Msvm_SCSIProtocolController.NameFormat
- Msvm_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b65390c7cb03f195e9de39aedc3629688717e0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547207"
---
# <a name="msvm_scsiprotocolcontroller-class"></a><span data-ttu-id="73dd6-103">\_Класс мсвм сксипротоколконтроллер</span><span class="sxs-lookup"><span data-stu-id="73dd6-103">Msvm\_SCSIProtocolController class</span></span>

<span data-ttu-id="73dd6-104">Представляет искусственный контроллер SCSI.</span><span class="sxs-lookup"><span data-stu-id="73dd6-104">Represents a synthetic SCSI controller.</span></span> <span data-ttu-id="73dd6-105">Синтетический контроллер SCSI может поддерживать до 256 дисков.</span><span class="sxs-lookup"><span data-stu-id="73dd6-105">A synthetic SCSI controller can support up to 256 drives.</span></span>

<span data-ttu-id="73dd6-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="73dd6-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="73dd6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73dd6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SCSIProtocolController : CIM_SCSIProtocolController
{
  string   InstanceID;
  string   Caption = "SCSI Controller";
  string   Description = "Microsoft Virtual SCSI Controller";
  string   ElementName = "SCSI Controller";
  datetime InstallDate;
  string   Name = "SCSI Controller";
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
  string   CreationClassName = "Msvm_SCSIProtocolController";
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
  uint32   MaxUnitsControlled = 256;
  uint16   NameFormat = 0;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="73dd6-108">Члены</span><span class="sxs-lookup"><span data-stu-id="73dd6-108">Members</span></span>

<span data-ttu-id="73dd6-109">Класс **мсвм \_ сксипротоколконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="73dd6-109">The **Msvm\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="73dd6-110">Методы</span><span class="sxs-lookup"><span data-stu-id="73dd6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="73dd6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="73dd6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="73dd6-112">Методы</span><span class="sxs-lookup"><span data-stu-id="73dd6-112">Methods</span></span>

<span data-ttu-id="73dd6-113">Класс **мсвм \_ сксипротоколконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="73dd6-113">The **Msvm\_SCSIProtocolController** class has these methods.</span></span>



| <span data-ttu-id="73dd6-114">Метод</span><span class="sxs-lookup"><span data-stu-id="73dd6-114">Method</span></span>                                                                       | <span data-ttu-id="73dd6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="73dd6-115">Description</span></span>                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="73dd6-116">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="73dd6-116">**EnableDevice**</span></span>                                                             | <span data-ttu-id="73dd6-117">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="73dd6-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73dd6-118">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="73dd6-118">**OnlineDevice**</span></span>                                                             | <span data-ttu-id="73dd6-119">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="73dd6-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73dd6-120">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="73dd6-120">**QuiesceDevice**</span></span>                                                            | <span data-ttu-id="73dd6-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="73dd6-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="73dd6-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="73dd6-122">**RequestStateChange**</span></span>](msvm-scsiprotocolcontroller-requeststatechange.md) | <span data-ttu-id="73dd6-123">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="73dd6-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="73dd6-124">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="73dd6-124">**Reset**</span></span>](msvm-scsiprotocolcontroller-reset.md)                           | <span data-ttu-id="73dd6-125">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="73dd6-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="73dd6-126">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="73dd6-126">**RestoreProperties**</span></span>                                                        | <span data-ttu-id="73dd6-127">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="73dd6-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73dd6-128">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="73dd6-128">**SaveProperties**</span></span>                                                           | <span data-ttu-id="73dd6-129">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="73dd6-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73dd6-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="73dd6-130">**SetPowerState**</span></span>                                                            | <span data-ttu-id="73dd6-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="73dd6-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="73dd6-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="73dd6-132">Properties</span></span>

<span data-ttu-id="73dd6-133">Класс **мсвм \_ сксипротоколконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="73dd6-133">The **Msvm\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73dd6-134">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="73dd6-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-135">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="73dd6-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-137">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="73dd6-137">Any additional availability and status of the device.</span></span> <span data-ttu-id="73dd6-138">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="73dd6-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="73dd6-139">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-139">Value</span></span>                                                                            | <span data-ttu-id="73dd6-140">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-140">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="73dd6-141"><dt>1-6</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-141"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="73dd6-142"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-142"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="73dd6-143">Не применимо</span><span class="sxs-lookup"><span data-stu-id="73dd6-143">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73dd6-144">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="73dd6-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-145">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-147">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="73dd6-147">The primary availability and status of the device.</span></span> <span data-ttu-id="73dd6-148">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="73dd6-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="73dd6-149">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-149">Value</span></span>                                                                        | <span data-ttu-id="73dd6-150">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-150">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="73dd6-151"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-151"><dt>6</dt></span></span> </dl> | <span data-ttu-id="73dd6-152">Не применимо</span><span class="sxs-lookup"><span data-stu-id="73dd6-152">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73dd6-153">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="73dd6-153">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-154">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="73dd6-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-156">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="73dd6-156">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="73dd6-157">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-157">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-158">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="73dd6-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-161">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="73dd6-161">A short description of the object.</span></span> <span data-ttu-id="73dd6-162">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-163">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="73dd6-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-164">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-166">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="73dd6-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="73dd6-167">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="73dd6-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73dd6-168">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="73dd6-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="73dd6-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="73dd6-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="73dd6-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="73dd6-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="73dd6-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="73dd6-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="73dd6-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="73dd6-176">)</span><span class="sxs-lookup"><span data-stu-id="73dd6-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73dd6-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="73dd6-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-180">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="73dd6-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="73dd6-181">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="73dd6-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-182">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73dd6-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-185">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="73dd6-185">A description of the object.</span></span> <span data-ttu-id="73dd6-186">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="73dd6-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-188">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-190">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="73dd6-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="73dd6-191">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="73dd6-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73dd6-192">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="73dd6-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="73dd6-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="73dd6-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="73dd6-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="73dd6-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="73dd6-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="73dd6-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="73dd6-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="73dd6-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="73dd6-201">)</span><span class="sxs-lookup"><span data-stu-id="73dd6-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73dd6-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="73dd6-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-205">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение «Microsoft:*GUID* \\ *устройства-данные*».</span><span class="sxs-lookup"><span data-stu-id="73dd6-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="73dd6-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-209">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="73dd6-209">A display name for the object.</span></span> <span data-ttu-id="73dd6-210">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-211">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="73dd6-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-212">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-214">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="73dd6-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="73dd6-215">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73dd6-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="73dd6-216">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-216">Value</span></span>                                                                        | <span data-ttu-id="73dd6-217">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-217">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="73dd6-218"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-218"><dt>2</dt></span></span> </dl> | <span data-ttu-id="73dd6-219">Активировано</span><span class="sxs-lookup"><span data-stu-id="73dd6-219">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73dd6-220">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="73dd6-220">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-221">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-223">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="73dd6-223">The enabled and disabled states of an element.</span></span> <span data-ttu-id="73dd6-224">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="73dd6-224">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="73dd6-225">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73dd6-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="73dd6-226">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-226">Value</span></span>                                                                        | <span data-ttu-id="73dd6-227">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-227">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="73dd6-228"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-228"><dt>5</dt></span></span> </dl> | <span data-ttu-id="73dd6-229">Не применимо</span><span class="sxs-lookup"><span data-stu-id="73dd6-229">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73dd6-230">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="73dd6-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-231">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73dd6-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-233">Указывает, что сообщение об ошибке в свойстве **ластерроркоде** теперь отключено.</span><span class="sxs-lookup"><span data-stu-id="73dd6-233">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="73dd6-234">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-235">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="73dd6-235">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-236">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-238">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="73dd6-238">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="73dd6-239">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-239">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-240">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="73dd6-240">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-241">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-243">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="73dd6-243">The current health of the element.</span></span> <span data-ttu-id="73dd6-244">Это выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="73dd6-244">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="73dd6-245">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="73dd6-245">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="73dd6-246">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-247">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="73dd6-247">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-248">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="73dd6-248">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-250">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="73dd6-250">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="73dd6-251">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="73dd6-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-252">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="73dd6-252">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-253">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73dd6-253">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-255">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="73dd6-255">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="73dd6-256">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="73dd6-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-260">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="73dd6-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-261">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="73dd6-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="73dd6-262">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-263">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="73dd6-263">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-264">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73dd6-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-266">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="73dd6-266">The last error code reported by the logical device.</span></span> <span data-ttu-id="73dd6-267">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-268">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="73dd6-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-269">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73dd6-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-271">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-271">This property has been deprecated.</span></span> <span data-ttu-id="73dd6-272">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="73dd6-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-273">**максунитсконтроллед**</span><span class="sxs-lookup"><span data-stu-id="73dd6-273">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-274">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73dd6-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-276">Максимальное число единиц, которое может контролироваться или получить доступ через этот контроллер протокола.</span><span class="sxs-lookup"><span data-stu-id="73dd6-276">The maximum number of units that can be controlled by or accessed through this protocol controller.</span></span> <span data-ttu-id="73dd6-277">Это свойство наследуется от [**CIM \_ протоколконтроллер**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="73dd6-277">This property is inherited from [**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-278">**Name**</span><span class="sxs-lookup"><span data-stu-id="73dd6-278">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-281">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="73dd6-281">The label by which the object is known.</span></span> <span data-ttu-id="73dd6-282">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-283">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="73dd6-283">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-284">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-286">Указывает, как выбрано имя контроллера протокола SCSI.</span><span class="sxs-lookup"><span data-stu-id="73dd6-286">Identifies how the name of the SCSI protocol controller is selected.</span></span> <span data-ttu-id="73dd6-287">Это свойство наследуется от [**CIM \_ сксипротоколконтроллер**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="73dd6-287">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>



| <span data-ttu-id="73dd6-288">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-288">Value</span></span>                                                                        | <span data-ttu-id="73dd6-289">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-289">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="73dd6-290"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-290"><dt>0</dt></span></span> </dl> | <span data-ttu-id="73dd6-291">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="73dd6-291">Unknown</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73dd6-292">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="73dd6-292">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-293">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-293">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-295">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="73dd6-295">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="73dd6-296">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="73dd6-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73dd6-297">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="73dd6-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="73dd6-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="73dd6-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="73dd6-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="73dd6-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="73dd6-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="73dd6-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="73dd6-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="73dd6-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="73dd6-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="73dd6-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="73dd6-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="73dd6-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="73dd6-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="73dd6-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="73dd6-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="73dd6-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="73dd6-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="73dd6-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="73dd6-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="73dd6-317">)</span><span class="sxs-lookup"><span data-stu-id="73dd6-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73dd6-318">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="73dd6-318">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-319">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="73dd6-319">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-321">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="73dd6-321">The current status of the object.</span></span> <span data-ttu-id="73dd6-322">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="73dd6-323">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-323">Value</span></span>                                                                            | <span data-ttu-id="73dd6-324">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-324">Meaning</span></span>       |
|----------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="73dd6-325"><dt>открыт</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-325"><dt>{ 2 }</dt></span></span> </dl> |               |
| <dl> <span data-ttu-id="73dd6-326"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-326"><dt>2</dt></span></span> </dl>     | <span data-ttu-id="73dd6-327">ОК</span><span class="sxs-lookup"><span data-stu-id="73dd6-327">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73dd6-328">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="73dd6-328">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-331">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="73dd6-331">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="73dd6-332">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="73dd6-332">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="73dd6-333">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73dd6-333">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-334">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="73dd6-334">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-335">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="73dd6-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-337">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="73dd6-337">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="73dd6-338">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="73dd6-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-339">**осернамеформат**</span><span class="sxs-lookup"><span data-stu-id="73dd6-339">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-342">Строка, описывающая способ идентификации контроллера протокола, если **намеформат** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="73dd6-342">A string that describes how the protocol controller is identified when the **NameFormat** is 1 (Other).</span></span> <span data-ttu-id="73dd6-343">Это свойство наследуется от [**CIM \_ сксипротоколконтроллер**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="73dd6-343">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-344">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="73dd6-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-345">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="73dd6-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-347">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="73dd6-347">The power management capabilities of the device.</span></span> <span data-ttu-id="73dd6-348">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-349">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="73dd6-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-350">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73dd6-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-352">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="73dd6-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="73dd6-353">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-354">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="73dd6-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-355">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73dd6-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-357">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="73dd6-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="73dd6-358">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-359">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="73dd6-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-360">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-362">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="73dd6-362">Provides high level status information.</span></span> <span data-ttu-id="73dd6-363">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="73dd6-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="73dd6-364">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="73dd6-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73dd6-365">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73dd6-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="73dd6-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="73dd6-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-367"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="73dd6-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="73dd6-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="73dd6-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="73dd6-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="73dd6-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="73dd6-372">)</span><span class="sxs-lookup"><span data-stu-id="73dd6-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73dd6-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="73dd6-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-374">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-376">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="73dd6-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="73dd6-377">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="73dd6-377">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="73dd6-378">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="73dd6-378">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="73dd6-379">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73dd6-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="73dd6-380">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-380">Value</span></span>                                                                         | <span data-ttu-id="73dd6-381">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-381">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="73dd6-382"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-382"><dt>12</dt></span></span> </dl> | <span data-ttu-id="73dd6-383">Не применимо</span><span class="sxs-lookup"><span data-stu-id="73dd6-383">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73dd6-384">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="73dd6-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-385">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-386">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-387">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="73dd6-387">The current status of the object.</span></span> <span data-ttu-id="73dd6-388">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-388">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-389">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="73dd6-389">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-390">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="73dd6-390">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-392">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="73dd6-392">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="73dd6-393">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="73dd6-393">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="73dd6-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-395">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-397">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="73dd6-397">The current state of the logical device.</span></span> <span data-ttu-id="73dd6-398">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-399">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="73dd6-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-400">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-401">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-402">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="73dd6-402">The scoping system's creation class name.</span></span> <span data-ttu-id="73dd6-403">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="73dd6-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="73dd6-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-405">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73dd6-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-407">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="73dd6-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="73dd6-408">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="73dd6-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-409">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="73dd6-409">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-410">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73dd6-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-412">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="73dd6-412">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="73dd6-413">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73dd6-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-414">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="73dd6-414">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-415">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73dd6-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-417">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="73dd6-417">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="73dd6-418">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-418">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73dd6-419">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="73dd6-419">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73dd6-420">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73dd6-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73dd6-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73dd6-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73dd6-422">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="73dd6-422">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="73dd6-423">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="73dd6-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73dd6-424">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73dd6-424">Remarks</span></span>

<span data-ttu-id="73dd6-425">Доступ к классу **\_ сксипротоколконтроллер мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="73dd6-425">Access to the **Msvm\_SCSIProtocolController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="73dd6-426">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="73dd6-426">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="73dd6-427">Требования</span><span class="sxs-lookup"><span data-stu-id="73dd6-427">Requirements</span></span>



| <span data-ttu-id="73dd6-428">Требование</span><span class="sxs-lookup"><span data-stu-id="73dd6-428">Requirement</span></span> | <span data-ttu-id="73dd6-429">Значение</span><span class="sxs-lookup"><span data-stu-id="73dd6-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73dd6-430">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73dd6-430">Minimum supported client</span></span><br/> | <span data-ttu-id="73dd6-431">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="73dd6-431">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="73dd6-432">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73dd6-432">Minimum supported server</span></span><br/> | <span data-ttu-id="73dd6-433">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="73dd6-433">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73dd6-434">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="73dd6-434">Namespace</span></span><br/>                | <span data-ttu-id="73dd6-435">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="73dd6-435">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="73dd6-436">MOF</span><span class="sxs-lookup"><span data-stu-id="73dd6-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73dd6-437"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="73dd6-438">DLL</span><span class="sxs-lookup"><span data-stu-id="73dd6-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73dd6-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="73dd6-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="73dd6-440">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73dd6-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73dd6-441">**\_СКСИПРОТОКОЛКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="73dd6-441">**CIM\_SCSIProtocolController**</span></span>](cim-scsiprotocolcontroller.md)
</dt> <dt>

[<span data-ttu-id="73dd6-442">**\_СКСИПРОТОКОЛКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="73dd6-442">**CIM\_SCSIProtocolController**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)
</dt> <dt>

[<span data-ttu-id="73dd6-443">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="73dd6-443">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

