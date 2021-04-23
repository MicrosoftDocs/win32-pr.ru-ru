---
description: Представляет дисковод компакт-дисков в компьютерной системе под управлением Windows.
ms.assetid: 08087976-ca88-4ac8-9456-0d8bd799e66c
ms.tgt_platform: multiple
title: Класс Win32_CDROMDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CDROMDrive
- Win32_CDROMDrive.Reset
- Win32_CDROMDrive.SetPowerState
- Win32_CDROMDrive.Availability
- Win32_CDROMDrive.Capabilities
- Win32_CDROMDrive.CapabilityDescriptions
- Win32_CDROMDrive.Caption
- Win32_CDROMDrive.CompressionMethod
- Win32_CDROMDrive.ConfigManagerErrorCode
- Win32_CDROMDrive.ConfigManagerUserConfig
- Win32_CDROMDrive.CreationClassName
- Win32_CDROMDrive.DefaultBlockSize
- Win32_CDROMDrive.Description
- Win32_CDROMDrive.DeviceID
- Win32_CDROMDrive.Drive
- Win32_CDROMDrive.DriveIntegrity
- Win32_CDROMDrive.ErrorCleared
- Win32_CDROMDrive.ErrorDescription
- Win32_CDROMDrive.ErrorMethodology
- Win32_CDROMDrive.FileSystemFlags
- Win32_CDROMDrive.FileSystemFlagsEx
- Win32_CDROMDrive.Id
- Win32_CDROMDrive.InstallDate
- Win32_CDROMDrive.LastErrorCode
- Win32_CDROMDrive.Manufacturer
- Win32_CDROMDrive.MaxBlockSize
- Win32_CDROMDrive.MaximumComponentLength
- Win32_CDROMDrive.MaxMediaSize
- Win32_CDROMDrive.MediaLoaded
- Win32_CDROMDrive.MediaType
- Win32_CDROMDrive.MfrAssignedRevisionLevel
- Win32_CDROMDrive.MinBlockSize
- Win32_CDROMDrive.Name
- Win32_CDROMDrive.NeedsCleaning
- Win32_CDROMDrive.NumberOfMediaSupported
- Win32_CDROMDrive.PNPDeviceID
- Win32_CDROMDrive.PowerManagementCapabilities
- Win32_CDROMDrive.PowerManagementSupported
- Win32_CDROMDrive.RevisionLevel
- Win32_CDROMDrive.SCSIBus
- Win32_CDROMDrive.SCSILogicalUnit
- Win32_CDROMDrive.SCSIPort
- Win32_CDROMDrive.SCSITargetId
- Win32_CDROMDrive.SerialNumber
- Win32_CDROMDrive.Size
- Win32_CDROMDrive.Status
- Win32_CDROMDrive.StatusInfo
- Win32_CDROMDrive.SystemCreationClassName
- Win32_CDROMDrive.SystemName
- Win32_CDROMDrive.TransferRate
- Win32_CDROMDrive.VolumeName
- Win32_CDROMDrive.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c352d2ee717f5eb888b49d6e5e8ff456cc5a85f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990708"
---
# <a name="win32_cdromdrive-class"></a><span data-ttu-id="234a5-103">\_Класс Win32 кдромдриве</span><span class="sxs-lookup"><span data-stu-id="234a5-103">Win32\_CDROMDrive class</span></span>

<span data-ttu-id="234a5-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ кдромдриве для Win32** представляет дисковод компакт-дисков в компьютерной системе под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="234a5-104">The **Win32\_CDROMDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a CD-ROM drive on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="234a5-105">Имейте в виду, что имя диска не соответствует назначенному устройству букве логического диска.</span><span class="sxs-lookup"><span data-stu-id="234a5-105">Be aware that the name of the drive does not correspond to the logical drive letter assigned to the device.</span></span>

 

