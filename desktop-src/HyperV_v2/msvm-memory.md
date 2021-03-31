---
description: Представляет память, выделенную для виртуальной машины в данный момент.
ms.assetid: 4CAA64FC-5A06-409B-9E92-32DF3F47D5FD
title: Класс Msvm_Memory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory
- Msvm_Memory.SetPowerState
- Msvm_Memory.EnableDevice
- Msvm_Memory.OnlineDevice
- Msvm_Memory.QuiesceDevice
- Msvm_Memory.SaveProperties
- Msvm_Memory.RestoreProperties
- Msvm_Memory.InstanceID
- Msvm_Memory.Caption
- Msvm_Memory.Description
- Msvm_Memory.ElementName
- Msvm_Memory.InstallDate
- Msvm_Memory.OperationalStatus
- Msvm_Memory.StatusDescriptions
- Msvm_Memory.Status
- Msvm_Memory.HealthState
- Msvm_Memory.CommunicationStatus
- Msvm_Memory.DetailedStatus
- Msvm_Memory.OperatingStatus
- Msvm_Memory.PrimaryStatus
- Msvm_Memory.EnabledState
- Msvm_Memory.OtherEnabledState
- Msvm_Memory.RequestedState
- Msvm_Memory.EnabledDefault
- Msvm_Memory.TimeOfLastStateChange
- Msvm_Memory.AvailableRequestedStates
- Msvm_Memory.TransitioningToState
- Msvm_Memory.SystemCreationClassName
- Msvm_Memory.SystemName
- Msvm_Memory.CreationClassName
- Msvm_Memory.DeviceID
- Msvm_Memory.PowerManagementSupported
- Msvm_Memory.PowerManagementCapabilities
- Msvm_Memory.Availability
- Msvm_Memory.StatusInfo
- Msvm_Memory.LastErrorCode
- Msvm_Memory.ErrorDescription
- Msvm_Memory.ErrorCleared
- Msvm_Memory.OtherIdentifyingInfo
- Msvm_Memory.PowerOnHours
- Msvm_Memory.TotalPowerOnHours
- Msvm_Memory.IdentifyingDescriptions
- Msvm_Memory.AdditionalAvailability
- Msvm_Memory.MaxQuiesceTime
- Msvm_Memory.DataOrganization
- Msvm_Memory.Purpose
- Msvm_Memory.Access
- Msvm_Memory.BlockSize
- Msvm_Memory.NumberOfBlocks
- Msvm_Memory.ConsumableBlocks
- Msvm_Memory.IsBasedOnUnderlyingRedundancy
- Msvm_Memory.SequentialAccess
- Msvm_Memory.ExtentStatus
- Msvm_Memory.NoSinglePointOfFailure
- Msvm_Memory.DataRedundancy
- Msvm_Memory.PackageRedundancy
- Msvm_Memory.DeltaReservation
- Msvm_Memory.Primordial
- Msvm_Memory.Name
- Msvm_Memory.NameFormat
- Msvm_Memory.NameNamespace
- Msvm_Memory.OtherNameNamespace
- Msvm_Memory.OtherNameFormat
- Msvm_Memory.Volatile
- Msvm_Memory.ErrorMethodology
- Msvm_Memory.StartingAddress
- Msvm_Memory.EndingAddress
- Msvm_Memory.ErrorInfo
- Msvm_Memory.OtherErrorDescription
- Msvm_Memory.CorrectableError
- Msvm_Memory.ErrorTime
- Msvm_Memory.ErrorAccess
- Msvm_Memory.ErrorTransferSize
- Msvm_Memory.ErrorData
- Msvm_Memory.ErrorDataOrder
- Msvm_Memory.ErrorAddress
- Msvm_Memory.SystemLevelAddress
- Msvm_Memory.ErrorResolution
- Msvm_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ec6b287f3281fd0224e9c2efc39391781bd7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913128"
---
# <a name="msvm_memory-class"></a><span data-ttu-id="e5252-103">\_Класс памяти мсвм</span><span class="sxs-lookup"><span data-stu-id="e5252-103">Msvm\_Memory class</span></span>

<span data-ttu-id="e5252-104">Представляет память, выделенную для виртуальной машины в данный момент.</span><span class="sxs-lookup"><span data-stu-id="e5252-104">Represents the memory currently allocated to a virtual machine.</span></span>

