---
description: Функция Свкмаин в следующем примере представляет собой функцию ServiceMain для примера службы.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Написание функции ServiceMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca28b09efdc228457ae85d8a3343f334a26f246b6e48e49208d7416551e7f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887977"
---
# <a name="writing-a-servicemain-function"></a>Написание функции ServiceMain

Функция Свкмаин в следующем примере представляет собой функцию [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) для примера службы. Свкмаин имеет доступ к аргументам командной строки для службы в соответствии с функциями **Main** консольного приложения. Первый параметр содержит число аргументов, передаваемых в службу во втором параметре. Всегда будет существовать хотя бы один аргумент. Второй параметр является указателем на массив строковых указателей. Первый элемент массива всегда является именем службы.

Функция Свкмаин сначала вызывает функцию [**регистерсервицектрлхандлер**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) для регистрации функции свкктрлхандлер в качестве функции [**обработчика**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) службы и начала инициализации. **Регистерсервицектрлхандлер** должен быть первой неудачной функцией в [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) , поэтому служба может использовать маркер состояния, возвращенный этой функцией, для вызова [**сбой SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) с \_ остановленным состоянием службы в случае возникновения ошибки.

Затем функция Свкмаин вызывает функцию Репортсвкстатус, чтобы указать, что ее начальное состояние — \_ \_ Ожидание запуска службы. Пока служба находится в этом состоянии, никакие элементы управления не принимаются. Для упрощения логики службы рекомендуется, чтобы служба не принимала какие-либо элементы управления, пока выполняется ее инициализация.

Наконец, функция Свкмаин вызывает функцию СвЦинит для выполнения инициализации, зависящей от службы, и начинает работу, выполняемую службой.

Пример функции инициализации, СвЦинит, является очень простым примером. Он не выполняет более сложные задачи инициализации, такие как создание дополнительных потоков. Он создает событие, которое обработчик управления службами может сообщить, чтобы указать, что служба должна быть остановлена, а затем вызывает Репортсвкстатус, чтобы указать, что служба перешла в \_ состояние выполнения службы. На этом этапе служба завершила свою инициализацию и готова принять элементы управления. Для лучшей производительности системы приложение должно перейти в состояние выполнения в течение 25-100 миллисекунд.

Так как этот пример службы не выполняет никаких реальных задач, СвЦинит просто ожидает сигнала о событии остановки службы, вызвав функцию [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) , вызывает репортсвкстатус, чтобы указать, что служба перешла в \_ остановленное состояние, и возвращает. (Обратите внимание, что функция должна возвращать, вместо того чтобы вызывать функцию [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) , так как функция возврата позволяет очищать память, выделенную для аргументов.) Можно выполнить дополнительные задачи очистки, используя функцию [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) вместо **WaitForSingleObject**. Поток, выполняющий функцию [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) , завершается, но сама служба продолжит работу. Когда обработчик управления службами сообщает о событии, поток из пула потоков выполняет обратный вызов для выполнения дополнительной очистки, в том числе Задание состояния "Служба \_ остановлена".

Обратите внимание, что в этом примере используется Свкрепортевент для записи событий ошибок в журнал событий. Исходный код для Свкрепортевент см. в разделе [SVC. cpp](svc-cpp.md). Пример функции обработчика элемента управления см. [в разделе Написание функции обработчика элемента управления](writing-a-control-handler-function.md).

В этом примере используются следующие глобальные определения.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



Следующий пример фрагмента кода взят из полного примера службы.


```C++
//
// Purpose: 
//   Entry point for the service
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None.
//
VOID WINAPI SvcMain( DWORD dwArgc, LPTSTR *lpszArgv )
{
    // Register the handler function for the service

    gSvcStatusHandle = RegisterServiceCtrlHandler( 
        SVCNAME, 
        SvcCtrlHandler);

    if( !gSvcStatusHandle )
    { 
        SvcReportEvent(TEXT("RegisterServiceCtrlHandler")); 
        return; 
    } 

    // These SERVICE_STATUS members remain as set here

    gSvcStatus.dwServiceType = SERVICE_WIN32_OWN_PROCESS; 
    gSvcStatus.dwServiceSpecificExitCode = 0;    

    // Report initial status to the SCM

    ReportSvcStatus( SERVICE_START_PENDING, NO_ERROR, 3000 );

    // Perform service-specific initialization and work.

    SvcInit( dwArgc, lpszArgv );
}

//
// Purpose: 
//   The service code
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None
//
VOID SvcInit( DWORD dwArgc, LPTSTR *lpszArgv)
{
    // TO_DO: Declare and set any required variables.
    //   Be sure to periodically call ReportSvcStatus() with 
    //   SERVICE_START_PENDING. If initialization fails, call
    //   ReportSvcStatus with SERVICE_STOPPED.

    // Create an event. The control handler function, SvcCtrlHandler,
    // signals this event when it receives the stop control code.

    ghSvcStopEvent = CreateEvent(
                         NULL,    // default security attributes
                         TRUE,    // manual reset event
                         FALSE,   // not signaled
                         NULL);   // no name

    if ( ghSvcStopEvent == NULL)
    {
        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }

    // Report running status when initialization is complete.

    ReportSvcStatus( SERVICE_RUNNING, NO_ERROR, 0 );

    // TO_DO: Perform work until service stops.

    while(1)
    {
        // Check whether to stop the service.

        WaitForSingleObject(ghSvcStopEvent, INFINITE);

        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }
}

//
// Purpose: 
//   Sets the current service status and reports it to the SCM.
//
// Parameters:
//   dwCurrentState - The current state (see SERVICE_STATUS)
//   dwWin32ExitCode - The system error code
//   dwWaitHint - Estimated time for pending operation, 
//     in milliseconds
// 
// Return value:
//   None
//
VOID ReportSvcStatus( DWORD dwCurrentState,
                      DWORD dwWin32ExitCode,
                      DWORD dwWaitHint)
{
    static DWORD dwCheckPoint = 1;

    // Fill in the SERVICE_STATUS structure.

    gSvcStatus.dwCurrentState = dwCurrentState;
    gSvcStatus.dwWin32ExitCode = dwWin32ExitCode;
    gSvcStatus.dwWaitHint = dwWaitHint;

    if (dwCurrentState == SERVICE_START_PENDING)
        gSvcStatus.dwControlsAccepted = 0;
    else gSvcStatus.dwControlsAccepted = SERVICE_ACCEPT_STOP;

    if ( (dwCurrentState == SERVICE_RUNNING) ||
           (dwCurrentState == SERVICE_STOPPED) )
        gSvcStatus.dwCheckPoint = 0;
    else gSvcStatus.dwCheckPoint = dwCheckPoint++;

    // Report the status of the service to the SCM.
    SetServiceStatus( gSvcStatusHandle, &gSvcStatus );
}

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функция ServiceMain службы](service-servicemain-function.md)
</dt> <dt>

[Полный пример службы](the-complete-service-sample.md)
</dt> </dl>

 

 
