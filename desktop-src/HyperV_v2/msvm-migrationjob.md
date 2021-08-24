---
description: Этот класс представляет задание операции миграции, созданное для миграции хранилища или виртуальной системы с помощью службы миграции виртуальной системы.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Класс Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba979953a9e7a17df70247cdb176cba2f5782d4f9f6fc13d8f4addc161bbaf50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521204"
---
# <a name="msvm_migrationjob-class"></a>\_Класс мсвм мигратионжоб

Этот класс представляет задание операции миграции, созданное для миграции хранилища или виртуальной системы с помощью службы миграции виртуальной системы.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ мигратионжоб** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ мигратионжоб** содержит следующие методы.



| Метод                                                             | Описание                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Ошибка**](geterror-msvm-migrationjob.md)                     | Возвращает объект ошибки для задания миграции, если оно существует.<br/>                |
| [**жетеррорекс**](geterrorex-msvm-migrationjob.md)                 | Возвращает объекты ошибок для задания миграции, если они существуют.<br/>                |
| **киллжоб**                                                        | Этот метод не поддерживается.<br/>                                                   |
| [**Равен**](requeststatechange-msvm-migrationjob.md) | Запрашивает изменение состояния задания миграции на указанное состояние.<br/> |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ мигратионжоб** имеет следующие свойства.

<dl> <dt>

**Отменяемых**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли отменить задание. Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен.

</dd> <dt>

**Caption**
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

**делетеонкомплетион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, следует ли автоматически удалять задание после завершения. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**дестинатионхост**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя узла целевой платформы виртуализации, на которой выполняется миграция виртуальной системы. Это значение будет **равно NULL** для миграции хранилища.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополняет свойство **примаристатус** дополнительными сведениями о состоянии. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**елапседтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Интервал времени, в течение которого выполнялось задание, или общее время выполнения, если задание завершено. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Код ошибки, зависящий от поставщика. Если задание завершилось без ошибок, значение должно быть равно нулю. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, содержащая описание ошибки поставщика. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Задание CIM**](cim-job.md)".**ErrorCode**")
</dt> </dl>

Сводное описание ошибки, если оно есть.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущая работоспособность элемента. Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов. Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.

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

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.

</dd> <dt>

**жобрунтимес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество запусков задания. Значение 1 указывает, что задание не повторяется, а любое ненулевое значение указывает на ограничение на количество повторений задания. Ноль указывает, что количество операций, которые может обработать задание, не ограничено, но оно будет завершено либо после достижения **унтилтиме** , либо после того, как задание будет прервано вручную. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**JobState** — это целочисленное перечисление, указывающее операционное состояние задания. Он также может указывать на переходы между этими состояниями, например "завершение работы" и "Запуск". Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).



| Значение                                                                                                                                                                                                                                                                 | Значение                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <dt>**Новое**</dt> <dt>2</dt> </dl>                                                           | Задание никогда не запускалось.<br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Начиная**</dt> с <dt>3</dt> </dl>                                       | Задание переходит из состояния 2 (новое), 5 (приостановлено) или 11 (служба) в состояние 4 (работает).<br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <dt>**Выполнение**</dt> <dt>4</dt> </dl>                                           | Задание выполняется.<br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <dt>**Приостановлено**</dt> <dt>5</dt> </dl>                                   | Задание остановлено, но его можно легко перезапустить.<br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Завершение работы**</dt> <dt>6</dt> </dl>                   | Задание переходит в состояние 7 (завершено), 8 (завершено) или 9 (прервано).<br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <dt>**Завершено**</dt> <dt>7</dt> </dl>                                   | Задание выполнено нормально.<br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <dt>**Завершено**</dt> <dt>8</dt> </dl>                               | Задание остановлено запросом на изменение состояния "завершено". Задание и все его базовые процессы завершены и могут быть перезапущены только в качестве нового задания. Требование перезапуска задания только в том случае, если задано новое задание.<br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <dt>**Уничтожено**</dt> <dt>9</dt> </dl>                                               | Задание остановлено запросом на изменение состояния "Kill". Базовые процессы могут по-прежнему выполняться, а для освобождения ресурсов может потребоваться очистка.<br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <dt>**Исключение**</dt> <dt>10</dt> </dl>                                  | Задание находится в ненормальном состоянии, что может указывать на состояние ошибки. Фактическое состояние задания может быть доступно через объекты конкретного задания.<br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <dt>**Служба**</dt> <dt>11</dt> </dl>                                          | Задание находится в состоянии, зависящем от поставщика, которое поддерживает обнаружение проблем, разрешение или и то, и другое.<br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**Зарезервировано**</dt> <dt>12 32767</dt> в формате DMTF </dl>            | Зарезервировано.<br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Поставщик Зарезервированный**</dt> <dt>32768 65535</dt> </dl> | Зарезервировано.<br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, представляющая состояние задания. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**JobType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип задания, отслеживаемого этим объектом.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

