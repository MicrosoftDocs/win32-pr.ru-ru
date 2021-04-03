---
title: Чтение пользователя не может изменить пароль (поставщик WinNT)
description: Возможность изменения собственного пароля пользователем — это разрешение, которое может быть предоставлено или запрещено.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- Чтение пользователя не может изменить пароль (службы WinNT Provider) ADSI
- Пользователь не может изменить пароль (интерфейс WinNT Provider) ADSI, чтение
- WinNT Provider ADSI, примеры управления пользователями, пользователь не может изменить пароль, чтение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab257f620d3e103866639f8ecacb57cc924efec4
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/27/2020
ms.locfileid: "103987239"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>Чтение пользователя не может изменить пароль (поставщик WinNT)

Возможность изменения собственного пароля пользователем — это разрешение, которое может быть предоставлено или запрещено. Чтобы определить, предоставлено ли пользователю это разрешение у поставщика WinNT, прочтите **ADS \_ УФ PASSWD не \_ \_ удается \_ изменить** значение свойства **усерфлагс** объекта пользователя. Флаг **ADS \_ УФ \_ PASSWD не может \_ \_ измениться** в перечислении [**\_ \_ \_ enum флага пользователя ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) .

## <a name="example-code"></a>Пример кода

В следующем примере кода показано, как получить флаг **ADS \_ УФ \_ PASSWD \_ не \_ изменять** свойство **усерфлагс** объекта пользователя.


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Function UserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
    Dim oUser As IADs
    
    strPath = "WinNT://" + strDomain + "/" + strUser
    
    If "" <> strUserCred Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("WinNT:")
        Set oUser = dso.OpenDSObject(strPath, strUserCred, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strPath)
    End If
    
    If (oUser.Get("userFlags") And ADS_UF_PASSWD_CANT_CHANGE) <> 0 Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



В следующем примере кода показано, как получить флаг **ADS \_ УФ \_ PASSWD \_ не \_ изменять** свойство **усерфлагс** объекта пользователя.


```C++
//***************************************************************************
//
//  UserCannotChangePassword()
//
//***************************************************************************

HRESULT UserCannotChangePassword(LPCWSTR pwszDomain, 
                                 LPCWSTR pwszUser, 
                                 LPCWSTR pwszUserCred, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
{
    if(NULL == pwszDomain || NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
    *pfCannotChangePassword = FALSE;

    HRESULT hr;
    IADs *pads;

    CComBSTR sbstrADsPath = L"WinNT://";
    sbstrADsPath += pwszDomain;
    sbstrADsPath += "/";
    sbstrADsPath += pwszUser;

    hr = ADsOpenObject( sbstrADsPath,
                        pwszUserCred,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("userFlags"), &svar);
        if(SUCCEEDED(hr))
        {
            if(ADS_UF_PASSWD_CANT_CHANGE & svar.lVal)
            {
                *pfCannotChangePassword = TRUE;
            }
            else
            {
                *pfCannotChangePassword = FALSE;
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




