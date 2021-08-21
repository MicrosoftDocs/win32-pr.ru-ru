---
description: Представляет программное обеспечение низкого уровня, которое загружается в ОЗУ для настройки и запуска системы.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Класс Msvm_BIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8433c8fda6d438e4f77fb763be42467aab05ab976927f018e895a30d5f9c6226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149304"
---
# <a name="msvm_bioselement-class"></a>\_Класс мсвм биоселемент

Представляет программное обеспечение низкого уровня, которое загружается в ОЗУ для настройки и запуска системы. BIOS не является логическим устройством, поэтому виртуальная BIOS не должна рассматриваться как устройство виртуальной машины. Так как устройство не является устройством, оно не имеет соответствующего пула ресурсов. Объект BIOS связан с виртуальной машиной через ассоциацию [**мсвм \_ систембиос**](msvm-systembios.md) .

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ биоселемент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ биоселемент** имеет следующие свойства.

<dl> <dt>

**басебоардсериалнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Серийный номер для основной платы на виртуальной машине.

</dd> <dt>

**биосгуид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор BIOS.

</dd> <dt>

**биоснумлокк**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включенное состояние NUM LOCK в BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Серийный номер BIOS.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Порядок, в котором устройства будут искать загрузочный сектор при запуске.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Внутренний идентификатор для этой компиляции программного элемента. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение 14.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**чассисассеттаг**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Автоматически заполняется BIOS при создании виртуальной машины.

</dd> <dt>

**чассиссериалнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Автоматически заполняется BIOS при создании виртуальной машины.

</dd> <dt>

**Исходный код**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Набор кодов, используемый программным элементом. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение **null**.

</dd> <dt>

**коммуникатионстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает способность инструментирования взаимодействовать с базовым управляемым элементом. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**куррентлангуаже**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Выбранный в данный момент язык для BIOS. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение "en \| US \| ISO8859-1".

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

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя элемента. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает текущую работоспособность элемента. Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.

При возникновении критической ошибки просмотрите подробные сведения в журнале событий. Свойство **EnabledState** также может содержать дополнительные сведения. Например, если место на диске критически низкий, значение **HealthState** равно 25, виртуальная машина будет приостановлена, а параметру **EnabledState** будет присвоено значение 32768 (приостановлено).

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Значение                                                                                                                                                                                                                                                            | Значение                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**ОК**</dt> <dt>5</dt> </dl>                                                                               | Виртуальная машина полностью работоспособна и работает в нормальных рабочих параметрах и без ошибок.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Серьезный сбой**</dt> <dt>20</dt> </dl>             | Произошла серьезная ошибка виртуальной машины. Это значение используется, когда на одном или нескольких дисках, содержащих виртуальные жесткие диски виртуальной машины, недостаточно места на диске, а виртуальная машина приостановлена.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Критический сбой**</dt> <dt>25</dt> </dl> | Элемент нефункциональный, и восстановление может быть невозможным. Это может означать, что рабочий процесс для виртуальной машины (Vmwp.exe) не отвечает на запросы контроля или информации или что на одном или нескольких дисках, содержащих виртуальные жесткие диски виртуальной машины, недостаточно места на диске.<br/> |



 

</dd> <dt>

**идентификатионкоде**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Идентификатор изготовителя для этого программного элемента. Часто это будет единицей складского учета (SKU) или номером части. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Автоматически заполняется BIOS при создании виртуальной машины. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

**лангуажеедитион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (32)
</dt> </dl>

Языковой выпуск этого программного элемента. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение **null**.

</dd> <dt>

**листофлангуажес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список устанавливаемых языков для BIOS. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение "en \| US \| ISO8859-1".

</dd> <dt>

**лоадедендингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **unit64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конечный адрес памяти, которую занимает эта BIOS. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение 0xFFFFF.

</dd> <dt>

**лоадедстартингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **unit64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Начальный адрес памяти, которую занимает эта BIOS. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение 0xE0000.

</dd> <dt>

**лоадутилитинформатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая программу BIOS Flash/Load, необходимую для обновления элемента BIOS. В этом свойстве могут быть указаны версия и другие сведения. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение **null**.

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (256)
</dt> </dl>

Производитель этой BIOS. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение "Корпорация Майкрософт".

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (1024)
</dt> </dl>

Имя, используемое для обнаружения этого программного элемента. При создании подклассов это свойство может быть переопределено как свойство ключа. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение "BIOS".

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

Массив, содержащий текущие состояния объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement). Значение с нулевым индексом (0) является одним из следующих значений.