<span data-ttu-id="234a5-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="234a5-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="234a5-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="234a5-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="234a5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="234a5-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CDROMDrive : CIM_CDROMDrive
{
  uint16   Availability;
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
  string   Drive;
  boolean  DriveIntegrity;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint16   FileSystemFlags;
  uint32   FileSystemFlagsEx;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint32   MaximumComponentLength;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  string   MfrAssignedRevisionLevel;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   RevisionLevel;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  string   SerialNumber;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  real64   TransferRate;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="234a5-109">Члены</span><span class="sxs-lookup"><span data-stu-id="234a5-109">Members</span></span>

<span data-ttu-id="234a5-110">Класс **Win32 \_ кдромдриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="234a5-110">The **Win32\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="234a5-111">Методы</span><span class="sxs-lookup"><span data-stu-id="234a5-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="234a5-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="234a5-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="234a5-113">Методы</span><span class="sxs-lookup"><span data-stu-id="234a5-113">Methods</span></span>

<span data-ttu-id="234a5-114">Класс **Win32 \_ кдромдриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="234a5-114">The **Win32\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="234a5-115">Метод</span><span class="sxs-lookup"><span data-stu-id="234a5-115">Method</span></span>            | <span data-ttu-id="234a5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="234a5-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="234a5-117">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="234a5-117">**Reset**</span></span>         | <span data-ttu-id="234a5-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="234a5-118">Not implemented.</span></span> <span data-ttu-id="234a5-119">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ кдромдриве**](cim-cdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="234a5-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="234a5-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="234a5-120">**SetPowerState**</span></span> | <span data-ttu-id="234a5-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="234a5-121">Not implemented.</span></span> <span data-ttu-id="234a5-122">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ кдромдриве**](cim-cdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="234a5-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="234a5-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="234a5-123">Properties</span></span>

<span data-ttu-id="234a5-124">Класс **Win32 \_ кдромдриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="234a5-124">The **Win32\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="234a5-125">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="234a5-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="234a5-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="234a5-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-129">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="234a5-129">Availability and status of the device.</span></span>

<span data-ttu-id="234a5-130">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="234a5-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="234a5-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="234a5-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="234a5-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="234a5-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="234a5-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-134">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="234a5-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="234a5-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="234a5-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="234a5-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="234a5-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="234a5-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="234a5-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="234a5-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="234a5-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="234a5-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="234a5-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="234a5-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="234a5-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="234a5-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="234a5-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="234a5-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="234a5-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="234a5-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="234a5-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="234a5-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="234a5-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="234a5-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="234a5-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="234a5-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="234a5-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="234a5-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="234a5-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="234a5-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="234a5-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="234a5-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="234a5-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="234a5-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="234a5-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="234a5-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="234a5-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="234a5-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="234a5-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="234a5-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="234a5-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="234a5-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="234a5-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="234a5-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="234a5-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="234a5-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="234a5-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="234a5-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="234a5-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-162">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="234a5-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="234a5-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-164">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="234a5-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-165">Массив возможностей устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="234a5-165">Array of capabilities of the media access device.</span></span> <span data-ttu-id="234a5-166">Например, устройство может поддерживать произвольный доступ (3), съемный носитель (7) и автоматическую чистку (9).</span><span class="sxs-lookup"><span data-stu-id="234a5-166">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="234a5-167">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="234a5-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="234a5-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="234a5-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="234a5-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="234a5-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="234a5-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="234a5-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="234a5-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="234a5-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="234a5-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="234a5-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="234a5-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="234a5-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="234a5-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="234a5-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="234a5-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-176">Поддержка съемных носителей</span><span class="sxs-lookup"><span data-stu-id="234a5-176">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="234a5-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="234a5-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="234a5-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="234a5-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="234a5-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="234a5-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="234a5-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="234a5-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-181">Поддержка носителя Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="234a5-181">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="234a5-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="234a5-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="234a5-183">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="234a5-183">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-184">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="234a5-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="234a5-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-186">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="234a5-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-187">Массив более подробных объяснений для любого из функций доступа к устройствам, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="234a5-187">Array of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="234a5-188">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="234a5-188">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="234a5-189">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-189">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-190">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="234a5-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-193">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="234a5-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-194">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="234a5-194">Short description of the object a one-line string.</span></span>

<span data-ttu-id="234a5-195">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-196">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="234a5-196">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="234a5-199">Алгоритм или инструмент, используемый устройством для поддержки сжатия.</span><span class="sxs-lookup"><span data-stu-id="234a5-199">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="234a5-200">Если нет возможности описать схему сжатия (возможно, потому, что она неизвестна), используйте следующие слова: "Unknown", чтобы указать, что устройство поддерживает сжатие данных. "Сжатый" для представления того, что устройство поддерживает возможности сжатия, но либо схема сжатия неизвестна, либо не раскрывается. и "не сжато" для представления того, что устройство не поддерживает возможности сжатия.</span><span class="sxs-lookup"><span data-stu-id="234a5-200">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="234a5-201">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="234a5-202">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="234a5-202">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="234a5-203">Схема сжатия неизвестна или не описана.</span><span class="sxs-lookup"><span data-stu-id="234a5-203">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="234a5-204">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="234a5-204">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="234a5-205">Логический файл сжат, но схема сжатия неизвестна или не описана</span><span class="sxs-lookup"><span data-stu-id="234a5-205">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="234a5-206">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="234a5-206">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="234a5-207">Если логический файл не сжат</span><span class="sxs-lookup"><span data-stu-id="234a5-207">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="234a5-208">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="234a5-208">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-209">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="234a5-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-211">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="234a5-211">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-212">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="234a5-212">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="234a5-213">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-213">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="234a5-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="234a5-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="234a5-215"> (0)</span><span class="sxs-lookup"><span data-stu-id="234a5-215">(0)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-216">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="234a5-216">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="234a5-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="234a5-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="234a5-218">(1)</span><span class="sxs-lookup"><span data-stu-id="234a5-218">(1)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-219">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="234a5-219">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="234a5-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="234a5-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="234a5-221">(2)</span><span class="sxs-lookup"><span data-stu-id="234a5-221">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="234a5-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="234a5-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="234a5-223">(3)</span><span class="sxs-lookup"><span data-stu-id="234a5-223">(3)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-224">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="234a5-224">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="234a5-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="234a5-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="234a5-226">(4)</span><span class="sxs-lookup"><span data-stu-id="234a5-226">(4)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-227">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="234a5-227">Device is not working properly.</span></span> <span data-ttu-id="234a5-228">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="234a5-228">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="234a5-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="234a5-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="234a5-230">(5)</span><span class="sxs-lookup"><span data-stu-id="234a5-230">(5)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-231">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="234a5-231">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="234a5-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="234a5-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="234a5-233"> (6)</span><span class="sxs-lookup"><span data-stu-id="234a5-233">(6)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-234">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="234a5-234">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="234a5-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="234a5-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="234a5-236">(7)</span><span class="sxs-lookup"><span data-stu-id="234a5-236">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="234a5-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="234a5-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="234a5-238">(8)</span><span class="sxs-lookup"><span data-stu-id="234a5-238">(8)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-239">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="234a5-239">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="234a5-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="234a5-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="234a5-241">(9)</span><span class="sxs-lookup"><span data-stu-id="234a5-241">(9)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-242">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="234a5-242">Device is not working properly.</span></span> <span data-ttu-id="234a5-243">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="234a5-243">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="234a5-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="234a5-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="234a5-245">(10)</span><span class="sxs-lookup"><span data-stu-id="234a5-245">(10)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-246">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="234a5-246">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="234a5-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="234a5-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="234a5-248">(11)</span><span class="sxs-lookup"><span data-stu-id="234a5-248">(11)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-249">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="234a5-249">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="234a5-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="234a5-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="234a5-251">(12)</span><span class="sxs-lookup"><span data-stu-id="234a5-251">(12)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-252">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="234a5-252">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="234a5-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="234a5-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="234a5-254">(13)</span><span class="sxs-lookup"><span data-stu-id="234a5-254">(13)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-255">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="234a5-255">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="234a5-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="234a5-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="234a5-257">(14)</span><span class="sxs-lookup"><span data-stu-id="234a5-257">(14)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-258">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="234a5-258">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="234a5-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="234a5-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="234a5-260">(15)</span><span class="sxs-lookup"><span data-stu-id="234a5-260">(15)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-261">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="234a5-261">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="234a5-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="234a5-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="234a5-263">(16)</span><span class="sxs-lookup"><span data-stu-id="234a5-263">(16)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-264">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="234a5-264">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="234a5-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="234a5-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="234a5-266">(17)</span><span class="sxs-lookup"><span data-stu-id="234a5-266">(17)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-267">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="234a5-267">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="234a5-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="234a5-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="234a5-269">(18)</span><span class="sxs-lookup"><span data-stu-id="234a5-269">(18)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-270">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="234a5-270">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="234a5-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="234a5-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="234a5-272">(19)</span><span class="sxs-lookup"><span data-stu-id="234a5-272">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="234a5-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="234a5-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="234a5-274">(20)</span><span class="sxs-lookup"><span data-stu-id="234a5-274">(20)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-275">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="234a5-275">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="234a5-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="234a5-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="234a5-277">(21)</span><span class="sxs-lookup"><span data-stu-id="234a5-277">(21)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-278">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="234a5-278">System failure.</span></span> <span data-ttu-id="234a5-279">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="234a5-279">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="234a5-280">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="234a5-280">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="234a5-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="234a5-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="234a5-282">(22)</span><span class="sxs-lookup"><span data-stu-id="234a5-282">(22)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-283">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="234a5-283">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="234a5-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="234a5-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="234a5-285">(23)</span><span class="sxs-lookup"><span data-stu-id="234a5-285">(23)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-286">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="234a5-286">System failure.</span></span> <span data-ttu-id="234a5-287">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="234a5-287">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="234a5-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="234a5-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="234a5-289">(24)</span><span class="sxs-lookup"><span data-stu-id="234a5-289">(24)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-290">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="234a5-290">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="234a5-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="234a5-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="234a5-292">(25)</span><span class="sxs-lookup"><span data-stu-id="234a5-292">(25)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-293">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="234a5-293">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="234a5-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="234a5-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="234a5-295">(26)</span><span class="sxs-lookup"><span data-stu-id="234a5-295">(26)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-296">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="234a5-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="234a5-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="234a5-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="234a5-298">(27)</span><span class="sxs-lookup"><span data-stu-id="234a5-298">(27)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-299">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="234a5-299">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="234a5-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="234a5-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="234a5-301">(28)</span><span class="sxs-lookup"><span data-stu-id="234a5-301">(28)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-302">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="234a5-302">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="234a5-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="234a5-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="234a5-304">(29)</span><span class="sxs-lookup"><span data-stu-id="234a5-304">(29)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-305">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="234a5-305">Device is disabled.</span></span> <span data-ttu-id="234a5-306">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="234a5-306">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="234a5-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="234a5-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="234a5-308">(30)</span><span class="sxs-lookup"><span data-stu-id="234a5-308">(30)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-309">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="234a5-309">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="234a5-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="234a5-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="234a5-311">1-31</span><span class="sxs-lookup"><span data-stu-id="234a5-311">(31)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-312">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="234a5-312">Device is not working properly.</span></span> <span data-ttu-id="234a5-313">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="234a5-313">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="234a5-314">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="234a5-314">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-315">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="234a5-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-317">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="234a5-317">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-318">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="234a5-318">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="234a5-319">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-320">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="234a5-320">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-323">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="234a5-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="234a5-324">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="234a5-324">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="234a5-325">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="234a5-325">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="234a5-326">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-327">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="234a5-327">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-328">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="234a5-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-330">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="234a5-330">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-331">Размер блока по умолчанию (в байтах) для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="234a5-331">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="234a5-332">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-332">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="234a5-333">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="234a5-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-334">**Описание**</span><span class="sxs-lookup"><span data-stu-id="234a5-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-335">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-337">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="234a5-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-338">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="234a5-338">Description of the object.</span></span>

<span data-ttu-id="234a5-339">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-340">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="234a5-340">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-341">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-343">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жетлогикалдривестрингс")</span><span class="sxs-lookup"><span data-stu-id="234a5-343">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetLogicalDriveStrings")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-344">Уникальный идентификатор для устройства чтения компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="234a5-344">Unique identifier for a CD-ROM drive.</span></span>

