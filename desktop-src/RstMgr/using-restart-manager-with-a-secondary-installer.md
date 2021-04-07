---
title: Использование диспетчера перезапуска с дополнительным установщиком
description: В следующей процедуре описывается использование диспетчера перезапуска с основным и дополнительным установщиками.
ms.assetid: aa55ab09-206b-49ed-8cb4-e311c1ed2d9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb44105d9f3d391bb2ed793aca8a6da2c330b30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887967"
---
# <a name="using-restart-manager-with-a-secondary-installer"></a><span data-ttu-id="086d7-103">Использование диспетчера перезапуска с дополнительным установщиком</span><span class="sxs-lookup"><span data-stu-id="086d7-103">Using Restart Manager with a Secondary Installer</span></span>

<span data-ttu-id="086d7-104">В следующей процедуре описывается использование диспетчера перезапуска с основным и дополнительным установщиками.</span><span class="sxs-lookup"><span data-stu-id="086d7-104">The following procedure describes the use of the Restart Manager with primary and secondary installers.</span></span>

<span data-ttu-id="086d7-105">При использовании основных и вторичных установщиков основной установщик управляет пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="086d7-105">When using primary and secondary installers, the primary installer controls the user interface.</span></span>

<span data-ttu-id="086d7-106">**Использование диспетчера перезапуска с основным и дополнительным установщиками**</span><span class="sxs-lookup"><span data-stu-id="086d7-106">**To use Restart Manager with primary and secondary installers**</span></span>

