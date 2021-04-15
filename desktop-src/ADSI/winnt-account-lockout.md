---
title: Блокировка учетной записи (поставщик WinNT)
description: При превышении числа неудачных попыток входа учетная запись пользователя блокируется на количество минут, заданное атрибутом Локкаутдуратион.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Блокировка учетной записи ADSI, поставщик WinNT
- Службы WinNT Provider ADSI, примеры управления пользователями, блокировка учетной записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654365"
---
# <a name="account-lockout-winnt-provider"></a><span data-ttu-id="26963-105">Блокировка учетной записи (поставщик WinNT)</span><span class="sxs-lookup"><span data-stu-id="26963-105">Account Lockout (WinNT Provider)</span></span>

<span data-ttu-id="26963-106">При превышении числа неудачных попыток входа учетная запись пользователя блокируется на количество минут, заданное атрибутом [**локкаутдуратион**](/windows/desktop/ADSchema/a-lockoutduration) .</span><span class="sxs-lookup"><span data-stu-id="26963-106">When the number of failed logon attempts is exceeded, the user account becomes locked out for the number of minutes specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="26963-107">Свойство [**IADsUser. исаккаунтлоккед**](iadsuser-property-methods.md) является свойством, используемым для чтения и изменения состояния блокировки учетной записи пользователя, но у поставщика WinNT ADSI есть ограничения, ограничивающие использование свойства **исаккаунтлоккед** .</span><span class="sxs-lookup"><span data-stu-id="26963-107">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the WinNT ADSI provider has restrictions that limit the use of the **IsAccountLocked** property.</span></span>

## <a name="resetting-the-account-lockout-status"></a><span data-ttu-id="26963-108">Сброс состояния блокировки учетной записи</span><span class="sxs-lookup"><span data-stu-id="26963-108">Resetting the Account Lockout Status</span></span>

<span data-ttu-id="26963-109">При использовании поставщика WinNT свойству [**исаккаунтлоккед**](iadsuser-property-methods.md) может быть присвоено только **значение false**, которое разблокирует учетную запись.</span><span class="sxs-lookup"><span data-stu-id="26963-109">When using the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can only be set to **FALSE**, which unlocks the account.</span></span> <span data-ttu-id="26963-110">Попытка установить свойство **исаккаунтлоккед** в **значение true** завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="26963-110">Attempting to set the **IsAccountLocked** property to **TRUE** will fail.</span></span> <span data-ttu-id="26963-111">Только система может заблокировать учетную запись.</span><span class="sxs-lookup"><span data-stu-id="26963-111">Only the system can lock an account.</span></span>

<span data-ttu-id="26963-112">В следующем примере кода показано, как использовать Visual Basic с интерфейсом ADSI для разблокировки учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="26963-112">The following code example demonstrates how to use Visual Basic with ADSI to unlock a user account.</span></span>


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



<span data-ttu-id="26963-113">В следующем примере кода показано, как использовать C++ с ADSI для разблокировки учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="26963-113">The following code example demonstrates how to use C++ with ADSI to unlock a user account.</span></span>


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a><span data-ttu-id="26963-114">Чтение состояния блокировки учетной записи</span><span class="sxs-lookup"><span data-stu-id="26963-114">Reading the Account Lockout Status</span></span>

<span data-ttu-id="26963-115">С помощью поставщика WinNT можно использовать свойство [**исаккаунтлоккед**](iadsuser-property-methods.md) , чтобы определить, заблокирована ли учетная запись. Если учетная запись заблокирована, свойство **исаккаунтлоккед** будет содержать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="26963-115">With the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can be used to determine if an account is locked out. If an account is locked out, the **IsAccountLocked** property will contain **TRUE**.</span></span> <span data-ttu-id="26963-116">Если учетная запись не заблокирована, свойство **исаккаунтлоккед** будет содержать **значение false**.</span><span class="sxs-lookup"><span data-stu-id="26963-116">If an account is not locked out, the **IsAccountLocked** property will contain **FALSE**.</span></span>

<span data-ttu-id="26963-117">В следующем примере кода показано, как использовать Visual Basic с интерфейсом ADSI, чтобы определить, заблокирована ли учетная запись.</span><span class="sxs-lookup"><span data-stu-id="26963-117">The following code example demonstrates how to use Visual Basic with ADSI to determine if an account is locked out.</span></span>


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



<span data-ttu-id="26963-118">В следующем примере кода показано, как использовать C++ с ADSI, чтобы определить, заблокирована ли учетная запись.</span><span class="sxs-lookup"><span data-stu-id="26963-118">The following code example demonstrates how to use C++ with ADSI to determine if an account is locked out.</span></span>


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 