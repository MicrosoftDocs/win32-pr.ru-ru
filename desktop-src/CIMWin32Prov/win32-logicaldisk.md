---
description: Представляет источник данных, который разрешается в фактическое локальное запоминающее устройство в компьютерной системе под Windows.
ms.assetid: 134a90cc-b2c3-4ade-a317-b96c4aabe63d
ms.tgt_platform: multiple
title: Класс Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk
- Win32_LogicalDisk.Reset
- Win32_LogicalDisk.SetPowerState
- Win32_LogicalDisk.Access
- Win32_LogicalDisk.Availability
- Win32_LogicalDisk.BlockSize
- Win32_LogicalDisk.Caption
- Win32_LogicalDisk.Compressed
- Win32_LogicalDisk.ConfigManagerErrorCode
- Win32_LogicalDisk.ConfigManagerUserConfig
- Win32_LogicalDisk.CreationClassName
- Win32_LogicalDisk.Description
- Win32_LogicalDisk.DeviceID
- Win32_LogicalDisk.DriveType
- Win32_LogicalDisk.ErrorCleared
- Win32_LogicalDisk.ErrorDescription
- Win32_LogicalDisk.ErrorMethodology
- Win32_LogicalDisk.FileSystem
- Win32_LogicalDisk.FreeSpace
- Win32_LogicalDisk.InstallDate
- Win32_LogicalDisk.LastErrorCode
- Win32_LogicalDisk.MaximumComponentLength
- Win32_LogicalDisk.MediaType
- Win32_LogicalDisk.Name
- Win32_LogicalDisk.NumberOfBlocks
- Win32_LogicalDisk.PNPDeviceID
- Win32_LogicalDisk.PowerManagementCapabilities
- Win32_LogicalDisk.PowerManagementSupported
- Win32_LogicalDisk.ProviderName
- Win32_LogicalDisk.Purpose
- Win32_LogicalDisk.QuotasDisabled
- Win32_LogicalDisk.QuotasIncomplete
- Win32_LogicalDisk.QuotasRebuilding
- Win32_LogicalDisk.Size
- Win32_LogicalDisk.Status
- Win32_LogicalDisk.StatusInfo
- Win32_LogicalDisk.SupportsDiskQuotas
- Win32_LogicalDisk.SupportsFileBasedCompression
- Win32_LogicalDisk.SystemCreationClassName
- Win32_LogicalDisk.SystemName
- Win32_LogicalDisk.VolumeDirty
- Win32_LogicalDisk.VolumeName
- Win32_LogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad1472f14e73d06c19ccc0808794a47f7588cf9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655673"
---
# <a name="win32_logicaldisk-class"></a><span data-ttu-id="21fa9-103">\_Класс Win32 LogicalDisk</span><span class="sxs-lookup"><span data-stu-id="21fa9-103">Win32\_LogicalDisk class</span></span>

<span data-ttu-id="21fa9-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) для **Win32 \_ LogicalDisk** представляет источник данных, который разрешается в фактическое локальное запоминающее устройство в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="21fa9-104">The **Win32\_LogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a data source that resolves to an actual local storage device on a computer system running Windows.</span></span>

<span data-ttu-id="21fa9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="21fa9-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="21fa9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="21fa9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21fa9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDisk : CIM_LogicalDisk
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
  uint32   DriveType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  uint32   MediaType;
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
  string   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VolumeDirty;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="21fa9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="21fa9-108">Members</span></span>

<span data-ttu-id="21fa9-109">Класс **Win32 \_ LogicalDisk** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="21fa9-109">The **Win32\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="21fa9-110">Методы</span><span class="sxs-lookup"><span data-stu-id="21fa9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="21fa9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="21fa9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="21fa9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="21fa9-112">Methods</span></span>

