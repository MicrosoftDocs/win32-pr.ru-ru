---
title: Использование данных счетчика с помощью функций PerfLib
description: Функции API PerfLib можно использовать для прямого использования данных счетчиков производительности v2, если не удается использовать PDH.
ms.date: 08/17/2020
ms.topic: article
ms.openlocfilehash: 9fec3bb97ec32ff98e2b317b737023da81147bdd
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2020
ms.locfileid: "105719156"
---
# <a name="using-the-perflib-functions-to-consume-counter-data"></a>Использование данных счетчика с помощью функций PerfLib

Используйте функции-потребители PerfLib, чтобы использовать данные производительности из поставщиков данных производительности v2, если нельзя использовать [функции вспомогательных данных производительности (PDH)](using-the-pdh-functions-to-consume-counter-data.md). Эти функции могут использоваться при написании приложений OneCore для сборки каунтерсетс v2 или при необходимости сборки v2 каунтерсетс с минимальными зависимостями и издержками.

> [!TIP]
> Функции-потребители версии PerfLib v2 сложнее использовать, чем функции модуля поддержки данных производительности (PDH) и поддерживают сбор данных только от поставщиков v2. Для большинства приложений предпочтительнее использовать функции PDH.

Функции-потребители версии PerfLib v2 — это API низкого уровня для сбора данных от **поставщиков v2**. Функции-потребители версии PerfLib v2 не поддерживают сбор данных от **поставщиков v1**.

> [!WARNING]
> Функции-потребители версии PerfLib v2 потенциально могут получать данные из ненадежных источников, например из локальных служб с ограниченными правами доступа или с удаленных компьютеров. Функции-потребители версии PerfLib v2 не проверяют данные на целостность или согласованность. Чтобы убедиться в том, что возвращенные данные являются последовательными, это приложение-потребитель, например, значения размера в возвращенном блоке данных не превышают фактический размер возвращенного блока данных. Это особенно важно, когда приложение-потребитель работает с повышенными привилегиями.

## <a name="perflib-usage"></a>Использование PerfLib

`perflib.h`Заголовок включает объявления, используемые поставщиками пользовательского режима v2 (например, API поставщика PerfLib) и v2 (т. е. пользовательский API-интерфейс PerfLib). Он объявляет следующие функции для использования данных о производительности v2:

- Используйте [**перфенумератекаунтерсет**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecounterset) для получения идентификаторов GUID каунтерсетс, зарегистрированных поставщиками v2 в системе.
- Используйте [**перфкуерикаунтерсетрегистратионинфо**](/windows/desktop/api/Perflib/nf-perflib-perfquerycountersetregistrationinfo) для получения сведений о конкретном наборе счетчиков, таких как имя, описание, тип (одиночный экземпляр или несколько экземпляров), типы счетчиков, имена счетчиков и описания счетчиков.
- Используйте [**перфенумератекаунтерсетинстанцес**](/windows/desktop/api/Perflib/nf-perflib-perfenumeratecountersetinstances) для получения имен текущих активных экземпляров набора счетчиков с несколькими экземплярами.
- Используйте [**перфопенкуерихандле**](/windows/desktop/api/Perflib/nf-perflib-perfopenqueryhandle) для создания нового маркера запроса, который будет использоваться для сбора данных из одного или нескольких каунтерсетс.
- Чтобы закрыть маркер запроса, используйте [**перфклосекуерихандле**](/windows/desktop/api/Perflib/nf-perflib-perfclosequeryhandle) .
- Используйте [**перфаддкаунтерс**](/windows/desktop/api/Perflib/nf-perflib-perfaddcounters) , чтобы добавить запрос в обработчик запроса.
- Используйте [**перфделетекаунтерс**](/windows/desktop/api/Perflib/nf-perflib-perfdeletecounters) для удаления запроса из маркера запроса.
- Используйте [**перфкуерикаунтеринфо**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterinfo) для получения сведений о текущих запросах к обработчику запроса.
- Используйте [**перфкуерикаунтердата**](/windows/desktop/api/Perflib/nf-perflib-perfquerycounterdata) , чтобы получить данные о производительности из маркера запроса.

