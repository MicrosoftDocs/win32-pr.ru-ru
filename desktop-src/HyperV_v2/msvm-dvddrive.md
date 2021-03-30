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
# <a name="msvm_dvddrive-class"></a>\_Класс мсвм двддриве

Представляет DVD-дисковод в виртуальной машине. Этот DVD-дисковод может быть транзитным (если физический жесткий диск был подключен к виртуальной машине) или искусственным и заполнен ISO-файлом носителя. Так как виртуальные и физические DVD-дисководы можно добавлять и удалять с виртуальной машины, существует два пула ресурсов, связанных с этим классом, один для транзитных DVD-дисков, а другой — для виртуальных DVD-дисководов. DVD-дисководы можно добавлять или удалять только в том случае, если виртуальная машина находится в автономном режиме.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **мсвм \_ двддриве** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ двддриве** содержит следующие методы.



| Метод                                                         | Описание                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| **енабледевице**                                               | Этот метод не поддерживается.<br/> |
| [**локкмедиа**](msvm-dvddrive-lockmedia.md)                   | Блокирует или освобождает носитель.<br/>  |
| **онлинедевице**                                               | Этот метод не поддерживается.<br/> |
| **куиесцедевице**                                              | Этот метод не поддерживается.<br/> |
| [**Равен**](msvm-dvddrive-requeststatechange.md) | Запрашивает изменение состояния.<br/>      |
| [**Перезапуск**](msvm-dvddrive-reset.md)                           | Сбрасывает виртуальное устройство.<br/>    |
| **ресторепропертиес**                                          | Этот метод не поддерживается.<br/> |
| **савепропертиес**                                             | Этот метод не поддерживается.<br/> |
| **SetPowerState**                                              | Этот метод не поддерживается.<br/> |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ двддриве** имеет следующие свойства.

<dl> <dt>

**аддитионалаваилабилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Любая дополнительная доступность и состояние устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение 6 (неприменимо).

</dd> <dt>

**Доступность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Первичная доступность и состояние устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение 6 (неприменимо).

</dd> <dt>

**аваилаблерекуестедстатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния. Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) . Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния. Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.

Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Тип данных: массив **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возможности устройства доступа к носителю. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)и задается для следующих значений.



| Значение                                                                             | Значение                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>{3, 7}</dt> </dl> |                                                                                                 |
| <dl> <dt>3</dt> </dl>      | Соответствующая запись в **капабилитидескриптионс** — "случайный доступ".<br/>            |
| <dl> <dt>7</dt> </dl>      | Соответствующая запись в **капабилитидескриптионс** — "поддерживает съемные носители".<br/> |



 

</dd> <dt>

**капабилитидескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк произвольной формы, который содержит подробные объяснения для доступа к функциям устройств, указанным в массиве свойств **capabilities** . Каждая запись этого массива связана с записью в массиве свойств **capabilities** , расположенной по тому же индексу. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**коммуникатионстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает способность инструментирования взаимодействовать с базовым управляемым элементом. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**компрессионмесод**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, указывающая алгоритм или средство, используемые для сжатия логического файла. Если схема сжатия неизвестна или не описана, используйте "Unknown". Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый". Если логический файл не сжат, используйте параметр NOT сжатый. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

"Не сжато"

Неизвестный

Сжатия

"Не сжато"

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

</dd> <dt>

**дефаултблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Размер блока по умолчанию для устройства (в байтах). Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополняет свойство **примаристатус** дополнительными сведениями о состоянии. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение «Microsoft:*GUID* \\ *устройства-данные*».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**енабледдефаулт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конфигурация по умолчанию или запуска администратора для включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включенные и отключенные состояния элемента. Он также может указывать на переходы между этими запрошенными состояниями. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**еррорклеаред**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, была ли отменена ошибка, сообщаемая в **ластерроркоде** . Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**еррормесодологи**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая типы обнаружения ошибок и исправления, поддерживаемые этим устройством. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**форматссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Форматы компакт-дисков и DVD-дисков, поддерживаемые этим устройством. Это свойство наследуется от [**CIM \_ двддриве**](/previous-versions//cc136812(v=vs.85)).

Этот массив содержит следующие значения для ISO.

<dl> <dt>

{16, 22}
</dt> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>**Компакт-** диск (16)
</dt> <dt>

<span id="DVD"></span><span id="dvd"></span>**DVD-диск** (22)
</dt> </dl>

Этот массив содержит следующие значения для физического сквозного передачи.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>**Компакт-** диск (16)
</dt> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)
</dt> <dt>

<span id="CD-I"></span><span id="cd-i"></span>**Компакт-I** (18)
</dt> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**Записываемый компакт-диск** (19)
</dt> <dt>

<span id="DVD"></span><span id="dvd"></span>**DVD-диск** (22)
</dt> <dt>

<span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW +** (23)
</dt> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)
</dt> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)
</dt> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-видео** (26)
</dt> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Дивкс** (27)
</dt> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)
</dt> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)
</dt> <dt>