<span data-ttu-id="234a5-345">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-346">**Накопитель**</span><span class="sxs-lookup"><span data-stu-id="234a5-346">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-349">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жетдриветипе")</span><span class="sxs-lookup"><span data-stu-id="234a5-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-350">Буква дисковода компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="234a5-350">Drive letter of the CD-ROM drive.</span></span>

<span data-ttu-id="234a5-351">Пример: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="234a5-351">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="234a5-352">**дривеинтегрити**</span><span class="sxs-lookup"><span data-stu-id="234a5-352">**DriveIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-353">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="234a5-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-355">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="234a5-355">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-356">Если **значение — true**, файлы могут быть правильно считаны с компакт-устройства.</span><span class="sxs-lookup"><span data-stu-id="234a5-356">If **True**, files can be accurately read from the CD device.</span></span> <span data-ttu-id="234a5-357">Это достигается путем считывания блока данных дважды и сравнения данных с самим собой.</span><span class="sxs-lookup"><span data-stu-id="234a5-357">This is achieved by reading a block of data twice and comparing the data against itself.</span></span>

</dd> <dt>

<span data-ttu-id="234a5-358">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="234a5-358">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-359">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="234a5-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="234a5-361">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="234a5-361">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="234a5-362">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-363">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="234a5-363">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-364">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="234a5-366">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="234a5-366">More information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="234a5-367">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-368">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="234a5-368">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-369">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="234a5-371">Тип обнаружения и исправления ошибок, поддерживаемых этим устройством.</span><span class="sxs-lookup"><span data-stu-id="234a5-371">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="234a5-372">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-372">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-373">**филесистемфлагс**</span><span class="sxs-lookup"><span data-stu-id="234a5-373">**FileSystemFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-374">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="234a5-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-376">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции Win32API файловой системы \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="234a5-376">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-377">Это свойство устарело.</span><span class="sxs-lookup"><span data-stu-id="234a5-377">This property is obsolete.</span></span> <span data-ttu-id="234a5-378">Вместо этого свойства используйте **филесистемфлагсекс**.</span><span class="sxs-lookup"><span data-stu-id="234a5-378">In place of this property, use **FileSystemFlagsEx**.</span></span>