<span data-ttu-id="e5252-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e5252-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5252-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5252-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Memory : CIM_Memory
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
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose = "System Memory";
  uint16   Access = 3;
  uint64   BlockSize = 1048576;
  uint64   NumberOfBlocks;
  uint64   ConsumableBlocks;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = 2;
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 1;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial;
  string   Name = "GUID";
  uint16   NameFormat = 0;
  uint16   NameNamespace = 0;
  string   OtherNameNamespace;
  string   OtherNameFormat;
  boolean  Volatile = True;
  string   ErrorMethodology;
  uint64   StartingAddress = 0;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="e5252-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e5252-107">Members</span></span>

<span data-ttu-id="e5252-108">Класс **\_ памяти мсвм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e5252-108">The **Msvm\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="e5252-109">Методы</span><span class="sxs-lookup"><span data-stu-id="e5252-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e5252-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5252-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e5252-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e5252-111">Methods</span></span>

<span data-ttu-id="e5252-112">Класс **\_ памяти мсвм** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e5252-112">The **Msvm\_Memory** class has these methods.</span></span>



| <span data-ttu-id="e5252-113">Метод</span><span class="sxs-lookup"><span data-stu-id="e5252-113">Method</span></span>                                                       | <span data-ttu-id="e5252-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e5252-114">Description</span></span>                              |
|:-------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e5252-115">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="e5252-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="e5252-116">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e5252-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e5252-117">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="e5252-117">**OnlineDevice**</span></span>                                             | <span data-ttu-id="e5252-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e5252-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e5252-119">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="e5252-119">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="e5252-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e5252-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e5252-121">**Равен**</span><span class="sxs-lookup"><span data-stu-id="e5252-121">**RequestStateChange**</span></span>](msvm-memory-requeststatechange.md) | <span data-ttu-id="e5252-122">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="e5252-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e5252-123">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="e5252-123">**Reset**</span></span>](msvm-memory-reset.md)                           | <span data-ttu-id="e5252-124">Сбрасывает виртуальную память.</span><span class="sxs-lookup"><span data-stu-id="e5252-124">Resets the virtual memory.</span></span><br/>    |
| <span data-ttu-id="e5252-125">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="e5252-125">**RestoreProperties**</span></span>                                        | <span data-ttu-id="e5252-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e5252-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e5252-127">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="e5252-127">**SaveProperties**</span></span>                                           | <span data-ttu-id="e5252-128">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e5252-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e5252-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e5252-129">**SetPowerState**</span></span>                                            | <span data-ttu-id="e5252-130">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e5252-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e5252-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5252-131">Properties</span></span>

