---
description: Представляет физический диск, отображаемый на компьютере под управлением операционной системы Windows.
ms.assetid: c1fc6a1e-e725-484b-aacf-279f777e9b19
ms.tgt_platform: multiple
title: Класс Win32_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDrive
- Win32_DiskDrive.Reset
- Win32_DiskDrive.SetPowerState
- Win32_DiskDrive.Availability
- Win32_DiskDrive.BytesPerSector
- Win32_DiskDrive.Capabilities
- Win32_DiskDrive.CapabilityDescriptions
- Win32_DiskDrive.Caption
- Win32_DiskDrive.CompressionMethod
- Win32_DiskDrive.ConfigManagerErrorCode
- Win32_DiskDrive.ConfigManagerUserConfig
- Win32_DiskDrive.CreationClassName
- Win32_DiskDrive.DefaultBlockSize
- Win32_DiskDrive.Description
- Win32_DiskDrive.DeviceID
- Win32_DiskDrive.ErrorCleared
- Win32_DiskDrive.ErrorDescription
- Win32_DiskDrive.ErrorMethodology
- Win32_DiskDrive.FirmwareRevision
- Win32_DiskDrive.Index
- Win32_DiskDrive.InstallDate
- Win32_DiskDrive.InterfaceType
- Win32_DiskDrive.LastErrorCode
- Win32_DiskDrive.Manufacturer
- Win32_DiskDrive.MaxBlockSize
- Win32_DiskDrive.MaxMediaSize
- Win32_DiskDrive.MediaLoaded
- Win32_DiskDrive.MediaType
- Win32_DiskDrive.MinBlockSize
- Win32_DiskDrive.Model
- Win32_DiskDrive.Name
- Win32_DiskDrive.NeedsCleaning
- Win32_DiskDrive.NumberOfMediaSupported
- Win32_DiskDrive.Partitions
- Win32_DiskDrive.PNPDeviceID
- Win32_DiskDrive.PowerManagementCapabilities
- Win32_DiskDrive.PowerManagementSupported
- Win32_DiskDrive.SCSIBus
- Win32_DiskDrive.SCSILogicalUnit
- Win32_DiskDrive.SCSIPort
- Win32_DiskDrive.SCSITargetId
- Win32_DiskDrive.SectorsPerTrack
- Win32_DiskDrive.SerialNumber
- Win32_DiskDrive.Signature
- Win32_DiskDrive.Size
- Win32_DiskDrive.Status
- Win32_DiskDrive.StatusInfo
- Win32_DiskDrive.SystemCreationClassName
- Win32_DiskDrive.SystemName
- Win32_DiskDrive.TotalCylinders
- Win32_DiskDrive.TotalHeads
- Win32_DiskDrive.TotalSectors
- Win32_DiskDrive.TotalTracks
- Win32_DiskDrive.TracksPerCylinder
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 751dee053574be417cb312f6b046ae6b7703d543
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539140"
---
# <a name="win32_diskdrive-class"></a><span data-ttu-id="333a5-103">\_Класс Win32 дискдриве</span><span class="sxs-lookup"><span data-stu-id="333a5-103">Win32\_DiskDrive class</span></span>

<span data-ttu-id="333a5-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ дискдриве для Win32** представляет физический диск, как видно на компьютере, работающем под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="333a5-104">The **Win32\_DiskDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical disk drive as seen by a computer running the Windows operating system.</span></span>

