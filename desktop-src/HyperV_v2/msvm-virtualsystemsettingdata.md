---
description: Представляет параметры виртуализации для виртуальной машины.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Класс Msvm_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990928"
---
# <a name="msvm_virtualsystemsettingdata-class"></a>\_Класс мсвм виртуалсистемсеттингдата

Представляет параметры виртуализации для виртуальной машины.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемсеттингдата** имеет следующие свойства.

<dl> <dt>

**аддитионалрековеринформатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Дополнительные сведения, предоставленные действию восстановления. Значение этого свойства определяется действием в **аутоматикрековеряктион**. Если **аутоматикрековеряктион** равен 0 ("None") или 1 ("Restart"), это значение равно **null**. Если **аутоматикрековеряктион** имеет значение 2 ("вернуться к снимку"), это путь к объекту моментального снимка, который должен быть применен при сбое рабочего процесса виртуальной машины.

</dd> <dt>

**алловфуллсксикоммандсет**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

**Значение true** , если команды SCSI из операционной системы на виртуальной машине передаются транзитным дискам. в противном случае — **значение false**. Если задано **значение true**, команды SCSI, выдаваемые гостевой операционной системой для транзитных дисков, не фильтруются. Рекомендуется, чтобы фильтрация SCSI оставалась включенной для рабочих развертываний.

</dd> <dt>

**алловредуцедфкредунданци**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, разрешена ли динамическая миграция виртуальной машины, настроенной с виртуальным Fibre Channelным адаптером, на конечный компьютер, на котором могут отсутствовать или уменьшаться пути к целевым устройствам Fibre Channel. Это свойство должно быть сброшено после динамической миграции.



| Значение                                                                            | Значение                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>False</dt> </dl> | Невозможно выполнить динамическую миграцию виртуальной машины на целевой компьютер, который может не иметь или не уменьшить пути к целевому Fibre Channel устройствам.<br/>                                                                                                     |
| <dl> <dt>True</dt> </dl>  | Виртуальную машину можно динамически перенести на целевой компьютер, который может не иметь или не уменьшить пути к целевому Fibre Channel устройств. Гостевая операционная система может потерять возможность подключения к хранилищу и может вести себя непредсказуемым образом.<br/> |



 

</dd> <dt>

**Архитектура**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Архитектура этой системы.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

<dt>

<span id="x64"></span><span id="X64"></span>

**x64** ()


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

**arm64** ()


</dt> <dd></dd> </dl>

</dd> <dt>

**аутоматиккритикалеррорактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Определяет действие, выполняемое на виртуальной машине, когда происходит критическая ошибка, например Отключение хранилища.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (0)


</dt> <dd>

Для критических ошибок не будет выполняться никаких действий.

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Приостановить возобновление** (1)


</dt> <dd>

Вызывает приостановку и автоматическое возобновление работы виртуальной машины после устранения критической ошибки.

</dd> </dl>

</dd> <dt>

**аутоматиккритикалеррорактионтимеаут**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**подтип**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("интервал")
</dt> </dl>

Определяет максимальное время, в течение которого **аутоматиккритикалеррорактион** будет выполняться для устранения критической ошибки. Это применимо только в том случае, если значение свойства **аутоматиккритикалеррорактион** не равно 0 (нет). По истечении времени ожидания виртуальная машина будет выключена. Значение будет округляться в большую сторону до ближайшей минуты. Значение 0 означает, что виртуальная машина должна быть выключена немедленно при возникновении критической ошибки.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**аутоматикрековеряктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной машины при сбое программного обеспечения, выполняемого виртуальной машиной. Сбои в этом случае означают сбой, который обнаруживается платформой размещения, например условие состояния взаимоблокировки. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

Это может быть одно из следующих значений.



| Значение                                                                               | Значение                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>2</dt> </dl>        | Нет.<br/>               |
| <dl> <dt>3</dt> </dl>        | Перезапуск.<br/>            |
| <dl> <dt>4</dt> </dl>        | Вернуться к моментальному снимку.<br/> |
| <dl> <dt>5.. 32768</dt> </dl> | Зарезервировано.<br/>           |



 

</dd> <dt>

**аутоматикшутдовнактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной машины при завершении работы узла. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

Это может быть одно из следующих значений.



| Значение                                                                               | Значение                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <dt>2</dt> </dl>        | Отключить.<br/>   |
| <dl> <dt>3</dt> </dl>        | Сохранить состояние.<br/> |
| <dl> <dt>4</dt> </dl>        | Завершение работы.<br/>   |
| <dl> <dt>5.. 32768</dt> </dl> | Зарезервировано.<br/>   |



 

