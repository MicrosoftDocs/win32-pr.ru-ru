---
description: Представляет DVD-дисковод в виртуальной машине.
ms.assetid: BA813950-436F-46F1-8C1F-79C5AB1A459B
title: Класс Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive
- Msvm_DVDDrive.SetPowerState
- Msvm_DVDDrive.EnableDevice
- Msvm_DVDDrive.OnlineDevice
- Msvm_DVDDrive.QuiesceDevice
- Msvm_DVDDrive.SaveProperties
- Msvm_DVDDrive.RestoreProperties
- Msvm_DVDDrive.InstanceID
- Msvm_DVDDrive.Caption
- Msvm_DVDDrive.Description
- Msvm_DVDDrive.ElementName
- Msvm_DVDDrive.InstallDate
- Msvm_DVDDrive.Name
- Msvm_DVDDrive.OperationalStatus
- Msvm_DVDDrive.StatusDescriptions
- Msvm_DVDDrive.Status
- Msvm_DVDDrive.HealthState
- Msvm_DVDDrive.CommunicationStatus
- Msvm_DVDDrive.DetailedStatus
- Msvm_DVDDrive.OperatingStatus
- Msvm_DVDDrive.PrimaryStatus
- Msvm_DVDDrive.EnabledState
- Msvm_DVDDrive.OtherEnabledState
- Msvm_DVDDrive.RequestedState
- Msvm_DVDDrive.EnabledDefault
- Msvm_DVDDrive.TimeOfLastStateChange
- Msvm_DVDDrive.AvailableRequestedStates
- Msvm_DVDDrive.TransitioningToState
- Msvm_DVDDrive.SystemCreationClassName
- Msvm_DVDDrive.SystemName
- Msvm_DVDDrive.CreationClassName
- Msvm_DVDDrive.DeviceID
- Msvm_DVDDrive.PowerManagementSupported
- Msvm_DVDDrive.PowerManagementCapabilities
- Msvm_DVDDrive.Availability
- Msvm_DVDDrive.StatusInfo
- Msvm_DVDDrive.LastErrorCode
- Msvm_DVDDrive.ErrorDescription
- Msvm_DVDDrive.ErrorCleared
- Msvm_DVDDrive.OtherIdentifyingInfo
- Msvm_DVDDrive.PowerOnHours
- Msvm_DVDDrive.TotalPowerOnHours
- Msvm_DVDDrive.IdentifyingDescriptions
- Msvm_DVDDrive.AdditionalAvailability
- Msvm_DVDDrive.MaxQuiesceTime
- Msvm_DVDDrive.Capabilities
- Msvm_DVDDrive.CapabilityDescriptions
- Msvm_DVDDrive.ErrorMethodology
- Msvm_DVDDrive.CompressionMethod
- Msvm_DVDDrive.NumberOfMediaSupported
- Msvm_DVDDrive.MaxMediaSize
- Msvm_DVDDrive.DefaultBlockSize
- Msvm_DVDDrive.MaxBlockSize
- Msvm_DVDDrive.MinBlockSize
- Msvm_DVDDrive.NeedsCleaning
- Msvm_DVDDrive.MediaIsLocked
- Msvm_DVDDrive.Security
- Msvm_DVDDrive.LastCleaned
- Msvm_DVDDrive.MaxAccessTime
- Msvm_DVDDrive.UncompressedDataRate
- Msvm_DVDDrive.LoadTime
- Msvm_DVDDrive.UnloadTime
- Msvm_DVDDrive.MountCount
- Msvm_DVDDrive.TimeOfLastMount
- Msvm_DVDDrive.TotalMountTime
- Msvm_DVDDrive.UnitsDescription
- Msvm_DVDDrive.MaxUnitsBeforeCleaning
- Msvm_DVDDrive.UnitsUsed
- Msvm_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e4b3c9006babb2c7e18b6aed6e85cbee47299429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912572"
---
# <a name="msvm_dvddrive-class"></a><span data-ttu-id="c4405-103">\_Класс мсвм двддриве</span><span class="sxs-lookup"><span data-stu-id="c4405-103">Msvm\_DVDDrive class</span></span>

