---
description: Представляет дисковод гибких дисков внутри виртуальной машины.
ms.assetid: 4624ABAF-3761-416F-9044-7A39EBF53D3D
title: Класс Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive
- Msvm_DisketteDrive.SetPowerState
- Msvm_DisketteDrive.EnableDevice
- Msvm_DisketteDrive.OnlineDevice
- Msvm_DisketteDrive.QuiesceDevice
- Msvm_DisketteDrive.SaveProperties
- Msvm_DisketteDrive.RestoreProperties
- Msvm_DisketteDrive.InstanceID
- Msvm_DisketteDrive.Caption
- Msvm_DisketteDrive.Description
- Msvm_DisketteDrive.ElementName
- Msvm_DisketteDrive.InstallDate
- Msvm_DisketteDrive.Name
- Msvm_DisketteDrive.OperationalStatus
- Msvm_DisketteDrive.StatusDescriptions
- Msvm_DisketteDrive.Status
- Msvm_DisketteDrive.HealthState
- Msvm_DisketteDrive.CommunicationStatus
- Msvm_DisketteDrive.DetailedStatus
- Msvm_DisketteDrive.OperatingStatus
- Msvm_DisketteDrive.PrimaryStatus
- Msvm_DisketteDrive.EnabledState
- Msvm_DisketteDrive.OtherEnabledState
- Msvm_DisketteDrive.RequestedState
- Msvm_DisketteDrive.EnabledDefault
- Msvm_DisketteDrive.TimeOfLastStateChange
- Msvm_DisketteDrive.AvailableRequestedStates
- Msvm_DisketteDrive.TransitioningToState
- Msvm_DisketteDrive.SystemCreationClassName
- Msvm_DisketteDrive.SystemName
- Msvm_DisketteDrive.CreationClassName
- Msvm_DisketteDrive.DeviceID
- Msvm_DisketteDrive.PowerManagementSupported
- Msvm_DisketteDrive.PowerManagementCapabilities
- Msvm_DisketteDrive.Availability
- Msvm_DisketteDrive.StatusInfo
- Msvm_DisketteDrive.LastErrorCode
- Msvm_DisketteDrive.ErrorDescription
- Msvm_DisketteDrive.ErrorCleared
- Msvm_DisketteDrive.OtherIdentifyingInfo
- Msvm_DisketteDrive.PowerOnHours
- Msvm_DisketteDrive.TotalPowerOnHours
- Msvm_DisketteDrive.IdentifyingDescriptions
- Msvm_DisketteDrive.AdditionalAvailability
- Msvm_DisketteDrive.MaxQuiesceTime
- Msvm_DisketteDrive.Capabilities
- Msvm_DisketteDrive.CapabilityDescriptions
- Msvm_DisketteDrive.ErrorMethodology
- Msvm_DisketteDrive.CompressionMethod
- Msvm_DisketteDrive.NumberOfMediaSupported
- Msvm_DisketteDrive.MaxMediaSize
- Msvm_DisketteDrive.DefaultBlockSize
- Msvm_DisketteDrive.MaxBlockSize
- Msvm_DisketteDrive.MinBlockSize
- Msvm_DisketteDrive.NeedsCleaning
- Msvm_DisketteDrive.MediaIsLocked
- Msvm_DisketteDrive.Security
- Msvm_DisketteDrive.LastCleaned
- Msvm_DisketteDrive.MaxAccessTime
- Msvm_DisketteDrive.UncompressedDataRate
- Msvm_DisketteDrive.LoadTime
- Msvm_DisketteDrive.UnloadTime
- Msvm_DisketteDrive.MountCount
- Msvm_DisketteDrive.TimeOfLastMount
- Msvm_DisketteDrive.TotalMountTime
- Msvm_DisketteDrive.UnitsDescription
- Msvm_DisketteDrive.MaxUnitsBeforeCleaning
- Msvm_DisketteDrive.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1dbc9e21626e2f5e8269fb3a398dd48a6ea442e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815232"
---
# <a name="msvm_diskettedrive-class"></a><span data-ttu-id="cd2c9-103">\_Класс мсвм дискеттедриве</span><span class="sxs-lookup"><span data-stu-id="cd2c9-103">Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="cd2c9-104">Представляет дисковод гибких дисков внутри виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-104">Represents a floppy drive inside the virtual machine.</span></span> <span data-ttu-id="cd2c9-105">Дисковод гибких дисков может быть заполнен файлом, представляющим гибкий носитель, или диском, который может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-105">A floppy drive can be populated with a file representing floppy media or the drive can be empty.</span></span> <span data-ttu-id="cd2c9-106">Физический носитель не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-106">Physical media is not supported.</span></span> <span data-ttu-id="cd2c9-107">В каждом контроллере флоппи-дисковода есть только один дисковод гибких дисков, который не является съемным.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-107">There is exactly one floppy drive per floppy controller and it is not removable.</span></span>

