---
description: Представляет задание, созданное с помощью команды AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Класс Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072377"
---
# <a name="win32_scheduledjob-class"></a>\_Класс Win32 ScheduledJob

 [Класс WMI](../wmisdk/retrieving-a-class.md) **\_ ScheduledJob для Win32**   представляет задание, созданное с помощью команды **at** .

> [!Note]  
> Класс **Win32 \_ ScheduledJob** не представляет задание, созданное с помощью мастера запланированных заданий, из панели управления. Задачу, созданную WMI, нельзя изменить в пользовательском интерфейсе запланированных задач. Дополнительные сведения см. в разделе "Замечания".

 

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ ScheduledJob** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ ScheduledJob** содержит следующие методы.



| Метод                                                      | Описание                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Создания**](create-method-in-class-win32-scheduledjob.md) | Метод класса, который отправляет задание в операционную систему для выполнения в указанное будущее время и дату.<br/> |
| [**Удалить**](delete-method-in-class-win32-scheduledjob.md) | Метод класса, который удаляет запланированное задание.<br/>                                                                 |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ ScheduledJob** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Команда**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| ")
</dt> </dl>

Имя команды, пакетной программы или двоичного файла (и аргументы командной строки), которые служба расписаний использует для вызова задания.

Пример: "**Defrag** **/к/ф**"

</dd> <dt>