</dd> <dt>

<span data-ttu-id="234a5-379">**филесистемфлагсекс**</span><span class="sxs-lookup"><span data-stu-id="234a5-379">**FileSystemFlagsEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-380">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="234a5-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-382">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="234a5-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-383">Флаги файловой системы, связанные с устройством чтения компакт-дисков Windows.</span><span class="sxs-lookup"><span data-stu-id="234a5-383">File system flags associated with the Windows CD-ROM drive.</span></span> <span data-ttu-id="234a5-384">Этот параметр может быть любым сочетанием флагов, **но \_ \_ Сжатие файлов FS и файл** **\_ \_ - \_ Vol** со степенью сжатия являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="234a5-384">This parameter can be any combination of flags, but **FS\_FILE\_COMPRESSION** and **FS\_VOL\_IS\_COMPRESSED** are mutually exclusive.</span></span>

<dt>

<span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>

<span data-ttu-id="234a5-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Поиск с учетом регистра** (1)</span><span class="sxs-lookup"><span data-stu-id="234a5-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Case Sensitive Search** (1)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-386">Файловая система поддерживает имена файлов с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="234a5-386">The file system supports case-sensitive file names.</span></span>

</dd> <dt>

<span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>

<span data-ttu-id="234a5-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Имена с сохранением регистра** (2)</span><span class="sxs-lookup"><span data-stu-id="234a5-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Case Preserved Names** (2)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-388">Файловая система сохраняет регистр имен файлов при размещении на диске имени.</span><span class="sxs-lookup"><span data-stu-id="234a5-388">The file system preserves the case of file names when it places a name on a disk.</span></span>

</dd> <dt>

<span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>

<span data-ttu-id="234a5-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Юникод на диске** (4)</span><span class="sxs-lookup"><span data-stu-id="234a5-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode On Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-390">Файловая система поддерживает Юникод в именах файлов по мере их появления на диске.</span><span class="sxs-lookup"><span data-stu-id="234a5-390">The file system supports Unicode in file names as they appear on the disk.</span></span>

</dd> <dt>

<span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>

<span data-ttu-id="234a5-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Постоянные списки ACL** (8)</span><span class="sxs-lookup"><span data-stu-id="234a5-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Persistent ACLs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-392">Файловая система сохраняет и обеспечивает применение списков управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="234a5-392">The file system preserves and enforces access control lists (ACLs).</span></span> <span data-ttu-id="234a5-393">Например, файловая система NTFS сохраняет и применяет списки ACL, а файловая система FAT — нет.</span><span class="sxs-lookup"><span data-stu-id="234a5-393">For example, the NTFS file system preserves and enforces ACLs and the FAT file system does not.</span></span>

</dd> <dt>

<span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>

<span data-ttu-id="234a5-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**Сжатие файлов** (16)</span><span class="sxs-lookup"><span data-stu-id="234a5-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**File Compression** (16)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-395">Файловая система поддерживает сжатие на основе файлов.</span><span class="sxs-lookup"><span data-stu-id="234a5-395">The file system supports file-based compression.</span></span>

</dd> <dt>

<span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>

<span data-ttu-id="234a5-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Квоты томов** (32)</span><span class="sxs-lookup"><span data-stu-id="234a5-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Volume Quotas** (32)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-397">Файловая система поддерживает дисковые квоты.</span><span class="sxs-lookup"><span data-stu-id="234a5-397">The file system supports disk quotas.</span></span>

