---
description: Трассировка событий в DirectShow
ms.assetid: e78c4514-25f4-441d-bfd0-6dac4f7567fd
title: Трассировка событий в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c567d8a2e75d838570323d8ad6be04f11502c9c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682330"
---
# <a name="event-tracing-in-directshow"></a><span data-ttu-id="59382-103">Трассировка событий в DirectShow</span><span class="sxs-lookup"><span data-stu-id="59382-103">Event Tracing in DirectShow</span></span>

<span data-ttu-id="59382-104">DirectShow поддерживает трассировку событий Windows (ETW), которую можно использовать для создания журналов событий для инструментирования или отладки.</span><span class="sxs-lookup"><span data-stu-id="59382-104">DirectShow supports Event Tracing for Windows (ETW), which can be used to create event logs for instrumentation or debugging.</span></span> <span data-ttu-id="59382-105">Дополнительные сведения о трассировке событий Windows см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="59382-105">For more information about ETW, see the Windows SDK documentation.</span></span> <span data-ttu-id="59382-106">Чтобы использовать события ETW в приложении DirectShow, необходимо включить трассировку, а затем обработать события трассировки.</span><span class="sxs-lookup"><span data-stu-id="59382-106">To consume ETW events in a DirectShow application, you must enable tracing and then process the trace events.</span></span> <span data-ttu-id="59382-107">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="59382-107">Use the following steps.</span></span>

<span data-ttu-id="59382-108">**Настройка необходимых разделов реестра**</span><span class="sxs-lookup"><span data-stu-id="59382-108">**Set the Necessary Registry Keys**</span></span>

<span data-ttu-id="59382-109">Чтобы включить трассировку на компьютере пользователя, необходимо сначала задать следующие разделы реестра:</span><span class="sxs-lookup"><span data-stu-id="59382-109">To enable tracing on the user's computer, first set the following registry keys:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DirectX
    GlitchInstrumentation = 0x00000001 (REG_DWORD)
HKEY_LOCAL_MACHINE\SOFTWARE\DEBUG\Quartz.dll
    PERFLOG = 0x00000001 (REG_DWORD) 
