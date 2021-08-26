---
description: Представляет возможности и емкость управления секционированной области физического диска в компьютерной системе, работающей Windows.
ms.assetid: 7e78be3f-bae4-4374-abbf-7c4e63ba7593
ms.tgt_platform: multiple
title: Класс Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition
- Win32_DiskPartition.AdditionalAvailability
- Win32_DiskPartition.Availability
- Win32_DiskPartition.PowerManagementCapabilities
- Win32_DiskPartition.IdentifyingDescriptions
- Win32_DiskPartition.MaxQuiesceTime
- Win32_DiskPartition.OtherIdentifyingInfo
- Win32_DiskPartition.StatusInfo
- Win32_DiskPartition.PowerOnHours
- Win32_DiskPartition.TotalPowerOnHours
- Win32_DiskPartition.Access
- Win32_DiskPartition.BlockSize
- Win32_DiskPartition.Bootable
- Win32_DiskPartition.BootPartition
- Win32_DiskPartition.Caption
- Win32_DiskPartition.ConfigManagerErrorCode
- Win32_DiskPartition.ConfigManagerUserConfig
- Win32_DiskPartition.CreationClassName
- Win32_DiskPartition.Description
- Win32_DiskPartition.DeviceID
- Win32_DiskPartition.DiskIndex
- Win32_DiskPartition.ErrorCleared
- Win32_DiskPartition.ErrorDescription
- Win32_DiskPartition.ErrorMethodology
- Win32_DiskPartition.HiddenSectors
- Win32_DiskPartition.Index
- Win32_DiskPartition.InstallDate
- Win32_DiskPartition.LastErrorCode
- Win32_DiskPartition.Name
- Win32_DiskPartition.NumberOfBlocks
- Win32_DiskPartition.PNPDeviceID
- Win32_DiskPartition.PowerManagementSupported
- Win32_DiskPartition.PrimaryPartition
- Win32_DiskPartition.Purpose
- Win32_DiskPartition.RewritePartition
- Win32_DiskPartition.Size
- Win32_DiskPartition.StartingOffset
- Win32_DiskPartition.Status
- Win32_DiskPartition.SystemCreationClassName
- Win32_DiskPartition.SystemName
- Win32_DiskPartition.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b33b812def4c921d528942e3bc416aa8791b4b0faecaaaeaf9d8cf9ccd345959
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085814"
---
# <a name="win32_diskpartition-class"></a>\_Класс Win32 дискпартитион

Класс **WMI \_ дискпартитион** [инструментария](/windows/desktop/WmiSdk/retrieving-a-class) Win32 представляет возможности и Управление емкостью секционированной области физического диска в компьютерной системе, работающей Windows. Пример: диск \# 0, раздел \# 1.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskPartition : CIM_DiskPartition
{
  unit16   AdditionalAvailability;
  uint16   Availability;
  uint16   PowerManagementCapabilities[];
  string   IdentifyingDescriptions[1];
  uint64   MaxQuiesceTime;
  uint64   OtherIdentifyingInfo;
  uint16   StatusInfo;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  uint16   Access;
  uint64   BlockSize;
  boolean  Bootable;
  boolean  BootPartition;
  string.  Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string.  CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DiskIndex;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   HiddenSectors;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  boolean  RewritePartition;
  uint64   Size;
  uint64   StartingOffset;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   Type;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ дискпартитион** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ дискпартитион** содержит следующие методы.



| Метод                                                     | Описание                                                                                                   |
|:-----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Перезапуск**](win32-diskpartition-reset.md)                 | Запрашивает сброс логического устройства.<br/>                                                            |
| [**SetPowerState**](win32-diskpartition-setpowerstate.md) | Задает требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ дискпартитион** имеет следующие свойства.

<dl> <dt>

**Доступ**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Доступ к носителю доступен.

Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)


</dt> <dd>

Возможность записи

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Однократная запись** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**аддитионалаваилабилити**
</dt> <dd> <dl> <dt>

Тип данных: **unit16**
</dt> <dt>

Тип доступа: только для записи
</dt> </dl>