</dd> <dt>

<span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>

<span data-ttu-id="234a5-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Поддержка разреженных файлов** (64)</span><span class="sxs-lookup"><span data-stu-id="234a5-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Supports Sparse Files** (64)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-399">Файловая система поддерживает резервные файлы.</span><span class="sxs-lookup"><span data-stu-id="234a5-399">The file system supports spare files.</span></span>

</dd> <dt>

<span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>

<span data-ttu-id="234a5-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Поддержка точек повторного анализа** (128)</span><span class="sxs-lookup"><span data-stu-id="234a5-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Supports Reparse Points** (128)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-401">Файловая система поддерживает точки повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="234a5-401">The file system supports reparse points.</span></span>

</dd> <dt>

<span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>

<span data-ttu-id="234a5-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Поддержка удаленного хранилища** (256)</span><span class="sxs-lookup"><span data-stu-id="234a5-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Supports Remote Storage** (256)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-403">Файловая система поддерживает удаленное хранение файлов.</span><span class="sxs-lookup"><span data-stu-id="234a5-403">The file system supports the remote storage of files.</span></span>

</dd> <dt>

<span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>

<span data-ttu-id="234a5-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Поддержка длинных имен** (16384)</span><span class="sxs-lookup"><span data-stu-id="234a5-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Supports Long Names** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-405">Файловая система поддерживает имена файлов длиной более восьми символов.</span><span class="sxs-lookup"><span data-stu-id="234a5-405">The file system supports file names that are longer than eight characters.</span></span>

</dd> <dt>

<span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>

<span data-ttu-id="234a5-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Том сжат** (32768)</span><span class="sxs-lookup"><span data-stu-id="234a5-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Volume Is Compressed** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-407">Указанный том диска является сжатым томом, например томом DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="234a5-407">The specified disk volume is a compressed volume, for example, a DoubleSpace volume.</span></span>

</dd> <dt>

<span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>

<span data-ttu-id="234a5-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Том только для чтения** (524289)</span><span class="sxs-lookup"><span data-stu-id="234a5-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Read Only Volume** (524289)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-409">Указанный том доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="234a5-409">The specified volume is read-only.</span></span>

</dd> <dt>

<span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>

<span data-ttu-id="234a5-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Поддержка идентификаторов объектов** (65536)</span><span class="sxs-lookup"><span data-stu-id="234a5-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Supports Object IDS** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-411">Файловая система поддерживает идентификаторы объектов.</span><span class="sxs-lookup"><span data-stu-id="234a5-411">The file system supports object identifiers.</span></span>

</dd> <dt>

<span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>

<span data-ttu-id="234a5-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Поддержка шифрования** (131072)</span><span class="sxs-lookup"><span data-stu-id="234a5-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Supports Encryption** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-413">Файловая система поддерживает шифрованную файловую систему (EFS).</span><span class="sxs-lookup"><span data-stu-id="234a5-413">The file system supports the Encrypted File System (EFS).</span></span>

</dd> <dt>

<span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>

<span data-ttu-id="234a5-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Поддерживает именованные потоки** (262144)</span><span class="sxs-lookup"><span data-stu-id="234a5-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Supports Named Streams** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-415">Файловая система поддерживает именованные потоки.</span><span class="sxs-lookup"><span data-stu-id="234a5-415">The file system supports named streams.</span></span>

</dd> </dl>

<span data-ttu-id="234a5-416">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="234a5-416">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="234a5-417">**Id**</span><span class="sxs-lookup"><span data-stu-id="234a5-417">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-418">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-420">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жетдриветипе")</span><span class="sxs-lookup"><span data-stu-id="234a5-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-421">Буква диска, однозначно определяющая устройство чтения компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="234a5-421">Drive letter that uniquely identifies this CD-ROM drive.</span></span>

<span data-ttu-id="234a5-422">Пример: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="234a5-422">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="234a5-423">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="234a5-423">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-424">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="234a5-424">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-426">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="234a5-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-427">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="234a5-427">Date and time the object is installed.</span></span> <span data-ttu-id="234a5-428">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="234a5-428">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="234a5-429">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-430">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="234a5-430">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-431">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="234a5-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="234a5-433">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="234a5-433">Last error code reported by the logical device.</span></span>