</dd> <dt>

**аутоматикснапшотсенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включены ли Автоматические моментальные снимки для этой виртуальной машины.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**аутоматикстартупактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной машины при запуске узла. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

Это может быть одно из следующих значений.



| Значение                                                                               | Значение                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>2</dt> </dl>        | Нет.<br/>                         |
| <dl> <dt>3</dt> </dl>        | Перезапустить, если ранее он был активен.<br/> |
| <dl> <dt>4</dt> </dl>        | Всегда запускать.<br/>                 |
| <dl> <dt>5.. 32768</dt> </dl> | Зарезервировано.<br/>                     |



 

</dd> <dt>

**аутоматикстартупактионделай**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время задержки перед автоматическим запуском виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**аутоматикстартупактионсекуенценумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число, указывающее относительную последовательность активации виртуальной машины при запуске главной системы. Меньшее значение указывает на более раннюю активацию. Если одна или несколько конфигураций отображают одно и то же значение, последовательность зависит от реализации. Значение 0 указывает, что последовательность зависит от реализации. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**басебоардсериалнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Серийный номер основной платы для виртуальной машины.

</dd> <dt>

**биосгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Глобальный уникальный идентификатор BIOS виртуальной машины.

</dd> <dt>

**биоснумлокк**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

**Значение true** , если параметр Num Lock установлен в значение on BIOS; **Значение false** , если BIOS имеет значение OFF для параметра Num Lock.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Серийный номер BIOS для виртуальной машины.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Порядок загрузки, заданный в BIOS виртуальной машины. Это свойство представляет собой массив значений **BootOrder** \[ \] от 0 до **BootOrder** \[ 3 \] включительно, где каждое значение обозначает устройство для загрузки. Каждое из 4 значений в массиве должно быть задано и не должно совпадать с другим значением в массиве. Виртуальная машина сначала попытается загрузиться с устройства, указанного первым значением в массиве. Если это устройство не содержит загрузочный сектор, виртуальная машина попытается загрузиться со следующего устройства, указанного свойством **BootOrder** , и т. д. Если устройство, указанное в **BootOrder** , не содержит загрузочный сектор, виртуальная машина не сможет загрузиться. Значение по умолчанию для виртуальной машины — \[ 0, 1, 2, 3 \] .

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Дискета** (0)


</dt> <dd>

Виртуальная машина будет пытаться загрузиться с гибкого диска в дисководе.

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span id="CD-ROM"></span><span id="cd-rom"></span>**Компакт-** диск (1)


</dt> <dd>

Виртуальная машина будет пытаться загрузиться с первого компакт-или DVD-диска, найденного в загрузочном секторе.

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Жесткий диск IDE** (2)


</dt> <dd>

Виртуальная машина попытается выполнить загрузку с первого жесткого диска, найденного в загрузочном секторе.

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Загрузка PXE** (3)


</dt> <dd>

Виртуальная машина будет пытаться загрузить PXE из сети.

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Жесткий диск SCSI** (4)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Зарезервировано** (5.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**бутсаурцеордер**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Исходный порядок загрузки для виртуальной машины.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**чассисассеттаг**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Тег ресурса для корпуса виртуальной машины.

</dd> <dt>

**чассиссериалнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Серийный номер корпуса для виртуальной машины.

</dd> <dt>

**конфигуратиондатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранится информация о конфигурации виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Файл ConfigurationFile**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный путь и имя файла, в котором хранятся сведения о конфигурации виртуальной машины. Этот путь задается относительно свойства **конфигуратиондатарут** . Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор конфигурации виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**консолемоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Определяет режим консоли для виртуальной машины.

> [!Note]  
> Это свойство было добавлено в Windows 10 и Windows Server 2016.

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**По умолчанию** (0)


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

**COM1** (1)


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

**COM2** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания параметров виртуальной машины. Если этот объект представляет текущие параметры виртуальной машины, это значение будет соответствовать времени создания системы. Если этот объект представляет параметры моментального снимка для виртуальной машины, это значение будет соответствовать времени создания моментального снимка. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**дебугчаннелид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Идентификатор канала, используемый для отладки виртуальной машины с помощью унифицированного отладчика.

</dd> <dt>

**дебугпорт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Порт TCP/IP, используемый для отладки виртуальной машины с помощью искусственной отладки.

</dd> <dt>

**дебугпортенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, использует ли виртуальная машина искусственную отладку. Это может быть одно из следующих значений.

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>**Выкл** . (0)


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span id="On"></span><span id="on"></span><span id="ON"></span>**В** (1)


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**Онаутоассигнед** (2)


</dt> <dd>

Назначено авто

</dd> </dl>

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда устанавливается в одно из следующих значений.



| Значение                                                                                                                  | Значение                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>"Активные параметры для виртуальной машины"</dt> </dl>   | Этот экземпляр ссылается на виртуальную машину.<br/> |
| <dl> <dt>"Параметры моментальных снимков для виртуальной машины"</dt> </dl> | Этот экземпляр ссылается на моментальный снимок.<br/>        |



 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85))и всегда устанавливается в качестве отображаемого имени для компьютера. Длина имени не может превышать 100 символов.

