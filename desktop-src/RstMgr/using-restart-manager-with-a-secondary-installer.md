---
title: Использование диспетчера перезапуска с дополнительным установщиком
description: В следующей процедуре описывается использование диспетчера перезапуска с основным и дополнительным установщиками.
ms.assetid: aa55ab09-206b-49ed-8cb4-e311c1ed2d9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aefb1f9658752677e7850e939fcb6a3c4c6047c5efc2dc0ceb06ec0f51900ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009992"
---
# <a name="using-restart-manager-with-a-secondary-installer"></a>Использование диспетчера перезапуска с дополнительным установщиком

В следующей процедуре описывается использование диспетчера перезапуска с основным и дополнительным установщиками.

При использовании основных и вторичных установщиков основной установщик управляет пользовательским интерфейсом.

**Использование диспетчера перезапуска с основным и дополнительным установщиками**

1.  Основной установщик вызывает функцию [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) для запуска сеанса диспетчера перезапуска и получения маркера сеанса и ключа.
2.  Основной установщик запускает или связывается с дополнительным установщиком и предоставляет ему ключ сеанса, полученный на предыдущем шаге.
3.  Вторичный установщик вызывает функцию [**рмжоинсессион**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) с ключом сеанса, чтобы присоединиться к сеансу диспетчера перезапуска. Вторичный установщик может присоединиться к сеансу, запущенному основным установщиком, только если оба установщика работают в одном контексте пользователя.
4.  Основной и дополнительный установщики вызывают функцию [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) для регистрации ресурсов. Диспетчер перезапуска может использовать только зарегистрированные ресурсы, чтобы определить, какие приложения и службы должны быть выключены и перезапущены. Все ресурсы, на которые может повлиять установка, должны быть зарегистрированы в сеансе. Ресурсы можно идентифицировать по имени файла, краткому имени службы или структуре [**\_ уникального \_ процесса RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) .
5.  Основной установщик вызывает функцию [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) для получения массива структур [**\_ \_ сведений о процессе RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) , в котором перечислены все приложения и службы, которые должны быть выключены и перезапущены.

    Если значение параметра *лпдвребутреасон* , возвращаемое функцией [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) , не равно нулю, диспетчеру перезапуска не удается освободить зарегистрированный ресурс при завершении работы приложения или службы. В этом случае для продолжения установки требуется завершение работы системы и перезапуск. Основной установщик должен запрашивать у пользователя действие, прекращать работу программ или служб или запланировать завершение работы и перезагрузку системы.

    Если значение параметра *лпдвребутреасон* , возвращаемое функцией [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) , равно нулю, установщик должен вызвать функцию [**рмшутдовн**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) . При этом службы и приложения, использующие зарегистрированные ресурсы, завершаются. Затем основной и дополнительный установщики должны выполнить системные изменения, необходимые для завершения установки. Наконец, основной установщик должен вызвать функцию [**рмрестарт**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) , чтобы диспетчер перезапуска мог перезапустить приложения, работа которых была завершена и которые были зарегистрированы для перезапуска.

6.  Основной и дополнительный установщик вызывают функцию [**рмендсессион**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) , чтобы закрыть сеанс диспетчера перезапуска.

В следующем фрагменте кода показан пример основного установщика, запускаемого и использующего сеанс диспетчера перезапуска. для примера требуется Windows 7 или Windows Server 2008 R2. в Windows Vista или Windows Server 2008 приложение калькулятора закрывается, но не перезапускается. В этом примере показано, как основной установщик может использовать диспетчер перезапуска для завершения работы и перезапуска процесса. В примере предполагается, что калькулятор уже выполняется перед запуском сеанса диспетчера перезапуска.


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



В следующем фрагменте кода приведен пример присоединения дополнительного установщика к существующему сеансу диспетчера перезапуска. для примера требуется Windows Vista или Windows Server 2008. Вторичный установщик получает ключ сеанса от основного установщика и использует его для приподключения к сеансу.


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



 

 




