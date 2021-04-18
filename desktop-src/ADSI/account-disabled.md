---
title: Учетная запись отключена (поставщик LDAP)
description: Чтобы отключить учетную запись пользователя, задайте для свойства Аккаунтдисаблед в интерфейсе IADsUser значение TRUE. Это похоже на поставщика WinNT. В следующих примерах кода показано, как отключить учетную запись пользователя.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- Учетная запись отключила ADSI, поставщик LDAP
- ADSI поставщика LDAP, примеры управления пользователями, учетная запись отключена
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61fb65a06f4e2afb1b43595b955c577b2a6090
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105656819"
---
# <a name="account-disabled-ldap-provider"></a>Учетная запись отключена (поставщик LDAP)

Чтобы отключить учетную запись пользователя, задайте для свойства Аккаунтдисаблед в интерфейсе [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) значение **true** . Это похоже на поставщика WinNT. В следующих примерах кода показано, как отключить учетную запись пользователя.

## <a name="example-1"></a>Пример 1


```VB
Dim usr As IADsUser
On Error GoTo Cleanup

Set usr = GetObject("LDAP:// CN=JeffSmith, OU=Sales, DC=Fabrikam, DC=Com")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



## <a name="example-2"></a>Пример 2


```C++
IADsUser *pUser = NULL;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"LDAP://serv1/cn=Jeff Smith,cn=Users, dc=Fabrikam, dc=com";
hr = ADsGetObject(adsPath,IID_IADsUser,(void**)&pUser);

if(FAILED(hr)){return;}

hr = pUser->put_AccountDisabled(true);
hr = pUser->SetInfo();
```



 

 




