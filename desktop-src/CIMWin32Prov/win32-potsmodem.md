---
description: '\_Класс WMI потсмодем инструментария Win32 представляет службы и характеристики модема простой старой телефонной службы (POTS) в компьютерной системе, на которой работает Windows.'
ms.assetid: 24589942-e2c3-477e-8179-59ae4a4aa85a
ms.tgt_platform: multiple
title: Класс Win32_POTSModem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModem
- Win32_POTSModem.Reset
- Win32_POTSModem.SetPowerState
- Win32_POTSModem.AnswerMode
- Win32_POTSModem.AttachedTo
- Win32_POTSModem.Availability
- Win32_POTSModem.BlindOff
- Win32_POTSModem.BlindOn
- Win32_POTSModem.Caption
- Win32_POTSModem.CompatibilityFlags
- Win32_POTSModem.CompressionInfo
- Win32_POTSModem.CompressionOff
- Win32_POTSModem.CompressionOn
- Win32_POTSModem.ConfigManagerErrorCode
- Win32_POTSModem.ConfigManagerUserConfig
- Win32_POTSModem.ConfigurationDialog
- Win32_POTSModem.CountriesSupported
- Win32_POTSModem.CountrySelected
- Win32_POTSModem.CreationClassName
- Win32_POTSModem.CurrentPasswords
- Win32_POTSModem.DCB
- Win32_POTSModem.Default
- Win32_POTSModem.Description
- Win32_POTSModem.DeviceID
- Win32_POTSModem.DeviceLoader
- Win32_POTSModem.DeviceType
- Win32_POTSModem.DialType
- Win32_POTSModem.DriverDate
- Win32_POTSModem.ErrorCleared
- Win32_POTSModem.ErrorControlForced
- Win32_POTSModem.ErrorControlInfo
- Win32_POTSModem.ErrorControlOff
- Win32_POTSModem.ErrorControlOn
- Win32_POTSModem.ErrorDescription
- Win32_POTSModem.FlowControlHard
- Win32_POTSModem.FlowControlOff
- Win32_POTSModem.FlowControlSoft
- Win32_POTSModem.InactivityScale
- Win32_POTSModem.InactivityTimeout
- Win32_POTSModem.Index
- Win32_POTSModem.IndexEx
- Win32_POTSModem.InstallDate
- Win32_POTSModem.LastErrorCode
- Win32_POTSModem.MaxBaudRateToPhone
- Win32_POTSModem.MaxBaudRateToSerialPort
- Win32_POTSModem.MaxNumberOfPasswords
- Win32_POTSModem.Model
- Win32_POTSModem.ModemInfPath
- Win32_POTSModem.ModemInfSection
- Win32_POTSModem.ModulationBell
- Win32_POTSModem.ModulationCCITT
- Win32_POTSModem.ModulationScheme
- Win32_POTSModem.Name
- Win32_POTSModem.PNPDeviceID
- Win32_POTSModem.PortSubClass
- Win32_POTSModem.PowerManagementCapabilities
- Win32_POTSModem.PowerManagementSupported
- Win32_POTSModem.Prefix
- Win32_POTSModem.Properties
- Win32_POTSModem.ProviderName
- Win32_POTSModem.Pulse
- Win32_POTSModem.Reset
- Win32_POTSModem.ResponsesKeyName
- Win32_POTSModem.RingsBeforeAnswer
- Win32_POTSModem.SpeakerModeDial
- Win32_POTSModem.SpeakerModeOff
- Win32_POTSModem.SpeakerModeOn
- Win32_POTSModem.SpeakerModeSetup
- Win32_POTSModem.SpeakerVolumeHigh
- Win32_POTSModem.SpeakerVolumeInfo
- Win32_POTSModem.SpeakerVolumeLow
- Win32_POTSModem.SpeakerVolumeMed
- Win32_POTSModem.Status
- Win32_POTSModem.StatusInfo
- Win32_POTSModem.StringFormat
- Win32_POTSModem.SupportsCallback
- Win32_POTSModem.SupportsSynchronousConnect
- Win32_POTSModem.SystemCreationClassName
- Win32_POTSModem.SystemName
- Win32_POTSModem.Terminator
- Win32_POTSModem.TimeOfLastReset
- Win32_POTSModem.Tone
- Win32_POTSModem.VoiceSwitchFeature
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e79cb842acd2063522f901d050c3fab6db3251a39a212a234f062935cc30b87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020112"
---
# <a name="win32_potsmodem-class"></a>\_Класс Win32 потсмодем

