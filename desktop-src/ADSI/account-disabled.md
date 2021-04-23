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
# <a name="account-disabled-ldap-provider"></a><span data-ttu-id="4f814-107">Учетная запись отключена (поставщик LDAP)</span><span class="sxs-lookup"><span data-stu-id="4f814-107">Account Disabled (LDAP Provider)</span></span>

<span data-ttu-id="4f814-108">Чтобы отключить учетную запись пользователя, задайте для свойства Аккаунтдисаблед в интерфейсе [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) значение **true** .</span><span class="sxs-lookup"><span data-stu-id="4f814-108">To disable a user account, set the AccountDisabled property to **TRUE** in the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span> <span data-ttu-id="4f814-109">Это похоже на поставщика WinNT.</span><span class="sxs-lookup"><span data-stu-id="4f814-109">This is similar to the WinNT provider.</span></span> <span data-ttu-id="4f814-110">В следующих примерах кода показано, как отключить учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="4f814-110">The following code examples show how to disable a user account.</span></span>

## <a name="example-1"></a><span data-ttu-id="4f814-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f814-111">Example 1</span></span>


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



## <a name="example-2"></a><span data-ttu-id="4f814-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4f814-112">Example 2</span></span>


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



 

 




