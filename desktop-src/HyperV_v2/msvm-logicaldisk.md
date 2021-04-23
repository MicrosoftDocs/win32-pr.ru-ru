---
description: Представляет носитель диска хранилища и используется для заполнения дисков хранилища.
ms.assetid: 06955C09-CA56-4B4C-997B-9B65AF125375
title: Класс Msvm_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk
- Msvm_LogicalDisk.SetPowerState
- Msvm_LogicalDisk.EnableDevice
- Msvm_LogicalDisk.OnlineDevice
- Msvm_LogicalDisk.QuiesceDevice
- Msvm_LogicalDisk.SaveProperties
- Msvm_LogicalDisk.RestoreProperties
- Msvm_LogicalDisk.InstanceID
- Msvm_LogicalDisk.Caption
- Msvm_LogicalDisk.Description
- Msvm_LogicalDisk.ElementName
- Msvm_LogicalDisk.InstallDate
- Msvm_LogicalDisk.Name
- Msvm_LogicalDisk.OperationalStatus
- Msvm_LogicalDisk.StatusDescriptions
- Msvm_LogicalDisk.Status
- Msvm_LogicalDisk.HealthState
- Msvm_LogicalDisk.CommunicationStatus
- Msvm_LogicalDisk.DetailedStatus
- Msvm_LogicalDisk.OperatingStatus
- Msvm_LogicalDisk.PrimaryStatus
- Msvm_LogicalDisk.EnabledState
- Msvm_LogicalDisk.OtherEnabledState
- Msvm_LogicalDisk.RequestedState
- Msvm_LogicalDisk.EnabledDefault
- Msvm_LogicalDisk.TimeOfLastStateChange
- Msvm_LogicalDisk.AvailableRequestedStates
- Msvm_LogicalDisk.TransitioningToState
- Msvm_LogicalDisk.SystemCreationClassName
- Msvm_LogicalDisk.SystemName
- Msvm_LogicalDisk.CreationClassName
- Msvm_LogicalDisk.DeviceID
- Msvm_LogicalDisk.PowerManagementSupported
- Msvm_LogicalDisk.PowerManagementCapabilities
- Msvm_LogicalDisk.Availability
- Msvm_LogicalDisk.StatusInfo
- Msvm_LogicalDisk.LastErrorCode
- Msvm_LogicalDisk.ErrorDescription
- Msvm_LogicalDisk.ErrorCleared
- Msvm_LogicalDisk.OtherIdentifyingInfo
- Msvm_LogicalDisk.PowerOnHours
- Msvm_LogicalDisk.TotalPowerOnHours
- Msvm_LogicalDisk.IdentifyingDescriptions
- Msvm_LogicalDisk.AdditionalAvailability
- Msvm_LogicalDisk.MaxQuiesceTime
- Msvm_LogicalDisk.DataOrganization
- Msvm_LogicalDisk.Purpose
- Msvm_LogicalDisk.Access
- Msvm_LogicalDisk.ErrorMethodology
- Msvm_LogicalDisk.BlockSize
- Msvm_LogicalDisk.NumberOfBlocks
- Msvm_LogicalDisk.ConsumableBlocks
- Msvm_LogicalDisk.IsBasedOnUnderlyingRedundancy
- Msvm_LogicalDisk.SequentialAccess
- Msvm_LogicalDisk.ExtentStatus
- Msvm_LogicalDisk.NoSinglePointOfFailure
- Msvm_LogicalDisk.DataRedundancy
- Msvm_LogicalDisk.PackageRedundancy
- Msvm_LogicalDisk.DeltaReservation
- Msvm_LogicalDisk.Primordial
- Msvm_LogicalDisk.NameFormat
- Msvm_LogicalDisk.NameNamespace
- Msvm_LogicalDisk.OtherNameNamespace
- Msvm_LogicalDisk.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5071f2a102a32364888c9c7de5121ede5249f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683550"
---
# <a name="msvm_logicaldisk-class"></a><span data-ttu-id="e2b0b-103">\_Класс мсвм LogicalDisk</span><span class="sxs-lookup"><span data-stu-id="e2b0b-103">Msvm\_LogicalDisk class</span></span>

<span data-ttu-id="e2b0b-104">Представляет носитель диска хранилища и используется для заполнения дисков хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-104">Represents storage drive media and is used to populate the storage drives.</span></span> <span data-ttu-id="e2b0b-105">Поддерживаются следующие типы носителей: виртуальные жесткие файлы, виртуальные гибкие файлы, ISO-файлы и носитель физического устройства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-105">The media types supported include virtual hard files, virtual floppy files, ISO files, and physical device media.</span></span>

