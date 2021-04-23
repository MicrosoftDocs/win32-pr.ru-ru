---
title: Регистрация для перезапуска приложения
description: Чтобы зарегистрировать приложение для перезапуска, вызовите функцию Регистераппликатионрестарт.
ms.assetid: 4dfbced7-77db-4042-823f-b4b81b2b27a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 717f8984f26570284a70b40eef70a9d6f753d66a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260995"
---
# <a name="registering-for-application-restart"></a><span data-ttu-id="26f1e-103">Регистрация для перезапуска приложения</span><span class="sxs-lookup"><span data-stu-id="26f1e-103">Registering for Application Restart</span></span>

<span data-ttu-id="26f1e-104">Чтобы зарегистрировать приложение для перезапуска, вызовите функцию [**регистераппликатионрестарт**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) .</span><span class="sxs-lookup"><span data-stu-id="26f1e-104">To register your application to be restarted, call the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function.</span></span> <span data-ttu-id="26f1e-105">[Отчеты об ошибках Windows (WER)](/windows/desktop/wer/windows-error-reporting) перезапускает приложение, если оно было запущено не менее 60 секунд, прежде чем перестать отвечать на запросы или не удается обнаружить необработанное исключение.</span><span class="sxs-lookup"><span data-stu-id="26f1e-105">[Windows Error Reporting (WER)](/windows/desktop/wer/windows-error-reporting) will restart your application if it has been running for at least 60 seconds before becoming unresponsive or encountering an unhandled exception.</span></span>

<span data-ttu-id="26f1e-106">Следует также рассмотреть возможность [регистрации для восстановления](registering-for-application-recovery.md), которая позволяет сохранять данные и сведения о состоянии, которые могут оказаться полезными при перезапуске приложения WER.</span><span class="sxs-lookup"><span data-stu-id="26f1e-106">You should consider also [registering for recovery](registering-for-application-recovery.md), which lets you save data and state information that may be helpful when WER restarts your application.</span></span> <span data-ttu-id="26f1e-107">WER перезапустит приложение после завершения процесса восстановления, если вы также зарегистрировались для восстановления.</span><span class="sxs-lookup"><span data-stu-id="26f1e-107">WER will restart the application after the recovery process completes, if you also register for recovery.</span></span>

<span data-ttu-id="26f1e-108">После завершения процесса восстановления WER завершает работу приложения, а затем перезапускает его.</span><span class="sxs-lookup"><span data-stu-id="26f1e-108">After the recovery process completes, WER terminates the application and then restarts it.</span></span> <span data-ttu-id="26f1e-109">Для консольных приложений приложение запускается в отдельном окне консоли, которое закрывается при выходе из приложения.</span><span class="sxs-lookup"><span data-stu-id="26f1e-109">For console applications, the application is started in a separate console window that closes when the application exits.</span></span>

<span data-ttu-id="26f1e-110">**Примечание для авторов установщика приложений:** Регистрация для перезапуска приложения также приведет к автоматическому перезапуску приложения после перезагрузки компьютера в случае перезагрузки компьютера из-за обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="26f1e-110">**Note for application installer authors:** Registering for application restart will also cause Windows to automatically restart the application after the computer is restarted in cases where the computer is restarted due to a software update.</span></span> <span data-ttu-id="26f1e-111">Чтобы это работало, установщик приложения должен вызвать функцию [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) с \_ установленным флагом евкс Рестартаппс или функцией [**инитиатешутдовн**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) с \_ установленным флагом Shutdown рестартаппс.</span><span class="sxs-lookup"><span data-stu-id="26f1e-111">For this to work, the installer of the application must call the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function with the EWX\_RESTARTAPPS flag set or the [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) function with the SHUTDOWN\_RESTARTAPPS flag set.</span></span>

<span data-ttu-id="26f1e-112">В следующем примере показано, как выполнить регистрацию, чтобы средство WER перезапускает приложение.</span><span class="sxs-lookup"><span data-stu-id="26f1e-112">The following example shows how to register to have WER restart your application.</span></span> <span data-ttu-id="26f1e-113">В примере возникает нарушение прав доступа после регистрации для перезапуска приложения.</span><span class="sxs-lookup"><span data-stu-id="26f1e-113">The example causes an access violation after registering for application restart.</span></span> <span data-ttu-id="26f1e-114">Нарушение прав доступа будет выотчеты об ошибках Windowsо, и будет продемонстрировано взаимодействие с пользователем при создании отчетов об ошибках, включая перезапуск приложения.</span><span class="sxs-lookup"><span data-stu-id="26f1e-114">The access violation will be picked up by Windows Error Reporting and will demonstrate the error reporting user experience, including application restart.</span></span> <span data-ttu-id="26f1e-115">Его следует запускать из окна консоли без аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="26f1e-115">It should be run from a console window with no command line arguments.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

#define RESTART_SWITCH L"/restart"

void GetRestartInfo(int argc, wchar_t* argv[], BOOL* pfIsRestart, DWORD* pdwRecordId); 
DWORD InitApplication(BOOL fIsRestart, DWORD* pdwRecordId); 
BOOL WINAPI CtrlHandler(DWORD dwControlType);
DWORD WINAPI Recover(PVOID pContext);

