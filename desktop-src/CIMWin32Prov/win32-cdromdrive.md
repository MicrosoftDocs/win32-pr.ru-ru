---
description: Представляет устройство чтения компакт-дисков в компьютерной системе, на которой работает Windows.
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
ms.openlocfilehash: 1148cffe4e6a13aac1b873a95cd57233ae65addeb5aca15dfe8ccdab834d730c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118418255"
---
# <a name="win32_cdromdrive-class"></a>\_Класс Win32 кдромдриве

Класс **WMI \_ кдромдриве** [инструментария](/windows/desktop/WmiSdk/retrieving-a-class) Win32 представляет устройство чтения компакт-дисков в компьютерной системе, на которой работает Windows.

> [!Note]  
> Имейте в виду, что имя диска не соответствует назначенному устройству букве логического диска.

 

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **Win32 \_ кдромдриве** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ кдромдриве** содержит следующие методы.



| Метод            | Описание                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Сброс**         | Не реализован. Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ кдромдриве**](cim-cdromdrive.md) .<br/>                 |
| **SetPowerState** | Не реализован. Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ кдромдриве**](cim-cdromdrive.md) .<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ кдромдриве** имеет следующие свойства.

<dl> <dt>

**Доступность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")
</dt> </dl>

Доступность и состояние устройства.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)


</dt> <dd>

Работа или полная мощность

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)


</dt> <dd>

Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)


</dt> <dd>

Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)


</dt> <dd>

Устройство не работает, но его можно быстро включить в полную работу.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)


</dt> <dd>

Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)


</dt> <dd>

Устройство приостановлено.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)


</dt> <dd>

Устройство не готово.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)


</dt> <dd>

Устройство не настроено.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)


</dt> <dd>

Устройство находится в тихом режиме.

</dd> </dl>

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| служба хранилища устройства \| 001,9 "," MIF. DMTF \| служба хранилища устройства \| 001,11 "," MIF. DMTF \| служба хранилища устройства \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")
</dt> </dl>

Массив возможностей устройства доступа к носителю. Например, устройство может поддерживать произвольный доступ (3), съемный носитель (7) и автоматическую чистку (9).

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)


</dt> <dd>

Поддержка съемных носителей

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)


</dt> <dd>

Поддержка носителя Dual-Sided

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**капабилитидескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")
</dt> </dl>

Массив более подробных объяснений для любого из функций доступа к устройствам, указанных в массиве **capabilities** . Каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Краткое описание объекта — однострочная строка.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**компрессионмесод**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Алгоритм или инструмент, используемый устройством для поддержки сжатия. Если нет возможности описать схему сжатия (возможно, потому, что она неизвестна), используйте следующие слова: "Unknown", чтобы указать, что устройство поддерживает сжатие данных. "Сжатый" для представления того, что устройство поддерживает возможности сжатия, но либо схема сжатия неизвестна, либо не раскрывается. и "не сжато" для представления того, что устройство не поддерживает возможности сжатия.

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

<dt>



 ("Неизвестно")


</dt> <dd>

Схема сжатия неизвестна или не описана.

</dd> <dt>



 ("Сжатый")


</dt> <dd>

Логический файл сжат, но схема сжатия неизвестна или не описана

</dd> <dt>



 ("Не сжато")


</dt> <dd>

Если логический файл не сжат

</dd> </dl>

</dd> <dt>

**конфигманажерерроркоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Windows Configuration Manager код ошибки.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**  (0)


</dt> <dd>

Устройство работает правильно.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.** (1)


</dt> <dd>

Устройство настроено неправильно.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.** (3)


</dt> <dd>

Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.** (4)


</dt> <dd>

Устройство работает неправильно. Один из драйверов или реестр может быть поврежден.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**драйверу для этого устройства нужен ресурс, который Windows не может управлять.** (5)


</dt> <dd>

драйверу для устройства требуется ресурс, который Windows не может управляться.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**  (6)


</dt> <dd>

Конфигурация загрузки для устройства конфликтует с другими устройствами.

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.** (8)


</dt> <dd>

Отсутствует загрузчик драйверов для устройства.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.** (9)


</dt> <dd>

Устройство работает неправильно. Встроенное по управления неправильно сообщает ресурсы для устройства.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.** (10)


</dt> <dd>

Не удается запустить устройство.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.** (11)


