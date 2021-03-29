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
# <a name="account-expiration-ldap-provider"></a>Истечение срока действия учетной записи (поставщик LDAP)

Чтобы задать дату окончания срока действия учетной записи, задайте для свойства [**IADsUser. аккаунтекспиратиондате**](iadsuser-property-methods.md) требуемое значение даты. Чтобы отключить дату истечения срока действия учетной записи, установите для атрибута [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) значение 0. В следующих примерах кода показано, как задать дату окончания срока действия.


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
> Атрибут [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) содержит дату окончания срока действия учетной записи. В оснастке MMC "Active Directory пользователи и компьютеры" отображается дата истечения срока действия учетной записи в конце. То есть оснастка консоли управления Active Directory "пользователи и компьютеры" отобразит дату истечения срока действия учетной записи как один день раньше даты, содержащейся в атрибуте **accountExpires** .

 

 

 