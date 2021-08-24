---
title: Регистрация имен участников-служб для службы
description: В следующем примере кода регистрируется или отменяется регистрация одного или нескольких имен субъектов-служб (SPN) для экземпляра службы.
ms.assetid: 60c252c7-76d2-4683-bf90-0f3483e6e8e0
ms.tgt_platform: multiple
keywords:
- Регистрация имен участников-служб для службы AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ff5d339ac9c2e51bceb15f29b7ad9cfd94e992ce826d596e2d81fcb25178ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184449"
---
# <a name="registering-the-spns-for-a-service"></a>Регистрация имен участников-служб для службы

В следующем примере кода регистрируется или отменяется регистрация одного или нескольких имен субъектов-служб (SPN) для экземпляра службы.

В этом примере вызывается функция [**дсвритеаккаунтспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) , которая хранит имена участников-служб в домен Active Directory Services [**в атрибуте «**](/windows/desktop/ADSchema/a-serviceprincipalname) перечислить» объекта Account, заданного параметром *псзсервицеакктдн* . Объект Account соответствует учетной записи входа, указанной в вызове [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) для этого экземпляра службы. Если учетная запись входа является учетной записью пользователя домена, *псзсервицеакктдн* должен быть различающимся именем объекта учетной записи в домен Active Directory серверах для этой учетной записи пользователя. Если учетная запись входа в службу является учетной записью LocalSystem, *псзсервицеакктдн* должно быть различающимся именем объекта учетной записи компьютера для главного компьютера, на котором установлена служба.


```C++
/***************************************************************************

    SpnRegister()

    Register or unregister the SPNs under the service's account.

    If the service runs in LocalSystem account, pszServiceAcctDN is the 
    distinguished name of the local computer account.

    Parameters:

    pszServiceAcctDN - Contains the distinguished name of the logon 
    account for this instance of the service.

    pspn - Contains an array of SPNs to register.

    ulSpn - Contains the number of SPNs in the array.

    Operation - Contains one of the DS_SPN_WRITE_OP values that determines 
    the type of operation to perform on the SPNs.

***************************************************************************/

DWORD SpnRegister(TCHAR *pszServiceAcctDN,
                  TCHAR **pspn,
                  unsigned long ulSpn,
                  DS_SPN_WRITE_OP Operation)
{
    DWORD dwStatus;
    HANDLE hDs;
    TCHAR szSamName[512];
    DWORD dwSize = sizeof(szSamName) / sizeof(szSamName[0]);
    PDOMAIN_CONTROLLER_INFO pDcInfo;

    // Bind to a domain controller. 
    // Get the domain for the current user.
    if(GetUserNameEx(NameSamCompatible, szSamName, &dwSize))
    {
        TCHAR *pWhack = _tcschr(szSamName, '\\');
        if(pWhack)
        {
            *pWhack = '\0';
        }
    } 
    else 
    {
        return GetLastError();
    }
     
    // Get the name of a domain controller in that domain.
    dwStatus = DsGetDcName(NULL,
        szSamName,
        NULL,
        NULL,
        DS_IS_FLAT_NAME |
            DS_RETURN_DNS_NAME |
            DS_DIRECTORY_SERVICE_REQUIRED,
        &pDcInfo);
    if(dwStatus != 0) 
    {
        return dwStatus;
    }
     
    // Bind to the domain controller.
    dwStatus = DsBind(pDcInfo->DomainControllerName, NULL, &hDs);
     
    // Free the DOMAIN_CONTROLLER_INFO buffer.
    NetApiBufferFree(pDcInfo);
    if(dwStatus != 0) 
    {
        return dwStatus;
    }
     
    // Write the SPNs to the service account or computer account.
    dwStatus = DsWriteAccountSpn(
            hDs,                    // Handle to the directory.
            Operation,              // Add or remove SPN from account's existing SPNs.
            pszServiceAcctDN,       // DN of service account or computer account.
            ulSpn,                  // Number of SPNs to add.
            (const TCHAR **)pspn);  // Array of SPNs.

    // Unbind the DS in any case.
    DsUnBind(&hDs);
     
    return dwStatus;
}
```



 

 