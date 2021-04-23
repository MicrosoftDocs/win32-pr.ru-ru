---
description: Сеанс ведения журнала ядра NT — это сеанс трассировки событий, в котором записывается предопределенный набор событий ядра.
ms.assetid: 3c4258d8-8073-4cc5-a29d-ce485a3fdc14
title: Настройка и запуск сеанса ведения журнала ядра NT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13cb0d429bc4b0e01e02c33e2686040f0b7454b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986133"
---
# <a name="configuring-and-starting-the-nt-kernel-logger-session"></a><span data-ttu-id="a8b92-103">Настройка и запуск сеанса ведения журнала ядра NT</span><span class="sxs-lookup"><span data-stu-id="a8b92-103">Configuring and Starting the NT Kernel Logger Session</span></span>

<span data-ttu-id="a8b92-104">Сеанс ведения журнала ядра NT — это сеанс трассировки событий, в котором записывается предопределенный набор событий ядра.</span><span class="sxs-lookup"><span data-stu-id="a8b92-104">The NT Kernel Logger session is an event tracing session that records a predefined set of kernel events.</span></span> <span data-ttu-id="a8b92-105">Вы не вызываете функцию [**енаблетраце**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) для включения поставщиков ядра.</span><span class="sxs-lookup"><span data-stu-id="a8b92-105">You do not call the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable the kernel providers.</span></span> <span data-ttu-id="a8b92-106">Вместо этого используйте член **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , чтобы указать события ядра, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a8b92-106">Instead, you use the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure to specify the kernel events that you want to receive.</span></span> <span data-ttu-id="a8b92-107">Функция [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) использует флаги включения, указанные для включения поставщиков ядра.</span><span class="sxs-lookup"><span data-stu-id="a8b92-107">The [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function uses the enable flags that you specify to enable the kernel providers.</span></span>

<span data-ttu-id="a8b92-108">Существует только один сеанс журнала ядра NT.</span><span class="sxs-lookup"><span data-stu-id="a8b92-108">There is only one NT Kernel Logger session.</span></span> <span data-ttu-id="a8b92-109">Если сеанс уже используется, функция [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) возвращает ошибку \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a8b92-109">If the session is already in use, the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function returns ERROR\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="a8b92-110">Дополнительные сведения о запуске сеанса трассировки событий см. в разделе [Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="a8b92-110">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="a8b92-111">Дополнительные сведения о запуске закрытого сеанса ведения журнала см. в разделе [Настройка и запуск закрытого сеанса ведения журнала](configuring-and-starting-a-private-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="a8b92-111">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="a8b92-112">Дополнительные сведения о запуске глобального сеанса ведения журнала см. в разделе [Настройка и запуск глобального сеанса ведения журнала](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="a8b92-112">For details on starting a Global Logger session, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="a8b92-113">Дополнительные сведения о запуске сеанса авторегистратора см. в разделе [Настройка и запуск сеанса авторегистратора](configuring-and-starting-an-autologger-session.md).</span><span class="sxs-lookup"><span data-stu-id="a8b92-113">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

<span data-ttu-id="a8b92-114">В следующем примере показано, как настроить и запустить сеанс журнала ядра NT, который собирает сетевые события ядра TCP/IP и записывает их в файл размером 5 МБ.</span><span class="sxs-lookup"><span data-stu-id="a8b92-114">The following example shows how to configure and start an NT Kernel Logger session that collects network TCP/IP kernel events and writes them to a 5MB circular file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a8b92-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a8b92-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8b92-116">Настройка и запуск закрытого сеанса ведения журнала</span><span class="sxs-lookup"><span data-stu-id="a8b92-116">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="a8b92-117">Настройка и запуск сеанса Системтрацепровидер</span><span class="sxs-lookup"><span data-stu-id="a8b92-117">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="a8b92-118">Настройка и запуск сеанса авторегистратора</span><span class="sxs-lookup"><span data-stu-id="a8b92-118">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="a8b92-119">Настройка и запуск сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="a8b92-119">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="a8b92-120">Обновление сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="a8b92-120">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
