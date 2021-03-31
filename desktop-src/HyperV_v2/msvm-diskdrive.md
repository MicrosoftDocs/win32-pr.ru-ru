---
description: Представляет жесткий диск внутри виртуальной машины.
ms.assetid: BF03CD02-7CDE-45E2-84D1-EC8E4457094A
title: Класс Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive
- Msvm_DiskDrive.SetPowerState
- Msvm_DiskDrive.EnableDevice
- Msvm_DiskDrive.OnlineDevice
- Msvm_DiskDrive.QuiesceDevice
- Msvm_DiskDrive.SaveProperties
- Msvm_DiskDrive.RestoreProperties
- Msvm_DiskDrive.InstanceID
- Msvm_DiskDrive.Caption
- Msvm_DiskDrive.Description
- Msvm_DiskDrive.ElementName
- Msvm_DiskDrive.InstallDate
- Msvm_DiskDrive.Name
- Msvm_DiskDrive.OperationalStatus
- Msvm_DiskDrive.StatusDescriptions
- Msvm_DiskDrive.Status
- Msvm_DiskDrive.HealthState
- Msvm_DiskDrive.CommunicationStatus
- Msvm_DiskDrive.DetailedStatus
- Msvm_DiskDrive.OperatingStatus
- Msvm_DiskDrive.PrimaryStatus
- Msvm_DiskDrive.EnabledState
- Msvm_DiskDrive.OtherEnabledState
- Msvm_DiskDrive.RequestedState
- Msvm_DiskDrive.EnabledDefault
- Msvm_DiskDrive.TimeOfLastStateChange
- Msvm_DiskDrive.AvailableRequestedStates
- Msvm_DiskDrive.TransitioningToState
- Msvm_DiskDrive.SystemCreationClassName
- Msvm_DiskDrive.SystemName
- Msvm_DiskDrive.CreationClassName
- Msvm_DiskDrive.DeviceID
- Msvm_DiskDrive.PowerManagementSupported
- Msvm_DiskDrive.PowerManagementCapabilities
- Msvm_DiskDrive.Availability
- Msvm_DiskDrive.StatusInfo
- Msvm_DiskDrive.LastErrorCode
- Msvm_DiskDrive.ErrorDescription
- Msvm_DiskDrive.ErrorCleared
- Msvm_DiskDrive.OtherIdentifyingInfo
- Msvm_DiskDrive.PowerOnHours
- Msvm_DiskDrive.TotalPowerOnHours
- Msvm_DiskDrive.IdentifyingDescriptions
- Msvm_DiskDrive.AdditionalAvailability
- Msvm_DiskDrive.MaxQuiesceTime
- Msvm_DiskDrive.Capabilities
- Msvm_DiskDrive.CapabilityDescriptions
- Msvm_DiskDrive.ErrorMethodology
- Msvm_DiskDrive.CompressionMethod
- Msvm_DiskDrive.NumberOfMediaSupported
- Msvm_DiskDrive.MaxMediaSize
- Msvm_DiskDrive.DefaultBlockSize
- Msvm_DiskDrive.MaxBlockSize
- Msvm_DiskDrive.MinBlockSize
- Msvm_DiskDrive.NeedsCleaning
- Msvm_DiskDrive.MediaIsLocked
- Msvm_DiskDrive.Security
- Msvm_DiskDrive.LastCleaned
- Msvm_DiskDrive.MaxAccessTime
- Msvm_DiskDrive.UncompressedDataRate
- Msvm_DiskDrive.LoadTime
- Msvm_DiskDrive.UnloadTime
- Msvm_DiskDrive.MountCount
- Msvm_DiskDrive.TimeOfLastMount
- Msvm_DiskDrive.TotalMountTime
- Msvm_DiskDrive.UnitsDescription
- Msvm_DiskDrive.MaxUnitsBeforeCleaning
- Msvm_DiskDrive.UnitsUsed
- Msvm_DiskDrive.DriveNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 60a08a2b73149285ddf3b0edf0003e5490b1c5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912576"
---
# <a name="msvm_diskdrive-class"></a><span data-ttu-id="9c970-103">\_Класс мсвм дискдриве</span><span class="sxs-lookup"><span data-stu-id="9c970-103">Msvm\_DiskDrive class</span></span>

