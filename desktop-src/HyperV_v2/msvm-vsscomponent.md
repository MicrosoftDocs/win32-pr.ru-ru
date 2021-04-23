---
description: Представляет состояние службы служба теневого копирования томов (VSS), которая реализует инициатор запроса VSS в гостевой операционной системе.
ms.assetid: 4DD38929-1E3F-4105-BC1A-B367516F7B6E
title: Класс Msvm_VssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent
- Msvm_VssComponent.SetPowerState
- Msvm_VssComponent.EnableDevice
- Msvm_VssComponent.OnlineDevice
- Msvm_VssComponent.QuiesceDevice
- Msvm_VssComponent.SaveProperties
- Msvm_VssComponent.RestoreProperties
- Msvm_VssComponent.InstanceID
- Msvm_VssComponent.Caption
- Msvm_VssComponent.Description
- Msvm_VssComponent.ElementName
- Msvm_VssComponent.InstallDate
- Msvm_VssComponent.Name
- Msvm_VssComponent.OperationalStatus
- Msvm_VssComponent.StatusDescriptions
- Msvm_VssComponent.Status
- Msvm_VssComponent.HealthState
- Msvm_VssComponent.CommunicationStatus
- Msvm_VssComponent.DetailedStatus
- Msvm_VssComponent.OperatingStatus
- Msvm_VssComponent.PrimaryStatus
- Msvm_VssComponent.EnabledState
- Msvm_VssComponent.OtherEnabledState
- Msvm_VssComponent.RequestedState
- Msvm_VssComponent.EnabledDefault
- Msvm_VssComponent.TimeOfLastStateChange
- Msvm_VssComponent.AvailableRequestedStates
- Msvm_VssComponent.TransitioningToState
- Msvm_VssComponent.SystemCreationClassName
- Msvm_VssComponent.SystemName
- Msvm_VssComponent.CreationClassName
- Msvm_VssComponent.DeviceID
- Msvm_VssComponent.PowerManagementSupported
- Msvm_VssComponent.PowerManagementCapabilities
- Msvm_VssComponent.Availability
- Msvm_VssComponent.StatusInfo
- Msvm_VssComponent.LastErrorCode
- Msvm_VssComponent.ErrorDescription
- Msvm_VssComponent.ErrorCleared
- Msvm_VssComponent.OtherIdentifyingInfo
- Msvm_VssComponent.PowerOnHours
- Msvm_VssComponent.TotalPowerOnHours
- Msvm_VssComponent.IdentifyingDescriptions
- Msvm_VssComponent.AdditionalAvailability
- Msvm_VssComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab4039ce110af9fa023a662c31d1f9962b080e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662217"
---
# <a name="msvm_vsscomponent-class"></a><span data-ttu-id="9be81-103">\_Класс мсвм всскомпонент</span><span class="sxs-lookup"><span data-stu-id="9be81-103">Msvm\_VssComponent class</span></span>

<span data-ttu-id="9be81-104">Представляет состояние службы служба теневого копирования томов (VSS), которая реализует инициатор запроса VSS в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="9be81-104">Represents the state of the Volume Shadow Copy Service (VSS) service, which implements the VSS Requester in the guest operating system.</span></span>

<span data-ttu-id="9be81-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9be81-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be81-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9be81-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "VSS";
  string   Description = "Microsoft VSS Service";
  string   ElementName = "VSS";
  datetime InstallDate;
  string   Name = "VSS";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VssComponent";
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

## <a name="members"></a><span data-ttu-id="9be81-107">Члены</span><span class="sxs-lookup"><span data-stu-id="9be81-107">Members</span></span>

<span data-ttu-id="9be81-108">Класс **мсвм \_ всскомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9be81-108">The **Msvm\_VssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9be81-109">Методы</span><span class="sxs-lookup"><span data-stu-id="9be81-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9be81-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9be81-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9be81-111">Методы</span><span class="sxs-lookup"><span data-stu-id="9be81-111">Methods</span></span>

<span data-ttu-id="9be81-112">Класс **мсвм \_ всскомпонент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9be81-112">The **Msvm\_VssComponent** class has these methods.</span></span>



