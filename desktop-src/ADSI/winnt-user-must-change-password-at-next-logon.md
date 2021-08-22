---
title: Пользователь должен сменить пароль при следующем входе в систему (поставщик WinNT)
description: Чтобы включить этот параметр, задайте для атрибута Пассвордекспиред пользователя значение One (1). Установка этого атрибута равным нулю (0) позволяет пользователю войти в систему, не меняя пароль.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- Пользователь должен сменить пароль при следующем входе (WinNT Provider) ADSI
- Пользователь должен сменить пароль при следующем входе в систему ADSI, поставщик WinNT
- WinNT Provider ADSI, примеры управления пользователями, пользователь должен сменить пароль при следующем входе в систему
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be50e5cdccb4969e59a5b32516a35278b867062e8cced2e80d96b26c56c6173b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023042"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a>Пользователь должен сменить пароль при следующем входе в систему (поставщик WinNT)

Чтобы включить этот параметр, задайте для атрибута **пассвордекспиред** пользователя значение One (1). Установка этого атрибута равным нулю (0) позволяет пользователю войти в систему, не меняя пароль.

## <a name="example-1"></a>Пример 1

в следующем примере кода показано, как задать параметр сменить пароль при следующем входе в систему с помощью Visual Basic с интерфейсом ADSI.


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a>Пример 2

В следующем примере кода показано, как задать параметр сменить пароль при следующем входе в систему с помощью C++ и ADSI.


```C++
IADsUser *pUser = NULL;
HRESULT hr;

hr=ADsGetObject(L"WinNT://Fabrikam/jeffsmith,user",
                IID_IADsUser,
                (void**)&pUser);
VARIANT var;
VariantInit(&var);
V_I4(&var)=1;
V_VT(&var)=VT_I4;
hr = pUser->Put(_bstr_t("PasswordExpired"),var); // User must change password.
hr = pUser->SetInfo();

VariantClear(&var);
pUser->Release();
```



 

 




