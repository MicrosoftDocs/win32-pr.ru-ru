---
description: Представляет состояние службы обмена ключами и значениями, которая предоставляет механизм обмена данными между виртуальной машиной и операционной системой, работающей в операционной системе управления.
ms.assetid: AA68BC74-A919-4029-B703-E08F00449F20
title: Класс Msvm_KvpExchangeComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponent
- Msvm_KvpExchangeComponent.SetPowerState
- Msvm_KvpExchangeComponent.EnableDevice
- Msvm_KvpExchangeComponent.OnlineDevice
- Msvm_KvpExchangeComponent.QuiesceDevice
- Msvm_KvpExchangeComponent.SaveProperties
- Msvm_KvpExchangeComponent.RestoreProperties
- Msvm_KvpExchangeComponent.InstanceID
- Msvm_KvpExchangeComponent.Caption
- Msvm_KvpExchangeComponent.Description
- Msvm_KvpExchangeComponent.ElementName
- Msvm_KvpExchangeComponent.InstallDate
- Msvm_KvpExchangeComponent.Name
- Msvm_KvpExchangeComponent.OperationalStatus
- Msvm_KvpExchangeComponent.StatusDescriptions
- Msvm_KvpExchangeComponent.Status
- Msvm_KvpExchangeComponent.HealthState
- Msvm_KvpExchangeComponent.CommunicationStatus
- Msvm_KvpExchangeComponent.DetailedStatus
- Msvm_KvpExchangeComponent.OperatingStatus
- Msvm_KvpExchangeComponent.PrimaryStatus
- Msvm_KvpExchangeComponent.EnabledState
- Msvm_KvpExchangeComponent.OtherEnabledState
- Msvm_KvpExchangeComponent.RequestedState
- Msvm_KvpExchangeComponent.EnabledDefault
- Msvm_KvpExchangeComponent.TimeOfLastStateChange
- Msvm_KvpExchangeComponent.AvailableRequestedStates
- Msvm_KvpExchangeComponent.TransitioningToState
- Msvm_KvpExchangeComponent.SystemCreationClassName
- Msvm_KvpExchangeComponent.SystemName
- Msvm_KvpExchangeComponent.CreationClassName
- Msvm_KvpExchangeComponent.DeviceID
- Msvm_KvpExchangeComponent.PowerManagementSupported
- Msvm_KvpExchangeComponent.PowerManagementCapabilities
- Msvm_KvpExchangeComponent.Availability
- Msvm_KvpExchangeComponent.StatusInfo
- Msvm_KvpExchangeComponent.LastErrorCode
- Msvm_KvpExchangeComponent.ErrorDescription
- Msvm_KvpExchangeComponent.ErrorCleared
- Msvm_KvpExchangeComponent.OtherIdentifyingInfo
- Msvm_KvpExchangeComponent.PowerOnHours
- Msvm_KvpExchangeComponent.TotalPowerOnHours
- Msvm_KvpExchangeComponent.IdentifyingDescriptions
- Msvm_KvpExchangeComponent.AdditionalAvailability
- Msvm_KvpExchangeComponent.MaxQuiesceTime
- Msvm_KvpExchangeComponent.GuestExchangeItems
- Msvm_KvpExchangeComponent.GuestIntrinsicExchangeItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3aa7f269d24c284eef3ad2c519f5fdbf48513a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913131"
---
# <a name="msvm_kvpexchangecomponent-class"></a><span data-ttu-id="dc09d-103">\_Класс мсвм квпексчанжекомпонент</span><span class="sxs-lookup"><span data-stu-id="dc09d-103">Msvm\_KvpExchangeComponent class</span></span>

<span data-ttu-id="dc09d-104">Представляет состояние службы обмена ключами и значениями, которая предоставляет механизм обмена данными между виртуальной машиной и операционной системой, работающей в операционной системе управления.</span><span class="sxs-lookup"><span data-stu-id="dc09d-104">Represents the state of the key/value pair exchange service, which provides a mechanism to exchange data between the virtual machine and the operating system running on the management operating system.</span></span>