</dt> <dd>

Сбой устройства.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.** (12)


</dt> <dd>

Устройству не удается найти достаточно свободных ресурсов для использования.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.** (13)


</dt> <dd>

Windows не может проверить ресурсы устройства.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.** (14)


</dt> <dd>

Устройство не может работать должным образом, пока компьютер не будет перезагружен.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.** (15)


</dt> <dd>

Устройство не работает должным образом из-за возможной проблемы повторного перечисления.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.** (16)


</dt> <dd>

Windows не удается найти все ресурсы, используемые устройством.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.** (17)


</dt> <dd>

Устройство запрашивает неизвестный тип ресурса.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.** (18)


</dt> <dd>

Необходимо переустановить драйверы устройств.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.** (20)


</dt> <dd>

Реестр может быть поврежден.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.** (21)


</dt> <dd>

Сбой системы. Если изменение драйвера устройства неэффективно, см. документацию по оборудованию. Windows удаляет устройство.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.** (22)


</dt> <dd>

Устройство отключено.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.** (23)


</dt> <dd>

Сбой системы. Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.** (24)


</dt> <dd>

Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows все еще настраивает это устройство.** (25)


</dt> <dd>

Windows все еще настраивает устройство.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows все еще настраивает это устройство.** (26)


</dt> <dd>

Windows все еще настраивает устройство.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.** (27)


</dt> <dd>

Устройство не имеет допустимой конфигурации журнала.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.** (28)


</dt> <dd>

Драйверы устройств не установлены.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.** (29)


</dt> <dd>

Устройство отключено. Встроенное по устройства не предпредоставил необходимые ресурсы.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.** (30)


</dt> <dd>

Устройство использует ресурс IRQ, который используется другим устройством.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.** 1-31


</dt> <dd>

Устройство работает неправильно. Windows не может загрузить необходимые драйверы устройств.

</dd> </dl>

</dd> <dt>

**конфигманажерусерконфиг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Если **значение — true**, устройство использует определяемую пользователем конфигурацию.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**дефаултблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")
</dt> </dl>

Размер блока по умолчанию (в байтах) для этого устройства.

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")
</dt> </dl>

Описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жетлогикалдривестрингс")
</dt> </dl>

Уникальный идентификатор для устройства чтения компакт-дисков.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**Накопитель**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жетдриветипе")
</dt> </dl>

Буква дисковода компакт-дисков.

Пример: "d: \\ "

</dd> <dt>

**дривеинтегрити**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Если **значение — true**, файлы могут быть правильно считаны с компакт-устройства. Это достигается путем считывания блока данных дважды и сравнения данных с самим собой.

</dd> <dt>

**еррорклеаред**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о корректирующих действиях, которые могут быть выполнены.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**еррормесодологи**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип обнаружения и исправления ошибок, поддерживаемых этим устройством.

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

</dd> <dt>

**филесистемфлагс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции Win32API файловой системы \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")
</dt> </dl>

Это свойство устарело. Вместо этого свойства используйте **филесистемфлагсекс**.

</dd> <dt>

**филесистемфлагсекс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")
</dt> </dl>

флаги файловой системы, связанные с дисководом Windows CD-rom. Этот параметр может быть любым сочетанием флагов, **но \_ \_ Сжатие файлов FS и файл** **\_ \_ - \_ Vol** со степенью сжатия являются взаимоисключающими.

<dt>

<span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>

<span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Поиск с учетом регистра** (1)


</dt> <dd>

Файловая система поддерживает имена файлов с учетом регистра.

</dd> <dt>

<span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>

<span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Имена с сохранением регистра** (2)


</dt> <dd>

Файловая система сохраняет регистр имен файлов при размещении на диске имени.

</dd> <dt>

<span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>

<span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Юникод на диске** (4)


</dt> <dd>

Файловая система поддерживает Юникод в именах файлов по мере их появления на диске.

</dd> <dt>

<span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>

<span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Постоянные списки ACL** (8)


</dt> <dd>

Файловая система сохраняет и обеспечивает применение списков управления доступом (ACL). Например, файловая система NTFS сохраняет и применяет списки ACL, а файловая система FAT — нет.

</dd> <dt>

<span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>

<span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**Сжатие файлов** (16)


</dt> <dd>