<span data-ttu-id="e5252-132">Класс **\_ памяти мсвм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e5252-132">The **Msvm\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5252-133">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="e5252-133">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-136">Описание свойств чтения и записи носителя.</span><span class="sxs-lookup"><span data-stu-id="e5252-136">Describes the read/write properties of the media.</span></span> <span data-ttu-id="e5252-137">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и по умолчанию имеет значение 3 (поддерживается для чтения и записи).</span><span class="sxs-lookup"><span data-stu-id="e5252-137">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to 3 (Read/Write Supported) by default.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-138">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="e5252-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-139">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e5252-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-141">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="e5252-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-142">**аддитионалеррордата**</span><span class="sxs-lookup"><span data-stu-id="e5252-142">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-143">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e5252-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-145">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-145">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-146">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="e5252-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-147">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-149">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5252-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-150">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="e5252-150">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-151">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e5252-151">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-153">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e5252-153">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e5252-154">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e5252-154">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-155">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="e5252-155">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-156">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-158">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="e5252-158">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="e5252-159">Если размер блока переменной, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="e5252-159">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="e5252-160">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите 1 (один).</span><span class="sxs-lookup"><span data-stu-id="e5252-160">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span> <span data-ttu-id="e5252-161">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение 1048576.</span><span class="sxs-lookup"><span data-stu-id="e5252-161">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1048576.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-162">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e5252-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-165">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e5252-165">A short description of the object.</span></span> <span data-ttu-id="e5252-166">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-167">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="e5252-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-170">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="e5252-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e5252-171">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e5252-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5252-172">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e5252-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e5252-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="e5252-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="e5252-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="e5252-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="e5252-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e5252-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e5252-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e5252-180">)</span><span class="sxs-lookup"><span data-stu-id="e5252-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e5252-181">**консумаблеблоккс**</span><span class="sxs-lookup"><span data-stu-id="e5252-181">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-182">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-184">Максимальное количество блоков **, размерностей, доступных** для использования при слоевых экстентах хранения с помощью Ассоциации BasedOn.</span><span class="sxs-lookup"><span data-stu-id="e5252-184">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the BasedOn association.</span></span> <span data-ttu-id="e5252-185">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5252-185">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-186">**корректаблиррор**</span><span class="sxs-lookup"><span data-stu-id="e5252-186">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-187">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5252-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-189">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-189">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e5252-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-191">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-193">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e5252-193">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e5252-194">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5252-194">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-195">**Организация**</span><span class="sxs-lookup"><span data-stu-id="e5252-195">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-196">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-198">Тип используемой организации данных.</span><span class="sxs-lookup"><span data-stu-id="e5252-198">The type of data organization used.</span></span> <span data-ttu-id="e5252-199">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="e5252-199">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-200">**Избыточность**</span><span class="sxs-lookup"><span data-stu-id="e5252-200">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-201">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-203">Количество полных копий данных, которые в настоящее время хранятся.</span><span class="sxs-lookup"><span data-stu-id="e5252-203">The number of complete copies of data that is currently maintained.</span></span> <span data-ttu-id="e5252-204">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="e5252-204">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-205">**делтаресерватион**</span><span class="sxs-lookup"><span data-stu-id="e5252-205">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-206">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e5252-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-208">Текущее значение для разностного резервирования.</span><span class="sxs-lookup"><span data-stu-id="e5252-208">The current value for delta reservation.</span></span> <span data-ttu-id="e5252-209">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="e5252-209">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-210">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5252-210">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-213">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e5252-213">A description of the object.</span></span> <span data-ttu-id="e5252-214">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-215">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e5252-215">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-216">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-218">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="e5252-218">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e5252-219">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e5252-219">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5252-220">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e5252-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="e5252-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="e5252-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="e5252-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="e5252-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="e5252-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="e5252-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e5252-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e5252-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e5252-229">)</span><span class="sxs-lookup"><span data-stu-id="e5252-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e5252-230">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e5252-230">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-233">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e5252-233">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="e5252-234">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5252-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e5252-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-236">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-238">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e5252-238">A display name for the object.</span></span> <span data-ttu-id="e5252-239">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-240">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="e5252-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-241">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-243">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e5252-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e5252-244">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e5252-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e5252-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-246">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-248">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e5252-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e5252-249">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="e5252-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e5252-250">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e5252-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e5252-251">Значение</span><span class="sxs-lookup"><span data-stu-id="e5252-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e5252-252">Значение</span><span class="sxs-lookup"><span data-stu-id="e5252-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e5252-253"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e5252-254">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="e5252-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="e5252-255"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e5252-256"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="e5252-257">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="e5252-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e5252-258"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e5252-259">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="e5252-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="e5252-260"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="e5252-261">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="e5252-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="e5252-262"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="e5252-263">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="e5252-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="e5252-264"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e5252-265">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="e5252-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="e5252-266"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="e5252-267">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="e5252-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="e5252-268"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="e5252-269">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="e5252-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="e5252-270"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="e5252-271">Элемент включен, но находится в ограниченном режиме.</span><span class="sxs-lookup"><span data-stu-id="e5252-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="e5252-272">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="e5252-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="e5252-273">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="e5252-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="e5252-274"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="e5252-275">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="e5252-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="e5252-276">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="e5252-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="e5252-277">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="e5252-277">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-278">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-278">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-280">Конечный адрес непрерывного блока памяти.</span><span class="sxs-lookup"><span data-stu-id="e5252-280">The ending address of the contiguous memory block.</span></span> <span data-ttu-id="e5252-281">Так как свойство **стартингаддресс** всегда равно 0, это значение всегда отражает общий объем памяти виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5252-281">Since the **StartingAddress** property is always 0, this value always reflects the total amount of memory in the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-282">**ерроракцесс**</span><span class="sxs-lookup"><span data-stu-id="e5252-282">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-283">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-285">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-285">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-286">**еррораддресс**</span><span class="sxs-lookup"><span data-stu-id="e5252-286">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-287">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-289">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-289">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-290">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="e5252-290">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-291">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5252-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-293">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-293">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-294">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="e5252-294">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-295">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e5252-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-297">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-297">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-298">**еррордатаордер**</span><span class="sxs-lookup"><span data-stu-id="e5252-298">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-299">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-301">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-301">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e5252-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-305">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-305">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-306">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e5252-306">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-307">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-309">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-309">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-310">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="e5252-310">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-311">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-313">Строка, описывающая тип обнаружения и исправления ошибок, поддерживаемых этой областью хранения.</span><span class="sxs-lookup"><span data-stu-id="e5252-313">A string that describes the type of error detection and correction supported by this storage extent.</span></span> <span data-ttu-id="e5252-314">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5252-314">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-315">**еррорресолутион**</span><span class="sxs-lookup"><span data-stu-id="e5252-315">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-316">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-318">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-318">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-319">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="e5252-319">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-320">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e5252-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-322">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory) , но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-322">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory) but it not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-323">**еррортрансферсизе**</span><span class="sxs-lookup"><span data-stu-id="e5252-323">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-324">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5252-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-326">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-326">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-327">**екстентстатус**</span><span class="sxs-lookup"><span data-stu-id="e5252-327">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-328">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e5252-328">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-330">В экстентах хранения дополнительные сведения о состоянии выходят за пределы, полученные в **OperationalStatus** , и другие свойства, унаследованные от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-330">Storage extents have additional status information beyond that captured in the **OperationalStatus** and other properties inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="e5252-331">Эти дополнительные сведения (например, "Защита отключена", значение = 9) захватывается в свойстве **волуместатус** .</span><span class="sxs-lookup"><span data-stu-id="e5252-331">This additional information (for example, "Protection Disabled", value=9) is captured in the **VolumeStatus** property.</span></span> <span data-ttu-id="e5252-332">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение 2 (нет или неприменимо).</span><span class="sxs-lookup"><span data-stu-id="e5252-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2 (None/Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-333">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e5252-333">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-334">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-336">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="e5252-336">The current health of the element.</span></span> <span data-ttu-id="e5252-337">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="e5252-337">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e5252-338">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="e5252-338">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e5252-339">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="e5252-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-340">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e5252-340">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-341">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e5252-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-343">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5252-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-344">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e5252-344">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-345">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e5252-345">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-347">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5252-347">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e5252-348">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-349">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e5252-349">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-350">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5252-352">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e5252-352">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e5252-353">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="e5252-353">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e5252-354">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-354">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-355">**исбаседонундерлингредунданци**</span><span class="sxs-lookup"><span data-stu-id="e5252-355">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-356">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5252-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-358">**Значение true** , если базовые экстенты хранения участвуют в группе избыточности хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5252-358">**True** if the underlying storage extents participate in a Storage Redundancy Group.</span></span> <span data-ttu-id="e5252-359">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="e5252-359">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-360">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="e5252-360">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-361">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5252-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-363">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-364">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="e5252-364">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-365">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-367">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-368">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5252-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-369">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5252-371">Квалификаторы: **maxlen** (1024), **override** ("имя")</span><span class="sxs-lookup"><span data-stu-id="e5252-371">Qualifiers: **MaxLen** (1024), **Override** ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e5252-372">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="e5252-372">The label by which the object is known.</span></span> <span data-ttu-id="e5252-373">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="e5252-373">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="e5252-374">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="e5252-374">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="e5252-375">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="e5252-375">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-376">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-378">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="e5252-378">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-379">**наменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="e5252-379">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-380">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-382">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="e5252-382">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-383">**носинглепоинтоффаилуре**</span><span class="sxs-lookup"><span data-stu-id="e5252-383">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-384">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5252-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-386">**Значение true** , если не существует единой точки отказа.</span><span class="sxs-lookup"><span data-stu-id="e5252-386">**True** if there exists no single point of failure.</span></span> <span data-ttu-id="e5252-387">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="e5252-387">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-388">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="e5252-388">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-389">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-391">Вычисленное значение, представляющее общий объем памяти, деленный на размер **блока**.</span><span class="sxs-lookup"><span data-stu-id="e5252-391">A calculated value that represents the total amount of memory divided by the **BlockSize**.</span></span> <span data-ttu-id="e5252-392">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e5252-392">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-393">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="e5252-393">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-394">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-396">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e5252-396">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e5252-397">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e5252-397">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5252-398">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-398">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e5252-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e5252-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="e5252-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="e5252-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="e5252-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="e5252-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="e5252-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="e5252-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="e5252-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="e5252-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="e5252-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="e5252-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="e5252-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="e5252-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="e5252-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="e5252-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="e5252-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="e5252-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e5252-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e5252-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e5252-418">)</span><span class="sxs-lookup"><span data-stu-id="e5252-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e5252-419">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e5252-419">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-420">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e5252-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-422">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e5252-422">The current statuses of the object.</span></span> <span data-ttu-id="e5252-423">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-424">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="e5252-424">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-425">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-427">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e5252-427">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e5252-428">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="e5252-428">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e5252-429">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5252-429">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-430">**осереррордескриптион**</span><span class="sxs-lookup"><span data-stu-id="e5252-430">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-431">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-433">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-433">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-434">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e5252-434">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-435">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e5252-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-436">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-437">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5252-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-438">**осернамеформат**</span><span class="sxs-lookup"><span data-stu-id="e5252-438">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-441">Пространство имен свойства **Name** , если свойство **намеформат** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e5252-441">The namespace of the **Name** property when the **NameFormat** property includes the value 1 (Other").</span></span> <span data-ttu-id="e5252-442">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5252-442">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-443">**осернаменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="e5252-443">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-444">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-445">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-446">Пространство имен свойства **Name** , если свойство **наменамеспаце** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e5252-446">The namespace of the **Name** property when the **NameNamespace** property includes the value 1 (Other).</span></span> <span data-ttu-id="e5252-447">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e5252-447">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-448">**паккажередунданци**</span><span class="sxs-lookup"><span data-stu-id="e5252-448">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-449">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-451">Количество физических пакетов, которые в данный момент могут завершиться сбоем без потери данных.</span><span class="sxs-lookup"><span data-stu-id="e5252-451">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="e5252-452">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="e5252-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-453">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="e5252-453">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-454">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e5252-454">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-456">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-456">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-457">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="e5252-457">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-458">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5252-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-459">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-460">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-460">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-461">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="e5252-461">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-462">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-463">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-464">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-464">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-465">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="e5252-465">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-466">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-466">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-467">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-468">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="e5252-468">Provides high level status information.</span></span> <span data-ttu-id="e5252-469">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="e5252-469">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e5252-470">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e5252-470">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5252-471">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e5252-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e5252-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-473"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="e5252-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="e5252-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="e5252-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e5252-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e5252-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="e5252-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e5252-478">)</span><span class="sxs-lookup"><span data-stu-id="e5252-478">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e5252-479">**Исходный пул**</span><span class="sxs-lookup"><span data-stu-id="e5252-479">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-480">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5252-480">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-482">**Значение true** , если содержащаяся система не имеет возможности создавать или удалять этот операционный элемент.</span><span class="sxs-lookup"><span data-stu-id="e5252-482">**True** if the containing system does not have the ability to create or delete this operational element.</span></span> <span data-ttu-id="e5252-483">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e5252-483">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-484">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="e5252-484">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-485">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-486">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-487">Строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="e5252-487">A string that describes the media and its use.</span></span> <span data-ttu-id="e5252-488">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение "системная память".</span><span class="sxs-lookup"><span data-stu-id="e5252-488">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "System Memory".</span></span>