// A simple example to show how to use application recovery. For simplicity,
// the state information (record ID) is passed as part of the command line. 
void wmain(int argc, wchar_t* argv[])
{
    HRESULT hr = S_OK;
    DWORD dwRecordId = 0;
    BOOL fIsRestart = FALSE;

    GetRestartInfo(argc, argv, &fIsRestart, &dwRecordId);

    if (FAILED(hr = InitApplication(fIsRestart, &dwRecordId)))
    {
        wprintf(L"Failed to initialize the application.\n");
        goto cleanup;
    }

    // Do work. If you have a lot of state information, you should
    // periodically persist the state information to save time
    // in the recovery process.

    // The application must exist for at least 60 seconds for the
    // application to be restarted. Use Sleep() to mimic 60 seconds
    // worth of work.
    wprintf(L"Sleeping...\n");
    Sleep(62 * 1000);

    // Set the record ID to verify restart value.
    dwRecordId = 10;

    // Generate an access violation to force a restart. If we've already
    // restarted just exit because the example already demonstrated
    // the restart feature.
    if (FALSE == fIsRestart)
    {
        wprintf(L"Causing access violation...\n");
        int* p = NULL;
        *p = 5;
    }

cleanup:

    wprintf(L"Exiting...\n");
}


// Get the restart info from the command line. The command line is 
// of the form, /restart -r <RecordId>. The application 
// is being restarted if the first argument is /restart.
void GetRestartInfo(int argc, wchar_t* argv[], BOOL* pfIsRestart, DWORD* pdwRecordId) 
{
    if (argc > 1)
    {
        if (!wcsncmp(RESTART_SWITCH, argv[1], sizeof(RESTART_SWITCH)))
        {
            *pfIsRestart = TRUE;
            *pdwRecordId = _wtoi(argv[3]);
        }
    }

}

// Initialize the application. If this is a restart, use the state 
// information to reset the state of the application. This example 
// does not fail the initialization process if the process of 
// registering for application recovery and restart failed.
DWORD InitApplication(BOOL fIsRestart, DWORD* pdwRecordId)
{
    DWORD status = ERROR_SUCCESS;  // Set only if the initializing the application fails,
    HRESULT hr = S_OK;             // not if registering for recovery and restart fails.
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    wprintf(L"Entering InitApplication...\n");

    if (fIsRestart)
    {
        // TODO: Use the record ID to initialize the application.
        wprintf(L"Restart record ID is %lu\n", *pdwRecordId);
    }
    else
    {
        // This is not a restart, so initialize the application accordingly.
    }

    // Register for restart. The command line is updated in the recovery callback.
    RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
    StringCchPrintf(wsCommandLine, sizeof(wsCommandLine), L"/restart -r %lu", *pdwRecordId);

    hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
    if (FAILED(hr))
    {
        // Not failing because the registration failed.
        wprintf(L"RegisterApplicationRestart failed with ox%x.\n", hr);
        goto cleanup;
    }

    // Register the callback that handles the control event notifications.
    // Used for recovery when an installer is updating a component of the
    // application.
    if (!SetConsoleCtrlHandler(CtrlHandler, TRUE))
    {
        // Not failing initialization because the registration failed.
        // Consider calling UnregisterApplicationRestart if you must
        // have the latest state information.
        wprintf(L"SetConsoleCtrlHandler failed.\n");
        goto cleanup;
    }

    // Register the callback that handles recovery when the application
    // encounters an unhandled exception or becomes unresponsive.
    hr = RegisterApplicationRecoveryCallback(Recover, pdwRecordId, RECOVERY_DEFAULT_PING_INTERVAL, 0);
    if (FAILED(hr))
    {
        // Not failing initialization because the registration failed.
        // Consider calling UnregisterApplicationRestart if you must
        // have the latest state information.
        wprintf(L"RegisterApplicationRecoveryCallback failed with ox%x.\n", hr);
        goto cleanup;
    }

cleanup:

    return hr;
}


// Implement the callback for handling control character events.
// You'd implement this callback if an installer could update a
// component of your application. The system sends a CTRL_C_EVENT
// notification when an installer needs to shutdown your application
// or restart the computer in order to complete the installation.
// You can use the CTRL_C_EVENT to save final state information or
// data before exiting.
BOOL WINAPI CtrlHandler(DWORD dwControlType)
{
    wprintf(L"Entering CtrlHandler...\n");

    switch (dwControlType)
    {
        case CTRL_C_EVENT:
            wprintf(L"Handling CTRL_C_EVENT\n");
            return FALSE;

        // Other cases go here.

        default: 
            wprintf(L"Other, %ul\n", dwControlType);
            return FALSE;
    }
}


// Implement the recovery callback. This callback lets the application
// save state information or data in the event that the application
// encounters an unhandled exception or becomes unresponsive.
DWORD WINAPI Recover(PVOID pContext)
{
    HRESULT hr = S_OK;
    BOOL bCanceled = FALSE;
    DWORD dwRecordId = *(DWORD*)pContext;
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    wprintf(L"Entering Recover callback...\n");

    // Do recovery work. 

    // Update the restart command line.
    RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
    StringCchPrintf(wsCommandLine, sizeof(wsCommandLine), L"/restart -r %lu", dwRecordId);

    hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
    if (FAILED(hr))
    {
        // Not failing because the registration failed.
        wprintf(L"RegisterApplicationRestart failed with ox%x.\n", hr);
    }

    // You must call the ApplicationRecoveryInProgress function within
    // the specified ping interval or the recovery callback exits.
    // Typically, you would do a block of work, call the function, and repeat.
    hr = ApplicationRecoveryInProgress(&bCanceled);
    if (bCanceled)  
    {
        wprintf(L"Recovery was canceled by the user.\n");
        goto cleanup;
    }

    // Do more recovery work. 
    
    // You could also call the RegisterApplicationRestart function to
    // update the command line used for the restart.

cleanup:

    // Save the state file.

    wprintf(L"Leaving Recover callback...\n");
    ApplicationRecoveryFinished((bCanceled) ? FALSE: TRUE);

    return 0;
}
```



 

 