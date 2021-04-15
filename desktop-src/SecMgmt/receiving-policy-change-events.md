---
description: LSA предоставляет функции, которые можно использовать для получения уведомлений при изменении политики в локальной системе.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Получение событий изменения политики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33145974ce712f21b338ba35f1571c8f3046c42c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682584"
---
# <a name="receiving-policy-change-events"></a>Получение событий изменения политики

LSA предоставляет функции, которые можно использовать для получения уведомлений при изменении политики в локальной системе.

Чтобы получить уведомление, создайте новый объект события, вызвав функцию [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) , а затем вызовите функцию [**лсарегистерполицичанженотификатион**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) . Приложение может затем вызвать функцию Wait, такую как [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)или [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) , чтобы дождаться возникновения события. Функция Wait возвращает, когда происходит событие, или по истечении времени ожидания. Как правило, события уведомления используются в многопоточных приложениях, в которых один поток ожидает событие, а другие потоки продолжают обработку.

Если приложению больше не требуется получать уведомления, оно должно вызвать [**лсаунрегистерполицичанженотификатион**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) , а затем вызвать функцию [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) , чтобы освободить обработчик объекта события.

В следующем примере показано, как приложение с одним потоком может принимать события уведомления при изменении политики аудита системы.


```C++
#include <windows.h>
#include <stdio.h>

void WaitForPolicyChanges()
{
  HANDLE hEvent;
  NTSTATUS ntsResult;
  DWORD dwResult;

  // Create an event object.
  hEvent = CreateEvent( 
    NULL,  // child processes cannot inherit 
    FALSE, // automatically reset event
    FALSE, // start as a nonsignaled event
    NULL   // do not need a name
  );

  // Check that the event was created.
  if (hEvent == NULL) 
  {
    wprintf(L"Event object creation failed: %d\n",GetLastError());
    return;
  }
  // Register to receive auditing policy change notifications.
  ntsResult = LsaRegisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );
  if (STATUS_SUCCESS != ntsResult)
  {
    wprintf(L"LsaRegisterPolicyChangeNotification failed.\n");
    CloseHandle(hEvent);
    return;
  }

  // Wait for the event to be triggered.
  dwResult = WaitForSingleObject( 
    hEvent, // handle to the event object
    300000  // time-out interval, in milliseconds
  );

  // The wait function returned.
  if (dwResult == WAIT_OBJECT_0)
  {  // received the notification signal
    wprintf(L"Notification received.\n");
  } 
  else 
  {  // received a time-out or error
    wprintf(L"Notification was not received.\n");
  }
  // Unregister for notification.
  LsaUnregisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );

  // Free the event handle.
  CloseHandle(hEvent);
}
```



Дополнительные сведения об объектах событий, функциях Wait и синхронизации см. [в разделе Использование объектов событий](/windows/desktop/Sync/using-event-objects).

 

 
