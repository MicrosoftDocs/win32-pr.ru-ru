---
description: Чтобы обновить свойства сеанса трассировки событий, вызовите функцию Контролтраце с помощью управляющего \_ \_ кода обновления элемента управления трассировки событий \_ .
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: Обновление сеанса трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e580c2e84dec6682e5fad323fe0cad427300a21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991307"
---
# <a name="updating-an-event-tracing-session"></a><span data-ttu-id="c6eae-103">Обновление сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="c6eae-103">Updating an Event Tracing Session</span></span>

<span data-ttu-id="c6eae-104">Чтобы обновить свойства сеанса трассировки событий, вызовите функцию [**контролтраце**](/windows/win32/api/evntrace/nf-evntrace-controltracea) с помощью управляющего кода **\_ \_ \_ обновления элемента управления трассировки событий** .</span><span class="sxs-lookup"><span data-stu-id="c6eae-104">To update the properties of an event tracing session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function using the **EVENT\_TRACE\_CONTROL\_UPDATE** control code.</span></span> <span data-ttu-id="c6eae-105">Можно указать сеанс для обновления с помощью маркера сеанса, полученного из предыдущего вызова [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea), или имени сеанса.</span><span class="sxs-lookup"><span data-stu-id="c6eae-105">You can specify the session to update using a session handle obtained from an earlier call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), or a session name.</span></span> <span data-ttu-id="c6eae-106">Свойства сеанса трассировки событий обновляются с использованием значений, указанных в структуре [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="c6eae-106">The properties of the event tracing session are updated using the values specified in the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span> <span data-ttu-id="c6eae-107">Можно обновить только подмножество свойств.</span><span class="sxs-lookup"><span data-stu-id="c6eae-107">You can update only a subset of the properties.</span></span> <span data-ttu-id="c6eae-108">Список свойств, которые можно обновить, см. в параметре *Properties* функции **контролтраце** .</span><span class="sxs-lookup"><span data-stu-id="c6eae-108">For a list of the properties you can update, see the *Properties* parameter of the **ControlTrace** function.</span></span>

<span data-ttu-id="c6eae-109">Если вызов [**контролтраце**](/windows/win32/api/evntrace/nf-evntrace-controltracea) успешно выполнен, структура [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) обновляется для отражения новых значений свойств.</span><span class="sxs-lookup"><span data-stu-id="c6eae-109">If the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) call is successful, the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is updated to reflect the new property values.</span></span> <span data-ttu-id="c6eae-110">Структура также будет содержать новую статистику выполнения для сеанса трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="c6eae-110">The structure will also contain the new run statistics for the event tracing session.</span></span>

<span data-ttu-id="c6eae-111">В следующем примере показано, как обновить сеанс трассировки событий ядра.</span><span class="sxs-lookup"><span data-stu-id="c6eae-111">The following example shows how to update the kernel event tracing session.</span></span> <span data-ttu-id="c6eae-112">В примере запрашиваются текущие значения свойств и обновляется структура перед обновлением сеанса.</span><span class="sxs-lookup"><span data-stu-id="c6eae-112">The example queries for the current property values and updates the structure before updating the session.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <wmistr.h>
#include <evntrace.h>

#define MAX_SESSION_NAME_LEN 1024
#define MAX_LOGFILE_PATH_LEN 1024

void wmain(void)
{
    ULONG status = ERROR_SUCCESS;
    EVENT_TRACE_PROPERTIES* pSessionProperties = NULL;
    ULONG BufferSize = 0;

    // Allocate memory for the session properties. The memory must
    // be large enough to include the log file name and session name.
    // This example specifies the maximum size for the session name 
    // and log file name.
    
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) + 
        (MAX_SESSION_NAME_LEN * sizeof(WCHAR)) + 
        (MAX_LOGFILE_PATH_LEN * sizeof(WCHAR));

    pSessionProperties = (EVENT_TRACE_PROPERTIES*) malloc(BufferSize);    
    if (NULL == pSessionProperties)
    {
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);
        goto cleanup;
    }
    
    ZeroMemory(pSessionProperties, BufferSize);
    pSessionProperties->Wnode.BufferSize = BufferSize;

    // Query for the kernel trace session's current property values.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_QUERY);

    if (ERROR_SUCCESS != status)
    {
        if (ERROR_WMI_INSTANCE_NOT_FOUND == status)
        {
            wprintf(L"The Kernel Logger is not running.\n");
        }
        else
        {
            wprintf(L"ControlTrace(query) failed with %lu\n", status);
        }

        goto cleanup;
    }

    // Update the enable flags to also enable the Process and Thread providers.

    pSessionProperties->LogFileNameOffset = 0;  // Zero tells ETW not to update the file name
    pSessionProperties->Wnode.Flags = WNODE_FLAG_TRACED_GUID;
    pSessionProperties->EnableFlags |= EVENT_TRACE_FLAG_PROCESS | EVENT_TRACE_FLAG_THREAD;

    // Update the session's properties.

    status = ControlTrace((TRACEHANDLE)NULL, KERNEL_LOGGER_NAME, pSessionProperties, EVENT_TRACE_CONTROL_UPDATE);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"ControlTrace(update) failed with %lu.\n", status);
        goto cleanup;
    }

    wprintf(L"\nUpdated session");

cleanup:

    if (pSessionProperties)
    {
        free(pSessionProperties);
        pSessionProperties = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="c6eae-113">См. также</span><span class="sxs-lookup"><span data-stu-id="c6eae-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6eae-114">Настройка и запуск закрытого сеанса ведения журнала</span><span class="sxs-lookup"><span data-stu-id="c6eae-114">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="c6eae-115">Настройка и запуск сеанса Системтрацепровидер</span><span class="sxs-lookup"><span data-stu-id="c6eae-115">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="c6eae-116">Настройка и запуск сеанса авторегистратора</span><span class="sxs-lookup"><span data-stu-id="c6eae-116">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="c6eae-117">Настройка и запуск сеанса трассировки событий</span><span class="sxs-lookup"><span data-stu-id="c6eae-117">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="c6eae-118">Настройка и запуск сеанса ведения журнала ядра NT</span><span class="sxs-lookup"><span data-stu-id="c6eae-118">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
