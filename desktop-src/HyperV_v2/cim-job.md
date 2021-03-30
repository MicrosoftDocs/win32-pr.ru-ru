---
description: Логический элемент, представляющий выполняемую единицу работы, например скрипт или задание печати. Задание отличается от процесса, так как задание может быть запланировано или поставлено в очередь, а его выполнение не ограничивается одной системой.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: Класс CIM_Job (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999036"
---
# <a name="cim_job-class-hyper-v-management"></a>Класс CIM_Job (Управление Hyper-V)

Логический элемент, представляющий выполняемую единицу работы, например скрипт или задание печати. Задание отличается от процесса, так как задание может быть запланировано или поставлено в очередь, а его выполнение не ограничивается одной системой.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
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
};
```

## <a name="members"></a>Члены

Класс **\_ заданий CIM** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ заданий CIM** содержит эти методы.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Метод</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="cim-job-killjob.md"><strong>киллжоб</strong></a></td>
<td style="text-align: left;">Этот метод является устаревшим. Вместо этого используйте метод <strong>RequestStateChange</strong> .<br/>
<blockquote>
[!Note]<br />
Нерекомендуемое описание: завершает задание.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Свойства

Класс **\_ заданий CIM** имеет следующие свойства.

<dl> <dt>

**делетеонкомплетион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

**Значение true** , чтобы удалить задание после завершения; в противном случае — **значение false**.

> [!Note]  
> Это свойство не удаляет задания, которые были завершены до того, как это свойство будет установлено в **значение true**.

 

</dd> <dt>

**елапседтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Длительность выполнения задания.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**ErrorDescription**")
</dt> </dl>

Код ошибки, зависящий от поставщика, который фиксирует сведения об обработке повторяющихся заданий. Если задание завершилось без ошибок, значение должно быть равно нулю.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**ErrorCode**")
</dt> </dl>

Строка произвольной формы, содержащая описание соответствующего кода ошибки в свойстве **ErrorCode** .

</dd> <dt>

**жобрунтимес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Количество запусков задания.

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Строка произвольной формы, представляющая состояние задания.

</dd> <dt>

**локалорутктиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, представляют ли значения времени в свойствах **рунстартинтервал** и **унтилтиме** местное время или время в формате UTC.

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

**Местное время** (1)


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

**Время в формате UTC** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Уведомление**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Пользователь, уведомляющий о завершении или сбое задания.

</dd> <dt>

**осеррековеряктион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рековеряктион**")
</dt> </dl>

Строка, описывающая действие восстановления, если свойство **рековеряктион** является **другим** ("1").

</dd> <dt>

**Владелец**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ овнингжобелемент**](cim-owningjobelement.md).")
</dt> </dl>

Пользователь, отправивший задание, или имя службы или метода, запросившего задание.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("процент"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **Пунит** ("процент")
</dt> </dl>

Процент завершенного задания.

> [!Note]  
> Значение "101" не определено и будет запрещено в следующей основной редакции спецификации.

 

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Важность задания. Чем меньше число, тем выше приоритет.

</dd> <dt>

**рековеряктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Осеррековеряктион**")
</dt> </dl>

Описывает действие восстановления, выполняемое при сбое выполнения задания.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd>

Неизвестно, какое действие восстановления будет выполнено.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd>

Действие восстановления будет указано в свойстве **осеррековеряктион** .

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Не продолжать** (2)


</dt> <dd>

Останавливает выполнение задания и соответствующим образом обновляет его состояние.

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Перейти к следующему заданию** (3)


</dt> <dd>

Перейти к следующему заданию в очереди.

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Повторно запустить задание** (4)


</dt> <dd>

Задание должно быть запущено повторно.

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Запустить задание восстановления** (5)


</dt> <dd>

Запустите задание, связанное с использованием отношения **рековерижоб** . Обратите внимание, что задание восстановления уже должно находиться в очереди, из которой он будет выполняться.

</dd> </dl>

</dd> <dt>

**рундай**
</dt> <dd> <dl> <dt>

Тип данных: **sint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рунмонс**","**\_ Задание CIM**.**Рундайофвик**","**\_ Задание CIM**.**Рунстартинтервал**")
</dt> </dl>

Целое число, используемое в сочетании со свойством **рундайофвик** для указания дня обработки задания. или, если **рундайофвик** имеет значение 0, **рундай** указывает день месяца, когда задание обрабатывается. Если **рундай** является отрицательным целым числом, он указывает день относительно конца месяца или, если **рундай** является положительным целым числом, он указывает день относительно начала месяца.

</dd> <dt>

**рундайофвик**
</dt> <dd> <dl> <dt>

Тип данных: **sint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рунмонс**","**\_ Задание CIM**.**Рундай**","**\_ Задание CIM**.**Рунстартинтервал**")
</dt> </dl>

Целое число, используемое в сочетании со свойством **рундай** для указания дня обработки задания. или, если **рундайофвик** имеет значение 0, **рундай** указывает день месяца, когда задание обрабатывается.

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-Суббота** (-7)


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-Пятница** (-6)


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-Четверг** (-5)


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**Среда** (-4)


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-Вторник** (-3)


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-Понедельник** (-2)


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

**– Воскресенье** (-1)


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

**Ексактдайофмонс** (0)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Воскресенье** (1)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Понедельник** (2)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Вторник** (3)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Среда** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Четверг** (5)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Пятница** (6)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Суббота** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**рунмонс**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рундай**","**\_ Задание CIM**.**Рундайофвик**","**\_ Задание CIM**.**Рунстартинтервал**")
</dt> </dl>

Месяц, когда обработано задание.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Январь** (0)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Февраль** (1)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Март** (2)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Апрель** (3)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Май** (4)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Июнь** (5)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Июль** (6)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Август** (7)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Сентябрь** (8)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Октябрь** (9)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Ноябрь** (10)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Декабрь** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**рунстартинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Рунмонс**","**\_ Задание CIM**.**Рундай**","**\_ Задание CIM**.**Рундайофвик**","**\_ Задание CIM**.**Рунстартинтервал**")
</dt> </dl>

Интервал времени после полуночи при обработке задания. Например, "00000000020000.000000:000" указывает, что задание выполняется в два или более часов местного времени или в формате UTC (время в формате UTC указано с помощью свойства **локалорутктиме** ).

</dd> <dt>

**счедуледстарттиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ Задание CIM**".**Рунмонс**","**\_ Задание CIM**.**Рундай**","**\_ Задание CIM**.**Рундайофвик**","**\_ Задание CIM**.**Рунстартинтервал**")
</dt> </dl>

> [!Note]  
> Это свойство использовать не рекомендуется. Вместо этого рекомендуется использовать свойства **рунмонс**, **рундай**, **рундайофвик** и **рунстартинтервал** .

 

Время, когда запланировано запуск текущего задания. Это время может быть представлено в виде даты и времени или интервала относительно времени, когда запрашивается свойство. Значение, равное нулю, указывает, что задание уже исполняется.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время запуска задания. Это время может быть представлено датой и временем или интервалом относительно времени, когда запрашивается свойство.

</dd> <dt>

**тимесубмиттед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время отправки задания. Значение, равное нулю, указывает, что родительский элемент не может сообщать дату и время.

</dd> <dt>

**унтилтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ Задание CIM**".**Локалорутктиме**")
</dt> </dl>

Время, после которого задание станет недействительным или должно быть остановлено. Время может быть представлено датой и временем или интервалом относительно времени, когда запрашивается это свойство. Значение всех девяти указывает, что задание может выполняться неограниченное время.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЛОГИКАЛЕЛЕМЕНТ CIM**](cim-logicalelement.md)
</dt> </dl>

 