Класс **WMI \_ потсмодем** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет службы и характеристики модема простой старой телефонной службы (POTS) в компьютерной системе, на которой работает Windows.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModem : CIM_PotsModem
{
  uint16   AnswerMode;
  string   AttachedTo;
  uint16   Availability;
  string   BlindOff;
  string   BlindOn;
  string   Caption;
  string   CompatibilityFlags;
  uint16   CompressionInfo;
  string   CompressionOff;
  string   CompressionOn;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   ConfigurationDialog;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  uint8    DCB[];
  uint8    Default[];
  string   Description;
  string   DeviceID;
  string   DeviceLoader;
  string   DeviceType;
  uint16   DialType;
  datetime DriverDate;
  boolean  ErrorCleared;
  string   ErrorControlForced;
  uint16   ErrorControlInfo;
  string   ErrorControlOff;
  string   ErrorControlOn;
  string   ErrorDescription;
  string   FlowControlHard;
  string   FlowControlOff;
  string   FlowControlSoft;
  string   InactivityScale;
  uint32   InactivityTimeout;
  uint32   Index;
  string   IndexEx;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  string   Model;
  string   ModemInfPath;
  string   ModemInfSection;
  string   ModulationBell;
  string   ModulationCCITT;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  string   PortSubClass;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Prefix;
  uint8    Properties[];
  string   ProviderName;
  string   Pulse;
  string   Reset;
  string   ResponsesKeyName;
  uint8    RingsBeforeAnswer;
  string   SpeakerModeDial;
  string   SpeakerModeOff;
  string   SpeakerModeOn;
  string   SpeakerModeSetup;
  string   SpeakerVolumeHigh;
  uint16   SpeakerVolumeInfo;
  string   SpeakerVolumeLow;
  string   SpeakerVolumeMed;
  string   Status;
  uint16   StatusInfo;
  string   StringFormat;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  string   Terminator;
  datetime TimeOfLastReset;
  string   Tone;
  string   VoiceSwitchFeature;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ потсмодем** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ потсмодем** содержит следующие методы.



| Метод            | Описание                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Сброс**         | Не реализован. Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ потсмодем**](cim-potsmodem.md).<br/>                 |
| **SetPowerState** | Не реализован. Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ потсмодем**](cim-potsmodem.md).<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ потсмодем** имеет следующие свойства.

<dl> <dt>

**ансвермоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущий параметр автоматического ответа или ответного вызова для модема.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (2)


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

**Ответ вручную** (3)


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

**Автоматический ответ** (4)


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

**Автоматический ответ с обратным вызовом** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**AttachedTo**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| аттачедто")
</dt> </dl>

Порт, к которому подключен POTS-модем.

Пример: "COM1"

</dd> <dt>

**Доступность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")
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

**блиндофф**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| блиндофф")
</dt> </dl>

Командная строка, используемая для обнаружения гудка в наборе перед набором номера.

Пример: X4

</dd> <dt>

**блиндон**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| блиндон")
</dt> </dl>

Командная строка, используемая для набираемого номера.

Пример: "X3"

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**CompatibilityFlags**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| компатибилитифлагс")
</dt> </dl>

Все протоколы модемного подключения, с которыми совместимо это модемное устройство.

</dd> <dt>

**компрессионинфо**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Характеристики сжатия данных модема.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd>

Неизвестно

</dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**Без сжатия** (2)


</dt> <dd>

Другие

</dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)


</dt> <dd>

Без сжатия

</dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span id="v.42bis"></span><span id="V.42BIS"></span>**V. 42bis** (4)


</dt> <dd>

MNP 5

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5.0**


</dt> <dd>

V. 42bis

</dd> </dl>

</dd> <dt>

**компрессионофф**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ \\ \\ класса Control \| Compression \_ Off")
</dt> </dl>

Строка команды, используемая для отключения аппаратного сжатия данных.

Пример: "S46 = 136"

</dd> <dt>

**компрессионон**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ элемент управления \\ \\ \| Compression класса \_ On")
</dt> </dl>

Командная строка, используемая для включения аппаратного сжатия данных.

Пример: "S46 = 138"

</dd> <dt>

**конфигманажерерроркоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Код ошибки Win32 Configuration Manager.

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

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Если **значение — true**, устройство использует определяемую пользователем конфигурацию.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**конфигуратиондиалог**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| конфигдиалог")
</dt> </dl>

Строка инициализации модема. Это свойство состоит из командных строк из других свойств этого класса.

</dd> <dt>

