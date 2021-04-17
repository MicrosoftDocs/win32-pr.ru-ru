---
description: Следующий пример связывает функцию асинхронного вызова процедур (APC), также известную как подпрограммы завершения, с таймером ожидания при установке таймера.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Использование ожидающих таймеров при асинхронном вызове процедуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628288b1c5e1ce7c83e104cf6daa9e6fdcc3eb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663411"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a><span data-ttu-id="0e2b6-103">Использование ожидающих таймеров при асинхронном вызове процедуры</span><span class="sxs-lookup"><span data-stu-id="0e2b6-103">Using Waitable Timers with an Asynchronous Procedure Call</span></span>

<span data-ttu-id="0e2b6-104">Следующий пример связывает функцию [асинхронного вызова процедур](asynchronous-procedure-calls.md) (APC), также известную как подпрограммы завершения, с [таймером ожидания](waitable-timer-objects.md) при установке таймера.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-104">The following example associates an [asynchronous procedure call](asynchronous-procedure-calls.md) (APC) function, also known as a completion routine, with a [waitable timer](waitable-timer-objects.md) when the timer is set.</span></span> <span data-ttu-id="0e2b6-105">Адрес подпрограммы завершения является четвертым параметром функции [**сетваитаблетимер**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) .</span><span class="sxs-lookup"><span data-stu-id="0e2b6-105">The address of the completion routine is the fourth parameter to the [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) function.</span></span> <span data-ttu-id="0e2b6-106">Пятый параметр — это указатель void, который можно использовать для передачи аргументов в подпрограммы завершения.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-106">The fifth parameter is a void pointer that you can use to pass arguments to the completion routine.</span></span>

<span data-ttu-id="0e2b6-107">Подпрограммы завершения будут выполняться тем же потоком, который вызвал [**сетваитаблетимер**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer).</span><span class="sxs-lookup"><span data-stu-id="0e2b6-107">The completion routine will be executed by the same thread that called [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer).</span></span> <span data-ttu-id="0e2b6-108">Этот поток должен находиться в состоянии оповещения для выполнения процедуры завершения.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-108">This thread must be in an alertable state to execute the completion routine.</span></span> <span data-ttu-id="0e2b6-109">Это достигается путем вызова функции [**слипекс**](/windows/win32/api/synchapi/nf-synchapi-sleepex) , которая является функцией, поддерживающей оповещение.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-109">It accomplishes this by calling the [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) function, which is an alertable function.</span></span>

<span data-ttu-id="0e2b6-110">Каждый поток имеет очередь APC.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-110">Each thread has an APC queue.</span></span> <span data-ttu-id="0e2b6-111">Если в очереди APC потока имеется запись во время вызова одной из функций, которые могут получать оповещения, поток не помещается в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-111">If there is an entry in the thread's APC queue at the time that one of the alertable functions is called, the thread is not put to sleep.</span></span> <span data-ttu-id="0e2b6-112">Вместо этого запись удаляется из очереди APC и вызывается подпрограммы завершения.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-112">Instead, the entry is removed from the APC queue and the completion routine is called.</span></span>

<span data-ttu-id="0e2b6-113">Если в очереди APC нет записей, поток приостанавливается до тех пор, пока не будет достигнуто ожидание.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-113">If no entry exists in the APC queue, the thread is suspended until the wait is satisfied.</span></span> <span data-ttu-id="0e2b6-114">Ожидание может быть удовлетворено добавлением записи в очередь APC, временем ожидания или превращением дескриптора в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-114">The wait can be satisfied by adding an entry to the APC queue, by a timeout, or by a handle becoming signaled.</span></span> <span data-ttu-id="0e2b6-115">Если ожидание выполняется записью в очереди APC, происходит пробуждение потока и вызывается подпрограммы завершения.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-115">If the wait is satisfied by an entry in the APC queue, the thread is awakened and the completion routine is called.</span></span> <span data-ttu-id="0e2b6-116">В этом случае возвращаемое значение функции — **Ожидание \_ \_ завершения ввода-вывода**.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-116">In this case, the return value of the function is **WAIT\_IO\_COMPLETION**.</span></span>