**DaysOfMonth**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетью Win32API \| [**по \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**")
</dt> </dl>

Дни месяца, в которые запланировано выполнение задания. Если задание планируется запускать в несколько дней месяца, эти значения можно объединить в логическое или. Например, если задание выполняется в первый и в 16-й день каждого месяца, значение свойства **DaysOfMonth** будет равно 1 или 32768.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

-

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

ое

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

3-й

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

4-й

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

го

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

шестую

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

7

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

ВОСЬМ

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

го

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

Конференции

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

11th

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

12th

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

13th

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

14

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

15

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

й

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

17

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

18

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

й

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

заказан

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

21st

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

22nd

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

23rd

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

24

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

ая

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

26th

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

27

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

28

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

29

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

30

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

м

</dd> </dl>

</dd> <dt>

**DaysOfWeek**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетью Win32API \| [**по \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")
</dt> </dl>

Дни недели, в которые запланировано выполнение задания. Если задание запланировано на несколько дней недели, значения можно объединить в логическую или. Например, если задание планируется запускать в понедельниках, по средам и пятницу, значение свойства **DaysOfWeek** будет равно 1 или 4 или 16.

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Понедельник** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Вторник** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Среда** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Четверг** (8)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Пятница** (16)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Суббота** (32)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Воскресенье** (64)


</dt> <dd></dd> </dl>

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
</dt> </dl>

Текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**елапседтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время выполнения задания.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Указывает, когда был установлен объект. Отсутствие значения не означает, что объект не установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**интерактвисдесктоп**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures On \| [**\_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **flags** \| **Job \_ uninteractive**")
</dt> </dl>

Указанное задание является интерактивным. Это означает, что пользователь может предоставить входные данные для запланированного задания во время его выполнения.

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетью Win32API \| [**в \_ перечислении**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JOBID**")
</dt> </dl>

Идентификатор задания. Он используется методами в качестве маркера для одного задания, запланированного на этом компьютере.

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры управления \| [**при \_ перечислении**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **flags** \| **Job \_ \_ Error**")
</dt> </dl>

Состояние выполнения при последнем запланированном запуске этого задания.

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

**Успешно** ("успешно")


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

**Сбой** ("сбой")


</dt> <dd></dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")
</dt> </dl>

Метка, по которой известен объект. При создании подклассов это свойство может быть переопределено как свойство ключа.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Уведомление**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Пользователь получает уведомление о завершении задания или сбое.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**Владелец**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Пользователь, отправивший задание.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Важность выполнения задания.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**рунрепеатедли**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетями Win32API \| [**по \_ сведениям**](/windows/win32/api/lmat/ns-lmat-at_info). \|  \| **Задание \_ выполняется \_ периодически**")
</dt> </dl>

Запланированное задание выполняется несколько раз в дни, когда запланировано задание. Если задано **значение false**, задание выполняется один раз.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры управления сетью Win32API \| [**в \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **жобтиме**")
</dt> </dl>

Время выполнения задания в формате UTC в виде "YYYYMMDDHHMMSS". ММММММ (+-) OOO ", где" ГГГГММДД "должен быть заменен на" \* \* \* \* \* \* \* \* ". Замена необходима, так как служба планирования позволяет настраивать задания только один раз или запускать в день месяца или недели. Задание не может выполняться в указанную дату.

Раздел "(+-) OOO" в значении свойства **StartTime** является текущим смещением для локального преобразования времени. Смещение — это разница между временем в формате UTC и местным временем. Чтобы вычислить смещение для часового пояса, умножьте число часов, в течение которых часовой пояс составляет вперед или выше среднего времени по Гринвичу (GMT) на 60 (Используйте положительное число в часах, если часовой пояс находится впереди GMT и отрицательное число, если часовой пояс находится за GMT). Добавьте дополнительные 60 к вычислению, если часовой пояс использует летнее время. Например, тихоокеанское стандартное часовое пояса составляет восемь часов после GMT, поэтому он равен-420 (-8 \* 60 + 60) при использовании летнего времени и-480 (-8 \* 60), если летнее время не используется. Можно также определить значение смещения, запросив свойство смещения класса [**\_ часового пояса Win32**](win32-timezone.md) .

Например: " \* \* \* \* \* \* \* \* 123000.000000-420" указывает 14,30 (2:30 вечера) PST, в котором действует летнее время.

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Строка, указывающая текущее состояние объекта. Можно определить операционное и нерабочее состояние. Оперативное состояние может включать "ОК", "деградация" и "пред Fail". "Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).

Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание". "Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.

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

**тимесубмиттед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время отправки задания.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**унтилтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время, когда задание является недопустимым или должно быть остановлено.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Каждое задание, запланированное для службы расписания, хранится постоянно (планировщик может запустить задание после перезагрузки) и выполняется в указанное время и день недели или месяца. Если компьютер неактивен или запланированная служба не запущена в указанное время, служба расписаний запускает указанное задание в следующий день в указанное время.

Задания планируются в соответствии со временем в формате UTC с смещением смещения от среднего времени по Гринвичу (GMT). Это означает, что задание можно указать с помощью любого часового пояса. Класс **Win32 \_ ScheduledJob** Возвращает местное время со СМЕЩЕНИЕМ в формате UTC при перечислении объекта и преобразует его в местное время при создании заданий. Например, задание, указанное для запуска на компьютере в Бостоне в 10:30 P.M. Время работы с графиком в понедельник будет запланировано локально в 1:30 утра. Вторник, средство EST.

> [!Note]  
> Клиент должен учитывать, выполняется ли летнее время на локальном компьютере, и, если это так, вычтите смещение в 60 минут от смещения UTC.

 

Класс **Win32 \_ ScheduledJob** является производным от [**\_ задания CIM**](cim-job.md). Для создания запланированного задания с помощью этого класса необходимо быть членом группы "Администраторы".

Класс **Win32 \_ ScheduledJob** внутренне использует протокол AT, который привязан к устаревшим данным, начиная с Windows 8 и Windows Server 2012. В качестве первого шага по умолчанию протокол AT отключен. Если протокол отключен, например вызов метода [**CREATE**](create-method-in-class-win32-scheduledjob.md) для объекта **Win32 \_ ScheduledJob** , произойдет сбой с ошибкой 0x8. Можно включить по протоколу обратно, добавив следующую запись реестра:

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

Возможно, потребуется перезагрузить компьютер, чтобы сделать этот параметр эффективным.

Поскольку **Win32 \_ ScheduledJob** основан на API Win32 [**нетсчедулежобжетинфо**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , этот класс нельзя использовать совместно с планировщик задач. Если вы хотите использовать планировщик задач, используйте API планировщик задач. Дополнительные сведения см. в [справочнике по планировщик задач](../taskschd/task-scheduler-reference.md).

## <a name="examples"></a>Примеры

Следующий пример кода на языке VBScript планирует Notepad.exe запускаться в интерактивном режиме в 1:25 на локальном компьютере каждый понедельник.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Задание CIM**](cim-job.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> <dt>

[Задачи WMI: запланированные задачи](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
