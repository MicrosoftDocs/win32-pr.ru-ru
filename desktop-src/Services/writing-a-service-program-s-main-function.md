---
description: Следующий пример можно использовать в качестве точки входа для программы службы, которая поддерживает одну службу.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Написание главной функции в служебных программах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82e3c519650957f4f27b00ff54864f558cafba3db960f30c0dd20517328f1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966615"
---
# <a name="writing-a-service-programs-main-function"></a>Написание основной функции служебной программы

Функция **Main** [служебной программы](service-programs.md) вызывает функцию [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) для подключения к [диспетчеру управления службами](service-control-manager.md) (SCM) и запуска потока диспетчера управления. Поток диспетчера обрабатывается, ожидая входящих управляющих запросов для служб, указанных в таблице диспетчеризации. Этот поток возвращается при возникновении ошибки или при завершении всех служб в процессе. Когда все службы в процессе прерываются, SCM отправляет управляющий запрос в поток диспетчера, который сообщает о его завершении. Затем этот поток возвращается из вызова **сбой StartServiceCtrlDispatcher** , и процесс может завершиться.

В этом примере используются следующие глобальные определения.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



Следующий пример можно использовать в качестве точки входа для программы службы, которая поддерживает одну службу. Если программа службы поддерживает несколько служб, добавьте имена дополнительных служб в таблицу диспетчеризации, чтобы они могли отслеживаться потоком Dispatcher.

\_Функция тмаин является точкой входа. Функция Свкрепортевент записывает информационные сообщения и ошибки в журнал событий. Дополнительные сведения о написании функции Свкмаин см. [в разделе Написание функции ServiceMain](writing-a-servicemain-function.md). Дополнительные сведения о функции СвЦинсталл см. в разделе [Установка службы](installing-a-service.md). Дополнительные сведения о написании функции Свкктрлхандлер см. [в разделе Написание функции обработчика элемента управления](writing-a-control-handler-function.md). Полный пример службы, включая источник функции Свкрепортевент, см. в разделе [SVC. cpp](svc-cpp.md).


```C++
//
// Purpose: 
//   Entry point for the process
//
// Parameters:
//   None
// 
// Return value:
//   None, defaults to 0 (zero)
//
int __cdecl _tmain(int argc, TCHAR *argv[])
{ 
    // If command-line parameter is "install", install the service. 
    // Otherwise, the service is probably being started by the SCM.

    if( lstrcmpi( argv[1], TEXT("install")) == 0 )
    {
        SvcInstall();
        return;
    }

    // TO_DO: Add any additional services for the process to this table.
    SERVICE_TABLE_ENTRY DispatchTable[] = 
    { 
        { SVCNAME, (LPSERVICE_MAIN_FUNCTION) SvcMain }, 
        { NULL, NULL } 
    }; 
 
    // This call returns when the service has stopped. 
    // The process should simply terminate when the call returns.

    if (!StartServiceCtrlDispatcher( DispatchTable )) 
    { 
        SvcReportEvent(TEXT("StartServiceCtrlDispatcher")); 
    } 
} 

```



Ниже приведен пример файла Sample. h, созданный компилятором сообщений. Дополнительные сведения см. в разделе [Sample.MC](sample-mc.md).

``` syntax
 // The following are message definitions.
//
//  Values are 32 bit values layed out as follows:
//
//   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
//   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
//  +---+-+-+-----------------------+-------------------------------+
//  |Sev|C|R|     Facility          |               Code            |
//  +---+-+-+-----------------------+-------------------------------+
//
//  where
//
//      Sev - is the severity code
//
//          00 - Success
//          01 - Informational
//          10 - Warning
//          11 - Error
//
//      C - is the Customer code flag
//
//      R - is a reserved bit
//
//      Facility - is the facility code
//
//      Code - is the facility's status code
//
//
// Define the facility codes
//
#define FACILITY_SYSTEM                  0x0
#define FACILITY_STUBS                   0x3
#define FACILITY_RUNTIME                 0x2
#define FACILITY_IO_ERROR_CODE           0x4


//
// Define the severity codes
//
#define STATUS_SEVERITY_WARNING          0x2
#define STATUS_SEVERITY_SUCCESS          0x0
#define STATUS_SEVERITY_INFORMATIONAL    0x1
#define STATUS_SEVERITY_ERROR            0x3


//
// MessageId: SVC_ERROR
//
// MessageText:
//
//  An error has occurred (%2).
//  
//
#define SVC_ERROR                        ((DWORD)0xC0020001L)
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Точка входа службы](service-entry-point.md)
</dt> <dt>

[Полный пример службы](the-complete-service-sample.md)
</dt> </dl>

 

 