<span data-ttu-id="9c970-104">Представляет жесткий диск внутри виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c970-104">Represents a hard disk drive inside of a virtual machine.</span></span> <span data-ttu-id="9c970-105">Это может быть транзитное устройство (если физический жесткий диск был подключен к виртуальной машине) или искусственное устройство, заполненное виртуальным жестким диском.</span><span class="sxs-lookup"><span data-stu-id="9c970-105">This hard disk drive can be either a pass-through device (if a physical hard disk was attached to the virtual machine) or a synthetic device that is populated with virtual hard disk media.</span></span> <span data-ttu-id="9c970-106">Так как виртуальные и физические жесткие диски можно добавлять и удалять с виртуальной машины, существует два пула ресурсов, связанных с этим классом, один для транзитных жестких дисков, а другой для виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="9c970-106">Because virtual and physical hard disks can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through hard disks and the other for virtual hard disks.</span></span> <span data-ttu-id="9c970-107">Жесткие диски можно добавлять в виртуальный SCSI-контроллер или удалять их только в том случае, если виртуальная машина находится в режиме «в сети».</span><span class="sxs-lookup"><span data-stu-id="9c970-107">Hard disks can only be added to or removed from the virtual SCSI controller when the virtual machine is online.</span></span> <span data-ttu-id="9c970-108">Диски можно добавлять или удалять только из виртуального IDE-контроллера, если виртуальная машина находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="9c970-108">Disks can only be added to or removed from the virtual IDE controller when the virtual machine is offline.</span></span>

