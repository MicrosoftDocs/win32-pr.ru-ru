---
title: Изменение пароля для учетной записи пользователя службы
description: Для экземпляра службы, который входит в систему с учетной записью пользователя, а не учетной записью LocalSystem, диспетчер управления службами (SCM) на главном компьютере хранит пароль учетной записи, который используется для входа в службу при запуске службы.
ms.assetid: d9cef772-bd85-4103-901e-3cf786b29163
ms.tgt_platform: multiple
keywords:
- Изменение пароля учетной записи пользователя службы AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf16b018796979d3710825472a5f9abab72cd24
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487500"
---
# <a name="changing-the-password-on-a-services-user-account"></a><span data-ttu-id="abbd2-104">Изменение пароля для учетной записи пользователя службы</span><span class="sxs-lookup"><span data-stu-id="abbd2-104">Changing the Password on a Service's User Account</span></span>

<span data-ttu-id="abbd2-105">Для экземпляра службы, который входит в систему с учетной записью пользователя, а не учетной записью LocalSystem, диспетчер управления службами (SCM) на главном компьютере хранит пароль учетной записи, который используется для входа в службу при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="abbd2-105">For a service instance that logs on with a user account, rather than the LocalSystem account, the Service Control Manager (SCM) on the host computer stores the account password, which it uses to log on the service when the service starts.</span></span> <span data-ttu-id="abbd2-106">Как и для любой учетной записи пользователя, необходимо периодически менять пароль для обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="abbd2-106">As with any user account, you must change the password periodically to maintain security.</span></span> <span data-ttu-id="abbd2-107">При изменении пароля учетной записи службы обновите пароль, хранящийся в SCM.</span><span class="sxs-lookup"><span data-stu-id="abbd2-107">When you change the password on a service account, update the password stored by the SCM.</span></span> <span data-ttu-id="abbd2-108">В следующем примере кода показано, как выполнить оба действия.</span><span class="sxs-lookup"><span data-stu-id="abbd2-108">The following code example shows how to do both.</span></span>

<span data-ttu-id="abbd2-109">В примерах кода для задания пароля учетной записи используется [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="abbd2-109">The code examples use [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) to set the account password.</span></span> <span data-ttu-id="abbd2-110">Этот метод использует различающееся имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="abbd2-110">This method uses the distinguished name of the account.</span></span> <span data-ttu-id="abbd2-111">Затем в примере открывается обработчик для установленной службы на указанном главном компьютере и используется функция [**чанжесервицеконфиг**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) для обновления пароля, кэшированного SCM.</span><span class="sxs-lookup"><span data-stu-id="abbd2-111">Then the sample opens a handle to the installed service on the specified host computer, and uses the [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) function to update the password cached by the SCM.</span></span> <span data-ttu-id="abbd2-112">Эта функция использует имя SAM (" <domain> \\ <username> ") учетной записи.</span><span class="sxs-lookup"><span data-stu-id="abbd2-112">This function uses the SAM name ("<domain>\\<username>") of the account.</span></span>

> [!Note]  
> <span data-ttu-id="abbd2-113">Этот код должен быть выполнен администратором домена.</span><span class="sxs-lookup"><span data-stu-id="abbd2-113">This code must be executed by a domain administrator.</span></span>

 

<span data-ttu-id="abbd2-114">Для реплицируемой службы, в которой каждая реплика использует другую учетную запись входа, можно обновить пароли для всех реплик, перечисляя экземпляры службы.</span><span class="sxs-lookup"><span data-stu-id="abbd2-114">For a replicable service in which each replica uses a different logon account, you could update the passwords for all of the replicas by enumerating the service instances.</span></span> <span data-ttu-id="abbd2-115">Дополнительные сведения и пример кода см. в разделе [перечисление реплик службы](enumerating-the-replicas-of-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="abbd2-115">For more information and a code example, see [Enumerating the Replicas of a Service](enumerating-the-replicas-of-a-service.md).</span></span>


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



 

 