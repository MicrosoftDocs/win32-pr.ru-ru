---
description: Следующий пример связывает функцию асинхронного вызова процедур (APC), также известную как подпрограммы завершения, с таймером ожидания при установке таймера.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Использование ожидающих таймеров при асинхронном вызове процедуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62436011a3da0ac17525a0ce977e7bcd25382c5c267b62b9c972381e0f28562d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661154"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Использование ожидающих таймеров при асинхронном вызове процедуры

Следующий пример связывает функцию [асинхронного вызова процедур](asynchronous-procedure-calls.md) (APC), также известную как подпрограммы завершения, с [таймером ожидания](waitable-timer-objects.md) при установке таймера. Адрес подпрограммы завершения является четвертым параметром функции [**сетваитаблетимер**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) . Пятый параметр — это указатель void, который можно использовать для передачи аргументов в подпрограммы завершения.

Подпрограммы завершения будут выполняться тем же потоком, который вызвал [**сетваитаблетимер**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Этот поток должен находиться в состоянии оповещения для выполнения процедуры завершения. Это достигается путем вызова функции [**слипекс**](/windows/win32/api/synchapi/nf-synchapi-sleepex) , которая является функцией, поддерживающей оповещение.

Каждый поток имеет очередь APC. Если в очереди APC потока имеется запись во время вызова одной из функций, которые могут получать оповещения, поток не помещается в спящий режим. Вместо этого запись удаляется из очереди APC и вызывается подпрограммы завершения.

Если в очереди APC нет записей, поток приостанавливается до тех пор, пока не будет достигнуто ожидание. Ожидание может быть удовлетворено добавлением записи в очередь APC, временем ожидания или превращением дескриптора в сигнальное состояние. Если ожидание выполняется записью в очереди APC, происходит пробуждение потока и вызывается подпрограммы завершения. В этом случае возвращаемое значение функции — **Ожидание \_ \_ завершения ввода-вывода**.

После выполнения процедуры завершения система проверяет наличие другой записи в очереди APC для обработки. Функция с функцией оповещения будет возвращать данные только после обработки всех записей APC. Таким образом, если записи добавляются в очередь APC быстрее, чем они могут быть обработаны, возможно, вызов функции с возможностью оповещения никогда не будет возвращать значение. Это особенно возможно в случае с ожидающими таймерами, если период меньше, чем время, необходимое для выполнения подпрограммы завершения.

При использовании таймера ожидания с помощью APC поток, задающий таймер, не должен ждать обработки таймера. Это приведет к тому, что поток будет выходить из-за того, что таймер становится сигнальным, а не в результате добавления записи в очередь APC. В результате поток больше не находится в состоянии оповещения, а подпрограммы завершения не вызываются. В следующем коде вызов [**слипекс**](/windows/win32/api/synchapi/nf-synchapi-sleepex) пробуждения потока при добавлении записи в очередь APC потока после того, как таймер установлен в сигнальное состояние.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование ожидающих объектов таймера](using-waitable-timer-objects.md)
</dt> </dl>

 

 
