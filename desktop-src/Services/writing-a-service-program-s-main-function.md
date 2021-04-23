---
description: Следующий пример можно использовать в качестве точки входа для программы службы, которая поддерживает одну службу.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Написание главной функции в служебных программах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83aa743bfabbeafa2e05818c5bb068a949dce807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541103"
---
# <a name="writing-a-service-programs-main-function"></a><span data-ttu-id="bb1c2-103">Написание основной функции служебной программы</span><span class="sxs-lookup"><span data-stu-id="bb1c2-103">Writing a Service Program's main Function</span></span>

<span data-ttu-id="bb1c2-104">Функция **Main** [служебной программы](service-programs.md) вызывает функцию [**сбой StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) для подключения к [диспетчеру управления службами](service-control-manager.md) (SCM) и запуска потока диспетчера управления.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-104">The **main** function of a [service program](service-programs.md) calls the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function to connect to the [service control manager](service-control-manager.md) (SCM) and start the control dispatcher thread.</span></span> <span data-ttu-id="bb1c2-105">Поток диспетчера обрабатывается, ожидая входящих управляющих запросов для служб, указанных в таблице диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-105">The dispatcher thread loops, waiting for incoming control requests for the services specified in the dispatch table.</span></span> <span data-ttu-id="bb1c2-106">Этот поток возвращается при возникновении ошибки или при завершении всех служб в процессе.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-106">This thread returns when there is an error or when all of the services in the process have terminated.</span></span> <span data-ttu-id="bb1c2-107">Когда все службы в процессе прерываются, SCM отправляет управляющий запрос в поток диспетчера, который сообщает о его завершении.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-107">When all services in the process have terminated, the SCM sends a control request to the dispatcher thread telling it to exit.</span></span> <span data-ttu-id="bb1c2-108">Затем этот поток возвращается из вызова **сбой StartServiceCtrlDispatcher** , и процесс может завершиться.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-108">This thread then returns from the **StartServiceCtrlDispatcher** call and the process can terminate.</span></span>

<span data-ttu-id="bb1c2-109">В этом примере используются следующие глобальные определения.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-109">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="bb1c2-110">Следующий пример можно использовать в качестве точки входа для программы службы, которая поддерживает одну службу.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-110">The following example can be used as the entry point for a service program that supports a single service.</span></span> <span data-ttu-id="bb1c2-111">Если программа службы поддерживает несколько служб, добавьте имена дополнительных служб в таблицу диспетчеризации, чтобы они могли отслеживаться потоком Dispatcher.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-111">If your service program supports multiple services, add the names of the additional services to the dispatch table so they can be monitored by the dispatcher thread.</span></span>

<span data-ttu-id="bb1c2-112">\_Функция тмаин является точкой входа.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-112">The \_tmain function is the entry point.</span></span> <span data-ttu-id="bb1c2-113">Функция Свкрепортевент записывает информационные сообщения и ошибки в журнал событий.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-113">The SvcReportEvent function writes informational messages and errors to the event log.</span></span> <span data-ttu-id="bb1c2-114">Дополнительные сведения о написании функции Свкмаин см. [в разделе Написание функции ServiceMain](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="bb1c2-114">For information about writing the SvcMain function, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span> <span data-ttu-id="bb1c2-115">Дополнительные сведения о функции СвЦинсталл см. в разделе [Установка службы](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="bb1c2-115">For more information about the SvcInstall function, see [Installing a Service](installing-a-service.md).</span></span> <span data-ttu-id="bb1c2-116">Дополнительные сведения о написании функции Свкктрлхандлер см. [в разделе Написание функции обработчика элемента управления](writing-a-control-handler-function.md).</span><span class="sxs-lookup"><span data-stu-id="bb1c2-116">For information about writing the SvcCtrlHandler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span> <span data-ttu-id="bb1c2-117">Полный пример службы, включая источник функции Свкрепортевент, см. в разделе [SVC. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="bb1c2-117">For the complete example service, including the source for the SvcReportEvent function, see [Svc.cpp](svc-cpp.md).</span></span>


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



<span data-ttu-id="bb1c2-118">Ниже приведен пример файла Sample. h, созданный компилятором сообщений.</span><span class="sxs-lookup"><span data-stu-id="bb1c2-118">The following is an example Sample.h as generated by the message compiler.</span></span> <span data-ttu-id="bb1c2-119">Дополнительные сведения см. в разделе [Sample.MC](sample-mc.md).</span><span class="sxs-lookup"><span data-stu-id="bb1c2-119">For more information, see [Sample.mc](sample-mc.md).</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bb1c2-120">См. также</span><span class="sxs-lookup"><span data-stu-id="bb1c2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb1c2-121">Точка входа службы</span><span class="sxs-lookup"><span data-stu-id="bb1c2-121">Service Entry Point</span></span>](service-entry-point.md)
</dt> <dt>

[<span data-ttu-id="bb1c2-122">Полный пример службы</span><span class="sxs-lookup"><span data-stu-id="bb1c2-122">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