<span data-ttu-id="21fa9-113">Класс **Win32 \_ LogicalDisk** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="21fa9-113">The **Win32\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="21fa9-114">Метод</span><span class="sxs-lookup"><span data-stu-id="21fa9-114">Method</span></span>                                                                             | <span data-ttu-id="21fa9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="21fa9-115">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21fa9-116">**Команду**</span><span class="sxs-lookup"><span data-stu-id="21fa9-116">**Chkdsk**</span></span>](chkdsk-method-in-class-win32-logicaldisk.md)                         | <span data-ttu-id="21fa9-117">Вызывает операцию [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) на диске.</span><span class="sxs-lookup"><span data-stu-id="21fa9-117">Invokes the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation on the disk.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="21fa9-118">**ексклудефромауточк**</span><span class="sxs-lookup"><span data-stu-id="21fa9-118">**ExcludeFromAutochk**</span></span>](excludefromautochk-method-in-class-win32-logicaldisk.md) | <span data-ttu-id="21fa9-119">Исключает диски из операции [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) для запуска при следующей перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="21fa9-119">Excludes disks from the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation to be run at the next restart.</span></span><br/>                                                                                      |
| <span data-ttu-id="21fa9-120">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="21fa9-120">**Reset**</span></span>                                                                          | <span data-ttu-id="21fa9-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="21fa9-121">Not implemented.</span></span> <span data-ttu-id="21fa9-122">Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ LogicalDisk**](cim-logicaldisk.md) для документации.</span><span class="sxs-lookup"><span data-stu-id="21fa9-122">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md) for documentation.</span></span><br/> |
| [<span data-ttu-id="21fa9-123">**счедулеауточк**</span><span class="sxs-lookup"><span data-stu-id="21fa9-123">**ScheduleAutoChk**</span></span>](scheduleautochk-method-in-class-win32-logicaldisk.md)       | <span data-ttu-id="21fa9-124">Планирует запуск [**программы chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) при следующей перезагрузке, если установлен бит "грязный".</span><span class="sxs-lookup"><span data-stu-id="21fa9-124">Schedules [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart if the dirty bit has been set.</span></span><br/>                                                                                |
| <span data-ttu-id="21fa9-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="21fa9-125">**SetPowerState**</span></span>                                                                  | <span data-ttu-id="21fa9-126">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="21fa9-126">Not implemented.</span></span> <span data-ttu-id="21fa9-127">Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-127">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="21fa9-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="21fa9-128">Properties</span></span>

<span data-ttu-id="21fa9-129">Класс **Win32 \_ LogicalDisk** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-129">The **Win32\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21fa9-130">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="21fa9-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21fa9-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-133">Тип доступного доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="21fa9-133">Type of media access available.</span></span>

<span data-ttu-id="21fa9-134">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21fa9-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="21fa9-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="21fa9-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="21fa9-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="21fa9-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="21fa9-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-138">Возможность записи</span><span class="sxs-lookup"><span data-stu-id="21fa9-138">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="21fa9-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="21fa9-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="21fa9-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="21fa9-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21fa9-141">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="21fa9-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-142">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21fa9-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="21fa9-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-145">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-145">Availability and status of the device.</span></span>

<span data-ttu-id="21fa9-146">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21fa9-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="21fa9-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21fa9-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="21fa9-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="21fa9-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="21fa9-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-150">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="21fa9-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="21fa9-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="21fa9-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="21fa9-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="21fa9-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="21fa9-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="21fa9-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="21fa9-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="21fa9-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="21fa9-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="21fa9-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-156">Автономная миграция</span><span class="sxs-lookup"><span data-stu-id="21fa9-156">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="21fa9-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="21fa9-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="21fa9-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="21fa9-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="21fa9-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="21fa9-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="21fa9-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="21fa9-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="21fa9-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="21fa9-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-162">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="21fa9-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="21fa9-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="21fa9-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-164">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="21fa9-164">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="21fa9-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="21fa9-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-166">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="21fa9-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="21fa9-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="21fa9-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="21fa9-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="21fa9-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-169">Устройство находится в состоянии предупреждения, а также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="21fa9-169">The device is in a warning state, but also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="21fa9-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="21fa9-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-171">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="21fa9-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="21fa9-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="21fa9-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-173">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="21fa9-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="21fa9-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="21fa9-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-175">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="21fa9-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="21fa9-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="21fa9-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-177">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="21fa9-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21fa9-178">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="21fa9-178">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-179">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="21fa9-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-181">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="21fa9-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-182">Размер (в байтах) блоков, образующих эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="21fa9-182">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="21fa9-183">Если значение неизвестно или если концепция блока является недопустимой (например, для агрегатных экстентов, памяти или логических дисков), введите 1.</span><span class="sxs-lookup"><span data-stu-id="21fa9-183">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter 1.</span></span>

<span data-ttu-id="21fa9-184">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="21fa9-185">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="21fa9-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-186">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="21fa9-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-189">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="21fa9-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-190">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="21fa9-190">Short description of the object a one-line string.</span></span>

<span data-ttu-id="21fa9-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-192">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="21fa9-192">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-193">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-195">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ Vol \_ \_ сжат")</span><span class="sxs-lookup"><span data-stu-id="21fa9-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-196">Если **значение — true**, логический том существует как единая сжатая сущность, например том DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="21fa9-196">If **True**, the logical volume exists as a single compressed entity, such as a DoubleSpace volume.</span></span> <span data-ttu-id="21fa9-197">Если поддерживается сжатие на основе файлов, например NTFS, это свойство имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="21fa9-197">If file based compression is supported, such as on NTFS, this property is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-198">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="21fa9-198">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-199">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21fa9-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-201">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="21fa9-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-202">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="21fa9-202">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="21fa9-203">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-203">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="21fa9-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="21fa9-205"> (0)</span><span class="sxs-lookup"><span data-stu-id="21fa9-205">(0)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-206">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="21fa9-206">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="21fa9-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="21fa9-208">(1)</span><span class="sxs-lookup"><span data-stu-id="21fa9-208">(1)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-209">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="21fa9-209">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="21fa9-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="21fa9-211">(2)</span><span class="sxs-lookup"><span data-stu-id="21fa9-211">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="21fa9-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="21fa9-213">(3)</span><span class="sxs-lookup"><span data-stu-id="21fa9-213">(3)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-214">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="21fa9-214">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="21fa9-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="21fa9-216">(4)</span><span class="sxs-lookup"><span data-stu-id="21fa9-216">(4)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-217">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="21fa9-217">Device is not working properly.</span></span> <span data-ttu-id="21fa9-218">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="21fa9-218">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="21fa9-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="21fa9-220">(5)</span><span class="sxs-lookup"><span data-stu-id="21fa9-220">(5)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-221">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="21fa9-221">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="21fa9-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="21fa9-223"> (6)</span><span class="sxs-lookup"><span data-stu-id="21fa9-223">(6)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-224">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="21fa9-224">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="21fa9-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="21fa9-226">(7)</span><span class="sxs-lookup"><span data-stu-id="21fa9-226">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="21fa9-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="21fa9-228">(8)</span><span class="sxs-lookup"><span data-stu-id="21fa9-228">(8)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-229">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-229">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="21fa9-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="21fa9-231">(9)</span><span class="sxs-lookup"><span data-stu-id="21fa9-231">(9)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-232">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="21fa9-232">Device is not working properly.</span></span> <span data-ttu-id="21fa9-233">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-233">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="21fa9-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="21fa9-235">(10)</span><span class="sxs-lookup"><span data-stu-id="21fa9-235">(10)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-236">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="21fa9-236">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="21fa9-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="21fa9-238">(11)</span><span class="sxs-lookup"><span data-stu-id="21fa9-238">(11)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-239">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-239">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="21fa9-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="21fa9-241">(12)</span><span class="sxs-lookup"><span data-stu-id="21fa9-241">(12)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-242">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="21fa9-242">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="21fa9-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="21fa9-244">(13)</span><span class="sxs-lookup"><span data-stu-id="21fa9-244">(13)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-245">Windows не удается проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-245">Windows cannot verify the device resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="21fa9-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="21fa9-247">(14)</span><span class="sxs-lookup"><span data-stu-id="21fa9-247">(14)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-248">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="21fa9-248">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="21fa9-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="21fa9-250">(15)</span><span class="sxs-lookup"><span data-stu-id="21fa9-250">(15)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-251">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="21fa9-251">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="21fa9-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="21fa9-253">(16)</span><span class="sxs-lookup"><span data-stu-id="21fa9-253">(16)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-254">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="21fa9-254">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="21fa9-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="21fa9-256">(17)</span><span class="sxs-lookup"><span data-stu-id="21fa9-256">(17)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-257">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="21fa9-257">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="21fa9-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="21fa9-259">(18)</span><span class="sxs-lookup"><span data-stu-id="21fa9-259">(18)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-260">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="21fa9-260">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="21fa9-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="21fa9-262">(19)</span><span class="sxs-lookup"><span data-stu-id="21fa9-262">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="21fa9-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="21fa9-264">(20)</span><span class="sxs-lookup"><span data-stu-id="21fa9-264">(20)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-265">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="21fa9-265">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="21fa9-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="21fa9-267">(21)</span><span class="sxs-lookup"><span data-stu-id="21fa9-267">(21)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-268">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="21fa9-268">System failure.</span></span> <span data-ttu-id="21fa9-269">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="21fa9-269">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="21fa9-270">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="21fa9-270">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="21fa9-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="21fa9-272">(22)</span><span class="sxs-lookup"><span data-stu-id="21fa9-272">(22)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-273">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="21fa9-273">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="21fa9-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="21fa9-275">(23)</span><span class="sxs-lookup"><span data-stu-id="21fa9-275">(23)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-276">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="21fa9-276">System failure.</span></span> <span data-ttu-id="21fa9-277">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="21fa9-277">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="21fa9-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="21fa9-279">(24)</span><span class="sxs-lookup"><span data-stu-id="21fa9-279">(24)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-280">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="21fa9-280">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="21fa9-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="21fa9-282">(25)</span><span class="sxs-lookup"><span data-stu-id="21fa9-282">(25)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-283">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="21fa9-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="21fa9-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="21fa9-285">(26)</span><span class="sxs-lookup"><span data-stu-id="21fa9-285">(26)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-286">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="21fa9-286">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="21fa9-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="21fa9-288">(27)</span><span class="sxs-lookup"><span data-stu-id="21fa9-288">(27)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-289">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="21fa9-289">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="21fa9-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="21fa9-291">(28)</span><span class="sxs-lookup"><span data-stu-id="21fa9-291">(28)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-292">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="21fa9-292">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="21fa9-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="21fa9-294">(29)</span><span class="sxs-lookup"><span data-stu-id="21fa9-294">(29)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-295">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="21fa9-295">Device is disabled.</span></span> <span data-ttu-id="21fa9-296">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="21fa9-296">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="21fa9-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="21fa9-298">(30)</span><span class="sxs-lookup"><span data-stu-id="21fa9-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-299">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="21fa9-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="21fa9-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="21fa9-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="21fa9-301">1-31</span><span class="sxs-lookup"><span data-stu-id="21fa9-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-302">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="21fa9-302">Device is not working properly.</span></span> <span data-ttu-id="21fa9-303">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="21fa9-303">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21fa9-304">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="21fa9-304">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-305">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-307">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="21fa9-307">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-308">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="21fa9-308">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="21fa9-309">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-310">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="21fa9-310">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-311">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-313">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="21fa9-313">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-314">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="21fa9-314">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="21fa9-315">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="21fa9-315">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="21fa9-316">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-317">**Описание**</span><span class="sxs-lookup"><span data-stu-id="21fa9-317">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-318">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-320">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="21fa9-320">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-321">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="21fa9-321">Description of the object.</span></span>

<span data-ttu-id="21fa9-322">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-323">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="21fa9-323">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-326">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="21fa9-326">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-327">Уникальный идентификатор логического диска от других устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="21fa9-327">Unique identifier of the logical disk from other devices on the system.</span></span>

<span data-ttu-id="21fa9-328">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="21fa9-329">Пример кода, который извлекает это свойство, см. в разделе "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="21fa9-329">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-330">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="21fa9-330">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-331">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21fa9-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-333">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| филефунктионс \| жетдриветипе")</span><span class="sxs-lookup"><span data-stu-id="21fa9-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|FileFunctions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-334">Числовое значение, соответствующее типу дискового накопителя, представляемого этим логическим диском.</span><span class="sxs-lookup"><span data-stu-id="21fa9-334">Numeric value that corresponds to the type of disk drive this logical disk represents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21fa9-335">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="21fa9-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Root_Directory"></span><span id="no_root_directory"></span><span id="NO_ROOT_DIRECTORY"></span>

<span data-ttu-id="21fa9-336">**Нет корневого каталога** (1)</span><span class="sxs-lookup"><span data-stu-id="21fa9-336">**No Root Directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Disk"></span><span id="removable_disk"></span><span id="REMOVABLE_DISK"></span>

<span data-ttu-id="21fa9-337">**Съемный диск** (2)</span><span class="sxs-lookup"><span data-stu-id="21fa9-337">**Removable Disk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Disk"></span><span id="local_disk"></span><span id="LOCAL_DISK"></span>

<span data-ttu-id="21fa9-338">**Локальный диск** (3)</span><span class="sxs-lookup"><span data-stu-id="21fa9-338">**Local Disk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Drive"></span><span id="network_drive"></span><span id="NETWORK_DRIVE"></span>

<span data-ttu-id="21fa9-339">**Сетевой диск** (4)</span><span class="sxs-lookup"><span data-stu-id="21fa9-339">**Network Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Compact_Disc"></span><span id="compact_disc"></span><span id="COMPACT_DISC"></span>

<span data-ttu-id="21fa9-340">**Компакт-диск** (5)</span><span class="sxs-lookup"><span data-stu-id="21fa9-340">**Compact Disc** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM_Disk"></span><span id="ram_disk"></span><span id="RAM_DISK"></span>

<span data-ttu-id="21fa9-341">**Электронный диск** (6)</span><span class="sxs-lookup"><span data-stu-id="21fa9-341">**RAM Disk** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21fa9-342">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="21fa9-342">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-343">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-345">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="21fa9-345">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="21fa9-346">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-347">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="21fa9-347">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-348">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-350">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="21fa9-350">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="21fa9-351">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-352">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="21fa9-352">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-355">Тип обнаружения и исправления ошибок, поддерживаемый этой областью хранения.</span><span class="sxs-lookup"><span data-stu-id="21fa9-355">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="21fa9-356">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-356">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-357">**Системой**</span><span class="sxs-lookup"><span data-stu-id="21fa9-357">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-360">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="21fa9-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-361">Файловая система на логическом диске.</span><span class="sxs-lookup"><span data-stu-id="21fa9-361">File system on the logical disk.</span></span>

<span data-ttu-id="21fa9-362">Пример: "NTFS"</span><span class="sxs-lookup"><span data-stu-id="21fa9-362">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-363">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="21fa9-363">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-364">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="21fa9-364">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-366">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="21fa9-366">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-367">Пространство в байтах, доступное на логическом диске.</span><span class="sxs-lookup"><span data-stu-id="21fa9-367">Space, in bytes, available on the logical disk.</span></span>

<span data-ttu-id="21fa9-368">Это свойство наследуется от [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-368">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="21fa9-369">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="21fa9-369">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="21fa9-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-371">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="21fa9-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-373">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="21fa9-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-374">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="21fa9-374">Date and time the object was installed.</span></span> <span data-ttu-id="21fa9-375">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="21fa9-375">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="21fa9-376">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-377">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="21fa9-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-378">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21fa9-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-379">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-380">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="21fa9-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="21fa9-381">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-382">**максимумкомпонентленгс**</span><span class="sxs-lookup"><span data-stu-id="21fa9-382">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-383">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21fa9-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-385">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="21fa9-385">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-386">Максимальная длина компонента имени файла, поддерживаемого диском Windows.</span><span class="sxs-lookup"><span data-stu-id="21fa9-386">Maximum length of a filename component supported by the Windows drive.</span></span> <span data-ttu-id="21fa9-387">Компонент filename — это часть имени файла между символами обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="21fa9-387">A filename component is that portion of a filename between backslashes.</span></span> <span data-ttu-id="21fa9-388">Значение можно использовать, чтобы указать, что в указанной файловой системе поддерживаются длинные имена.</span><span class="sxs-lookup"><span data-stu-id="21fa9-388">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="21fa9-389">Например, для файловой системы FAT, поддерживающей длинные имена, функция сохраняет значение 255, а не предыдущий индикатор 8,3.</span><span class="sxs-lookup"><span data-stu-id="21fa9-389">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="21fa9-390">Длинные имена также могут поддерживаться в системах, использующих файловую систему NTFS.</span><span class="sxs-lookup"><span data-stu-id="21fa9-390">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="21fa9-391">Пример: 255</span><span class="sxs-lookup"><span data-stu-id="21fa9-391">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-392">**Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="21fa9-392">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-393">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21fa9-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-395">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| входные и выходные функции устройства Win32API \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="21fa9-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-396">Тип носителя, который в настоящее время имеется на логическом диске.</span><span class="sxs-lookup"><span data-stu-id="21fa9-396">Type of media currently present in the logical drive.</span></span> <span data-ttu-id="21fa9-397">Это значение будет одним из значений \_ перечисления типа мультимедиа, определенного в виниоктл. h.</span><span class="sxs-lookup"><span data-stu-id="21fa9-397">This value will be one of the values of the MEDIA\_TYPE enumeration defined in Winioctl.h.</span></span> <span data-ttu-id="21fa9-398">Значение может быть точным для съемных дисков, если в настоящее время нет носителя.</span><span class="sxs-lookup"><span data-stu-id="21fa9-398">The value may not be exact for removable drives if currently there is no media in the drive.</span></span>

<dt>

<span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>

<span data-ttu-id="21fa9-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**Формат неизвестен** (0)</span><span class="sxs-lookup"><span data-stu-id="21fa9-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**Format is unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-дюймовый гибкий диск** (1)</span><span class="sxs-lookup"><span data-stu-id="21fa9-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (1)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-401">5 1/4-дюймовый гибкий диск — 1,2 МБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-401">5 1/4-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (2)</span><span class="sxs-lookup"><span data-stu-id="21fa9-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (2)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-403">3 1/2-дюймовый гибкий диск — 1,44 МБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-403">3 1/2-Inch Floppy Disk - 1.44 MB -512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (3)</span><span class="sxs-lookup"><span data-stu-id="21fa9-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (3)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-405">3 1/2-дюймовый гибкий диск — 2,88 МБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-405">3 1/2-Inch Floppy Disk - 2.88 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (4)</span><span class="sxs-lookup"><span data-stu-id="21fa9-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-407">3 1/2-дюймовый гибкий диск — 20,8 МБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-407">3 1/2-Inch Floppy Disk - 20.8 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (5)</span><span class="sxs-lookup"><span data-stu-id="21fa9-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (5)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-409">3 1/2-дюймовый гибкий диск — 720 КБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-409">3 1/2-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-дюймовый гибкий диск** (6)</span><span class="sxs-lookup"><span data-stu-id="21fa9-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (6)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-411">5 1/4-дюймовый гибкий диск — 360 КБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-411">5 1/4-Inch Floppy Disk - 360 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-дюймовый гибкий диск** (7)</span><span class="sxs-lookup"><span data-stu-id="21fa9-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (7)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-413">5 1/4-дюймовый гибкий диск — 320 КБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-413">5 1/4-Inch Floppy Disk - 320 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-дюймовый гибкий диск** (8)</span><span class="sxs-lookup"><span data-stu-id="21fa9-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (8)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-415">5 1/4-дюймовый гибкий диск — 320 КБ — 1024 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-415">5 1/4-Inch Floppy Disk - 320 KB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-дюймовый гибкий диск** (9)</span><span class="sxs-lookup"><span data-stu-id="21fa9-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (9)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-417">5 1/4-дюймовый гибкий диск — 180 КБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-417">5 1/4-Inch Floppy Disk - 180 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-дюймовый гибкий диск** (10)</span><span class="sxs-lookup"><span data-stu-id="21fa9-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (10)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-419">5 1/4-дюймовый гибкий диск — 160 КБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-419">5 1/4-Inch Floppy Disk - 160 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>

<span data-ttu-id="21fa9-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Съемный носитель (не дискета** ) (11)</span><span class="sxs-lookup"><span data-stu-id="21fa9-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Removable media other than floppy** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>

<span data-ttu-id="21fa9-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Фиксированный жесткий диск** (12)</span><span class="sxs-lookup"><span data-stu-id="21fa9-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Fixed hard disk media** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (13)</span><span class="sxs-lookup"><span data-stu-id="21fa9-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (13)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-423">3 1/2-дюймовый гибкий диск — 120 МБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-423">3 1/2-Inch Floppy Disk - 120 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (14)</span><span class="sxs-lookup"><span data-stu-id="21fa9-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (14)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-425">3 1/2-дюймовый гибкий диск — 640 КБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-425">3 1/2-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-дюймовый гибкий диск** (15)</span><span class="sxs-lookup"><span data-stu-id="21fa9-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (15)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-427">5 1/4-дюймовый гибкий диск — 640 КБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-427">5 1/4-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-дюймовый гибкий диск** (16)</span><span class="sxs-lookup"><span data-stu-id="21fa9-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (16)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-429">5 1/4-дюймовый гибкий диск — 720 КБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-429">5 1/4-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (17)</span><span class="sxs-lookup"><span data-stu-id="21fa9-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (17)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-431">3 1/2-дюймовый гибкий диск — 1,2 МБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-431">3 1/2-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (18)</span><span class="sxs-lookup"><span data-stu-id="21fa9-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (18)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-433">3 1/2-дюймовый гибкий диск — 1,23 МБ — 1024 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-433">3 1/2-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5-дюймовый гибкий диск** (19)</span><span class="sxs-lookup"><span data-stu-id="21fa9-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (19)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-435">5 1/4-дюймовый гибкий диск — 1,23 МБ — 1024 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-435">5 1/4-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (20)</span><span class="sxs-lookup"><span data-stu-id="21fa9-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (20)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-437">3 1/2-дюймовый гибкий диск — 128 МБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-437">3 1/2-Inch Floppy Disk - 128 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3-дюймовый гибкий диск** (21)</span><span class="sxs-lookup"><span data-stu-id="21fa9-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (21)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-439">3 1/2-дюймовый гибкий диск — 230 МБ — 512 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-439">3 1/2-Inch Floppy Disk - 230 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="21fa9-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8-дюймовый гибкий диск** (22)</span><span class="sxs-lookup"><span data-stu-id="21fa9-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8-Inch Floppy Disk** (22)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-441">8-дюймовый гибкий диск — 256 КБ — 128 байт/сектор</span><span class="sxs-lookup"><span data-stu-id="21fa9-441">8-Inch Floppy Disk - 256 KB - 128 bytes/sector</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21fa9-442">**Name**</span><span class="sxs-lookup"><span data-stu-id="21fa9-442">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-443">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-445">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="21fa9-445">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-446">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="21fa9-446">Label by which the object is known.</span></span> <span data-ttu-id="21fa9-447">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="21fa9-447">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="21fa9-448">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-448">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-449">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="21fa9-449">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-450">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="21fa9-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-452">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="21fa9-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-453">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="21fa9-453">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="21fa9-454">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-454">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="21fa9-455">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="21fa9-455">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="21fa9-456">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-456">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="21fa9-457">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="21fa9-457">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-458">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="21fa9-458">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-459">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-461">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="21fa9-461">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-462">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-462">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="21fa9-463">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="21fa9-464">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="21fa9-464">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-465">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="21fa9-465">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-466">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="21fa9-466">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-467">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-468">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="21fa9-468">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="21fa9-469">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-469">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21fa9-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="21fa9-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="21fa9-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="21fa9-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="21fa9-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="21fa9-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="21fa9-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="21fa9-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-474">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="21fa9-474">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="21fa9-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="21fa9-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-476">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="21fa9-476">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="21fa9-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="21fa9-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-478">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="21fa9-478">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="21fa9-479">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="21fa9-479">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="21fa9-480">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="21fa9-480">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="21fa9-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="21fa9-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-482">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="21fa9-482">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="21fa9-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="21fa9-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="21fa9-484">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="21fa9-484">Timed Power-On Supported</span></span>

<span data-ttu-id="21fa9-485">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="21fa9-485">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21fa9-486">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="21fa9-486">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-487">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-487">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-488">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-489">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="21fa9-489">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="21fa9-490">Это свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="21fa9-490">This property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="21fa9-491">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-492">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="21fa9-492">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-493">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-494">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-495">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| сетевые функции Windows \| внетжетконнектион")</span><span class="sxs-lookup"><span data-stu-id="21fa9-495">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-496">Сетевой путь к логическому устройству.</span><span class="sxs-lookup"><span data-stu-id="21fa9-496">Network path to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-497">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="21fa9-497">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-498">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-499">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-500">Произвольная строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="21fa9-500">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="21fa9-501">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-501">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-502">**куотасдисаблед**</span><span class="sxs-lookup"><span data-stu-id="21fa9-502">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-503">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-504">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-505">Указывает, что Управление квотами не включено (TRUE) в этой системе.</span><span class="sxs-lookup"><span data-stu-id="21fa9-505">Indicates that quota management is not enabled (TRUE) on this system.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-506">**куотасинкомплете**</span><span class="sxs-lookup"><span data-stu-id="21fa9-506">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-507">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-507">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-508">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-509">Указывает, что Управление квотами использовалось, но было отключено (**true**).</span><span class="sxs-lookup"><span data-stu-id="21fa9-509">Indicates that the quota management was used but has been disabled (**True**).</span></span> <span data-ttu-id="21fa9-510">Незавершенные ссылается на сведения, оставшиеся в файловой системе после отключения управления квотами.</span><span class="sxs-lookup"><span data-stu-id="21fa9-510">Incomplete refers to the information left in the file system after quota management was disabled.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-511">**куотасребуилдинг**</span><span class="sxs-lookup"><span data-stu-id="21fa9-511">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-512">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-512">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-513">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-514">Если **значение — true**, то указывает, что файловая система находится в активном процессе компиляции данных и настройки дискового пространства для управления квотами.</span><span class="sxs-lookup"><span data-stu-id="21fa9-514">If **True**, indicates that the file system is in the active process of compiling information and setting the disk up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-515">**Размер**</span><span class="sxs-lookup"><span data-stu-id="21fa9-515">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-516">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-517">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-518">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="21fa9-518">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-519">Размер диска.</span><span class="sxs-lookup"><span data-stu-id="21fa9-519">Size of the disk drive.</span></span>

<span data-ttu-id="21fa9-520">Это свойство наследуется от [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-520">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="21fa9-521">Пример кода, который извлекает это свойство, см. в разделе "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="21fa9-521">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-522">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="21fa9-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-523">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-525">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="21fa9-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-526">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="21fa9-526">Current status of the object.</span></span> <span data-ttu-id="21fa9-527">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="21fa9-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="21fa9-528">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="21fa9-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="21fa9-529">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="21fa9-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="21fa9-530">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="21fa9-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="21fa9-531">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="21fa9-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="21fa9-532">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="21fa9-533">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="21fa9-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="21fa9-534">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="21fa9-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="21fa9-535">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="21fa9-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="21fa9-536">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="21fa9-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21fa9-537">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="21fa9-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="21fa9-538">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="21fa9-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="21fa9-539">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="21fa9-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="21fa9-540">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="21fa9-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="21fa9-541">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="21fa9-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="21fa9-542">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="21fa9-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="21fa9-543">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="21fa9-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="21fa9-544">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="21fa9-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="21fa9-545">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="21fa9-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21fa9-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="21fa9-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-547">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21fa9-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-548">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-549">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="21fa9-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-550">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-550">State of the logical device.</span></span> <span data-ttu-id="21fa9-551">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="21fa9-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="21fa9-552">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21fa9-553">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="21fa9-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21fa9-554">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="21fa9-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="21fa9-555">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="21fa9-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="21fa9-556">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="21fa9-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="21fa9-557">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="21fa9-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21fa9-558">**суппортсдисккуотас**</span><span class="sxs-lookup"><span data-stu-id="21fa9-558">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-559">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-559">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-560">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-560">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-561">Если **значение — true**, этот том поддерживает дисковые квоты.</span><span class="sxs-lookup"><span data-stu-id="21fa9-561">If **True**, this volume supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-562">**суппортсфилебаседкомпрессион**</span><span class="sxs-lookup"><span data-stu-id="21fa9-562">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-563">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-564">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-565">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System functions \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ File \_ Compression")</span><span class="sxs-lookup"><span data-stu-id="21fa9-565">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-566">Если **значение — true**, раздел логического диска поддерживает сжатие на основе файлов, как в случае с файловой системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="21fa9-566">If **True**, the logical disk partition supports file-based compression, such as is the case with the NTFS file system.</span></span> <span data-ttu-id="21fa9-567">Это свойство имеет **значение false** , если **сжатое** свойство имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="21fa9-567">This property is **False** when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-568">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="21fa9-568">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-569">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-569">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-570">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-570">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-571">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="21fa9-571">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-572">Значение **Свойства "** область видимости компьютера".</span><span class="sxs-lookup"><span data-stu-id="21fa9-572">Value of the scoping computer **CreationClassName** property.</span></span>

<span data-ttu-id="21fa9-573">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-574">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="21fa9-574">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-575">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-575">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-576">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-577">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="21fa9-577">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-578">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="21fa9-578">Name of the scoping system.</span></span>

<span data-ttu-id="21fa9-579">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="21fa9-579">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-580">**волумедирти**</span><span class="sxs-lookup"><span data-stu-id="21fa9-580">**VolumeDirty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-581">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21fa9-581">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-582">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-582">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-583">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("фсктл \_ является \_ томом \_ грязным")</span><span class="sxs-lookup"><span data-stu-id="21fa9-583">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL\_IS\_VOLUME\_DIRTY")</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-584">Если **значение — true**, диск требует запуска [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) при следующей перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="21fa9-584">If **True**, the disk requires [**ChkDsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart.</span></span> <span data-ttu-id="21fa9-585">Это свойство применимо только к тем экземплярам логического диска, которые представляют физический диск на компьютере.</span><span class="sxs-lookup"><span data-stu-id="21fa9-585">This property is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="21fa9-586">Он неприменим к сопоставленным логическим дискам.</span><span class="sxs-lookup"><span data-stu-id="21fa9-586">It is not applicable to mapped logical drives.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-587">**Тома**</span><span class="sxs-lookup"><span data-stu-id="21fa9-587">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-588">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-589">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="21fa9-589">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-590">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="21fa9-590">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-591">Имя тома логического диска.</span><span class="sxs-lookup"><span data-stu-id="21fa9-591">Volume name of the logical disk.</span></span>

<span data-ttu-id="21fa9-592">Ограничения: не более 32 символов.</span><span class="sxs-lookup"><span data-stu-id="21fa9-592">Constraints: Maximum 32 characters.</span></span>

<span data-ttu-id="21fa9-593">Пример кода, который извлекает это свойство, см. в разделе "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="21fa9-593">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="21fa9-594">**волумесериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="21fa9-594">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21fa9-595">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21fa9-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-596">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21fa9-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21fa9-597">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции файловой системы Win32API [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="21fa9-597">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="21fa9-598">Серийный номер тома логического диска.</span><span class="sxs-lookup"><span data-stu-id="21fa9-598">Volume serial number of the logical disk.</span></span>

<span data-ttu-id="21fa9-599">Ограничения: не более 11 символов.</span><span class="sxs-lookup"><span data-stu-id="21fa9-599">Constraints: Maximum 11 characters.</span></span>

<span data-ttu-id="21fa9-600">Пример: "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="21fa9-600">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21fa9-601">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21fa9-601">Remarks</span></span>

<span data-ttu-id="21fa9-602">Класс **Win32 \_ LogicalDisk** является производным от [**CIM \_ LogicalDisk**](cim-logicaldisk.md) , который является производным от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="21fa9-602">The **Win32\_LogicalDisk** class is derived from [**CIM\_LogicalDisk**](cim-logicaldisk.md) which derives from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="21fa9-603">Класс **CIM \_ сторажеекстент** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="21fa9-603">The **CIM\_StorageExtent** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="21fa9-604">Физический диск является основой любой системы управления хранением.</span><span class="sxs-lookup"><span data-stu-id="21fa9-604">A physical disk drive is the cornerstone of any storage management system.</span></span> <span data-ttu-id="21fa9-605">Однако после установки физического диска ни пользователи, ни системные администраторы не работают непосредственно с оборудованием.</span><span class="sxs-lookup"><span data-stu-id="21fa9-605">However, after a physical disk drive has been installed, neither users nor system administrators typically deal with the hardware directly.</span></span> <span data-ttu-id="21fa9-606">Вместо этого, как пользователи, так и системные администраторы взаимодействуют с логическими дисками, созданными на диске.</span><span class="sxs-lookup"><span data-stu-id="21fa9-606">Instead, both users and system administrators interact with the logical drives that have been created on the disk.</span></span>

<span data-ttu-id="21fa9-607">Логический диск — это подразделение раздела, которому назначена собственная буква диска.</span><span class="sxs-lookup"><span data-stu-id="21fa9-607">A logical drive is a subdivision of a partition that has been assigned its own drive letter.</span></span> <span data-ttu-id="21fa9-608">(Возможно, имеется раздел, которому не назначена буква диска.) Когда вы говорите о диске C или диск D, вы ссылаетесь на логический диск, а не на физический диск.</span><span class="sxs-lookup"><span data-stu-id="21fa9-608">(It is possible to have a partition that has not been assigned a drive letter.) When you talk about drive C or drive D, you are referring to a logical drive rather than to a physical disk drive.</span></span> <span data-ttu-id="21fa9-609">Аналогично, при сохранении документа на диске E он сохраняется на логическом диске.</span><span class="sxs-lookup"><span data-stu-id="21fa9-609">Likewise, when you save a document to drive E, you are saving it to the logical drive.</span></span> <span data-ttu-id="21fa9-610">Физические диски составляют оборудование, которое образует диск, включая такие компоненты, как головные, секторы и цилиндры.</span><span class="sxs-lookup"><span data-stu-id="21fa9-610">Physical disks compose the hardware that makes up a drive, including such components as heads, sectors, and cylinders.</span></span> <span data-ttu-id="21fa9-611">Логические диски, напротив, имеют такие свойства, как место на диске, доступное место на диске и буквы дисков.</span><span class="sxs-lookup"><span data-stu-id="21fa9-611">Logical drives, by contrast, have properties such as disk space, available disk space, and drive letters.</span></span>

> [!Note]  
> <span data-ttu-id="21fa9-612">Класс **Win32 \_ LogicalDisk** можно использовать только для перечисления свойств локальных дисков.</span><span class="sxs-lookup"><span data-stu-id="21fa9-612">The **Win32\_LogicalDisk** class can be used only to enumerate the properties of local disk drives.</span></span> <span data-ttu-id="21fa9-613">Однако можно использовать класс [**Win32 \_ маппедлогикалдиск**](win32-mappedlogicaldisk.md) для перечисления свойств сопоставленных сетевых дисков.</span><span class="sxs-lookup"><span data-stu-id="21fa9-613">However, you can use the [**Win32\_MappedLogicalDisk**](win32-mappedlogicaldisk.md) class to enumerate the properties of mapped network drives.</span></span>

 

## <a name="examples"></a><span data-ttu-id="21fa9-614">Примеры</span><span class="sxs-lookup"><span data-stu-id="21fa9-614">Examples</span></span>

<span data-ttu-id="21fa9-615">Другие примеры можно найти с помощью **Win32 \_ LogicalDisk** для получения данных о диске или томе в разделе [задачи WMI: диски и файловые системы](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) .</span><span class="sxs-lookup"><span data-stu-id="21fa9-615">You can find other examples using **Win32\_LogicalDisk** to obtain disk or volume data in the [WMI Tasks: Disks and File Systems](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) topic.</span></span>

<span data-ttu-id="21fa9-616">Пример кода VBScript для средства [извлечения информации WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) в коллекции TechNet использует класс **Win32 \_ LogicalDisk** для получения сведений об оборудовании с нескольких удаленных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="21fa9-616">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_LogicalDisk** class to retrieve hardware information from a number of remote computers.</span></span>

<span data-ttu-id="21fa9-617">[Сведения о получении диска с помощью WMI/CIM...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) Пример кода PowerShell в коллекции TechNet использует **Win32 \_ LogicalDisk** для извлечения **DeviceID**, **тома** и **размера** с целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="21fa9-617">The [Get Disk info using wmi/cim...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) PowerShell code example on the TechNet Gallery uses **Win32\_LogicalDisk** to retrieve **DeviceID**, **VolumeName**, and **Size** from a target device.</span></span> <span data-ttu-id="21fa9-618">В частности, этот пример включает в себя строгую обработку исключений и возвращает один объект на компьютер, а не на диск.</span><span class="sxs-lookup"><span data-stu-id="21fa9-618">In particular, this sample includes rigorous exception handling, and returns a single object per computer, rather than per disk.</span></span>

<span data-ttu-id="21fa9-619">Сценарии предприятия часто используют настройку оборудования и программного обеспечения на удаленных компьютерах. в свою очередь, для этого необходимо заранее выяснить тип дисков, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="21fa9-619">Enterprise scripting often involves configuring hardware and software on remote computers; in turn, this requires you to know, in advance, the type of disk drives installed on a computer.</span></span> <span data-ttu-id="21fa9-620">Например, сценарий, устанавливающий приложение на диске E, работает только в том случае, если диск E является жестким диском.</span><span class="sxs-lookup"><span data-stu-id="21fa9-620">For example, a script that installs an application on drive E works only if drive E is a hard disk.</span></span> <span data-ttu-id="21fa9-621">Если диск E представляет собой дискету или дисковод компакт-дисков, сценарий завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="21fa9-621">If drive E happens to represent a floppy disk or a CD-ROM drive, the script fails.</span></span> <span data-ttu-id="21fa9-622">Следующий код определяет диски и типы дисков, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="21fa9-622">The following code identifies the drives and drive types installed on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk")
For Each objDisk in colDisks
 Wscript.Echo "DeviceID: "& objDisk.DeviceID 
 Select Case objDisk.DriveType
 Case 1
 Wscript.Echo "No root directory."
 Case 2
 Wscript.Echo "DriveType: Removable drive."
 Case 3
 Wscript.Echo "DriveType: Local hard disk."
 Case 4
 Wscript.Echo "DriveType: Network disk." 
 Case 5
 Wscript.Echo "DriveType: Compact disk." 
 Case 6
 Wscript.Echo "DriveType: RAM disk." 
 Case Else
 Wscript.Echo "Drive type could not be determined."
 End Select
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...
{
   string strComputer = &quot;.&quot;;
            
   ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
   ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk&quot;);
   ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
   ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

   foreach (ManagementObject objDisk in colDisks)
   {
      Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
                
      switch ((uint)(objDisk[&quot;DriveType&quot;]))
      {
         case 1: {   Console.WriteLine(&quot;No root directory.&quot;);
                     break;}
         case 2: {   Console.WriteLine(&quot;DriveType: Removable drive.&quot;); 
                     break;}
         case 3: {   Console.WriteLine(&quot;DriveType: Local hard disk.&quot;);
                     break;}
         case 4: {   Console.WriteLine(&quot;DriveType: Network disk.&quot;);
                     break;}
         case 5: {   Console.WriteLine(&quot;DriveType: Compact disk.&quot;);
                     break;}
         case 6: {   Console.WriteLine(&quot;DriveType: RAM disk.&quot;);
                     break;}
         default: {  Console.WriteLine(&quot;Drive type could not be determined.&quot;);
                     break;}
      }
      //Readline is in here so the user can see the result before the code exists
      Console.ReadLine();
   }
}
```





<span data-ttu-id="21fa9-623">В следующих примерах перечисляются объемы свободного места на всех жестких дисках компьютера.</span><span class="sxs-lookup"><span data-stu-id="21fa9-623">The following samples enumerate the free space on all the hard disk drives on a computer.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk WHERE DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
 Wscript.Echo "Device ID: " & objDisk.DeviceID 
 Wscript.Echo "Free Disk Space: " & objDisk.FreeSpace
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...

const int HARD_DISK = 3;
string strComputer = &quot;.&quot;;

ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk WHERE DriveType = &quot; + HARD_DISK + &quot;&quot;);
ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

foreach (ManagementObject objDisk in colDisks)
{
    Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
    Console.WriteLine(&quot;Free Disk Space : {0}&quot;, objDisk[&quot;FreeSpace&quot;]);
    Console.ReadLine();
}
```





<span data-ttu-id="21fa9-624">В следующем примере кода возвращается тип файловой системы (FAT, NTFS, FAT32 и т. д.), используемой на каждом диске компьютера.</span><span class="sxs-lookup"><span data-stu-id="21fa9-624">The following code example returns the type of file system (FAT, NTFS, FAT32, and so on) used on each drive in a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
    Wscript.Echo "DeviceID: "& vbTab &  objDisk.DeviceID  
    Wscript.Echo "File System: "& vbTab & objDisk.FileSystem
Next
```


```PowerShell

Get-WMIObject Win32_LogicalDisk | Select DeviceID, FileSystem | Format=Table -AutoSize
```





<span data-ttu-id="21fa9-625">Следующий пример кода PowerShell извлекает дополнительные сведения о логических локальных дисках.</span><span class="sxs-lookup"><span data-stu-id="21fa9-625">The following PowerShell code sample retrieves additional information about the logical local disks.</span></span>


```PowerShell
Write-Host "Drive information for $env:ComputerName"

Get-WmiObject -Class Win32_LogicalDisk |
    Where-Object {$_.DriveType -ne 5} |
    Sort-Object -Property Name | 
    Select-Object Name, VolumeName, FileSystem, Description, VolumeDirty, `
        @{"Label"="DiskSize(GB)";"Expression"={"{0:N}" -f ($_.Size/1GB) -as [float]}}, `
        @{"Label"="FreeSpace(GB)";"Expression"={"{0:N}" -f ($_.FreeSpace/1GB) -as [float]}}, `
        @{"Label"="%Free";"Expression"={"{0:N}" -f ($_.FreeSpace/$_.Size*100) -as [float]}} |
    Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="21fa9-626">Требования</span><span class="sxs-lookup"><span data-stu-id="21fa9-626">Requirements</span></span>



| <span data-ttu-id="21fa9-627">Требование</span><span class="sxs-lookup"><span data-stu-id="21fa9-627">Requirement</span></span> | <span data-ttu-id="21fa9-628">Значение</span><span class="sxs-lookup"><span data-stu-id="21fa9-628">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21fa9-629">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21fa9-629">Minimum supported client</span></span><br/> | <span data-ttu-id="21fa9-630">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21fa9-630">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21fa9-631">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21fa9-631">Minimum supported server</span></span><br/> | <span data-ttu-id="21fa9-632">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21fa9-632">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21fa9-633">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="21fa9-633">Namespace</span></span><br/>                | <span data-ttu-id="21fa9-634">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="21fa9-634">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21fa9-635">MOF</span><span class="sxs-lookup"><span data-stu-id="21fa9-635">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21fa9-636"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21fa9-636"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21fa9-637">DLL</span><span class="sxs-lookup"><span data-stu-id="21fa9-637">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21fa9-638"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21fa9-638"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21fa9-639">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21fa9-639">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21fa9-640">**Логический диск CIM \_**</span><span class="sxs-lookup"><span data-stu-id="21fa9-640">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="21fa9-641">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="21fa9-641">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="21fa9-642">Задачи WMI: диски и файловые системы</span><span class="sxs-lookup"><span data-stu-id="21fa9-642">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