**Создание удаленной виртуальной машины** (300)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

**Проверка совместимости виртуальной машины** (301)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

**проверка совместимости виртуальной машины и служба хранилища** (302)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

**проверка совместимости служба хранилища** (303)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

**проверка служба хранилища миграции** (304)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

**Перемещение виртуальной машины** (305)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

**перемещение виртуальной машины и служба хранилища** (306)


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

**перемещение служба хранилища** (307)


</dt> <dd></dd> </dl>

</dd> <dt>

**локалорутктиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

Указывает, представляют ли значения времени, представленные в свойствах **рунстартинтервал** и **унтилтиме** , местное время или время в формате UTC.

<dl> <dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Местное время** (1)
</dt> <dt>

<span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Время в формате UTC** (2)
</dt> </dl>

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**мсвм \_ виртуалсистеммигратионсеттингдата**](msvm-virtualsystemmigrationsettingdata.md).**Мигратионтипе**")
</dt> </dl>

Тип миграции, представленный этим объектом задания. Это будет одно из значений, определенных для свойства **мигратионтипе** класса [**\_ виртуалсистеммигратионсеттингдата мсвм**](msvm-virtualsystemmigrationsettingdata.md) .

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Отображаемое имя для этого экземпляра задания. Кроме того, отображаемое имя можно использовать в качестве свойства для поиска или запроса. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**невресаурцесеттингдата**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Для динамической миграции всегда будет задано **значение NULL**.

Если для миграции хранилища задано **значение NULL**, то ни один из виртуальных жестких дисков виртуальной машины не будет перемещен. В противном случае он будет содержать массив внедренных экземпляров класса [**мсвм \_ сторажеаллокатионсеттингдата**](msvm-storageallocationsettingdata.md) , представляющих виртуальные жесткие диски для перемещения. В свойстве **Connection** этих экземпляров будет указано целевое расположение виртуального жесткого диска.

</dd> <dt>

**невсистемсеттингдата**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Для динамической миграции всегда будет задано **значение NULL**.

Для миграции хранилища, если это значение равно **null**, корни данных виртуальной машины не перемещаются. В противном случае он будет содержать встроенный экземпляр класса [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md) , где свойства **Екстерналдатарут**, **снапшотдатарут** и **свапфиледатарут** будут указывать новые корни данных.

</dd> <dt>

**Уведомление**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Пользователь, который получает уведомление о завершении задания или сбое. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

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

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).

</dd> <dt>

**осеррековеряктион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая действие восстановления, если свойство **рековеряктион** экземпляра имеет значение 1 (другое). Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**Владелец**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Пользователь, отправивший задание. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **MinValue** (0), **MaxValue** (100), **единицы** ("процент")
</dt> </dl>

Процент завершения задания. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**примаристатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о состоянии высокого уровня. Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Важность выполнения задания. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**рековеряктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описывает действие восстановления, которое необходимо выполнить для неуспешного выполнения задания. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Не продолжать** (2)
</dt> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Перейти к следующему заданию** (3)
</dt> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Повторно запустить задание** (4)
</dt> <dt>

<span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Запустить задание восстановления** (5)
</dt> </dl>

</dd> <dt>

**рундай**
</dt> <dd> <dl> <dt>

Тип данных: **sint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **MinValue** (-31), **MaxValue** (31)
</dt> </dl>