<span data-ttu-id="c4405-104">Представляет DVD-дисковод в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c4405-104">Represents a DVD drive inside of a virtual machine.</span></span> <span data-ttu-id="c4405-105">Этот DVD-дисковод может быть транзитным (если физический жесткий диск был подключен к виртуальной машине) или искусственным и заполнен ISO-файлом носителя.</span><span class="sxs-lookup"><span data-stu-id="c4405-105">This DVD drive can either be a pass-through device (if a physical hard disk was attached to the virtual machine) or synthetic and populated with ISO file media.</span></span> <span data-ttu-id="c4405-106">Так как виртуальные и физические DVD-дисководы можно добавлять и удалять с виртуальной машины, существует два пула ресурсов, связанных с этим классом, один для транзитных DVD-дисков, а другой — для виртуальных DVD-дисководов.</span><span class="sxs-lookup"><span data-stu-id="c4405-106">Because virtual and physical DVD drives can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through DVD drives, and the other for virtual DVD drives.</span></span> <span data-ttu-id="c4405-107">DVD-дисководы можно добавлять или удалять только в том случае, если виртуальная машина находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="c4405-107">DVD drives can only be added or removed if the virtual machine is offline.</span></span>

<span data-ttu-id="c4405-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c4405-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4405-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4405-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DVDDrive : CIM_DVDDrive
{
  string   InstanceID;
  string   Caption = "DVD Drive";
  string   Description = "Microsoft Virtual DVD Drive";
  string   ElementName = "DVD Drive";
  datetime InstallDate;
  string   Name = "DVD Drive";
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
  uint16   CreationClassName = "Msvm_DVDDrive";
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
  uint32   Capabilities[] = {3, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Removable Media"};
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 9400000;
  uint64   DefaultBlockSize = 2048;
  uint64   MaxBlockSize = 2048;
  uint64   MinBlockSize = 2048;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint16   FormatsSupported[] = {16, 22};
};
```

## <a name="members"></a><span data-ttu-id="c4405-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c4405-110">Members</span></span>

<span data-ttu-id="c4405-111">Класс **мсвм \_ двддриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c4405-111">The **Msvm\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="c4405-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c4405-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4405-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4405-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c4405-114">Методы</span><span class="sxs-lookup"><span data-stu-id="c4405-114">Methods</span></span>

<span data-ttu-id="c4405-115">Класс **мсвм \_ двддриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c4405-115">The **Msvm\_DVDDrive** class has these methods.</span></span>



| <span data-ttu-id="c4405-116">Метод</span><span class="sxs-lookup"><span data-stu-id="c4405-116">Method</span></span>                                                         | <span data-ttu-id="c4405-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c4405-117">Description</span></span>                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="c4405-118">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="c4405-118">**EnableDevice**</span></span>                                               | <span data-ttu-id="c4405-119">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c4405-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="c4405-120">**локкмедиа**</span><span class="sxs-lookup"><span data-stu-id="c4405-120">**LockMedia**</span></span>](msvm-dvddrive-lockmedia.md)                   | <span data-ttu-id="c4405-121">Блокирует или освобождает носитель.</span><span class="sxs-lookup"><span data-stu-id="c4405-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="c4405-122">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="c4405-122">**OnlineDevice**</span></span>                                               | <span data-ttu-id="c4405-123">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c4405-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c4405-124">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="c4405-124">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="c4405-125">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c4405-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="c4405-126">**Равен**</span><span class="sxs-lookup"><span data-stu-id="c4405-126">**RequestStateChange**</span></span>](msvm-dvddrive-requeststatechange.md) | <span data-ttu-id="c4405-127">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="c4405-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="c4405-128">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="c4405-128">**Reset**</span></span>](msvm-dvddrive-reset.md)                           | <span data-ttu-id="c4405-129">Сбрасывает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="c4405-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="c4405-130">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="c4405-130">**RestoreProperties**</span></span>                                          | <span data-ttu-id="c4405-131">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c4405-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c4405-132">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="c4405-132">**SaveProperties**</span></span>                                             | <span data-ttu-id="c4405-133">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c4405-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c4405-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c4405-134">**SetPowerState**</span></span>                                              | <span data-ttu-id="c4405-135">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c4405-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c4405-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4405-136">Properties</span></span>

<span data-ttu-id="c4405-137">Класс **мсвм \_ двддриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c4405-137">The **Msvm\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4405-138">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="c4405-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-139">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c4405-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-141">Любая дополнительная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="c4405-142">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="c4405-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-143">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="c4405-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-146">Первичная доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-146">The primary availability and status of the device.</span></span> <span data-ttu-id="c4405-147">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение 6 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="c4405-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-148">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="c4405-148">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-149">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c4405-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-151">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="c4405-151">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="c4405-152">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c4405-152">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="c4405-153">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="c4405-153">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="c4405-154">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="c4405-154">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="c4405-155">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4405-155">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-156">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c4405-156">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-157">Тип данных: массив **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4405-157">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-159">Возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="c4405-159">The capabilities of the media access device.</span></span> <span data-ttu-id="c4405-160">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и задается для следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c4405-160">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="c4405-161">Значение</span><span class="sxs-lookup"><span data-stu-id="c4405-161">Value</span></span>                                                                             | <span data-ttu-id="c4405-162">Значение</span><span class="sxs-lookup"><span data-stu-id="c4405-162">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4405-163"><dt>{3, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="c4405-163"><dt>{3, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="c4405-164"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c4405-164"><dt>3</dt></span></span> </dl>      | <span data-ttu-id="c4405-165">Соответствующая запись в **капабилитидескриптионс** — "случайный доступ".</span><span class="sxs-lookup"><span data-stu-id="c4405-165">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="c4405-166"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c4405-166"><dt>7</dt></span></span> </dl>      | <span data-ttu-id="c4405-167">Соответствующая запись в **капабилитидескриптионс** — "поддерживает съемные носители".</span><span class="sxs-lookup"><span data-stu-id="c4405-167">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c4405-168">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="c4405-168">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-169">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c4405-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-171">Массив строк произвольной формы, который содержит подробные объяснения для доступа к функциям устройств, указанным в массиве свойств **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="c4405-171">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="c4405-172">Каждая запись этого массива связана с записью в массиве свойств **capabilities** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="c4405-172">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="c4405-173">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-173">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-174">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c4405-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-177">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c4405-177">A short description of the object.</span></span> <span data-ttu-id="c4405-178">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-179">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="c4405-179">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-180">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-182">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="c4405-182">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c4405-183">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c4405-183">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4405-184">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-184">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-185">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="c4405-185">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-188">Строка, указывающая алгоритм или средство, используемые для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="c4405-188">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="c4405-189">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="c4405-189">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="c4405-190">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="c4405-190">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="c4405-191">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="c4405-191">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="c4405-192">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-192">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="c4405-193">"Не сжато"</span><span class="sxs-lookup"><span data-stu-id="c4405-193">"Not Compressed"</span></span>

<span data-ttu-id="c4405-194">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="c4405-194">"Unknown"</span></span>

<span data-ttu-id="c4405-195">Сжатия</span><span class="sxs-lookup"><span data-stu-id="c4405-195">"Compressed"</span></span>

<span data-ttu-id="c4405-196">"Не сжато"</span><span class="sxs-lookup"><span data-stu-id="c4405-196">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="c4405-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c4405-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-198">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-200">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c4405-200">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c4405-201">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c4405-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-202">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="c4405-202">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-203">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-205">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="c4405-205">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="c4405-206">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-206">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-207">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c4405-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-210">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c4405-210">A description of the object.</span></span> <span data-ttu-id="c4405-211">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-212">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c4405-212">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-213">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-215">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="c4405-215">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c4405-216">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c4405-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4405-217">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-218">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c4405-218">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-221">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение «Microsoft:*GUID* \\ *устройства-данные*».</span><span class="sxs-lookup"><span data-stu-id="c4405-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="c4405-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c4405-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-225">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c4405-225">A display name for the object.</span></span> <span data-ttu-id="c4405-226">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-227">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="c4405-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-228">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-230">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c4405-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c4405-231">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4405-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-232">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c4405-232">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-233">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-235">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c4405-235">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c4405-236">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="c4405-236">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c4405-237">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4405-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-238">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="c4405-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-239">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c4405-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-240">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-241">Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="c4405-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="c4405-242">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c4405-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-246">Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="c4405-246">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="c4405-247">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-248">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="c4405-248">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-251">Строка, описывающая типы обнаружения ошибок и исправления, поддерживаемые этим устройством.</span><span class="sxs-lookup"><span data-stu-id="c4405-251">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="c4405-252">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-252">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-253">**форматссуппортед**</span><span class="sxs-lookup"><span data-stu-id="c4405-253">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-254">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c4405-254">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-256">Форматы компакт-дисков и DVD-дисков, поддерживаемые этим устройством.</span><span class="sxs-lookup"><span data-stu-id="c4405-256">The CD and DVD formats that are supported by this device.</span></span> <span data-ttu-id="c4405-257">Это свойство наследуется от [**CIM \_ двддриве**](/previous-versions//cc136812(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4405-257">This property is inherited from [**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85)).</span></span>

<span data-ttu-id="c4405-258">Этот массив содержит следующие значения для ISO.</span><span class="sxs-lookup"><span data-stu-id="c4405-258">This array contains the following values for ISO.</span></span>

<dl> <dt>

<span data-ttu-id="c4405-259">{16, 22}</span><span class="sxs-lookup"><span data-stu-id="c4405-259">{16, 22}</span></span>
</dt> <dt>

<span data-ttu-id="c4405-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**Компакт-** диск (16)</span><span class="sxs-lookup"><span data-stu-id="c4405-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-261"><span id="DVD"></span><span id="dvd"></span>**DVD-диск** (22)</span><span class="sxs-lookup"><span data-stu-id="c4405-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> </dl>

<span data-ttu-id="c4405-262">Этот массив содержит следующие значения для физического сквозного передачи.</span><span class="sxs-lookup"><span data-stu-id="c4405-262">This array contains the following values for physical pass-through.</span></span>

<dl> <dt>

<span data-ttu-id="c4405-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c4405-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c4405-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**Компакт-** диск (16)</span><span class="sxs-lookup"><span data-stu-id="c4405-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="c4405-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-267"><span id="CD-I"></span><span id="cd-i"></span>**Компакт-I** (18)</span><span class="sxs-lookup"><span data-stu-id="c4405-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**Записываемый компакт-диск** (19)</span><span class="sxs-lookup"><span data-stu-id="c4405-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-269"><span id="DVD"></span><span id="dvd"></span>**DVD-диск** (22)</span><span class="sxs-lookup"><span data-stu-id="c4405-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW +** (23)</span><span class="sxs-lookup"><span data-stu-id="c4405-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW+** (23)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="c4405-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="c4405-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-видео** (26)</span><span class="sxs-lookup"><span data-stu-id="c4405-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Дивкс** (27)</span><span class="sxs-lookup"><span data-stu-id="c4405-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="c4405-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span><span class="sxs-lookup"><span data-stu-id="c4405-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-277"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="c4405-277"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**Записываемый DVD-диск** (36)</span><span class="sxs-lookup"><span data-stu-id="c4405-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="c4405-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**Аудио DVD** (38)</span><span class="sxs-lookup"><span data-stu-id="c4405-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="c4405-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="c4405-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="c4405-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>
</dt> <dt>

<span data-ttu-id="c4405-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="c4405-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c4405-285">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c4405-285">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-286">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-288">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="c4405-288">The current health of the element.</span></span> <span data-ttu-id="c4405-289">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c4405-289">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c4405-290">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="c4405-290">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c4405-291">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-292">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c4405-292">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-293">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c4405-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-295">Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="c4405-295">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="c4405-296">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c4405-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c4405-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-298">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4405-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-300">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4405-300">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c4405-301">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-302">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c4405-302">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4405-305">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c4405-305">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c4405-306">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c4405-306">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c4405-307">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-307">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-308">**ластклеанед**</span><span class="sxs-lookup"><span data-stu-id="c4405-308">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-309">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4405-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-311">Дата и время последней очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-311">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="c4405-312">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-312">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-313">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="c4405-313">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-314">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4405-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-316">Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="c4405-316">The last error code reported by the logical device.</span></span> <span data-ttu-id="c4405-317">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-317">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-318">**лоадтиме**</span><span class="sxs-lookup"><span data-stu-id="c4405-318">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-319">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-321">Время в миллисекундах от "Load" до возможности чтения или записи мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c4405-321">The time, in milliseconds, from 'load' to being able to read or write a media.</span></span> <span data-ttu-id="c4405-322">Например, для дисков это интервал между диском, который не передается на диск, сообщает, что он готов для чтения и записи (т. е. диск вращается с номинальной скоростью).</span><span class="sxs-lookup"><span data-stu-id="c4405-322">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="c4405-323">Для ленточных накопителей это время с носителя, добавляемого для сообщения о готовности к работе для приложения.</span><span class="sxs-lookup"><span data-stu-id="c4405-323">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="c4405-324">Обычно это в области BOT ленты.</span><span class="sxs-lookup"><span data-stu-id="c4405-324">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="c4405-325">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-325">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-326">**максакцесстиме**</span><span class="sxs-lookup"><span data-stu-id="c4405-326">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-327">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-329">Время (в миллисекундах) перехода с первого места на носителе к расположению, которое находится в самом начале относительно времени.</span><span class="sxs-lookup"><span data-stu-id="c4405-329">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="c4405-330">Для дискового накопителя это соответствует полной и полной задержке при повороте.</span><span class="sxs-lookup"><span data-stu-id="c4405-330">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="c4405-331">Для ленточных накопителей этот элемент представляет собой поиск с начала ленты до наиболее физической отдаленной точки.</span><span class="sxs-lookup"><span data-stu-id="c4405-331">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="c4405-332">(Конец ленты может находиться в самой физической точке, но это не обязательно верно). Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-332">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-333">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="c4405-333">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-334">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-336">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="c4405-336">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="c4405-337">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-337">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-338">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="c4405-338">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-339">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-341">Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="c4405-341">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="c4405-342">Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024).</span><span class="sxs-lookup"><span data-stu-id="c4405-342">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="c4405-343">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-343">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-344">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="c4405-344">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-345">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-347">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c4405-347">This property has been deprecated.</span></span> <span data-ttu-id="c4405-348">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-349">**максунитсбефореклеанинг**</span><span class="sxs-lookup"><span data-stu-id="c4405-349">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-350">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-352">Максимальное число единиц, которое можно использовать до очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-352">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="c4405-353">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-353">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-354">**медиаислоккед**</span><span class="sxs-lookup"><span data-stu-id="c4405-354">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-355">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c4405-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-357">**Значение true** , если носитель заблокирован на устройстве и не может быть извлечен. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c4405-357">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="c4405-358">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-358">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-359">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="c4405-359">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-360">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-362">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="c4405-362">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="c4405-363">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-363">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-364">**маунткаунт**</span><span class="sxs-lookup"><span data-stu-id="c4405-364">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-365">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-367">Для устройства, которое поддерживает съемные носители, число подключенных носителей для передачи данных или очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-367">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="c4405-368">Для устройств, обращающихся к несъемным носителям, например к жестким дискам, это свойство неприменимо и должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="c4405-368">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="c4405-369">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-369">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-370">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4405-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-371">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-373">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="c4405-373">The label by which the object is known.</span></span> <span data-ttu-id="c4405-374">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="c4405-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-375">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="c4405-375">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-376">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c4405-376">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-378">**Значение true** , если устройству доступа к носителю требуется очистка; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c4405-378">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="c4405-379">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-379">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-380">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="c4405-380">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-381">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4405-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-383">Максимальное количество отдельных носителей, которые могут быть поддерживаются или вставлены.</span><span class="sxs-lookup"><span data-stu-id="c4405-383">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="c4405-384">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-384">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-385">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="c4405-385">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-386">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-388">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c4405-388">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c4405-389">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c4405-389">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4405-390">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-391">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c4405-391">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-392">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c4405-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-394">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c4405-394">The current statuses of the object.</span></span> <span data-ttu-id="c4405-395">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-395">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-396">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="c4405-396">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-397">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-398">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-399">Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="c4405-399">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="c4405-400">Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="c4405-400">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="c4405-401">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4405-401">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c4405-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-403">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c4405-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-405">Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-405">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c4405-406">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c4405-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-407">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="c4405-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-408">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c4405-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-410">Возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-410">The power management capabilities of the device.</span></span> <span data-ttu-id="c4405-411">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-412">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="c4405-412">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-413">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c4405-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-415">Указывает, можно ли управлять питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-415">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="c4405-416">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-416">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-417">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="c4405-417">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-418">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-420">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="c4405-420">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="c4405-421">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-422">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="c4405-422">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-423">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-425">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="c4405-425">Provides high level status information.</span></span> <span data-ttu-id="c4405-426">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="c4405-426">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="c4405-427">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="c4405-427">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4405-428">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-428">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-429">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c4405-429">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-430">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-430">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-432">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="c4405-432">The last requested or desired state for the element.</span></span> <span data-ttu-id="c4405-433">Фактическое состояние элемента представлено свойством **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c4405-433">The actual state of the element is represented by the **EnabledState** property.</span></span> <span data-ttu-id="c4405-434">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="c4405-434">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="c4405-435">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="c4405-435">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="c4405-436">В этом случае используется значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="c4405-436">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="c4405-437">Это свойство наследуется от **CIM \_ енабледлогикалелемент**.</span><span class="sxs-lookup"><span data-stu-id="c4405-437">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-438">**Безопасность**</span><span class="sxs-lookup"><span data-stu-id="c4405-438">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-439">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-441">Операционная безопасность, определенная для устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-441">The operational security defined for the device.</span></span> <span data-ttu-id="c4405-442">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-442">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-443">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c4405-443">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-444">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-445">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-446">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c4405-446">The current status of the object.</span></span> <span data-ttu-id="c4405-447">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-448">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="c4405-448">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-449">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c4405-449">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4405-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-451">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c4405-451">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c4405-452">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4405-452">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c4405-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-454">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-456">Текущее состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-456">The current state of the logical device.</span></span> <span data-ttu-id="c4405-457">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-458">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c4405-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-459">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-461">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="c4405-461">The scoping system's creation class name.</span></span> <span data-ttu-id="c4405-462">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c4405-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-463">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c4405-463">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-464">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-466">Уникальный идентификатор для области виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c4405-466">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="c4405-467">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c4405-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-468">**тимеофластмаунт**</span><span class="sxs-lookup"><span data-stu-id="c4405-468">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-469">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4405-469">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-471">Для устройства, которое поддерживает съемные носители, последняя Дата и время подключения носителя к устройству.</span><span class="sxs-lookup"><span data-stu-id="c4405-471">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="c4405-472">Для устройств, обращающихся к несъемным носителям, например жестким дискам, это свойство не имеет смысла и неприменимо.</span><span class="sxs-lookup"><span data-stu-id="c4405-472">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="c4405-473">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-473">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-474">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="c4405-474">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-475">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4405-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-476">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-477">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="c4405-477">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c4405-478">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="c4405-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-479">**тоталмаунттиме**</span><span class="sxs-lookup"><span data-stu-id="c4405-479">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-480">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-482">Для устройства, которое поддерживает съемные носители, общее время (в секундах) подключения носителя для передачи данных или очистки устройства.</span><span class="sxs-lookup"><span data-stu-id="c4405-482">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="c4405-483">Для устройств, обращающихся к несъемным носителям, например к жестким дискам, это свойство неприменимо и должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="c4405-483">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="c4405-484">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-484">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-485">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="c4405-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-486">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-488">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="c4405-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="c4405-489">Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-490">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="c4405-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-491">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4405-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-492">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-493">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c4405-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c4405-494">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="c4405-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4405-495">**ункомпресседдатарате**</span><span class="sxs-lookup"><span data-stu-id="c4405-495">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-496">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4405-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-497">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-498">Постоянная скорость передачи данных (в КБ/с), которую устройство может читать и записывать на носитель.</span><span class="sxs-lookup"><span data-stu-id="c4405-498">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="c4405-499">Это постоянная скорость необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="c4405-499">This is a sustained, raw data rate.</span></span> <span data-ttu-id="c4405-500">В этом свойстве не следует сообщать о максимальных тарифах или тарифах, имеющих значение сжатия.</span><span class="sxs-lookup"><span data-stu-id="c4405-500">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="c4405-501">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-501">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-502">**унитсдескриптион**</span><span class="sxs-lookup"><span data-stu-id="c4405-502">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-503">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4405-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-504">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-505">Единицы измерения относительно его использования в **максунитсбефореклеанинг**.</span><span class="sxs-lookup"><span data-stu-id="c4405-505">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="c4405-506">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-506">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-507">**унитсусед**</span><span class="sxs-lookup"><span data-stu-id="c4405-507">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-508">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-509">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-510">Текущее количество используемых единиц.</span><span class="sxs-lookup"><span data-stu-id="c4405-510">The current number of units used.</span></span> <span data-ttu-id="c4405-511">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-511">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4405-512">**унлоадтиме**</span><span class="sxs-lookup"><span data-stu-id="c4405-512">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4405-513">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4405-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4405-514">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4405-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4405-515">Время в миллисекундах от возможности чтения или записи носителя в его выгрузку.</span><span class="sxs-lookup"><span data-stu-id="c4405-515">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="c4405-516">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="c4405-516">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4405-517">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4405-517">Remarks</span></span>

<span data-ttu-id="c4405-518">Доступ к классу **\_ двддриве мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c4405-518">Access to the **Msvm\_DVDDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c4405-519">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c4405-519">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4405-520">Требования</span><span class="sxs-lookup"><span data-stu-id="c4405-520">Requirements</span></span>



| <span data-ttu-id="c4405-521">Требование</span><span class="sxs-lookup"><span data-stu-id="c4405-521">Requirement</span></span> | <span data-ttu-id="c4405-522">Значение</span><span class="sxs-lookup"><span data-stu-id="c4405-522">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4405-523">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4405-523">Minimum supported client</span></span><br/> | <span data-ttu-id="c4405-524">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c4405-524">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c4405-525">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4405-525">Minimum supported server</span></span><br/> | <span data-ttu-id="c4405-526">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c4405-526">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4405-527">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4405-527">Namespace</span></span><br/>                | <span data-ttu-id="c4405-528">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c4405-528">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c4405-529">MOF</span><span class="sxs-lookup"><span data-stu-id="c4405-529">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4405-530"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4405-530"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4405-531">DLL</span><span class="sxs-lookup"><span data-stu-id="c4405-531">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4405-532"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4405-532"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4405-533">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4405-533">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4405-534">**\_ДВДДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="c4405-534">**CIM\_DVDDrive**</span></span>](cim-dvddrive.md)
</dt> <dt>

<span data-ttu-id="c4405-535">[**\_ДВДДРИВЕ CIM**](/previous-versions//cc136812(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4405-535">[**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c4405-536">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="c4405-536">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