<span data-ttu-id="234a5-434">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-434">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-435">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="234a5-435">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-438">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="234a5-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-439">Изготовитель устройства чтения компакт-дисков Windows.</span><span class="sxs-lookup"><span data-stu-id="234a5-439">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="234a5-440">Пример: "ПЛЕКСТОР"</span><span class="sxs-lookup"><span data-stu-id="234a5-440">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="234a5-441">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="234a5-441">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-442">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="234a5-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-444">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="234a5-444">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-445">Максимальный размер блока в байтах для носителя, доступного этому устройству.</span><span class="sxs-lookup"><span data-stu-id="234a5-445">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="234a5-446">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-446">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="234a5-447">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="234a5-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-448">**максимумкомпонентленгс**</span><span class="sxs-lookup"><span data-stu-id="234a5-448">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-449">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="234a5-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-451">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="234a5-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-452">Максимальная длина компонента имени файла, поддерживаемого дисководом компакт-дисков Windows.</span><span class="sxs-lookup"><span data-stu-id="234a5-452">Maximum length of a filename component supported by the Windows CD-ROM drive.</span></span> <span data-ttu-id="234a5-453">Компонент имени файла часть имени файла между символами обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="234a5-453">A file name component the portion of a file name between backslashes.</span></span> <span data-ttu-id="234a5-454">Значение можно использовать, чтобы указать, что в указанной файловой системе поддерживаются длинные имена.</span><span class="sxs-lookup"><span data-stu-id="234a5-454">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="234a5-455">Например, для файловой системы FAT, поддерживающей длинные имена, функция сохраняет значение 255, а не предыдущий индикатор 8,3.</span><span class="sxs-lookup"><span data-stu-id="234a5-455">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="234a5-456">Длинные имена также могут поддерживаться в системах, использующих файловую систему NTFS.</span><span class="sxs-lookup"><span data-stu-id="234a5-456">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="234a5-457">Пример: 255</span><span class="sxs-lookup"><span data-stu-id="234a5-457">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="234a5-458">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="234a5-458">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-459">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="234a5-459">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-461">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="234a5-461">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-462">Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="234a5-462">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="234a5-463">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="234a5-464">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="234a5-464">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-465">**медиалоадед**</span><span class="sxs-lookup"><span data-stu-id="234a5-465">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-466">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="234a5-466">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-467">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-468">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="234a5-468">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-469">Если задано **значение true**, компакт-диск находится в дисководе.</span><span class="sxs-lookup"><span data-stu-id="234a5-469">If **True**, a CD-ROM is in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="234a5-470">**Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="234a5-470">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-471">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-473">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| жетдриветипе")</span><span class="sxs-lookup"><span data-stu-id="234a5-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-474">Тип носителя, который может использоваться этим устройством или к которому можно получить доступ.</span><span class="sxs-lookup"><span data-stu-id="234a5-474">Type of media that can be used or accessed by this device.</span></span> <span data-ttu-id="234a5-475">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="234a5-475">Possible values are:</span></span>

<dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="234a5-476">**Произвольный доступ** ("случайный доступ")</span><span class="sxs-lookup"><span data-stu-id="234a5-476">**Random Access** ("Random Access")</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="234a5-477">**Поддерживает запись** ("поддерживает запись")</span><span class="sxs-lookup"><span data-stu-id="234a5-477">**Supports Writing** ("Supports Writing")</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="234a5-478">**Съемный носитель** (съемный носитель)</span><span class="sxs-lookup"><span data-stu-id="234a5-478">**Removable Media** ("Removable Media")</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="234a5-479">**компакт-** диск ("CD-ROM")</span><span class="sxs-lookup"><span data-stu-id="234a5-479">**CD-ROM** ("CD-ROM")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="234a5-480">**мфрассигнедревисионлевел**</span><span class="sxs-lookup"><span data-stu-id="234a5-480">**MfrAssignedRevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-483">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK \| кернелмодедриверс \| [**Storage \_ Device \_ дескриптор**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| продуктревисионоффсет")</span><span class="sxs-lookup"><span data-stu-id="234a5-483">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK\|KernelModeDrivers\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-484">Уровень редакции встроенного по, назначенный производителем.</span><span class="sxs-lookup"><span data-stu-id="234a5-484">Firmware revision level that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="234a5-485">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="234a5-485">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-486">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="234a5-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-488">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="234a5-488">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-489">Минимальный размер блока в байтах для носителя, доступного этому устройству.</span><span class="sxs-lookup"><span data-stu-id="234a5-489">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="234a5-490">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-490">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="234a5-491">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="234a5-491">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-492">**Name**</span><span class="sxs-lookup"><span data-stu-id="234a5-492">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-493">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-494">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-495">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="234a5-495">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-496">Метка для объекта.</span><span class="sxs-lookup"><span data-stu-id="234a5-496">Label for the object.</span></span> <span data-ttu-id="234a5-497">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="234a5-497">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="234a5-498">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-498">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-499">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="234a5-499">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-500">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="234a5-500">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-501">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="234a5-502">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="234a5-502">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="234a5-503">Возможность ручной или автоматической очистки указывается в свойстве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="234a5-503">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="234a5-504">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-504">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-505">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="234a5-505">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-506">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="234a5-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="234a5-508">Максимальное количество носителей, которые можно поддерживать или вставлять, если устройство доступа к носителю поддерживает несколько отдельных носителей.</span><span class="sxs-lookup"><span data-stu-id="234a5-508">Maximum number of media that can be supported or inserted, when the media access device supports multiple individual media.</span></span>

<span data-ttu-id="234a5-509">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-509">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-510">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="234a5-510">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-511">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-512">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-513">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="234a5-513">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-514">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="234a5-514">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="234a5-515">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-515">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="234a5-516">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="234a5-516">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="234a5-517">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="234a5-517">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-518">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="234a5-518">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="234a5-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="234a5-520">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="234a5-520">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="234a5-521">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-521">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="234a5-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="234a5-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="234a5-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="234a5-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-524">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="234a5-524">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="234a5-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="234a5-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="234a5-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="234a5-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-527">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="234a5-527">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="234a5-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="234a5-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-529">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="234a5-529">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="234a5-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="234a5-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-531">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="234a5-531">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="234a5-532">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="234a5-532">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="234a5-533">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="234a5-533">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="234a5-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="234a5-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-535">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState*, установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="234a5-535">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="234a5-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="234a5-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="234a5-537">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="234a5-537">Timed Power-On Supported</span></span>