Если потребитель будет потреблять данные только от конкретного поставщика, где индексы GUID и счетчика стабильны и у вас есть доступ к файлу символов, созданному [КТРПП](ctrpp.md)(из `-ch` параметра КТРПП), можно жестко кодировать значения GUID и индекса счетчиков в наборе счетчиков в потребителе.

В противном случае необходимо загрузить метаданные CounterSet, чтобы определить идентификаторы GUID и индексы счетчика, которые будут использоваться в запросе, следующим образом:

- Чтобы получить список поддерживаемых идентификаторов GUID набора счетчиков, используйте **перфенумератекаунтерсет** .
- Для каждого идентификатора GUID используйте **перфкуерикаунтерсетрегистратионинфо** для загрузки имени CounterSet. При обнаружении искомого имени закройте его.
- Используйте **перфкуерикаунтерсетрегистратионинфо** для загрузки оставшихся метаданных (конфигурация CounterSet, имена счетчиков, индексы счетчиков, типы счетчиков) для этого CounterSet.

Если нужно просто знать имена текущих экземпляров набора счетчиков (т. е. Если фактические значения данных производительности не нужны), можно использовать **перфенумератекаунтерсетинстанцес**. Это принимает идентификатор GUID набора счетчиков в качестве входных данных и возвращает `PERF_INSTANCE_HEADER` блок с именами и идентификаторами текущих активных экземпляров данного набора счетчиков.

### <a name="queries"></a>Запросы

Чтобы получить данные о производительности, необходимо создать обработчик запроса, добавить в него запросы и получить данные из запросов.

С обработчиком запросов может быть связано много запросов. При вызове **перфкуерикаунтердата** для обработчика запроса PerfLib будет выполнять все запросы к этому обработчику и получать все результаты.

Каждый запрос указывает идентификатор GUID CounterSet, фильтр имени экземпляра, необязательный фильтр ИДЕНТИФИКАТОРов экземпляра и фильтр необязательного идентификатора счетчика.

- Требуется идентификатор GUID CounterSet. Указывает идентификатор GUID набора счетчиков, из которого запрос будет выполнять накопление данных. Это похоже на `FROM` предложение SQL-запроса.
- Требуется фильтр имени экземпляра. Он указывает шаблон с подстановочным знаком, которому должно соответствовать имя экземпляра, если экземпляр должен быть добавлен в запрос, с `*` указанием «любых символов» и `?` указанием «один символ». Для каунтерсетс с одним экземпляром **необходимо** задать строку нулевой длины `""` . Для каунтерсетс нескольких экземпляров это значение **должно** быть непустой строкой (используйте `"*"` для принятия всех имен экземпляров). Это похоже на `WHERE InstanceName LIKE NameFilter` предложение SQL-запроса.
- Фильтр ИДЕНТИФИКАТОРов экземпляров является необязательным. Если он есть (т. е. Если задано значение `0xFFFFFFFF` , отличное от), это означает, что запрос должен выполнять только те экземпляры, в которых идентификатор экземпляра совпадает с указанным идентификатором. Если отсутствует (т. е. Если задано значение `0xFFFFFFFF` ), это означает, что запрос должен принимать все идентификаторы экземпляров. Это похоже на `WHERE InstanceId == IdFilter` предложение SQL-запроса.
- Фильтр по ИДЕНТИФИКАТОРу счетчика является необязательным. Если он есть (т. е. Если задано значение `PERF_WILDCARD_COUNTER` , отличное от), это означает, что запрос должен состоять из одного счетчика, аналогичного `SELECT CounterName` ПРЕДЛОЖЕНию SQL-запроса. Если отсутствует (т. е. Если задано значение `PERF_WILDCARD_COUNTER` ), это означает, что запрос должен выполнять все доступные счетчики аналогично `SELECT *` ПРЕДЛОЖЕНию SQL-запроса.

Используйте **перфаддкаунтерс** для добавления запросов в обработчик запроса. Используйте **перфделетекаунтерс** для удаления запросов из маркера запроса.

