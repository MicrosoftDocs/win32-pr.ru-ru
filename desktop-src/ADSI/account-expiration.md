---
title: Истечение срока действия учетной записи (поставщик LDAP)
description: Чтобы задать дату окончания срока действия учетной записи, задайте для свойства IADsUser. Аккаунтекспиратиондате требуемое значение даты.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- Интерфейсы ADSI для истечения срока действия учетной записи, поставщик LDAP
- Поставщики LDAP ADSI, примеры управления пользователями, истечение срока действия учетной записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03ea33d8d5abb219c2b562aa05058b5dec45919
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654353"
---
# <a name="account-expiration-ldap-provider"></a><span data-ttu-id="1bc14-105">Истечение срока действия учетной записи (поставщик LDAP)</span><span class="sxs-lookup"><span data-stu-id="1bc14-105">Account Expiration (LDAP Provider)</span></span>

<span data-ttu-id="1bc14-106">Чтобы задать дату окончания срока действия учетной записи, задайте для свойства [**IADsUser. аккаунтекспиратиондате**](iadsuser-property-methods.md) требуемое значение даты.</span><span class="sxs-lookup"><span data-stu-id="1bc14-106">To set the account expiration date, set the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property to the desired date value.</span></span> <span data-ttu-id="1bc14-107">Чтобы отключить дату истечения срока действия учетной записи, установите для атрибута [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) значение 0.</span><span class="sxs-lookup"><span data-stu-id="1bc14-107">To disable the account expiration date, set the [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) attribute to zero.</span></span> <span data-ttu-id="1bc14-108">В следующих примерах кода показано, как задать дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="1bc14-108">The following code examples show how to set the expiration date.</span></span>


```VB
Public Sub SetUserAccountExpirationDate(User As IADsUser, ExpirationDate As Date)
    If 0 = ExpirationDate Then
        ' Disable the account expiration date.
        User.Put "accountExpires", 0
    Else
        ' Set the new account expiration date.
        User.AccountExpirationDate = ExpirationDate
    End If
    
    User.SetInfo
 
End Sub
```




```C++
/***************************************************************************

    SetUserAccountExpirationDate()

***************************************************************************/

HRESULT SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
    if(!pUser) 
    {
        return E_INVALIDARG;
    }

    HRESULT hr;

    if(!date || date < 0) 
    {
        // Account never expires. Set the accountExpires attribute to zero.
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        
        hr = pUser->Put(CComBSTR("accountExpires"), var); 

        VariantClear(&var);
    }
    else 
    {
        // Account expires on date.
        hr = pUser->put_AccountExpirationDate(date); 
    }

    if(S_OK == hr)
    {
        hr = pUser->SetInfo();
    }

    return hr;
}
```



> [!Note]  
> <span data-ttu-id="1bc14-109">Атрибут [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) содержит дату окончания срока действия учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1bc14-109">The [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) attribute contains the account expire date.</span></span> <span data-ttu-id="1bc14-110">В оснастке MMC "Active Directory пользователи и компьютеры" отображается дата истечения срока действия учетной записи в конце.</span><span class="sxs-lookup"><span data-stu-id="1bc14-110">The Active Directory Users and Computers MMC snap-in displays the date that the account will expire at the end of.</span></span> <span data-ttu-id="1bc14-111">То есть оснастка консоли управления Active Directory "пользователи и компьютеры" отобразит дату истечения срока действия учетной записи как один день раньше даты, содержащейся в атрибуте **accountExpires** .</span><span class="sxs-lookup"><span data-stu-id="1bc14-111">That is, the Active Directory Users and Computers MMC snap-in will display the account expiration date as one day earlier than the date contained in the **accountExpires** attribute.</span></span>

 

 

 