<span data-ttu-id="234a5-538">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="234a5-538">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="234a5-539">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="234a5-539">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-540">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="234a5-540">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-541">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-541">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="234a5-542">Если **значение — true**, устройство может управляться с помощью управления питанием. Это означает, что его можно перевести в режим приостановки и т. д.</span><span class="sxs-lookup"><span data-stu-id="234a5-542">If **True**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="234a5-543">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="234a5-543">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="234a5-544">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-544">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-545">**ревисионлевел**</span><span class="sxs-lookup"><span data-stu-id="234a5-545">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-546">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-547">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-548">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| ревисионлевел")</span><span class="sxs-lookup"><span data-stu-id="234a5-548">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|RevisionLevel")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-549">Уровень редакции встроенного по устройства чтения компакт-дисков Windows.</span><span class="sxs-lookup"><span data-stu-id="234a5-549">Firmware revision level of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="234a5-550">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="234a5-550">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-551">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="234a5-551">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-552">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-553">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SCSI-структуры \| [**SCSI \_ \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| пасид")</span><span class="sxs-lookup"><span data-stu-id="234a5-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-554">Номер шины SCSI для диска.</span><span class="sxs-lookup"><span data-stu-id="234a5-554">SCSI bus number for the disk drive.</span></span>

<span data-ttu-id="234a5-555">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="234a5-555">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="234a5-556">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="234a5-556">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-557">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="234a5-557">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-558">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-559">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SCSI Structures \| [**SCSI \_ \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| LUN")</span><span class="sxs-lookup"><span data-stu-id="234a5-559">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-560">Логический номер устройства (LUN) SCSI диска.</span><span class="sxs-lookup"><span data-stu-id="234a5-560">SCSI logical unit number (LUN) of the disk drive.</span></span> <span data-ttu-id="234a5-561">LUN используется для обозначения контроллера SCSI, к которому осуществляется доступ в системе, где используется более одного контроллера.</span><span class="sxs-lookup"><span data-stu-id="234a5-561">The LUN is used to designate which SCSI controller is being accessed in a system with more than one controller being used.</span></span> <span data-ttu-id="234a5-562">Идентификатор устройства SCSI аналогичен, но представляет собой обозначение нескольких устройств на одном контроллере.</span><span class="sxs-lookup"><span data-stu-id="234a5-562">The SCSI device identifier is similar, but is the designation for multiple devices on one controller.</span></span>

<span data-ttu-id="234a5-563">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="234a5-563">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="234a5-564">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="234a5-564">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-565">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="234a5-565">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-566">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-567">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SCSI-структуры \| [**SCSI \_ \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| сксистатус")</span><span class="sxs-lookup"><span data-stu-id="234a5-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|ScsiStatus")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-568">Номер порта SCSI диска.</span><span class="sxs-lookup"><span data-stu-id="234a5-568">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="234a5-569">Пример: 1</span><span class="sxs-lookup"><span data-stu-id="234a5-569">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="234a5-570">**скситаржетид**</span><span class="sxs-lookup"><span data-stu-id="234a5-570">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-571">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="234a5-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-572">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-573">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| DeviceIoControl \| ioctl \_ SCSI \_ Get \_ Address")</span><span class="sxs-lookup"><span data-stu-id="234a5-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|DeviceIoControl\|IOCTL\_SCSI\_GET\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-574">Номер идентификатора SCSI устройства чтения компакт-дисков Windows.</span><span class="sxs-lookup"><span data-stu-id="234a5-574">SCSI identifier number of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="234a5-575">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="234a5-575">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="234a5-576">**Номер**</span><span class="sxs-lookup"><span data-stu-id="234a5-576">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-577">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-578">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-579">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры устройства \| [**хранения \_ \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| сериалнумбероффсет ")</span><span class="sxs-lookup"><span data-stu-id="234a5-579">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-580">Номер, предоставленный производителем для идентификации физического носителя.</span><span class="sxs-lookup"><span data-stu-id="234a5-580">Number supplied by the manufacturer that identifies the physical media.</span></span> <span data-ttu-id="234a5-581">Пример: WD-WM3493798728.</span><span class="sxs-lookup"><span data-stu-id="234a5-581">Example: WD-WM3493798728.</span></span>

</dd> <dt>

<span data-ttu-id="234a5-582">**Размер**</span><span class="sxs-lookup"><span data-stu-id="234a5-582">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-583">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="234a5-583">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-584">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-585">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жетдискфриспаце"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="234a5-585">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDiskFreeSpace"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-586">Размер диска.</span><span class="sxs-lookup"><span data-stu-id="234a5-586">Size of the disk drive.</span></span>

<span data-ttu-id="234a5-587">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="234a5-587">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-588">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="234a5-588">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-589">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-590">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-591">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="234a5-591">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-592">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="234a5-592">Current status of the object.</span></span> <span data-ttu-id="234a5-593">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="234a5-593">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="234a5-594">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="234a5-594">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="234a5-595">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="234a5-595">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="234a5-596">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="234a5-596">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="234a5-597">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="234a5-597">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="234a5-598">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-598">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="234a5-599">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="234a5-599">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="234a5-600">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="234a5-600">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="234a5-601">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="234a5-601">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="234a5-602">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="234a5-602">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="234a5-603">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="234a5-603">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="234a5-604">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="234a5-604">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="234a5-605">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="234a5-605">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="234a5-606">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="234a5-606">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="234a5-607">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="234a5-607">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="234a5-608">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="234a5-608">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="234a5-609">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="234a5-609">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="234a5-610">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="234a5-610">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="234a5-611">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="234a5-611">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="234a5-612">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="234a5-612">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-613">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="234a5-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-614">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-615">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="234a5-615">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-616">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="234a5-616">State of the logical device.</span></span> <span data-ttu-id="234a5-617">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="234a5-617">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="234a5-618">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-618">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="234a5-619">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="234a5-619">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="234a5-620">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="234a5-620">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="234a5-621">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="234a5-621">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="234a5-622">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="234a5-622">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="234a5-623">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="234a5-623">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="234a5-624">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="234a5-624">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-625">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-626">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-626">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-627">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="234a5-627">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="234a5-628">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="234a5-628">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="234a5-629">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-629">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-630">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="234a5-630">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-631">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-632">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-632">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-633">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="234a5-633">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="234a5-634">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="234a5-634">Name of the scoping system.</span></span>