После изменения запросов в обработчике запроса используйте **перфкуерикаунтеринфо** для получения индексов запросов. Индексы указывают порядок, в котором результаты запроса будут возвращены функцией **перфкуерикаунтердата** (результаты не всегда будут соответствовать порядку добавления запросов).

После подготовки обработчика запроса используйте **перфкуерикаунтердата** , чтобы получить данные. Обычно данные периодически собираются (один раз в минуту), а затем обрабатывают данные по мере необходимости.

> [!NOTE]
> Счетчики производительности не предназначены для сбора более одного раза в секунду.

**Перфкуерикаунтердата** будет возвращать `PERF_DATA_HEADER` блок, состоящий из заголовка данных с отметками времени, за которым следует последовательность `PERF_COUNTER_HEADER` блоков, каждая из которых содержит результаты одного запроса.

`PERF_COUNTER_HEADER`Может содержать различные типы данных, как указано в значении `dwType` поля:

- `PERF_ERROR_RETURN` -PerfLib не может получить допустимые данные счетчика от поставщика.
- `PERF_SINGLE_COUNTER` — Запрос был для одного счетчика из одного экземпляра счетчика. Результаты содержат только запрошенное значение счетчика.
- `PERF_MULTIPLE_COUNTERS` — Запрос был создан для нескольких счетчиков из одного экземпляра счетчика. Результат содержит значения счетчиков вместе со сведениями для сопоставления каждого значения с соответствующим счетчиком (т. е. заголовки столбцов).
- `PERF_MULTIPLE_INSTANCES` — Запрос был для одного счетчика из множества счетчиков с несколькими экземплярами. Результаты содержат сведения об экземпляре (т. е. заголовки строк) и одно значение счетчика на один экземпляр.
- `PERF_COUNTERSET` — Запрос был создан для нескольких счетчиков из множества счетчиков с несколькими экземплярами. Результаты содержат сведения об экземпляре (т. е. заголовки строк), значения счетчиков для каждого экземпляра и сведения для сопоставления каждого значения с соответствующим счетчиком (т. е. заголовки столбцов).

Значения, возвращаемые функцией **перфкуерикаунтердата** , — `UINT32` или `UINT64` необработанные значения. Как правило, для получения ожидаемых отформатированных значений обычно требуется определенная обработка. Требуемая обработка зависит от типа счетчика. Многим типам счетчиков требуются дополнительные сведения для завершения обработки, такие как отметка времени или значение из базового счетчика в одном и том же примере.

Некоторые типы счетчиков являются "разностными" счетчиками, которые имеют смысл только при сравнении с данными из предыдущего примера. Например, счетчик типа `PERF_SAMPLE_COUNTER` имеет отформатированное значение, которое должно показывать скорость (количество вхождений определенного элемента в секунду в течение интервала выборки), но фактическое необработанное значение — это просто количество (количество появлений определенного объекта). Чтобы получить отформатированное значение Rate, необходимо применить формулу, соответствующую типу счетчика. Формула для `PERF_SAMPLE_COUNTER` `(N1 - N0) / ((T1 - T0) / F)` : вычитание значения текущей выборки из предыдущего примера (с последующим количеством событий в течение интервала выборки), а затем деление результата на количество секунд в интервале выборки (получено путем вычитания отметки времени текущей выборки из метки времени предыдущей выборки и деления на частоту для преобразования TimeSpan в секунды).

Дополнительные сведения о вычислении форматированных значений из необработанных значений см. в разделе [Вычисление значений счетчиков](calculating-counter-values.md) .

## <a name="sample"></a>Образец

В следующем коде реализуется потребитель, использующий функции-потребители версии PerfLib v2 для чтения сведений о производительности ЦП из счетчика "сведения о процессоре".

Потребитель организован следующим образом:

- `CpuPerfCounters`Класс реализует логику для использования данных о производительности. Он инкапсулирует обработчик запроса и буфер данных, в которые записываются результаты запроса.
- `CpuPerfTimestamp`Структура хранит сведения о метке времени для образца. Каждый раз при сборе данных вызывающий объект получает один `CpuPerfTimestamp` .
- `CpuPerfData`Структура хранит сведения о производительности (имя экземпляра и необработанные значения производительности) для одного ЦП. Каждый раз при сборе данных вызывающий объект получает массив `CpuPerfData` (по одному на ЦП).

В этом образце используются жестко закодированные идентификаторы GUID и ИДЕНТИФИКАТОРы счетчиков, так как они оптимизированы для конкретного CounterSet (сведения о процессоре), который не изменяет значения GUID или ID. Более универсальный класс, считывающий данные производительности из произвольных каунтерсетс, должен будет использовать **перфкуерикаунтерсетрегистратионинфо** для поиска сопоставления между идентификаторами счетчиков и значениями счетчиков во время выполнения.

Простая `CpuPerfCountersConsumer.cpp` программа показывает, как использовать значения из `CpuPerfCounters` класса.

### <a name="cpuperfcountersh"></a>Кпуперфкаунтерс. h

```cpp
#pragma once
#include <sal.h>

// Contains timestamp data for a Processor Information data collection.
struct CpuPerfTimestamp
{
    __int64 PerfTimeStamp;   // Timestamp from the high-resolution clock.
    __int64 PerfTime100NSec; // The number of 100 nanosecond intervals since January 1, 1601, in Coordinated Universal Time (UTC).
    __int64 PerfFreq;        // The frequency of the high-resolution clock.
};

// Contains the raw data from a Processor Information sample.
// Note that the values returned are raw data. Converting from raw data to a
// friendly value may require computation, and the computation may require
// two samples of data. The computation depends on the Type, and the formula
// to use for each type can be found on MSDN.
// For example, ProcessorTime contains raw data of type PERF_100NSEC_TIMER_INV.
// Given two samples of data, s0 at time t0 and s1 at time t1, the friendly
// "% Processor Time" value is computed as:
// 100*(1-(s1.ProcessorTime-s0.ProcessorTime)/(t1.PerfTime100NSec-t0.PerfTime100NSec))
struct CpuPerfData
{
    wchar_t Name[16]; // Format: "NumaNode,NumaIndex", "NumaNode,_Total", or "_Total".
    __int64 unsigned ProcessorTime; // % Processor Time (#0, Type=PERF_100NSEC_TIMER_INV)
    __int64 unsigned UserTime; // % User Time (#1, Type=PERF_100NSEC_TIMER)
    __int64 unsigned PrivilegedTime; // % Privileged Time (#2, Type=PERF_100NSEC_TIMER)
    __int32 unsigned Interrupts; // Interrupts / sec (#3, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned DpcTime; // % DPC Time (#4, Type=PERF_100NSEC_TIMER)
    __int64 unsigned InterruptTime; // % Interrupt Time (#5, Type=PERF_100NSEC_TIMER)
    __int32 unsigned DpcsQueued; // DPCs Queued / sec (#6, Type=PERF_COUNTER_COUNTER)
    __int32 unsigned Dpcs; // DPC Rate (#7, Type=PERF_COUNTER_RAWCOUNT)
    __int64 unsigned IdleTime; // % Idle Time (#8, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Time; // % C1 Time (#9, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C2Time; // % C2 Time (#10, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C3Time; // % C3 Time (#11, Type=PERF_100NSEC_TIMER)
    __int64 unsigned C1Transitions; // C1 Transitions / sec (#12, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C2Transitions; // C2 Transitions / sec (#13, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned C3Transitions; // C3 Transitions / sec (#14, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned PriorityTime; // % Priority Time (#15, Type=PERF_100NSEC_TIMER_INV)
    __int32 unsigned ParkingStatus; // Parking Status (#16, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorFrequency; // Processor Frequency (#17, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PercentMaximumFrequency; // % of Maximum Frequency (#18, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ProcessorStateFlags; // Processor State Flags (#19, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned ClockInterrupts; // Clock Interrupts / sec (#20, Type=PERF_COUNTER_COUNTER)
    __int64 unsigned AverageIdleTime; // Average Idle Time (#21, Type=PERF_PRECISION_100NS_TIMER)
    __int64 unsigned AverageIdleTimeBase; // Average Idle Time Base (#22, Type=PERF_PRECISION_TIMESTAMP)
    __int64 unsigned IdleBreakEvents; // Idle Break Events / sec (#23, Type=PERF_COUNTER_BULK_COUNT)
    __int64 unsigned ProcessorPerformance; // % Processor Performance (#24, Type=PERF_AVERAGE_BULK)
    __int32 unsigned ProcessorPerformanceBase; // % Processor Performance Base (#25, Type=PERF_AVERAGE_BASE)
    __int64 unsigned ProcessorUtility; // % Processor Utility (#26, Type=PERF_AVERAGE_BULK)
    __int64 unsigned PrivilegedUtility; // % Privileged Utility (#28, Type=PERF_AVERAGE_BULK)
    __int32 unsigned UtilityBase; // % Utility Base (#27, Type=PERF_AVERAGE_BASE)
    __int32 unsigned PercentPerformanceLimit; // % Performance Limit (#30, Type=PERF_COUNTER_RAWCOUNT)
    __int32 unsigned PerformanceLimitFlags; // Performance Limit Flags (#31, Type=PERF_COUNTER_RAWCOUNT)
};

// Performs data collection from the Processor Information performance counter.
class CpuPerfCounters
{
public:

    CpuPerfCounters(CpuPerfCounters const&) = delete;
    void operator=(CpuPerfCounters const&) = delete;

    ~CpuPerfCounters();
    CpuPerfCounters() noexcept;

    // Reads CPU performance counter data.
    // Returns ERROR_SUCCESS (0) on success, ERROR_MORE_DATA if bufferCount is
    // too small, or another Win32 error code on failure.
    _Success_(return == 0)
    unsigned
    ReadData(
        _Out_opt_ CpuPerfTimestamp* timestamp,
        _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
        unsigned bufferCount,
        _Out_ unsigned* bufferUsed) noexcept;

private:

    void* m_hQuery;
    void* m_pData;
    unsigned m_cbData;
};
```