<span data-ttu-id="e2b0b-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b0b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2b0b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalDisk : CIM_LogicalDisk
{
  string   InstanceID;
  string   Caption;
  uint64   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_LogicalDisk";
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
  uint16   DataOrganization = 2;
  string   Purpose;
  uint16   Access;
  string   ErrorMethodology;
  uint64   BlockSize = 512;
  uint64   NumberOfBlocks = 266338304;
  uint64   ConsumableBlocks = 0;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = { 2 };
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 0;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial = False;
  uint16   NameFormat = 12;
  uint16   NameNamespace = 8;
  string   OtherNameNamespace;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="e2b0b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e2b0b-108">Members</span></span>

<span data-ttu-id="e2b0b-109">Класс **мсвм \_ LogicalDisk** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e2b0b-109">The **Msvm\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="e2b0b-110">Методы</span><span class="sxs-lookup"><span data-stu-id="e2b0b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2b0b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e2b0b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2b0b-112">Методы</span><span class="sxs-lookup"><span data-stu-id="e2b0b-112">Methods</span></span>

<span data-ttu-id="e2b0b-113">Класс **мсвм \_ LogicalDisk** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-113">The **Msvm\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="e2b0b-114">Метод</span><span class="sxs-lookup"><span data-stu-id="e2b0b-114">Method</span></span>                                                            | <span data-ttu-id="e2b0b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="e2b0b-115">Description</span></span>                              |
|:------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e2b0b-116">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-116">**EnableDevice**</span></span>                                                  | <span data-ttu-id="e2b0b-117">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e2b0b-118">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-118">**OnlineDevice**</span></span>                                                  | <span data-ttu-id="e2b0b-119">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e2b0b-120">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-120">**QuiesceDevice**</span></span>                                                 | <span data-ttu-id="e2b0b-121">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e2b0b-122">**Равен**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-122">**RequestStateChange**</span></span>](msvm-logicaldisk-requeststatechange.md) | <span data-ttu-id="e2b0b-123">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e2b0b-124">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-124">**Reset**</span></span>](msvm-logicaldisk-reset.md)                           | <span data-ttu-id="e2b0b-125">Сбрасывает службу.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-125">Resets the service.</span></span><br/>           |
| <span data-ttu-id="e2b0b-126">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-126">**RestoreProperties**</span></span>                                             | <span data-ttu-id="e2b0b-127">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e2b0b-128">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-128">**SaveProperties**</span></span>                                                | <span data-ttu-id="e2b0b-129">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e2b0b-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-130">**SetPowerState**</span></span>                                                 | <span data-ttu-id="e2b0b-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e2b0b-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="e2b0b-132">Properties</span></span>

<span data-ttu-id="e2b0b-133">Класс **мсвм \_ LogicalDisk** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-133">The **Msvm\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2b0b-134">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-134">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-137">Указывает, доступен ли мультимедиа для чтения, записи или для того и другого.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-137">Indicates whether the media is readable, writeable, or both.</span></span> <span data-ttu-id="e2b0b-138">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-138">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="e2b0b-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-139">Value</span></span>                                                                        | <span data-ttu-id="e2b0b-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-140">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="e2b0b-141"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-141"><dt>0</dt></span></span> </dl> | <span data-ttu-id="e2b0b-142">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="e2b0b-142">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="e2b0b-143"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-143"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e2b0b-144">Чтения.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-144">Readable.</span></span><br/>   |
| <dl> <span data-ttu-id="e2b0b-145"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-145"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e2b0b-146">Возможностью записи.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-146">Writeable.</span></span><br/>  |
| <dl> <span data-ttu-id="e2b0b-147"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-147"><dt>3</dt></span></span> </dl> | <span data-ttu-id="e2b0b-148">Read/write.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-148">Read/write.</span></span><br/> |
| <dl> <span data-ttu-id="e2b0b-149"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-149"><dt>4</dt></span></span> </dl> | <span data-ttu-id="e2b0b-150">Однократная запись.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-150">Write once.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2b0b-151">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-152">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e2b0b-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-154">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-154">Any additional availability and status of the device.</span></span> <span data-ttu-id="e2b0b-155">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-155">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="e2b0b-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-156">Value</span></span>                                                                            | <span data-ttu-id="e2b0b-157">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-157">Meaning</span></span>                    |
|----------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="e2b0b-158"><dt>1-6</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-158"><dt>{ 6 }</dt></span></span> </dl> | <span data-ttu-id="e2b0b-159">Не применяется</span><span class="sxs-lookup"><span data-stu-id="e2b0b-159">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2b0b-160">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-161">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-163">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-163">The primary availability and status of the device.</span></span> <span data-ttu-id="e2b0b-164">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-164">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="e2b0b-165">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-165">Value</span></span>                                                                        | <span data-ttu-id="e2b0b-166">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-166">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="e2b0b-167"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-167"><dt>6</dt></span></span> </dl> | <span data-ttu-id="e2b0b-168">Не применяется</span><span class="sxs-lookup"><span data-stu-id="e2b0b-168">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2b0b-169">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-169">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-170">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e2b0b-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-172">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-172">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="e2b0b-173">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e2b0b-173">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="e2b0b-174">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-174">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="e2b0b-175">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-175">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="e2b0b-176">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-176">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-178">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-180">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-180">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="e2b0b-181">Если размер блока является переменным, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-181">If the block size is variable, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="e2b0b-182">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), это значение будет содержать 1.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-182">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), this will contain 1.</span></span> <span data-ttu-id="e2b0b-183">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-183">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-184">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-187">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-187">A short description of the object.</span></span> <span data-ttu-id="e2b0b-188">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="e2b0b-189">"ISO-образ диска"</span><span class="sxs-lookup"><span data-stu-id="e2b0b-189">"ISO Disk Image"</span></span>