</dd> <dt>

<span data-ttu-id="e5252-489">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e5252-489">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-490">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-490">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-491">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-492">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="e5252-492">The last requested or desired state for the element.</span></span> <span data-ttu-id="e5252-493">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="e5252-493">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e5252-494">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="e5252-494">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="e5252-495">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e5252-495">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="e5252-496">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="e5252-496">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="e5252-497">Это свойство наследуется от **CIM \_ енабледлогикалелемент**.</span><span class="sxs-lookup"><span data-stu-id="e5252-497">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-498">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="e5252-498">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-499">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5252-499">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-500">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-501">**Значение true** , если доступ к хранилищу осуществляется последовательно с помощью устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="e5252-501">**True** if the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="e5252-502">Раздел ленты — это пример последовательного доступа к экстенту хранения.</span><span class="sxs-lookup"><span data-stu-id="e5252-502">A tape partition is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="e5252-503">Тома хранилища, разделы диска и логические диски представляют собой недоступные для произвольного доступа экстенты.</span><span class="sxs-lookup"><span data-stu-id="e5252-503">Storage volumes, disk partitions, and logical disks represent randomly accessed extents.</span></span> <span data-ttu-id="e5252-504">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и всегда имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="e5252-504">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-505">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="e5252-505">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-506">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-506">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-508">Начальный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="e5252-508">The beginning address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="e5252-509">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory)и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="e5252-509">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-510">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e5252-510">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-511">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-512">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-512">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-513">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-513">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-514">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="e5252-514">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-515">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e5252-515">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5252-516">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-517">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e5252-517">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e5252-518">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e5252-518">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-519">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e5252-519">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-520">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-521">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-522">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-522">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-523">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="e5252-523">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-524">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-524">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-525">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-526">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="e5252-526">The scoping system's creation class name.</span></span> <span data-ttu-id="e5252-527">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5252-527">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-528">**системлевеладдресс**</span><span class="sxs-lookup"><span data-stu-id="e5252-528">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-529">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5252-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-530">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-531">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-531">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-532">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e5252-532">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-533">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5252-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-534">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-535">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5252-535">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="e5252-536">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5252-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-537">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="e5252-537">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-538">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e5252-538">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-539">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-540">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e5252-540">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e5252-541">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение "null".</span><span class="sxs-lookup"><span data-stu-id="e5252-541">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="e5252-542">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="e5252-542">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-543">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e5252-543">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-544">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-545">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e5252-545">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5252-546">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="e5252-546">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-547">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5252-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-548">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-549">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e5252-549">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e5252-550">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e5252-550">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5252-551">**Независимо**</span><span class="sxs-lookup"><span data-stu-id="e5252-551">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5252-552">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5252-552">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5252-553">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5252-553">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5252-554">Указывает, является ли память энергозависимой.</span><span class="sxs-lookup"><span data-stu-id="e5252-554">Indicates whether memory is volatile.</span></span> <span data-ttu-id="e5252-555">Это свойство наследуется [**от \_ памяти CIM**](/windows/desktop/CIMWin32Prov/cim-memory)и всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="e5252-555">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **True**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5252-556">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5252-556">Remarks</span></span>

