---
description: '&Win32 \_ маппедлогикалдиск \# 32; Класс WMI представляет сетевые устройства хранения, сопоставленные как логические диски в компьютерной системе.'
ms.assetid: 5dd4b0eb-7872-4f2d-9c8b-ea03f7e2c16d
ms.tgt_platform: multiple
title: Класс Win32_MappedLogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MappedLogicalDisk
- Win32_MappedLogicalDisk.Reset
- Win32_MappedLogicalDisk.SetPowerState
- Win32_MappedLogicalDisk.Access
- Win32_MappedLogicalDisk.Availability
- Win32_MappedLogicalDisk.BlockSize
- Win32_MappedLogicalDisk.Caption
- Win32_MappedLogicalDisk.Compressed
- Win32_MappedLogicalDisk.ConfigManagerErrorCode
- Win32_MappedLogicalDisk.ConfigManagerUserConfig
- Win32_MappedLogicalDisk.CreationClassName
- Win32_MappedLogicalDisk.Description
- Win32_MappedLogicalDisk.DeviceID
- Win32_MappedLogicalDisk.ErrorCleared
- Win32_MappedLogicalDisk.ErrorDescription
- Win32_MappedLogicalDisk.ErrorMethodology
- Win32_MappedLogicalDisk.FileSystem
- Win32_MappedLogicalDisk.FreeSpace
- Win32_MappedLogicalDisk.InstallDate
- Win32_MappedLogicalDisk.LastErrorCode
- Win32_MappedLogicalDisk.MaximumComponentLength
- Win32_MappedLogicalDisk.Name
- Win32_MappedLogicalDisk.NumberOfBlocks
- Win32_MappedLogicalDisk.PNPDeviceID
- Win32_MappedLogicalDisk.PowerManagementCapabilities
- Win32_MappedLogicalDisk.PowerManagementSupported
- Win32_MappedLogicalDisk.ProviderName
- Win32_MappedLogicalDisk.Purpose
- Win32_MappedLogicalDisk.QuotasDisabled
- Win32_MappedLogicalDisk.QuotasIncomplete
- Win32_MappedLogicalDisk.QuotasRebuilding
- Win32_MappedLogicalDisk.SessionID
- Win32_MappedLogicalDisk.Size
- Win32_MappedLogicalDisk.Status
- Win32_MappedLogicalDisk.StatusInfo
- Win32_MappedLogicalDisk.SupportsDiskQuotas
- Win32_MappedLogicalDisk.SupportsFileBasedCompression
- Win32_MappedLogicalDisk.SystemCreationClassName
- Win32_MappedLogicalDisk.SystemName
- Win32_MappedLogicalDisk.VolumeName
- Win32_MappedLogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75c3dfee876c34f36fd0b4cf0b59d3a61afcd75c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142682"
---
# <a name="win32_mappedlogicaldisk-class"></a><span data-ttu-id="b32d0-103">\_Класс Win32 маппедлогикалдиск</span><span class="sxs-lookup"><span data-stu-id="b32d0-103">Win32\_MappedLogicalDisk class</span></span>

<span data-ttu-id="b32d0-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ маппедлогикалдиск для Win32** представляет сетевые устройства хранения, сопоставленные как логические диски в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="b32d0-104">The **Win32\_MappedLogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents network storage devices that are mapped as logical disks on the computer system.</span></span>

<span data-ttu-id="b32d0-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b32d0-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="b32d0-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b32d0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b32d0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{BCF02FFE-5560-4de2-B419-272918693426}"), AMENDMENT]
class Win32_MappedLogicalDisk : CIM_LogicalDisk
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProviderName;
  string   Purpose;
  boolean  QuotasDisabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   SessionID;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="b32d0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b32d0-108">Members</span></span>

<span data-ttu-id="b32d0-109">Класс **Win32 \_ маппедлогикалдиск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b32d0-109">The **Win32\_MappedLogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="b32d0-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b32d0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b32d0-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b32d0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b32d0-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b32d0-112">Methods</span></span>

