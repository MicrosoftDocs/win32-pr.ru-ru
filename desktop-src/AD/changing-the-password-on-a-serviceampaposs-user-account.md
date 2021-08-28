---
title: Изменение пароля для учетной записи пользователя службы
description: Для экземпляра службы, который входит в систему с учетной записью пользователя, а не учетной записью LocalSystem, диспетчер управления службами (SCM) на главном компьютере хранит пароль учетной записи, который используется для входа в службу при запуске службы.
ms.assetid: d9cef772-bd85-4103-901e-3cf786b29163
ms.tgt_platform: multiple
keywords:
- Изменение пароля учетной записи пользователя службы AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66f0d7b4dc668697b7a0a8d5b120735f3a445cf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881628"
---
# <a name="changing-the-password-on-a-services-user-account"></a>Изменение пароля для учетной записи пользователя службы

Для экземпляра службы, который входит в систему с учетной записью пользователя, а не учетной записью LocalSystem, диспетчер управления службами (SCM) на главном компьютере хранит пароль учетной записи, который используется для входа в службу при запуске службы. Как и для любой учетной записи пользователя, необходимо периодически менять пароль для обеспечения безопасности. При изменении пароля учетной записи службы обновите пароль, хранящийся в SCM. В следующем примере кода показано, как выполнить оба действия.

В примерах кода для задания пароля учетной записи используется [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . Этот метод использует различающееся имя учетной записи. Затем в примере открывается обработчик для установленной службы на указанном главном компьютере и используется функция [**чанжесервицеконфиг**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) для обновления пароля, кэшированного SCM. Эта функция использует имя SAM &lt; &gt; \\ &lt; учетной записи ("домен имя_пользователя &gt; ").

> [!Note]  
> Этот код должен быть выполнен администратором домена.

 

Для реплицируемой службы, в которой каждая реплика использует другую учетную запись входа, можно обновить пароли для всех реплик, перечисляя экземпляры службы. Дополнительные сведения и пример кода см. в разделе [перечисление реплик службы](enumerating-the-replicas-of-a-service.md).


```C++
DWORD UpdateAccountPassword(
    LPTSTR szServerDNS,   // DNS name of host computer
    LPTSTR szAccountDN,   // Distinguished name of service 
                          // logon account
    LPTSTR szServiceName, // Name of the service
    LPTSTR szOldPassword, // Old password
    LPTSTR szNewPassword  // New password
    )
{
SC_HANDLE schService = NULL;
SC_HANDLE schSCManager = NULL;
 
DWORD dwLen = MAX_PATH;
TCHAR szAccountPath[MAX_PATH];
IADsUser *pUser = NULL;
HRESULT hr;
 
DWORD dwStatus = 0;
SC_LOCK sclLock = NULL; 

if( !szServerDNS || 
    !szAccountDN || 
    !szServiceName || 
    !szOldPassword || 
    !szNewPassword)
{
    _tprintf(TEXT("Invalid parameter"));
    goto cleanup;
}
 
// Set the password on the account.
// Use the distinguished name to bind to the account object.
_tcsncpy_s(szAccountPath, TEXT("LDAP://"), MAX_PATH);
_tcscat_s(szAccountPath, 
    szAccountDN, 
    MAX_PATH - _tcslen(szAccountPath));
hr = ADsGetObject(szAccountPath, IID_IADsUser, (void**)&pUser);
if (FAILED(hr)) 
{
    _tprintf(TEXT("Get IADsUser failed - 0x%x\n"), dwStatus = hr);
       goto cleanup;
}
 
// Set the password on the account. 
hr = pUser->ChangePassword(CComBSTR(szOldPassword), 
    CComBSTR(szNewPassword));
if (FAILED(hr)) 
{
    _tprintf(TEXT("ChangePassword failed - 0x%x\n"), 
             dwStatus = hr);
    goto cleanup;
}
 
// Update the account and password in the SCM database.
// Open the Service Control Manager on the specified computer.
schSCManager = OpenSCManager(
                szServerDNS,          // DNS name of host computer
                NULL,                 // database (NULL == default)
                SC_MANAGER_ALL_ACCESS // access required
                        );
if (! schSCManager) 
{
    _tprintf(TEXT("OpenSCManager failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Open a handle to the service instance.
schService = OpenService(schSCManager, 
    szServiceName, 
    SERVICE_ALL_ACCESS);
if (! schService) 
{
    _tprintf(TEXT("OpenService failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Get the SCM database lock before changing the password. 
sclLock = LockServiceDatabase(schSCManager); 
if (sclLock == NULL) {
    _tprintf(TEXT("LockServiceDatabase failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
 
// Set the account and password that the service uses at startup.
if (! ChangeServiceConfig( 
        schService,        // Handle of service 
        SERVICE_NO_CHANGE, // Service type: no change 
        SERVICE_NO_CHANGE, // Change service start type 
        SERVICE_NO_CHANGE, // Error control: no change 
        NULL,              // Binary path: no change 
        NULL,              // Load order group: no change 
        NULL,              // Tag ID: no change 
        NULL,              // Dependencies: no change 
        NULL,              // Account name: no change 
        szNewPassword,     // New password 
        NULL) )            // Display name: no change
{
    _tprintf(TEXT("ChangeServiceConfig failed - %d\n"), 
        dwStatus = GetLastError());
    goto cleanup;
}
_tprintf(TEXT("Password changed for service instance on: %s\n"), 
    szServerDNS);

cleanup:
 
if (sclLock)
    UnlockServiceDatabase(sclLock); 
if (schService)
    CloseServiceHandle(schService);
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (pUser)
    pUser->Release();
 
return dwStatus;
}
```



 

 
