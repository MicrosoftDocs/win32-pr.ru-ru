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
# <a name="receiving-policy-change-events"></a><span data-ttu-id="7c678-103">Получение событий изменения политики</span><span class="sxs-lookup"><span data-stu-id="7c678-103">Receiving Policy Change Events</span></span>

<span data-ttu-id="7c678-104">LSA предоставляет функции, которые можно использовать для получения уведомлений при изменении политики в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="7c678-104">The LSA provides functions you can use to receive notification when there is a change in policy on the local system.</span></span>

<span data-ttu-id="7c678-105">Чтобы получить уведомление, создайте новый объект события, вызвав функцию [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) , а затем вызовите функцию [**лсарегистерполицичанженотификатион**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) .</span><span class="sxs-lookup"><span data-stu-id="7c678-105">To receive notification, create a new event object by calling the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function, and then call the [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) function.</span></span> <span data-ttu-id="7c678-106">Приложение может затем вызвать функцию Wait, такую как [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)или [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) , чтобы дождаться возникновения события.</span><span class="sxs-lookup"><span data-stu-id="7c678-106">Your application can then call a wait function such as [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), or [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the event to occur.</span></span> <span data-ttu-id="7c678-107">Функция Wait возвращает, когда происходит событие, или по истечении времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="7c678-107">The wait function returns when the event occurs, or when the time-out period expires.</span></span> <span data-ttu-id="7c678-108">Как правило, события уведомления используются в многопоточных приложениях, в которых один поток ожидает событие, а другие потоки продолжают обработку.</span><span class="sxs-lookup"><span data-stu-id="7c678-108">Typically, notification events are used in multithreaded applications, in which one thread waits for an event, while other threads continue processing.</span></span>

<span data-ttu-id="7c678-109">Если приложению больше не требуется получать уведомления, оно должно вызвать [**лсаунрегистерполицичанженотификатион**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) , а затем вызвать функцию [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) , чтобы освободить обработчик объекта события.</span><span class="sxs-lookup"><span data-stu-id="7c678-109">When your application no longer needs to receive notifications, it should call [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) and then call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to free the event object handle.</span></span>

<span data-ttu-id="7c678-110">В следующем примере показано, как приложение с одним потоком может принимать события уведомления при изменении политики аудита системы.</span><span class="sxs-lookup"><span data-stu-id="7c678-110">The following example shows how a single-threaded application can receive notification events when the system's auditing policy changes.</span></span>


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



<span data-ttu-id="7c678-111">Дополнительные сведения об объектах событий, функциях Wait и синхронизации см. [в разделе Использование объектов событий](/windows/desktop/Sync/using-event-objects).</span><span class="sxs-lookup"><span data-stu-id="7c678-111">For more information about event objects, wait functions, and synchronization, see [Using Event Objects](/windows/desktop/Sync/using-event-objects).</span></span>

 

 
