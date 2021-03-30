---
description: Описывает физический модуль обработки трехмерных графики (GPU).
ms.assetid: 24e3d141-cbfe-4d40-907c-9a467c586c46
title: Класс Msvm_Physical3dGraphicsProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Physical3dGraphicsProcessor
- Msvm_Physical3dGraphicsProcessor.RequestStateChange
- Msvm_Physical3dGraphicsProcessor.SetPowerState
- Msvm_Physical3dGraphicsProcessor.Reset
- Msvm_Physical3dGraphicsProcessor.EnableDevice
- Msvm_Physical3dGraphicsProcessor.OnlineDevice
- Msvm_Physical3dGraphicsProcessor.QuiesceDevice
- Msvm_Physical3dGraphicsProcessor.SaveProperties
- Msvm_Physical3dGraphicsProcessor.RestoreProperties
- Msvm_Physical3dGraphicsProcessor.InstanceID
- Msvm_Physical3dGraphicsProcessor.Caption
- Msvm_Physical3dGraphicsProcessor.Description
- Msvm_Physical3dGraphicsProcessor.ElementName
- Msvm_Physical3dGraphicsProcessor.InstallDate
- Msvm_Physical3dGraphicsProcessor.Name
- Msvm_Physical3dGraphicsProcessor.OperationalStatus
- Msvm_Physical3dGraphicsProcessor.StatusDescriptions
- Msvm_Physical3dGraphicsProcessor.Status
- Msvm_Physical3dGraphicsProcessor.HealthState
- Msvm_Physical3dGraphicsProcessor.CommunicationStatus
- Msvm_Physical3dGraphicsProcessor.DetailedStatus
- Msvm_Physical3dGraphicsProcessor.OperatingStatus
- Msvm_Physical3dGraphicsProcessor.PrimaryStatus
- Msvm_Physical3dGraphicsProcessor.EnabledState
- Msvm_Physical3dGraphicsProcessor.OtherEnabledState
- Msvm_Physical3dGraphicsProcessor.RequestedState
- Msvm_Physical3dGraphicsProcessor.EnabledDefault
- Msvm_Physical3dGraphicsProcessor.TimeOfLastStateChange
- Msvm_Physical3dGraphicsProcessor.AvailableRequestedStates
- Msvm_Physical3dGraphicsProcessor.TransitioningToState
- Msvm_Physical3dGraphicsProcessor.SystemCreationClassName
- Msvm_Physical3dGraphicsProcessor.SystemName
- Msvm_Physical3dGraphicsProcessor.CreationClassName
- Msvm_Physical3dGraphicsProcessor.DeviceID
- Msvm_Physical3dGraphicsProcessor.PowerManagementSupported
- Msvm_Physical3dGraphicsProcessor.PowerManagementCapabilities
- Msvm_Physical3dGraphicsProcessor.Availability
- Msvm_Physical3dGraphicsProcessor.StatusInfo
- Msvm_Physical3dGraphicsProcessor.LastErrorCode
- Msvm_Physical3dGraphicsProcessor.ErrorDescription
- Msvm_Physical3dGraphicsProcessor.ErrorCleared
- Msvm_Physical3dGraphicsProcessor.OtherIdentifyingInfo
- Msvm_Physical3dGraphicsProcessor.PowerOnHours
- Msvm_Physical3dGraphicsProcessor.TotalPowerOnHours
- Msvm_Physical3dGraphicsProcessor.IdentifyingDescriptions
- Msvm_Physical3dGraphicsProcessor.AdditionalAvailability
- Msvm_Physical3dGraphicsProcessor.MaxQuiesceTime
- Msvm_Physical3dGraphicsProcessor.EnabledForVirtualization
- Msvm_Physical3dGraphicsProcessor.CompatibleForVirtualization
- Msvm_Physical3dGraphicsProcessor.GPUID
- Msvm_Physical3dGraphicsProcessor.DirectXVersion
- Msvm_Physical3dGraphicsProcessor.PixelShaderVersion
- Msvm_Physical3dGraphicsProcessor.DedicatedVideoMemory
- Msvm_Physical3dGraphicsProcessor.DedicatedSystemMemory
- Msvm_Physical3dGraphicsProcessor.SharedSystemMemory
- Msvm_Physical3dGraphicsProcessor.TotalVideoMemory
- Msvm_Physical3dGraphicsProcessor.AvailableVideoMemory
- Msvm_Physical3dGraphicsProcessor.DriverProvider
- Msvm_Physical3dGraphicsProcessor.DriverDate
- Msvm_Physical3dGraphicsProcessor.DriverInstalled
- Msvm_Physical3dGraphicsProcessor.DriverVersion
- Msvm_Physical3dGraphicsProcessor.DriverModelVersion
- Msvm_Physical3dGraphicsProcessor.Rating
- Msvm_Physical3dGraphicsProcessor.AdapterIndexID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e257fa319b1d1b55562f47c7a3049a694fc27f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817881"
---
# <a name="msvm_physical3dgraphicsprocessor-class"></a><span data-ttu-id="f8372-103">\_Класс мсвм Physical3dGraphicsProcessor</span><span class="sxs-lookup"><span data-stu-id="f8372-103">Msvm\_Physical3dGraphicsProcessor class</span></span>