Дополнительные доступность и состояние устройства, кроме указанного в свойстве Availability. Свойство **Availability** указывает основное состояние и доступность устройства. В некоторых случаях это не будет достаточно для обозначения полного состояния устройства. В таких случаях для предоставления дополнительных сведений можно использовать свойство **аддитионалаваилабилити** . Например, основная **доступность** устройства может быть отключена (значение = 8), но она может также находиться в состоянии низкого энергопотребления (**аддитоналаваилабилити** value = 14), либо на устройстве может выполняться диагностика (**Аддитионалаваилабилити** значение = 5, в тесте).

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Работа/полная мощность** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Предупреждение** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**В тесте** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Выключение питания** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

Не в **линии** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

Не **обслуживает** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Снижение работоспособности** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**Не установлено** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Ошибка установки** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

Энергосбережение **— неизвестно** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

Энергосбережение **— режим низкого энергопотребления** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

Энергосбережение **— ждущий режим** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Цикл электропитания** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

Энергосбережение **— предупреждение** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Приостановлено** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**Не готово** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**Не настроено** (20)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Замораживание** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

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


</dt> <dd></dd> <dt>

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

**BlockSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")
</dt> </dl>

Размер в байтах блоков, образующих эту область хранения. Если значение неизвестно или если концепция блока является недопустимой (например, для агрегатных экстентов, памяти или логических дисков), введите 1.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).

</dd> <dt>

**Загружаемый**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, может ли компьютер загружаться из этого раздела.

Это свойство наследуется от [**CIM \_ дискпартитион**](cim-diskpartition.md).

</dd> <dt>

**бутпартитион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| ReadFile")
</dt> </dl>

Секция — это активный раздел. Операционная система использует активный раздел при загрузке с жесткого диска.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **String.**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Краткое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

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


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.** (4)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**драйверу для этого устройства нужен ресурс, который Windows не может управлять.** (5)


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**  (6)


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.** (8)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.** (9)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.** (10)


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.** (11)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.** (12)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.** (13)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.** (14)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.** (15)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.** (16)


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.** (17)


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.** (18)


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.** (20)


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.** (21)


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.** (22)


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.** (23)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.** (24)


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows все еще настраивает это устройство.** (25)


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows все еще настраивает это устройство.** (26)


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.** (27)


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.** (28)


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.** (29)


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.** (30)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.** 1-31


</dt> <dd></dd> </dl>

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

Тип данных: **String.**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

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

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Уникальный идентификатор диска и раздела из остальной части системы.

</dd> <dt>

**DiskIndex**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| ReadFile")
</dt> </dl>

Номер индекса диска, содержащего этот раздел.

Пример: 0

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

Сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть предприняты.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**еррормесодологи**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип обнаружения и исправления ошибок, поддерживаемый этой областью хранения.

Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).

</dd> <dt>

**хидденсекторс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")
</dt> </dl>

Число скрытых секторов в секции.

Пример: 63

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк произвольной формы, предоставляющий объяснения и подробные сведения, лежащие в основе записей в массиве Осеридентифингинфо. Обратите внимание, что каждая запись этого массива связана с записью в Осеридентифингинфо, расположенной в том же индексе.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Номер индекса секции.

Пример: 1

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")
</dt> </dl>

Дата установки объекта. Для этого свойства не требуется значение, указывающее, что объект установлен.

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

**макскуиесцетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **поддерживается**
</dt> </dl>

Максимальное время в миллисекундах, в течение которого устройство может работать в замороженном состоянии. Состояние устройства определяется в его свойствах Availability и Аддитионалаваилабилити, где заморожено передает значение 21. Что происходит в конце предельного времени, зависит от устройства. Устройство может разморозьте, находиться в автономном режиме или предпринимать другие действия. Значение 0 указывает, что устройство может оставаться замороженным в неограниченное время.

> [!Note]
>
> "Свойство Макскуиесцетиме не рекомендуется к использованию. При оценке использования замораживания было определено, что это единственное свойство не подходит для описания, когда устройство будет автоматически выходить из состояния загружена. Фактически, наиболее вероятный сценарий для выхода устройства из состояния загружена был определен на основе числа ожидающих запросов в очереди, а не в течение максимального времени. Оно будет повторно вычислено и перепозиционировано позже. \\n

 

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")
</dt> </dl>