</dd> <dt>

**енханцедсессионтранспорттипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает тип транспорта, используемый при подключении к расширенному сеансу.

> [!Note]  
> Это свойство было добавлено в Windows 10 версии 1803.

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

**Канал VMBus** (0)


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

**Сокет Hyper-V** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**гуестконтролледкачетипес**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, может ли гостевой клиент управлять типами кэша.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**гуестстатедатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

FilePath каталога, в котором хранятся сведения о состоянии гостевой среды выполнения.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**гуестстатефиле**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к файлу, где хранятся сведения о состоянии гостевой среды выполнения. Относительный путь добавляет к значению свойства **гуестстатедатарут** .

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**хигхммиогапсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Размер верхнего (свыше 4 ГБ) Memory-Mapped зазора ввода-вывода в МБ

> [!Note]  
> Это свойство было добавлено в Windows 10 версии 1703.

 

</dd> <dt>

**инкременталбаккупенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, поддерживает ли модуль записи VSS Hyper-V добавочное резервное копирование этой виртуальной машины.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**исаутоматикснапшот**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, создается ли для пользователя моментальный снимок автоматически.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**IsSaved**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** , если конфигурация содержит ссылку на файл сохраненного состояния; в противном случае — **значение false**. Это не указывает на наличие такого файла, и только в конфигурации его указывает.

</dd> <dt>

**локкондисконнект**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Блокировка консоли при отключении от Vmconnect.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**логдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранится информация журнала для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ловммиогапсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Настраивает размер первого зазора MMIO для виртуальной машины (в мегабайтах).

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

Диапазон: 128 3584

</dd> <dt>

**нетворкбутпреферредпротокол**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Определяет, является ли предпочтительным протоколом для загрузки PXE IPv4 или IPv6.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> </dl>

</dd> <dt>

**Примечания**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указанные пользователем примечания, связанные с виртуальной машиной. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Родительский объект**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если этот экземпляр не представляет систему на основе моментального снимка виртуальной машины, это свойство имеет **значение NULL**. В противном случае свойство содержит путь к объекту **мсвм \_ виртуалсистемсеттингдата** , на котором основан этот экземпляр. При создании иерархии дерева моментальных снимков для виртуальной машины это свойство ссылается на объект, производный от которого является текущим экземпляром (текущий экземпляр является дочерним узлом, а объект, на который ссылается это свойство, является родительским узлом).

</dd> <dt>

**парентпаккаже**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если эта система является контейнером, то путь к Мсвм \_ контаинерпаккаже, на котором основана данная система.

> [!Note]  
> Добавлено в Windows 10; удалено в Windows 10, версия 1703.

 

</dd> <dt>

**паусеафтербутфаилуре**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, будет ли BIOS приостанавливать работу после каждой неудачной записи загрузки, ожидающей нажатия пользователем клавиши. **Значение true** , если BIOS приостанавливает работу; в противном случае — **значение false**.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**рековерифиле**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Полный путь к файлу, в котором хранится информация, связанная с восстановлением для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**SecureBootEnabled**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включена ли безопасная загрузка для виртуальной машины. **Значение true** , если включено; в противном случае — **значение false**.

