---
description: Чтобы запустить службу, программа управления службами открывает обработчик для установленной базы данных, а затем задает маркер в вызове функции StartService.
ms.assetid: 7ee5254d-b035-4888-88e9-93e3e55d737e
title: Запуск службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8f30bb7f6ce9695a050033314a62ae870250c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999387"
---
# <a name="starting-a-service"></a><span data-ttu-id="ba9ba-103">Запуск службы</span><span class="sxs-lookup"><span data-stu-id="ba9ba-103">Starting a Service</span></span>

<span data-ttu-id="ba9ba-104">Чтобы запустить службу, [Программа управления службами](service-control-programs.md) открывает обработчик для установленной базы данных, а затем задает маркер в вызове функции [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="ba9ba-104">To start a service, a [service control program](service-control-programs.md) opens a handle to an installed database and then specifies the handle in a call to the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function.</span></span> <span data-ttu-id="ba9ba-105">После запуска службы программа использует членов структуры [**\_ \_ процесса состояния службы**](/windows/desktop/api/Winsvc/ns-winsvc-service_status_process) , возвращаемой функцией [**куерисервицестатусекс**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) для отслеживания хода выполнения службы.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-105">After starting the service, the program uses the members of the [**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status_process) structure returned by the [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function to track the progress of the service.</span></span>

<span data-ttu-id="ba9ba-106">Функция Достартсвк в следующем примере показывает, как запустить службу.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-106">The DoStartSvc function in the following example shows how to start a service.</span></span> <span data-ttu-id="ba9ba-107">Переменная Сзсвкнаме представляет собой глобальную переменную, которая содержит имя запускаемой службы.</span><span class="sxs-lookup"><span data-stu-id="ba9ba-107">The szSvcName variable is a global variable that contains the name of the service to be started.</span></span> <span data-ttu-id="ba9ba-108">Полный пример, задающий эту переменную, см. в разделе [свкконтрол. cpp](svccontrol-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="ba9ba-108">For the complete example that sets this variable, see [SvcControl.cpp](svccontrol-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Starts the service if possible.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoStartSvc()
{
    SERVICE_STATUS_PROCESS ssStatus; 
    DWORD dwOldCheckPoint; 
    DWORD dwStartTickCount;
    DWORD dwWaitTime;
    DWORD dwBytesNeeded;

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // servicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,         // SCM database 
        szSvcName,            // name of service 
        SERVICE_ALL_ACCESS);  // full access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Check the status in case the service is not stopped. 

    if (!QueryServiceStatusEx( 
            schService,                     // handle to service 
            SC_STATUS_PROCESS_INFO,         // information level
            (LPBYTE) &ssStatus,             // address of structure
            sizeof(SERVICE_STATUS_PROCESS), // size of structure
            &dwBytesNeeded ) )              // size needed if buffer is too small
    {
        printf("QueryServiceStatusEx failed (%d)\n", GetLastError());
        CloseServiceHandle(schService); 
        CloseServiceHandle(schSCManager);
        return; 
    }

    // Check if the service is already running. It would be possible 
    // to stop the service here, but for simplicity this example just returns. 

    if(ssStatus.dwCurrentState != SERVICE_STOPPED && ssStatus.dwCurrentState != SERVICE_STOP_PENDING)
    {
        printf("Cannot start the service because it is already running\n");
        CloseServiceHandle(schService); 
        CloseServiceHandle(schSCManager);
        return; 
    }

    // Save the tick count and initial checkpoint.

    dwStartTickCount = GetTickCount();
    dwOldCheckPoint = ssStatus.dwCheckPoint;

    // Wait for the service to stop before attempting to start it.

    while (ssStatus.dwCurrentState == SERVICE_STOP_PENDING)
    {
        // Do not wait longer than the wait hint. A good interval is 
        // one-tenth of the wait hint but not less than 1 second  
        // and not more than 10 seconds. 
 
        dwWaitTime = ssStatus.dwWaitHint / 10;

        if( dwWaitTime < 1000 )
            dwWaitTime = 1000;
        else if ( dwWaitTime > 10000 )
            dwWaitTime = 10000;

        Sleep( dwWaitTime );

        // Check the status until the service is no longer stop pending. 
 
        if (!QueryServiceStatusEx( 
                schService,                     // handle to service 
                SC_STATUS_PROCESS_INFO,         // information level
                (LPBYTE) &ssStatus,             // address of structure
                sizeof(SERVICE_STATUS_PROCESS), // size of structure
                &dwBytesNeeded ) )              // size needed if buffer is too small
        {
            printf("QueryServiceStatusEx failed (%d)\n", GetLastError());
            CloseServiceHandle(schService); 
            CloseServiceHandle(schSCManager);
            return; 
        }

        if ( ssStatus.dwCheckPoint > dwOldCheckPoint )
        {
            // Continue to wait and check.

            dwStartTickCount = GetTickCount();
            dwOldCheckPoint = ssStatus.dwCheckPoint;
        }
        else
        {
            if(GetTickCount()-dwStartTickCount > ssStatus.dwWaitHint)
            {
                printf("Timeout waiting for service to stop\n");
                CloseServiceHandle(schService); 
                CloseServiceHandle(schSCManager);
                return; 
            }
        }
    }

    // Attempt to start the service.

    if (!StartService(
            schService,  // handle to service 
            0,           // number of arguments 
            NULL) )      // no arguments 
    {
        printf("StartService failed (%d)\n", GetLastError());
        CloseServiceHandle(schService); 
        CloseServiceHandle(schSCManager);
        return; 
    }
    else printf("Service start pending...\n"); 

    // Check the status until the service is no longer start pending. 
 
    if (!QueryServiceStatusEx( 
            schService,                     // handle to service 
            SC_STATUS_PROCESS_INFO,         // info level
            (LPBYTE) &ssStatus,             // address of structure
            sizeof(SERVICE_STATUS_PROCESS), // size of structure
            &dwBytesNeeded ) )              // if buffer too small
    {
        printf("QueryServiceStatusEx failed (%d)\n", GetLastError());
        CloseServiceHandle(schService); 
        CloseServiceHandle(schSCManager);
        return; 
    }
 
    // Save the tick count and initial checkpoint.

    dwStartTickCount = GetTickCount();
    dwOldCheckPoint = ssStatus.dwCheckPoint;

    while (ssStatus.dwCurrentState == SERVICE_START_PENDING) 
    { 
        // Do not wait longer than the wait hint. A good interval is 
        // one-tenth the wait hint, but no less than 1 second and no 
        // more than 10 seconds. 
 
        dwWaitTime = ssStatus.dwWaitHint / 10;

        if( dwWaitTime < 1000 )
            dwWaitTime = 1000;
        else if ( dwWaitTime > 10000 )
            dwWaitTime = 10000;

        Sleep( dwWaitTime );

        // Check the status again. 
 
        if (!QueryServiceStatusEx( 
            schService,             // handle to service 
            SC_STATUS_PROCESS_INFO, // info level
            (LPBYTE) &ssStatus,             // address of structure
            sizeof(SERVICE_STATUS_PROCESS), // size of structure
            &dwBytesNeeded ) )              // if buffer too small
        {
            printf("QueryServiceStatusEx failed (%d)\n", GetLastError());
            break; 
        }
 
        if ( ssStatus.dwCheckPoint > dwOldCheckPoint )
        {
            // Continue to wait and check.

            dwStartTickCount = GetTickCount();
            dwOldCheckPoint = ssStatus.dwCheckPoint;
        }
        else
        {
            if(GetTickCount()-dwStartTickCount > ssStatus.dwWaitHint)
            {
                // No progress made within the wait hint.
                break;
            }
        }
    } 

    // Determine whether the service is running.

    if (ssStatus.dwCurrentState == SERVICE_RUNNING) 
    {
        printf("Service started successfully.\n"); 
    }
    else 
    { 
        printf("Service not started. \n");
        printf("  Current State: %d\n", ssStatus.dwCurrentState); 
        printf("  Exit Code: %d\n", ssStatus.dwWin32ExitCode); 
        printf("  Check Point: %d\n", ssStatus.dwCheckPoint); 
        printf("  Wait Hint: %d\n", ssStatus.dwWaitHint); 
    } 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="ba9ba-109">См. также</span><span class="sxs-lookup"><span data-stu-id="ba9ba-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba9ba-110">Запуск службы</span><span class="sxs-lookup"><span data-stu-id="ba9ba-110">Service Startup</span></span>](service-startup.md)
</dt> <dt>

[<span data-ttu-id="ba9ba-111">Полный пример службы</span><span class="sxs-lookup"><span data-stu-id="ba9ba-111">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



