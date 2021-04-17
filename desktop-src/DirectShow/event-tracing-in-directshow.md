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
# <a name="event-tracing-in-directshow"></a>Трассировка событий в DirectShow

DirectShow поддерживает трассировку событий Windows (ETW), которую можно использовать для создания журналов событий для инструментирования или отладки. Дополнительные сведения о трассировке событий Windows см. в документации по Windows SDK. Чтобы использовать события ETW в приложении DirectShow, необходимо включить трассировку, а затем обработать события трассировки. Выполните следующие действия.

**Настройка необходимых разделов реестра**

Чтобы включить трассировку на компьютере пользователя, необходимо сначала задать следующие разделы реестра:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\DirectX
    GlitchInstrumentation = 0x00000001 (REG_DWORD)
HKEY_LOCAL_MACHINE\SOFTWARE\DEBUG\Quartz.dll
    PERFLOG = 0x00000001 (REG_DWORD) 
```



Эти ключи применяются к двоичным файлам выпуска и отладки.

**Включение трассировки в приложении**

Чтобы включить трассировку в приложении, выполните следующие действия.

1.  Вызовите **старттраце** , чтобы запустить новый сеанс трассировки.
2.  Вызовите **енаблетраце** , чтобы включить трассировку. GUID поставщика для DirectShow — GUID \_ DSHOW \_ CTL.
3.  Перед выходом из приложения вызовите **стоптраце** , чтобы закрыть сеанс трассировки.

**Обработка событий**

Чтобы обработать события, выполните следующие действия.

1.  Вызовите **опентраце** , чтобы открыть трассировку для обработки.
2.  Вызовите **процесстраце** для обработки событий.
3.  В обратном вызове **процесстраце** используйте идентификатор GUID события, чтобы найти тип события. Идентификатор GUID события указывает структуру, используемую для данных события. См. раздел [идентификаторы GUID событий трассировки](trace-guids.md).
4.  Вызовите **клосетраце** , чтобы закрыть маркер трассировки.

**Пример кода**

В следующем коде показан вспомогательный класс, который включает трассировку. В этом коде показано, как записать события в файл журнала, который может быть обработан после завершения сеанса. Можно также обрабатывать события в режиме реального времени. Дополнительные сведения см. в документации по ETW в Windows SDK.


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



В следующем коде показано, как обрабатывать журнал событий:


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Отладка в DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