| Значение                                                                                                                                                                                                                                                                   | Значение                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**ОК**</dt> <dt>2</dt> </dl>                                                                                      | Виртуальная машина работоспособна и работает нормально.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Снижение уровня работоспособности**</dt> <dt>3</dt> </dl>                                         | Виртуальная машина работает только частично. Это означает, что хранилище, которое содержит конфигурацию, недоступно. Виртуальная машина в этом состоянии может быть выключена или удалена. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Прогнозный сбой**</dt> <dt>5</dt> </dl> | Виртуальная машина работоспособна, но может завершиться с ошибкой в будущем. Это означает, что недостаточно свободного места в хранилище, содержащем виртуальный жесткий диск виртуальной машины. Виртуальная машина будет приостановлена, если свободное место на диске не станет доступным.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Остановлено**</dt> <dt>10</dt> </dl>                                            | Это значение не поддерживается. Если виртуальная машина остановлена, свойство **EnabledState** будет иметь значение 3 (отключено).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**В службе**</dt> <dt>11</dt> </dl>                                | Виртуальная машина обрабатывает запрос.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Неактивность**</dt> <dt>15</dt> </dl>                                            | Это значение не поддерживается. Если виртуальная машина приостановлена или приостановлена, свойство **EnabledState** будет иметь значение 32769 (приостановлено) или 32768 (приостановлено).<br/>                                                                                    |



 

Значение с индексом 1 является необязательным и содержит дополнительные сведения о состоянии. Клиент должен использовать первичное состояние из нулевого индекса (0), чтобы определить, может ли новый запрос выдаться виртуальной машине. Если значение **OperationalStatus** \[ 0 \] равно 2 (ОК), операция, указанная в **OperationalStatus** \[ 1, \] может быть прервана.

Значение в **OperationalStatus** \[ 1 \] имеет одно из следующих значений.



| Значение                                                                                                                                                                                                                                                                                                   | Значение                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Создание моментального снимка**</dt> <dt>32768</dt> </dl>                                 | Моментальный снимок находится в процессе создания для виртуальной машины.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Применение моментального снимка**</dt> <dt>32769</dt> </dl>                                 | Моментальный снимок находится в процессе применения к виртуальной машине.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Удаление моментального снимка**</dt> <dt>32770</dt> </dl>                                 | Моментальный снимок находится в процессе удаления из виртуальной машины.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**Ожидание запуска**</dt> <dt>32771</dt> </dl>                                     | Виртуальная машина будет запущена после истечения интервала автоматической загрузки.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Слияние дисков**</dt> <dt>32772</dt> </dl>                                                 | Выполняется слияние виртуальных жестких дисков из ранее удаленных моментальных снимков.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Экспорт виртуальной машины**</dt> <dt>32773</dt> </dl> | Выполняется экспорт виртуальной машины.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Миграция виртуальной машины**</dt> <dt>32774</dt> </dl> | Виртуальная машина переносится с одного физического компьютера на другой.<br/>  |



 

</dd> <dt>

**осертаржетос**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Изготовитель и операционная система для программного элемента, если свойство **таржетоператингсистем** имеет значение 1 (другое), которое требует, чтобы свойство **осертаржетос** имело значение, отличное от **null** . Для всех остальных значений **таржетоператингсистем** свойство **Осертаржетос** должно иметь **значение NULL**. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение **null**.

</dd> <dt>

**примарибиос**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если значение равно true, это основная BIOS компьютерной системы. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение **true**.

</dd> <dt>

**примаристатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о состоянии высокого уровня. Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**регистрюрис**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк, представляющий расположение публикации реестра атрибутов BIOS или реестров, которым соответствует реализация. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата выпуска BIOS. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**Номер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Назначенный серийный номер BIOS. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement).

</dd> <dt>

**софтварилементид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (256)
</dt> </dl>

Идентификатор программного элемента. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение "Microsoft:*GUID* \\ *, зависящие от устройства*".

</dd> <dt>

**софтварилементстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние жизненного цикла программного элемента. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение 2 (исполняемый объект).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.

</dd> <dt>

**статусдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **arrayType** ("индексированный")
</dt> </dl>

Массив, содержащий строки, описывающие соответствующие значения массива **OperationalStatus** . Например, если 11 (в службе) — значение, назначенное для **OperationalStatus** \[ 0 \] , то **статусдескриптионс** \[ 0 \] может содержать объяснение, почему виртуальная машина обрабатывает запрос. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**таржетоператингсистем**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Среда операционной системы элемента. Это свойство наследуется от [**CIM \_ софтварилемент**](/windows/desktop/CIMWin32Prov/cim-softwareelement)и всегда имеет значение 0 (неизвестно).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Версия BIOS. Это свойство наследуется от [**CIM \_ биоселемент**](/windows/desktop/CIMWin32Prov/cim-bioselement)и всегда имеет значение "8.02.00".

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ биоселемент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_БИОСЕЛЕМЕНТ CIM**](cim-bioselement.md)
</dt> <dt>

[Классы BIOS](bios-classes.md)
</dt> <dt>

[**\_БИОСЕЛЕМЕНТ CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