<span data-ttu-id="0e2b6-117">После выполнения процедуры завершения система проверяет наличие другой записи в очереди APC для обработки.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-117">After the completion routine is executed, the system checks for another entry in the APC queue to process.</span></span> <span data-ttu-id="0e2b6-118">Функция с функцией оповещения будет возвращать данные только после обработки всех записей APC.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-118">An alertable function will return only after all APC entries have been processed.</span></span> <span data-ttu-id="0e2b6-119">Таким образом, если записи добавляются в очередь APC быстрее, чем они могут быть обработаны, возможно, вызов функции с возможностью оповещения никогда не будет возвращать значение.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-119">Therefore, if entries are being added to the APC queue faster than they can be processed, it is possible that a call to an alertable function will never return.</span></span> <span data-ttu-id="0e2b6-120">Это особенно возможно в случае с ожидающими таймерами, если период меньше, чем время, необходимое для выполнения подпрограммы завершения.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-120">This is especially possible with waitable timers, if the period is shorter than the amount of time required to execute the completion routine.</span></span>

<span data-ttu-id="0e2b6-121">При использовании таймера ожидания с помощью APC поток, задающий таймер, не должен ждать обработки таймера.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-121">When you are using a waitable timer with an APC, the thread that sets the timer should not wait on the handle of the timer.</span></span> <span data-ttu-id="0e2b6-122">Это приведет к тому, что поток будет выходить из-за того, что таймер становится сигнальным, а не в результате добавления записи в очередь APC.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-122">By doing so, you would cause the thread to wake up as a result of the timer becoming signaled rather than as the result of an entry being added to the APC queue.</span></span> <span data-ttu-id="0e2b6-123">В результате поток больше не находится в состоянии оповещения, а подпрограммы завершения не вызываются.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-123">As a result, the thread is no longer in an alertable state and the completion routine is not called.</span></span> <span data-ttu-id="0e2b6-124">В следующем коде вызов [**слипекс**](/windows/win32/api/synchapi/nf-synchapi-sleepex) пробуждения потока при добавлении записи в очередь APC потока после того, как таймер установлен в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="0e2b6-124">In the following code, the call to [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) awakens the thread when an entry is added to the thread's APC queue after the timer is set to the signaled state.</span></span>


```C++
#define UNICODE 1
#define _UNICODE 1

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define _SECOND 10000000

typedef struct _MYDATA {
   TCHAR *szText;
   DWORD dwValue;
} MYDATA;

VOID CALLBACK TimerAPCProc(
   LPVOID lpArg,               // Data value
   DWORD dwTimerLowValue,      // Timer low value
   DWORD dwTimerHighValue )    // Timer high value

{
   // Formal parameters not used in this example.
   UNREFERENCED_PARAMETER(dwTimerLowValue);
   UNREFERENCED_PARAMETER(dwTimerHighValue);

   MYDATA *pMyData = (MYDATA *)lpArg;

   _tprintf( TEXT("Message: %s\nValue: %d\n\n"), pMyData->szText,
          pMyData->dwValue );
   MessageBeep(0);

}

int main( void ) 
{
   HANDLE          hTimer;
   BOOL            bSuccess;
   __int64         qwDueTime;
   LARGE_INTEGER   liDueTime;
   MYDATA          MyData;

   MyData.szText = TEXT("This is my data");
   MyData.dwValue = 100;

   hTimer = CreateWaitableTimer(
           NULL,                   // Default security attributes
           FALSE,                  // Create auto-reset timer
           TEXT("MyTimer"));       // Name of waitable timer
   if (hTimer != NULL)
   {
      __try 
      {
         // Create an integer that will be used to signal the timer 
         // 5 seconds from now.
         qwDueTime = -5 * _SECOND;

         // Copy the relative time into a LARGE_INTEGER.
         liDueTime.LowPart  = (DWORD) ( qwDueTime & 0xFFFFFFFF );
         liDueTime.HighPart = (LONG)  ( qwDueTime >> 32 );

         bSuccess = SetWaitableTimer(
            hTimer,           // Handle to the timer object
            &liDueTime,       // When timer will become signaled
            2000,             // Periodic timer interval of 2 seconds
            TimerAPCProc,     // Completion routine
            &MyData,          // Argument to the completion routine
            FALSE );          // Do not restore a suspended system

         if ( bSuccess ) 
         {
            for ( ; MyData.dwValue < 1000; MyData.dwValue += 100 ) 
            {
               SleepEx(
                  INFINITE,     // Wait forever
                  TRUE );       // Put thread in an alertable state
            }

         } 
         else 
         {
            printf("SetWaitableTimer failed with error %d\n", GetLastError());
         }

      } 
      __finally 
      {
         CloseHandle( hTimer );
      }
   } 
   else 
   {
      printf("CreateWaitableTimer failed with error %d\n", GetLastError());
   }

   return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="0e2b6-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0e2b6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e2b6-126">Использование ожидающих объектов таймера</span><span class="sxs-lookup"><span data-stu-id="0e2b6-126">Using Waitable Timer Objects</span></span>](using-waitable-timer-objects.md)
</dt> </dl>

 

 