<span data-ttu-id="e2b0b-190">"Образ жесткого диска"</span><span class="sxs-lookup"><span data-stu-id="e2b0b-190">"Hard Disk Image"</span></span>

<span data-ttu-id="e2b0b-191">"Образ гибкого диска"</span><span class="sxs-lookup"><span data-stu-id="e2b0b-191">"Floppy Disk Image"</span></span>

<span data-ttu-id="e2b0b-192">"CD/DVD-диск"</span><span class="sxs-lookup"><span data-stu-id="e2b0b-192">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-193">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-194">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-196">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e2b0b-197">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2b0b-198">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-199">**консумаблеблоккс**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-199">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-200">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-202">Максимальное количество блоков **, размерностей, доступных** для использования при слоевых экстентах хранения с использованием ассоциации [**мсвм \_ BasedOn**](msvm-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="e2b0b-202">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the [**Msvm\_BasedOn**](msvm-basedon.md) association.</span></span> <span data-ttu-id="e2b0b-203">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-203">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-204">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-204">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-205">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-207">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-207">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e2b0b-208">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-209">**Организация**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-209">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-210">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-212">Тип используемой организации данных.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-212">The type of data organization used.</span></span> <span data-ttu-id="e2b0b-213">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-213">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="e2b0b-214">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-214">Value</span></span>                                                                        | <span data-ttu-id="e2b0b-215">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-215">Meaning</span></span>                 |
|------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="e2b0b-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e2b0b-217">Фиксированный блок.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-217">Fixed block.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2b0b-218">**Избыточность**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-218">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-219">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-221">Количество полных копий данных, хранящихся в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-221">The number of complete copies of data currently maintained.</span></span> <span data-ttu-id="e2b0b-222">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-222">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-223">**делтаресерватион**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-223">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-224">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-224">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-226">Процентное значение, указывающее объем пространства, которое должно быть зарезервировано в реплике для кэширования изменений.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-226">A percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span> <span data-ttu-id="e2b0b-227">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-227">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-228">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-228">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-229">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-231">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-231">A description of the object.</span></span> <span data-ttu-id="e2b0b-232">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-232">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-233">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-233">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-234">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-235">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-236">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-236">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e2b0b-237">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-237">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2b0b-238">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-239">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-239">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-240">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-242">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение «Microsoft:*GUID* \\ *устройства-данные*».</span><span class="sxs-lookup"><span data-stu-id="e2b0b-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-243">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-243">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-246">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-246">A display name for the object.</span></span> <span data-ttu-id="e2b0b-247">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-247">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="e2b0b-248">"ISO-образ диска"</span><span class="sxs-lookup"><span data-stu-id="e2b0b-248">"ISO Disk Image"</span></span>

<span data-ttu-id="e2b0b-249">"Образ жесткого диска"</span><span class="sxs-lookup"><span data-stu-id="e2b0b-249">"Hard Disk Image"</span></span>

