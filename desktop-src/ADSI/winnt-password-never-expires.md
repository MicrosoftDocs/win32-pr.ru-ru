---
title: Срок действия пароля никогда не истекает (поставщик WinNT)
description: Чтобы включить этот параметр с помощью поставщика WinNT ADSI, установите флаг ADS \_ УФ \_ не \_ Expires \_ (0x10000) в атрибуте усерфлагс. Примечание для Windows 2000 и более поздних версий используйте поставщик LDAP ADSI для операций управления пользователями, как показано ниже.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- Срок действия пароля никогда не истекает (поставщик WinNT)
- Срок действия пароля не ограничен интерфейсом ADSI, поставщик WinNT
- Службы WinNT Provider ADSI, примеры управления пользователями, срок действия пароля не истекает
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343871e7ba8748b3e406f7c84a5a34c01a2793a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105656816"
---
# <a name="password-never-expires-winnt-provider"></a>Срок действия пароля никогда не истекает (поставщик WinNT)

Чтобы включить этот параметр с помощью поставщика WinNT ADSI, установите флаг **ADS \_ УФ \_ не \_ Expires \_** (0x10000) в атрибуте **усерфлагс** .

> [!Note]  
> Для Windows 2000 и более поздних версий используйте поставщик LDAP ADSI для операций управления пользователями, как показано ниже. Дополнительные сведения см. в разделе [срок действия пароля никогда не истекает (поставщик LDAP)](password-never-expires.md).

 

## <a name="example-1"></a>Пример 1

В следующем примере кода показано, как задать параметр Password без истечения срока действия с помощью Visual Basic с ADSI.


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a>Пример 2

В следующем примере кода показано, как задать параметр Password без истечения срока действия с помощью C++ с ADSI.


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




