---
title: Изменение пользователя не может изменить пароль (поставщик LDAP)
description: Возможность изменения собственного пароля пользователем — это разрешение, которое может быть предоставлено или запрещено.
ms.assetid: 9d5c2d6a-9997-4d0c-b896-bf1b578e64ac
ms.tgt_platform: multiple
keywords:
- Изменение пользователя не может изменить пароль (поставщик LDAP) ADSI
- Пользователь не может изменять пароль (поставщик LDAP) ADSI, изменение
- Поставщик LDAP ADSI, примеры управления пользователями, пользователь должен сменить пароль при следующем входе в систему, изменить
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec664f9a79e0de4ff0b75ae31abd8dc1532cd17c0d3d35a934e094da45eb3383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179022"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a>Изменение пользователя не может изменить пароль (поставщик LDAP)

Возможность изменения собственного пароля пользователем — это разрешение, которое может быть предоставлено или запрещено. Чтобы запретить это разрешение, установите два элемента ACE в списке управления доступом на уровне пользователей (DACL) для объекта пользователя с типом ACE **AD \_ ACETYPE \_ доступ \_ запрещенный \_ объект** . Одна запись ACE запрещает пользователю разрешение, а другая ACE запрещает разрешение для группы «все». Оба элемента ACE — это отклонения ACE для конкретного объекта, которые указывают идентификатор GUID расширенного разрешения на смену паролей. Чтобы предоставить это разрешение, задайте те же записи ACE с типом ACE **AD \_ ACETYPE \_ Access \_ Allowed \_ Object** .

В следующей процедуре описывается, как изменить или добавить ACE для этого разрешения.

**Изменение или добавление записей ACE для этого разрешения**

1.  Привязка к объекту пользователя.
2.  Получите объект [**иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) из свойства **нтсекуритидескриптор** объекта пользователя.
3.  Получите интерфейс [**иадсакцессконтроллист**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) для дескриптора безопасности из свойства [**иадссекуритидескриптор. дискретионарякл**](iadssecuritydescriptor-property-methods.md) .
4.  Перечислите записи ACE для объекта и выполните поиск записей ACE с изменением GUID пароля ({AB721A53-1E2F-11D0-9819-00AA0040529B}) для свойства [**иадсакцессконтролентри. ObjectType**](iadsaccesscontrolentry-property-methods.md) и "Everyone" или "NT Authority \\ Self" для свойства **иадсакцессконтролентри. опекун** .

    > [!Note]  
    > Строки "все" и "самоцентр NT \\ " локализуются на основе языка первого контроллера домена в домене. По этой причине строки не следует использовать напрямую. Имена учетных записей должны быть получены во время выполнения путем вызова функции [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) с идентификатором безопасности для хорошо известных субъектов безопасности ("s-1-1-0") и "NT Authority" \\ ("s-1-5-10"). Примеры функций **жетсидаккаунтнаме**, **Жетсидаккаунтнаме \_ Everyone** и **жетсидаккаунтнаме \_ Self** C++, показанные в статье [Чтение пользователя, не могут изменить пароль (поставщик LDAP)](reading-user-cannot-change-password-ldap-provider.md) демонстрируют, как это сделать.

     

