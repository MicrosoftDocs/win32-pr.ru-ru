---
description: Windows предоставляет интерфейсы API, которые можно использовать для получения меток времени с высоким разрешением или для измерения временных интервалов.
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: Получение высокоточных меток времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a1300967738b717ab8d8c822bf2af3f6a4a7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999757"
---
# <a name="acquiring-high-resolution-time-stamps"></a>Получение высокоточных меток времени

Windows предоставляет интерфейсы API, которые можно использовать для получения меток времени с высоким разрешением или для измерения временных интервалов. Основной API для машинного кода — [**QueryPerformanceCounter (QPC)**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Для драйверов устройств API режима ядра — [**кекуериперформанцекаунтер**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter). Для управляемого кода класс [**System. Diagnostics. Секундомер**](/previous-versions/windows/) использует **QPC** в качестве точного времени.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) не зависит от и не синхронизируется со всеми внешними временными ссылками. Чтобы получить метки времени, которые можно синхронизировать со внешней ссылкой времени (например, время в формате UTC) для использования в долгосрочных измерениях с высоким разрешением, используйте [**жетсистемтимепреЦисеасфилетиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

Метки времени и измерения интервала времени являются неотъемлемой частью измерений производительности компьютера и сети. Эти операции измерения производительности включают вычисление времени отклика, пропускной способности и задержки, а также выполнение кода профилирования. Каждая из этих операций включает в себя измерение действий, возникающих в течение интервала времени, определяемого начальным и завершающим событием, которое может быть независимым от любой внешней ссылки времени дня.

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) обычно является лучшим методом для использования в событиях отметки времени и измеряет небольшие интервалы времени, происходящие в одной системе или виртуальной машине. Используйте [**жетсистемтимепреЦисеасфилетиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) , если вы хотите, чтобы события отметок времени набросаны на несколько компьютеров, при условии, что каждый компьютер участвует в схеме синхронизации времени, например в протоколе NTP. **QPC** помогает избежать проблем, которые могут возникнуть при использовании других подходов к измерению времени, таких как чтение счетчика меток времени процессора (TSC) напрямую.