### <a name="cpuperfcounterscpp"></a>Кпуперфкаунтерс. cpp

```cpp
#include "CpuPerfCounters.h"
#include <windows.h>
#include <perflib.h>
#include <winperf.h>
#include <stdlib.h>

_Check_return_ _Ret_maybenull_ _Post_writable_byte_size_(cb)
static void*
AllocateBytes(unsigned cb) noexcept
{
    return malloc(cb);
}

static void
FreeBytes(_Pre_maybenull_ _Post_invalid_ void* p) noexcept
{
    if (p)
    {
        free(p);
    }
    return;
}

static void
AssignCounterValue(
    _Inout_ __int32 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 4 ||
        pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

static void
AssignCounterValue(
    _Inout_ __int64 unsigned* pVar,
    _In_ PERF_COUNTER_DATA const* pData) noexcept
{
    if (pData->dwDataSize == 8)
    {
        *pVar = *reinterpret_cast<__int64 unsigned const*>(pData + 1);
    }
    else if (pData->dwDataSize == 4)
    {
        *pVar = *reinterpret_cast<__int32 unsigned const*>(pData + 1);
    }
}

CpuPerfCounters::~CpuPerfCounters()
{
    if (m_hQuery)
    {
        PerfCloseQueryHandle(m_hQuery);
    }

    FreeBytes(m_pData);
}

CpuPerfCounters::CpuPerfCounters() noexcept
    : m_hQuery()
    , m_pData()
    , m_cbData()
{
    return;
}

_Success_(return == 0)
unsigned
CpuPerfCounters::ReadData(
    _Out_opt_ CpuPerfTimestamp* timestamp,
    _Out_cap_post_count_(bufferCount, *bufferUsed) CpuPerfData* buffer,
    unsigned bufferCount,
    _Out_ unsigned* bufferUsed) noexcept
{
    unsigned status;
    DWORD cbData;
    PERF_DATA_HEADER* pDataHeader;
    PERF_COUNTER_HEADER const* pCounterHeader;
    PERF_MULTI_COUNTERS const* pMultiCounters;
    PERF_MULTI_INSTANCES const* pMultiInstances;
    PERF_INSTANCE_HEADER const* pInstanceHeader;
    unsigned cInstances = 0;

    if (m_hQuery == nullptr)
    {
        HANDLE hQuery = 0;
        status = PerfOpenQueryHandle(nullptr, &hQuery);
        if (ERROR_SUCCESS != status)
        {
            goto Done;
        }

        struct
        {
            PERF_COUNTER_IDENTIFIER Identifier;
            WCHAR Name[4];
        } querySpec = {
            {
                // ProcessorCounterSetGuid
                { 0xb4fc721a, 0x378, 0x476f, 0x89, 0xba, 0xa5, 0xa7, 0x9f, 0x81, 0xb, 0x36 },
                0,
                sizeof(querySpec),
                PERF_WILDCARD_COUNTER, // Get all data for each CPU.
                0xFFFFFFFF // Get data for all instance IDs.
            },
            L"*" // Get data for all instance names.
        };

        status = PerfAddCounters(hQuery, &querySpec.Identifier, sizeof(querySpec));
        if (ERROR_SUCCESS == status)
        {
            status = querySpec.Identifier.Status;
        }

        if (ERROR_SUCCESS != status)
        {
            PerfCloseQueryHandle(hQuery);
            goto Done;
        }

        // NOTE: A program that adds more than one query to the handle would need to call
        // PerfQueryCounterInfo to determine the order of the query results.

        m_hQuery = hQuery;
    }

    for (;;)
    {
        cbData = 0;
        pDataHeader = static_cast<PERF_DATA_HEADER*>(m_pData);
        status = PerfQueryCounterData(m_hQuery, pDataHeader, m_cbData, &cbData);
        if (ERROR_SUCCESS == status)
        {
            break;
        }
        else if (ERROR_NOT_ENOUGH_MEMORY != status)
        {
            goto Done;
        }

        FreeBytes(m_pData);
        m_cbData = 0;

        m_pData = AllocateBytes(cbData);
        if (nullptr == m_pData)
        {
            status = ERROR_OUTOFMEMORY;
            goto Done;
        }

        m_cbData = cbData;
    }

    // PERF_DATA_HEADER block = PERF_DATA_HEADER + dwNumCounters PERF_COUNTER_HEADER blocks
    if (cbData < sizeof(PERF_DATA_HEADER) ||
        cbData < pDataHeader->dwTotalSize ||
        pDataHeader->dwTotalSize < sizeof(PERF_DATA_HEADER) ||
        pDataHeader->dwNumCounters != 1)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_COUNTERSET block = PERF_COUNTER_HEADER + PERF_MULTI_COUNTERS block + PERF_MULTI_INSTANCES block
    cbData = pDataHeader->dwTotalSize - sizeof(PERF_DATA_HEADER);
    pCounterHeader = reinterpret_cast<PERF_COUNTER_HEADER*>(pDataHeader + 1);
    if (cbData < sizeof(PERF_COUNTER_HEADER) ||
        cbData < pCounterHeader->dwSize ||
        pCounterHeader->dwSize < sizeof(PERF_COUNTER_HEADER) ||
        PERF_COUNTERSET != pCounterHeader->dwType)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_COUNTERS block = PERF_MULTI_COUNTERS + dwCounters DWORDs
    cbData = pCounterHeader->dwSize - sizeof(PERF_COUNTER_HEADER);
    pMultiCounters = reinterpret_cast<PERF_MULTI_COUNTERS const*>(pCounterHeader + 1);
    if (cbData < sizeof(PERF_MULTI_COUNTERS) ||
        cbData < pMultiCounters->dwSize ||
        pMultiCounters->dwSize < sizeof(PERF_MULTI_COUNTERS) ||
        (pMultiCounters->dwSize - sizeof(PERF_MULTI_COUNTERS)) / sizeof(DWORD) < pMultiCounters->dwCounters)
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    // PERF_MULTI_INSTANCES block = PERF_MULTI_INSTANCES + dwInstances instance data blocks
    cbData -= pMultiCounters->dwSize;
    pMultiInstances = reinterpret_cast<PERF_MULTI_INSTANCES const*>((LPCBYTE)pMultiCounters + pMultiCounters->dwSize);
    if (cbData < sizeof(PERF_MULTI_INSTANCES) ||
        cbData < pMultiInstances->dwTotalSize ||
        pMultiInstances->dwTotalSize < sizeof(PERF_MULTI_INSTANCES))
    {
        status = ERROR_INVALID_DATA;
        goto Done;
    }

    cInstances = pMultiInstances->dwInstances;
    if (bufferCount < cInstances)
    {
        status = ERROR_MORE_DATA;
        goto Done;
    }

    memset(buffer, 0, sizeof(buffer[0]) * cInstances);

    cbData = pMultiInstances->dwTotalSize - sizeof(PERF_MULTI_INSTANCES);
    pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pMultiInstances + 1);
    for (unsigned iInstance = 0; iInstance != pMultiInstances->dwInstances; iInstance += 1)
    {
        CpuPerfData& d = buffer[iInstance];

        // instance data block = PERF_INSTANCE_HEADER block + dwCounters PERF_COUNTER_DATA blocks
        if (cbData < sizeof(PERF_INSTANCE_HEADER) ||
            cbData < pInstanceHeader->Size ||
            pInstanceHeader->Size < sizeof(PERF_INSTANCE_HEADER))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        unsigned const instanceNameMax = (pInstanceHeader->Size - sizeof(PERF_INSTANCE_HEADER)) / sizeof(WCHAR);
        WCHAR const* const instanceName = reinterpret_cast<WCHAR const*>(pInstanceHeader + 1);
        if (instanceNameMax == wcsnlen(instanceName, instanceNameMax))
        {
            status = ERROR_INVALID_DATA;
            goto Done;
        }

        wcsncpy_s(d.Name, instanceName, _TRUNCATE);

        cbData -= pInstanceHeader->Size;
        PERF_COUNTER_DATA const* pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pInstanceHeader + pInstanceHeader->Size);
        for (unsigned iCounter = 0; iCounter != pMultiCounters->dwCounters; iCounter += 1)
        {
            if (cbData < sizeof(PERF_COUNTER_DATA) ||
                cbData < pCounterData->dwSize ||
                pCounterData->dwSize < sizeof(PERF_COUNTER_DATA) + 8 ||
                pCounterData->dwSize - sizeof(PERF_COUNTER_DATA) < pCounterData->dwDataSize)
            {
                status = ERROR_INVALID_DATA;
                goto Done;
            }

            DWORD const* pCounterIds = reinterpret_cast<DWORD const*>(pMultiCounters + 1);
            switch (pCounterIds[iCounter])
            {
            case 0: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.ProcessorTime, pCounterData);
                break;
            case 1: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.UserTime, pCounterData);
                break;
            case 2: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.PrivilegedTime, pCounterData);
                break;
            case 3: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.Interrupts, pCounterData);
                break;
            case 4: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.DpcTime, pCounterData);
                break;
            case 5: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.InterruptTime, pCounterData);
                break;
            case 6: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.DpcsQueued, pCounterData);
                break;
            case 7: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.Dpcs, pCounterData);
                break;
            case 8: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.IdleTime, pCounterData);
                break;
            case 9: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C1Time, pCounterData);
                break;
            case 10: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C2Time, pCounterData);
                break;
            case 11: // PERF_100NSEC_TIMER
                AssignCounterValue(&d.C3Time, pCounterData);
                break;
            case 12: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C1Transitions, pCounterData);
                break;
            case 13: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C2Transitions, pCounterData);
                break;
            case 14: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.C3Transitions, pCounterData);
                break;
            case 15: // PERF_100NSEC_TIMER_INV
                AssignCounterValue(&d.PriorityTime, pCounterData);
                break;
            case 16: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ParkingStatus, pCounterData);
                break;
            case 17: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorFrequency, pCounterData);
                break;
            case 18: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentMaximumFrequency, pCounterData);
                break;
            case 19: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.ProcessorStateFlags, pCounterData);
                break;
            case 20: // PERF_COUNTER_COUNTER
                AssignCounterValue(&d.ClockInterrupts, pCounterData);
                break;
            case 21: // PERF_PRECISION_100NS_TIMER
                AssignCounterValue(&d.AverageIdleTime, pCounterData);
                break;
            case 22: // PERF_PRECISION_TIMESTAMP
                AssignCounterValue(&d.AverageIdleTimeBase, pCounterData);
                break;
            case 23: // PERF_COUNTER_BULK_COUNT
                AssignCounterValue(&d.IdleBreakEvents, pCounterData);
                break;
            case 24: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorPerformance, pCounterData);
                break;
            case 25: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.ProcessorPerformanceBase, pCounterData);
                break;
            case 26: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.ProcessorUtility, pCounterData);
                break;
            case 28: // PERF_AVERAGE_BULK
                AssignCounterValue(&d.PrivilegedUtility, pCounterData);
                break;
            case 27: // PERF_AVERAGE_BASE
                AssignCounterValue(&d.UtilityBase, pCounterData);
                break;
            case 30: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PercentPerformanceLimit, pCounterData);
                break;
            case 31: // PERF_COUNTER_RAWCOUNT
                AssignCounterValue(&d.PerformanceLimitFlags, pCounterData);
                break;
            }

            cbData -= pCounterData->dwSize;
            pCounterData = reinterpret_cast<PERF_COUNTER_DATA const*>((LPCBYTE)pCounterData + pCounterData->dwSize);
        }

        pInstanceHeader = reinterpret_cast<PERF_INSTANCE_HEADER const*>(pCounterData);
    }

    if (nullptr != timestamp)
    {
        timestamp->PerfTimeStamp = pDataHeader->PerfTimeStamp;
        timestamp->PerfTime100NSec = pDataHeader->PerfTime100NSec;
        timestamp->PerfFreq = pDataHeader->PerfFreq;
    }

    status = ERROR_SUCCESS;

Done:

    *bufferUsed = cInstances;
    return status;
}
```

