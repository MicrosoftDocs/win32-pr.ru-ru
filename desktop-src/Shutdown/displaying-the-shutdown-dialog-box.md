---
description: В следующем примере выполняется перезагрузка локальной системы с помощью функции Инитиатесистемшутдовн.
ms.assetid: 928c2d48-daa5-4c27-816b-766adedba7eb
title: Отображение диалогового окна «Завершение работы»
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedfee9e96fa1e6183cbe1d9322a603b65ae4b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663088"
---
# <a name="displaying-the-shutdown-dialog-box"></a><span data-ttu-id="31902-103">Отображение диалогового окна «Завершение работы»</span><span class="sxs-lookup"><span data-stu-id="31902-103">Displaying the Shutdown Dialog Box</span></span>

<span data-ttu-id="31902-104">В следующем примере выполняется перезагрузка локальной системы с помощью функции [**инитиатесистемшутдовн**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) .</span><span class="sxs-lookup"><span data-stu-id="31902-104">The following example reboots the local system using the [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) function.</span></span> <span data-ttu-id="31902-105">Система отображает диалоговое окно с пользовательским сообщением и сообщением для закрытия приложений в течение заданного интервала времени ожидания (30 секунд).</span><span class="sxs-lookup"><span data-stu-id="31902-105">The system displays a dialog box with a custom message and a message to the user to close applications within the specified time-out interval (30 seconds).</span></span> <span data-ttu-id="31902-106">По истечении интервала времени ожидания система перезапускается.</span><span class="sxs-lookup"><span data-stu-id="31902-106">After the time-out interval elapses, the system is restarted.</span></span>

<span data-ttu-id="31902-107">\_ \_ Перед вызовом [**инитиатесистемшутдовн**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)приложение должно включить привилегию имени для завершения работы SE.</span><span class="sxs-lookup"><span data-stu-id="31902-107">The application must enable the SE\_SHUTDOWN\_NAME privilege before calling [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna).</span></span> <span data-ttu-id="31902-108">Дополнительные сведения см. в разделе [привилегии](../secauthz/privileges.md).</span><span class="sxs-lookup"><span data-stu-id="31902-108">For more information, see [Privileges](../secauthz/privileges.md).</span></span>


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL MySystemShutdown( LPTSTR lpMsg )
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   BOOL fResult;               // system shutdown flag 
 
   // Get the current process token handle so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
      (PTOKEN_PRIVILEGES) NULL, 0); 
 
   // Cannot test the return value of AdjustTokenPrivileges. 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Display the shutdown dialog box and start the countdown. 
 
   fResult = InitiateSystemShutdown( 
      NULL,    // shut down local computer 
      lpMsg,   // message for user
      30,      // time-out period, in seconds 
      FALSE,   // ask user to close apps 
      TRUE);   // reboot after shutdown 
 
   if (!fResult) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE; 
}
```



<span data-ttu-id="31902-109">Если функция [**абортсистемшутдовн**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) выполняется в течение времени ожидания, заданного параметром [**инитиатесистемшутдовн**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), система не завершает работу.</span><span class="sxs-lookup"><span data-stu-id="31902-109">If the [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) function is executed in the time-out period specified by [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), the system does not shut down.</span></span> <span data-ttu-id="31902-110">Например, если Превентсистемшутдовн вызывается после Мисистемшутдовн, система закрывает диалоговое окно и не перезапускает систему.</span><span class="sxs-lookup"><span data-stu-id="31902-110">For example, if PreventSystemShutdown is called after MySystemShutdown, the system closes the dialog box and does not restart the system.</span></span>


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL PreventSystemShutdown()
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   // Get the current process token handle  so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
         TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
         &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Prevent the system from shutting down. 
 
   if ( !AbortSystemShutdown(NULL) ) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
       (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE;
}
```



 

 