<span data-ttu-id="9c970-109">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9c970-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c970-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c970-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskDrive : CIM_DiskDrive
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 2000000000;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = True;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint32   DriveNumber;
};
```

## <a name="members"></a><span data-ttu-id="9c970-111">Члены</span><span class="sxs-lookup"><span data-stu-id="9c970-111">Members</span></span>

<span data-ttu-id="9c970-112">Класс **мсвм \_ дискдриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9c970-112">The **Msvm\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="9c970-113">Методы</span><span class="sxs-lookup"><span data-stu-id="9c970-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c970-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c970-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c970-115">Методы</span><span class="sxs-lookup"><span data-stu-id="9c970-115">Methods</span></span>

<span data-ttu-id="9c970-116">Класс **мсвм \_ дискдриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9c970-116">The **Msvm\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="9c970-117">Метод</span><span class="sxs-lookup"><span data-stu-id="9c970-117">Method</span></span>                                                          | <span data-ttu-id="9c970-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9c970-118">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="9c970-119">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="9c970-119">**EnableDevice**</span></span>                                                | <span data-ttu-id="9c970-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9c970-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9c970-121">**локкмедиа**</span><span class="sxs-lookup"><span data-stu-id="9c970-121">**LockMedia**</span></span>](msvm-diskdrive-lockmedia.md)                   | <span data-ttu-id="9c970-122">Блокирует или освобождает носитель.</span><span class="sxs-lookup"><span data-stu-id="9c970-122">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="9c970-123">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="9c970-123">**OnlineDevice**</span></span>                                                | <span data-ttu-id="9c970-124">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9c970-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9c970-125">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="9c970-125">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="9c970-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9c970-126">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9c970-127">**Равен**</span><span class="sxs-lookup"><span data-stu-id="9c970-127">**RequestStateChange**</span></span>](msvm-diskdrive-requeststatechange.md) | <span data-ttu-id="9c970-128">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="9c970-128">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="9c970-129">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="9c970-129">**Reset**</span></span>](msvm-diskdrive-reset.md)                           | <span data-ttu-id="9c970-130">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="9c970-130">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="9c970-131">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="9c970-131">**RestoreProperties**</span></span>                                           | <span data-ttu-id="9c970-132">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9c970-132">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9c970-133">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="9c970-133">**SaveProperties**</span></span>                                              | <span data-ttu-id="9c970-134">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9c970-134">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9c970-135">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9c970-135">**SetPowerState**</span></span>                                               | <span data-ttu-id="9c970-136">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9c970-136">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9c970-137">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c970-137">Properties</span></span>

<span data-ttu-id="9c970-138">Класс **мсвм \_ дискдриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9c970-138">The **Msvm\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c970-139">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="9c970-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-140">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9c970-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c970-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-142">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="9c970-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-143">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="9c970-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-146">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9c970-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-147">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="9c970-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-148">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9c970-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c970-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-150">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9c970-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9c970-151">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c970-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-152">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="9c970-152">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-153">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9c970-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c970-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-155">Возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="9c970-155">The capabilities of the media access device.</span></span> <span data-ttu-id="9c970-156">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и задается для следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9c970-156">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="9c970-157">Значение</span><span class="sxs-lookup"><span data-stu-id="9c970-157">Value</span></span>                                                                        | <span data-ttu-id="9c970-158">Значение</span><span class="sxs-lookup"><span data-stu-id="9c970-158">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c970-159"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-159"><dt>3</dt></span></span> </dl> | <span data-ttu-id="9c970-160">Соответствующая запись в **капабилитидескриптионс** — "случайный доступ".</span><span class="sxs-lookup"><span data-stu-id="9c970-160">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>    |
| <dl> <span data-ttu-id="9c970-161"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-161"><dt>4</dt></span></span> </dl> | <span data-ttu-id="9c970-162">Соответствующая запись в **капабилитидескриптионс** имеет значение "поддерживает запись".</span><span class="sxs-lookup"><span data-stu-id="9c970-162">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9c970-163">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="9c970-163">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-164">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9c970-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c970-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-166">Массив строк произвольной формы, который содержит подробные объяснения для доступа к функциям устройств, указанным в массиве свойств **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="9c970-166">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="9c970-167">Каждая запись этого массива связана с записью в массиве свойств **capabilities** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="9c970-167">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="9c970-168">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="9c970-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-169">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9c970-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-172">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9c970-172">A short description of the object.</span></span> <span data-ttu-id="9c970-173">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-174">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="9c970-174">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-175">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-177">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="9c970-177">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9c970-178">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9c970-178">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9c970-179">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-179">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9c970-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9c970-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="9c970-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="9c970-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="9c970-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="9c970-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9c970-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9c970-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9c970-187">)</span><span class="sxs-lookup"><span data-stu-id="9c970-187">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c970-188">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="9c970-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-191">Строка, указывающая алгоритм или средство, используемые для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="9c970-191">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="9c970-192">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="9c970-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="9c970-193">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="9c970-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="9c970-194">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="9c970-194">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="9c970-195">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение "не сжато".</span><span class="sxs-lookup"><span data-stu-id="9c970-195">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="9c970-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9c970-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-197">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-199">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9c970-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9c970-200">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9c970-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-201">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="9c970-201">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-202">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-204">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="9c970-204">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="9c970-205">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и установлено в значение 512.</span><span class="sxs-lookup"><span data-stu-id="9c970-205">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-206">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9c970-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-209">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9c970-209">A description of the object.</span></span> <span data-ttu-id="9c970-210">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9c970-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-212">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-214">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="9c970-214">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9c970-215">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9c970-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9c970-216">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9c970-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="9c970-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="9c970-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="9c970-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="9c970-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="9c970-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="9c970-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9c970-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9c970-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9c970-225">)</span><span class="sxs-lookup"><span data-stu-id="9c970-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c970-226">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9c970-226">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-229">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9c970-229">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="9c970-230">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9c970-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-231">**дривенумбер**</span><span class="sxs-lookup"><span data-stu-id="9c970-231">**DriveNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-232">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c970-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-234">Количество физических дисков в системе размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="9c970-234">The number of the physical drives on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9c970-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-236">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-238">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="9c970-238">A display name for the object.</span></span> <span data-ttu-id="9c970-239">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-240">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="9c970-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-241">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-243">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="9c970-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9c970-244">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c970-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9c970-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-246">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-248">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="9c970-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9c970-249">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="9c970-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="9c970-250">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c970-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9c970-251">Значение</span><span class="sxs-lookup"><span data-stu-id="9c970-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9c970-252">Значение</span><span class="sxs-lookup"><span data-stu-id="9c970-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9c970-253"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9c970-254">Не удалось определить состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="9c970-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9c970-255"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="9c970-256"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="9c970-257">Элемент работает.</span><span class="sxs-lookup"><span data-stu-id="9c970-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="9c970-258"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9c970-259">Элемент отключен.</span><span class="sxs-lookup"><span data-stu-id="9c970-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="9c970-260"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="9c970-261">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="9c970-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="9c970-262"><dt>**Неприменимо**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="9c970-263">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="9c970-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="9c970-264"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="9c970-265">Элемент может выполнять команды, и при этом будут удалены все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="9c970-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="9c970-266"><dt>**В тесте**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="9c970-267">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="9c970-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="9c970-268"><dt>**Отложено**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="9c970-269">Элемент может быть выполнен с помощью команд, но он будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="9c970-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="9c970-270"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="9c970-271">Элемент включен, но находится в ограниченном режиме.</span><span class="sxs-lookup"><span data-stu-id="9c970-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="9c970-272">Поведение элемента аналогично включенному состоянию (2), но обрабатывает только ограниченный набор команд.</span><span class="sxs-lookup"><span data-stu-id="9c970-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="9c970-273">Все остальные запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="9c970-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="9c970-274"><dt>**Начало**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="9c970-275">Элемент находится в процессе перехода в состояние Enabled (2).</span><span class="sxs-lookup"><span data-stu-id="9c970-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="9c970-276">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="9c970-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="9c970-277">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="9c970-277">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-278">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9c970-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-280">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-281">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9c970-281">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-284">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-285">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="9c970-285">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-288">Строка, описывающая типы обнаружения ошибок и исправления, поддерживаемые этим устройством.</span><span class="sxs-lookup"><span data-stu-id="9c970-288">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="9c970-289">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение "None".</span><span class="sxs-lookup"><span data-stu-id="9c970-289">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "None".</span></span>

</dd> <dt>

<span data-ttu-id="9c970-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9c970-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-291">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-293">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="9c970-293">The current health of the element.</span></span> <span data-ttu-id="9c970-294">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="9c970-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9c970-295">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="9c970-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9c970-296">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="9c970-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-297">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9c970-297">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-298">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9c970-298">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c970-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-300">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9c970-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9c970-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-302">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c970-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-304">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c970-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="9c970-305">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9c970-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c970-309">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="9c970-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9c970-310">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="9c970-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9c970-311">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-312">**ластклеанед**</span><span class="sxs-lookup"><span data-stu-id="9c970-312">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-313">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c970-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-315">Дата и время последней очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="9c970-315">The date and time when the device was last cleaned.</span></span> <span data-ttu-id="9c970-316">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9c970-316">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-317">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="9c970-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-318">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c970-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-320">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-321">**лоадтиме**</span><span class="sxs-lookup"><span data-stu-id="9c970-321">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-322">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-324">Время в миллисекундах от загрузки до возможности чтения или записи носителя.</span><span class="sxs-lookup"><span data-stu-id="9c970-324">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="9c970-325">Например, для дисков это интервал между диском, который не передается на диск, сообщает, что он готов для чтения и записи (т. е. диск вращается с номинальной скоростью).</span><span class="sxs-lookup"><span data-stu-id="9c970-325">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="9c970-326">Для ленточных накопителей это время с носителя, добавляемого для сообщения о готовности к работе для приложения.</span><span class="sxs-lookup"><span data-stu-id="9c970-326">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="9c970-327">Обычно это в области BOT ленты.</span><span class="sxs-lookup"><span data-stu-id="9c970-327">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="9c970-328">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) и имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c970-328">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-329">**максакцесстиме**</span><span class="sxs-lookup"><span data-stu-id="9c970-329">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-330">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-332">Время (в миллисекундах) перехода с первого места на носителе к расположению, которое находится в самом начале относительно времени.</span><span class="sxs-lookup"><span data-stu-id="9c970-332">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="9c970-333">Для диска это означает полный поиск и полную задержку вращения.</span><span class="sxs-lookup"><span data-stu-id="9c970-333">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="9c970-334">Для ленточных накопителей этот элемент представляет собой поиск с начала ленты до наиболее физической отдаленной точки.</span><span class="sxs-lookup"><span data-stu-id="9c970-334">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="9c970-335">(Конец ленты может находиться в самой физической точке, но это не обязательно верно). Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c970-335">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-336">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="9c970-336">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-337">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-339">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="9c970-339">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="9c970-340">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 512 для виртуальных жестких дисков, переменная для сквозных дисков.</span><span class="sxs-lookup"><span data-stu-id="9c970-340">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-341">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="9c970-341">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-342">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-344">Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="9c970-344">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="9c970-345">Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024).</span><span class="sxs-lookup"><span data-stu-id="9c970-345">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="9c970-346">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 2 000 000 000 для виртуальных жестких дисков, переменная для сквозных дисков.</span><span class="sxs-lookup"><span data-stu-id="9c970-346">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 2,000,000,000 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-347">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="9c970-347">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-348">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-350">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-351">**максунитсбефореклеанинг**</span><span class="sxs-lookup"><span data-stu-id="9c970-351">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-352">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-354">Максимальное число единиц, которое можно использовать до очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="9c970-354">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="9c970-355">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="9c970-355">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0xffffffffffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-356">**медиаислоккед**</span><span class="sxs-lookup"><span data-stu-id="9c970-356">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-357">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9c970-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-359">**Значение true** , если носитель заблокирован на устройстве и не может быть извлечен. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9c970-359">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="9c970-360">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="9c970-360">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-361">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="9c970-361">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-362">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-362">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-364">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="9c970-364">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="9c970-365">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и установлено в значение 512.</span><span class="sxs-lookup"><span data-stu-id="9c970-365">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-366">**маунткаунт**</span><span class="sxs-lookup"><span data-stu-id="9c970-366">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-367">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-369">Для устройства, которое поддерживает съемные носители, число подключенных носителей для передачи данных или очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="9c970-369">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="9c970-370">Для устройств, обращающихся к несъемным носителям, например к жестким дискам, это свойство неприменимо и должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c970-370">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="9c970-371">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c970-371">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-372">**Name**</span><span class="sxs-lookup"><span data-stu-id="9c970-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-373">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-375">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="9c970-375">The label by which the object is known.</span></span> <span data-ttu-id="9c970-376">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-377">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="9c970-377">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-378">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9c970-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-379">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-380">**Значение true** , если устройству доступа к носителю требуется очистка; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9c970-380">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="9c970-381">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="9c970-381">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-382">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="9c970-382">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-383">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c970-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-385">Максимальное количество отдельных носителей, которые могут быть поддерживаются или вставлены.</span><span class="sxs-lookup"><span data-stu-id="9c970-385">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="9c970-386">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="9c970-386">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-387">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="9c970-387">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-388">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-390">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9c970-390">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9c970-391">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9c970-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9c970-392">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9c970-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9c970-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="9c970-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="9c970-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="9c970-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="9c970-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="9c970-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="9c970-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="9c970-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="9c970-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="9c970-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="9c970-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="9c970-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="9c970-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="9c970-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="9c970-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="9c970-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="9c970-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9c970-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9c970-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9c970-412">)</span><span class="sxs-lookup"><span data-stu-id="9c970-412">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c970-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9c970-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-414">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9c970-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c970-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-416">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9c970-416">The current statuses of the object.</span></span> <span data-ttu-id="9c970-417">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-418">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="9c970-418">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-419">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-421">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="9c970-421">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9c970-422">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="9c970-422">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9c970-423">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9c970-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-424">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9c970-424">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-425">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9c970-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c970-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-427">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9c970-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-428">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="9c970-428">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-429">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9c970-429">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9c970-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-431">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-432">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="9c970-432">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-433">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9c970-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-435">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-436">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="9c970-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-437">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-438">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-439">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-440">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="9c970-440">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-441">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-443">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="9c970-443">Provides high level status information.</span></span> <span data-ttu-id="9c970-444">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="9c970-444">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9c970-445">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="9c970-445">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9c970-446">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-446">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9c970-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9c970-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-448"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="9c970-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="9c970-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="9c970-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9c970-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9c970-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9c970-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9c970-453">)</span><span class="sxs-lookup"><span data-stu-id="9c970-453">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c970-454">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9c970-454">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-455">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-456">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-457">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="9c970-457">The last requested or desired state for the element.</span></span> <span data-ttu-id="9c970-458">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="9c970-458">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9c970-459">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="9c970-459">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="9c970-460">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9c970-460">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="9c970-461">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="9c970-461">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="9c970-462">Это свойство наследуется от **CIM \_ енабледлогикалелемент**.</span><span class="sxs-lookup"><span data-stu-id="9c970-462">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-463">**Безопасность**</span><span class="sxs-lookup"><span data-stu-id="9c970-463">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-464">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-466">Операционная безопасность, определенная для устройства.</span><span class="sxs-lookup"><span data-stu-id="9c970-466">The operational security defined for the device.</span></span> <span data-ttu-id="9c970-467">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 3 (нет).</span><span class="sxs-lookup"><span data-stu-id="9c970-467">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 3 (None).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-468">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9c970-468">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-469">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-471">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-472">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="9c970-472">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-473">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9c970-473">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9c970-474">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-475">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9c970-475">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9c970-476">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9c970-476">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9c970-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-478">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-479">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-480">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-480">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-481">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="9c970-481">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-482">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-483">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-484">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="9c970-484">The scoping system's creation class name.</span></span> <span data-ttu-id="9c970-485">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9c970-485">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9c970-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-488">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-489">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c970-489">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="9c970-490">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9c970-490">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-491">**тимеофластмаунт**</span><span class="sxs-lookup"><span data-stu-id="9c970-491">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-492">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c970-492">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-493">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-494">Для устройства, которое поддерживает съемные носители, последняя Дата и время подключения носителя к устройству.</span><span class="sxs-lookup"><span data-stu-id="9c970-494">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="9c970-495">Для устройств, обращающихся к несъемным носителям, например жестким дискам, это свойство не имеет смысла и неприменимо.</span><span class="sxs-lookup"><span data-stu-id="9c970-495">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="9c970-496">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9c970-496">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-497">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="9c970-497">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-498">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9c970-498">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-499">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-500">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="9c970-500">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9c970-501">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение "null".</span><span class="sxs-lookup"><span data-stu-id="9c970-501">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="9c970-502">**тоталмаунттиме**</span><span class="sxs-lookup"><span data-stu-id="9c970-502">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-503">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-503">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-504">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-505">Для устройства, которое поддерживает съемные носители, общее время (в секундах) подключения носителя для передачи данных или очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="9c970-505">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="9c970-506">Для устройств, обращающихся к несъемным носителям, например к жестким дискам, это свойство неприменимо и должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c970-506">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="9c970-507">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c970-507">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-508">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="9c970-508">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-509">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-509">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-510">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-511">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="9c970-511">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-512">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="9c970-512">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-513">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9c970-513">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-514">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-515">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="9c970-515">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9c970-516">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c970-516">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c970-517">**ункомпресседдатарате**</span><span class="sxs-lookup"><span data-stu-id="9c970-517">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-518">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c970-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-520">Постоянная скорость передачи данных в КБ/с, которую устройство может читать и записывать на носитель.</span><span class="sxs-lookup"><span data-stu-id="9c970-520">The sustained data transfer rate in KB/sec that the device can read from and write to a media.</span></span> <span data-ttu-id="9c970-521">Это постоянная скорость необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="9c970-521">This is a sustained, raw data rate.</span></span> <span data-ttu-id="9c970-522">В этом свойстве не следует сообщать о максимальных тарифах или тарифах, имеющих значение сжатия.</span><span class="sxs-lookup"><span data-stu-id="9c970-522">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="9c970-523">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9c970-523">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-524">**унитсдескриптион**</span><span class="sxs-lookup"><span data-stu-id="9c970-524">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-525">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9c970-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-526">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-527">Единицы измерения относительно его использования в **максунитсбефореклеанинг**.</span><span class="sxs-lookup"><span data-stu-id="9c970-527">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="9c970-528">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9c970-528">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-529">**унитсусед**</span><span class="sxs-lookup"><span data-stu-id="9c970-529">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-530">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-531">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-532">Текущее количество используемых единиц.</span><span class="sxs-lookup"><span data-stu-id="9c970-532">The current number of units used.</span></span> <span data-ttu-id="9c970-533">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c970-533">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9c970-534">**унлоадтиме**</span><span class="sxs-lookup"><span data-stu-id="9c970-534">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c970-535">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9c970-535">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c970-536">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9c970-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c970-537">Время в миллисекундах от возможности чтения или записи носителя в выгрузке.</span><span class="sxs-lookup"><span data-stu-id="9c970-537">The time, in milliseconds, from being able to read or write a media to its unload.</span></span> <span data-ttu-id="9c970-538">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="9c970-538">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c970-539">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c970-539">Remarks</span></span>

<span data-ttu-id="9c970-540">Доступ к классу **\_ дискдриве мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="9c970-540">Access to the **Msvm\_DiskDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9c970-541">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9c970-541">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c970-542">Требования</span><span class="sxs-lookup"><span data-stu-id="9c970-542">Requirements</span></span>



| <span data-ttu-id="9c970-543">Требование</span><span class="sxs-lookup"><span data-stu-id="9c970-543">Requirement</span></span> | <span data-ttu-id="9c970-544">Значение</span><span class="sxs-lookup"><span data-stu-id="9c970-544">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c970-545">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c970-545">Minimum supported client</span></span><br/> | <span data-ttu-id="9c970-546">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9c970-546">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9c970-547">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c970-547">Minimum supported server</span></span><br/> | <span data-ttu-id="9c970-548">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9c970-548">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c970-549">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9c970-549">Namespace</span></span><br/>                | <span data-ttu-id="9c970-550">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9c970-550">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9c970-551">MOF</span><span class="sxs-lookup"><span data-stu-id="9c970-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c970-552"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-552"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c970-553">DLL</span><span class="sxs-lookup"><span data-stu-id="9c970-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c970-554"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c970-554"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c970-555">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c970-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c970-556">**\_ДИСКДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="9c970-556">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="9c970-557">**\_ДИСКДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="9c970-557">**CIM\_DiskDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskdrive)
</dt> <dt>

[<span data-ttu-id="9c970-558">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="9c970-558">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