<span data-ttu-id="dc09d-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="dc09d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc09d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc09d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Key-Value Pair Exchange";
  string   Description = "Microsoft Key-Value Pair Exchange Service";
  string   ElementName = "Key-Value pair Exchange";
  datetime InstallDate;
  string   Name = "Key-Value Pair Exchange";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_KvpExchangeComponent";
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
  string   GuestExchangeItems[];
  string   GuestIntrinsicExchangeItems[];
};
```

## <a name="members"></a><span data-ttu-id="dc09d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="dc09d-107">Members</span></span>

<span data-ttu-id="dc09d-108">Класс **мсвм \_ квпексчанжекомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dc09d-108">The **Msvm\_KvpExchangeComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="dc09d-109">Методы</span><span class="sxs-lookup"><span data-stu-id="dc09d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="dc09d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc09d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dc09d-111">Методы</span><span class="sxs-lookup"><span data-stu-id="dc09d-111">Methods</span></span>

<span data-ttu-id="dc09d-112">Класс **мсвм \_ квпексчанжекомпонент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dc09d-112">The **Msvm\_KvpExchangeComponent** class has these methods.</span></span>



| <span data-ttu-id="dc09d-113">Метод</span><span class="sxs-lookup"><span data-stu-id="dc09d-113">Method</span></span>                                                                     | <span data-ttu-id="dc09d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="dc09d-114">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="dc09d-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="dc09d-115">**EnableDevice**</span></span>                                                           | <span data-ttu-id="dc09d-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc09d-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="dc09d-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="dc09d-117">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="dc09d-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc09d-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="dc09d-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="dc09d-119">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="dc09d-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc09d-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="dc09d-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="dc09d-121">**RequestStateChange**</span></span>](msvm-kvpexchangecomponent-requeststatechange.md) | <span data-ttu-id="dc09d-122">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="dc09d-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="dc09d-123">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="dc09d-123">**Reset**</span></span>](msvm-kvpexchangecomponent-reset.md)                           | <span data-ttu-id="dc09d-124">Сбрасывает компонент.</span><span class="sxs-lookup"><span data-stu-id="dc09d-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="dc09d-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="dc09d-125">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="dc09d-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc09d-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="dc09d-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="dc09d-127">**SaveProperties**</span></span>                                                         | <span data-ttu-id="dc09d-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc09d-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="dc09d-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dc09d-129">**SetPowerState**</span></span>                                                          | <span data-ttu-id="dc09d-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc09d-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dc09d-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc09d-131">Properties</span></span>

<span data-ttu-id="dc09d-132">Класс **мсвм \_ квпексчанжекомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dc09d-132">The **Msvm\_KvpExchangeComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc09d-133">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="dc09d-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dc09d-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-136">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="dc09d-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="dc09d-137">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc09d-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="dc09d-138">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-138">Value</span></span>                                                                            | <span data-ttu-id="dc09d-139">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="dc09d-140"><dt>1-6</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="dc09d-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="dc09d-142">Не применимо</span><span class="sxs-lookup"><span data-stu-id="dc09d-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dc09d-143">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="dc09d-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-146">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="dc09d-146">The primary availability and status of the device.</span></span> <span data-ttu-id="dc09d-147">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc09d-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="dc09d-148">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-148">Value</span></span>                                                                        | <span data-ttu-id="dc09d-149">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="dc09d-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="dc09d-151">Не применимо</span><span class="sxs-lookup"><span data-stu-id="dc09d-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dc09d-152">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="dc09d-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-153">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dc09d-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-155">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dc09d-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="dc09d-156">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-157">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dc09d-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-160">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dc09d-160">A short description of the object.</span></span> <span data-ttu-id="dc09d-161">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-162">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="dc09d-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-163">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-165">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="dc09d-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="dc09d-166">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="dc09d-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dc09d-167">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dc09d-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dc09d-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="dc09d-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="dc09d-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="dc09d-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="dc09d-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="dc09d-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dc09d-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dc09d-175">)</span><span class="sxs-lookup"><span data-stu-id="dc09d-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dc09d-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc09d-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-179">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="dc09d-179">The scoping system's creation class name.</span></span> <span data-ttu-id="dc09d-180">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc09d-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-181">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dc09d-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-184">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dc09d-184">A description of the object.</span></span> <span data-ttu-id="dc09d-185">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="dc09d-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-187">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-189">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="dc09d-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="dc09d-190">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="dc09d-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dc09d-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dc09d-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="dc09d-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="dc09d-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="dc09d-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="dc09d-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="dc09d-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="dc09d-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="dc09d-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dc09d-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dc09d-200">)</span><span class="sxs-lookup"><span data-stu-id="dc09d-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dc09d-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dc09d-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-204">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dc09d-204">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="dc09d-205">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc09d-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dc09d-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-209">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="dc09d-209">A display name for the object.</span></span> <span data-ttu-id="dc09d-210">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-211">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="dc09d-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-212">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-214">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc09d-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="dc09d-215">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-215">Value</span></span>                                                                        | <span data-ttu-id="dc09d-216">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-216">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="dc09d-217"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-217"><dt>7</dt></span></span> </dl> | <span data-ttu-id="dc09d-218">Нет значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc09d-218">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dc09d-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="dc09d-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-220">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-222">Включенное состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="dc09d-222">The enabled state of the element.</span></span> <span data-ttu-id="dc09d-223">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc09d-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="dc09d-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="dc09d-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="dc09d-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dc09d-226">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="dc09d-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-227">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dc09d-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-229">Указывает, что сообщение об ошибке в свойстве **ластерроркоде** теперь отключено.</span><span class="sxs-lookup"><span data-stu-id="dc09d-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="dc09d-230">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dc09d-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-234">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="dc09d-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="dc09d-235">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-236">**гуестексчанжеитемс**</span><span class="sxs-lookup"><span data-stu-id="dc09d-236">**GuestExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-237">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dc09d-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-239">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), **Хипервембеддединстанце** ("мсвм \_ квпексчанжедатаитем")</span><span class="sxs-lookup"><span data-stu-id="dc09d-239">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-240">Массив внедренных экземпляров [**мсвм \_ квпексчанжедатаитем**](msvm-kvpexchangedataitem.md) , которые содержат набор пар "ключ-значение", которые службы, работающие в гостевой операционной системе, были отправлены для доступа внешним клиентам.</span><span class="sxs-lookup"><span data-stu-id="dc09d-240">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that services running within the guest operating system have pushed up to be available for access by external clients.</span></span> <span data-ttu-id="dc09d-241">Этот массив не будет содержать встроенные элементы, которые напрямую передаются службой Integration Services.</span><span class="sxs-lookup"><span data-stu-id="dc09d-241">This array will not contain any intrinsic items that are pushed by the integration service directly.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-242">**гуестинтринсицексчанжеитемс**</span><span class="sxs-lookup"><span data-stu-id="dc09d-242">**GuestIntrinsicExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-243">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dc09d-243">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-245">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), **Хипервембеддединстанце** ("мсвм \_ квпексчанжедатаитем")</span><span class="sxs-lookup"><span data-stu-id="dc09d-245">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-246">Массив внедренных экземпляров [**мсвм \_ квпексчанжедатаитем**](msvm-kvpexchangedataitem.md) , содержащих набор пар "ключ-значение", которые гостевая операционная система настроила на доступ внешним клиентам.</span><span class="sxs-lookup"><span data-stu-id="dc09d-246">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that the guest operating system has pushed up to be available for access by external clients.</span></span> <span data-ttu-id="dc09d-247">Этот массив не будет содержать элементы данных, отправленные другими службами, работающими в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="dc09d-247">This array will not contain any data items pushed by other services running within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-248">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="dc09d-248">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-249">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-249">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-251">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="dc09d-251">The current health of the element.</span></span> <span data-ttu-id="dc09d-252">Это выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="dc09d-252">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="dc09d-253">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="dc09d-253">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="dc09d-254">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-255">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dc09d-255">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-256">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dc09d-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-258">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="dc09d-258">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="dc09d-259">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-259">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-260">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dc09d-260">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-261">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc09d-261">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-263">Дата и время установки службы интеграции в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="dc09d-263">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="dc09d-264">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-264">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-265">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dc09d-265">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-266">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-268">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="dc09d-268">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-269">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="dc09d-269">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dc09d-270">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-271">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="dc09d-271">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-272">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc09d-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-274">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="dc09d-274">The last error code reported by the logical device.</span></span> <span data-ttu-id="dc09d-275">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-276">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="dc09d-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-277">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc09d-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-279">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-279">This property has been deprecated.</span></span> <span data-ttu-id="dc09d-280">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc09d-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-281">**Name**</span><span class="sxs-lookup"><span data-stu-id="dc09d-281">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-284">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="dc09d-284">The label by which the object is known.</span></span> <span data-ttu-id="dc09d-285">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-286">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="dc09d-286">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-287">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-289">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="dc09d-289">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="dc09d-290">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="dc09d-290">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dc09d-291">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dc09d-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dc09d-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="dc09d-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="dc09d-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="dc09d-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="dc09d-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="dc09d-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="dc09d-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="dc09d-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="dc09d-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="dc09d-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="dc09d-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="dc09d-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="dc09d-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="dc09d-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="dc09d-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="dc09d-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="dc09d-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="dc09d-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dc09d-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dc09d-311">)</span><span class="sxs-lookup"><span data-stu-id="dc09d-311">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dc09d-312">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="dc09d-312">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-313">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dc09d-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-315">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="dc09d-315">The current status of the element.</span></span> <span data-ttu-id="dc09d-316">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="dc09d-317">Ниже приведены возможные значения для  \[ \] значения свойства OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="dc09d-317">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="dc09d-318">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-318">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="dc09d-319">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-319">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="dc09d-320"><dt>**ОК**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-320"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="dc09d-321">Служба работает нормально.</span><span class="sxs-lookup"><span data-stu-id="dc09d-321">The service is operating normally.</span></span> <span data-ttu-id="dc09d-322"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="dc09d-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="dc09d-323"><dt>**Снижение уровня работоспособности**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-323"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="dc09d-324">Служба работает нормально, но Гостевая служба согласовала совместимую версию протокола связи.</span><span class="sxs-lookup"><span data-stu-id="dc09d-324">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="dc09d-325"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="dc09d-325">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="dc09d-326"><dt>**Неустранимая ошибка**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-326"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="dc09d-327">Гостевая версия не поддерживает совместимую версию протокола.</span><span class="sxs-lookup"><span data-stu-id="dc09d-327">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="dc09d-328"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="dc09d-328">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="dc09d-329"><dt>**Нет контакта**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-329"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="dc09d-330">Гостевая служба не установлена или еще не подключена.</span><span class="sxs-lookup"><span data-stu-id="dc09d-330">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="dc09d-331"><dt>**Потеря связи**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-331"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="dc09d-332">Гостевая служба больше не отвечает в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="dc09d-332">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="dc09d-333">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="dc09d-333">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-336">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="dc09d-336">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="dc09d-337">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="dc09d-337">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="dc09d-338">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc09d-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-339">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="dc09d-339">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-340">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dc09d-340">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-342">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dc09d-342">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="dc09d-343">Это свойство наследуется от CIM с параметром и всегда имеет значение **null**. [**\_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)</span><span class="sxs-lookup"><span data-stu-id="dc09d-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-344">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="dc09d-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-345">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dc09d-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-347">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="dc09d-347">The power management capabilities of the device.</span></span> <span data-ttu-id="dc09d-348">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-349">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="dc09d-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-350">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dc09d-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-352">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="dc09d-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="dc09d-353">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-354">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="dc09d-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-355">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc09d-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-357">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="dc09d-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="dc09d-358">Это свойство наследуется от [**CIM \_ , но**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-359">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="dc09d-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-360">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-362">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="dc09d-362">Provides high level status information.</span></span> <span data-ttu-id="dc09d-363">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="dc09d-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="dc09d-364">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="dc09d-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dc09d-365">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dc09d-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dc09d-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-367"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="dc09d-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="dc09d-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="dc09d-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="dc09d-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dc09d-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dc09d-372">)</span><span class="sxs-lookup"><span data-stu-id="dc09d-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dc09d-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="dc09d-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-374">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-376">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="dc09d-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="dc09d-377">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc09d-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="dc09d-378">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-378">Value</span></span>                                                                         | <span data-ttu-id="dc09d-379">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="dc09d-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="dc09d-381">Не применимо</span><span class="sxs-lookup"><span data-stu-id="dc09d-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dc09d-382">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="dc09d-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-383">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-385">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="dc09d-385">The current status of the object.</span></span> <span data-ttu-id="dc09d-386">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-387">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="dc09d-387">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-388">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dc09d-388">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-390">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="dc09d-390">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="dc09d-391">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dc09d-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-392">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dc09d-392">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-393">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-395">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dc09d-395">The current state of the logical device.</span></span> <span data-ttu-id="dc09d-396">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-397">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="dc09d-397">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-398">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-400">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="dc09d-400">The scoping system's creation class name.</span></span> <span data-ttu-id="dc09d-401">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc09d-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dc09d-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc09d-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-405">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="dc09d-405">The scoping system's name.</span></span> <span data-ttu-id="dc09d-406">Это значение соответствует значению свойства [**Name**](msvm-computersystem.md) класса **мсвм \_ ComputerSystem** для виртуальной машины с областями.</span><span class="sxs-lookup"><span data-stu-id="dc09d-406">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="dc09d-407">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc09d-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-408">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="dc09d-408">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-409">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc09d-409">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-411">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="dc09d-411">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="dc09d-412">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-413">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="dc09d-413">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-414">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc09d-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-416">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="dc09d-416">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="dc09d-417">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-417">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dc09d-418">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="dc09d-418">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc09d-419">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc09d-419">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc09d-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc09d-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc09d-421">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="dc09d-421">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="dc09d-422">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="dc09d-422">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc09d-423">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc09d-423">Remarks</span></span>

<span data-ttu-id="dc09d-424">Доступ к классу **\_ квпексчанжекомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="dc09d-424">Access to the **Msvm\_KvpExchangeComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dc09d-425">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dc09d-425">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc09d-426">Требования</span><span class="sxs-lookup"><span data-stu-id="dc09d-426">Requirements</span></span>



| <span data-ttu-id="dc09d-427">Требование</span><span class="sxs-lookup"><span data-stu-id="dc09d-427">Requirement</span></span> | <span data-ttu-id="dc09d-428">Значение</span><span class="sxs-lookup"><span data-stu-id="dc09d-428">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc09d-429">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc09d-429">Minimum supported client</span></span><br/> | <span data-ttu-id="dc09d-430">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dc09d-430">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dc09d-431">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc09d-431">Minimum supported server</span></span><br/> | <span data-ttu-id="dc09d-432">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dc09d-432">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc09d-433">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dc09d-433">Namespace</span></span><br/>                | <span data-ttu-id="dc09d-434">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dc09d-434">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dc09d-435">MOF</span><span class="sxs-lookup"><span data-stu-id="dc09d-435">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc09d-436"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-436"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc09d-437">DLL</span><span class="sxs-lookup"><span data-stu-id="dc09d-437">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc09d-438"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc09d-438"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc09d-439">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc09d-439">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc09d-440">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="dc09d-440">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="dc09d-441">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="dc09d-441">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