<span data-ttu-id="b32d0-113">Класс **Win32 \_ маппедлогикалдиск** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b32d0-113">The **Win32\_MappedLogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="b32d0-114">Метод</span><span class="sxs-lookup"><span data-stu-id="b32d0-114">Method</span></span>            | <span data-ttu-id="b32d0-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b32d0-115">Description</span></span>                                                                                                                                                                                |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b32d0-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="b32d0-116">**Reset**</span></span>         | <span data-ttu-id="b32d0-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="b32d0-117">Not implemented.</span></span> <span data-ttu-id="b32d0-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>                 |
| <span data-ttu-id="b32d0-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b32d0-119">**SetPowerState**</span></span> | <span data-ttu-id="b32d0-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="b32d0-120">Not implemented.</span></span> <span data-ttu-id="b32d0-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b32d0-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="b32d0-122">Properties</span></span>

<span data-ttu-id="b32d0-123">Класс **Win32 \_ маппедлогикалдиск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-123">The **Win32\_MappedLogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b32d0-124">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="b32d0-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b32d0-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-127">Состояние доступа устройства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-127">Device access state.</span></span>

<span data-ttu-id="b32d0-128">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b32d0-129">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b32d0-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="b32d0-130">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="b32d0-130">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="b32d0-131">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="b32d0-131">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="b32d0-132">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="b32d0-132">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="b32d0-133">**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="b32d0-133">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b32d0-134">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="b32d0-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b32d0-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-137">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="b32d0-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-138">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-138">Availability and status of the device.</span></span>

<span data-ttu-id="b32d0-139">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b32d0-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b32d0-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b32d0-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b32d0-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b32d0-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="b32d0-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-143">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="b32d0-143">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b32d0-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="b32d0-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b32d0-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="b32d0-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b32d0-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="b32d0-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b32d0-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="b32d0-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b32d0-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="b32d0-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-149">Автономная миграция</span><span class="sxs-lookup"><span data-stu-id="b32d0-149">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b32d0-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="b32d0-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b32d0-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="b32d0-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b32d0-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="b32d0-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b32d0-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="b32d0-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b32d0-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="b32d0-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-155">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b32d0-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b32d0-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="b32d0-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-157">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может демонстрировать снижение производительности.</span><span class="sxs-lookup"><span data-stu-id="b32d0-157">The device is in a power save state but still functioning and can exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b32d0-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="b32d0-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-159">Устройство не работает, но может быть включено в полный режим.</span><span class="sxs-lookup"><span data-stu-id="b32d0-159">The device is not functioning, but can be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b32d0-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="b32d0-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b32d0-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="b32d0-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-162">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b32d0-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b32d0-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="b32d0-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-164">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="b32d0-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b32d0-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="b32d0-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-166">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="b32d0-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b32d0-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="b32d0-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-168">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="b32d0-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b32d0-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="b32d0-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-170">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="b32d0-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b32d0-171">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="b32d0-171">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-172">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b32d0-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-174">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="b32d0-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-175">Размер (в байтах) блоков, образующих эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="b32d0-175">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="b32d0-176">Если эта концепция недопустима для типа устройства, значение равно 1.</span><span class="sxs-lookup"><span data-stu-id="b32d0-176">If this concept is not valid for the device type, the value is 1.</span></span>

<span data-ttu-id="b32d0-177">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-177">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b32d0-178">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b32d0-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-179">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b32d0-179">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-182">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b32d0-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-183">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b32d0-183">Short description of the object.</span></span>

