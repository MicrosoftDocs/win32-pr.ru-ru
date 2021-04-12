---
title: Срок действия пароля не истекает (поставщик LDAP)
description: Чтобы включить параметр "срок действия пароля не ограничен" с помощью поставщика LDAP, установите \_ флаг ADS УФ \_ не \_ Expires \_ PASSWD для атрибута userAccountControl пользователя.
ms.assetid: b8d7e7fe-c846-45c4-9c5f-770530453836
ms.tgt_platform: multiple
keywords:
- Срок действия пароля не ограничен интерфейсом ADSI, поставщику LDAP
- ADSI поставщика LDAP, примеры управления пользователями, срок действия пароля не истекает
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c0d9eb42d37c1bcc7d65495fa0d72609060407
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413721"
---
# <a name="password-never-expires-ldap-provider"></a>Срок действия пароля не истекает (поставщик LDAP)

Чтобы включить параметр "срок действия пароля не ограничен" с помощью поставщика LDAP, установите флаг [**ADS \_ УФ \_ не \_ Expires \_ PASSWD**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) для атрибута [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) пользователя.


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000

Set usr = GetObject("LDAP://CN=jeffsmith,OU=Sales,DC=Fabrikam,DC=Com")
flag = usr.Get("userAccountControl")
newFlag = flag Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "userAccountControl", newFlag
usr.SetInfo
```




```C++
#include <activeds.h>

IADsUser *pUser;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath = L"LDAP://serv1/cn=Jeff Smith,cn=Users,dc=Fabrikam,dc=com";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->Get(_bstr_t("userAccountControl"), &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(_bstr_t("userAccountControl"), var);

hr = pUser->SetInfo();
VariantClear(&var);
hr = pUser->Release();
```



 

 