<span data-ttu-id="f8372-104">Описывает физический модуль обработки трехмерных графики (GPU).</span><span class="sxs-lookup"><span data-stu-id="f8372-104">Describes the physical 3-D graphics processing unit (GPU).</span></span>

<span data-ttu-id="f8372-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f8372-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8372-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8372-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Physical3dGraphicsProcessor : CIM_LogicalDevice
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
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
  Boolean  EnabledForVirtualization;
  Boolean  CompatibleForVirtualization;
  string   GPUID;
  string   DirectXVersion;
  string   PixelShaderVersion;
  uint64   DedicatedVideoMemory;
  uint64   DedicatedSystemMemory;
  uint64   SharedSystemMemory;
  uint64   TotalVideoMemory;
  uint64   AvailableVideoMemory;
  string   DriverProvider;
  datetime DriverDate;
  datetime DriverInstalled;
  string   DriverVersion;
  string   DriverModelVersion;
  uint64   Rating;
  uint64   AdapterIndexID;
};
```

## <a name="members"></a><span data-ttu-id="f8372-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f8372-107">Members</span></span>

<span data-ttu-id="f8372-108">Класс **мсвм \_ Physical3dGraphicsProcessor** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f8372-108">The **Msvm\_Physical3dGraphicsProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="f8372-109">Методы</span><span class="sxs-lookup"><span data-stu-id="f8372-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f8372-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8372-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f8372-111">Методы</span><span class="sxs-lookup"><span data-stu-id="f8372-111">Methods</span></span>

<span data-ttu-id="f8372-112">Класс **мсвм \_ Physical3dGraphicsProcessor** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f8372-112">The **Msvm\_Physical3dGraphicsProcessor** class has these methods.</span></span>



| <span data-ttu-id="f8372-113">Метод</span><span class="sxs-lookup"><span data-stu-id="f8372-113">Method</span></span>                 | <span data-ttu-id="f8372-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f8372-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="f8372-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="f8372-115">**EnableDevice**</span></span>       | <span data-ttu-id="f8372-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8372-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f8372-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="f8372-117">**OnlineDevice**</span></span>       | <span data-ttu-id="f8372-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8372-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f8372-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="f8372-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="f8372-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8372-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f8372-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="f8372-121">**RequestStateChange**</span></span> | <span data-ttu-id="f8372-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8372-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f8372-123">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="f8372-123">**Reset**</span></span>              | <span data-ttu-id="f8372-124">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8372-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f8372-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="f8372-125">**RestoreProperties**</span></span>  | <span data-ttu-id="f8372-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8372-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f8372-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="f8372-127">**SaveProperties**</span></span>     | <span data-ttu-id="f8372-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8372-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f8372-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f8372-129">**SetPowerState**</span></span>      | <span data-ttu-id="f8372-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f8372-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f8372-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8372-131">Properties</span></span>

<span data-ttu-id="f8372-132">Класс **мсвм \_ Physical3dGraphicsProcessor** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f8372-132">The **Msvm\_Physical3dGraphicsProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8372-133">**адаптериндексид**</span><span class="sxs-lookup"><span data-stu-id="f8372-133">**AdapterIndexID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-134">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-136">Указывает идентификатор индекса адаптера, выделенный для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="f8372-136">Specifies the adapter index identifier allocated to this device.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-137">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="f8372-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-138">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f8372-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8372-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-140">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="f8372-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="f8372-141">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-142">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="f8372-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-145">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="f8372-145">The primary availability and status of the device.</span></span> <span data-ttu-id="f8372-146">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-147">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="f8372-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-148">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f8372-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8372-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-150">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f8372-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f8372-151">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f8372-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-152">**аваилаблевидеомемори**</span><span class="sxs-lookup"><span data-stu-id="f8372-152">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-153">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-155">Указывает объем видеопамяти в байтах, доступный GPU.</span><span class="sxs-lookup"><span data-stu-id="f8372-155">Specifies the amount of video memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-156">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f8372-156">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-159">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f8372-159">A short description of the object.</span></span> <span data-ttu-id="f8372-160">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-161">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="f8372-161">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-162">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-164">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="f8372-164">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f8372-165">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f8372-165">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8372-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8372-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f8372-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="f8372-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="f8372-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="f8372-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="f8372-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f8372-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f8372-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8372-174">)</span><span class="sxs-lookup"><span data-stu-id="f8372-174">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8372-175">**компатиблефорвиртуализатион**</span><span class="sxs-lookup"><span data-stu-id="f8372-175">**CompatibleForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-176">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f8372-176">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-178">**значение true** , если совместимо для виртуализации; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f8372-178">**true** if compatible for virtualization; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="f8372-179">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="f8372-179">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="f8372-180">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f8372-180">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-183">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="f8372-183">The scoping system's creation class name.</span></span> <span data-ttu-id="f8372-184">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f8372-184">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-185">**дедикатедсистеммемори**</span><span class="sxs-lookup"><span data-stu-id="f8372-185">**DedicatedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-186">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-188">Указывает объем системной памяти в байтах, выделенной для GPU.</span><span class="sxs-lookup"><span data-stu-id="f8372-188">Specifies the amount of system memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-189">**дедикатедвидеомемори**</span><span class="sxs-lookup"><span data-stu-id="f8372-189">**DedicatedVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-190">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-192">Указывает объем видеопамяти в байтах, выделенной для GPU.</span><span class="sxs-lookup"><span data-stu-id="f8372-192">Specifies the amount of video memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-193">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f8372-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-196">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f8372-196">A description of the object.</span></span> <span data-ttu-id="f8372-197">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-198">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f8372-198">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-199">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-201">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="f8372-201">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f8372-202">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f8372-202">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8372-203">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8372-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="f8372-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="f8372-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="f8372-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="f8372-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="f8372-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="f8372-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f8372-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f8372-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8372-212">)</span><span class="sxs-lookup"><span data-stu-id="f8372-212">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8372-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f8372-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-216">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f8372-216">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="f8372-217">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f8372-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-218">**директксверсион**</span><span class="sxs-lookup"><span data-stu-id="f8372-218">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8372-221">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="f8372-221">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="f8372-222">Указывает виртуализации DirectX, поддерживаемый GPU.</span><span class="sxs-lookup"><span data-stu-id="f8372-222">Specifies the verison of DirectX that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-223">**дривердате**</span><span class="sxs-lookup"><span data-stu-id="f8372-223">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-224">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8372-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-226">Указывает дату сборки драйвера.</span><span class="sxs-lookup"><span data-stu-id="f8372-226">Specifies the driver build date.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-227">**дриверинсталлед**</span><span class="sxs-lookup"><span data-stu-id="f8372-227">**DriverInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-228">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8372-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-230">Указывает дату и время установки драйвера.</span><span class="sxs-lookup"><span data-stu-id="f8372-230">Specifies the date and time that the driver was installed.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-231">**дривермоделверсион**</span><span class="sxs-lookup"><span data-stu-id="f8372-231">**DriverModelVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8372-234">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="f8372-234">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="f8372-235">Указывает версию модели драйвера.</span><span class="sxs-lookup"><span data-stu-id="f8372-235">Specifies the driver model version.</span></span>

> [!Note]  
> <span data-ttu-id="f8372-236">Это свойство было добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="f8372-236">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="f8372-237">**дриверпровидер**</span><span class="sxs-lookup"><span data-stu-id="f8372-237">**DriverProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-238">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8372-240">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="f8372-240">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="f8372-241">Указывает имя поставщика драйвера.</span><span class="sxs-lookup"><span data-stu-id="f8372-241">Specifies the name of the driver provider.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-242">**дриверверсион**</span><span class="sxs-lookup"><span data-stu-id="f8372-242">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8372-245">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="f8372-245">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="f8372-246">Указывает версию драйвера.</span><span class="sxs-lookup"><span data-stu-id="f8372-246">Specifies the driver version.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-247">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f8372-247">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-250">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="f8372-250">A display name for the object.</span></span> <span data-ttu-id="f8372-251">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-252">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="f8372-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-253">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-255">Конфигурация по умолчанию или запуск администратора для свойства **EnabledState** элемента.</span><span class="sxs-lookup"><span data-stu-id="f8372-255">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="f8372-256">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="f8372-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-257">**енабледфорвиртуализатион**</span><span class="sxs-lookup"><span data-stu-id="f8372-257">**EnabledForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-258">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f8372-258">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-260">Указывает, был ли адаптер включен для использования с RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="f8372-260">Specifies whether the adapter has been enabled for use with RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-261">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f8372-261">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-262">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-264">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="f8372-264">The enabled and disabled states of an element.</span></span> <span data-ttu-id="f8372-265">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f8372-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="f8372-266">Значение</span><span class="sxs-lookup"><span data-stu-id="f8372-266">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="f8372-267">Значение</span><span class="sxs-lookup"><span data-stu-id="f8372-267">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="f8372-268"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-268"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="f8372-269">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="f8372-269">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="f8372-270"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-270"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="f8372-271"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-271"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="f8372-272">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="f8372-272">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="f8372-273"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-273"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="f8372-274">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="f8372-274">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="f8372-275"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-275"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="f8372-276">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="f8372-276">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="f8372-277"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-277"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="f8372-278">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="f8372-278">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="f8372-279"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-279"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="f8372-280">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="f8372-280">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="f8372-281"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-281"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="f8372-282">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="f8372-282">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="f8372-283"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-283"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="f8372-284">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="f8372-284">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="f8372-285"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-285"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="f8372-286">Элемент включен, но в режиме с ограниченным доступом.</span><span class="sxs-lookup"><span data-stu-id="f8372-286">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="f8372-287">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="f8372-287">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="f8372-288">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="f8372-288">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="f8372-289"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-289"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="f8372-290">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="f8372-290">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="f8372-291">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="f8372-291">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="f8372-292">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="f8372-292">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-293">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f8372-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-295">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="f8372-295">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="f8372-296">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-297">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f8372-297">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-300">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="f8372-300">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="f8372-301">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-302">**GPUID**</span><span class="sxs-lookup"><span data-stu-id="f8372-302">**GPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8372-305">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="f8372-305">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="f8372-306">Содержит идентификатор GPU для адаптера.</span><span class="sxs-lookup"><span data-stu-id="f8372-306">Contains the GPU identifier for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-307">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f8372-307">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-308">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-310">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="f8372-310">The current health of the element.</span></span> <span data-ttu-id="f8372-311">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-312">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f8372-312">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-313">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f8372-313">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f8372-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-315">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="f8372-315">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="f8372-316">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f8372-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-318">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8372-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-320">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="f8372-320">The date and time when the object was installed.</span></span> <span data-ttu-id="f8372-321">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="f8372-321">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="f8372-322">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-323">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f8372-323">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8372-326">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="f8372-326">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f8372-327">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="f8372-327">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f8372-328">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-328">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-329">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="f8372-329">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-330">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8372-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-332">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="f8372-332">The last error code reported by the logical device.</span></span> <span data-ttu-id="f8372-333">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-333">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-334">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="f8372-334">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-335">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-337">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="f8372-337">This property has been deprecated.</span></span> <span data-ttu-id="f8372-338">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-339">**Name**</span><span class="sxs-lookup"><span data-stu-id="f8372-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-342">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f8372-342">The label by which the object is known.</span></span> <span data-ttu-id="f8372-343">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-344">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="f8372-344">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-345">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-347">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f8372-347">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f8372-348">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f8372-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8372-349">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8372-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f8372-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="f8372-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="f8372-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="f8372-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="f8372-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="f8372-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="f8372-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="f8372-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="f8372-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="f8372-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="f8372-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="f8372-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="f8372-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="f8372-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="f8372-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="f8372-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="f8372-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f8372-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f8372-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8372-369">)</span><span class="sxs-lookup"><span data-stu-id="f8372-369">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8372-370">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f8372-370">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-371">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f8372-371">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8372-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-373">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f8372-373">The current statuses of the object.</span></span> <span data-ttu-id="f8372-374">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-375">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="f8372-375">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-378">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="f8372-378">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f8372-379">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="f8372-379">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="f8372-380">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f8372-380">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-381">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f8372-381">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-382">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f8372-382">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f8372-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-384">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f8372-384">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="f8372-385">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-386">**пикселшадерверсион**</span><span class="sxs-lookup"><span data-stu-id="f8372-386">**PixelShaderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-387">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8372-389">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="f8372-389">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="f8372-390">Указывает виртуализации шейдера пикселей, поддерживаемое графическим процессором.</span><span class="sxs-lookup"><span data-stu-id="f8372-390">Specifies the pixel shader verison that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-391">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="f8372-391">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-392">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f8372-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f8372-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-394">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="f8372-394">The power management capabilities of the device.</span></span> <span data-ttu-id="f8372-395">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-396">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="f8372-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-397">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f8372-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-398">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-399">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="f8372-399">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="f8372-400">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-401">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="f8372-401">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-402">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-402">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-404">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="f8372-404">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="f8372-405">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-405">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-406">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="f8372-406">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-407">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-407">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-409">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="f8372-409">Provides high level status information.</span></span> <span data-ttu-id="f8372-410">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="f8372-410">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f8372-411">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="f8372-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f8372-412">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f8372-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f8372-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-414"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="f8372-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="f8372-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="f8372-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f8372-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f8372-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f8372-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f8372-419">)</span><span class="sxs-lookup"><span data-stu-id="f8372-419">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f8372-420">**Оценка**</span><span class="sxs-lookup"><span data-stu-id="f8372-420">**Rating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-421">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8372-423">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения")</span><span class="sxs-lookup"><span data-stu-id="f8372-423">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="f8372-424">Указывает рейтинг GPU RemoteFX для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="f8372-424">Specifies the GPU RemoteFX rating for this device.</span></span> <span data-ttu-id="f8372-425">Это свойство в настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-425">This property is not currently used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-426">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f8372-426">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-427">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-429">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="f8372-429">The last requested or desired state for the element.</span></span> <span data-ttu-id="f8372-430">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="f8372-430">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-431">**шаредсистеммемори**</span><span class="sxs-lookup"><span data-stu-id="f8372-431">**SharedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-432">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-432">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-433">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-434">Указывает объем общей системной памяти в байтах, доступный для GPU.</span><span class="sxs-lookup"><span data-stu-id="f8372-434">Specifies the amount of shared system memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-435">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f8372-435">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-438">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f8372-438">The current status of the object.</span></span> <span data-ttu-id="f8372-439">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-440">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="f8372-440">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-441">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f8372-441">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f8372-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-443">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f8372-443">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f8372-444">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f8372-444">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-445">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f8372-445">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-446">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-448">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f8372-448">The current state of the logical device.</span></span> <span data-ttu-id="f8372-449">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-450">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f8372-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-451">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-452">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-453">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="f8372-453">The scoping system's creation class name.</span></span> <span data-ttu-id="f8372-454">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f8372-454">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-455">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f8372-455">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-456">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f8372-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-458">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="f8372-458">The scoping system's name.</span></span> <span data-ttu-id="f8372-459">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f8372-459">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f8372-460">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="f8372-460">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-461">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8372-461">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-462">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-463">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="f8372-463">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f8372-464">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f8372-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-465">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="f8372-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-466">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-467">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-468">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="f8372-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="f8372-469">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="f8372-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-470">**тоталвидеомемори**</span><span class="sxs-lookup"><span data-stu-id="f8372-470">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-471">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f8372-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-473">Указывает общий объем видеопамяти (в байтах), имеющейся на GPU.</span><span class="sxs-lookup"><span data-stu-id="f8372-473">Specifies the total amount of video memory, in bytes, present on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="f8372-474">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="f8372-474">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8372-475">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8372-475">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8372-476">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8372-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8372-477">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="f8372-477">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f8372-478">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f8372-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8372-479">Требования</span><span class="sxs-lookup"><span data-stu-id="f8372-479">Requirements</span></span>



| <span data-ttu-id="f8372-480">Требование</span><span class="sxs-lookup"><span data-stu-id="f8372-480">Requirement</span></span> | <span data-ttu-id="f8372-481">Значение</span><span class="sxs-lookup"><span data-stu-id="f8372-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8372-482">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8372-482">Minimum supported client</span></span><br/> | <span data-ttu-id="f8372-483">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f8372-483">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f8372-484">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8372-484">Minimum supported server</span></span><br/> | <span data-ttu-id="f8372-485">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8372-485">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f8372-486">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f8372-486">Namespace</span></span><br/>                | <span data-ttu-id="f8372-487">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f8372-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f8372-488">MOF</span><span class="sxs-lookup"><span data-stu-id="f8372-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8372-489"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8372-490">DLL</span><span class="sxs-lookup"><span data-stu-id="f8372-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8372-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f8372-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