<span data-ttu-id="333a5-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="333a5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="333a5-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="333a5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="333a5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="333a5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDrive : CIM_DiskDrive
{
  uint16   Availability;
  uint32   BytesPerSector;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FirmwareRevision;
  uint32   Index;
  datetime InstallDate;
  string   InterfaceType;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  uint64   MinBlockSize;
  string   Model;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Partitions;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  uint32   SectorsPerTrack;
  string   SerialNumber;
  uint32   Signature;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   TotalCylinders;
  uint32   TotalHeads;
  uint64   TotalSectors;
  uint64   TotalTracks;
  uint32   TracksPerCylinder;
};
```

## <a name="members"></a><span data-ttu-id="333a5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="333a5-108">Members</span></span>

<span data-ttu-id="333a5-109">Класс **Win32 \_ дискдриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="333a5-109">The **Win32\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="333a5-110">Методы</span><span class="sxs-lookup"><span data-stu-id="333a5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="333a5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="333a5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="333a5-112">Методы</span><span class="sxs-lookup"><span data-stu-id="333a5-112">Methods</span></span>

<span data-ttu-id="333a5-113">Класс **Win32 \_ дискдриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="333a5-113">The **Win32\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="333a5-114">Метод</span><span class="sxs-lookup"><span data-stu-id="333a5-114">Method</span></span>            | <span data-ttu-id="333a5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="333a5-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="333a5-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="333a5-116">**Reset**</span></span>         | <span data-ttu-id="333a5-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="333a5-117">Not implemented.</span></span> <span data-ttu-id="333a5-118">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ дискдриве**](cim-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="333a5-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="333a5-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="333a5-119">**SetPowerState**</span></span> | <span data-ttu-id="333a5-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="333a5-120">Not implemented.</span></span> <span data-ttu-id="333a5-121">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ дискдриве**](cim-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="333a5-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="333a5-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="333a5-122">Properties</span></span>

<span data-ttu-id="333a5-123">Класс **Win32 \_ дискдриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="333a5-123">The **Win32\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="333a5-124">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="333a5-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="333a5-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-127">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="333a5-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-128">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="333a5-128">Availability and status of the device.</span></span>

<span data-ttu-id="333a5-129">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="333a5-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="333a5-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="333a5-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="333a5-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="333a5-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="333a5-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-133">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="333a5-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="333a5-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="333a5-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="333a5-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="333a5-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="333a5-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="333a5-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="333a5-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="333a5-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="333a5-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="333a5-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="333a5-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="333a5-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="333a5-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="333a5-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="333a5-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="333a5-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="333a5-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="333a5-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="333a5-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="333a5-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="333a5-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="333a5-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="333a5-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="333a5-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="333a5-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="333a5-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="333a5-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="333a5-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="333a5-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="333a5-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="333a5-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="333a5-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="333a5-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="333a5-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="333a5-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="333a5-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="333a5-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="333a5-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="333a5-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="333a5-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-156">Диск недоступен.</span><span class="sxs-lookup"><span data-stu-id="333a5-156">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="333a5-157">**битесперсектор**</span><span class="sxs-lookup"><span data-stu-id="333a5-157">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-158">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-160">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры \| [**диска \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| битесперсектор "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="333a5-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|BytesPerSector"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-161">Число байтов в каждом секторе для физического диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-161">Number of bytes in each sector for the physical disk drive.</span></span>

<span data-ttu-id="333a5-162">Пример: 512</span><span class="sxs-lookup"><span data-stu-id="333a5-162">Example: 512</span></span>

</dd> <dt>

<span data-ttu-id="333a5-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="333a5-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-164">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="333a5-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="333a5-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-166">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="333a5-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-167">Массив возможностей устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="333a5-167">Array of capabilities of the media access device.</span></span> <span data-ttu-id="333a5-168">Например, устройство может поддерживать произвольный доступ (3), съемный носитель (7) и автоматическую чистку (9).</span><span class="sxs-lookup"><span data-stu-id="333a5-168">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="333a5-169">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="333a5-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="333a5-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="333a5-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="333a5-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="333a5-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="333a5-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="333a5-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="333a5-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="333a5-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="333a5-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="333a5-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="333a5-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="333a5-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="333a5-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="333a5-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="333a5-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-178">Поддержка съемных носителей</span><span class="sxs-lookup"><span data-stu-id="333a5-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="333a5-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="333a5-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="333a5-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="333a5-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="333a5-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="333a5-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="333a5-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="333a5-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-183">Поддержка носителя Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="333a5-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="333a5-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="333a5-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-185">Извлечение до отключения диска не требуется</span><span class="sxs-lookup"><span data-stu-id="333a5-185">Ejection Prior to Drive Dismount Not Required</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="333a5-186">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="333a5-186">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-187">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="333a5-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="333a5-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-189">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="333a5-189">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-190">Список более подробных объяснений для любого из функций доступа к устройствам, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="333a5-190">List of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="333a5-191">Обратите внимание, что каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="333a5-191">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="333a5-192">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-192">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-193">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="333a5-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-196">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="333a5-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-197">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="333a5-197">Short description of the object.</span></span>

<span data-ttu-id="333a5-198">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-199">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="333a5-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="333a5-202">Алгоритм или инструмент, используемый устройством для поддержки сжатия.</span><span class="sxs-lookup"><span data-stu-id="333a5-202">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="333a5-203">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-203">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="333a5-204">Имя алгоритма сжатия или одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="333a5-204">The name of the compression algorithm or one of the following values.</span></span>

<dt>



 <span data-ttu-id="333a5-205">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="333a5-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="333a5-206">Поддерживает ли устройство возможности сжатия или нет.</span><span class="sxs-lookup"><span data-stu-id="333a5-206">Whether the device supports compression capabilities or not is not known.</span></span>

</dd> <dt>



 <span data-ttu-id="333a5-207">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="333a5-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="333a5-208">Устройство поддерживает возможности сжатия, но его схема сжатия неизвестна или не раскрывается.</span><span class="sxs-lookup"><span data-stu-id="333a5-208">The device supports compression capabilities but its compression scheme is not known or not disclosed.</span></span>

</dd> <dt>



 <span data-ttu-id="333a5-209">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="333a5-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="333a5-210">Устройство не поддерживает сжатие.</span><span class="sxs-lookup"><span data-stu-id="333a5-210">The device does not support compression.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="333a5-211">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="333a5-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-212">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-214">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="333a5-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-215">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="333a5-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="333a5-216">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="333a5-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="333a5-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="333a5-218"> (0)</span><span class="sxs-lookup"><span data-stu-id="333a5-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-219">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="333a5-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="333a5-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="333a5-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="333a5-221">(1)</span><span class="sxs-lookup"><span data-stu-id="333a5-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-222">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="333a5-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="333a5-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="333a5-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="333a5-224">(2)</span><span class="sxs-lookup"><span data-stu-id="333a5-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="333a5-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="333a5-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="333a5-226">(3)</span><span class="sxs-lookup"><span data-stu-id="333a5-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-227">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="333a5-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="333a5-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="333a5-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="333a5-229">(4)</span><span class="sxs-lookup"><span data-stu-id="333a5-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-230">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="333a5-230">Device is not working properly.</span></span> <span data-ttu-id="333a5-231">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="333a5-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="333a5-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="333a5-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="333a5-233">(5)</span><span class="sxs-lookup"><span data-stu-id="333a5-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-234">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="333a5-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="333a5-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="333a5-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="333a5-236"> (6)</span><span class="sxs-lookup"><span data-stu-id="333a5-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-237">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="333a5-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="333a5-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="333a5-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="333a5-239">(7)</span><span class="sxs-lookup"><span data-stu-id="333a5-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="333a5-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="333a5-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="333a5-241">(8)</span><span class="sxs-lookup"><span data-stu-id="333a5-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-242">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="333a5-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="333a5-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="333a5-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="333a5-244">(9)</span><span class="sxs-lookup"><span data-stu-id="333a5-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-245">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="333a5-245">Device is not working properly.</span></span> <span data-ttu-id="333a5-246">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="333a5-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="333a5-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="333a5-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="333a5-248">(10)</span><span class="sxs-lookup"><span data-stu-id="333a5-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-249">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="333a5-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="333a5-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="333a5-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="333a5-251">(11)</span><span class="sxs-lookup"><span data-stu-id="333a5-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-252">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="333a5-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="333a5-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="333a5-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="333a5-254">(12)</span><span class="sxs-lookup"><span data-stu-id="333a5-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-255">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="333a5-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="333a5-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="333a5-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="333a5-257">(13)</span><span class="sxs-lookup"><span data-stu-id="333a5-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-258">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="333a5-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="333a5-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="333a5-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="333a5-260">(14)</span><span class="sxs-lookup"><span data-stu-id="333a5-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-261">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="333a5-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="333a5-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="333a5-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="333a5-263">(15)</span><span class="sxs-lookup"><span data-stu-id="333a5-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-264">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="333a5-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="333a5-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="333a5-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="333a5-266">(16)</span><span class="sxs-lookup"><span data-stu-id="333a5-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-267">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="333a5-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="333a5-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="333a5-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="333a5-269">(17)</span><span class="sxs-lookup"><span data-stu-id="333a5-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-270">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="333a5-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="333a5-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="333a5-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="333a5-272">(18)</span><span class="sxs-lookup"><span data-stu-id="333a5-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-273">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="333a5-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="333a5-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="333a5-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="333a5-275">(19)</span><span class="sxs-lookup"><span data-stu-id="333a5-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="333a5-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="333a5-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="333a5-277">(20)</span><span class="sxs-lookup"><span data-stu-id="333a5-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-278">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="333a5-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="333a5-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="333a5-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="333a5-280">(21)</span><span class="sxs-lookup"><span data-stu-id="333a5-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-281">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="333a5-281">System failure.</span></span> <span data-ttu-id="333a5-282">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="333a5-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="333a5-283">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="333a5-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="333a5-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="333a5-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="333a5-285">(22)</span><span class="sxs-lookup"><span data-stu-id="333a5-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-286">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="333a5-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="333a5-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="333a5-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="333a5-288">(23)</span><span class="sxs-lookup"><span data-stu-id="333a5-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-289">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="333a5-289">System failure.</span></span> <span data-ttu-id="333a5-290">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="333a5-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="333a5-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="333a5-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="333a5-292">(24)</span><span class="sxs-lookup"><span data-stu-id="333a5-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-293">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="333a5-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="333a5-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="333a5-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="333a5-295">(25)</span><span class="sxs-lookup"><span data-stu-id="333a5-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-296">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="333a5-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="333a5-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="333a5-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="333a5-298">(26)</span><span class="sxs-lookup"><span data-stu-id="333a5-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-299">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="333a5-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="333a5-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="333a5-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="333a5-301">(27)</span><span class="sxs-lookup"><span data-stu-id="333a5-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-302">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="333a5-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="333a5-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="333a5-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="333a5-304">(28)</span><span class="sxs-lookup"><span data-stu-id="333a5-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-305">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="333a5-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="333a5-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="333a5-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="333a5-307">(29)</span><span class="sxs-lookup"><span data-stu-id="333a5-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-308">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="333a5-308">Device is disabled.</span></span> <span data-ttu-id="333a5-309">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="333a5-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="333a5-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="333a5-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="333a5-311">(30)</span><span class="sxs-lookup"><span data-stu-id="333a5-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-312">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="333a5-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="333a5-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="333a5-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="333a5-314">1-31</span><span class="sxs-lookup"><span data-stu-id="333a5-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-315">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="333a5-315">Device is not working properly.</span></span> <span data-ttu-id="333a5-316">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="333a5-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="333a5-317">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="333a5-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-318">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="333a5-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-320">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="333a5-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-321">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="333a5-321">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="333a5-322">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-323">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="333a5-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-326">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="333a5-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="333a5-327">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="333a5-327">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="333a5-328">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="333a5-328">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="333a5-329">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-330">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="333a5-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-331">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="333a5-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-333">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="333a5-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-334">Размер блока по умолчанию (в байтах) для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="333a5-334">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="333a5-335">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="333a5-336">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="333a5-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-337">**Описание**</span><span class="sxs-lookup"><span data-stu-id="333a5-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-340">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="333a5-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-341">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="333a5-341">Description of the object.</span></span>

<span data-ttu-id="333a5-342">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="333a5-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-344">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-346">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="333a5-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-347">Уникальный идентификатор диска с другими устройствами в системе.</span><span class="sxs-lookup"><span data-stu-id="333a5-347">Unique identifier of the disk drive with other devices on the system.</span></span>

<span data-ttu-id="333a5-348">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-349">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="333a5-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-350">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="333a5-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="333a5-352">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="333a5-352">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="333a5-353">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="333a5-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="333a5-357">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="333a5-357">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="333a5-358">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-359">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="333a5-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="333a5-362">Тип обнаружения и исправления ошибок, поддерживаемых этим устройством.</span><span class="sxs-lookup"><span data-stu-id="333a5-362">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="333a5-363">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-364">**фирмвареревисион**</span><span class="sxs-lookup"><span data-stu-id="333a5-364">**FirmwareRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-365">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-367">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры устройства \| [**хранения \_ \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| продуктревисионоффсет ")</span><span class="sxs-lookup"><span data-stu-id="333a5-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-368">Редакция встроенного по для диска, назначенного производителем.</span><span class="sxs-lookup"><span data-stu-id="333a5-368">Revision for the disk drive firmware that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="333a5-369">**Index**</span><span class="sxs-lookup"><span data-stu-id="333a5-369">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-370">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-372">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows 95/98 functions \| \_ Map \_ info \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="333a5-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows 95/98 Functions\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-373">Номер физического диска данного диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-373">Physical drive number of the given drive.</span></span> <span data-ttu-id="333a5-374">Это свойство заполняется структурой [**\_ \_ номера устройства хранения**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) , возвращенного из [**хранилища ioctl получение кода управления \_ \_ \_ \_ номера устройства**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) .</span><span class="sxs-lookup"><span data-stu-id="333a5-374">This property is filled by the [**STORAGE\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) structure returned from the [**IOCTL\_STORAGE\_GET\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) control code.</span></span> <span data-ttu-id="333a5-375">Значение 0xFFFFFFFF указывает, что заданный диск не соответствует физическому диску.</span><span class="sxs-lookup"><span data-stu-id="333a5-375">A value of 0xffffffff indicates that the given drive does not map to a physical drive.</span></span>

<span data-ttu-id="333a5-376">Пример: 1</span><span class="sxs-lookup"><span data-stu-id="333a5-376">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="333a5-377">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="333a5-377">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-378">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="333a5-378">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-379">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-380">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="333a5-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-381">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="333a5-381">Date and time the object was installed.</span></span> <span data-ttu-id="333a5-382">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="333a5-382">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="333a5-383">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-383">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-384">**InterfaceType**</span><span class="sxs-lookup"><span data-stu-id="333a5-384">**InterfaceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-385">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-386">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-387">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| входные и выходные функции устройства Win32API \| [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="333a5-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-388">Тип интерфейса физического диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-388">Interface type of physical disk drive.</span></span>

<span data-ttu-id="333a5-389">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="333a5-389">The values are:</span></span>

<span data-ttu-id="333a5-390">SCSI</span><span class="sxs-lookup"><span data-stu-id="333a5-390">SCSI</span></span>

<span data-ttu-id="333a5-391">HDC</span><span class="sxs-lookup"><span data-stu-id="333a5-391">HDC</span></span>

<span data-ttu-id="333a5-392">IDE</span><span class="sxs-lookup"><span data-stu-id="333a5-392">IDE</span></span>

<span data-ttu-id="333a5-393">USB</span><span class="sxs-lookup"><span data-stu-id="333a5-393">USB</span></span>

<span data-ttu-id="333a5-394">1394</span><span class="sxs-lookup"><span data-stu-id="333a5-394">1394</span></span>

</dd> <dt>

<span data-ttu-id="333a5-395">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="333a5-395">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-396">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="333a5-398">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="333a5-398">Last error code reported by the logical device.</span></span>

<span data-ttu-id="333a5-399">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-400">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="333a5-400">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-401">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-403">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ локальный \_ компьютер \\ \\ оборудование \\ \\ Девицемап \\ \\ SCSI SCSI \\ \\ Port \\ \\ SCSI \\ \\ Target ID идентификатор \\ \\ логического устройства \\ \\ идентификатор", "Win32Registry \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="333a5-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-404">Имя изготовителя диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-404">Name of the disk drive manufacturer.</span></span>

<span data-ttu-id="333a5-405">Пример: Seagate</span><span class="sxs-lookup"><span data-stu-id="333a5-405">Example: "Seagate"</span></span>

</dd> <dt>

<span data-ttu-id="333a5-406">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="333a5-406">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-407">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="333a5-407">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-409">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="333a5-409">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-410">Максимальный размер блока в байтах для носителя, доступного этому устройству.</span><span class="sxs-lookup"><span data-stu-id="333a5-410">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="333a5-411">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="333a5-412">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="333a5-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-413">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="333a5-413">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-414">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="333a5-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-416">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="333a5-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-417">Максимальный размер носителя (в КБ), поддерживаемый этим устройством.</span><span class="sxs-lookup"><span data-stu-id="333a5-417">Maximum media size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="333a5-418">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="333a5-419">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="333a5-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-420">**медиалоадед**</span><span class="sxs-lookup"><span data-stu-id="333a5-420">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-421">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="333a5-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-423">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры \| [**диска \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| \| фикседмедиа ")</span><span class="sxs-lookup"><span data-stu-id="333a5-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType\|FixedMedia")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-424">**Значение true** показывает, что носитель для диска загружен, что означает, что устройство имеет доступную для чтения файловую систему и доступна.</span><span class="sxs-lookup"><span data-stu-id="333a5-424">If **True**, the media for a disk drive is loaded, which means that the device has a readable file system and is accessible.</span></span> <span data-ttu-id="333a5-425">Для несъемных дисков это свойство всегда будет иметь **значение true**.</span><span class="sxs-lookup"><span data-stu-id="333a5-425">For fixed disk drives, this property will always be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="333a5-426">**Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="333a5-426">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-429">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры \| [**диска \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| ")</span><span class="sxs-lookup"><span data-stu-id="333a5-429">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-430">Тип носителя, используемого устройством или доступ к которому осуществляется.</span><span class="sxs-lookup"><span data-stu-id="333a5-430">Type of media used or accessed by this device.</span></span>

<span data-ttu-id="333a5-431">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="333a5-431">Possible values are:</span></span>

<dt>

<span id="External_hard_disk_media"></span><span id="external_hard_disk_media"></span><span id="EXTERNAL_HARD_DISK_MEDIA"></span>

<span data-ttu-id="333a5-432">**Носитель внешних жестких дисков**</span><span class="sxs-lookup"><span data-stu-id="333a5-432">**External hard disk media**</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="333a5-433">**Съемный носитель** ("съемный носитель, отличный от дискеты")</span><span class="sxs-lookup"><span data-stu-id="333a5-433">**Removable media** ("Removable media other than floppy")</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk"></span><span id="fixed_hard_disk"></span><span id="FIXED_HARD_DISK"></span>

<span data-ttu-id="333a5-434">**Фиксированный жесткий диск** ("несъемный жесткий диск")</span><span class="sxs-lookup"><span data-stu-id="333a5-434">**Fixed hard disk** ("Fixed hard disk media")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="333a5-435">**Неизвестно** (неизвестный формат)</span><span class="sxs-lookup"><span data-stu-id="333a5-435">**Unknown** ("Format is unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="333a5-436">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="333a5-436">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-437">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="333a5-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-438">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-439">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="333a5-439">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-440">Минимальный размер блока в байтах для носителя, доступного этому устройству.</span><span class="sxs-lookup"><span data-stu-id="333a5-440">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="333a5-441">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-441">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="333a5-442">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="333a5-442">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-443">**Модель**</span><span class="sxs-lookup"><span data-stu-id="333a5-443">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-444">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-445">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-446">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ локальный \_ компьютер \\ \\ оборудование \\ \\ Девицемап \\ \\ SCSI порт SCSI SCSI \\ \\ \\ \\ \\ \\ Target ID идентификатор \\ \\ логического устройства ID \\ \\ ", "Win32Registry \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="333a5-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-447">Номер модели диска изготовителя.</span><span class="sxs-lookup"><span data-stu-id="333a5-447">Manufacturer's model number of the disk drive.</span></span>

<span data-ttu-id="333a5-448">Пример: "ST32171W"</span><span class="sxs-lookup"><span data-stu-id="333a5-448">Example: "ST32171W"</span></span>

</dd> <dt>

<span data-ttu-id="333a5-449">**Name**</span><span class="sxs-lookup"><span data-stu-id="333a5-449">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-450">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-452">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="333a5-452">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-453">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="333a5-453">Label by which the object is known.</span></span> <span data-ttu-id="333a5-454">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="333a5-454">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="333a5-455">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-455">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-456">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="333a5-456">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-457">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="333a5-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="333a5-459">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="333a5-459">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="333a5-460">Возможность ручной или автоматической очистки указывается в свойстве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="333a5-460">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="333a5-461">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-461">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-462">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="333a5-462">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-463">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-464">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="333a5-465">Максимальное количество носителей, которое может поддерживаться или вставляться (если устройство доступа к носителю поддерживает несколько отдельных носителей).</span><span class="sxs-lookup"><span data-stu-id="333a5-465">Maximum number of media which can be supported or inserted (when the media access device supports multiple individual media).</span></span>

<span data-ttu-id="333a5-466">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-466">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-467">**Секции**</span><span class="sxs-lookup"><span data-stu-id="333a5-467">**Partitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-468">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-470">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры " \| [**\_ сведения о секции**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| рекогнизедпартитион")</span><span class="sxs-lookup"><span data-stu-id="333a5-470">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RecognizedPartition")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-471">Количество разделов на этом физическом диске, распознаваемых операционной системой.</span><span class="sxs-lookup"><span data-stu-id="333a5-471">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

<span data-ttu-id="333a5-472">Пример: 2</span><span class="sxs-lookup"><span data-stu-id="333a5-472">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="333a5-473">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="333a5-473">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-474">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-476">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="333a5-476">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-477">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="333a5-477">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="333a5-478">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="333a5-479">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="333a5-479">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="333a5-480">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="333a5-480">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-481">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="333a5-481">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="333a5-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="333a5-483">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="333a5-483">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="333a5-484">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-484">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="333a5-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="333a5-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="333a5-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="333a5-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-487">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="333a5-487">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="333a5-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="333a5-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="333a5-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="333a5-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-490">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="333a5-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="333a5-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="333a5-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-492">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="333a5-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="333a5-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="333a5-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-494">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="333a5-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="333a5-495">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="333a5-495">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="333a5-496">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="333a5-496">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="333a5-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="333a5-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-498">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="333a5-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="333a5-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="333a5-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="333a5-500">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="333a5-500">Timed Power-On Supported</span></span>

<span data-ttu-id="333a5-501">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="333a5-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="333a5-502">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="333a5-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-503">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="333a5-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-504">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="333a5-505">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="333a5-505">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="333a5-506">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="333a5-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="333a5-507">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-508">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="333a5-508">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-509">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-509">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-510">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-510">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-511">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| устройства ввода и вывода структуры \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| пасид")</span><span class="sxs-lookup"><span data-stu-id="333a5-511">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-512">Номер шины SCSI на диске.</span><span class="sxs-lookup"><span data-stu-id="333a5-512">SCSI bus number of the disk drive.</span></span>

<span data-ttu-id="333a5-513">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="333a5-513">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="333a5-514">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="333a5-514">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-515">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="333a5-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-516">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-517">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| устройства Win32API входные и выходные структуры \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| LUN")</span><span class="sxs-lookup"><span data-stu-id="333a5-517">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-518">Логический номер устройства (LUN) SCSI диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-518">SCSI logical unit number (LUN) of the disk drive.</span></span>

<span data-ttu-id="333a5-519">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="333a5-519">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="333a5-520">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="333a5-520">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-521">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="333a5-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-522">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-523">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| устройства ввода и вывода структуры \| [**SCSI \_ адрес**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| номер_порта")</span><span class="sxs-lookup"><span data-stu-id="333a5-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PortNumber")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-524">Номер порта SCSI диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-524">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="333a5-525">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="333a5-525">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="333a5-526">**скситаржетид**</span><span class="sxs-lookup"><span data-stu-id="333a5-526">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-527">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="333a5-527">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-528">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-529">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| устройства ввода и вывода структуры \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| TargetId")</span><span class="sxs-lookup"><span data-stu-id="333a5-529">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|TargetId")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-530">Номер идентификатора SCSI диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-530">SCSI identifier number of the disk drive.</span></span>

<span data-ttu-id="333a5-531">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="333a5-531">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="333a5-532">**секторспертракк**</span><span class="sxs-lookup"><span data-stu-id="333a5-532">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-533">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-533">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-534">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-535">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры \| [**диска \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| секторспертракк ")</span><span class="sxs-lookup"><span data-stu-id="333a5-535">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-536">Количество секторов в каждой дорожке для этого физического диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-536">Number of sectors in each track for this physical disk drive.</span></span>

<span data-ttu-id="333a5-537">Пример: 63</span><span class="sxs-lookup"><span data-stu-id="333a5-537">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="333a5-538">**Номер**</span><span class="sxs-lookup"><span data-stu-id="333a5-538">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-539">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-540">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-541">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры устройства \| [**хранения \_ \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| сериалнумбероффсет ")</span><span class="sxs-lookup"><span data-stu-id="333a5-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-542">Число, выделенное производителем для распознавания физического носителя.</span><span class="sxs-lookup"><span data-stu-id="333a5-542">Number allocated by the manufacturer to identify the physical media.</span></span>

<span data-ttu-id="333a5-543">Пример: WD-WM3493798728</span><span class="sxs-lookup"><span data-stu-id="333a5-543">Example: WD-WM3493798728</span></span>

</dd> <dt>

<span data-ttu-id="333a5-544">**Образец**</span><span class="sxs-lookup"><span data-stu-id="333a5-544">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-545">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-545">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-546">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-547">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры входных и выходных данных устройства Win32API \| подпись [**\_ \_ сведений о макете**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information) \| ")</span><span class="sxs-lookup"><span data-stu-id="333a5-547">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DRIVE\_LAYOUT\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information)\|Signature")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-548">Идентификация диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-548">Disk identification.</span></span> <span data-ttu-id="333a5-549">Это свойство можно использовать для задания общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="333a5-549">This property can be used to identify a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="333a5-550">**Размер**</span><span class="sxs-lookup"><span data-stu-id="333a5-550">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-551">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="333a5-551">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-552">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-553">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры \| [**диска с \_ геометрией**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="333a5-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-554">Размер диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-554">Size of the disk drive.</span></span> <span data-ttu-id="333a5-555">Он вычисляется путем умножения общего числа цилиндров, дорожек в каждом цилиндре, секторов в каждой дорожке и байтов в каждом секторе.</span><span class="sxs-lookup"><span data-stu-id="333a5-555">It is calculated by multiplying the total number of cylinders, tracks in each cylinder, sectors in each track, and bytes in each sector.</span></span>

<span data-ttu-id="333a5-556">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="333a5-556">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-557">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="333a5-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-558">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-559">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-560">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="333a5-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-561">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="333a5-561">Current status of the object.</span></span> <span data-ttu-id="333a5-562">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="333a5-562">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="333a5-563">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="333a5-563">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="333a5-564">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="333a5-564">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="333a5-565">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="333a5-565">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="333a5-566">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="333a5-566">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="333a5-567">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-567">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="333a5-568">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="333a5-568">Values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="333a5-569">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="333a5-569">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="333a5-570">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="333a5-570">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="333a5-571">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="333a5-571">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="333a5-572">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="333a5-572">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="333a5-573">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="333a5-573">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="333a5-574">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="333a5-574">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="333a5-575">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="333a5-575">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="333a5-576">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="333a5-576">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="333a5-577">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="333a5-577">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="333a5-578">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="333a5-578">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="333a5-579">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="333a5-579">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="333a5-580">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="333a5-580">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="333a5-581">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="333a5-581">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-582">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="333a5-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-583">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-583">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-584">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="333a5-584">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-585">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="333a5-585">State of the logical device.</span></span> <span data-ttu-id="333a5-586">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="333a5-586">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="333a5-587">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="333a5-588">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="333a5-588">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="333a5-589">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="333a5-589">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="333a5-590">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="333a5-590">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="333a5-591">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="333a5-591">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="333a5-592">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="333a5-592">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="333a5-593">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="333a5-593">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-594">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-594">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-595">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-596">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="333a5-596">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="333a5-597">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="333a5-597">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="333a5-598">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-598">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-599">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="333a5-599">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-600">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="333a5-600">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-601">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-602">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="333a5-602">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="333a5-603">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="333a5-603">Name of the scoping system.</span></span>

<span data-ttu-id="333a5-604">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="333a5-604">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-605">**TotalCylinders**</span><span class="sxs-lookup"><span data-stu-id="333a5-605">**TotalCylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-606">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="333a5-606">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-607">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-608">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| входные и выходные структуры \| [**диска \_ геометрические**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| цилиндры")</span><span class="sxs-lookup"><span data-stu-id="333a5-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|Cylinders")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-609">Общее число цилиндров на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="333a5-609">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="333a5-610">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="333a5-610">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="333a5-611">Значение может быть неточным, если диск использует схему перевода для поддержки размеров дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="333a5-611">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="333a5-612">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="333a5-612">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="333a5-613">Пример: 657</span><span class="sxs-lookup"><span data-stu-id="333a5-613">Example: 657</span></span>

<span data-ttu-id="333a5-614">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="333a5-614">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-615">**TotalHeads**</span><span class="sxs-lookup"><span data-stu-id="333a5-615">**TotalHeads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-616">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-616">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-617">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-618">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры \| [**диска \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| тракксперцилиндер ")</span><span class="sxs-lookup"><span data-stu-id="333a5-618">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-619">Общее количество головок на диске.</span><span class="sxs-lookup"><span data-stu-id="333a5-619">Total number of heads on the disk drive.</span></span> <span data-ttu-id="333a5-620">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="333a5-620">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="333a5-621">Значение может быть неточным, если диск использует схему перевода для поддержки размеров дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="333a5-621">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="333a5-622">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="333a5-622">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="333a5-623">**TotalSectors**</span><span class="sxs-lookup"><span data-stu-id="333a5-623">**TotalSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-624">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="333a5-624">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-625">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-626">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры \| [**диска \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| секторспертракк ")</span><span class="sxs-lookup"><span data-stu-id="333a5-626">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-627">Общее количество секторов на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="333a5-627">Total number of sectors on the physical disk drive.</span></span> <span data-ttu-id="333a5-628">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="333a5-628">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="333a5-629">Значение может быть неточным, если диск использует схему перевода для поддержки размеров дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="333a5-629">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="333a5-630">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="333a5-630">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="333a5-631">Пример: 2649024</span><span class="sxs-lookup"><span data-stu-id="333a5-631">Example: 2649024</span></span>

<span data-ttu-id="333a5-632">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="333a5-632">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-633">**TotalTracks**</span><span class="sxs-lookup"><span data-stu-id="333a5-633">**TotalTracks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-634">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="333a5-634">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-635">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-636">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры \| [**диска \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| тракксперцилиндер ")</span><span class="sxs-lookup"><span data-stu-id="333a5-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-637">Общее число дорожек на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="333a5-637">Total number of tracks on the physical disk drive.</span></span> <span data-ttu-id="333a5-638">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="333a5-638">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="333a5-639">Значение может быть неточным, если диск использует схему перевода для поддержки размеров дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="333a5-639">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="333a5-640">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="333a5-640">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="333a5-641">Пример: 42048</span><span class="sxs-lookup"><span data-stu-id="333a5-641">Example: 42048</span></span>

<span data-ttu-id="333a5-642">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="333a5-642">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="333a5-643">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="333a5-643">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="333a5-644">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="333a5-644">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="333a5-645">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="333a5-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="333a5-646">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры \| [**диска \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| тракксперцилиндер ")</span><span class="sxs-lookup"><span data-stu-id="333a5-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="333a5-647">Количество дорожек в каждом цилиндре на физическом диске.</span><span class="sxs-lookup"><span data-stu-id="333a5-647">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="333a5-648">Примечание. значение этого свойства получается через расширенные функции прерывания 13h BIOS.</span><span class="sxs-lookup"><span data-stu-id="333a5-648">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="333a5-649">Значение может быть неточным, если диск использует схему перевода для поддержки размеров дисков с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="333a5-649">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="333a5-650">Точные спецификации дисков можно узнать у изготовителя.</span><span class="sxs-lookup"><span data-stu-id="333a5-650">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="333a5-651">Пример: 64</span><span class="sxs-lookup"><span data-stu-id="333a5-651">Example: 64</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="333a5-652">Комментарии</span><span class="sxs-lookup"><span data-stu-id="333a5-652">Remarks</span></span>

<span data-ttu-id="333a5-653">Физические жесткие диски — это основной носитель для хранения данных в любой вычислительной среде.</span><span class="sxs-lookup"><span data-stu-id="333a5-653">Physical hard disk drives are the primary storage medium for information in any computing environment.</span></span> <span data-ttu-id="333a5-654">Хотя организации часто используют такие устройства, как ленточные накопители и дисководы компакт-дисков для архивирования данных, эти устройства не подходят для повседневного хранения данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="333a5-654">Although organizations often use devices such as tape drives and compact disc drives for archiving data, these devices are not suited for day-to-day storage of user data.</span></span> <span data-ttu-id="333a5-655">Только физические жесткие диски обеспечивают скорость и удобство использования, необходимые для хранения данных, а также для запуска приложений и операционной системы.</span><span class="sxs-lookup"><span data-stu-id="333a5-655">Only physical hard disks offer the speed and ease of use required for storing data and for running applications and the operating system.</span></span>

<span data-ttu-id="333a5-656">Для эффективного управления данными важно иметь подробный учет всех физических дисков, их возможностей и емкости.</span><span class="sxs-lookup"><span data-stu-id="333a5-656">To efficiently manage data, it is important to have a detailed inventory of all your physical disks, their capabilities, and their capacities.</span></span> <span data-ttu-id="333a5-657">Для получения такого типа инвентаризации можно использовать класс **Win32 \_ дискдриве** .</span><span class="sxs-lookup"><span data-stu-id="333a5-657">You can use the **Win32\_DiskDrive** class to derive this type of inventory.</span></span>

<span data-ttu-id="333a5-658">Любой интерфейс к физическому диску Windows — это потомок (или член) этого класса.</span><span class="sxs-lookup"><span data-stu-id="333a5-658">Any interface to a Windows physical disk drive is a descendant (or member) of this class.</span></span> <span data-ttu-id="333a5-659">Функции диска, показанные в этом объекте, соответствуют логическим характеристикам и характеристики управления диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-659">The features of the disk drive seen through this object correspond to the logical and management characteristics of the drive.</span></span> <span data-ttu-id="333a5-660">В некоторых случаях это может не отражать фактические физические характеристики устройства.</span><span class="sxs-lookup"><span data-stu-id="333a5-660">In some cases, this may not reflect the actual physical characteristics of the device.</span></span> <span data-ttu-id="333a5-661">Любой объект, основанный на другом логическом устройстве, не будет членом этого класса.</span><span class="sxs-lookup"><span data-stu-id="333a5-661">Any object based on another logical device would not be a member of this class.</span></span>

<span data-ttu-id="333a5-662">По соображениям безопасности пользователь, подключающийся с удаленного компьютера, должен иметь разрешение **SC \_ Manager \_ Connect** , чтобы иметь возможность перечислить этот класс.</span><span class="sxs-lookup"><span data-stu-id="333a5-662">For security reasons, a user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="333a5-663">Дополнительные сведения см. в разделе [Безопасность службы и права доступа](/windows/desktop/Services/service-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="333a5-663">For more information, see [Service Security and Access Rights](/windows/desktop/Services/service-security-and-access-rights).</span></span>

<span data-ttu-id="333a5-664">Класс **Win32 \_ дискдриве** является производным от [**CIM \_ дискдриве**](cim-diskdrive.md) , который является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="333a5-664">The **Win32\_DiskDrive** class is derived from [**CIM\_DiskDrive**](cim-diskdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="333a5-665">Класс **CIM \_ медиаакцессдевице** является производным от [**CIM \_**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="333a5-665">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="333a5-666">Примеры</span><span class="sxs-lookup"><span data-stu-id="333a5-666">Examples</span></span>

<span data-ttu-id="333a5-667">[Отчет об инвентаризации серверов](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) . пример кода CIM POWERSHELL & WMI в коллекции TechNet использует ряд классов, включая **Win32 \_ дискдриве**, для получения сведений о состоянии сервера.</span><span class="sxs-lookup"><span data-stu-id="333a5-667">The [Servers Inventory report-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell code example on TechNet Gallery uses a number of classes, including **Win32\_DiskDrive**, to return information about server status.</span></span>

<span data-ttu-id="333a5-668">При [сопоставлении диска с буквой диска с помощью \_ Свойства Дискдриве интерфейса Win32](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) в примере кода PowerShell устройство преобразуется в букву диска.</span><span class="sxs-lookup"><span data-stu-id="333a5-668">The [Map Drive to Drive Letter Using the Win32\_DiskDrive Interface Type Property](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) PowerShell code sample maps a drive to a drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="333a5-669">Требования</span><span class="sxs-lookup"><span data-stu-id="333a5-669">Requirements</span></span>



| <span data-ttu-id="333a5-670">Требование</span><span class="sxs-lookup"><span data-stu-id="333a5-670">Requirement</span></span> | <span data-ttu-id="333a5-671">Значение</span><span class="sxs-lookup"><span data-stu-id="333a5-671">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="333a5-672">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="333a5-672">Minimum supported client</span></span><br/> | <span data-ttu-id="333a5-673">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="333a5-673">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="333a5-674">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="333a5-674">Minimum supported server</span></span><br/> | <span data-ttu-id="333a5-675">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="333a5-675">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="333a5-676">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="333a5-676">Namespace</span></span><br/>                | <span data-ttu-id="333a5-677">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="333a5-677">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="333a5-678">MOF</span><span class="sxs-lookup"><span data-stu-id="333a5-678">MOF</span></span><br/>                      | <dl> <span data-ttu-id="333a5-679"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="333a5-679"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="333a5-680">DLL</span><span class="sxs-lookup"><span data-stu-id="333a5-680">DLL</span></span><br/>                      | <dl> <span data-ttu-id="333a5-681"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="333a5-681"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="333a5-682">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="333a5-682">See also</span></span>

<dl> <dt>

[<span data-ttu-id="333a5-683">**\_ДИСКДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="333a5-683">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="333a5-684">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="333a5-684">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="333a5-685">Задачи WMI: диски и файловые системы</span><span class="sxs-lookup"><span data-stu-id="333a5-685">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

