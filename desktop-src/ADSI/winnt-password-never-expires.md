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
# <a name="password-never-expires-winnt-provider"></a><span data-ttu-id="5af60-106">Срок действия пароля никогда не истекает (поставщик WinNT)</span><span class="sxs-lookup"><span data-stu-id="5af60-106">Password Never Expires (WinNT Provider)</span></span>

<span data-ttu-id="5af60-107">Чтобы включить этот параметр с помощью поставщика WinNT ADSI, установите флаг **ADS \_ УФ \_ не \_ Expires \_** (0x10000) в атрибуте **усерфлагс** .</span><span class="sxs-lookup"><span data-stu-id="5af60-107">To enable this option using the WinNT ADSI provider, set the **ADS\_UF\_DONT\_EXPIRE\_PASSWD** (0x10000) flag on the **UserFlags** attribute.</span></span>

> [!Note]  
> <span data-ttu-id="5af60-108">Для Windows 2000 и более поздних версий используйте поставщик LDAP ADSI для операций управления пользователями, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="5af60-108">For Windows 2000 and later, use the LDAP ADSI provider for user management operations as shown.</span></span> <span data-ttu-id="5af60-109">Дополнительные сведения см. в разделе [срок действия пароля никогда не истекает (поставщик LDAP)](password-never-expires.md).</span><span class="sxs-lookup"><span data-stu-id="5af60-109">For more information, see [Password Never Expires (LDAP Provider)](password-never-expires.md).</span></span>

 

## <a name="example-1"></a><span data-ttu-id="5af60-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5af60-110">Example 1</span></span>

<span data-ttu-id="5af60-111">В следующем примере кода показано, как задать параметр Password без истечения срока действия с помощью Visual Basic с ADSI.</span><span class="sxs-lookup"><span data-stu-id="5af60-111">The following code example shows how to set the password never expires option using Visual Basic with ADSI.</span></span>


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="5af60-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5af60-112">Example 2</span></span>

<span data-ttu-id="5af60-113">В следующем примере кода показано, как задать параметр Password без истечения срока действия с помощью C++ с ADSI.</span><span class="sxs-lookup"><span data-stu-id="5af60-113">The following code example shows how to set the password never expires option using C++ with ADSI.</span></span>


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



 

 