<span data-ttu-id="b32d0-184">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-185">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="b32d0-185">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-186">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b32d0-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-188">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ Vol \_ \_ сжат")</span><span class="sxs-lookup"><span data-stu-id="b32d0-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-189">**Значение true**, если файл сжат.</span><span class="sxs-lookup"><span data-stu-id="b32d0-189">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-190">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b32d0-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-191">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b32d0-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-193">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b32d0-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-194">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b32d0-194">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b32d0-195">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b32d0-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b32d0-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="b32d0-197">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-198">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="b32d0-198">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b32d0-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b32d0-200">(1)</span><span class="sxs-lookup"><span data-stu-id="b32d0-200">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-201">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="b32d0-201">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b32d0-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b32d0-203">(2)</span><span class="sxs-lookup"><span data-stu-id="b32d0-203">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b32d0-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b32d0-205">(3)</span><span class="sxs-lookup"><span data-stu-id="b32d0-205">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-206">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b32d0-206">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b32d0-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b32d0-208">(4)</span><span class="sxs-lookup"><span data-stu-id="b32d0-208">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-209">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b32d0-209">Device is not working properly.</span></span> <span data-ttu-id="b32d0-210">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b32d0-210">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b32d0-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b32d0-212">(5)</span><span class="sxs-lookup"><span data-stu-id="b32d0-212">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-213">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="b32d0-213">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b32d0-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b32d0-215"> (6)</span><span class="sxs-lookup"><span data-stu-id="b32d0-215">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-216">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="b32d0-216">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b32d0-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b32d0-218">(7)</span><span class="sxs-lookup"><span data-stu-id="b32d0-218">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b32d0-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b32d0-220">(8)</span><span class="sxs-lookup"><span data-stu-id="b32d0-220">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-221">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-221">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b32d0-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b32d0-223">(9)</span><span class="sxs-lookup"><span data-stu-id="b32d0-223">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-224">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b32d0-224">Device is not working properly.</span></span> <span data-ttu-id="b32d0-225">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-225">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b32d0-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b32d0-227">(10)</span><span class="sxs-lookup"><span data-stu-id="b32d0-227">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-228">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="b32d0-228">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b32d0-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b32d0-230">(11)</span><span class="sxs-lookup"><span data-stu-id="b32d0-230">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-231">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-231">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b32d0-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b32d0-233">(12)</span><span class="sxs-lookup"><span data-stu-id="b32d0-233">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-234">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="b32d0-234">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b32d0-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b32d0-236">(13)</span><span class="sxs-lookup"><span data-stu-id="b32d0-236">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-237">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-237">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b32d0-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b32d0-239">(14)</span><span class="sxs-lookup"><span data-stu-id="b32d0-239">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-240">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="b32d0-240">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b32d0-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b32d0-242">(15)</span><span class="sxs-lookup"><span data-stu-id="b32d0-242">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-243">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="b32d0-243">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b32d0-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b32d0-245">(16)</span><span class="sxs-lookup"><span data-stu-id="b32d0-245">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-246">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="b32d0-246">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b32d0-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b32d0-248">(17)</span><span class="sxs-lookup"><span data-stu-id="b32d0-248">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-249">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b32d0-249">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b32d0-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b32d0-251">(18)</span><span class="sxs-lookup"><span data-stu-id="b32d0-251">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-252">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b32d0-252">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b32d0-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b32d0-254">(19)</span><span class="sxs-lookup"><span data-stu-id="b32d0-254">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b32d0-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b32d0-256">(20)</span><span class="sxs-lookup"><span data-stu-id="b32d0-256">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-257">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b32d0-257">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b32d0-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b32d0-259">(21)</span><span class="sxs-lookup"><span data-stu-id="b32d0-259">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-260">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b32d0-260">System failure.</span></span> <span data-ttu-id="b32d0-261">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b32d0-261">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b32d0-262">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="b32d0-262">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b32d0-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b32d0-264">(22)</span><span class="sxs-lookup"><span data-stu-id="b32d0-264">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-265">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b32d0-265">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b32d0-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b32d0-267">(23)</span><span class="sxs-lookup"><span data-stu-id="b32d0-267">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-268">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b32d0-268">System failure.</span></span> <span data-ttu-id="b32d0-269">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b32d0-269">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b32d0-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b32d0-271">(24)</span><span class="sxs-lookup"><span data-stu-id="b32d0-271">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-272">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="b32d0-272">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b32d0-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b32d0-274">(25)</span><span class="sxs-lookup"><span data-stu-id="b32d0-274">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-275">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b32d0-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b32d0-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b32d0-277">(26)</span><span class="sxs-lookup"><span data-stu-id="b32d0-277">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-278">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b32d0-278">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b32d0-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b32d0-280">(27)</span><span class="sxs-lookup"><span data-stu-id="b32d0-280">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-281">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="b32d0-281">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b32d0-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b32d0-283">(28)</span><span class="sxs-lookup"><span data-stu-id="b32d0-283">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-284">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="b32d0-284">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b32d0-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b32d0-286">(29)</span><span class="sxs-lookup"><span data-stu-id="b32d0-286">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-287">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b32d0-287">Device is disabled.</span></span> <span data-ttu-id="b32d0-288">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b32d0-288">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b32d0-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b32d0-290">(30)</span><span class="sxs-lookup"><span data-stu-id="b32d0-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-291">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="b32d0-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b32d0-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b32d0-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b32d0-293">1-31</span><span class="sxs-lookup"><span data-stu-id="b32d0-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-294">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b32d0-294">Device is not working properly.</span></span> <span data-ttu-id="b32d0-295">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b32d0-295">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b32d0-296">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="b32d0-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-297">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b32d0-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-299">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b32d0-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-300">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b32d0-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b32d0-301">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b32d0-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-305">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b32d0-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-306">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b32d0-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b32d0-307">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b32d0-307">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b32d0-308">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-309">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b32d0-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-312">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b32d0-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-313">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b32d0-313">Description of the object.</span></span>