<span data-ttu-id="e2b0b-250">"Образ гибкого диска"</span><span class="sxs-lookup"><span data-stu-id="e2b0b-250">"Floppy Disk Image"</span></span>

<span data-ttu-id="e2b0b-251">"CD/DVD-диск"</span><span class="sxs-lookup"><span data-stu-id="e2b0b-251">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-252">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-253">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-255">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-255">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e2b0b-256">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-257">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-257">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-260">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-260">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e2b0b-261">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-261">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e2b0b-262">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-263">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-263">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-264">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-266">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="e2b0b-266">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="e2b0b-267">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-268">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-268">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-269">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-271">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-271">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="e2b0b-272">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-273">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-273">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-276">Строка, описывающая типы обнаружения ошибок и исправления, поддерживаемые этим устройством.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-276">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="e2b0b-277">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-277">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-278">**екстентстатус**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-278">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-279">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e2b0b-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-281">Любые дополнительные сведения о состоянии, не заданные в **OperationalStatus** и других унаследованных свойствах.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-281">Any additional status information beyond that captured in the **OperationalStatus** and other inherited properties.</span></span>



| <span data-ttu-id="e2b0b-282">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-282">Value</span></span>                                                                            | <span data-ttu-id="e2b0b-283">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-283">Meaning</span></span>                         |
|----------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="e2b0b-284"><dt>открыт</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-284"><dt>{ 2 }</dt></span></span> </dl> | <span data-ttu-id="e2b0b-285">Нет/неприменимо.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-285">None/Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2b0b-286">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-286">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-287">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-289">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-289">The current health of the element.</span></span> <span data-ttu-id="e2b0b-290">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-290">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e2b0b-291">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-291">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e2b0b-292">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-293">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-293">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-294">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-296">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="e2b0b-296">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="e2b0b-297">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-297">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-299">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-301">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-301">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e2b0b-302">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-303">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-303">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-306">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-306">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-307">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-307">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e2b0b-308">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-308">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-309">**исбаседонундерлингредунданци**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-309">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-310">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-312">Указывает, участвуют ли базовые экстенты хранения в группе избыточности хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-312">Indicates whether the underlying storage extents participate in a storage redundancy group.</span></span> <span data-ttu-id="e2b0b-313">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-313">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-314">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-315">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-317">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-317">The last error code reported by the logical device.</span></span> <span data-ttu-id="e2b0b-318">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-319">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-319">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-320">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-322">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-322">This property has been deprecated.</span></span> <span data-ttu-id="e2b0b-323">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-324">**Name**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-327">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-327">The label by which the object is known.</span></span> <span data-ttu-id="e2b0b-328">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="e2b0b-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-329">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-329">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-330">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-332">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="e2b0b-333">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-333">Value</span></span>                                                                         | <span data-ttu-id="e2b0b-334">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-334">Meaning</span></span>                                 |
|-------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="e2b0b-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-335"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="e2b0b-336">Другое</span><span class="sxs-lookup"><span data-stu-id="e2b0b-336">Other</span></span><br/>                        |
| <dl> <span data-ttu-id="e2b0b-337"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-337"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e2b0b-338">Имя устройства операционной системы</span><span class="sxs-lookup"><span data-stu-id="e2b0b-338">Operating system device name</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2b0b-339">**наменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-339">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-340">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-342">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-342">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="e2b0b-343">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-343">Value</span></span>                                                                        | <span data-ttu-id="e2b0b-344">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-344">Meaning</span></span>                                      |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e2b0b-345"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-345"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e2b0b-346">Другое</span><span class="sxs-lookup"><span data-stu-id="e2b0b-346">Other</span></span><br/>                             |
| <dl> <span data-ttu-id="e2b0b-347"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-347"><dt>8</dt></span></span> </dl> | <span data-ttu-id="e2b0b-348">Пространство имен устройств операционной системы</span><span class="sxs-lookup"><span data-stu-id="e2b0b-348">Operating system device namespace</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2b0b-349">**носинглепоинтоффаилуре**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-349">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-350">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-352">Указывает, не существует ли единой точки отказа.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-352">Indicates whether there exists no single point of failure.</span></span> <span data-ttu-id="e2b0b-353">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-353">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-354">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-354">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-355">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-357">Число последовательных блоков, каждый из которых блокирует размер значения, содержащегося **в свойстве** «область хранения».</span><span class="sxs-lookup"><span data-stu-id="e2b0b-357">The number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="e2b0b-358">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="e2b0b-359">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span> <span data-ttu-id="e2b0b-360">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-360">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-361">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-361">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-362">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-364">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e2b0b-364">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e2b0b-365">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-365">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2b0b-366">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-366">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-367">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-367">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-368">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e2b0b-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-370">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="e2b0b-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-371">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-371">The current statuses of the object.</span></span> <span data-ttu-id="e2b0b-372">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="e2b0b-373">Если требуемый уровень качества обслуживания для виртуального диска не может быть удовлетворен, основное состояние (OperationalStatus \[ 0 \] ) установлено на пониженное (3), а массив OperationalStatus дополнительно содержит дополнительное значение состояния, указывающее конкретную причину для условия качества обслуживания в соответствии с этой таблицей.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-373">When the required QoS level for the virtual disk can't be satisfied, the primary status (OperationalStatus\[0\]) is set to Degraded (3) and the OperationalStatus array additionally contains a secondary status value that indicates the specific reason for the QoS condition, according to this table.</span></span>



