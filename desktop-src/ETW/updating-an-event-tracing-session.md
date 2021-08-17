---
description: Чтобы обновить свойства сеанса трассировки событий, вызовите функцию Контролтраце с помощью управляющего \_ \_ кода обновления элемента управления трассировки событий \_ .
ms.assetid: 1496bf88-a989-4fa1-888a-90385c4ca8ee
title: Обновление сеанса трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa4f092211d59dda080906f01380f8751fbc099f79dc8f1cd8ea1f7a2ba36fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383344"
---
# <a name="updating-an-event-tracing-session"></a>Обновление сеанса трассировки событий

Чтобы обновить свойства сеанса трассировки событий, вызовите функцию [**контролтраце**](/windows/win32/api/evntrace/nf-evntrace-controltracea) с помощью управляющего кода **\_ \_ \_ обновления элемента управления трассировки событий** . Можно указать сеанс для обновления с помощью маркера сеанса, полученного из предыдущего вызова [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea), или имени сеанса. Свойства сеанса трассировки событий обновляются с использованием значений, указанных в структуре [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) . Можно обновить только подмножество свойств. Список свойств, которые можно обновить, см. в параметре *Properties* функции **контролтраце** .

Если вызов [**контролтраце**](/windows/win32/api/evntrace/nf-evntrace-controltracea) успешно выполнен, структура [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) обновляется для отражения новых значений свойств. Структура также будет содержать новую статистику выполнения для сеанса трассировки событий.

В следующем примере показано, как обновить сеанс трассировки событий ядра. В примере запрашиваются текущие значения свойств и обновляется структура перед обновлением сеанса.


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

[Настройка и запуск сеанса ведения журнала ядра NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> </dl>

 

 
