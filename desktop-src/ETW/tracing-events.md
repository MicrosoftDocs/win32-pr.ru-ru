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
# <a name="writing-mof-classic-events"></a><span data-ttu-id="9cb75-103">Запись событий MOF (классическая модель)</span><span class="sxs-lookup"><span data-stu-id="9cb75-103">Writing MOF (Classic) Events</span></span>

<span data-ttu-id="9cb75-104">Прежде чем можно будет записывать события в сеанс трассировки, необходимо зарегистрировать поставщик.</span><span class="sxs-lookup"><span data-stu-id="9cb75-104">Before you can write events to a trace session, you must register your provider.</span></span> <span data-ttu-id="9cb75-105">Регистрация поставщика сообщает ETW о том, что поставщик готов к записи событий в сеанс трассировки.</span><span class="sxs-lookup"><span data-stu-id="9cb75-105">Registering a provider tells ETW that your provider is ready to write events to a trace session.</span></span> <span data-ttu-id="9cb75-106">Процесс может зарегистрировать до 1 024 идентификаторов GUID поставщика. Однако количество поставщиков, которые регистрируется процессом, должно быть ограничено одним или двумя.</span><span class="sxs-lookup"><span data-stu-id="9cb75-106">A process can register up to 1,024 provider GUIDs; however, you should limit the number of providers that your process registers to one or two.</span></span>

<span data-ttu-id="9cb75-107">**До Windows Vista:** Количество поставщиков, которые может зарегистрировать процесс, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="9cb75-107">**Prior to Windows Vista:** There is no limit to the number of providers that a process can register.</span></span>