<span data-ttu-id="e5252-557">Доступ к классу **\_ памяти мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e5252-557">Access to the **Msvm\_Memory** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e5252-558">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e5252-558">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5252-559">Требования</span><span class="sxs-lookup"><span data-stu-id="e5252-559">Requirements</span></span>



| <span data-ttu-id="e5252-560">Требование</span><span class="sxs-lookup"><span data-stu-id="e5252-560">Requirement</span></span> | <span data-ttu-id="e5252-561">Значение</span><span class="sxs-lookup"><span data-stu-id="e5252-561">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5252-562">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5252-562">Minimum supported client</span></span><br/> | <span data-ttu-id="e5252-563">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e5252-563">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e5252-564">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5252-564">Minimum supported server</span></span><br/> | <span data-ttu-id="e5252-565">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e5252-565">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5252-566">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e5252-566">Namespace</span></span><br/>                | <span data-ttu-id="e5252-567">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e5252-567">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e5252-568">MOF</span><span class="sxs-lookup"><span data-stu-id="e5252-568">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5252-569"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-569"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5252-570">DLL</span><span class="sxs-lookup"><span data-stu-id="e5252-570">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5252-571"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5252-571"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e5252-572">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5252-572">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5252-573">**\_Память CIM**</span><span class="sxs-lookup"><span data-stu-id="e5252-573">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dt>

[<span data-ttu-id="e5252-574">**\_Память CIM**</span><span class="sxs-lookup"><span data-stu-id="e5252-574">**CIM\_Memory**</span></span>](/windows/desktop/CIMWin32Prov/cim-memory)
</dt> <dt>

[<span data-ttu-id="e5252-575">Классы памяти</span><span class="sxs-lookup"><span data-stu-id="e5252-575">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