**каунтриессуппортед**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив стран или регионов, в которых может действовать модем.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**каунтриселектед**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Страна или регион, для которых в настоящее время программируется модем. Если поддерживается несколько стран или регионов, это свойство определяет, какая из них выбрана в данный момент для использования.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется [**от \_ CIM**](cim-logicalfile.md)-унаследованной модели.

</dd> <dt>

**куррентпассвордс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список паролей, определенных в данный момент для модема. Этот массив можно оставить пустым по соображениям безопасности.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**DCB**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры связи Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")
</dt> </dl>

Параметры управления для устройства последовательного подключения (в данном случае это модемное устройство).

</dd> <dt>

**По умолчанию**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс управления \| по умолчанию")
</dt> </dl>

При **значении true** этот модем POTS является модемом по умолчанию в компьютерной системе, где работает Windows.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
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

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Уникальный идентификатор этого POTS модема с других устройств в системе.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**девицелоадер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| загрузчик")
</dt> </dl>

Имя загрузчика устройства для модема. Загрузчик устройства загружает драйверы и перечислители устройств и управляет ими для данного устройства.

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| типа устройства")
</dt> </dl>

Физический тип модема.

Значения качества производительности:

<dl> <dd>"Нуль Modem"</dd> <dd>"Внутренний модем"</dd> <dd>"Внешний модем"</dd> <dd>"PCMCIA Modem"</dd> <dd>Неизвестный</dd> </dl>

<dt>

<span id="Null_Modem"></span><span id="null_modem"></span><span id="NULL_MODEM"></span>

**Нуль-модем** ("нуль-модем")


</dt> <dd></dd> <dt>

<span id="Internal_Modem"></span><span id="internal_modem"></span><span id="INTERNAL_MODEM"></span>

**Внутренний модем** ("внутренний модем")


</dt> <dd></dd> <dt>

<span id="External_Modem"></span><span id="external_modem"></span><span id="EXTERNAL_MODEM"></span>

**Внешний модем** ("внешний модем")


</dt> <dd></dd> <dt>

<span id="PCMCIA_Modem"></span><span id="pcmcia_modem"></span><span id="PCMCIA_MODEM"></span>

**PCMCIA-модем** ("PCMCIA-модем")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> </dl>

</dd> <dt>

**диалтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип используемого метода набора номера.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

**Тон** (1)


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

**Импульс** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**дривердате**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| дривердате")
</dt> </dl>

Дата драйвера модема.

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

**еррорконтролфорцед**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ класс управления Win32Registry системы CurrentControlSet \\ \\ \\ \\ \| ErrorControl \_ forced")
</dt> </dl>

Командная строка, используемая для включения контроля исправления ошибок при установлении соединения. Это повышает надежность подключения.

Пример: "+ Q5S36 = 4S48 = 7"

</dd> <dt>

**еррорконтролинфо**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Характеристики исправления ошибок модема.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

**Без исправления ошибок** (2)


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

**MNP 4** (3)


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

**Лапм** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**еррорконтролофф**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ класс управления Win32Registry системы CurrentControlSet \\ \\ \\ \\ \| ErrorControl \_ Off")
</dt> </dl>

Командная строка, используемая для отключения управления ошибками.

Пример: "+ Q6S36 = 3S48 = 128"

</dd> <dt>

**еррорконтролон**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ On")
</dt> </dl>

Командная строка, используемая для включения управления ошибками.

Пример: "+ Q5S36 = 7S48 = 7"

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**фловконтролхард**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| фловконтрол \_ Hard")
</dt> </dl>

Командная строка, используемая для включения аппаратного управления потоком. Flow элемент управления состоит из сигналов, передаваемых между компьютерами и проверяющих готовность обоих компьютеров к передаче или приему данных.

Пример: "&K1"

</dd> <dt>

**фловконтролофф**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ класс управления Win32Registry системы CurrentControlSet \\ \\ \\ \\ \| фловконтрол \_ Off")
</dt> </dl>

Командная строка, используемая для отключения управления потоком. Flow элемент управления состоит из сигналов, передаваемых между компьютерами и проверяющих готовность обоих компьютеров к передаче или приему данных.

Пример: "&K0"

</dd> <dt>

**фловконтролсофт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| фловконтрол \_ Soft")
</dt> </dl>

Командная строка, используемая для включения управления потоком программного обеспечения. Flow элемент управления состоит из сигналов, передаваемых между компьютерами и проверяющих готовность обоих компьютеров к передаче или приему данных.

Пример: "&априорной оценкой K2"

</dd> <dt>