| <span data-ttu-id="e2b0b-374">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-374">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="e2b0b-375">Описание</span><span class="sxs-lookup"><span data-stu-id="e2b0b-375">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b0b-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Недостаточная пропускная способность (32788)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="e2b0b-377">Запрошенная минимальная частота операций ввода-вывода в настоящее время недоступна для устройства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-377">The requested minimum IOPS rate is currently not available to the device.</span></span> <br/> |



 

> [!Note]  
> <span data-ttu-id="e2b0b-378">OperationalStatus также используется для сообщения о других условиях ошибок или предупреждений (например, несоответствие протоколов между VSP и VSC).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-378">OperationalStatus is also used to report other error or warning conditions (for example, protocol mismatch between VSP and VSC).</span></span> <span data-ttu-id="e2b0b-379">Если существует несколько условий, первичное состояние устанавливается с пониженной производительностью, а одно или несколько вторичных значений состояния в любом порядке, начиная с индекса 1, заполняются массивом.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-379">If multiple conditions exists, the primary status is set Degraded, and one or more secondary status values, in any order starting at index 1, is filled in the array.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e2b0b-380"><span id="OK"></span><span id="ok"></span>**ОК** (2)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e2b0b-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (3)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="e2b0b-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (7)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="e2b0b-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (11)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e2b0b-384">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-384">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e2b0b-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (12)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="e2b0b-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (13)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="e2b0b-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (16)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e2b0b-388">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="e2b0b-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Несоответствие протоколов** (32775)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="e2b0b-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Истекло время ожидания связи** (32783)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e2b0b-391">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="e2b0b-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Недостаточная пропускная способность** (32788)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>

<span data-ttu-id="e2b0b-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Неизвестный идентификатор политики качества обслуживания** (32791)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Unknown QoS Policy ID** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>

<span data-ttu-id="e2b0b-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS не поддерживается** (32792)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS Not Supported** (32792)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e2b0b-395">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-395">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>

<span data-ttu-id="e2b0b-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**Несоответствие конфигурации качества обслуживания** (32793)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**QoS Configuration Mismatch** (32793)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e2b0b-397">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>