1.  <span data-ttu-id="086d7-107">Основной установщик вызывает функцию [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) для запуска сеанса диспетчера перезапуска и получения маркера сеанса и ключа.</span><span class="sxs-lookup"><span data-stu-id="086d7-107">The primary installer calls the [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) function to start the Restart Manager session and obtain a session handle and key.</span></span>
2.  <span data-ttu-id="086d7-108">Основной установщик запускает или связывается с дополнительным установщиком и предоставляет ему ключ сеанса, полученный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="086d7-108">The primary installer starts or contacts the secondary installer and provides it with the session key obtained in the previous step.</span></span>
3.  <span data-ttu-id="086d7-109">Вторичный установщик вызывает функцию [**рмжоинсессион**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) с ключом сеанса, чтобы присоединиться к сеансу диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="086d7-109">The secondary installer calls the [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) function with the session key to join the Restart Manager session.</span></span> <span data-ttu-id="086d7-110">Вторичный установщик может присоединиться к сеансу, запущенному основным установщиком, только если оба установщика работают в одном контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="086d7-110">A secondary installer can join a session that is started by the primary installer only when both installers run in the same user context.</span></span>
4.  <span data-ttu-id="086d7-111">Основной и дополнительный установщики вызывают функцию [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) для регистрации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="086d7-111">The primary and secondary installers call the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function to register resources.</span></span> <span data-ttu-id="086d7-112">Диспетчер перезапуска может использовать только зарегистрированные ресурсы, чтобы определить, какие приложения и службы должны быть выключены и перезапущены.</span><span class="sxs-lookup"><span data-stu-id="086d7-112">The Restart Manager can use only registered resources to determine which applications and services must be shut down and restarted.</span></span> <span data-ttu-id="086d7-113">Все ресурсы, на которые может повлиять установка, должны быть зарегистрированы в сеансе.</span><span class="sxs-lookup"><span data-stu-id="086d7-113">All resources that can be affected by the installation should be registered with the session.</span></span> <span data-ttu-id="086d7-114">Ресурсы можно идентифицировать по имени файла, краткому имени службы или структуре [**\_ уникального \_ процесса RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) .</span><span class="sxs-lookup"><span data-stu-id="086d7-114">Resources can be identified by filename, service short name, or an [**RM\_UNIQUE\_PROCESS**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) structure.</span></span>
5.  <span data-ttu-id="086d7-115">Основной установщик вызывает функцию [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) для получения массива структур [**\_ \_ сведений о процессе RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) , в котором перечислены все приложения и службы, которые должны быть выключены и перезапущены.</span><span class="sxs-lookup"><span data-stu-id="086d7-115">The primary installer calls the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to obtain an array of [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structures that lists all applications and services that must be shut down and restarted.</span></span>

    <span data-ttu-id="086d7-116">Если значение параметра *лпдвребутреасон* , возвращаемое функцией [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) , не равно нулю, диспетчеру перезапуска не удается освободить зарегистрированный ресурс при завершении работы приложения или службы.</span><span class="sxs-lookup"><span data-stu-id="086d7-116">If the value of the *lpdwRebootReason* parameter that is returned by the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function is nonzero, the Restart Manager is unable to free a registered resource by the shutdown of an application or service.</span></span> <span data-ttu-id="086d7-117">В этом случае для продолжения установки требуется завершение работы системы и перезапуск.</span><span class="sxs-lookup"><span data-stu-id="086d7-117">In this case, a system shutdown and restart is required to continue the installation.</span></span> <span data-ttu-id="086d7-118">Основной установщик должен запрашивать у пользователя действие, прекращать работу программ или служб или запланировать завершение работы и перезагрузку системы.</span><span class="sxs-lookup"><span data-stu-id="086d7-118">The primary installer should prompt the user for an action, stop programs or services, or schedule a system shutdown and restart.</span></span>

    <span data-ttu-id="086d7-119">Если значение параметра *лпдвребутреасон* , возвращаемое функцией [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) , равно нулю, установщик должен вызвать функцию [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) .</span><span class="sxs-lookup"><span data-stu-id="086d7-119">If the value of the *lpdwRebootReason* parameter that is returned by the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function is zero, the installer should call the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) function.</span></span> <span data-ttu-id="086d7-120">При этом службы и приложения, использующие зарегистрированные ресурсы, завершаются.</span><span class="sxs-lookup"><span data-stu-id="086d7-120">This shuts down the services and applications that are using registered resources.</span></span> <span data-ttu-id="086d7-121">Затем основной и дополнительный установщики должны выполнить системные изменения, необходимые для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="086d7-121">The primary and secondary installers should then perform system modifications that are required to complete the installation.</span></span> <span data-ttu-id="086d7-122">Наконец, основной установщик должен вызвать функцию [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) , чтобы диспетчер перезапуска мог перезапустить приложения, работа которых была завершена и которые были зарегистрированы для перезапуска.</span><span class="sxs-lookup"><span data-stu-id="086d7-122">Finally, the primary installer should call the [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function so that the Restart Manager can restart the applications it has shut down and that have been registered for a restart.</span></span>

6.  <span data-ttu-id="086d7-123">Основной и дополнительный установщик вызывают функцию [**рмендсессион**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) , чтобы закрыть сеанс диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="086d7-123">The primary and secondary installer call the [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) function to close the Restart Manager session.</span></span>

<span data-ttu-id="086d7-124">В следующем фрагменте кода показан пример основного установщика, запускаемого и использующего сеанс диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="086d7-124">The following code snippet shows an example of a primary installer starting and using a Restart Manager session.</span></span> <span data-ttu-id="086d7-125">Для этого примера требуется Windows 7 или Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="086d7-125">The example requires Windows 7 or Windows Server 2008 R2.</span></span> <span data-ttu-id="086d7-126">В Windows Vista или Windows Server 2008 приложение калькулятора завершает работу, но не перезапускается.</span><span class="sxs-lookup"><span data-stu-id="086d7-126">On Windows Vista or Windows Server 2008, the Calculator application shuts down but does not restart.</span></span> <span data-ttu-id="086d7-127">В этом примере показано, как основной установщик может использовать диспетчер перезапуска для завершения работы и перезапуска процесса.</span><span class="sxs-lookup"><span data-stu-id="086d7-127">This example shows how a primary installer can use Restart Manager to shutdown and restart a process.</span></span> <span data-ttu-id="086d7-128">В примере предполагается, что калькулятор уже выполняется перед запуском сеанса диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="086d7-128">The example assumes that Calculator is already running before starting the Restart Manager session.</span></span>


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the  
    // Text-Encoded session key,defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of calc files to be registered.
    DWORD dwFiles           = 2;   

    //
    // NOTE:We register two calc executable files. 
    // The second one is for the redirection of 32 bit calc on 
    // 64 bit machines. Even if you are using a 32 bit machine,  
    // you don't need to comment out the second line. 
    //
    LPCWSTR rgsFiles[]      = 
     {L"C:\\Windows\\System32\\calc.exe",
      L"C:\\Windows\\SysWow64\\calc.exe"};

    UINT nRetry             = 0; 
    UINT nAffectedApps      = 0;
    UINT nProcInfoNeeded    = 0;
    RM_REBOOT_REASON dwRebootReasons    = RmRebootReasonNone;
    RM_PROCESS_INFO *rgAffectedApps     = NULL;
    
    //
    // Start a Restart Manager Session
    //
    dwErrCode = RmStartSession(&dwSessionHandle, 0, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: we only register two calc executable files 
    // in this sample. You can register files, processes 
    // (in the form of process ID), and services (in the   
    // form of service short names) with Restart Manager.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,       // Files
                                    0,  
                                    NULL,           // Processes
                                    0, 
                                    NULL);          // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Obtain the list of affected applications/services.
    //
    // NOTE: Restart Manager returns the results into the  
    // buffer allocated by the caller. The first call to 
    // RmGetList() will return the size of the buffer  
    // (i.e. nProcInfoNeeded) the caller needs to allocate. 
    // The caller then needs to allocate the buffer  
    // (i.e. rgAffectedApps) and make another RmGetList() 
    // call to ask Restart Manager to write the results 
    // into the buffer. However, since Restart Manager 
    // refreshes the list every time RmGetList()is called, 
    // it is possible that the size returned by the first 
    // RmGetList()call is not sufficient to hold the results  
    // discovered by the second RmGetList() call. Therefore, 
    // it is recommended that the caller follows the 
    // following practice to handle this race condition:
    //   
    //    Use a loop to call RmGetList() in case the buffer 
    //    allocated according to the size returned in previous 
    //    call is not enough.      
    // 
    // In this example, we use a do-while loop trying to make 
    // 3 RmGetList() calls (including the first attempt to get 
    // buffer size) and if we still cannot succeed, we give up. 
    //
    do
    {
        dwErrCode = RmGetList(dwSessionHandle,
                              &nProcInfoNeeded,
                              &nAffectedApps, 
                              rgAffectedApps, 
                              (LPDWORD) &dwRebootReasons);
        if (ERROR_SUCCESS == dwErrCode)
        {
            //
            // RmGetList() succeeded
            //
            break;
        }

        if (ERROR_MORE_DATA != dwErrCode)
        {
            //
            // RmGetList() failed, with errors 
            // other than ERROR_MORE_DATA
            //
            goto RM_CLEANUP;
        }

        //
        // RmGetList() is asking for more data
        //
        nAffectedApps = nProcInfoNeeded;
        
        if (NULL != rgAffectedApps)
        {
            delete []rgAffectedApps;
            rgAffectedApps = NULL;
        }

        rgAffectedApps = new RM_PROCESS_INFO[nAffectedApps];
    } while ((ERROR_MORE_DATA == dwErrCode) && (nRetry ++ < 3));

    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    if (RmRebootReasonNone != dwRebootReasons)
    {
        //
        // Restart Manager cannot mitigate a reboot. 
        // We goes to the clean up. The caller may want   
        // to add additional code to handle this scenario.
        //
        goto RM_CLEANUP;
    }
    
    //
    // Now rgAffectedApps contains the affected applications 
    // and services. The number of applications and services
    // returned is nAffectedApps. The result of RmGetList can 
    // be interpreted by the user to determine subsequent  
    // action (e.g. ask user's permission to shutdown).
    //
    // CALLER CODE GOES HERE...
     
    //
    // Shut down all running instances of affected 
    // applications and services.
    //
    dwErrCode = RmShutdown(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // An installer can now replace or update
    // the calc executable file.
    //
    // CALLER CODE GOES HERE...


    //
    // Restart applications and services, after the 
    // files have been replaced or updated.
    //
    dwErrCode = RmRestart(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:
    
    if (NULL != rgAffectedApps)
    {
        delete [] rgAffectedApps;
        rgAffectedApps = NULL;
    }

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // Clean up the Restart Manager session.
        //
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}
```



<span data-ttu-id="086d7-129">В следующем фрагменте кода приведен пример присоединения дополнительного установщика к существующему сеансу диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="086d7-129">The following code snippet shows an example of joining a secondary installer to the existing Restart Manager session.</span></span> <span data-ttu-id="086d7-130">Для этого примера требуется Windows Vista или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="086d7-130">The example requires Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="086d7-131">Вторичный установщик получает ключ сеанса от основного установщика и использует его для приподключения к сеансу.</span><span class="sxs-lookup"><span data-stu-id="086d7-131">The secondary installer obtains the session key from the primary installer and uses this to join the session.</span></span>


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the 
    // Text-Encoded session key, defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of files to be registered.
    DWORD dwFiles           = 1;   
    //
    // We register oleaut32.dll with Restart Manager.
    //
    LPCWSTR rgsFiles[]      = 
        {L"C:\\Windows\\System32\\oleaut32.dll"};

    //    
    // Secondary installer needs to obtain the session key from  
    // the primary installer and uses it to join the session.
    //
    // CALLER CODE GOES HERE ...
    //

    // We assume the session key obtained is stored in sessKey
    dwErrCode = RmJoinSession(&dwSessionHandle, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: In Vista, the subordinate is only allowed to 
    // register resources and cannot perform any other 
    // getlist, shutdown, restart or filter operations.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,     // Files
                                    0,  
                                    NULL,         // Processes
                                    0, 
                                    NULL);        // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // The subordinate leaves the conductor's session 
        // by calling RmEndSession(). The session itself 
        // won't be destroyed until the primary installer 
        // calls RmEndSession()
        //          
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}

```



 

 




