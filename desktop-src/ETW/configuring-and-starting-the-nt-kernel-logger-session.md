---
description: Сеанс ведения журнала ядра NT — это сеанс трассировки событий, в котором записывается предопределенный набор событий ядра.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Настройка и запуск сеанса ведения журнала ядра NT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41398c9caac3ecd090af68a18bfb148095632d96b8c75eaaee7f04a551360fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901224"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a>Настройка и запуск сеанса ведения журнала ядра NT

Сеанс ведения журнала ядра NT — это сеанс трассировки событий, в котором записывается предопределенный набор событий ядра. Вы не вызываете функцию [**енаблетраце**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) для включения поставщиков ядра. Вместо этого используйте член **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , чтобы указать события ядра, которые требуется получить. Функция [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) использует флаги включения, указанные для включения поставщиков ядра.

Существует только один сеанс журнала ядра NT. Если сеанс уже используется, функция [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) возвращает ошибку \_ \_ .

Дополнительные сведения о запуске сеанса трассировки событий см. в разделе [Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md).

Дополнительные сведения о запуске закрытого сеанса ведения журнала см. в разделе [Настройка и запуск закрытого сеанса ведения журнала](configuring-and-starting-a-private-logger-session.md).

Дополнительные сведения о запуске глобального сеанса ведения журнала см. в разделе [Настройка и запуск глобального сеанса ведения журнала](configuring-and-starting-the-global-logger-session.md).

Дополнительные сведения о запуске сеанса авторегистратора см. в разделе [Настройка и запуск сеанса авторегистратора](configuring-and-starting-an-autologger-session.md).

В следующем примере показано, как настроить и запустить сеанс журнала ядра NT, который собирает сетевые события ядра TCP/IP и записывает их в файл размером 5 МБ.


```C++
#define INITGUID  // Include this #define to use SystemTraceControlGuid in Evntrace.h.

#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <strsafe.h>
#include <wmistr.h>
#include <evntrace.h>

#define LOGFILE_PATH L"<FULLPATHTOTHELOGFILE.etl>"

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    TRACEHANDLE SessionHandle = 0;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name,
    // which get appended to the end of the session properties structure.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(LOGFILE_PATH) + sizeof(KERNEL_LOGGER_NAME);
    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    // Set the session properties. You only append the log file name
    // to the properties structure; the StartTrace function appends
    // the session name for you.

    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->Wnode.ClientContext = 1; //QPC clock resolution
    pSessionProperties->Wnode.Guid = SystemTraceControlGuid; 
    pSessionProperties->EnableFlags = EVENT_TRACE_FLAG_NETWORK_TCPIP;
    pSessionProperties->LogFileMode = EVENT_TRACE_FILE_MODE_CIRCULAR;
    pSessionProperties->MaximumFileSize = 5;  // 5 MB
    pSessionProperties->LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);
    pSessionProperties->LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) + sizeof(KERNEL_LOGGER_NAME); 
    StringCbCopy((LPWSTR)((char*)pSessionProperties + pSessionProperties->LogFileNameOffset), sizeof(LOGFILE_PATH), LOGFILE_PATH);

    // Create the trace session.

    status = StartTrace((PTRACEHANDLE)&SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_ALREADY_EXISTS == status)
        {
            wprintf(L"The NT Kernel Logger session is already in use.\n");
        }
        else
        {
            wprintf(L"EnableTrace() failed with %lu\n", status);
        }

        goto cleanup;
    }

    wprintf(L"Press any key to end trace session ");
    _getch();

cleanup:

    if (SessionHandle)
    {
        status = ControlTrace(SessionHandle, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_STOP);

        if (ERROR_SUCCESS != status)
        {
            wprintf(L"ControlTrace(stop) failed with %lu\n", status);
        }
    }

    if (pSessionProperties)
        free(pSessionProperties);
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка и запуск закрытого сеанса ведения журнала](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Настройка и запуск сеанса Системтрацепровидер](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Настройка и запуск сеанса авторегистратора](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Обновление сеанса трассировки событий](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