<span data-ttu-id="234a5-635">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="234a5-635">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="234a5-636">**трансферрате**</span><span class="sxs-lookup"><span data-stu-id="234a5-636">**TransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-637">Тип данных: **real64**</span><span class="sxs-lookup"><span data-stu-id="234a5-637">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-638">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-638">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-639">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| ссылка на файл Win32API и Справочник по времени"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайт в секунду")</span><span class="sxs-lookup"><span data-stu-id="234a5-639">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Reference and Time Reference"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes per second")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-640">Скорость передачи устройства чтения компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="234a5-640">Transfer rate of the CD-ROM drive.</span></span> <span data-ttu-id="234a5-641">Значение-1 указывает, что скорость не может быть определена.</span><span class="sxs-lookup"><span data-stu-id="234a5-641">A value of -1 indicates that the rate cannot be determined.</span></span> <span data-ttu-id="234a5-642">В этом случае компакт-диск не находится на диске.</span><span class="sxs-lookup"><span data-stu-id="234a5-642">When this happens, the CD is not in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="234a5-643">**Тома**</span><span class="sxs-lookup"><span data-stu-id="234a5-643">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-644">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-644">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-645">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-646">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="234a5-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-647">Имя тома компакт-диска Windows.</span><span class="sxs-lookup"><span data-stu-id="234a5-647">Volume name of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="234a5-648">**волумесериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="234a5-648">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234a5-649">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="234a5-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="234a5-650">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234a5-650">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234a5-651">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="234a5-651">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="234a5-652">Серийный номер тома носителя в устройстве чтения компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="234a5-652">Volume serial number of the media in the CD-ROM drive.</span></span>

<span data-ttu-id="234a5-653">Пример: A8C3-D032</span><span class="sxs-lookup"><span data-stu-id="234a5-653">Example: A8C3-D032</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="234a5-654">Комментарии</span><span class="sxs-lookup"><span data-stu-id="234a5-654">Remarks</span></span>

<span data-ttu-id="234a5-655">Класс **Win32 \_ кдромдриве** является производным от [**CIM \_ кдромдриве**](cim-cdromdrive.md) , который является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="234a5-655">The **Win32\_CDROMDrive** class is derived from [**CIM\_CDROMDrive**](cim-cdromdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="234a5-656">Класс **CIM \_ медиаакцессдевице** является производным от [**CIM \_**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="234a5-656">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="234a5-657">Примеры</span><span class="sxs-lookup"><span data-stu-id="234a5-657">Examples</span></span>

<span data-ttu-id="234a5-658">В следующем примере на языке VBScript определяется, находится ли компакт-диск в дисководе CDROM.</span><span class="sxs-lookup"><span data-stu-id="234a5-658">The following VBScript example determines if a CD is in a CDROM drive.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject(_
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery( _
    "Select * from Win32_CDROMDrive")
For Each objItem in colItems
    Wscript.Echo "Device ID: " _
        & objItem.DeviceID
    Wscript.Echo "Media Loaded: " _
        & objItem.MediaLoaded
Next
```



## <a name="requirements"></a><span data-ttu-id="234a5-659">Требования</span><span class="sxs-lookup"><span data-stu-id="234a5-659">Requirements</span></span>



| <span data-ttu-id="234a5-660">Требование</span><span class="sxs-lookup"><span data-stu-id="234a5-660">Requirement</span></span> | <span data-ttu-id="234a5-661">Значение</span><span class="sxs-lookup"><span data-stu-id="234a5-661">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="234a5-662">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="234a5-662">Minimum supported client</span></span><br/> | <span data-ttu-id="234a5-663">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="234a5-663">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="234a5-664">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="234a5-664">Minimum supported server</span></span><br/> | <span data-ttu-id="234a5-665">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="234a5-665">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="234a5-666">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="234a5-666">Namespace</span></span><br/>                | <span data-ttu-id="234a5-667">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="234a5-667">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="234a5-668">MOF</span><span class="sxs-lookup"><span data-stu-id="234a5-668">MOF</span></span><br/>                      | <dl> <span data-ttu-id="234a5-669"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="234a5-669"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="234a5-670">DLL</span><span class="sxs-lookup"><span data-stu-id="234a5-670">DLL</span></span><br/>                      | <dl> <span data-ttu-id="234a5-671"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="234a5-671"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="234a5-672">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="234a5-672">See also</span></span>

<dl> <dt>

[<span data-ttu-id="234a5-673">**\_КДРОМДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="234a5-673">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dt>

[<span data-ttu-id="234a5-674">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="234a5-674">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="234a5-675">Задачи WMI: оборудование компьютера</span><span class="sxs-lookup"><span data-stu-id="234a5-675">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="234a5-676">Задачи WMI: диски и файловые системы</span><span class="sxs-lookup"><span data-stu-id="234a5-676">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