<span id="CD_"></span><span id="cd_"></span>**CD +** (35)
</dt> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**Записываемый DVD-диск** (36)
</dt> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)
</dt> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**Аудио DVD** (38)
</dt> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)
</dt> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)
</dt> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)
</dt> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)
</dt> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущая работоспособность элемента. Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов. Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк произвольной формы, предоставляющих объяснения и подробные сведения, лежащие в основе записей в массиве свойств **осеридентифингинфо** . Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания конфигурации виртуальной машины. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ластклеанед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время последней очистки устройства. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**ластерроркоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последний код ошибки, сообщаемый логическим устройством. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**лоадтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время в миллисекундах от "Load" до возможности чтения или записи мультимедиа. Например, для дисков это интервал между диском, который не передается на диск, сообщает, что он готов для чтения и записи (т. е. диск вращается с номинальной скоростью). Для ленточных накопителей это время с носителя, добавляемого для сообщения о готовности к работе для приложения. Обычно это в области BOT ленты. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**максакцесстиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время (в миллисекундах) перехода с первого места на носителе к расположению, которое находится в самом начале относительно времени. Для дискового накопителя это соответствует полной и полной задержке при повороте. Для ленточных накопителей этот элемент представляет собой поиск с начала ленты до наиболее физической отдаленной точки. (Конец ленты может находиться в самой физической точке, но это не обязательно верно). Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**максблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный размер блока в байтах для носителя, доступного устройству. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**максмедиасизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах). Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024). Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**макскуиесцетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство использовать не рекомендуется. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**максунитсбефореклеанинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное число единиц, которое можно использовать до очистки устройства. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**медиаислоккед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** , если носитель заблокирован на устройстве и не может быть извлечен. в противном случае — **значение false**. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**минблокксизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный размер блока (в байтах) для носителя, доступного устройству. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**маунткаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Для устройства, которое поддерживает съемные носители, число подключенных носителей для передачи данных или очистки устройства. Для устройств, обращающихся к несъемным носителям, например к жестким дискам, это свойство неприменимо и должно иметь значение 0. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка, по которой известен объект. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .

</dd> <dt>

**нидсклеанинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** , если устройству доступа к носителю требуется очистка; в противном случае — **значение false**. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**нумберофмедиасуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное количество отдельных носителей, которые могут быть поддерживаются или вставлены. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**оператингстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** . Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**осеренабледстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние включения или отключения элемента, если свойство **EnabledState** имеет значение 1 (другое). Это свойство должно иметь значение **null** , если свойство **EnabledState** имеет любое значение, отличное от 1. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополнительные данные, кроме сведений об ИДЕНТИФИКАТОРах устройств, которые можно использовать для идентификации логического устройства. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели и имеет значение **null**.

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возможности управления питанием устройства. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**поверманажементсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли управлять питанием устройства. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**поверонхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**примаристатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о состоянии высокого уровня. Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последнее запрошенное или требуемое состояние элемента. Фактическое состояние элемента представлено свойством **EnabledState** . Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния. Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать метод **RequestStateChange** . В этом случае используется значение 12 (неприменимо). Это свойство наследуется от **CIM \_ енабледлогикалелемент**.

</dd> <dt>

**Безопасность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Операционная безопасность, определенная для устройства. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.

</dd> <dt>

**статусдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строки, описывающие различные значения массива **OperationalStatus** . Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние логического устройства. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса создания системы области. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор для области виртуальной машины. Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

</dd> <dt>

**тимеофластмаунт**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Для устройства, которое поддерживает съемные носители, последняя Дата и время подключения носителя к устройству. Для устройств, обращающихся к несъемным носителям, например жестким дискам, это свойство не имеет смысла и неприменимо. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**тимеофластстатечанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата или время последнего изменения включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**тоталмаунттиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Для устройства, которое поддерживает съемные носители, общее время (в секундах) подключения носителя для передачи данных или очистки устройства. Для устройств, обращающихся к несъемным носителям, например к жестким дискам, это свойство неприменимо и должно иметь значение 0. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**тоталповеронхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее количество часов, в течение которых устройство было включено. Это свойство наследуется от [**CIM \_ -,**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)но не используется.

</dd> <dt>

**транситионингтостате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает целевое состояние, в которое переходит экземпляр. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не используется.

</dd> <dt>

**ункомпресседдатарате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Постоянная скорость передачи данных (в КБ/с), которую устройство может читать и записывать на носитель. Это постоянная скорость необработанных данных. В этом свойстве не следует сообщать о максимальных тарифах или тарифах, имеющих значение сжатия. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**унитсдескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Единицы измерения относительно его использования в **максунитсбефореклеанинг**. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**унитсусед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее количество используемых единиц. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**унлоадтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время в миллисекундах от возможности чтения или записи носителя в его выгрузку. Это свойство наследуется от [**CIM \_ медиаакцессдевице**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ двддриве мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ДВДДРИВЕ CIM**](cim-dvddrive.md)
</dt> <dt>

[**\_ДВДДРИВЕ CIM**](/previous-versions//cc136812(v=vs.85))
</dt> <dt>

[Классы хранения](storage-classes.md)
</dt> </dl>

 