5.  Измените свойство [**иадсакцессконтролентри. AceType**](iadsaccesscontrolentry-property-methods.md) записей ACE, найденных в **ADS \_ AceType \_ доступ \_ \_** , если пользователь не может изменить пароль или **рекламу \_ AceType \_ доступ к \_ разрешенному \_ объекту** , если пользователь может изменить свой пароль.
6.  Если элемент управления доступом "все" не найден, создайте новый объект [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , содержащий значения свойств, показанные в таблице ниже, и добавьте новую запись в список управления доступом с помощью метода [**иадсакцессконтроллист. аддаце**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .
7.  Если элемент управления доступом "самоцентр NT \\ " не найден, создайте новый объект [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) с теми же значениями свойств, приведенными в таблице ниже, за исключением того, что свойство " [**доверенное лицо**](iadsaccesscontrolentry-property-methods.md) " содержит имя учетной записи для SID "S-1-5-10" ("NT Authority \\ Self"). Добавьте запись в список управления доступом с помощью метода [**иадсакцессконтроллист. аддаце**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .
8.  Чтобы обновить свойство **нтсекуритидескриптор** объекта, вызовите метод [**iAds. разместил**](/windows/desktop/api/Iads/nf-iads-iads-put) с тем же [**Иадссекуритидескриптор**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) , полученным на шаге 2.
9.  Зафиксируйте локальные изменения на сервере с помощью метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .
10. Если был создан любой из записей ACE, необходимо переупорядочить список управления доступом, чтобы записи ACE находились в правильном порядке. Для этого вызовите функцию [**жетнамедсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) с параметром LDAP ADsPath объекта, а затем функцию [**сетнамедсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) с тем же списком DACL. Эта Переупорядочение выполняется автоматически при добавлении записей ACE.

В следующей таблице перечислены значения свойств объекта [**иадсакцессконтролентри**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .



| Иадсакцессконтролентри, свойство                                        | Значение                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](iadsaccesscontrolentry-property-methods.md)          | **AD \_ , \_ права \_ \_ доступа к управлению DS**                                                                                                                                   |
| [**AceType**](iadsaccesscontrolentry-property-methods.md)             | **Реклама \_ ACETYPE \_ отказ в доступе \_ \_** , если пользователь не может изменить пароль или **ADS \_ ACETYPE \_ доступ к \_ разрешенному \_ объекту** , если пользователь может изменить свой пароль. |
| [**AceFlags**](iadsaccesscontrolentry-property-methods.md)            | 0                                                                                                                                                                     |
| [**Метки**](iadsaccesscontrolentry-property-methods.md)               | **\_ \_ \_ имеется тип объекта флага ADS \_**                                                                                                                                  |
| [**ObjectType**](iadsaccesscontrolentry-property-methods.md)          | "{AB721A53-1E2F-11D0-9819-00AA0040529B}" — это идентификатор GUID изменения пароля в строковой форме.                                                                            |
| [**инхеритедобжекттипе**](iadsaccesscontrolentry-property-methods.md) | Не используется                                                                                                                                                              |
| [**Доверенное лицо**](iadsaccesscontrolentry-property-methods.md)             | Имя учетной записи для SID "S-1-1-0" (все).                                                                                                                            |



 

## <a name="example-code"></a>Пример кода

В следующем примере кода показано, как получить интерфейс для изменения списка DACL. Интерфейс [**иадсобжектоптионс**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) можно использовать, задав параметр **\_ \_ \_ DACL для сведений о безопасности в ADS** .

> [!Note]  
> Чтобы использовать код, описанный в этом примере, необходимо быть администратором. Если вы не являетесь администратором, вам потребуется добавить дополнительный код, который будет использовать интерфейс, позволяющий пользователю изменить способ сброса кэша на стороне клиента в службу домен Active Directory.

 


```C++
//
// Obtain an IADsObjectOptions interface from the object whose
// DACL you wish to modify.
//
long CanReadSetDACL = ADS_SECURITY_INFO_DACL;

CComPtr<IADsObjectOptions> spObjOps;

hr = pads->QueryInterface(IID_IADsObjectOptions, (void**)&spObjOps);

if(SUCCEEDED(hr))

{

//
// Set the option mask you want to change. In this case
// we want to change the objects security information, so we'll
// use the ADS_OPTION_SECURITY_MASK. Since we want to modify the 
// DACL, we'll set the variant to ADS_SEDCURITY_INFO_DACL flag. 
//

    CComVariant svar;
    svar = CanReadSetDACL;
    hr = spObjOps->SetOption(ADS_OPTION_SECURITY_MASK, svar); 

}
//
// The smart pointer declared for pObjOptions can be released
// or it will be destroyed and released once the pointer goes 
// out of scope.
//

```



В следующем примере кода показано, как изменить пользователь не может изменить пароль с помощью поставщика LDAP. В этом примере кода используется функция служебной программы **жетобжектаце** , определенная выше.

В этом примере используются примеры функций **жетсидаккаунтнаме \_ Everyone** и **жетсидаккаунтнаме \_ Self** C++, показанные в статье [Чтение пользователя не может изменить пароль (поставщик LDAP)](reading-user-cannot-change-password-ldap-provider.md).


```C++
#include <aclapi.h>

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    CreateACE()

    Creates an ACE and returns the IDispatch pointer for the ACE. This 
    pointer can be passed directly to IADsAccessControlList::AddAce.

    bstrTrustee - Contains the Trustee for the ACE.

    bstrObjectType - Contains the ObjectType for the ACE.

    lAccessMask - Contains the AccessMask for the ACE.

    lACEType - Contains the ACEType for the ACE.

    lACEFlags - Contains the ACEFlags for the ACE.

    lFlags - Contains the Flags for the ACE.

***************************************************************************/

IDispatch* CreateACE(BSTR bstrTrustee, 
                     BSTR bstrObjectType, 
                     long lAccessMask, 
                     long lACEType, 
                     long lACEFlags, 
                     long lFlags)
{
    HRESULT hr;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE = NULL;

    hr = CoCreateInstance(CLSID_AccessControlEntry,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsAccessControlEntry,
                          (void**)&pACE);
    if(SUCCEEDED(hr)) 
    {
        hr = pACE->put_Trustee(bstrTrustee); 
        hr = pACE->put_ObjectType(bstrObjectType);
        hr = pACE->put_AccessMask(lAccessMask); 
        hr = pACE->put_AceType(lACEType);
        hr = pACE->put_AceFlags(lACEFlags);
        hr = pACE->put_Flags(lFlags);

        hr = pACE->QueryInterface(IID_IDispatch, (LPVOID*)&pDisp);

        pACE->Release();
    }

    return pDisp;
}

/***************************************************************************

    ReorderACEs()

    Causes the ACEs of an object DACL to be reordered properly. The ACEs are 
    automatically put in the proper order when they are added to the DACL. 
    On older systems however, this does not occur automatically, so this 
    function is necessary so the deny ACEs are ordered in the list before 
    the allow ACEs.

    pwszDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the DS object to reorder the DACL for.

***************************************************************************/

HRESULT ReorderACEs(LPCWSTR pwszDN)
{
    HRESULT hr = E_FAIL;
    DWORD dwResult;
    ACL *pdacl;
    PSECURITY_DESCRIPTOR psd;
    
    dwResult = GetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                        SE_DS_OBJECT_ALL,
                                        DACL_SECURITY_INFORMATION,
                                        NULL,
                                        NULL,
                                        &pdacl,
                                        NULL,
                                        &psd);

    if(ERROR_SUCCESS == dwResult)
    {
        dwResult = SetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                            SE_DS_OBJECT_ALL,
                                            DACL_SECURITY_INFORMATION,
                                            NULL,
                                            NULL,
                                            pdacl,
                                            NULL);

        LocalFree(psd);
        
        if(ERROR_SUCCESS == dwResult)
        {
            hr = S_OK;
        }
    }
    
    return hr;
}

/***************************************************************************

    SetUserCannotChangePassword()

    Sets the "User Cannot Change Password" permission using the LDAP provider 
    to the specified setting. To do this, find the existing 
    ACEs and modify the AceType. If the ACE is not found, a new one of the 
    proper type is created and added. The ACEs should always be present, but 
    it is possible that the default DACL excludes them, so this situation 
    will be handled correctly.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to modify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    fCannotChangePassword - Contains the new setting for the privilege. 
    Contains nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT SetUserCannotChangePassword(LPCWSTR pwszUserDN, 
                                    LPCWSTR pwszUsername, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    HRESULT hr;

    CComBSTR sbstrEveryone;
    hr = GetSidAccountName_Everyone(&sbstrEveryone);
    if(FAILED(hr))
    {
        return hr;
    }

    CComBSTR sbstrSelf;
    hr = GetSidAccountName_Self(&sbstrSelf);
    if(FAILED(hr))
    {
        return hr;
    }

    if(NULL == pwszUserDN)
    {
        return E_INVALIDARG;
    }
    
    IADs *pads;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrSecDesc = "ntSecurityDescriptor";
        CComVariant svar;
        
        hr = pads->Get(sbstrSecDesc, &svar);
        if(SUCCEEDED(hr))
        {
            IADsSecurityDescriptor *psd;

            hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (LPVOID*)&psd);
            if(SUCCEEDED(hr))
            {
                IDispatch *pDisp;

                hr = psd->get_DiscretionaryAcl(&pDisp);
                if(SUCCEEDED(hr))
                {
                    IADsAccessControlList *pACL;

                    hr = pDisp->QueryInterface(IID_IADsAccessControlList, (void**)&pACL);
                    if(SUCCEEDED(hr)) 
                    {
                        BOOL fMustReorder = FALSE;
                        /*
                        Get the existing ACE for the change password permission 
                        for Everyone. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        if(pACEEveryone)
                        {
                            hr = pACEEveryone->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);

                            pACEEveryone->Release();
                        }
                        else
                        {
                            IDispatch *pDispEveryone = NULL;
                            
                            pDispEveryone = CreateACE(sbstrEveryone, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);
                            
                            if(pDispEveryone)
                            {
                                //add the new ACE for everyone
                                hr = pACL->AddAce(pDispEveryone);

                                pDispEveryone->Release();

                                fMustReorder = TRUE;
                            }                            
                        }
                        
                        /*
                        Get the existing ACE for the change password permission 
                        for Self. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACESelf = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        if(pACESelf)
                        {
                            hr = pACESelf->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
                        
                            pACESelf->Release();
                        }
                        else
                        {
                            IDispatch *pDispSelf = NULL;
                            
                            pDispSelf = CreateACE(sbstrSelf, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);

                            if(pDispSelf)
                            {
                                //add the new ACE for self
                                hr = pACL->AddAce(pDispSelf);

                                pDispSelf->Release();

                                fMustReorder = TRUE;
                            }                            
                        }

                        //update the security descriptor property
                        hr = pads->Put(sbstrSecDesc, svar);
                        
                        //commit the changes
                        hr = pads->SetInfo();

                        if(fMustReorder)
                        {
                            ReorderACEs(pwszUserDN);
                        }

                        pACL->Release();
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
    }

    return hr;
}
```



В следующем примере кода показано, как изменить пользователь не может изменить пароль с помощью поставщика LDAP.

> [!Note]  
> Приведенный ниже пример будет работать только с доменами, на которых первичным языком является английский, так как строки "все" и "самоцентр NT \\ " локализуются на основе языка первого контроллера домена в домене. не существует способа Visual Basic получить имена учетных записей для хорошо известного субъекта безопасности, не вызывая функцию [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) . при использовании Visual Basic рекомендуется использовать поставщика WinNT для изменения пользователя, не изменяющего разрешения на смену пароля, как показано в подокне [изменение пользователя не может изменить пароль (поставщик WinNT)](modifying-user-cannot-change-password-winnt-provider.md).

 


```VB
'******************************************************************************
'
'    SetUserCannotChangePassword
'
'    Sets the "User Cannot Change Password" permission using the LDAP provider
'    to the specified setting. This is accomplished by finding the existing
'    ACEs and modifying the AceType. The ACEs should always be present, but
'    it is possible that the default DACL excludes them. This function will not
'    work correctly if both ACEs are not present.
'
'    strUserDN - A string that contains the LDAP ADsPath of the user object to
'    modify.
'
'    strUsername - A string that contains the user name to use for
'    authorization. If this is an empty string, the credentials of the current
'    user are used.
'
'    strPassword - A string that contains the password to use for authorization.
'    This is ignored if strUsername is empty.
'
'    fCannotChangePassword - Contains the new setting for the privilege.
'    Contains True if the user cannot change their password or False if
'    the can change their password.
'
'******************************************************************************
Sub SetUserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String, fUserCannotChangePassword As Boolean)
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    
    fEveryone = False
    fSelf = False
    
    If "" <> strUsername Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oUser = dso.OpenDSObject(strUserDN, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strUserDN)
    End If
    
    Set oSecDesc = oUser.Get("ntSecurityDescriptor")
    Set oACL = oSecDesc.DiscretionaryAcl
    
    ' Modify the existing entries.
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        End If
    Next
    
    ' Update the ntSecurityDescriptor property.
    oUser.Put "ntSecurityDescriptor", oSecDesc
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



 

 