-   [Поддержка QPC в версиях Windows](#qpc-support-in-windows-versions)
-   [Руководство по приобретению меток времени](#guidance-for-acquiring-time-stamps)
    -   [Виртуализация](#virtualization)
    -   [Прямое использование TSC](#direct-tsc-usage)
    -   [Примеры получения меток времени](#examples-for-acquiring-time-stamps)
-   [Общие вопросы и ответы о QPC и TSC](#general-faq-about-qpc-and-tsc)
-   [Часто задаваемые вопросы о программировании с помощью QPC и TSC](#faq-about-programming-with-qpc-and-tsc)
-   [Характеристики часов низкого уровня оборудования](#low-level-hardware-clock-characteristics)
    -   [Абсолютные часы и разницы](#absolute-clocks-and-difference-clocks)
    -   [Разрешение, точность, точность и стабильность](#resolution-precision-accuracy-and-stability)
-   [Сведения о таймере оборудования](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a>Поддержка QPC в версиях Windows

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) был впервые появился в Windows 2000 и Windows XP и превратился в использование преимуществ улучшений в аппаратной платформе и процессорах. Здесь описаны характеристики **QPC** в различных версиях Windows, помогающие поддерживать программное обеспечение, работающее в этих версиях Windows.

### <a name="windows-xp-and-windows-2000"></a>Windows XP и Windows 2000

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) доступен в Windows XP и Windows 2000 и хорошо работает в большинстве систем. Однако некоторые аппаратные системы BIOS не сообщают о характеристиках аппаратного процессора правильно (неразновидности TSC), а некоторые многоядерные или многопроцессорные системы используют процессоры с Тскс, которые не удалось синхронизировать между ядрами. Системы с уязвимым встроенным по, которые работают под управлением этих версий Windows, могут не предоставлять одинаковое **QPC** чтение на разных ядрах, если в качестве основы для **QPC** использовался таймер TSC.

### <a name="windows-vista-and-windows-server-2008"></a>Windows Vista и Windows Server 2008

Все компьютеры, входящие в состав Windows Vista и Windows Server 2008, использовали счетчик платформы (таймер событий высокой точности (ХПЕТ)) или таймер управления питанием ACPI (таймер PM) в качестве базиса для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Такие таймеры платформы имеют более высокую задержку доступа, чем таймер TSC, и являются общими для нескольких процессоров. Это ограничивает масштабируемость **QPC** , если она вызывается параллельно из нескольких процессоров.

### <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 и Windows Server 2008 R2

Большинство компьютеров Windows 7 и Windows Server 2008 R2 имеют процессоры с постоянной ставкой Тскс и используют эти счетчики в качестве базиса для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Тскс — это аппаратные счетчики высокого разрешения для каждого процессора, доступ к которым можно получить с очень низкой задержкой и нагрузкой (в порядке 10 или 100 циклов машин, в зависимости от типа процессора). Windows 7 и Windows Server 2008 R2 используют Тскс в качестве основания для **QPC** в однопроцессорных системах, где операционная система (или низкоуровневая оболочка) может жестко синхронизировать отдельные тскс во всех процессорах во время инициализации системы. В таких системах стоимость чтения счетчика производительности значительно ниже по сравнению с системами, использующими счетчик платформы. Кроме того, не существует дополнительных затрат на параллельные вызовы и запросы пользовательского режима, которые позволяют избежать системных вызовов, что еще больше сокращает издержки. В системах, где таймер TSC не подходит для тимекипинг, Windows автоматически выбирает счетчик платформы (таймер ХПЕТ или ACPI PM Timer) в качестве базиса для **QPC**.

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a>Windows 8, Windows 8.1, Windows Server 2012 и Windows Server 2012 R2

Windows 8, Windows 8.1, Windows Server 2012 и Windows Server 2012 R2 используют Тскс в качестве основания для счетчика производительности. Алгоритм синхронизации TSC был значительно улучшен для лучшего размещения больших систем с большим количеством процессоров. Кроме того, добавлена поддержка нового точного API времени суток, что позволяет получать точные метки времени для часов стены с операционной системы. Дополнительные сведения см. в разделе [**жетсистемтимепреЦисеасфилетиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). На платформах PC на базе Windows RT счетчик производительности основывается на счетчике собственной платформы или системного счетчика, предоставляемого универсальным таймером Windows RT PC, если платформа настолько оснащена.

## <a name="guidance-for-acquiring-time-stamps"></a>Руководство по приобретению меток времени

Windows имеет и будет продолжать вкладываться в предоставление надежного и эффективного счетчика производительности. Если вам нужны отметки времени с разрешением 1 микросекунды или лучше, а метки времени не нужно синхронизировать со ссылкой на внешнее время, выберите [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), [**кекуериперформанцекаунтер**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)или [**кекуеринтеррупттимепреЦисе**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise). Если вам нужны отметки времени с синхронизированным временем в формате UTC с разрешением 1 микросекунды или выше, выберите [**жетсистемтимепреЦисеасфилетиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) или [**кекуерисистемтимепреЦисе**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise).

На относительно небольшом количестве платформ, которые не могут использовать регистр TSC как [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) , например, по причинам, описанным в [сведениях о аппаратном таймере](#hardware-timer-info), получение меток времени с высоким разрешением может значительно дороже, чем получение меток времени с низким разрешением. Если разрешение от 10 до 16 миллисекунд достаточно, можно использовать [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64), [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), [**кекуеринтеррупттиме**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)или [**кекуерюнбиасединтеррупттиме**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) для получения меток времени, которые не синхронизируются со внешними временными ссылками. Для штампов времени с синхронизированным временем в формате UTC используйте [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) или [**кекуерисистемтиме**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1). Если требуется более высокое разрешение, можно использовать [**куеринтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**куерюнбиасединтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)или [**кекуеринтеррупттимепреЦисе**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) для получения меток времени.

В общем случае результаты счетчика производительности будут согласованы во всех процессорах в многоядерных и многопроцессорных системах, даже если они измеряются в разных потоках или процессах. Ниже приведены некоторые исключения из этого правила.

-   Передовые операционные системы Windows Vista, работающие на определенных процессорах, могут нарушать эту согласованность по одной из следующих причин:

    -   Аппаратные процессоры имеют неизменяемую TSC, а BIOS не указывает это состояние правильно.
    -   Используемый алгоритм синхронизации TSC не подходит для систем с большим количеством процессоров.

-   При сравнении результатов счетчика производительности, полученных из разных потоков, рассмотрите возможность неоднозначного упорядочения значений, отличающихся от ± 1 Tick. Если отметки времени берутся из одного потока, неопределенность ± 1 тика не применяется. В этом контексте термин Tick ссылается на период времени, равный 1 (частота счетчика производительности, полученного от [**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)).

При использовании счетчика производительности в больших серверных системах с многовременными доменами, которые не синхронизированы в оборудовании, Windows определяет, что таймер TSC не может использоваться в целях обеспечения времени и выбирает счетчик платформы в качестве базиса для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Хотя этот сценарий по-прежнему обеспечивает надежные отметки времени, задержка доступа и масштабируемость неблагоприятно затрагиваются. Поэтому, как было сказано в предыдущем руководстве по использованию, используйте только API, которые обеспечивают 1 микросекунду или лучшее решение, если такое разрешение требуется. Таймер TSC используется в качестве базиса для **QPC** в многотактовых системах с несколькими часами, которые включают синхронизацию оборудования всех доменов процессоров, так как это эффективно делает их функциями единой системы домена часов.

Частота счетчика производительности зафиксирована при загрузке системы и согласована во всех процессорах, поэтому необходимо запросить частоту от [**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) при инициализации приложения, а затем кэшировать результат.

### <a name="virtualization"></a>Виртуализация

Предполагается, что счетчик производительности надежно работает на всех гостевых виртуальных машинах, работающих на правильных гипервизорах. Однако низкоуровневые оболочки, которые соответствуют интерфейсу гипервизора версии 1,0 и поверхности просвещение, могут существенно снизить издержки. Дополнительные сведения о интерфейсах гипервизора и просветлений см. в статье [спецификации гипервизора](/virtualization/hyper-v-on-windows/reference/tlfs).

### <a name="direct-tsc-usage"></a>Прямое использование TSC

Мы настоятельно не рекомендуем использовать инструкцию процессора **RDTSC** или **RDTSCP** для прямого запроса таймера TSC, так как вы не получаете надежные результаты в некоторых версиях Windows, в рамках динамической миграции виртуальных машин и в аппаратных системах без инвариантной или тесной синхронизации тскс. Вместо этого мы рекомендуем использовать [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) для использования абстракции, согласованности и переносимости, предоставляемой ИТ.

### <a name="examples-for-acquiring-time-stamps"></a>Примеры получения меток времени

В различных примерах кода в этих разделах показано, как получить отметки времени.

### <a name="using-qpc-in-native-code"></a>Использование QPC в машинном коде

В этом примере показано, как использовать [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) в машинном коде C и C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

QueryPerformanceFrequency(&Frequency); 
QueryPerformanceCounter(&StartingTime);

// Activity to be timed

QueryPerformanceCounter(&EndingTime);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;


//
// We now have the elapsed number of ticks, along with the
// number of ticks-per-second. We use these values
// to convert to the number of elapsed microseconds.
// To guard against loss-of-precision, we convert
// to microseconds *before* dividing by ticks-per-second.
//

ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



### <a name="acquiring-high-resolution-time-stamps-from-managed-code"></a>Получение меток времени с высоким разрешением из управляемого кода

В этом примере показано, как использовать класс управляемого кода [**System. Diagnostics. Секундомер**](/previous-versions/windows/) .


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



Класс [**System. Diagnostics. Секундомер**](/previous-versions/windows/) также предоставляет несколько удобных методов для выполнения измерений интервала времени.

### <a name="using-qpc-from-kernel-mode"></a>Использование QPC из режима ядра

Ядро Windows предоставляет доступ к счетчику производительности в режиме ядра через [**кекуериперформанцекаунтер**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) , из которого можно получить как счетчик производительности, так и частоту производительности. **Кекуериперформанцекаунтер** доступен только в режиме ядра и предоставляется для модулей записи драйверов устройств и других компонентов режима ядра.

В этом примере показано, как использовать [**кекуериперформанцекаунтер**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) в режиме ядра C и C++.


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

StartingTime = KeQueryPerformanceCounter(&Frequency);

// Activity to be timed

EndingTime = KeQueryPerformanceCounter(NULL);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;
ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



## <a name="general-faq-about-qpc-and-tsc"></a>Общие вопросы и ответы о QPC и TSC

Здесь приведены ответы на часто задаваемые вопросы о [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) и тскс в целом.

<dl> <dt>

<span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**Является QueryPerformanceCounter () аналогично функции Win32 Жеттикккаунт () или GetTickCount64 ()?**
</dt> <dd>

Нет. [**Жеттикккаунт**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) и [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) не связаны с [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). **Жеттикккаунт** и **GetTickCount64** возвращают количество миллисекунд с момента запуска системы.

</dd> <dt>

<span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**Следует ли использовать QPC или вызывать инструкции RDTSC/РДТСКП напрямую?**
</dt> <dd>

Чтобы избежать проблем с неправильными и переносимостью, мы настоятельно рекомендуем использовать [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) вместо использования регистра TSC или инструкций **RDTSC** или **RDTSCP** процессора.

</dd> <dt>

<span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**Что такое отношение QPC к внешнему эпохе времени? Можно ли синхронизировать его с внешним Эпохом, например в формате UTC?**
</dt> <dd>

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) основан на счетчике оборудования, который не может быть синхронизирован со внешней ссылкой на время, например в формате UTC. Для точной отметки времени дня, которую можно синхронизировать с внешней ссылкой в формате UTC, используйте [**жетсистемтимепреЦисеасфилетиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).

</dd> <dt>

<span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**QPC ли воздействие на летнее время, високосные секунды, часовые пояса или изменения системного времени, внесенные администратором?**
</dt> <dd>

Нет. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) полностью независим от системного времени и UTC.

</dd> <dt>

<span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**QPC ли влияние изменений частоты процессора, вызванных технологией управления питанием или технологии Turbo Boost?**
</dt> <dd>

Нет. Если процессор имеет инвариант TSC, эти изменения не затрагивают [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) . Если процессор не имеет инвариантов TSC, **QPC** вернется к аппаратному таймеру платформы, который не будет зависеть от изменения частоты процессора или технологии Turbo Boost.

</dd> <dt>

<span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**QPCа ли надежная работа на многопроцессорных системах, многоядерной системе и системах с технологией Hyper-Threading?**
</dt> <dd>

Да

</dd> <dt>

<span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**Разделы справки определить и проверить, работает ли QPC на моем компьютере?**
</dt> <dd>

Такие проверки выполнять не нужно.

</dd> <dt>

<span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**Какие процессоры имеют неинвариантный Тскс? Как проверить, не имеет ли моя система значение TSC?**
</dt> <dd>

Вам не нужно выполнять эту проверку самостоятельно. Операционные системы Windows выполняют несколько проверок при инициализации системы, чтобы определить, подходит ли таймер TSC в качестве основания для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Однако для справочных целей можно определить, имеет ли процессор инвариантный таймер TSC, используя один из следующих вариантов:

-   Служебная программа Coreinfo.exe из Windows Sysinternals
-   Проверка значений, возвращаемых инструкцией CPUID, относящейся к характеристикам TSC
-   документация производителя процессора

Ниже показаны неизменяемые сведения TSC, предоставляемые служебной программой Windows Sysinternals Coreinfo.exe ([www.sysinternals.com](https://www.sysinternals.com)). Звездочка означает «истина».

``` syntax
> Coreinfo.exe 

Coreinfo v3.2 - Dump information on system CPU and memory topology
Copyright (C) 2008-2012 Mark Russinovich
Sysinternals - www.sysinternals.com

 <unrelated text removed>

RDTSCP          * Supports RDTSCP instruction
TSC             * Supports RDTSC instruction
TSC-DEADLINE    - Local APIC supports one-shot deadline timer
TSC-INVARIANT   * TSC runs at constant rate
```

</dd> <dt>

<span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**Надежно ли QPC работает на компьютерных аппаратных платформах Windows RT?**
</dt> <dd>

Да

</dd> <dt>

<span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**Как часто QPC передвигаться?**
</dt> <dd>

Не менее 100 лет от самой последней загрузки системы и, возможно, дольше, основываясь на используемом базовом аппаратном таймере. Для большинства приложений смена не является проблемой.

</dd> <dt>

<span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**Какова стоимость вычислительных ресурсов при вызове QPC?**
</dt> <dd>

Вычислительный вызов [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) определяется преимущественно базовой аппаратной платформой. Если регистр TSC используется в качестве основания для QPC, вычислительные затраты определяются в первую очередь на время, затрачиваемое процессором на обработку инструкции **RDTSC** . Это время в диапазоне от 10 циклов ЦП до нескольких сотен циклов ЦП в зависимости от используемого процессора. Если таймер TSC не может быть использован, система выбирает другое аппаратное время. Так как эти базовые базы данных расположены на материнской плате (например, в Южной мост PCI или PCH), вычислительные затраты на вызов выше, чем таймер TSC, и часто встречаются в 0,8-1,0 микросекундах в зависимости от скорости процессора и других факторов оборудования. Эта стоимость определяется временем, необходимым для доступа к аппаратному устройству на материнской плате.

</dd> <dt>

<span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**Требуется ли для QPC переход ядра (системный вызов)?**
</dt> <dd>

Переход ядра не требуется, если система может использовать регистр TSC в качестве основания для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Если система должна использовать другую базу времени, например таймер ХПЕТ или PM, требуется системный вызов.

</dd> <dt>

<span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**Является ли счетчик производительности монотонным (не уменьшающимся)?**
</dt> <dd>

Да

</dd> <dt>

<span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**Можно ли использовать счетчик производительности для упорядочивания событий в течение времени?**
</dt> <dd>

Да. Однако при сравнении результатов счетчика производительности, полученных из разных потоков, значения, отличающиеся ± 1 Tick, имеют неоднозначное упорядочение, как если бы они имели одинаковую отметку времени.

</dd> <dt>

<span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**Насколько точны счетчики производительности?**
</dt> <dd>

Ответ зависит от различных факторов. Дополнительные сведения см. в разделе [характеристики аппаратных часов низкого уровня](#low-level-hardware-clock-characteristics).

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a>Часто задаваемые вопросы о программировании с помощью QPC и TSC

Здесь приведены ответы на часто задаваемые вопросы о программировании с помощью [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) и тскс.

<dl> <dt>

<span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**Мне нужно преобразовать выходные данные QPC в миллисекунды. Как избежать потери точности при преобразовании в Double или float?**
</dt> <dd>

При выполнении вычислений с целочисленными счетчиками производительности необходимо учитывать следующие моменты.

-   Деление целых чисел приведет к потере остатка. В некоторых случаях это может привести к потере точности.
-   Преобразование между 64-разрядными целыми числами и плавающей запятой (Double) может привести к потере точности, поскольку мантисса с плавающей запятой не может представлять все возможные целочисленные значения.
-   Умножение в 64 разрядов может привести к переполнению целого числа.

В качестве общего принципа отложите эти вычисления и преобразования максимально долго, чтобы избежать возникновения ошибок.

</dd> <dt>

<span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**Как выполнить преобразование QPC в 100 наносекунд, чтобы добавить его в FILETIME?**
</dt> <dd>

Время файла — это 64-разрядное значение, представляющее число 100-наносекундных интервалов, прошедших с 12:00 утра. 1 января 1601 скоординированного всемирного времени (UTC). Время файла используется вызовами API Win32, которые возвращают время дня, например [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) и [**жетсистемтимепреЦисеасфилетиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime). Напротив, [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) возвращает значения, представляющие время в единицах измерения 1/(частота счетчика производительности, полученного из [**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)). Для преобразования между двумя необходимо рассчитать отношение интервала **QPC** и 100-наносекундах интервалов. Будьте внимательны, чтобы избежать потери точности, поскольку значения могут быть небольшими (0,0000001/0,000000340).

</dd> <dt>

<span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**Почему отметка времени, возвращаемая из QPC, возвращает целое число со знаком?**
</dt> <dd>

Вычисления, затрагивающие метки времени [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) , могут содержать вычитание. Используя значение со знаком, можно выполнять вычисления, которые могут привести к отрицательным значениям.

</dd> <dt>

<span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**Как можно получить метки времени высокого разрешения из управляемого кода?**
</dt> <dd>

Вызовите метод [**секундомер.. timestamp**](/previous-versions/windows/) из класса [**System. Diagnostics. Секундомер**](/previous-versions/windows/) . Пример использования **секундомера. timestamp** см. в разделе [Получение меток времени с высоким разрешением из управляемого кода](#acquiring-high-resolution-time-stamps-from-managed-code).

</dd> <dt>

<span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**При каких обстоятельствах Куериперформанцефрекуенци возвращает значение FALSE или QueryPerformanceCounter возвращает нуль?**
</dt> <dd>

Это не произойдет в любой системе под управлением Windows XP или более поздней версии.

</dd> <dt>

<span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**Нужно ли устанавливать сходство потоков в одно ядро для использования QPC?**
</dt> <dd>

Нет. Дополнительные сведения см. в разделе [рекомендации по приобретению меток времени](#guidance-for-acquiring-time-stamps). Этот сценарий не является необходимым и нежелательным. Выполнение этого сценария может негативно сказаться на производительности приложения путем ограничения обработки одним ядром или созданием узкого места в одном ядре, если несколько потоков устанавливают свое сходство для одного ядра при вызове [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a>Характеристики часов низкого уровня оборудования

В этих разделах показаны характеристики аппаратных часов низкого уровня.

### <a name="absolute-clocks-and-difference-clocks"></a>Абсолютные часы и разницы

Абсолютные часы обеспечивают точность считывания по времени суток. Обычно они основаны на всеобщем скоординированном времени (UTC), поэтому их точность зависит от того, насколько они синхронизированы со ссылкой на внешнее время. Разница измеряет временные интервалы и обычно не основывается на внешнем эпохе времени. [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) — это разница времени и не синхронизируется с внешним временным временем или ссылкой. При использовании **QPC** для измерений интервалов времени обычно обеспечивается более высокая точность, чем при использовании меток времени, полученных из абсолютных часов. Это связано с тем, что процесс синхронизации времени с абсолютными часами может привести к появлению этапов и сдвигов частоты, которые увеличивают неопределенность краткосрочных интервалов времени.

### <a name="resolution-precision-accuracy-and-stability"></a>Разрешение, точность, точность и стабильность

[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) использует аппаратный счетчик в качестве базиса. Аппаратные таймеры состоят из трех частей: генератор тактов, счетчик, который подсчитывает такты, и способ получения значения счетчика. Характеристики этих трех компонентов определяют разрешение, точность, точность и стабильность **QPC**.

Если генератор оборудования обеспечивает такты с постоянной частотой, интервалы времени могут измеряться путем простого подсчета этих тактов. Частота, с которой создаются такты, называется частотой и выражается в герцах (Гц). Обратная частота частоты называется периодом или интервалом тактов и выражается в соответствующей международной единице времени (например, секунды, миллисекунда, микросекунда или наносекундных).

![временной интервал](images/tick-interval.png)

Разрешение таймера равно точке. Разрешение определяет возможность различать любые две отметки времени и размещает нижнюю границу наименьшего интервала времени, который может измеряться. Иногда это называется разрешением Tick.

Цифровое измерение времени представляет неопределенное измерение, равное ± 1 тактов, так как цифровой счетчик увеличивается на отдельные шаги, а время постоянно увеличивается. Это неопределенность называется ошибкой дискретизация. Для типичных измерений интервала времени этот результат часто можно игнорировать, так как ошибка куантизинг намного меньше, чем измеряется интервал времени.

![цифровое измерение времени](images/digital-time-measure.png)

Однако если измеряемый период является небольшим и приближается к разрешению таймера, необходимо учитывать эту ошибку куантизинг. В сообщении об ошибке отображается один из периодов времени.

На следующих двух схемах показано влияние неопределенности ± 1 тика с помощью таймера с разрешением 1 единицы времени.

![неопределенность Tick](images/tick-uncertainty.png)

[**Куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) возвращает частоту [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), а точка и разрешение равны обратному значению этого значения. Частота счетчика производительности, возвращаемая **куериперформанцефрекуенци** , определяется во время инициализации системы и не изменяется во время работы системы.

> [!Note]  
> Возможны случаи, когда [**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) не возвращает фактическую частоту генератора аппаратных тактов. Например, во многих случаях **куериперформанцефрекуенци** возвращает ЧАСТОТу TSC, деленную на 1024; и в Hyper-V частота счетчика производительности всегда составляет 10 МГц, когда Гостевая виртуальная машина выполняется в [низкоуровневой оболочке](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) , которая реализует [интерфейс гипервизора версии 1,0](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx). В результате не следует рассчитывать на то, что **куериперформанцефрекуенци** будет возвращать точную частоту TSC.

 

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) считывает счетчик производительности и возвращает общее количество тактов, произошедших с момента запуска операционной системы Windows, включая время перехода компьютера в спящий режим, например ждущий, спящий или подключенный режим ожидания.

В этих примерах показано, как вычислить интервал времени и разрешение, а также как преобразовать счетчик тактов в значение времени.

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Пример 1**
</dt> <dd>

[**Куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) возвращает значение 3 125 000 на определенном компьютере. Каков интервал времени и разрешение [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) измерений на этом компьютере? Интервал Tick (точка) — это обратная величина 3 125 000, которая равна 0,000000320 (320 наносекунд). Таким образом, каждый такт представляет передачу 320 наносекунд. Интервалы времени, меньшие 320 наносекунд, не могут измеряться на этом компьютере.

Интервал времени = 1/(частота производительности)

Интервал времени = 1/3125000 = 320 НС

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Пример 2**
</dt> <dd>

На том же компьютере, что и в предыдущем примере, разница между значениями, возвращаемыми двумя последовательными вызовами [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) , равна 5. Сколько времени прошло между двумя вызовами? 5 тактов, умноженные на 320 наносекунд, выдают 1,6 микросекунд.

Елапседтиме = \* интервал делений

Елапседтиме = 5 \* 320 NS = 1,6 μс

</dd> </dl>

Для доступа (чтения) счетчика тактов от программного обеспечения требуется время, а это время доступа может уменьшить точность измерения времени. Это связано с тем, что минимальный интервал времени (наименьший интервал времени, который можно измерять) — это большее из значений разрешения и времени доступа.

Точность = максимальное \[ разрешение, акцесстиме\]

Например, рассмотрим гипотетический аппаратный таймер с разрешением 100 НС и временем доступа 800 НС. Это может быть вызвано тем, что при использовании таймера платформы вместо регистра TSC в качестве основания для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Таким образом, точность будет 800 наносекунд не 100 наносекунд, как показано в этом вычислении.

Precision = MAX \[ 800 НС, 100 НС \] = 800 NS

На этих двух рисунках показан этот результат.

![время доступа qpc](images/qpc-access-time.png)

Если время доступа больше разрешения, не пытайтесь улучшить точность, выполнив подбор. Иными словами, следует предположить, что отметка времени выполняется точно в середине, в начале или в конце вызова.

В отличие от этого, рассмотрим следующий пример, в котором время доступа к [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) составляет только 20 наносекунд, а аппаратное разрешение — 100 наносекунд. Это может быть вызвано тем, что регистр TSC используется в качестве основания для **QPC**. Здесь точность ограничена с помощью разрешения часов.

![точность qpc](images/qpc-precision.png)

На практике можно найти источники времени, для которых время, необходимое для чтения счетчика, больше или меньше, чем разрешение. В любом случае точность будет равна большему из двух.

Эта таблица содержит сведения о приблизительном разрешении, времени доступа и точности различных часов. Обратите внимание, что некоторые значения зависят от разных процессоров, аппаратных платформ и скорости процессора.



| Источник часов                                                      | Номинальная тактовая частота | Разрешение часов    | Время доступа (номинал) | Точность       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| PC RTC                                                            | 64 Гц                   | 15,625 МС | Н/Д                   | Н/Д             |
| Счетчик производительности запросов, использующий таймер TSC с тактовой частотой процессора 3 ГГц  | 3 МГц                   | 333 наносекунд     | 30 наносекунд        | 333 наносекунд |
| **RDTSC** машины в системе со временем цикла 3 ГГц | 3 ГГц                   | 333 пикосекондс     | 30 наносекунд        | 30 наносекунд  |



 

Поскольку [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) использует счетчик оборудования, когда вы понимаете некоторые основные характеристики аппаратных счетчиков, вы получаете представление о возможностях и ограничениях **QPC**.

Наиболее часто используемым генератором аппаратных тактов является Crystal осциллятор. Crystal — это небольшая часть Quartz или другого церамик материала, которая представляет характеристики пиезоелектрик, которые предоставляют недорогую частотную ссылку с отличной стабильностью и точностью. Эта частота используется для создания тактов, подсчитанных часами.

Точность таймера относится к степени соответствия значению true или Standard. Это зависит главным образом от возможности Crystal осциллятор по заданной частоте. Если частота колебаний слишком высока, часы будут работать быстро, а измеряемые интервалы будут отображаться дольше, чем на самом деле. Если частота слишком мала, часы будут работать медленнее, а измеряемые интервалы будут короче, чем на самом деле.

Для типичных измерений интервала времени в течение короткой длительности (например, измерения времени отклика, измерения задержки сети и т. д.), как правило, достаточно осциллятор оборудования. Однако для некоторых измерений точность осциллятор частоты играет важную роль, особенно для длинных интервалов времени или при необходимости сравнения измерений, полученных на разных компьютерах. Оставшаяся часть этого раздела посвящена влиянию точности осциллятор.

Кристалс "частота колебаний" устанавливается во время производственного процесса и указывается производителем с точки зрения заданной частоты плюс или минус отклонения в производстве, выраженный в "штук в миллион" (стр/мин), которые называются максимальным смещением частоты. Кристалл с заданной частотой 1 000 000 Гц и максимальным смещением частоты в ± 10 стр/мин будет соответствовать ограничениям спецификации, если фактическая частота находилась в диапазоне от 999 990 Гц до 1 000 010 Гц.

При замене частей фразы на миллионы в микросекундах в секунду можно применить эту ошибку смещения частоты к измерению интервалов времени. Осциллятор с смещением + 10 в минуту будет иметь ошибку 10 микросекунд в секунду. Соответственно, при измерении интервала в 1 секунду он будет выполняться быстро и измерять интервал в 1 секунду как 0,999990 секунд.

Удобный справочник заключается в том, что ошибка частоты 100 стр/мин вызывает ошибку 8,64 секунд после 24 часов. Эта таблица представляет неопределенность измерения из-за более длинных интервалов времени в накопленной ошибке.



| Длительность интервала времени | Неопределенность измерений из-за накопленной ошибки с отклонением +/-10 PPM |
|------------------------|--------------------------------------------------------------------------------------|
| 1 микросекунда          | ± 10 пикосекондс (10-12)                                                             |
| 1 мс          | ± 10 наносекунд (10-9)                                                              |
| 1 с               | ± 10 микросекунд                                                                    |
| 1 час                 | ± 60 микросекунд                                                                    |
| 1 день                  | ± 0,86 секунд                                                                       |
| 1 неделя                 | ± 6,08 секунд                                                                       |



 

В приведенной выше таблице показано, что для небольших временных интервалов ошибку смещения частоты часто можно игнорировать. Однако для больших интервалов времени даже небольшое смещение частоты может привести к существенным незначительным измерениям.

Crystal осцилляторами, который используется в персональных компьютерах и серверах, обычно изготовлен с частотой, равной ± 30 – 50 штук в миллион, и редко Кристалс может быть отключен до 500 стр/с. Хотя Кристалс с гораздо более жесткими отклонениями смещения, они являются более ресурсоемкими и поэтому не используются на большинстве компьютеров.

Чтобы снизить негативные последствия этой ошибки смещения частоты, последние версии Windows, в особенности Windows 8, используют несколько аппаратных таймеров для определения смещения частоты и ее компенсации в максимально возможной степени. Этот процесс калибровки выполняется при запуске Windows.

Как показано в следующих примерах, ошибка смещения частоты аппаратных часов влияет на достижимую точность, а разрешение часов может быть менее важным.

![Частота ошибок смещения влияет на достижимость](images/freq-offset-error.png)

<dl> <dt>

<span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Пример 1**
</dt> <dd>

Предположим, что вы выполняете измерения интервала времени с помощью осциллятор с частотой 1 МГц, которая имеет разрешение 1 микросекунда, и значение максимальной частоты смещения в ± 50 стр/мин. Теперь давайте предположим, что смещение имеет ровно + 50 стр/мин. Это означает, что фактическая частота будет составлять 1 000 050 Гц. Если мы измеряем интервал времени, равный 24 часам, то измерение будет 4,3 секунд слишком коротким (23:59:55.700000, измеренное по сравнению с 24:00:00.000000 фактическим).

Секунд в день = 86400

Ошибка смещения частоты = 50 стр/мин = 0,00005

86 400 секунд \* 0,00005 = 4,3 секунд

</dd> <dt>

<span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Пример 2**
</dt> <dd>

Предположим, что тактовые частоты процессора контролируются Crystal осциллятор и заданной частотой 3 ГГц. Это означает, что разрешение будет равно 1 или 3000000000 или примерно 333 пикосекондс. Предположим, что кристалл, используемый для управления тактами процессора, имеет частотный допуск ± 50 стр/мин и фактически + 50 стр/мин. Несмотря на выразительное решение, измерение интервала времени, равное 24 часам, по-прежнему будет 4,3 секунд. (23:59:55.7000000000 измеряется в сравнении с 24:00:00.0000000000 фактическим).

Секунд в день = 86400

Ошибка смещения частоты = 50 стр/мин = 0,00005

86 400 секунд \* 0,00005 = 4,3 секунд

Это показывает, что таймеры TSC с высоким разрешением не обязательно обеспечивают более точные показатели, чем часы с низким разрешением.

</dd> <dt>

<span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Пример 3**
</dt> <dd>

Рассмотрите возможность использования двух разных компьютеров для измерения одного и того же 24-часового интервала времени. Оба компьютера имеют осциллятор с максимальным смещением частоты ± 50 стр/мин. Насколько продвинуться измерение одного и того же интервала времени в этих двух системах? Как и в предыдущих примерах, ± 50 стр/мин выдает максимальную ошибку ± 4,3 секунд после 24 часов. Если одна система работает в 4,3 секунд быстро, а другая 4,3 секунд работает медленнее, то максимальная ошибка может со8,6 ставлять не более 24 часов.

Секунд в день = 86400

Ошибка смещения частоты = ± 50 стр/мин = ± 0,00005

± (86 400 секунд \* 0,00005) = ± 4,3 секунд

Максимальное смещение между двумя системами = 8,6 секунд

В целом, ошибка смещения частоты становится все более важной при измерении длинных временных интервалов и при сравнении измерений между различными системами.

Стабильность таймера описывает, изменяется ли частота тактов с течением времени, например в результате изменения температуры. Функция Quartz Кристалс, используемая в качестве генераторов тактов на компьютерах, будет демонстрировать небольшие изменения частоты в качестве функции температуры. Ошибка, вызванная смещением в температуре, обычно мала по сравнению с ошибкой смещения частоты для общих диапазонов температуры. Однако разработчикам программного обеспечения для портативного оборудования или оборудования может потребоваться учитывать этот результат в больших колебаниях температуры.

</dd> </dl>

## <a name="hardware-timer-info"></a>Сведения о таймере оборудования

<dl> <dt>

<span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**Регистр TSC**
</dt> <dd>

Некоторые процессоры Intel и AMD содержат регистр TSC, который является 64-битным регистром, который увеличивается с высокой частотой, обычно равной процессорным часам. Значение этого счетчика можно прочитать с помощью инструкций на компьютере **RDTSC** или **RDTSCP** , предоставляя очень низкое время доступа и вычислительную стоимость в порядке десятков или сотен машинных циклов в зависимости от процессора.

Несмотря на то, что регистр TSC кажется идеальным механизмом отметки времени, в некоторых случаях он не может надежно работать в целях тимекипинг:

-   Не все процессоры имеют регистры TSC, поэтому использование регистра TSC в программном обеспечении напрямую создает проблему переносимости. (В этом случае в Windows будет выбран альтернативный источник времени для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) , что позволяет избежать проблемы переносимости.)
-   Некоторые процессоры могут варьировать частоту таймера TSC или прерывать изменение регистра TSC, что делает таймер TSC неприемлемым для временных целей этих процессоров. Эти процессоры говорят о том, что регистры TSC не являются инвариантными. (Windows автоматически обнаружит это и выберите альтернативный источник времени для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   В системах с несколькими процессорами или многоядерными системами некоторые процессоры и системы не могут синхронизировать часы каждого ядра с одним и тем же значением. (Windows автоматически обнаружит это и выберите альтернативный источник времени для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   В некоторых крупных многопроцессорных системах вы не сможете синхронизировать тактовые импульсы процессора с одним и тем же значением, даже если процессор имеет инвариантный таймер TSC. (Windows автоматически обнаружит это и выберите альтернативный источник времени для [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).
-   Некоторые процессоры будут выполнять инструкции в неопределенном порядке. Это может привести к неправильному счетчику циклов, если **RDTSC** используется для последовательностей инструкций времени, так как инструкция **RDTSC** может выполняться в другое время, чем указано в программе. Инструкция **RDTSCP** была введена на некоторых процессорах в ответ на эту проблему.

Как и другие таймеры, таймер TSC основан на Crystal осциллятор, Точная частота которого не известна заранее и имеет ошибку смещения частоты. Поэтому, прежде чем его можно будет использовать, его необходимо откалибровать с помощью другой ссылки времени.

Во время инициализации системы Windows проверяет, подходит ли таймер TSC для целей времени, и выполняет необходимую калибровку частоты и основную синхронизацию.

</dd> <dt>

<span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**Часы PM**
</dt> <dd>

Таймер ACPI, известный также как часы PM, был добавлен в системную архитектуру для обеспечения надежной отметки времени независимо от скорости процессора. Так как это была единственная цель этого таймера, она предоставляет отметку времени в одном цикле, но не предоставляет никаких других функциональных возможностей.

</dd> <dt>

<span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**Таймер ХПЕТ**
</dt> <dd>

Высокоточный таймер событий (ХПЕТ) был разработан корпорацией Intel и корпорацией Майкрософт в соответствии с требованиями к синхронизации мультимедиа и других приложений, зависящих от времени. Поддержка ХПЕТ в Windows, начиная с Windows Vista, и сертификация Windows 7 и Windows 8 с логотипом оборудования требует поддержки ХПЕТ в аппаратной платформе.

</dd> </dl>

 

 