<span data-ttu-id="cd2c9-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2c9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd2c9-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteDrive : CIM_DisketteDrive
{
  string   InstanceID;
  string   Caption = "Diskette Drive";
  string   Description = "Microsoft Virtual Diskette Drive";
  string   ElementName = "Diskette Drive";
  datetime InstallDate;
  string   Name = "Diskette Drive";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   CreationClassName = "Msvm_DisketteDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
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
  uint16   Capabilities[] = {3, 4, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Writing", "Supports Removable Media"};
  string   ErrorMethodology = { "None" };
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 1440;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize = 512;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 18446744073709551615;
  uint64   UnitsUsed = 0;
};
```

## <a name="members"></a><span data-ttu-id="cd2c9-110">Члены</span><span class="sxs-lookup"><span data-stu-id="cd2c9-110">Members</span></span>

<span data-ttu-id="cd2c9-111">Класс **мсвм \_ дискеттедриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cd2c9-111">The **Msvm\_DisketteDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="cd2c9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="cd2c9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="cd2c9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd2c9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cd2c9-114">Методы</span><span class="sxs-lookup"><span data-stu-id="cd2c9-114">Methods</span></span>

<span data-ttu-id="cd2c9-115">Класс **мсвм \_ дискеттедриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-115">The **Msvm\_DisketteDrive** class has these methods.</span></span>



| <span data-ttu-id="cd2c9-116">Метод</span><span class="sxs-lookup"><span data-stu-id="cd2c9-116">Method</span></span>                                                              | <span data-ttu-id="cd2c9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cd2c9-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="cd2c9-118">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="cd2c9-119">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="cd2c9-120">**локкмедиа**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-120">**LockMedia**</span></span>](msvm-diskettedrive-lockmedia.md)                   | <span data-ttu-id="cd2c9-121">Блокирует или освобождает носитель.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="cd2c9-122">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-122">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="cd2c9-123">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cd2c9-124">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-124">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="cd2c9-125">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="cd2c9-126">**Равен**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-126">**RequestStateChange**</span></span>](msvm-diskettedrive-requeststatechange.md) | <span data-ttu-id="cd2c9-127">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="cd2c9-128">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-128">**Reset**</span></span>](msvm-diskettedrive-reset.md)                           | <span data-ttu-id="cd2c9-129">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="cd2c9-130">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-130">**RestoreProperties**</span></span>                                               | <span data-ttu-id="cd2c9-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cd2c9-132">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-132">**SaveProperties**</span></span>                                                  | <span data-ttu-id="cd2c9-133">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cd2c9-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-134">**SetPowerState**</span></span>                                                   | <span data-ttu-id="cd2c9-135">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cd2c9-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="cd2c9-136">Properties</span></span>

<span data-ttu-id="cd2c9-137">Класс **мсвм \_ дискеттедриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-137">The **Msvm\_DisketteDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd2c9-138">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-139">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="cd2c9-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-141">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="cd2c9-142">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="cd2c9-143">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c9-143">Value</span></span>                                                                        | <span data-ttu-id="cd2c9-144">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c9-144">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="cd2c9-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c9-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="cd2c9-146">Не применяется</span><span class="sxs-lookup"><span data-stu-id="cd2c9-146">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd2c9-147">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-147">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-148">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-150">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-150">The primary availability and status of the device.</span></span> <span data-ttu-id="cd2c9-151">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-151">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="cd2c9-152">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c9-152">Value</span></span>                                                                        | <span data-ttu-id="cd2c9-153">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c9-153">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="cd2c9-154"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c9-154"><dt>6</dt></span></span> </dl> | <span data-ttu-id="cd2c9-155">Не применяется</span><span class="sxs-lookup"><span data-stu-id="cd2c9-155">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd2c9-156">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-157">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="cd2c9-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-159">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-159">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="cd2c9-160">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cd2c9-160">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="cd2c9-161">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-161">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="cd2c9-162">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-162">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="cd2c9-163">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-163">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-164">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-164">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-165">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="cd2c9-165">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-167">Возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-167">The capabilities of the media access device.</span></span> <span data-ttu-id="cd2c9-168">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и задается для следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="cd2c9-169">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c9-169">Value</span></span>                                                                                | <span data-ttu-id="cd2c9-170">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c9-170">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd2c9-171"><dt>{3, 4, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c9-171"><dt>{3, 4, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="cd2c9-172"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c9-172"><dt>3</dt></span></span> </dl>         | <span data-ttu-id="cd2c9-173">Соответствующая запись в **капабилитидескриптионс** — "случайный доступ".</span><span class="sxs-lookup"><span data-stu-id="cd2c9-173">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="cd2c9-174"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c9-174"><dt>4</dt></span></span> </dl>         | <span data-ttu-id="cd2c9-175">Соответствующая запись в **капабилитидескриптионс** имеет значение "поддерживает запись".</span><span class="sxs-lookup"><span data-stu-id="cd2c9-175">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/>         |
| <dl> <span data-ttu-id="cd2c9-176"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c9-176"><dt>7</dt></span></span> </dl>         | <span data-ttu-id="cd2c9-177">Соответствующая запись в **капабилитидескриптионс** — "поддерживает съемные носители".</span><span class="sxs-lookup"><span data-stu-id="cd2c9-177">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd2c9-178">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-178">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-179">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-181">Массив строк произвольной формы, который содержит подробные объяснения для доступа к функциям устройств, указанным в массиве свойств **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="cd2c9-181">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="cd2c9-182">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-182">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span> <span data-ttu-id="cd2c9-183">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-183">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-184">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-187">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-187">A short description of the object.</span></span> <span data-ttu-id="cd2c9-188">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-189">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-190">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-192">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="cd2c9-193">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd2c9-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-195">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-195">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-198">Строка, указывающая алгоритм или средство, используемые для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-198">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="cd2c9-199">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="cd2c9-199">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="cd2c9-200">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="cd2c9-200">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="cd2c9-201">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-201">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="cd2c9-202">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-202">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="cd2c9-203">"Не сжато"</span><span class="sxs-lookup"><span data-stu-id="cd2c9-203">"Not Compressed"</span></span>

<span data-ttu-id="cd2c9-204">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="cd2c9-204">"Unknown"</span></span>

<span data-ttu-id="cd2c9-205">Сжатия</span><span class="sxs-lookup"><span data-stu-id="cd2c9-205">"Compressed"</span></span>

<span data-ttu-id="cd2c9-206">"Не сжато"</span><span class="sxs-lookup"><span data-stu-id="cd2c9-206">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-210">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-210">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cd2c9-211">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-211">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-212">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-212">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-213">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-215">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-215">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="cd2c9-216">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-216">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-217">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-217">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-218">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-219">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-220">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-220">A description of the object.</span></span> <span data-ttu-id="cd2c9-221">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-222">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-222">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-223">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-225">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-225">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="cd2c9-226">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-226">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd2c9-227">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-227">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-228">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-228">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-231">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение «Microsoft:*GUID* \\ *устройства-данные*».</span><span class="sxs-lookup"><span data-stu-id="cd2c9-231">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-232">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-232">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-233">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-235">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-235">A display name for the object.</span></span> <span data-ttu-id="cd2c9-236">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-237">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-238">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-239">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-240">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-240">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="cd2c9-241">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) и всегда имеет значение 2 (включено).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-245">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="cd2c9-246">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-246">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="cd2c9-247">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-248">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-248">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-249">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-251">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="cd2c9-251">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="cd2c9-252">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-252">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-253">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-253">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-254">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-256">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-256">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="cd2c9-257">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-257">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-258">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-258">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-259">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-261">Строка, описывающая типы обнаружения ошибок и исправления, поддерживаемые этим устройством.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-261">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="cd2c9-262">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-262">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-263">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-263">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-264">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-266">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-266">The current health of the element.</span></span> <span data-ttu-id="cd2c9-267">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-267">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="cd2c9-268">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-268">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="cd2c9-269">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-269">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-270">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-270">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-271">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-271">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-273">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="cd2c9-273">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="cd2c9-274">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-276">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-278">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-278">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="cd2c9-279">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-280">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-280">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-281">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-283">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-283">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-284">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-284">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="cd2c9-285">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-285">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-286">**ластклеанед**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-286">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-287">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-287">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-289">Дата и время последней очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-289">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="cd2c9-290">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-290">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-291">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-291">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-292">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-294">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-294">The last error code reported by the logical device.</span></span> <span data-ttu-id="cd2c9-295">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-295">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-296">**лоадтиме**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-296">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-297">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-299">Время в миллисекундах от загрузки до возможности чтения или записи носителя.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-299">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="cd2c9-300">Например, для дисков это интервал между диском, который не передается на диск, сообщает, что он готов для чтения и записи (т. е. диск вращается с номинальной скоростью).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-300">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="cd2c9-301">Для ленточных накопителей это время с носителя, добавляемого для сообщения о готовности к работе для приложения.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-301">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="cd2c9-302">Обычно это в области BOT ленты.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-302">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="cd2c9-303">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-303">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-304">**максакцесстиме**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-304">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-305">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-307">Время (в миллисекундах) перехода с первого места на носителе к расположению, которое находится в самом начале относительно времени.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-307">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="cd2c9-308">Для дискового накопителя это соответствует полной и полной задержке при повороте.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-308">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="cd2c9-309">Для ленточных накопителей этот элемент представляет собой поиск с начала ленты до наиболее физической отдаленной точки.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-309">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="cd2c9-310">(Конец ленты может находиться в самой физической точке, но это не обязательно верно). Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-310">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-311">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-311">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-312">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-314">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-314">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="cd2c9-315">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-315">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-316">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-316">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-317">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-319">Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-319">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="cd2c9-320">Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-320">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="cd2c9-321">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-321">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-322">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-322">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-323">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-325">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-325">This property has been deprecated.</span></span> <span data-ttu-id="cd2c9-326">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-327">**максунитсбефореклеанинг**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-327">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-328">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-330">Максимальное число единиц, которое можно использовать до очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-330">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="cd2c9-331">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-331">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-332">**медиаислоккед**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-332">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-333">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-335">**Значение true** , если носитель заблокирован на устройстве и не может быть извлечен. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-335">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="cd2c9-336">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-336">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-337">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-337">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-338">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-340">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-340">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="cd2c9-341">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-341">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-342">**маунткаунт**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-342">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-343">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-343">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-345">Для устройства, которое поддерживает съемные носители, число подключенных носителей для передачи данных или очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-345">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="cd2c9-346">Для устройств, обращающихся к несъемным носителям, например к жестким дискам, это свойство неприменимо и должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-346">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="cd2c9-347">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-347">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-348">**Name**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-351">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-351">The label by which the object is known.</span></span> <span data-ttu-id="cd2c9-352">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="cd2c9-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-353">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-353">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-354">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-356">**Значение true** , если устройству доступа к носителю требуется очистка; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-356">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="cd2c9-357">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-357">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-358">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-358">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-359">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-359">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-361">Максимальное количество отдельных носителей, которые могут быть поддерживаются или вставлены.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-361">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="cd2c9-362">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-362">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-363">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-364">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-366">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="cd2c9-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="cd2c9-367">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd2c9-368">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-370">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="cd2c9-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-372">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-372">The current statuses of the object.</span></span> <span data-ttu-id="cd2c9-373">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-374">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-374">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-375">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-377">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-377">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="cd2c9-378">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-378">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="cd2c9-379">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-380">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-380">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-381">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-381">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-383">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-383">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="cd2c9-384">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-385">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-385">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-386">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="cd2c9-386">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-388">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-388">The power management capabilities of the device.</span></span> <span data-ttu-id="cd2c9-389">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-390">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-390">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-391">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-391">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-393">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-393">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="cd2c9-394">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-395">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-395">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-396">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-398">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-398">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="cd2c9-399">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-400">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-400">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-401">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-403">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-403">Provides high level status information.</span></span> <span data-ttu-id="cd2c9-404">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-404">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="cd2c9-405">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-405">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd2c9-406">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-407">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-407">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-408">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-410">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-410">The last requested or desired state for the element.</span></span> <span data-ttu-id="cd2c9-411">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-411">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="cd2c9-412">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-412">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="cd2c9-413">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-413">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="cd2c9-414">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-414">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="cd2c9-415">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-415">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-416">**Безопасность**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-416">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-417">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-419">Операционная безопасность, определенная для устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-419">The operational security defined for the device.</span></span> <span data-ttu-id="cd2c9-420">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-420">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>



| <span data-ttu-id="cd2c9-421">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c9-421">Value</span></span>                                                                        | <span data-ttu-id="cd2c9-422">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c9-422">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="cd2c9-423"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c9-423"><dt>3</dt></span></span> </dl> | <span data-ttu-id="cd2c9-424">Нет</span><span class="sxs-lookup"><span data-stu-id="cd2c9-424">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd2c9-425">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-425">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-426">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-427">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-428">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-428">The current status of the object.</span></span> <span data-ttu-id="cd2c9-429">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-430">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-430">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-431">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-431">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-433">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="cd2c9-433">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="cd2c9-434">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="cd2c9-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-436">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-438">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-438">The current state of the logical device.</span></span> <span data-ttu-id="cd2c9-439">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-440">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-440">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-441">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-441">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-443">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-443">The scoping system's creation class name.</span></span> <span data-ttu-id="cd2c9-444">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-446">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-448">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-448">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="cd2c9-449">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-450">**тимеофластмаунт**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-450">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-451">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-451">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-452">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-453">Для устройства, которое поддерживает съемные носители, последняя Дата и время подключения носителя к устройству.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-453">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="cd2c9-454">Для устройств, обращающихся к несъемным носителям, например жестким дискам, это свойство не имеет смысла и неприменимо.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-454">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="cd2c9-455">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-455">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-456">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-456">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-457">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-459">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-459">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="cd2c9-460">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-460">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-461">**тоталмаунттиме**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-461">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-462">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-463">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-464">Для устройства, которое поддерживает съемные носители, общее время (в секундах) подключения носителя для передачи данных или очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-464">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="cd2c9-465">Для устройств, обращающихся к несъемным носителям, например к жестким дискам, это свойство неприменимо и должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-465">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="cd2c9-466">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-466">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-467">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-467">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-468">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-468">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-470">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-470">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="cd2c9-471">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-471">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-472">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-472">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-473">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-473">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-474">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-475">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-475">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="cd2c9-476">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-476">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-477">**ункомпресседдатарате**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-477">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-478">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-479">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-480">Постоянная скорость передачи данных (в КБ/с), которую устройство может читать и записывать на носитель.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-480">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="cd2c9-481">Это постоянная скорость необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-481">This is a sustained, raw data rate.</span></span> <span data-ttu-id="cd2c9-482">В этом свойстве не следует сообщать о максимальных тарифах или тарифах, имеющих значение сжатия.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-482">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="cd2c9-483">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-483">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-484">**унитсдескриптион**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-484">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-485">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-486">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-487">Единицы измерения относительно его использования в **максунитсбефореклеанинг**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-487">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="cd2c9-488">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-488">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-489">**унитсусед**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-489">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-490">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-490">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-491">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-492">Текущее количество используемых единиц.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-492">The current number of units used.</span></span> <span data-ttu-id="cd2c9-493">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-493">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd2c9-494">**унлоадтиме**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-494">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2c9-495">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-495">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2c9-496">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd2c9-497">Время в миллисекундах от возможности чтения или записи носителя в его выгрузку.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-497">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="cd2c9-498">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-498">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd2c9-499">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd2c9-499">Remarks</span></span>

<span data-ttu-id="cd2c9-500">Доступ к классу **\_ дискеттедриве мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="cd2c9-500">Access to the **Msvm\_DisketteDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cd2c9-501">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cd2c9-501">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2c9-502">Требования</span><span class="sxs-lookup"><span data-stu-id="cd2c9-502">Requirements</span></span>



| <span data-ttu-id="cd2c9-503">Требование</span><span class="sxs-lookup"><span data-stu-id="cd2c9-503">Requirement</span></span> | <span data-ttu-id="cd2c9-504">Значение</span><span class="sxs-lookup"><span data-stu-id="cd2c9-504">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2c9-505">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd2c9-505">Minimum supported client</span></span><br/> | <span data-ttu-id="cd2c9-506">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cd2c9-506">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cd2c9-507">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd2c9-507">Minimum supported server</span></span><br/> | <span data-ttu-id="cd2c9-508">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cd2c9-508">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd2c9-509">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cd2c9-509">Namespace</span></span><br/>                | <span data-ttu-id="cd2c9-510">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="cd2c9-510">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cd2c9-511">MOF</span><span class="sxs-lookup"><span data-stu-id="cd2c9-511">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd2c9-512"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c9-512"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd2c9-513">DLL</span><span class="sxs-lookup"><span data-stu-id="cd2c9-513">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd2c9-514"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd2c9-514"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd2c9-515">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd2c9-515">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2c9-516">**\_ДИСКЕТТЕДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-516">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="cd2c9-517">**\_ДИСКЕТТЕДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="cd2c9-517">**CIM\_DisketteDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskettedrive)
</dt> <dt>

[<span data-ttu-id="cd2c9-518">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="cd2c9-518">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