| <span data-ttu-id="9be81-113">Метод</span><span class="sxs-lookup"><span data-stu-id="9be81-113">Method</span></span>                                                             | <span data-ttu-id="9be81-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9be81-114">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="9be81-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="9be81-115">**EnableDevice**</span></span>                                                   | <span data-ttu-id="9be81-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9be81-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9be81-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="9be81-117">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="9be81-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9be81-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9be81-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="9be81-119">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="9be81-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9be81-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9be81-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="9be81-121">**RequestStateChange**</span></span>](msvm-vsscomponent-requeststatechange.md) | <span data-ttu-id="9be81-122">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="9be81-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="9be81-123">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="9be81-123">**Reset**</span></span>](msvm-vsscomponent-reset.md)                           | <span data-ttu-id="9be81-124">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="9be81-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="9be81-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="9be81-125">**RestoreProperties**</span></span>                                              | <span data-ttu-id="9be81-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9be81-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9be81-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="9be81-127">**SaveProperties**</span></span>                                                 | <span data-ttu-id="9be81-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9be81-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9be81-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9be81-129">**SetPowerState**</span></span>                                                  | <span data-ttu-id="9be81-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9be81-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9be81-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="9be81-131">Properties</span></span>

<span data-ttu-id="9be81-132">Класс **мсвм \_ всскомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9be81-132">The **Msvm\_VssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9be81-133">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="9be81-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9be81-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9be81-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-136">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="9be81-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="9be81-137">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9be81-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="9be81-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-141">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="9be81-141">The primary availability and status of the device.</span></span> <span data-ttu-id="9be81-142">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9be81-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="9be81-143">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-143">Value</span></span>                                                                        | <span data-ttu-id="9be81-144">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9be81-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="9be81-146">Не применимо</span><span class="sxs-lookup"><span data-stu-id="9be81-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9be81-147">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="9be81-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-148">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9be81-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9be81-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-150">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9be81-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9be81-151">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9be81-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-152">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9be81-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-155">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9be81-155">A short description of the object.</span></span> <span data-ttu-id="9be81-156">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-157">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="9be81-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-158">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-160">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="9be81-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9be81-161">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9be81-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9be81-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9be81-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9be81-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="9be81-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="9be81-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="9be81-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="9be81-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9be81-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9be81-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9be81-170">)</span><span class="sxs-lookup"><span data-stu-id="9be81-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9be81-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9be81-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-174">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="9be81-174">The scoping system's creation class name.</span></span> <span data-ttu-id="9be81-175">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9be81-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-176">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9be81-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-179">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9be81-179">A description of the object.</span></span> <span data-ttu-id="9be81-180">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9be81-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-182">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-184">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="9be81-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9be81-185">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9be81-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9be81-186">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9be81-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="9be81-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="9be81-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="9be81-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="9be81-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="9be81-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="9be81-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9be81-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9be81-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9be81-195">)</span><span class="sxs-lookup"><span data-stu-id="9be81-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9be81-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9be81-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-199">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9be81-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="9be81-200">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)"унаследовано" и всегда имеет значение "Microsoft:*VMGUID* \\ *GUID*", где *VMGUID* — это свойство **Name** объекта [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , связанного с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="9be81-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9be81-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-204">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="9be81-204">A display name for the object.</span></span> <span data-ttu-id="9be81-205">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-206">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="9be81-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-207">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-209">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 7 (нет значения по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="9be81-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>