<span data-ttu-id="b32d0-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b32d0-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-318">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b32d0-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-319">Уникальный идентификатор массива памяти.</span><span class="sxs-lookup"><span data-stu-id="b32d0-319">Unique identifier of the memory array.</span></span>

<span data-ttu-id="b32d0-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b32d0-321">Пример: "массив памяти 1"</span><span class="sxs-lookup"><span data-stu-id="b32d0-321">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-322">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="b32d0-322">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-323">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b32d0-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-325">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="b32d0-325">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b32d0-326">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-327">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b32d0-327">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-330">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="b32d0-330">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span>

<span data-ttu-id="b32d0-331">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-332">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="b32d0-332">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-335">Типы проверки ошибок, используемые оборудованием.</span><span class="sxs-lookup"><span data-stu-id="b32d0-335">Types of error checking used by the hardware.</span></span>

<span data-ttu-id="b32d0-336">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-336">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-337">**Системой**</span><span class="sxs-lookup"><span data-stu-id="b32d0-337">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-340">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="b32d0-340">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-341">Access type: Read-only</span></span>

<span data-ttu-id="b32d0-342">Файловая система на логическом диске.</span><span class="sxs-lookup"><span data-stu-id="b32d0-342">File system on the logical disk.</span></span>

<span data-ttu-id="b32d0-343">Пример: "NTFS"</span><span class="sxs-lookup"><span data-stu-id="b32d0-343">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-344">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="b32d0-344">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-345">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b32d0-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-347">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b32d0-347">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-348">Свободное место на логическом диске.</span><span class="sxs-lookup"><span data-stu-id="b32d0-348">Space available on the logical disk.</span></span>

