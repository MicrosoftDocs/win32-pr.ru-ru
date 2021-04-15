---
title: Учетная запись отключена (поставщик WinNT)
description: При использовании поставщика WinNT учетную запись можно включить или отключить с помощью свойства IADsUser. Аккаунтдисаблед.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Учетная запись отключена (поставщик WinNT)
- Учетная запись отключила ADSI, поставщик WinNT
- Службы WinNT Provider ADSI, примеры управления пользователями, учетная запись отключена
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99b1fe45b71eda14547703f8721b2a13d581b8e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104424302"
---
# <a name="account-disabled-winnt-provider"></a>Учетная запись отключена (поставщик WinNT)

При использовании поставщика WinNT учетную запись можно включить или отключить с помощью свойства [**IADsUser. аккаунтдисаблед**](iadsuser-property-methods.md) .

## <a name="example-1"></a>Пример 1

В следующем примере кода показано, как отключить учетную запись, используя Visual Basic с ADSI.


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a>Пример 2

В следующем примере кода показано, как отключить учетную запись с помощью C++ и ADSI.


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