<span data-ttu-id="9cb75-108">Для регистрации классического поставщика вызовите функцию [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="9cb75-108">To register a classic provider, call the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="9cb75-109">Функция регистрирует GUID поставщика, идентификаторы GUID класса трассировки событий и определяет обратный вызов, который ETW вызывает, когда контроллер включает или отключает поставщик.</span><span class="sxs-lookup"><span data-stu-id="9cb75-109">The function registers the provider's GUID, event trace class GUIDs, and identifies the callback that ETW calls when a controller enables or disables the provider.</span></span>

<span data-ttu-id="9cb75-110">Если поставщик вызывает функцию [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) для записи событий в журнал, не нужно ВКЛЮЧАТЬ массив идентификаторов GUID класса (может иметь **значение NULL**) при вызове функции [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="9cb75-110">If the provider calls the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events, you do not need to include the array of class GUIDs (can be **NULL**) when calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span> <span data-ttu-id="9cb75-111">Необходимо включить массив, только если поставщик вызывает функцию [**трацеевентинстанце**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="9cb75-111">You only need to include the array if the provider calls the [**TraceEventInstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) function to log events.</span></span>

<span data-ttu-id="9cb75-112">**Windows XP и windows 2000:** Необходимо всегда включать массив идентификаторов GUID класса (не может иметь **значение NULL**).</span><span class="sxs-lookup"><span data-stu-id="9cb75-112">**Windows XP and Windows 2000:** You always need to include the array of class GUIDs (cannot be **NULL**).</span></span>

<span data-ttu-id="9cb75-113">После того как поставщик регистрируется и активируется контроллером, поставщик может регистрировать события в сеансе трассировки контроллера.</span><span class="sxs-lookup"><span data-stu-id="9cb75-113">After a provider registers itself and is enabled by the controller, the provider can log events to the controller's trace session.</span></span>

<span data-ttu-id="9cb75-114">Перед завершением работы поставщика вызовите функцию [**унрегистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) , чтобы удалить регистрацию поставщика из ETW.</span><span class="sxs-lookup"><span data-stu-id="9cb75-114">Before the provider exits, call the [**UnregisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-unregistertraceguids) function to remove the provider's registration from ETW.</span></span> <span data-ttu-id="9cb75-115">Функция [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) возвращает маркер регистрации, передаваемый в функцию **унрегистертрацегуидс** .</span><span class="sxs-lookup"><span data-stu-id="9cb75-115">The [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function returns the registration handle that you pass to the **UnregisterTraceGuids** function.</span></span>

<span data-ttu-id="9cb75-116">Если поставщик регистрирует события в глобальном сеансе ведения журнала, нет необходимости регистрировать поставщик в ETW, так как глобальный контроллер ведения журнала не включает и не отключает поставщиков.</span><span class="sxs-lookup"><span data-stu-id="9cb75-116">If your provider logs events to the Global Logger session only, you do not have to register your provider with ETW because the Global Logger controller does not enable or disable providers.</span></span> <span data-ttu-id="9cb75-117">Дополнительные сведения см. [в разделе Настройка и запуск сеанса глобального журнала](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="9cb75-117">For details, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="9cb75-118">Все [классические](about-event-tracing.md) поставщики (за исключением тех, которые отслеживают события в сеансе глобального журнала) должны реализовывать функцию [**контролкаллбакк**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) .</span><span class="sxs-lookup"><span data-stu-id="9cb75-118">All [classic](about-event-tracing.md) providers (except those that trace events to the Global Logger session) must implement the [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) function.</span></span> <span data-ttu-id="9cb75-119">Поставщик использует сведения в обратном вызове для определения его включения или отключения, а также записываемых событий.</span><span class="sxs-lookup"><span data-stu-id="9cb75-119">The provider uses the information in the callback to determine if it is enabled or disabled and which events it should write.</span></span>

<span data-ttu-id="9cb75-120">Поставщик указывает имя функции обратного вызова при вызове функции [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) для ее регистрации.</span><span class="sxs-lookup"><span data-stu-id="9cb75-120">The provider specifies the name of the callback function when it calls the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register itself.</span></span> <span data-ttu-id="9cb75-121">ETW вызывает функцию обратного вызова, когда контроллер вызывает функцию [**енаблетраце**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) для включения или отключения поставщика.</span><span class="sxs-lookup"><span data-stu-id="9cb75-121">ETW calls the callback function when the controller calls the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable or disable the provider.</span></span>

<span data-ttu-id="9cb75-122">В реализации [**контролкаллбакк**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) необходимо вызвать функцию [**жеттрацелогжерхандле**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) , чтобы получить маркер сеанса. При вызове функции [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) используется обработчик сеанса.</span><span class="sxs-lookup"><span data-stu-id="9cb75-122">In your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation, you must call the [**GetTraceLoggerHandle**](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle) function to retrieve the session handle; you use the session handle when calling the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="9cb75-123">Необходимо вызвать функцию [**жеттрацеенаблефлагс**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) или функцию [**Жеттрацеенаблелевел**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) в реализации **контролкаллбакк** , если ваш поставщик использует флаги включения или включения.</span><span class="sxs-lookup"><span data-stu-id="9cb75-123">You only need to call the [**GetTraceEnableFlags**](/windows/win32/api/evntrace/nf-evntrace-gettraceenableflags) function or the [**GetTraceEnableLevel**](/windows/win32/api/evntrace/nf-evntrace-gettraceenablelevel) function in your **ControlCallback** implementation if your provider uses the enable level or enable flags.</span></span>

<span data-ttu-id="9cb75-124">Поставщик может регистрировать события трассировки только в одном сеансе, но не существует никаких действий для предотвращения включения одного поставщика несколькими контроллерами.</span><span class="sxs-lookup"><span data-stu-id="9cb75-124">A provider can log trace events to only one session, but there is nothing to prevent multiple controllers from enabling a single provider.</span></span> <span data-ttu-id="9cb75-125">Чтобы другой контроллер не перенаправлял события трассировки в сеанс, может потребоваться добавить логику в реализацию [**контролкаллбакк**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) для сравнения дескрипторов сеанса и игнорировать запросы на включение из других контроллеров.</span><span class="sxs-lookup"><span data-stu-id="9cb75-125">To prevent another controller from redirecting your trace events to its session, you may want to add logic to your [**ControlCallback**](/windows/win32/api/evntrace/nc-evntrace-wmidprequest) implementation to compare session handles and ignore enable requests from other controllers.</span></span>

<span data-ttu-id="9cb75-126">Чтобы регистрировать события, [классические](about-event-tracing.md) Поставщики вызывают функцию [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) .</span><span class="sxs-lookup"><span data-stu-id="9cb75-126">To log events, [classic](about-event-tracing.md) providers call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function.</span></span> <span data-ttu-id="9cb75-127">Событие состоит из структуры [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) и любых данных, связанных с событием, которые добавляются к заголовку.</span><span class="sxs-lookup"><span data-stu-id="9cb75-127">An event consists of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and any event-specific data that is appended to the header.</span></span>

<span data-ttu-id="9cb75-128">Заголовок должен содержать следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="9cb75-128">The header must contain the following information:</span></span>

-   <span data-ttu-id="9cb75-129">Элемент **size** должен содержать общее число байтов, которое должно быть записано для события (включая размер структуры [**\_ \_ заголовка трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) и сведения о событиях, которые добавляются к заголовку).</span><span class="sxs-lookup"><span data-stu-id="9cb75-129">The **Size** member must contain the total number of bytes to be recorded for the event (including the size of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure and of any event-specific data that is appended to the header).</span></span>
-   <span data-ttu-id="9cb75-130">Элемент **GUID** должен содержать идентификатор GUID класса события (или член **гуидптр** должен содержать указатель на идентификатор GUID класса).</span><span class="sxs-lookup"><span data-stu-id="9cb75-130">The **Guid** member must contain the class GUID of the event (or the **GuidPtr** member must contain a pointer to the class GUID).</span></span>

    <span data-ttu-id="9cb75-131">**Windows XP и windows 2000:** Идентификатор GUID класса должен быть зарегистрирован ранее с помощью функции [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) .</span><span class="sxs-lookup"><span data-stu-id="9cb75-131">**Windows XP and Windows 2000:** The class GUID must have been registered previously using the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function.</span></span>

-   <span data-ttu-id="9cb75-132">Элемент **flags** должен содержать флаг флага **вноде \_ \_ traceed \_ GUID** .</span><span class="sxs-lookup"><span data-stu-id="9cb75-132">The **Flags** member must contain the **WNODE\_FLAG\_TRACED\_GUID** flag.</span></span> <span data-ttu-id="9cb75-133">Если вы указали идентификатор GUID класса с помощью члена **гуидптр** , также добавьте флаг вноде для параметра **\_ \_ \_ GUID \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="9cb75-133">If you specify the class GUID using the **GuidPtr** member, also add the **WNODE\_FLAG\_USE\_GUID\_PTR** flag.</span></span>
-   <span data-ttu-id="9cb75-134">Член **Class. Type** должен содержать тип события, если для публикации макета данных события используется MOF.</span><span class="sxs-lookup"><span data-stu-id="9cb75-134">The **Class.Type** member must contain the event type, if you use MOF to publish the layout of your event data.</span></span>
-   <span data-ttu-id="9cb75-135">Член **класса. Version** должен содержать версию события, если для публикации макета данных события используется MOF.</span><span class="sxs-lookup"><span data-stu-id="9cb75-135">The **Class.Version** member must contain the event version, if you use MOF to publish the layout of your event data.</span></span> <span data-ttu-id="9cb75-136">Версия используется для различения редакций с данными событий.</span><span class="sxs-lookup"><span data-stu-id="9cb75-136">The version is used to distinguish between revisions to the event data.</span></span> <span data-ttu-id="9cb75-137">Присвойте начальному номеру версии значение 0.</span><span class="sxs-lookup"><span data-stu-id="9cb75-137">Set the initial version number to 0.</span></span>

<span data-ttu-id="9cb75-138">Если вы пишете как поставщик, так и потребитель, можно использовать структуру для заполнения данных, связанных с событием, которые добавляются к заголовку.</span><span class="sxs-lookup"><span data-stu-id="9cb75-138">If you write both the provider and the consumer, you can use a structure to populate the event-specific data that is appended to the header.</span></span> <span data-ttu-id="9cb75-139">Однако, если вы используете MOF для публикации данных, связанных с событиями, чтобы любой потребитель мог обработать событие, не следует использовать структуру для добавления в заголовок данных, относящихся к событию.</span><span class="sxs-lookup"><span data-stu-id="9cb75-139">However, if you use MOF to publish the event-specific data so that any consumer can process the event, you should not use a structure to append the event-specific data to the header.</span></span> <span data-ttu-id="9cb75-140">Это связано с тем, что компилятор может добавлять дополнительные байты в данные, относящиеся к событию, для целей выравнивания байтов.</span><span class="sxs-lookup"><span data-stu-id="9cb75-140">This is because the compiler may add extra bytes to the event-specific data for byte alignment purposes.</span></span> <span data-ttu-id="9cb75-141">Поскольку определение MOF не учитывает дополнительные байты, потребитель может извлекать недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="9cb75-141">Because the MOF definition does not account for the extra bytes, the consumer may retrieve data that is not valid.</span></span>

<span data-ttu-id="9cb75-142">Следует либо выделить блок памяти для события и скопировать каждый элемент данных события в память, либо создать структуру, включающую в себя массив структур [**\_ полей MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) ; большинство приложений создаст структуру, включающую в себя массив структур **\_ полей MOF** .</span><span class="sxs-lookup"><span data-stu-id="9cb75-142">You should either allocate a block of memory for the event and copy each event data item to the memory, or create a structure that includes an array of [**MOF\_FIELD**](/windows/win32/api/evntrace/ns-evntrace-mof_field) structures; most applications will create a structure that includes an array of **MOF\_FIELD** structures.</span></span> <span data-ttu-id="9cb75-143">Убедитесь, что **заголовок. size** отражает фактическое число структур **\_ полей MOF** , которые фактически задаются перед записью события в журнал.</span><span class="sxs-lookup"><span data-stu-id="9cb75-143">Make sure that **Header.Size** reflects the actual number of **MOF\_FIELD** structures that are actually set before logging the event.</span></span> <span data-ttu-id="9cb75-144">Например, если событие содержит три поля данных, задайте **заголовок. size** для sizeof ( \_ заголовок трассировки событий \_ ) + (sizeof ( \_ поле MOF) \* 3).</span><span class="sxs-lookup"><span data-stu-id="9cb75-144">For example, if the event contains three data fields, set **Header.Size** to sizeof(EVENT\_TRACE\_HEADER) + (sizeof(MOF\_FIELD) \* 3).</span></span>

<span data-ttu-id="9cb75-145">Сведения о событиях, связанных с трассировкой, см. [в разделе Написание связанных событий в комплексном сценарии](writing-related-events-in-an-end-to-end-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="9cb75-145">For information on tracing related events, see [Writing Related Events in an End-to-End Scenario](writing-related-events-in-an-end-to-end-scenario.md).</span></span>

<span data-ttu-id="9cb75-146">В следующем примере показано, как вызвать функцию [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) для записи событий в журнал.</span><span class="sxs-lookup"><span data-stu-id="9cb75-146">The following example shows how to call the [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) function to log events.</span></span> <span data-ttu-id="9cb75-147">В этом примере указываются события, определенные при [публикации схемы событий для классического поставщика](publishing-your-event-schema-for-a-classic-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9cb75-147">The example references the events defined in [Publishing Your Event Schema for a Classic Provider](publishing-your-event-schema-for-a-classic-provider.md).</span></span>


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



 

 