<span data-ttu-id="b32d0-349">Это свойство наследуется от [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-349">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="b32d0-350">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b32d0-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-351">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b32d0-351">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-352">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b32d0-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-354">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b32d0-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-355">Access type: Read-only</span></span>

<span data-ttu-id="b32d0-356">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b32d0-356">Date and time the object was installed.</span></span> <span data-ttu-id="b32d0-357">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="b32d0-357">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b32d0-358">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-359">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b32d0-359">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-360">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b32d0-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-362">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="b32d0-362">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b32d0-363">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-364">**максимумкомпонентленгс**</span><span class="sxs-lookup"><span data-stu-id="b32d0-364">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-365">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b32d0-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-367">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="b32d0-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-368">Содержит максимальную длину компонента имени файла, поддерживаемого диском Windows.</span><span class="sxs-lookup"><span data-stu-id="b32d0-368">Contains the maximum length of a file-name component supported by the Windows drive.</span></span>

<span data-ttu-id="b32d0-369">Пример: 255</span><span class="sxs-lookup"><span data-stu-id="b32d0-369">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-370">**Name**</span><span class="sxs-lookup"><span data-stu-id="b32d0-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-371">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-373">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="b32d0-373">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-374">Метка объекта.</span><span class="sxs-lookup"><span data-stu-id="b32d0-374">Object label.</span></span>

<span data-ttu-id="b32d0-375">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-376">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="b32d0-376">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-377">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b32d0-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-379">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="b32d0-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-380">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="b32d0-380">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="b32d0-381">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-381">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="b32d0-382">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="b32d0-382">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="b32d0-383">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-383">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b32d0-384">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b32d0-384">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-385">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b32d0-385">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-386">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-388">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b32d0-388">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-389">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-389">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b32d0-390">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b32d0-391">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b32d0-391">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-392">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b32d0-392">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-393">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b32d0-393">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-395">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="b32d0-395">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b32d0-396">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-396">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b32d0-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b32d0-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b32d0-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b32d0-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b32d0-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="b32d0-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b32d0-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b32d0-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-401">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="b32d0-401">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b32d0-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="b32d0-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-403">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="b32d0-403">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b32d0-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="b32d0-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-405">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b32d0-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b32d0-406">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="b32d0-406">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b32d0-407">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b32d0-407">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b32d0-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="b32d0-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-409">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="b32d0-409">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b32d0-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="b32d0-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b32d0-411">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="b32d0-411">Timed Power-On Supported</span></span>

<span data-ttu-id="b32d0-412">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="b32d0-412">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b32d0-413">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="b32d0-413">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-414">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b32d0-414">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-416">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b32d0-416">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b32d0-417">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="b32d0-417">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b32d0-418">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-418">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-419">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="b32d0-419">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-420">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-422">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| сетевые функции Windows \| внетжетконнектион")</span><span class="sxs-lookup"><span data-stu-id="b32d0-422">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-423">Сетевой путь к логическому устройству.</span><span class="sxs-lookup"><span data-stu-id="b32d0-423">Network path name to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-424">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="b32d0-424">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-425">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-427">Произвольная строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="b32d0-427">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="b32d0-428">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-429">**куотасдисаблед**</span><span class="sxs-lookup"><span data-stu-id="b32d0-429">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-430">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b32d0-430">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-432">Если **значение — true**, Управление квотами для этого тома отключено.</span><span class="sxs-lookup"><span data-stu-id="b32d0-432">If **True**, quota management is not enabled for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-433">**куотасинкомплете**</span><span class="sxs-lookup"><span data-stu-id="b32d0-433">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-434">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b32d0-434">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-436">Если **значение — true**, используется управление квотами, но оно отключено.</span><span class="sxs-lookup"><span data-stu-id="b32d0-436">If **True**, quota management was used but has been disabled.</span></span> <span data-ttu-id="b32d0-437">Незавершенные ссылается на сведения, оставшиеся в файловой системе после отключения управления квотами.</span><span class="sxs-lookup"><span data-stu-id="b32d0-437">Incomplete refers to the information left in the file system after quota management has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-438">**куотасребуилдинг**</span><span class="sxs-lookup"><span data-stu-id="b32d0-438">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-439">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b32d0-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-441">Если **значение — true**, файловая система настраивается для управления квотами.</span><span class="sxs-lookup"><span data-stu-id="b32d0-441">If **True**, the file system is setting up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-442">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="b32d0-442">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-443">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-445">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b32d0-445">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-446">Идентификатор сеанса пользователя.</span><span class="sxs-lookup"><span data-stu-id="b32d0-446">ID of the user's session.</span></span> <span data-ttu-id="b32d0-447">Пользователь может подключиться с помощью локального имени входа или сеанса терминала.</span><span class="sxs-lookup"><span data-stu-id="b32d0-447">The user may be connected using a local login or a terminal session.</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-448">**Размер**</span><span class="sxs-lookup"><span data-stu-id="b32d0-448">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-449">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b32d0-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-451">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b32d0-451">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-452">Размер логического диска.</span><span class="sxs-lookup"><span data-stu-id="b32d0-452">Size of the logical disk.</span></span>

<span data-ttu-id="b32d0-453">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b32d0-453">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="b32d0-454">Это свойство наследуется от [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-454">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-455">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b32d0-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-456">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-458">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b32d0-458">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-459">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b32d0-459">Current status of the object.</span></span> <span data-ttu-id="b32d0-460">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="b32d0-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b32d0-461">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например, жесткий диск с поддержкой SMART может работать правильно, но прогнозирует сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="b32d0-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="b32d0-462">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="b32d0-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b32d0-463">Состояние службы применяется к административной работе, например к зеркальному переносу диска, перезагрузке списка разрешений пользователя или другой административной работе.</span><span class="sxs-lookup"><span data-stu-id="b32d0-463">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b32d0-464">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="b32d0-464">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b32d0-465">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b32d0-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b32d0-466">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="b32d0-466">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b32d0-467">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b32d0-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b32d0-468">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b32d0-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b32d0-469">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b32d0-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b32d0-470">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b32d0-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b32d0-471">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b32d0-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b32d0-472">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b32d0-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b32d0-473">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b32d0-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b32d0-474">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b32d0-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b32d0-475">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b32d0-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b32d0-476">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b32d0-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b32d0-477">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b32d0-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b32d0-478">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b32d0-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b32d0-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b32d0-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-480">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b32d0-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-482">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b32d0-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-483">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b32d0-483">State of the logical device.</span></span> <span data-ttu-id="b32d0-484">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="b32d0-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b32d0-485">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b32d0-486">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b32d0-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b32d0-487">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b32d0-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b32d0-488">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b32d0-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b32d0-489">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="b32d0-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b32d0-490">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="b32d0-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b32d0-491">**суппортсдисккуотас**</span><span class="sxs-lookup"><span data-stu-id="b32d0-491">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-492">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b32d0-492">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-493">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-494">Если **значение — true**, то файловая система, в которой сопоставлен этот сетевой диск, поддерживает дисковые квоты.</span><span class="sxs-lookup"><span data-stu-id="b32d0-494">If **True**, then the file system on which this network drive is mapped supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-495">**суппортсфилебаседкомпрессион**</span><span class="sxs-lookup"><span data-stu-id="b32d0-495">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-496">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b32d0-496">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-497">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-498">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System functions \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ File \_ Compression")</span><span class="sxs-lookup"><span data-stu-id="b32d0-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-499">Если **значение — true**, раздел логического диска поддерживает сжатие на основе файлов, как в случае с файловой системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="b32d0-499">If **True**, the logical disk partition supports file-based compression, such as is the case with NTFS.</span></span> <span data-ttu-id="b32d0-500">Это свойство имеет **значение false**, если **сжатое** свойство имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b32d0-500">This property is **False**, when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-501">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b32d0-501">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-502">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-503">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-504">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b32d0-504">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-505">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="b32d0-505">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b32d0-506">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-506">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-507">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b32d0-507">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-508">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-509">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-510">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b32d0-510">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-511">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="b32d0-511">Name of the scoping system.</span></span>