| <span data-ttu-id="9be81-210">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-210">Value</span></span>                                                                        | <span data-ttu-id="9be81-211">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-211">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="9be81-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-212"><dt>2</dt></span></span> </dl> | <span data-ttu-id="9be81-213">Активировано</span><span class="sxs-lookup"><span data-stu-id="9be81-213">Enabled</span></span><br/>    |
| <dl> <span data-ttu-id="9be81-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-214"><dt>3</dt></span></span> </dl> | <span data-ttu-id="9be81-215">Выключено</span><span class="sxs-lookup"><span data-stu-id="9be81-215">Disabled</span></span><br/>   |
| <dl> <span data-ttu-id="9be81-216"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-216"><dt>7</dt></span></span> </dl> | <span data-ttu-id="9be81-217">Нет значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9be81-217">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9be81-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9be81-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-219">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-221">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="9be81-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9be81-222">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9be81-222">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9be81-223">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-223">Value</span></span>                                                                        | <span data-ttu-id="9be81-224">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-224">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="9be81-225"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-225"><dt>2</dt></span></span> </dl> | <span data-ttu-id="9be81-226">Активировано</span><span class="sxs-lookup"><span data-stu-id="9be81-226">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="9be81-227"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-227"><dt>3</dt></span></span> </dl> | <span data-ttu-id="9be81-228">Выключено</span><span class="sxs-lookup"><span data-stu-id="9be81-228">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9be81-229">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="9be81-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-230">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9be81-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-232">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="9be81-232">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="9be81-233">Это свойство наследуется от [**CIM \_ , но**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9be81-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-237">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="9be81-237">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="9be81-238">Это свойство наследуется от [**CIM \_ , но**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9be81-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-240">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-242">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="9be81-242">The current health of the element.</span></span> <span data-ttu-id="9be81-243">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="9be81-243">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9be81-244">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="9be81-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9be81-245">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="9be81-246">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-246">Value</span></span>                                                                        | <span data-ttu-id="9be81-247">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-247">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="9be81-248"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-248"><dt>5</dt></span></span> </dl> | <span data-ttu-id="9be81-249">ОК</span><span class="sxs-lookup"><span data-stu-id="9be81-249">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9be81-250">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9be81-250">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-251">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9be81-251">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9be81-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-253">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="9be81-253">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="9be81-254">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-255">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9be81-255">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-256">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9be81-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-258">Дата и время установки службы интеграции в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="9be81-258">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="9be81-259">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-260">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9be81-260">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9be81-263">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="9be81-263">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9be81-264">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="9be81-264">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9be81-265">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-265">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-266">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="9be81-266">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-267">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9be81-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-269">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="9be81-269">The last error code reported by the logical device.</span></span> <span data-ttu-id="9be81-270">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-271">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="9be81-271">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-272">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9be81-272">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-274">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9be81-274">This property has been deprecated.</span></span> <span data-ttu-id="9be81-275">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9be81-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-276">**Name**</span><span class="sxs-lookup"><span data-stu-id="9be81-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-277">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-279">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="9be81-279">The label by which the object is known.</span></span> <span data-ttu-id="9be81-280">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-281">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="9be81-281">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-282">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-284">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9be81-284">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9be81-285">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9be81-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9be81-286">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9be81-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9be81-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="9be81-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="9be81-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="9be81-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="9be81-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="9be81-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="9be81-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="9be81-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="9be81-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="9be81-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="9be81-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="9be81-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="9be81-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="9be81-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="9be81-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="9be81-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="9be81-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9be81-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9be81-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9be81-306">)</span><span class="sxs-lookup"><span data-stu-id="9be81-306">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9be81-307">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9be81-307">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-308">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9be81-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9be81-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-310">Текущее состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="9be81-310">The current status of the element.</span></span> <span data-ttu-id="9be81-311">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="9be81-312">Ниже приведены возможные значения для  \[ \] значения свойства OperationalStatus 0.</span><span class="sxs-lookup"><span data-stu-id="9be81-312">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="9be81-313">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-313">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="9be81-314">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-314">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9be81-315"><dt>открыт</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-315"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="9be81-316"><dt>**ОК**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-316"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="9be81-317">Служба работает нормально.</span><span class="sxs-lookup"><span data-stu-id="9be81-317">The service is operating normally.</span></span> <span data-ttu-id="9be81-318"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9be81-318">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="9be81-319"><dt>**Снижение уровня работоспособности**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-319"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="9be81-320">Служба работает нормально, но Гостевая служба согласовала совместимую версию протокола связи.</span><span class="sxs-lookup"><span data-stu-id="9be81-320">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="9be81-321"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9be81-321">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="9be81-322"><dt>**Неустранимая ошибка**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-322"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="9be81-323">Гостевая версия не поддерживает совместимую версию протокола.</span><span class="sxs-lookup"><span data-stu-id="9be81-323">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="9be81-324"> \[ Значения свойств OperationalStatus 1 \] и **статусдескриптионс** \[ 1 \] могут содержать дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9be81-324">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="9be81-325"><dt>**Нет контакта**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-325"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="9be81-326">Гостевая служба не установлена или еще не подключена.</span><span class="sxs-lookup"><span data-stu-id="9be81-326">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="9be81-327"><dt>**Потеря связи**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-327"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="9be81-328">Гостевая служба больше не отвечает в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="9be81-328">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="9be81-329">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="9be81-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-332">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="9be81-332">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9be81-333">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="9be81-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9be81-334">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9be81-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9be81-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-336">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9be81-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9be81-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-338">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9be81-338">Additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="9be81-339">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9be81-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-340">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="9be81-340">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-341">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9be81-341">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9be81-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-343">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="9be81-343">The power management capabilities of the device.</span></span> <span data-ttu-id="9be81-344">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-345">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="9be81-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-346">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9be81-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-348">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="9be81-348">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="9be81-349">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-350">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="9be81-350">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-351">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9be81-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-353">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="9be81-353">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="9be81-354">Это свойство наследуется от [**CIM \_ , но**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-355">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="9be81-355">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-356">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-358">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="9be81-358">Provides high level status information.</span></span> <span data-ttu-id="9be81-359">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="9be81-359">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9be81-360">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9be81-360">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9be81-361">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9be81-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9be81-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-363"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="9be81-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="9be81-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="9be81-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9be81-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9be81-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9be81-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9be81-368">)</span><span class="sxs-lookup"><span data-stu-id="9be81-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9be81-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9be81-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-370">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-372">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="9be81-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="9be81-373">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9be81-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9be81-374">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-374">Value</span></span>                                                                         | <span data-ttu-id="9be81-375">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9be81-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="9be81-377">Не применимо</span><span class="sxs-lookup"><span data-stu-id="9be81-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9be81-378">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9be81-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-381">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9be81-381">A string that specifies the current status of the object.</span></span> <span data-ttu-id="9be81-382">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) , но не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-383">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="9be81-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-384">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9be81-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9be81-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-386">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9be81-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9be81-387">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9be81-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9be81-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-389">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-391">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9be81-391">The current state of the logical device.</span></span> <span data-ttu-id="9be81-392">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-393">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="9be81-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-394">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-396">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="9be81-396">The scoping system's creation class name.</span></span> <span data-ttu-id="9be81-397">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9be81-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9be81-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-399">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9be81-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-401">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="9be81-401">The scoping system's name.</span></span> <span data-ttu-id="9be81-402">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9be81-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9be81-403">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="9be81-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-404">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9be81-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-406">Дата или время последнего изменения **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="9be81-406">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="9be81-407">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9be81-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-408">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="9be81-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-409">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9be81-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-411">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="9be81-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="9be81-412">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9be81-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9be81-413">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="9be81-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be81-414">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9be81-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9be81-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9be81-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9be81-416">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="9be81-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9be81-417">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9be81-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9be81-418">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-418">Value</span></span>                                                                         | <span data-ttu-id="9be81-419">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-419">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="9be81-420"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-420"><dt>12</dt></span></span> </dl> | <span data-ttu-id="9be81-421">Не применимо</span><span class="sxs-lookup"><span data-stu-id="9be81-421">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9be81-422">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9be81-422">Remarks</span></span>

<span data-ttu-id="9be81-423">Доступ к классу **\_ всскомпонент мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="9be81-423">Access to the **Msvm\_VssComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9be81-424">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9be81-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9be81-425">Требования</span><span class="sxs-lookup"><span data-stu-id="9be81-425">Requirements</span></span>



| <span data-ttu-id="9be81-426">Требование</span><span class="sxs-lookup"><span data-stu-id="9be81-426">Requirement</span></span> | <span data-ttu-id="9be81-427">Значение</span><span class="sxs-lookup"><span data-stu-id="9be81-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9be81-428">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9be81-428">Minimum supported client</span></span><br/> | <span data-ttu-id="9be81-429">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9be81-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9be81-430">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9be81-430">Minimum supported server</span></span><br/> | <span data-ttu-id="9be81-431">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9be81-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9be81-432">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9be81-432">Namespace</span></span><br/>                | <span data-ttu-id="9be81-433">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9be81-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9be81-434">MOF</span><span class="sxs-lookup"><span data-stu-id="9be81-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9be81-435"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9be81-436">DLL</span><span class="sxs-lookup"><span data-stu-id="9be81-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9be81-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9be81-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9be81-438">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9be81-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be81-439">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="9be81-439">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="9be81-440">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="9be81-440">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