<span data-ttu-id="e2b0b-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Диск полон** (32794)</span><span class="sxs-lookup"><span data-stu-id="e2b0b-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disk Full** (32794)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e2b0b-399">Добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-399">Added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e2b0b-400">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-400">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-401">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-403">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-403">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e2b0b-404">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-404">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e2b0b-405">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-405">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-406">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-406">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-407">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-409">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-409">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="e2b0b-410">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-411">**осернамеформат**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-411">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-412">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-414">Строка, описывающая формат свойства **Name** , если **намеформат** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-414">A string that describes the format of the **Name** property when **NameFormat** contains the value 1 (Other).</span></span> <span data-ttu-id="e2b0b-415">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-415">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-416">**осернаменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-416">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-417">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-419">Строка, описывающая пространство имен свойства **Name** , если **наменамеспаце** содержит значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-419">A string that describes the namespace of the **Name** property when **NameNamespace** contains the value 1 (Other).</span></span> <span data-ttu-id="e2b0b-420">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-420">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-421">**паккажередунданци**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-421">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-422">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-423">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-424">Количество физических пакетов, которые в данный момент могут завершиться сбоем без потери данных.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-424">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="e2b0b-425">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-425">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-426">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-426">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-427">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e2b0b-427">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-429">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-429">The power management capabilities of the device.</span></span> <span data-ttu-id="e2b0b-430">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-430">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-431">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-432">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-433">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-434">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-434">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="e2b0b-435">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-436">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-437">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-438">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-439">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-439">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="e2b0b-440">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-440">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-441">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-441">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-442">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-442">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-444">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-444">Provides high level status information.</span></span> <span data-ttu-id="e2b0b-445">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-445">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="e2b0b-446">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-446">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2b0b-447">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-448">**Исходный пул**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-448">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-449">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-449">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-451">Указывает, имеет ли содержащаяся система возможность создания или удаления этого операционного элемента.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-451">Indicates whether the containing system has the ability to create or delete this operational element.</span></span> <span data-ttu-id="e2b0b-452">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent)и имеет значение **false** для носителя на основе файлов и **true** для транзитного носителя.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to **False** for file-based media and **True** for pass-through media.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-453">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-453">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-454">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-456">Строка, описывающая носитель и (или) его использование.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-456">A string that describes the media and/or its use.</span></span> <span data-ttu-id="e2b0b-457">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-457">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-458">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-458">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-459">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-461">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-461">The last requested or desired state for the element.</span></span> <span data-ttu-id="e2b0b-462">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-462">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e2b0b-463">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-463">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="e2b0b-464">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e2b0b-464">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="e2b0b-465">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-465">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="e2b0b-466">Это свойство наследуется от **CIM \_ енабледлогикалелемент**.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-466">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-467">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-467">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-468">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-468">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-470">Указывает, осуществляется ли к хранилищу последовательный доступ с помощью устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-470">Indicates whether the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="e2b0b-471">Транзитный ленточный носитель является примером последовательного доступа к экстенту хранения.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-471">Pass-through tape media is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="e2b0b-472">Это свойство наследуется от [**CIM \_ сторажеекстент**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-472">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-473">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-473">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-474">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-476">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-476">The current status of the object.</span></span> <span data-ttu-id="e2b0b-477">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-477">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-478">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-478">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-479">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-479">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-480">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-481">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e2b0b-481">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e2b0b-482">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-482">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-483">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-483">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-484">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-484">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-485">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-486">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-486">The current state of the logical device.</span></span> <span data-ttu-id="e2b0b-487">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-488">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-488">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-489">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-489">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-490">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-491">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-491">The scoping system's creation class name.</span></span> <span data-ttu-id="e2b0b-492">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-493">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-493">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-494">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-495">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-496">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-496">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="e2b0b-497">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-498">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-498">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-499">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-499">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-500">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-501">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-501">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e2b0b-502">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-502">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-503">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-503">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-504">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-504">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-505">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-506">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-506">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="e2b0b-507">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-507">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0b-508">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-508">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2b0b-509">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2b0b-510">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2b0b-511">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-511">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e2b0b-512">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-512">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2b0b-513">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2b0b-513">Remarks</span></span>

<span data-ttu-id="e2b0b-514">Доступ к классу **мсвм \_ LogicalDisk** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e2b0b-514">Access to the **Msvm\_LogicalDisk** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e2b0b-515">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e2b0b-515">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b0b-516">Требования</span><span class="sxs-lookup"><span data-stu-id="e2b0b-516">Requirements</span></span>



| <span data-ttu-id="e2b0b-517">Требование</span><span class="sxs-lookup"><span data-stu-id="e2b0b-517">Requirement</span></span> | <span data-ttu-id="e2b0b-518">Значение</span><span class="sxs-lookup"><span data-stu-id="e2b0b-518">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b0b-519">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2b0b-519">Minimum supported client</span></span><br/> | <span data-ttu-id="e2b0b-520">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e2b0b-520">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e2b0b-521">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2b0b-521">Minimum supported server</span></span><br/> | <span data-ttu-id="e2b0b-522">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e2b0b-522">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2b0b-523">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2b0b-523">Namespace</span></span><br/>                | <span data-ttu-id="e2b0b-524">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e2b0b-524">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e2b0b-525">MOF</span><span class="sxs-lookup"><span data-stu-id="e2b0b-525">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2b0b-526"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-526"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2b0b-527">DLL</span><span class="sxs-lookup"><span data-stu-id="e2b0b-527">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2b0b-528"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0b-528"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2b0b-529">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2b0b-529">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b0b-530">**Логический диск CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-530">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="e2b0b-531">**Логический диск CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-531">**CIM\_LogicalDisk**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldisk)
</dt> <dt>

[<span data-ttu-id="e2b0b-532">**Мсвм \_ сторажеалерт**</span><span class="sxs-lookup"><span data-stu-id="e2b0b-532">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="e2b0b-533">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="e2b0b-533">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

