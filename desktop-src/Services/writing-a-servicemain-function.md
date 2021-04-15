---
description: Функция Свкмаин в следующем примере представляет собой функцию ServiceMain для примера службы.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Написание функции ServiceMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3e947c356bad6c6d54395a671aa192c93de1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662343"
---
# <a name="writing-a-servicemain-function"></a><span data-ttu-id="c8be5-103">Написание функции ServiceMain</span><span class="sxs-lookup"><span data-stu-id="c8be5-103">Writing a ServiceMain Function</span></span>

<span data-ttu-id="c8be5-104">Функция Свкмаин в следующем примере представляет собой функцию [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) для примера службы.</span><span class="sxs-lookup"><span data-stu-id="c8be5-104">The SvcMain function in the following example is the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function for the example service.</span></span> <span data-ttu-id="c8be5-105">Свкмаин имеет доступ к аргументам командной строки для службы в соответствии с функциями **Main** консольного приложения.</span><span class="sxs-lookup"><span data-stu-id="c8be5-105">SvcMain has access to the command-line arguments for the service in the way that the **main** function of a console application does.</span></span> <span data-ttu-id="c8be5-106">Первый параметр содержит число аргументов, передаваемых в службу во втором параметре.</span><span class="sxs-lookup"><span data-stu-id="c8be5-106">The first parameter contains the number of arguments being passed to the service in the second parameter.</span></span> <span data-ttu-id="c8be5-107">Всегда будет существовать хотя бы один аргумент.</span><span class="sxs-lookup"><span data-stu-id="c8be5-107">There will always be at least one argument.</span></span> <span data-ttu-id="c8be5-108">Второй параметр является указателем на массив строковых указателей.</span><span class="sxs-lookup"><span data-stu-id="c8be5-108">The second parameter is a pointer to an array of string pointers.</span></span> <span data-ttu-id="c8be5-109">Первый элемент массива всегда является именем службы.</span><span class="sxs-lookup"><span data-stu-id="c8be5-109">The first item in the array is always the service name.</span></span>

<span data-ttu-id="c8be5-110">Функция Свкмаин сначала вызывает функцию [**регистерсервицектрлхандлер**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) для регистрации функции свкктрлхандлер в качестве функции [**обработчика**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) службы и начала инициализации.</span><span class="sxs-lookup"><span data-stu-id="c8be5-110">The SvcMain function first calls the [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) function to register the SvcCtrlHandler function as the service's [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function and begin initialization.</span></span> <span data-ttu-id="c8be5-111">**Регистерсервицектрлхандлер** должен быть первой неудачной функцией в [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) , поэтому служба может использовать маркер состояния, возвращенный этой функцией, для вызова [**сбой SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) с \_ остановленным состоянием службы в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="c8be5-111">**RegisterServiceCtrlHandler** should be the first nonfailing function in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) so the service can use the status handle returned by this function to call [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) with the SERVICE\_STOPPED state if an error occurs.</span></span>

<span data-ttu-id="c8be5-112">Затем функция Свкмаин вызывает функцию Репортсвкстатус, чтобы указать, что ее начальное состояние — \_ \_ Ожидание запуска службы.</span><span class="sxs-lookup"><span data-stu-id="c8be5-112">Next, the SvcMain function calls the ReportSvcStatus function to indicate that its initial status is SERVICE\_START\_PENDING.</span></span> <span data-ttu-id="c8be5-113">Пока служба находится в этом состоянии, никакие элементы управления не принимаются.</span><span class="sxs-lookup"><span data-stu-id="c8be5-113">While the service is in this state, no controls are accepted.</span></span> <span data-ttu-id="c8be5-114">Для упрощения логики службы рекомендуется, чтобы служба не принимала какие-либо элементы управления, пока выполняется ее инициализация.</span><span class="sxs-lookup"><span data-stu-id="c8be5-114">To simplify the logic of the service, it is recommended that the service not accept any controls while it is performing its initialization.</span></span>

<span data-ttu-id="c8be5-115">Наконец, функция Свкмаин вызывает функцию СвЦинит для выполнения инициализации, зависящей от службы, и начинает работу, выполняемую службой.</span><span class="sxs-lookup"><span data-stu-id="c8be5-115">Finally, the SvcMain function calls the SvcInit function to perform the service-specific initialization and begin the work to be performed by the service.</span></span>