```



<span data-ttu-id="59382-110">Эти ключи применяются к двоичным файлам выпуска и отладки.</span><span class="sxs-lookup"><span data-stu-id="59382-110">These keys apply to both release and debug binaries.</span></span>

<span data-ttu-id="59382-111">**Включение трассировки в приложении**</span><span class="sxs-lookup"><span data-stu-id="59382-111">**Enable Tracing in Your Application**</span></span>

<span data-ttu-id="59382-112">Чтобы включить трассировку в приложении, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="59382-112">To enable tracing in your application, perform the following steps:</span></span>

1.  <span data-ttu-id="59382-113">Вызовите **старттраце** , чтобы запустить новый сеанс трассировки.</span><span class="sxs-lookup"><span data-stu-id="59382-113">Call **StartTrace** to start a new tracing session.</span></span>
2.  <span data-ttu-id="59382-114">Вызовите **енаблетраце** , чтобы включить трассировку.</span><span class="sxs-lookup"><span data-stu-id="59382-114">Call **EnableTrace** to enable tracing.</span></span> <span data-ttu-id="59382-115">GUID поставщика для DirectShow — GUID \_ DSHOW \_ CTL.</span><span class="sxs-lookup"><span data-stu-id="59382-115">The provider GUID for DirectShow is GUID\_DSHOW\_CTL.</span></span>
3.  <span data-ttu-id="59382-116">Перед выходом из приложения вызовите **стоптраце** , чтобы закрыть сеанс трассировки.</span><span class="sxs-lookup"><span data-stu-id="59382-116">Before the application exits, call **StopTrace** to close the tracing session.</span></span>

<span data-ttu-id="59382-117">**Обработка событий**</span><span class="sxs-lookup"><span data-stu-id="59382-117">**Process the Events**</span></span>

<span data-ttu-id="59382-118">Чтобы обработать события, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="59382-118">To process the events, perform the following steps:</span></span>

1.  <span data-ttu-id="59382-119">Вызовите **опентраце** , чтобы открыть трассировку для обработки.</span><span class="sxs-lookup"><span data-stu-id="59382-119">Call **OpenTrace** to open the trace for processing.</span></span>
2.  <span data-ttu-id="59382-120">Вызовите **процесстраце** для обработки событий.</span><span class="sxs-lookup"><span data-stu-id="59382-120">Call **ProcessTrace** to process the events.</span></span>
3.  <span data-ttu-id="59382-121">В обратном вызове **процесстраце** используйте идентификатор GUID события, чтобы найти тип события.</span><span class="sxs-lookup"><span data-stu-id="59382-121">In the **ProcessTrace** callback, use the event GUID to find the event type.</span></span> <span data-ttu-id="59382-122">Идентификатор GUID события указывает структуру, используемую для данных события.</span><span class="sxs-lookup"><span data-stu-id="59382-122">The event GUID indicates the structure that is used for the event data.</span></span> <span data-ttu-id="59382-123">См. раздел [идентификаторы GUID событий трассировки](trace-guids.md).</span><span class="sxs-lookup"><span data-stu-id="59382-123">See [Trace Event GUIDs](trace-guids.md).</span></span>
4.  <span data-ttu-id="59382-124">Вызовите **клосетраце** , чтобы закрыть маркер трассировки.</span><span class="sxs-lookup"><span data-stu-id="59382-124">Call **CloseTrace** to close the trace handle.</span></span>

<span data-ttu-id="59382-125">**Пример кода**</span><span class="sxs-lookup"><span data-stu-id="59382-125">**Example Code**</span></span>

<span data-ttu-id="59382-126">В следующем коде показан вспомогательный класс, который включает трассировку.</span><span class="sxs-lookup"><span data-stu-id="59382-126">The following code shows a helper class that enables tracing.</span></span> <span data-ttu-id="59382-127">В этом коде показано, как записать события в файл журнала, который может быть обработан после завершения сеанса.</span><span class="sxs-lookup"><span data-stu-id="59382-127">This code shows how to write events to a log file, which can be processed after the session completes.</span></span> <span data-ttu-id="59382-128">Можно также обрабатывать события в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="59382-128">You can also process events in real time.</span></span> <span data-ttu-id="59382-129">Дополнительные сведения см. в документации по ETW в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="59382-129">For more information, refer to the ETW documentation in the Windows SDK.</span></span>


```C++
#include <wmistr.h>
#include <evntrace.h>
#include <perfstruct.h>

// Event classes. These are defined in dxmperf.h.
#ifndef DXMPERF_VIDEOREND
#define DXMPERF_VIDEOREND   0x00000001
#endif

#ifndef AUDIOBREAK_BIT
#define AUDIOBREAK_BIT      0x00000010
#endif

// This structure extends the EVENT_TRACE_PROPERTIES by adding fields
// for the name of the WMI session name and the log file.
struct PERFMON_LOGGERINFO
{
    EVENT_TRACE_PROPERTIES TraceProperties;
    WCHAR wcSessionName[ MAX_PATH ];    // Session name.
    WCHAR wcLogFileName[ MAX_PATH ];    // Log file.
};

// Helper class for DirectShow event tracing.
class CTrace
{
public:
    CTrace() : m_SessionLogger((TRACEHANDLE) INVALID_HANDLE_VALUE)
    {
        ZeroMemory(&m_LogInfo, sizeof(&m_LogInfo));
    }