День месяца, в который должно быть обработано задание. Для этого свойства существуют различные интерпретации в зависимости от значения **рундайофвик**.

Если **рундайофвик** имеет значение 0, а **рундай** является положительным, **рундай** определяет день месяца, в котором обработано задание. Например, если **рундайофвик** имеет значение 0, а **рундай** — 12, задание будет обработано на 12-<sup>й</sup> день месяца.

Если **рундайофвик** имеет значение 0, а **рундай** имеет отрицательное значение, **рундай** определяет число дней до последнего дня месяца, в котором обработано задание.  1 указывает последний день месяца, 2 — один день до последнего дня месяца и т. д. Например, если **рундайофвик** имеет значение 0, а **рундай** — значение 1, задание будет обрабатываться в последний день месяца.

Если **рундайофвик** не равен 0, **рундайофвик** — это день недели, в который будет обработано задание, относительно **рундай**. Например, если **рундай** имеет значение 15, а **рундайофвик** — 7 (+ Суббота), задание будет обработано в первую субботу в или после 15-<sup>го</sup> дня месяца. Если **рундай** имеет значение 20, а **рундайофвик** — 7 (Суббота), задание будет обработано в первую субботу в течение или до 20-<sup>го</sup> дня месяца. Если **рундай** имеет значение 1, а **рундайофвик** — 1 (воскресенье), задание будет обработано в последнем воскресенье месяца.

Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**рундайофвик**
</dt> <dd> <dl> <dt>

Тип данных: **sint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Положительное или отрицательное целое число, используемое в сочетании с **рундай** для обозначения дня недели или месяца, в котором обрабатывается задание. Дополнительные сведения см. в описании свойства **рундай** . Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

<dl> <dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Суббота** (7)
</dt> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Пятница** (6)
</dt> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Четверг** (5)
</dt> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**Среда** (4)
</dt> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Вторник** (3)
</dt> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Понедельник** (2)
</dt> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**– Воскресенье** (1)
</dt> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**Ексактдайофмонс** (0)
</dt> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Воскресенье** (1)
</dt> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Понедельник** (2)
</dt> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Вторник** (3)
</dt> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Среда** (4)
</dt> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Четверг** (5)
</dt> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Пятница** (6)
</dt> <dt>

<span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Суббота** (7)
</dt> </dl>

</dd> <dt>

**рунмонс**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Месяц, в течение которого должно быть обработано задание. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

<dl> <dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Январь** (0)
</dt> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Февраль** (1)
</dt> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>**Март** (2)
</dt> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>**Апрель** (3)
</dt> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>**Май** (4)
</dt> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>**Июнь** (5)
</dt> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>**Июль** (6)
</dt> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Август** (7)
</dt> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Сентябрь** (8)
</dt> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Октябрь** (9)
</dt> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Ноябрь** (10)
</dt> <dt>

<span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Декабрь** (11)
</dt> </dl>

</dd> <dt>

**рунстартинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Интервал времени после полуночи, когда должно быть обработано задание. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**счедуледстарттиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Запланированное время запуска задания (если применимо). Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время начала задания. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

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
</dt> </dl>

Строки, описывающие различные значения массива **OperationalStatus** . Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".

</dd> <dt>

**тимебефореремовал**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время (в минутах), в течение которого задание сохраняется после завершения выполнения, как успешно, так и в случае сбоя. Задание должно оставаться в наличии в течение некоторого периода времени независимо от значения свойства **делетеонкомплетион** . Значение по умолчанию — пять минут. Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85))и всегда имеет значение 00000000000500.000000:000.

</dd> <dt>

**тимеофластстатечанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата или время последнего изменения состояния задания. Если состояние задания не изменилось и заполнено это свойство, то для него должно быть задано значение 0. Если изменение состояния было запрошено, но отклонено или еще не обработано, свойство не должно обновляться. Это свойство наследуется от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> <dt>

**тимесубмиттед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время отправки задания. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**унтилтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время, когда задание недопустимо или должно быть остановлено. Это свойство наследуется [**от \_ задания CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**виртуалсистемнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальное имя затронутой виртуальной системы.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