Файловая система поддерживает сжатие на основе файлов.

</dd> <dt>

<span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>

<span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Квоты томов** (32)


</dt> <dd>

Файловая система поддерживает дисковые квоты.

</dd> <dt>

<span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>

<span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Поддержка разреженных файлов** (64)


</dt> <dd>

Файловая система поддерживает резервные файлы.

</dd> <dt>

<span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>

<span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Поддержка точек повторного анализа** (128)


</dt> <dd>

Файловая система поддерживает точки повторного анализа.

</dd> <dt>

<span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>

<span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**поддерживает удаленное служба хранилища** (256)


</dt> <dd>

Файловая система поддерживает удаленное хранение файлов.

</dd> <dt>

<span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>

<span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Поддержка длинных имен** (16384)


</dt> <dd>

Файловая система поддерживает имена файлов длиной более восьми символов.

</dd> <dt>

<span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>

<span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Том сжат** (32768)


</dt> <dd>

Указанный том диска является сжатым томом, например томом DoubleSpace.

</dd> <dt>

<span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>

<span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Том только для чтения** (524289)


</dt> <dd>

Указанный том доступен только для чтения.

</dd> <dt>

<span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>

<span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Поддержка идентификаторов объектов** (65536)


</dt> <dd>

Файловая система поддерживает идентификаторы объектов.

</dd> <dt>

<span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>

<span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Поддержка шифрования** (131072)


</dt> <dd>

Файловая система поддерживает шифрованную файловую систему (EFS).

</dd> <dt>

<span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>

<span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**поддерживает именованные Потоки** (262144)


</dt> <dd>

Файловая система поддерживает именованные потоки.

</dd> </dl>

Пример: 0

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жетдриветипе")
</dt> </dl>

Буква диска, однозначно определяющая устройство чтения компакт-дисков.

Пример: "d: \\ "

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")
</dt> </dl>

Дата и время установки объекта. Для этого свойства не требуется значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**ластерроркоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Код последней ошибки, сообщаемый логическим устройством.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")
</dt> </dl>

изготовитель дисковода компакт-дисков Windows.

Пример: "ПЛЕКСТОР"

</dd> <dt>

**максблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")
</dt> </dl>

Максимальный размер блока в байтах для носителя, доступного этому устройству.

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**максимумкомпонентленгс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")
</dt> </dl>

максимальная длина компонента имени файла, поддерживаемого дисководом Windows CD-ROM. Компонент имени файла часть имени файла между символами обратной косой черты. Значение можно использовать, чтобы указать, что в указанной файловой системе поддерживаются длинные имена. Например, для файловой системы FAT, поддерживающей длинные имена, функция сохраняет значение 255, а не предыдущий индикатор 8,3. Длинные имена также могут поддерживаться в системах, использующих файловую систему NTFS.

Пример: 255

</dd> <dt>

**максмедиасизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")
</dt> </dl>

Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**медиалоадед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")
</dt> </dl>

Если задано **значение true**, компакт-диск находится в дисководе.

</dd> <dt>

**Мультимедиа**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| жетдриветипе")
</dt> </dl>

Тип носителя, который может использоваться этим устройством или к которому можно получить доступ. Возможны следующие значения:

<dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

**Произвольный доступ** ("случайный доступ")


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

**Поддерживает запись** ("поддерживает запись")


</dt> <dd></dd> <dt>

<span id="Removable_Media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

**Съемный носитель** (съемный носитель)


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

**компакт-** диск ("CD-ROM")


</dt> <dd></dd> </dl>

</dd> <dt>

**мфрассигнедревисионлевел**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK \| кернелмодедриверс \| [**Storage \_ Device \_ дескриптор**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| продуктревисионоффсет")
</dt> </dl>

Уровень редакции встроенного по, назначенный производителем.

</dd> <dt>

**минблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")
</dt> </dl>

Минимальный размер блока в байтах для носителя, доступного этому устройству.

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")
</dt> </dl>

Метка для объекта. При создании подклассов свойство может быть переопределено как ключевое свойство.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**нидсклеанинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если задано **значение true**, устройству доступа к носителю требуется очистка. Возможность ручной или автоматической очистки указывается в свойстве **capabilities** .

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

</dd> <dt>

**нумберофмедиасуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное количество носителей, которые можно поддерживать или вставлять, если устройство доступа к носителю поддерживает несколько отдельных носителей.

Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Windows Самонастраивающийся идентификатор устройства логического устройства.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

Пример: " \* PNP030b"

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив конкретных возможностей логического устройства, связанных с питанием.

Это свойство наследуется **от \_ CIM**-унаследованной модели.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)