**инактивитискале**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| инактивитискале")
</dt> </dl>

Множитель, используемый со свойством **инактивититимеаут** для вычисления периода ожидания соединения.

</dd> <dt>

**InactivityTimeout**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("секунды")
</dt> </dl>

Ограничение времени (в секундах) автоматического отключения телефонной линии, если обмен данными не выполняется. Значение 0 (ноль) указывает, что эта функция имеется, но не включена.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Номер индекса для этого модема POTS.

Пример: 0

</dd> <dt>

**индексекс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор экземпляра устройства для этого модема POTS.

Пример: "1&08"

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** это свойство доступно, начиная с Windows Server 2016 и Windows 10.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
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

**максбаудратетофоне**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")
</dt> </dl>

Максимальная настраиваемая скорость связи для доступа к телефонной системе.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**максбаудратетосериалпорт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")
</dt> </dl>

Максимальная настраиваемая скорость обмена данными с COM-портом для внешнего модема. Введите 0 (ноль), если это не применимо.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**макснумберофпассвордс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число паролей, определяемых в самом модеме. Если эта функция не поддерживается, введите 0 (ноль).

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**Модель**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| системная \\ \\ \\ \\ \\ \\ модель управления классом CurrentControlSet \| ")
</dt> </dl>

Модель этого модема POTS.

Пример: "Спортстер 56K External"

</dd> <dt>

**модеминфпас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| инфпас")
</dt> </dl>

Путь к INF-файлу модема. Этот файл содержит сведения об инициализации модема и его драйвера.

пример: "C: \\ Windows \\ INF"

</dd> <dt>

**модеминфсектион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| инфсектион")
</dt> </dl>

Имя раздела в INF-файле модема, который содержит сведения о модеме.

</dd> <dt>

**модулатионбелл**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| модуляция \_ Bell")
</dt> </dl>

Командная строка, используемая для указания модему использования модуляций Bell для 300 и 1200 бит/с.

Пример: "B1"

</dd> <dt>

**модулатионкЦитт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| модуляция \_ CCITT")
</dt> </dl>

Командная строка, используемая для указания модему использования модуляций CCITT для 300 и 1200 бит/с.

Пример: B0

</dd> <dt>

**модулатионсчеме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Схема модуляции модема.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Не поддерживается** (2)


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

**Звонок 103** (3)


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

**Колокольчик 212A** (4)


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

**V. 22bis** (5)


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

**V. 32** (6)


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

**V. 32bis** (7)


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

**V. Turbo** (8)


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

**V. FC** (9)


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

**V. 34** (10)


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

**V. 34bis** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")
</dt> </dl>

Метка, по которой известен объект. При создании подклассов свойство может быть переопределено как ключевое свойство.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Windows Самонастраивающийся идентификатор устройства логического устройства.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

Пример: " \* PNP030b"

</dd> <dt>

**портсубкласс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| портсубкласс"), **value** ("параллельный порт", "последовательный порт", "модем")
</dt> </dl>

Определение порта, используемого для этого модема.

<dt>



 ("00")


</dt> <dd>

Parallel Port (Параллельный порт)

</dd> <dt>



 ("01")


</dt> <dd>

Последовательный порт

</dd> <dt>



 ("02")


</dt> <dd>

Modem (Модем)

</dd> </dl>

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


</dt> <dd></dd> <dt>

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

Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) . Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован. Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)


</dt> <dd>

Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).

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

Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.). Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**Prefix**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ управления \\ \\ \| префиксом класса")
</dt> </dl>

Префикс, используемый для доступа к внешней линии.

</dd> <dt>

**Свойства**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ \\ \\ Свойства класса элемента управления Win32Registry System CurrentControlSet \\ \\ \| ")
</dt> </dl>

Список всех свойств (и их значений) для этого модема.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| providerName")
</dt> </dl>

Сетевой путь к компьютеру, на котором находятся службы модема.

</dd> <dt>

**Ритм**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Pulse")
</dt> </dl>

Командная строка, используемая для указания модему использования импульсного режима для набора. Импульсный набор необходим для телефонных линий, которые не могут поддерживать тоновый набор.

Пример: "P"

</dd> <dt>

**Сброс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**переопределить**](../wmisdk/standard-qualifiers.md) (сбросить), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| rereset")
</dt> </dl>

Командная строка, используемая для сброса модема при следующем вызове.

Пример: "AT&F"

</dd> <dt>

**респонсескэйнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| респонсескэйнаме")
</dt> </dl>