> [!Note]  
> Безопасную загрузку можно включить только для виртуальных машин поколения 2.

 

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**секуребуттемплатеид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Глобальный уникальный идентификатор шаблона начальное значений переменных, связанных с безопасной загрузкой UEFI.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифивиртуалсистем**](https://www.bing.com/search?q=**ModifyVirtualSystem**) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

**снапшотдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**суспенддатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся сведения о приостановке виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**свапфиледатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся файлы подкачки для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**усерснапшоттипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает определяемый пользователем тип моментального снимка.

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** (2)


</dt> <dd>

Отключить создание моментального снимка.

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**Продуктионфаллбакктотест** (3)


</dt> <dd>

Моментальный снимок, совместимый с данными, для использования в рабочей среде. Выполняет моментальный снимок с состоянием приложения, если возможность создания моментального снимка с одинаковыми данными недоступна.

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**Продуктионнофаллбакк** (4)


</dt> <dd>

Моментальный снимок, совместимый с данными, для использования в рабочей среде. Не создает моментальный снимок с состоянием приложения, если невозможно создать моментальный снимок с одинаковыми данными.

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (5)


</dt> <dd>

Моментальный снимок, который содержит сведения о памяти и устройстве для целей тестирования и разработки.

</dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Версия виртуальной машины в формате "основной. дополнительный", например "2,0".

</dd> <dt>

**виртуалнумаенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**мсвм \_ процессорсеттингдата**](msvm-processorsettingdata.md).**Макспроцессорспернуманоде**","[**мсвм \_ меморисеттингдата**](msvm-memorysettingdata.md).**Максмемориблоккспернуманоде**")
</dt> </dl>

**Значение true** , если виртуальные узлы неоднородного доступа к памяти (NUMA) проецируются в виртуальную машину; **Значение false** , если виртуальная машина будет иметь один узел. Если **значение — true**, количество ВИРТУАЛЬНЫХ узлов NUMA, проецируемых в виртуальную машину, определяется значениями свойств [**Мсвм \_ Процессорсеттингдата. макспроцессорспернуманоде**](msvm-processorsettingdata.md) и [**мсвм \_ меморисеттингдата. максмемориблоккспернуманоде**](msvm-memorysettingdata.md) .

</dd> <dt>

**виртуалсистемидентифиер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ виртуалсистемсеттингдата. виртуалсистемидентифиер"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")
</dt> </dl>

Имя объекта [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , которому принадлежат данные этого параметра. Это свойство является переопределением из [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Допустимыми значениями для этого свойства являются Microsoft: Hyper-V: подтип: 1 и Microsoft: Hyper-V: подтип: 2. Виртуальная машина поколения 1 имеет подтип 1. Виртуальная машина поколения 2 имеет подтип 2.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-v: подтип: 1** ("Microsoft: Hyper-V: подтип: 1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-v: подтип: 2** ("Microsoft: Hyper-V: подтип: 2")


</dt> <dd></dd> </dl>

</dd> <dt>

**виртуалсистемтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип виртуальной машины, которую представляют данные параметров. Это свойство наследуется от класса [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) . Это может быть одно из следующих значений.



| Значение                                                                                                                                 | Значение                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>"Microsoft: Hyper-V: System: Реализовано"</dt> </dl>                        | Реализованная виртуальная машина.<br/>               |
| <dl> <dt>"Microsoft: Hyper-V: система: запланировано"</dt> </dl>                         | Запланированная виртуальная машина.<br/>                |
| <dl> <dt>"Microsoft: Hyper-V: моментальный снимок: реализован"</dt> </dl>                      | Моментальный снимок реализованной виртуальной машины.<br/> |
| <dl> <dt>"Microsoft: Hyper-V: моментальный снимок: восстановление"</dt> </dl>                      | Моментальный снимок виртуальной машины восстановления.<br/> |
| <dl> <dt>"Microsoft: Hyper-V: моментальный снимок: запланированный"</dt> </dl>                       | Моментальный снимок запланированной виртуальной машины.<br/>  |
| <dl> <dt>"Microsoft: Hyper-V: моментальный снимок: отсутствует"</dt> </dl>                       | Отсутствует моментальный снимок.<br/>                       |
| <dl> <dt>"Microsoft: Hyper-V: моментальный снимок: Реплика: Стандартный"</dt> </dl>              | Моментальный снимок точки репликации на основе времени.<br/>  |
| <dl> <dt>"Microsoft: Hyper-V: моментальный снимок: Реплика: Аппликатионконсистент"</dt> </dl> | Моментальный снимок точки репликации VSS.<br/>         |
| <dl> <dt>"Microsoft: Hyper-V: моментальный снимок: Реплика: Планнедфаиловер"</dt> </dl>       | Плановый моментальный снимок репликации.<br/>           |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ виртуалсистемсеттингдата мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[Классы виртуальных систем](virtual-system-classes.md)
</dt> </dl>

 