</dt> <dd>

Для этого устройства не поддерживаются мощности, связанные с питанием.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)


</dt> <dd>

Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)


</dt> <dd>

Устройство может изменить свое состояние электропитания на основе использования или других критериев.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)


</dt> <dd>

Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) . Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован. Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)


</dt> <dd>

Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState*, установленным в значение 5 (Power Cycle).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)


</dt> <dd>

Поддержка по времени Power-On

Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.

</dd> </dl>

</dd> <dt>

**поверманажементсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение — true**, устройство может управляться с помощью управления питанием. Это означает, что его можно перевести в режим приостановки и т. д. Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**ревисионлевел**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| ревисионлевел")
</dt> </dl>

уровень редакции встроенного по Windows дисководе компакт-дисков.

</dd> <dt>

**SCSIBus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SCSI-структуры \| [**SCSI \_ \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| пасид")
</dt> </dl>

Номер шины SCSI для диска.

Пример: 0

</dd> <dt>

**SCSILogicalUnit**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SCSI Structures \| [**SCSI \_ \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| LUN")
</dt> </dl>

Логический номер устройства (LUN) SCSI диска. LUN используется для обозначения контроллера SCSI, к которому осуществляется доступ в системе, где используется более одного контроллера. Идентификатор устройства SCSI аналогичен, но представляет собой обозначение нескольких устройств на одном контроллере.

Пример: 0

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SCSI-структуры \| [**SCSI \_ \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| сксистатус")
</dt> </dl>

Номер порта SCSI диска.

Пример: 1

</dd> <dt>

**скситаржетид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| DeviceIoControl \| ioctl \_ SCSI \_ Get \_ Address")
</dt> </dl>

номер идентификатора SCSI Windows дисковода компакт-дисков.

Пример: 0

</dd> <dt>

**Номер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры устройства \| [**хранения \_ \_**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| сериалнумбероффсет ")
</dt> </dl>

Номер, предоставленный производителем для идентификации физического носителя. Пример: WD-WM3493798728.

</dd> <dt>

**Размер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жетдискфриспаце"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Размер диска.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

В эти значения входят:

<dt>

<span id="OK"></span><span id="ok"></span>

**ОК** ("ОК")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Ошибка** ("ошибка")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Пониженная работоспособность** (пониженная работоспособность)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Пред-ошибка** ("пред Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Запуск** ("Запуск")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Остановка** ("остановка")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Служба** ("служба")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Пренапряжению** ("напряжению")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Невосстановление** ("невосстановление")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Нет контакта** ("нет контакта")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Потеря** связи ("потеря связи")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")
</dt> </dl>

Состояние логического устройства. Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Значение свойства **CreationClassName** компьютера.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Имя системы области.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**трансферрате**
</dt> <dd> <dl> <dt>

Тип данных: **real64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| ссылка на файл Win32API и Справочник по времени"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайт в секунду")
</dt> </dl>

Скорость передачи устройства чтения компакт-дисков. Значение-1 указывает, что скорость не может быть определена. В этом случае компакт-диск не находится на диске.

</dd> <dt>

**Тома**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")
</dt> </dl>

имя тома дисковода компакт-дисков Windows.

</dd> <dt>

**волумесериалнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Файловая система-функции \| [**жетволумеинформатион**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")
</dt> </dl>

Серийный номер тома носителя в устройстве чтения компакт-дисков.

Пример: A8C3-D032

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ кдромдриве** является производным от [**CIM \_ кдромдриве**](cim-cdromdrive.md) , который является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md). Класс **CIM \_ медиаакцессдевице** является производным от [**CIM \_**](cim-logicaldevice.md)с параметром.

## <a name="examples"></a>Примеры

В следующем примере на языке VBScript определяется, находится ли компакт-диск в дисководе CDROM.


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КДРОМДРИВЕ CIM**](cim-cdromdrive.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> <dt>

[Задачи WMI: оборудование компьютера](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[Задачи WMI: диски и файловые системы](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

