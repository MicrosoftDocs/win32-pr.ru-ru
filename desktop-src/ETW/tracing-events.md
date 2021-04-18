---
description: Прежде чем можно будет записывать события в сеанс трассировки, необходимо зарегистрировать поставщик.
ms.assetid: 21f62b5d-0a2d-468c-af88-2fab1512f0ec
title: Запись событий MOF (классическая модель)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3d041e2792540d4a05637bcffdb67e1164a95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986113"
---
# <a name="writing-mof-classic-events"></a>Запись событий MOF (классическая модель)

Прежде чем можно будет записывать события в сеанс трассировки, необходимо зарегистрировать поставщик. Регистрация поставщика сообщает ETW о том, что поставщик готов к записи событий в сеанс трассировки. Процесс может зарегистрировать до 1 024 идентификаторов GUID поставщика. Однако количество поставщиков, которые регистрируется процессом, должно быть ограничено одним или двумя.

**До Windows Vista:** Количество поставщиков, которые может зарегистрировать процесс, не ограничено.

Для регистрации классического поставщика вызовите функцию [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . Функция регистрирует GUID поставщика, идентификаторы GUID класса трассировки событий и определяет обратный вызов, который ETW вызывает, когда контроллер включает или отключает поставщик.

Если поставщик вызывает функцию [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) для записи событий в журнал, не нужно ВКЛЮЧАТЬ массив идентификаторов GUID класса (может иметь **значение NULL**) при вызове функции [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) . Необходимо включить массив, только если поставщик вызывает функцию [**трацеевентинстанце**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) для регистрации событий.

**Windows XP и windows 2000:** Необходимо всегда включать массив идентификаторов GUID класса (не может иметь **значение NULL**).

После того как поставщик регистрируется и активируется контроллером, поставщик может регистрировать события в сеансе трассировки контроллера.

Перед завершением работы поставщика вызовите функцию [**унрегистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) , чтобы удалить регистрацию поставщика из ETW. Функция [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) возвращает маркер регистрации, передаваемый в функцию **унрегистертрацегуидс** .

Если поставщик регистрирует события в глобальном сеансе ведения журнала, нет необходимости регистрировать поставщик в ETW, так как глобальный контроллер ведения журнала не включает и не отключает поставщиков. Дополнительные сведения см. [в разделе Настройка и запуск сеанса глобального журнала](configuring-and-starting-the-global-logger-session.md).

Все [классические](about-event-tracing.md) поставщики (за исключением тех, которые отслеживают события в сеансе глобального журнала) должны реализовывать функцию [**контролкаллбакк**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) . Поставщик использует сведения в обратном вызове для определения его включения или отключения, а также записываемых событий.

Поставщик указывает имя функции обратного вызова при вызове функции [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) для ее регистрации. ETW вызывает функцию обратного вызова, когда контроллер вызывает функцию [**енаблетраце**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) для включения или отключения поставщика.

В реализации [**контролкаллбакк**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) необходимо вызвать функцию [**жеттрацелогжерхандле**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) , чтобы получить маркер сеанса. При вызове функции [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) используется обработчик сеанса. Необходимо вызвать функцию [**жеттрацеенаблефлагс**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) или функцию [**Жеттрацеенаблелевел**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) в реализации **контролкаллбакк** , если ваш поставщик использует флаги включения или включения.

Поставщик может регистрировать события трассировки только в одном сеансе, но не существует никаких действий для предотвращения включения одного поставщика несколькими контроллерами. Чтобы другой контроллер не перенаправлял события трассировки в сеанс, может потребоваться добавить логику в реализацию [**контролкаллбакк**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) для сравнения дескрипторов сеанса и игнорировать запросы на включение из других контроллеров.

Чтобы регистрировать события, [классические](about-event-tracing.md) Поставщики вызывают функцию [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) . Событие состоит из структуры [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) и любых данных, связанных с событием, которые добавляются к заголовку.

Заголовок должен содержать следующие сведения:

-   Элемент **size** должен содержать общее число байтов, которое должно быть записано для события (включая размер структуры [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) и сведения о событиях, которые добавляются к заголовку).
-   Элемент **GUID** должен содержать идентификатор GUID класса события (или член **гуидптр** должен содержать указатель на идентификатор GUID класса).

    **Windows XP и windows 2000:** Идентификатор GUID класса должен быть зарегистрирован ранее с помощью функции [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .

-   Элемент **flags** должен содержать флаг флага **вноде \_ \_ traceed \_ GUID** . Если вы указали идентификатор GUID класса с помощью члена **гуидптр** , также добавьте флаг вноде для параметра **\_ \_ \_ GUID \_ ptr** .
-   Член **Class. Type** должен содержать тип события, если для публикации макета данных события используется MOF.
-   Член **класса. Version** должен содержать версию события, если для публикации макета данных события используется MOF. Версия используется для различения редакций с данными событий. Присвойте начальному номеру версии значение 0.

Если вы пишете как поставщик, так и потребитель, можно использовать структуру для заполнения данных, связанных с событием, которые добавляются к заголовку. Однако, если вы используете MOF для публикации данных, связанных с событиями, чтобы любой потребитель мог обработать событие, не следует использовать структуру для добавления в заголовок данных, относящихся к событию. Это связано с тем, что компилятор может добавлять дополнительные байты в данные, относящиеся к событию, для целей выравнивания байтов. Поскольку определение MOF не учитывает дополнительные байты, потребитель может извлекать недопустимые данные.

Следует либо выделить блок памяти для события и скопировать каждый элемент данных события в память, либо создать структуру, включающую в себя массив структур [**\_ полей MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) ; большинство приложений создаст структуру, включающую в себя массив структур **\_ полей MOF** . Убедитесь, что **заголовок. size** отражает фактическое число структур **\_ полей MOF** , которые фактически задаются перед записью события в журнал. Например, если событие содержит три поля данных, задайте **заголовок. size** для sizeof ( \_ заголовок трассировки событий \_ ) + (sizeof ( \_ поле MOF) \* 3).

Сведения о событиях, связанных с трассировкой, см. [в разделе Написание связанных событий в комплексном сценарии](writing-related-events-in-an-end-to-end-scenario.md).

В следующем примере показано, как вызвать функцию [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) для записи событий в журнал. В этом примере указываются события, определенные при [публикации схемы событий для классического поставщика](publishing-your-event-schema-for-a-classic-provider.md).


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

// GUID that identifies the category of events that the provider can log. 
// The GUID is also used in the event MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {B49D5931-AD85-4070-B1B1-3F81F1532875}
static const GUID MyCategoryGuid = 
{ 0xb49d5931, 0xad85, 0x4070, { 0xb1, 0xb1, 0x3f, 0x81, 0xf1, 0x53, 0x28, 0x75 } };

// GUID that identifies the provider that you are registering.
// The GUID is also used in the provider MOF class. 
// Remember to change this GUID if you copy and paste this example.

// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };

// Identifies the event type within the MyCategoryGuid category 
// of events to be logged. This is the same value as the EventType 
// qualifier that is defined in the event type MOF class for one of 
// the MyCategoryGuid category of events.

#define MY_EVENT_TYPE 1

// Event passed to TraceEvent

typedef struct _event
{
    EVENT_TRACE_HEADER Header;
    MOF_FIELD Data[MAX_MOF_FIELDS];  // Event-specific data
} MY_EVENT, *PMY_EVENT;

#define MAX_INDICES            3
#define MAX_SIGNATURE_LEN      32
#define EVENT_DATA_FIELDS_CNT  6

// Application data to be traced for Version 1 of the MOF class.

typedef struct _evtdata
{
    LONG Cost;
    DWORD Indices[MAX_INDICES];
    WCHAR Signature[MAX_SIGNATURE_LEN];
    BOOL IsComplete;
    GUID ID;
    DWORD Size;
}EVENT_DATA, *PEVENT_DATA;

// GUID used as the value for EVENT_DATA.ID.

// {25BAEDA9-C81A-4889-8764-184FE56750F2}
static const GUID tempID = 
{ 0x25baeda9, 0xc81a, 0x4889, { 0x87, 0x64, 0x18, 0x4f, 0xe5, 0x67, 0x50, 0xf2 } };

// Global variables to store tracing state information.

TRACEHANDLE g_SessionHandle = 0; // The handle to the session that enabled the provider.
ULONG g_EnableFlags = 0; // Determines which class of events to log.
UCHAR g_EnableLevel = 0; // Determines the severity of events to log.
BOOL g_TraceOn = FALSE;  // Used by the provider to determine whether it should log events.

ULONG WINAPI ControlCallback(WMIDPREQUESTCODE RequestCode, PVOID Context, ULONG* Reserved, PVOID Header);

// For this example to log the event, run the session example
// to enable the provider before running this example.

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_DATA EventData;
    MY_EVENT MyEvent; 
    TRACEHANDLE RegistrationHandle = 0; 
    TRACE_GUID_REGISTRATION EventClassGuids[] = {
        (LPGUID)&MyCategoryGuid, NULL
        };

    // Register the provider and specify the control callback function
    // that receives the enable/disable notifications.

    status = RegisterTraceGuids(
        (WMIDPREQUEST)ControlCallback,
        NULL,
        (LPGUID)&ProviderGuid,
        sizeof(EventClassGuids)/sizeof(TRACE_GUID_REGISTRATION),
        EventClassGuids,
        NULL,
        NULL,
        &RegistrationHandle
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegisterTraceGuids failed with %lu\n", status);
        goto cleanup;
    }

    // Set the event-specific data.

    EventData.Cost = 32;
    EventData.ID = tempID;
    EventData.Indices[0] = 4;
    EventData.Indices[1] = 5;
    EventData.Indices[2] = 6;
    EventData.IsComplete = TRUE;
    wcscpy_s(EventData.Signature, MAX_SIGNATURE_LEN, L"Signature");
    EventData.Size = 1024;

    // Log the event if the provider is enabled and the session
    // passed a severity level value >= TRACE_LEVEL_ERROR (or zero).
    // If your provider generates more than one class of events, you
    // would also need to check g_EnableFlags.

    if (g_TraceOn && (0 == g_EnableLevel || TRACE_LEVEL_ERROR <= g_EnableLevel))
    {
        // Initialize the event data structure.

        ZeroMemory(&MyEvent, sizeof(MY_EVENT));
        MyEvent.Header.Size = sizeof(EVENT_TRACE_HEADER) + (sizeof(MOF_FIELD) * EVENT_DATA_FIELDS_CNT);
        MyEvent.Header.Flags = WNODE_FLAG_TRACED_GUID | WNODE_FLAG_USE_MOF_PTR;
        MyEvent.Header.Guid = MyCategoryGuid;
        MyEvent.Header.Class.Type = MY_EVENT_TYPE;
        MyEvent.Header.Class.Version = 1;
        MyEvent.Header.Class.Level = g_EnableLevel;

        // Load the event data. You can also use the DEFINE_TRACE_MOF_FIELD
        // macro defined in evntrace.h to set the MOF_FIELD members. For example,
        // DEFINE_TRACE_MOF_FIELD(&EventData.Data[0], &EventData.Cost, sizeof(EventData.Cost), 0);

        MyEvent.Data[0].DataPtr = (ULONG64) &(EventData.Cost);
        MyEvent.Data[0].Length = sizeof(EventData.Cost);
        MyEvent.Data[1].DataPtr = (ULONG64) &(EventData.Indices);
        MyEvent.Data[1].Length = sizeof(EventData.Indices);
        MyEvent.Data[2].DataPtr = (ULONG64) &(EventData.Signature);
        MyEvent.Data[2].Length = (ULONG)(wcslen(EventData.Signature) + 1) * sizeof(WCHAR);
        MyEvent.Data[3].DataPtr = (ULONG64) &(EventData.IsComplete);
        MyEvent.Data[3].Length = sizeof(EventData.IsComplete);
        MyEvent.Data[4].DataPtr = (ULONG64) &(EventData.ID);
        MyEvent.Data[4].Length = sizeof(EventData.ID);
        MyEvent.Data[5].DataPtr = (ULONG64) &(EventData.Size);
        MyEvent.Data[5].Length = sizeof(EventData.Size);

        // Write the event.

        status = TraceEvent(g_SessionHandle, &(MyEvent.Header));

        if (ERROR_SUCCESS != status)
        {
            // Decide how you want to handle failures. Typically, you do not
            // want to terminate the application because you failed to
            // log an event. If the error is a memory failure, you may
            // may want to log a message to the system event log or turn
            // off logging.

            wprintf(L"TraceEvent() event failed with %lu\n", status);
            g_TraceOn = FALSE;
        }
    }

cleanup:

    if (RegistrationHandle)
    {
        UnregisterTraceGuids(RegistrationHandle);
    }
}


// The callback function that receives enable/disable notifications
// from one or more ETW sessions. Because more than one session
// can enable the provider, this example ignores requests from other 
// sessions if it is already enabled.

ULONG WINAPI ControlCallback(
    WMIDPREQUESTCODE RequestCode,
    PVOID Context,
    ULONG* Reserved, 
    PVOID Header
    )
{
    UNREFERENCED_PARAMETER(Context);
    UNREFERENCED_PARAMETER(Reserved);

    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE TempSessionHandle = 0; 

    switch (RequestCode)
    {
        case WMI_ENABLE_EVENTS:  // Enable the provider.
        {
            SetLastError(0);

            // If the provider is already enabled to a provider, ignore 
            // the request. Get the session handle of the enabling session.
            // You need the session handle to call the TraceEvent function.
            // The session could be enabling the provider or it could be
            // updating the level and enable flags.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (0 == g_SessionHandle)
            {
                g_SessionHandle = TempSessionHandle;
            }
            else if (g_SessionHandle != TempSessionHandle)
            {
                break;
            }

            // Get the severity level of the events that the
            // session wants you to log.

            g_EnableLevel = GetTraceEnableLevel(g_SessionHandle); 
            if (0 == g_EnableLevel)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable level means to your provider.
                    // For this example, it means log all events.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableLevel failed with, %lu.\n", status);
                    break;
                } 
            }

            // Get the enable flags that indicate the events that the
            // session wants you to log. The provider determines the
            // flags values. How it articulates the flag values and 
            // meanings to perspective sessions is up to it.

            g_EnableFlags = GetTraceEnableFlags(g_SessionHandle);
            if (0 == g_EnableFlags)
            {
                // If zero, determine whether the session passed zero
                // or an error occurred.

                if (ERROR_SUCCESS == (status = GetLastError()))
                {
                    // Decide what a zero enable flags value means to your provider.
                    ; 
                }
                else
                {
                    wprintf(L"GetTraceEnableFlags failed with, %lu.\n", status);
                    break;
                }
            }

            g_TraceOn = TRUE;
            break;
        }
 
        case WMI_DISABLE_EVENTS:  // Disable the provider.
        {
            // Disable the provider only if the request is coming from the
            // session that enabled the provider.

            TempSessionHandle = GetTraceLoggerHandle(Header);
            if (INVALID_HANDLE_VALUE == (HANDLE)TempSessionHandle)
            {
                wprintf(L"GetTraceLoggerHandle failed. Error code is %lu.\n", status = GetLastError());
                break;
            }

            if (g_SessionHandle == TempSessionHandle)
            {
                g_TraceOn = FALSE;
                g_SessionHandle = 0;
            }
            break;
        }

        default:
        {
            status = ERROR_INVALID_PARAMETER;
            break;
        }
    }

    return status;
}
```



 

 