    // Start: Starts a trace session.
    HRESULT Start(WCHAR *wszLogFile)
    {
        const WCHAR* wszSessionName = L"PerfMon_DirectShow"; 
        HRESULT hr = S_OK;
        ULONG result; 

        ZeroMemory(&m_LogInfo, sizeof(m_LogInfo));
        
        EVENT_TRACE_PROPERTIES& prop = m_LogInfo.TraceProperties;

        prop.Wnode.BufferSize = sizeof(m_LogInfo);  // Size of the structure.
        prop.Wnode.Flags = WNODE_FLAG_TRACED_GUID;  // Must be this value.

        // Use the QPC (high resolution timer).
        prop.Wnode.ClientContext = 1;        

        prop.Wnode.Guid = GUID_DSHOW_CTL;           // Event provider GUID.
        prop.LogFileMode = 
            EVENT_TRACE_FILE_MODE_CIRCULAR | EVENT_TRACE_USE_PAGED_MEMORY; 
        prop.EnableFlags = 
            EVENT_TRACE_FLAG_PROCESS;   // Process events.

        // Set the offset from the start of the structure to the log file name.
        prop.LogFileNameOffset = 
            sizeof(m_LogInfo.TraceProperties) + sizeof(m_LogInfo.wcSessionName);  

        // Set the offset from the start of the structure to the session name.
        prop.LoggerNameOffset = sizeof(m_LogInfo.TraceProperties); 

        // Copy the names into the structure.
        StringCchCopy(m_LogInfo.wcSessionName, MAX_PATH, wszSessionName);
        StringCchCopy(m_LogInfo.wcLogFileName, MAX_PATH, wszLogFile);

        // Start the trace.
        result = StartTrace(
            &m_SessionLogger, 
            m_LogInfo.wcSessionName, 
            &m_LogInfo.TraceProperties
            );

        if (result == ERROR_SUCCESS)
        {
            result = EnableTrace(
                TRUE,                                   // Enable.
                AUDIOBREAK_BIT | DXMPERF_VIDEOREND,     // Event classes.
                TRACE_LEVEL_VERBOSE,                    // Trace level.
                &GUID_DSHOW_CTL,                        // Event provider.
                m_SessionLogger                         // Session handle.
                );
        }
        if (result != ERROR_SUCCESS)
        { 
            hr = __HRESULT_FROM_WIN32(result);
        }
        return hr;
    }

    HRESULT Stop()
    {
        HRESULT hr = S_OK;

        // Stop the trace.
        if (m_SessionLogger != (TRACEHANDLE)INVALID_HANDLE_VALUE)
        {
            LONG result = 0;

            result = EnableTrace(FALSE, 0, 0, &GUID_DSHOW_CTL, m_SessionLogger);
            if (result == ERROR_SUCCESS)
            {
                result = StopTrace(
                    m_SessionLogger, 
                    m_LogInfo.wcSessionName, 
                    &m_LogInfo.TraceProperties);
            }

            m_SessionLogger = (TRACEHANDLE)INVALID_HANDLE_VALUE;
            if (result != ERROR_SUCCESS)
            { 
                hr = __HRESULT_FROM_WIN32(result);
            }
        }
        return hr;
    }

protected:
    TRACEHANDLE         m_SessionLogger;
    PERFMON_LOGGERINFO  m_LogInfo;
};
```



<span data-ttu-id="59382-130">В следующем коде показано, как обрабатывать журнал событий:</span><span class="sxs-lookup"><span data-stu-id="59382-130">The following code shows how to process the event log:</span></span>


```C++
// Callback for event processing.
VOID WINAPI EventCallback(PEVENT_TRACE pEvent)
{
    PERFINFO_DSHOW_STREAMTRACE  *pStreamTrace = NULL;
    PERFINFO_DSHOW_AVREND       *pVideoRender = NULL;
    PERFINFO_DSHOW_AUDIOBREAK   *pAudioBreak = NULL;

    if (pEvent->Header.Guid == GUID_STREAMTRACE) 
    {
        pStreamTrace = (PPERFINFO_DSHOW_STREAMTRACE)pEvent->MofData;

        switch (pStreamTrace->id)
        {
            // TODO: Handle the event.
        }
    }
    else if(pEvent->Header.Guid == GUID_VIDEOREND)
    {      
        pVideoRender = (PPERFINFO_DSHOW_AVREND)pEvent->MofData;
        // TODO: Handle the event.
    }
    else if(pEvent->Header.Guid == GUID_AUDIOBREAK)
    {
        pAudioBreak = (PPERFINFO_DSHOW_AUDIOBREAK)pEvent->MofData;
        // TODO: Handle the event.
    }
}

void ProcessTraceEvents(WCHAR *wszLogFile)
{
    ULONG result = 0;        
    EVENT_TRACE_LOGFILE logfile;

    ZeroMemory(&logfile, sizeof(logfile));
    logfile.LogFileName = wszLogFile;
    logfile.EventCallback  = EventCallback;   

    TRACEHANDLE handle = OpenTrace(&logfile);
    if (handle != (TRACEHANDLE)INVALID_HANDLE_VALUE)
    {
        result = ProcessTrace(&handle, 1, NULL, NULL);
        CloseTrace(handle);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="59382-131">См. также</span><span class="sxs-lookup"><span data-stu-id="59382-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59382-132">Отладка в DirectShow</span><span class="sxs-lookup"><span data-stu-id="59382-132">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