<span data-ttu-id="b32d0-512">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-512">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-513">**Тома**</span><span class="sxs-lookup"><span data-stu-id="b32d0-513">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-514">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-515">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b32d0-515">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-516">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="b32d0-516">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-517">Имя тома логического диска.</span><span class="sxs-lookup"><span data-stu-id="b32d0-517">Volume name of the logical disk.</span></span> <span data-ttu-id="b32d0-518">Значение этого свойства может содержать не более 32 символов.</span><span class="sxs-lookup"><span data-stu-id="b32d0-518">This property value can have a maximum of 32 characters.</span></span>

</dd> <dt>

<span data-ttu-id="b32d0-519">**волумесериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="b32d0-519">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b32d0-520">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b32d0-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-521">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b32d0-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b32d0-522">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="b32d0-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="b32d0-523">Серийный номер тома логического диска.</span><span class="sxs-lookup"><span data-stu-id="b32d0-523">Volume serial number of the logical disk.</span></span> <span data-ttu-id="b32d0-524">Значение этого свойства может содержать не более 11 символов.</span><span class="sxs-lookup"><span data-stu-id="b32d0-524">This property value can have a maximum of 11 characters.</span></span>

<span data-ttu-id="b32d0-525">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b32d0-525">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b32d0-526">Пример: "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="b32d0-526">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b32d0-527">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b32d0-527">Remarks</span></span>

<span data-ttu-id="b32d0-528">Для этого класса возвращаются следующие экземпляры, допустим, что пользователь а выполняет перечисление экземпляров:</span><span class="sxs-lookup"><span data-stu-id="b32d0-528">The instances returned for this class are as follows, supposing that user A is enumerating the instances:</span></span>

-   <span data-ttu-id="b32d0-529">Поставщик ищет сеанс входа пользователя а на этот компьютер:</span><span class="sxs-lookup"><span data-stu-id="b32d0-529">The provider looks for a logon session of user A on that machine:</span></span>

    -   <span data-ttu-id="b32d0-530">При наличии одного (и только одного) такого сеанса входа поставщик возвращает подключенные диски этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="b32d0-530">If there is one (and only one) such logon session, then the provider returns the mapped drives of that session.</span></span>
    -   <span data-ttu-id="b32d0-531">Если на компьютере имеется более одного сеанса, то не возвращаются экземпляры подключенных дисков (поскольку поставщик не имеет разумного способа выбора используемого сеанса).</span><span class="sxs-lookup"><span data-stu-id="b32d0-531">If there is more than one session for user A on the machine, then no mapped drive instances are returned (because the provider has no reasonable way of deciding which session to use).</span></span>

