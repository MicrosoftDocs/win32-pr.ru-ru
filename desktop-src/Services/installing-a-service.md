---
description: Программа настройки службы использует функцию CreateService для установки службы в базу данных SCM.
ms.assetid: b94bf94e-1b07-4686-be5c-306e7cf13f39
title: Установка службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 955875511688f9c3f2437d60fd615617e964c8f2f60333a7410143c7d451494b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968022"
---
# <a name="installing-a-service"></a>Установка службы

[Программа настройки службы](service-configuration-programs.md) использует функцию [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) для установки службы в базу данных SCM.

Функция СвЦинсталл в следующем примере показывает, как установить службу из самой программы Service. Полный пример см. в разделе [SVC. cpp](svc-cpp.md).


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Установка, удаление и перечисление служб](service-installation-removal-and-enumeration.md)
</dt> <dt>

[Полный пример службы](the-complete-service-sample.md)
</dt> </dl>

 

 



