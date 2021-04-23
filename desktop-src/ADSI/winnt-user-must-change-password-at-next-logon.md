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
ms.openlocfilehash: 787be5f5f4e1534574a68c179bb699ac68c61e3e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105656815"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a><span data-ttu-id="a6532-107">Пользователь должен сменить пароль при следующем входе в систему (поставщик WinNT)</span><span class="sxs-lookup"><span data-stu-id="a6532-107">User Must Change Password at Next Logon (WinNT Provider)</span></span>

<span data-ttu-id="a6532-108">Чтобы включить этот параметр, задайте для атрибута **пассвордекспиред** пользователя значение One (1).</span><span class="sxs-lookup"><span data-stu-id="a6532-108">To enable this option, set the **PasswordExpired** attribute of the user to one (1).</span></span> <span data-ttu-id="a6532-109">Установка этого атрибута равным нулю (0) позволяет пользователю войти в систему, не меняя пароль.</span><span class="sxs-lookup"><span data-stu-id="a6532-109">Setting this attribute to zero (0) enables the user to log on without changing the password.</span></span>

## <a name="example-1"></a><span data-ttu-id="a6532-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6532-110">Example 1</span></span>

<span data-ttu-id="a6532-111">В следующем примере кода показано, как задать параметр сменить пароль при следующем входе в систему с помощью Visual Basic с интерфейсом ADSI.</span><span class="sxs-lookup"><span data-stu-id="a6532-111">The following code example shows how to set the change password on next logon option using Visual Basic with ADSI.</span></span>


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="a6532-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a6532-112">Example 2</span></span>

<span data-ttu-id="a6532-113">В следующем примере кода показано, как задать параметр сменить пароль при следующем входе в систему с помощью C++ и ADSI.</span><span class="sxs-lookup"><span data-stu-id="a6532-113">The following code example shows how to set the change password on next logon option using C++ with ADSI.</span></span>


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



 

 