<span data-ttu-id="c8be5-116">Пример функции инициализации, СвЦинит, является очень простым примером. Он не выполняет более сложные задачи инициализации, такие как создание дополнительных потоков.</span><span class="sxs-lookup"><span data-stu-id="c8be5-116">The sample initialization function, SvcInit, is a very simple example; it does not perform more complex initialization tasks such as creating additional threads.</span></span> <span data-ttu-id="c8be5-117">Он создает событие, которое обработчик управления службами может сообщить, чтобы указать, что служба должна быть остановлена, а затем вызывает Репортсвкстатус, чтобы указать, что служба перешла в \_ состояние выполнения службы.</span><span class="sxs-lookup"><span data-stu-id="c8be5-117">It creates an event that the service control handler can signal to indicate that the service should stop, then calls ReportSvcStatus to indicate that the service has entered the SERVICE\_RUNNING state.</span></span> <span data-ttu-id="c8be5-118">На этом этапе служба завершила свою инициализацию и готова принять элементы управления.</span><span class="sxs-lookup"><span data-stu-id="c8be5-118">At this point, the service has completed its initialization and is ready to accept controls.</span></span> <span data-ttu-id="c8be5-119">Для лучшей производительности системы приложение должно перейти в состояние выполнения в течение 25-100 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="c8be5-119">For best system performance, your application should enter the running state within 25-100 milliseconds.</span></span>

<span data-ttu-id="c8be5-120">Так как этот пример службы не выполняет никаких реальных задач, СвЦинит просто ожидает сигнала о событии остановки службы, вызвав функцию [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) , вызывает репортсвкстатус, чтобы указать, что служба перешла в \_ остановленное состояние, и возвращает.</span><span class="sxs-lookup"><span data-stu-id="c8be5-120">Because this sample service does not complete any real tasks, SvcInit simply waits for the service stop event to be signaled by calling the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function, calls ReportSvcStatus to indicate that the service has entered the SERVICE\_STOPPED state, and returns.</span></span> <span data-ttu-id="c8be5-121">(Обратите внимание, что функция должна возвращать, вместо того чтобы вызывать функцию [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) , так как функция возврата позволяет очищать память, выделенную для аргументов.) Можно выполнить дополнительные задачи очистки, используя функцию [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) вместо **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="c8be5-121">(Note that it is important for the function to return, rather than call the [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) function, because returning allows for cleanup of the memory allocated for the arguments.) You can perform additional cleanup tasks by using the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) function instead of **WaitForSingleObject**.</span></span> <span data-ttu-id="c8be5-122">Поток, выполняющий функцию [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) , завершается, но сама служба продолжит работу.</span><span class="sxs-lookup"><span data-stu-id="c8be5-122">The thread that is running the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function terminates, but the service itself continues to run.</span></span> <span data-ttu-id="c8be5-123">Когда обработчик управления службами сообщает о событии, поток из пула потоков выполняет обратный вызов для выполнения дополнительной очистки, в том числе Задание состояния "Служба \_ остановлена".</span><span class="sxs-lookup"><span data-stu-id="c8be5-123">When the service control handler signals the event, a thread from the thread pool executes your callback to perform the additional cleanup, including setting the status to SERVICE\_STOPPED.</span></span>

<span data-ttu-id="c8be5-124">Обратите внимание, что в этом примере используется Свкрепортевент для записи событий ошибок в журнал событий.</span><span class="sxs-lookup"><span data-stu-id="c8be5-124">Note that this example uses SvcReportEvent to write error events to the event log.</span></span> <span data-ttu-id="c8be5-125">Исходный код для Свкрепортевент см. в разделе [SVC. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="c8be5-125">For the source code for SvcReportEvent, see [Svc.cpp](svc-cpp.md).</span></span> <span data-ttu-id="c8be5-126">Пример функции обработчика элемента управления см. [в разделе Написание функции обработчика элемента управления](writing-a-control-handler-function.md).</span><span class="sxs-lookup"><span data-stu-id="c8be5-126">For an example control handler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span>

<span data-ttu-id="c8be5-127">В этом примере используются следующие глобальные определения.</span><span class="sxs-lookup"><span data-stu-id="c8be5-127">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="c8be5-128">Следующий пример фрагмента кода взят из полного примера службы.</span><span class="sxs-lookup"><span data-stu-id="c8be5-128">The following sample fragment is taken from the complete service sample.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c8be5-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c8be5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8be5-130">Функция ServiceMain службы</span><span class="sxs-lookup"><span data-stu-id="c8be5-130">Service ServiceMain Function</span></span>](service-servicemain-function.md)
</dt> <dt>

[<span data-ttu-id="c8be5-131">Полный пример службы</span><span class="sxs-lookup"><span data-stu-id="c8be5-131">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