Метка, по которой известен объект. При создании подклассов свойство может быть переопределено как ключевое свойство.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")
</dt> </dl>

Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения. Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства. Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, который фиксирует дополнительные данные, помимо сведений о DeviceID, которые можно использовать для обнаружения объектного типа. Одним из примеров является хранение понятного имени операционной системы для устройства в этом свойстве. Максимальная длина — 256.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

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

Пример: " \* PNP030b"

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает конкретные возможности логического устройства, связанные с питанием. Значения массива 0 = "Unknown", 1 = "не поддерживается" и 2 = "Disabled" являются понятными. Значение 3 = "включено" указывает на то, что функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна. "Режим энергосбережения задается автоматически" (4). описывает, что устройство может изменить свое состояние электропитания в зависимости от использования или других критериев. "Состояние электропитания, устанавливаемое" (5) указывает, что метод SetPowerState поддерживается. "Цикл электропитания поддерживается" (6) указывает, что метод SetPowerState может быть вызван с помощью входной переменной PowerState, установленной в значение 5 ("цикл электропитания"). "Поддержка по времени ожидания" (7) указывает, что метод SetPowerState может быть вызван с помощью входной переменной PowerState, установленной в значение 5 ("цикл электропитания"), а параметр времени установлен на определенную дату и время (или интервал) для включения питания.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Не поддерживается** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (3)


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

**Режимы энергосбережения** записываются автоматически (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**Настраиваемое состояние питания** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**Поддержка циклов электропитания** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

**Поддерживается время включения** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**поверманажементсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.). Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**поверонхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**Основной раздел**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true**, если это основной раздел.

Это свойство наследуется от [**CIM \_ дискпартитион**](cim-diskpartition.md).

</dd> <dt>

**Назначение**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание носителя и его использование.

Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).

</dd> <dt>

**ревритепартитион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры " \| [**\_ сведения о секции**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| ревритепартитион")
</dt> </dl>

Если **значение — true**, сведения о секции изменились. При изменении раздела (с [**\_ \_ \_ \_ разметкой**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)диска с помощью ioctl) система использует это свойство, чтобы определить, какие секции изменились и требуется перезаписывать их сведения. Если **значение равно true**, необходимо перезаписывать секцию.

</dd> <dt>

**Размер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| ReadFile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Общий размер секции.

Пример: 1059045376

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**стартингоффсет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| ReadFile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Начальное смещение секции (в байтах).

Пример: 32256

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

Значения качества производительности:

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

Состояние логического устройства. Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").

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

Имя класса создания для системы области.

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

**тоталповеронхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее количество часов, в течение которых устройство было включено.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**Тип**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| партитионрекорд \| двпартитионтипе")
</dt> </dl>

Тип секции.

Значения качества производительности:

<dl> <dd>Использующ</dd> <dd>"12-разрядная система FAT"</dd> <dd>"XENIX тип 1"</dd> <dd>"XENIX тип 2"</dd> <dd>16-разрядная система FAT</dd> <dd>"Расширенный раздел"</dd> <dd>"MS-DOS v4 огромный"</dd> <dd>"Устанавливаемая файловая система"</dd> <dd>"PowerPC эталонной платформы"</dd> <dd>"UNIX"</dd> <dd>NTFS</dd> <dd>"Win95 w/Extended INT 13"</dd> <dd>"Расширенное w/Extended INT 13"</dd> <dd>"Диспетчер логических дисков"</dd> <dd>Неизвестный</dd> </dl>

<dt>

<span id="Unused"></span><span id="unused"></span><span id="UNUSED"></span>

Не **используется** ("не используется")


</dt> <dd></dd> <dt>

<span id="12-bit_FAT"></span><span id="12-bit_fat"></span><span id="12-BIT_FAT"></span>

**12-разрядная система FAT** ("12-РАЗРЯДНАЯ система FAT")


</dt> <dd></dd> <dt>

<span id="Xenix_Type_1"></span><span id="xenix_type_1"></span><span id="XENIX_TYPE_1"></span>

**Тип XENIX 1** ("тип XENIX 1")


</dt> <dd></dd> <dt>

<span id="Xenix_Type_2"></span><span id="xenix_type_2"></span><span id="XENIX_TYPE_2"></span>

**Тип XENIX 2** ("XENIX тип 2")


</dt> <dd></dd> <dt>

<span id="16-bit_FAT"></span><span id="16-bit_fat"></span><span id="16-BIT_FAT"></span>