Ответ. Этот модем может сообщить операционной системе о процессе подключения. Первые два символа указывают тип ответа. Два второго символа указывают сведения о выполняемом подключении. два второго символа используются только для выполнения согласования или для Подключение кодов ответа. Следующие восемь символов указывают скорость линии модем-модема, согласованную в битах в секунду (бит/с). Символы представляют собой 32-разрядный длинный целочисленный формат без знака (байт и слово в обратных). Последние восемь символов указывают на то, что модем переводится на другой порт или скорость связи с терминальным оборудованием (DTE). Обычно это поле не используется, так как модемы подключаются к заблокированной скорости порта независимо от скорости передачи данных между модемом или устройством связи (DCE).

</dd> <dt>

**рингсбефореансвер**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число звонков перед ответом модема на входящий вызов.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**спеакермодедиал**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакермодедиал")
</dt> </dl>

Командная строка, используемая для включения динамика модема после набора номера и отключения динамика при установке соединения.

Пример: "M1"

</dd> <dt>

**спеакермодеофф**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакермодеофф")
</dt> </dl>

Командная строка, используемая для выключения динамика модема.

Пример: M0

</dd> <dt>

**спеакермодеон**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакермодеон")
</dt> </dl>

Командная строка, используемая для включения динамика модема.

Пример: "m2"

</dd> <dt>

**спеакермодесетуп**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакермодесетуп")
</dt> </dl>

Командная строка, указывающая модему на необходимость включения динамика (до установления подключения).

Пример: "M3"

</dd> <dt>

**спеакерволумехигх**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| спеакерволуме \_ High")
</dt> </dl>

Командная строка, используемая для настройки динамика модема на самый большой том.

Пример: "L3"

</dd> <dt>

**спеакерволумеинфо**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описывает уровень громкости звуковых тонов с модема.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Не поддерживается** (2)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Высокий** (3)


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

**Средний** (4)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Низкий** (5)


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Выкл** . (6)


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

**Авто** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**спеакерволумелов**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| спеакерволуме \_ Low")
</dt> </dl>

Командная строка, используемая для настройки динамика модема на самый низкий том.

Пример: "L1"

</dd> <dt>

**спеакерволумемед**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакерволуме \_ MED")
</dt> </dl>

Командная строка, используемая для настройки динамика модема на средний том.

Пример: "L2"

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
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

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")
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

**StringFormat**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \_ \| структуры устройств Win32 API Line \| линедевкапс \| двстрингформат")
</dt> </dl>

Тип символов, используемых для текста, передаваемого через модем.

Значения качества производительности:

<dl> <dd>"Формат строки ASCII"</dd> <dd>"Формат строки DBCS"</dd> <dd>"Формат строки Юникода"</dd> </dl>

<dt>

<span id="ASCII_string_format"></span><span id="ascii_string_format"></span><span id="ASCII_STRING_FORMAT"></span>

**Формат строки ASCII** (формат строкового формата ASCII)


</dt> <dd></dd> <dt>

<span id="DBCS_string_format"></span><span id="dbcs_string_format"></span><span id="DBCS_STRING_FORMAT"></span>

**Формат строки DBCS** (формат строки DBCS)


</dt> <dd></dd> <dt>

<span id="UNICODE_string_format"></span><span id="unicode_string_format"></span><span id="UNICODE_STRING_FORMAT"></span>

**Формат строки Юникода** ("формат строки Юникода")


</dt> <dd></dd> </dl>

</dd> <dt>

**суппортскаллбакк**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, модем поддерживает обратный вызов.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**суппортссинчронаусконнект**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

При **значении true** синхронное, а также асинхронное взаимодействие поддерживается.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)
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

Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Имя системы области.

Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.

</dd> <dt>

**Признак конца**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ элемент управления \\ \\ \| признак конца класса")
</dt> </dl>

Строка, обозначающая конец строки команды.

Пример: "<CR"

</dd> <dt>

**тимеофластресет**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время последнего сброса модема.

Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).

</dd> <dt>

**Тон**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| тоновый")
</dt> </dl>

Командная строка, предопределяющая модему использовать тоновый режим для набора номера. Телефонная линия должна поддерживать тоновый набор.

Пример: "T"

</dd> <dt>

**воицесвитчфеатуре**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| воицесвитчфеатуре")
</dt> </dl>

Командные строки, используемые для активации возможностей голоса на голосовом модеме.

Пример: "AT + V"

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ потсмодем** является производным от [**CIM \_ потсмодем**](cim-potsmodem.md).

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

[**\_ПОТСМОДЕМ CIM**](cim-potsmodem.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