-   <span data-ttu-id="b32d0-532">Если сеансы пользователя A не запущены, и имеется локально вошедший в систему пользователь б:</span><span class="sxs-lookup"><span data-stu-id="b32d0-532">If there are no sessions of user A running, and there is a locally logged on user B:</span></span>

    -   <span data-ttu-id="b32d0-533">Если для пользователя б имеется один сеанс, поставщик олицетворяет и возвращает подключенные диски пользователя б. В этом случае поддерживается сценарий службы поддержки, желающий видеть экземпляры локального пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="b32d0-533">If there is a single session for user B, then the provider impersonates A and returns the mapped drives of user B. This case supports the scenario of Helpdesk wanting to see the instances of a locally logged on user.</span></span> <span data-ttu-id="b32d0-534">Тем не менее, возвращаемые экземпляры зависят от параметров локальной политики безопасности в панели управления средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="b32d0-534">However, whether instances are returned depends on the Local Security Policy settings in the Control Panel Administrative Tools.</span></span> <span data-ttu-id="b32d0-535">Если для следующей политики задано значение "создатель объекта", то не возвращаются экземпляры подключенных дисков, даже если член группы "Администраторы":</span><span class="sxs-lookup"><span data-stu-id="b32d0-535">If the following policy is set to "Object Creator", then no mapped drive instances are returned, even if A is a member of the Administrators group:</span></span>

        <span data-ttu-id="b32d0-536">"Системный объект: владелец по умолчанию для объектов, созданных членами группы" Администраторы ".</span><span class="sxs-lookup"><span data-stu-id="b32d0-536">"System object: default owner for objects created by members of the administrators group."</span></span>

    -   <span data-ttu-id="b32d0-537">Опять же, если на компьютере работает более одного сеанса пользователя B, поставщик не может решить, какой из них использовать.</span><span class="sxs-lookup"><span data-stu-id="b32d0-537">Again, if there is more than one session of user B running on the machine, then the provider has no way of deciding which to use.</span></span> <span data-ttu-id="b32d0-538">В этом случае не возвращаются экземпляры подключенных дисков.</span><span class="sxs-lookup"><span data-stu-id="b32d0-538">In this case, no mapped drive instances are returned.</span></span>

<span data-ttu-id="b32d0-539">Дополнительные сведения об использовании **Win32 \_ маппедлогикалдиск** см. в разделе [как определить диски, сопоставленные с сетевыми общими папками?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span><span class="sxs-lookup"><span data-stu-id="b32d0-539">For more information on using **Win32\_MappedLogicalDisk**, see [How Can I Determine Which Drives are Mapped to Network Shares?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="b32d0-540">Примеры</span><span class="sxs-lookup"><span data-stu-id="b32d0-540">Examples</span></span>

<span data-ttu-id="b32d0-541">В следующем фрагменте кода PowerShell показаны подключенные диски.</span><span class="sxs-lookup"><span data-stu-id="b32d0-541">The following PowerShell snippet shows mapped drives.</span></span>


```PowerShell
Get-WmiObject Win32_MappedLogicalDisk | Select Name, ProviderName, FileSystem, Size, FreeSpace | Format-Table
```



## <a name="requirements"></a><span data-ttu-id="b32d0-542">Требования</span><span class="sxs-lookup"><span data-stu-id="b32d0-542">Requirements</span></span>



| <span data-ttu-id="b32d0-543">Требование</span><span class="sxs-lookup"><span data-stu-id="b32d0-543">Requirement</span></span> | <span data-ttu-id="b32d0-544">Значение</span><span class="sxs-lookup"><span data-stu-id="b32d0-544">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b32d0-545">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b32d0-545">Minimum supported client</span></span><br/> | <span data-ttu-id="b32d0-546">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b32d0-546">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b32d0-547">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b32d0-547">Minimum supported server</span></span><br/> | <span data-ttu-id="b32d0-548">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b32d0-548">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b32d0-549">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b32d0-549">Namespace</span></span><br/>                | <span data-ttu-id="b32d0-550">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b32d0-550">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b32d0-551">MOF</span><span class="sxs-lookup"><span data-stu-id="b32d0-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b32d0-552"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b32d0-552"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b32d0-553">DLL</span><span class="sxs-lookup"><span data-stu-id="b32d0-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b32d0-554"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b32d0-554"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b32d0-555">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b32d0-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32d0-556">**Логический диск CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b32d0-556">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="b32d0-557">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="b32d0-557">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b32d0-558">Задачи WMI: диски и файловые системы</span><span class="sxs-lookup"><span data-stu-id="b32d0-558">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

