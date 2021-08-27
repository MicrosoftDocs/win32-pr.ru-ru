---
description: Программа настройки службы использует функции Чанжесервицеконфиг и ChangeServiceConfig2 для изменения параметров конфигурации установленной службы.
ms.assetid: 79aa4ad5-87ee-4f5d-9c8e-4e788f4c7182
title: Изменение конфигурации служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88cb7fe3739e1ff6cc47a548f5a40111c2383c27f2da34496e3038acbe835a4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126464"
---
# <a name="changing-a-services-configuration"></a>Изменение конфигурации службы

[Программа настройки службы](service-configuration-programs.md) использует функции [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) и [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) для изменения параметров конфигурации установленной службы. Программа открывает обработчик для объекта службы, изменяет его конфигурацию, а затем закрывает обработчик объекта службы.

В следующем примере функция Додисаблесвк использует [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) для изменения типа запуска службы на "Disabled", функция Доенаблесвк использует **чанжесервицеконфиг** для изменения типа запуска службы на "Enabled", а функция даупдатесвкдеск использует [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) , чтобы задать описание службы "это описание теста". Переменная Сзсвкнаме представляет собой глобальную переменную, которая содержит имя службы. Полный пример, задающий эту переменную, см. в разделе [свкконфиг. cpp](svcconfig-cpp.md).


```C++
//
// Purpose: 
//   Disables the service.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoDisableSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;

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

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,            // SCM database 
        szSvcName,               // name of service 
        SERVICE_CHANGE_CONFIG);  // need change config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Change the service start type.

    if (! ChangeServiceConfig( 
        schService,        // handle of service 
        SERVICE_NO_CHANGE, // service type: no change 
        SERVICE_DISABLED,  // service start type 
        SERVICE_NO_CHANGE, // error control: no change 
        NULL,              // binary path: no change 
        NULL,              // load order group: no change 
        NULL,              // tag ID: no change 
        NULL,              // dependencies: no change 
        NULL,              // account name: no change 
        NULL,              // password: no change 
        NULL) )            // display name: no change
    {
        printf("ChangeServiceConfig failed (%d)\n", GetLastError()); 
    }
    else printf("Service disabled successfully.\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}

//
// Purpose: 
//   Enables the service.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoEnableSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;

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

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,            // SCM database 
        szSvcName,               // name of service 
        SERVICE_CHANGE_CONFIG);  // need change config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Change the service start type.

    if (! ChangeServiceConfig( 
        schService,            // handle of service 
        SERVICE_NO_CHANGE,     // service type: no change 
        SERVICE_DEMAND_START,  // service start type 
        SERVICE_NO_CHANGE,     // error control: no change 
        NULL,                  // binary path: no change 
        NULL,                  // load order group: no change 
        NULL,                  // tag ID: no change 
        NULL,                  // dependencies: no change 
        NULL,                  // account name: no change 
        NULL,                  // password: no change 
        NULL) )                // display name: no change
    {
        printf("ChangeServiceConfig failed (%d)\n", GetLastError()); 
    }
    else printf("Service enabled successfully.\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}

//
// Purpose: 
//   Updates the service description to "This is a test description".
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoUpdateSvcDesc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    SERVICE_DESCRIPTION sd;
    LPTSTR szDesc = TEXT("This is a test description");

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

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,            // SCM database 
        szSvcName,               // name of service 
        SERVICE_CHANGE_CONFIG);  // need change config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Change the service description.

    sd.lpDescription = szDesc;

    if( !ChangeServiceConfig2(
        schService,                 // handle to service
        SERVICE_CONFIG_DESCRIPTION, // change: description
        &sd) )                      // new description
    {
        printf("ChangeServiceConfig2 failed\n");
    }
    else printf("Service description updated successfully.\n");

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Конфигурация службы.](service-configuration.md)
</dt> <dt>

[Полный пример службы](the-complete-service-sample.md)
</dt> </dl>

 

 