**16-разрядная система FAT** (16-РАЗРЯДНАЯ система FAT)


</dt> <dd></dd> <dt>

<span id="Extended_Partition"></span><span id="extended_partition"></span><span id="EXTENDED_PARTITION"></span>

**Расширенный раздел** ("Расширенный раздел")


</dt> <dd></dd> <dt>

<span id="MS-DOS_V4_Huge"></span><span id="ms-dos_v4_huge"></span><span id="MS-DOS_V4_HUGE"></span>

**MS-DOS v4 огромный** ("MS-DOS v4 огромный")


</dt> <dd></dd> <dt>

<span id="Installable_File_System"></span><span id="installable_file_system"></span><span id="INSTALLABLE_FILE_SYSTEM"></span>

**Устанавливаемая файловая система** ("устанавливаемая файловая система")


</dt> <dd></dd> <dt>

<span id="PowerPC_Reference_Platform"></span><span id="powerpc_reference_platform"></span><span id="POWERPC_REFERENCE_PLATFORM"></span>

**эталонная платформа PowerPC** ("PowerPC эталонная платформа")


</dt> <dd></dd> <dt>

<span id="UNIX"></span><span id="unix"></span>

**UNIX** ("Unix")


</dt> <dd></dd> <dt>

<span id="NTFS"></span><span id="ntfs"></span>

**NTFS** ("NTFS")


</dt> <dd></dd> <dt>

<span id="Win95_w_Extended_Int_13"></span><span id="win95_w_extended_int_13"></span><span id="WIN95_W_EXTENDED_INT_13"></span>

**Win95 с расширенным INT 13** ("Win95 w/Extended INT 13")


</dt> <dd></dd> <dt>

<span id="Extended_w_Extended_Int_13"></span><span id="extended_w_extended_int_13"></span><span id="EXTENDED_W_EXTENDED_INT_13"></span>

**Расширенное w/Extended INT 13** ("расширенное w/Extended INT 13")


</dt> <dd></dd> <dt>

<span id="Logical_Disk_Manager"></span><span id="logical_disk_manager"></span><span id="LOGICAL_DISK_MANAGER"></span>

**Диспетчер логических дисков** ("Диспетчер логических дисков")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ дискпартитион** является производным от [**CIM \_ дискпартитион**](cim-diskpartition.md).

Секция — это структурное разделение физического диска. Хотя диск может содержать один раздел, большие тома часто делятся на несколько разделов. Именно поэтому у вас могут быть диски C, D и E, даже если компьютер имеет только один физический жесткий диск.

Windows поддерживает следующие типы разделов:

-   Основной раздел. Это единственный тип раздела, на котором может быть установлена операционная система. Каждый диск может иметь до четырех основных разделов, каждому из которых назначена другая буква диска.
-   Дополнительный раздел. Дополнительный раздел, который можно разделить на несколько логических дисков, каждому из которых назначена уникальная буква диска. На диске может быть только один дополнительный раздел; Тем не менее этот раздел можно разделить на несколько логических дисков. Это позволяет диску иметь не более четырех допустимых первичных разделов.
-   Системный раздел. Любой основной раздел, содержащий операционную систему.

Разделы могут сообщить, как фактически используется физический диск. Изучив физические разделы на диске, можно определить следующие типы действий:

-   Как диск делится на логические диски.
-   Если на диске доступно несекционированное пространство, Это можно определить путем вычитания размера всех разделов на диске из размера самого диска.
-   Если можно загрузить компьютер с этого диска (то есть диск содержит загрузочный раздел).

Все эти вопросы можно устранить с помощью класса **Win32 \_ дискпартитион** .

## <a name="examples"></a>Примеры

Следующий пример кода PowerShell проверяет выравнивание дисков на компьютере: Если смещение имеет дробное значение, диск не выровнен правильно.


```PowerShell
$wql = "SELECT DiskIndex,Index,StartingOffset FROM Win32_DiskPartition"
Get-WmiObject -Query $wql -ComputerName '.' | Select-Object DiskIndex,Index,@{Name='Offset (KB)';Expression={$_.StartingOffset / 1024}} | Format-Table -AutoSize
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ДИСКПАРТИТИОН CIM**](cim-diskpartition.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[Задачи WMI: диски и файловые системы](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

