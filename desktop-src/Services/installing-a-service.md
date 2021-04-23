---
description: Программа настройки службы использует функцию CreateService для установки службы в базу данных SCM.
ms.assetid: b94bf94e-1b07-4686-be5c-306e7cf13f39
title: Установка службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e72953b2d3fc3ce549f614a035c9614c4d895a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662253"
---
# <a name="installing-a-service"></a><span data-ttu-id="866f7-103">Установка службы</span><span class="sxs-lookup"><span data-stu-id="866f7-103">Installing a Service</span></span>

<span data-ttu-id="866f7-104">[Программа настройки службы](service-configuration-programs.md) использует функцию [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для установки службы в базу данных SCM.</span><span class="sxs-lookup"><span data-stu-id="866f7-104">A [service configuration program](service-configuration-programs.md) uses the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to install a service in the SCM database.</span></span>

<span data-ttu-id="866f7-105">Функция СвЦинсталл в следующем примере показывает, как установить службу из самой программы Service.</span><span class="sxs-lookup"><span data-stu-id="866f7-105">The SvcInstall function in the following example shows how to install a service from the service program itself.</span></span> <span data-ttu-id="866f7-106">Полный пример см. в разделе [SVC. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="866f7-106">For the complete example, see [Svc.cpp](svc-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Installs a service in the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID SvcInstall()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    TCHAR szPath[MAX_PATH];

    if( !GetModuleFileName( "", szPath, MAX_PATH ) )
    {
        printf("Cannot install service (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Create the service

    schService = CreateService( 
        schSCManager,              // SCM database 
        SVCNAME,                   // name of service 
        SVCNAME,                   // service name to display 
        SERVICE_ALL_ACCESS,        // desired access 
        SERVICE_WIN32_OWN_PROCESS, // service type 
        SERVICE_DEMAND_START,      // start type 
        SERVICE_ERROR_NORMAL,      // error control type 
        szPath,                    // path to service's binary 
        NULL,                      // no load ordering group 
        NULL,                      // no tag identifier 
        NULL,                      // no dependencies 
        NULL,                      // LocalSystem account 
        NULL);                     // no password 
 
    if (schService == NULL) 
    {
        printf("CreateService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }
    else printf("Service installed successfully\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="866f7-107">См. также</span><span class="sxs-lookup"><span data-stu-id="866f7-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866f7-108">Установка, удаление и перечисление служб</span><span class="sxs-lookup"><span data-stu-id="866f7-108">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> <dt>

[<span data-ttu-id="866f7-109">Полный пример службы</span><span class="sxs-lookup"><span data-stu-id="866f7-109">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



