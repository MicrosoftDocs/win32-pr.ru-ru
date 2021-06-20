---
title: Чтение пользователя не может изменить пароль (поставщик WinNT)
description: Узнайте, как определить, имеет ли пользователь разрешение на изменение пароля для поставщика WinNT. Возможность пользователя изменять пароль может быть предоставлена или запрещена.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- Чтение пользователя не может изменить пароль (службы WinNT Provider) ADSI
- Пользователь не может изменить пароль (интерфейс WinNT Provider) ADSI, чтение
- WinNT Provider ADSI, примеры управления пользователями, пользователь не может изменить пароль, чтение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd075bfb6700779b60f9e578a4e89957487a2646
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405917"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="da8e9-107">Чтение пользователя не может изменить пароль (поставщик WinNT)</span><span class="sxs-lookup"><span data-stu-id="da8e9-107">Reading User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="da8e9-108">Возможность изменения собственного пароля пользователем — это разрешение, которое может быть предоставлено или запрещено.</span><span class="sxs-lookup"><span data-stu-id="da8e9-108">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="da8e9-109">Чтобы определить, предоставлено ли пользователю это разрешение у поставщика WinNT, прочтите **ADS \_ УФ PASSWD не \_ \_ удается \_ изменить** значение свойства **усерфлагс** объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="da8e9-109">To determine if the user has been granted this permission with the WinNT provider, read the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of the user object.</span></span> <span data-ttu-id="da8e9-110">Флаг **ADS \_ УФ \_ PASSWD не может \_ \_ измениться** в перечислении [**\_ \_ \_ enum флага пользователя ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) .</span><span class="sxs-lookup"><span data-stu-id="da8e9-110">The **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag is defined in the [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) enumeration.</span></span>

## <a name="example-code"></a><span data-ttu-id="da8e9-111">Пример кода</span><span class="sxs-lookup"><span data-stu-id="da8e9-111">Example Code</span></span>

<span data-ttu-id="da8e9-112">В следующем примере кода показано, как получить флаг **ADS \_ УФ \_ PASSWD \_ не \_ изменять** свойство **усерфлагс** объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="da8e9-112">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



<span data-ttu-id="da8e9-113">В следующем примере кода показано, как получить флаг **ADS \_ УФ \_ PASSWD \_ не \_ изменять** свойство **усерфлагс** объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="da8e9-113">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



 

 