### <a name="cpuperfcountersconsumercpp"></a>Кпуперфкаунтерсконсумер. cpp

```cpp
#include <windows.h>
#include <stdio.h>
#include "CpuPerfCounters.h"
#include <utility>

int wmain()
{
    unsigned status;
    unsigned const dataMax = 30; // Support up to 30 instances
    CpuPerfCounters cpc;
    CpuPerfTimestamp timestamp[2];
    CpuPerfTimestamp* t0 = timestamp + 0;
    CpuPerfTimestamp* t1 = timestamp + 1;
    CpuPerfData data[dataMax * 2];
    CpuPerfData* d0 = data + 0;
    CpuPerfData* d1 = data + dataMax;
    unsigned used;

    status = cpc.ReadData(t0, d0, dataMax, &used);
    printf("ReadData0 used=%u, status=%u\n", used, status);

    for (unsigned iSample = 1; iSample != 10; iSample += 1)
    {
        Sleep(1000);
        status = cpc.ReadData(t1, d1, dataMax, &used);
        printf("ReadData%u used=%u, status=%u\n", iSample, used, status);

        if (status == ERROR_SUCCESS && used != 0)
        {
            // Show the ProcessorTime value from instance #0 (usually the "_Total" instance):
            auto& s0 = d0[0];
            auto& s1 = d1[0];
            printf("  %ls/%ls = %f\n", s0.Name, s1.Name,
                100.0 * (1.0 - static_cast<double>(s1.ProcessorTime - s0.ProcessorTime) / static_cast<double>(t1->PerfTime100NSec - t0->PerfTime100NSec)));

            std::swap(t0, t1); // Swap "current" and "previous" timestamp pointers.
            std::swap(d0, d1); // Swap "current" and "previous" sample pointers.
        }
    }

    return status;
}
```
