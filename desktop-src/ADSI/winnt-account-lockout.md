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
# <a name="account-lockout-winnt-provider"></a>Блокировка учетной записи (поставщик WinNT)

При превышении числа неудачных попыток входа учетная запись пользователя блокируется на количество минут, заданное атрибутом [**локкаутдуратион**](/windows/desktop/ADSchema/a-lockoutduration) . Свойство [**IADsUser. исаккаунтлоккед**](iadsuser-property-methods.md) является свойством, используемым для чтения и изменения состояния блокировки учетной записи пользователя, но у поставщика WinNT ADSI есть ограничения, ограничивающие использование свойства **исаккаунтлоккед** .

## <a name="resetting-the-account-lockout-status"></a>Сброс состояния блокировки учетной записи

При использовании поставщика WinNT свойству [**исаккаунтлоккед**](iadsuser-property-methods.md) может быть присвоено только **значение false**, которое разблокирует учетную запись. Попытка установить свойство **исаккаунтлоккед** в **значение true** завершится ошибкой. Только система может заблокировать учетную запись.

В следующем примере кода показано, как использовать Visual Basic с интерфейсом ADSI для разблокировки учетной записи пользователя.


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



В следующем примере кода показано, как использовать C++ с ADSI для разблокировки учетной записи пользователя.


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



## <a name="reading-the-account-lockout-status"></a>Чтение состояния блокировки учетной записи

С помощью поставщика WinNT можно использовать свойство [**исаккаунтлоккед**](iadsuser-property-methods.md) , чтобы определить, заблокирована ли учетная запись. Если учетная запись заблокирована, свойство **исаккаунтлоккед** будет содержать **значение true**. Если учетная запись не заблокирована, свойство **исаккаунтлоккед** будет содержать **значение false**.

В следующем примере кода показано, как использовать Visual Basic с интерфейсом ADSI, чтобы определить, заблокирована ли учетная запись.


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



В следующем примере кода показано, как использовать C++ с ADSI, чтобы определить, заблокирована ли учетная запись.


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



 

 