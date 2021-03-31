---
title: Определение хозяина схемы
description: Службы домен Active Directory имеют систему обновления с несколькими хозяевами; Каждый контроллер домена содержит копию каталога, доступную для записи.
ms.assetid: 8e096351-43f8-48ee-acb6-681d9e38e93c
ms.tgt_platform: multiple
keywords:
- Определение хозяина схемы AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6869853cba68d7155f2091e2fe4515116944a629
ms.sourcegitcommit: f730b85cc85448913e50a7f331e10b646ea7978b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2019
ms.locfileid: "103889287"
---
# <a name="detecting-the-schema-master"></a>Определение хозяина схемы

Службы домен Active Directory имеют систему обновления с несколькими хозяевами; Каждый контроллер домена содержит копию каталога, доступную для записи. Обновления схемы распространяются во все домены, принадлежащие к одному дереву или лесу. Так как трудно выверять конфликтующие обновления схемы, обновления схемы могут выполняться только на одном сервере. Сервер, имеющий право на выполнение обновлений, может измениться, но только один сервер будет иметь это право в любое заданное время. Этот сервер называется хозяином схемы. Первый контроллер домена, установленный на предприятии, по умолчанию является хозяином схемы.

Изменения схемы могут выполняться только на уровне хозяина схемы. Чтобы определить, какой контроллер домена является хозяином схемы, выполните следующие действия.

**Определение хозяина схемы контроллера домена**

1.  Прочтите атрибут **фсморолеовнер** контейнера schema на любом контроллере домена. Атрибут **фсморолеовнер** Возвращает различающееся имя (DN) объекта **нтдсдса** для хозяина схемы.
2.  Выполните привязку к объекту **нтдсдса** , для которого только что ПОЛУЧЕНо различающееся имя. Родительским объектом этого объекта является серверный объект для контроллера домена, содержащего хозяин схемы.
3.  Получение ADsPath для родителя объекта **нтдсдса** . Родительский объект является серверным объектом.
4.  Привязка к объекту сервера.
5.  Получите атрибут **dNSHostName** объекта Server. Это DNS-имя контроллера домена, содержащего хозяин схемы.
6.  Укажите DNS-имя хозяина схемы в качестве сервера и DN в качестве РАЗЛИЧАЮЩЕГОСЯ имени контейнера схемы для привязки к хозяину схемы. Например, если сервер был "dc1.fabrikam.com", а DN контейнера схемы имел значение "CN = Schema, CN = Configuration, DC = Fabrikam, DC = com", путь ADsPath будет выглядеть следующим образом.
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

Рекомендуется найти хозяин схемы и выполнить привязку к нему, чтобы внести изменения в схему. Однако можно переместить хозяин схемы на другой сервер.

Чтобы сделать другой сервер хозяином схемы, пользователь с соответствующим уровнем привилегий может:

-   Используйте оснастку MMC диспетчера схем.
    > [!Note]
    > Оснастку MMC для Active Directory схемы необходимо зарегистрировать вручную. Чтобы зарегистрировать оснастку схемы, необходимо выполнить следующую команду из командной строки в каталоге Windows System32.
    >
    > **regsvr32.exe schmmgmt.dll**

     

-   Используйте служебную программу командной строки NTDSUTIL.
-   Используйте стороннее приложение (приложение, которое выдает соответствующую запись LDAP).

Чтобы стать хозяином схемы программным способом, приложение, выполняемое в контексте подходящим образом привилегированного пользователя, может выдать LDAP-запись атрибута эксплуатации **бекомесчемамастер** в RootDSE на этом контроллере домена. Это инициирует атомарную пересылку хозяина схемы непосредственно от текущего владельца к локальному контроллеру домена.

В следующем примере кода выполняется поиск хозяина схемы. Следующая функция выполняет привязку к контейнеру схемы на компьютере, который является хозяином схемы.


```C++
HRESULT BindToSchemaMaster(IADsContainer **ppSchemaMaster)
{
HRESULT hr = E_FAIL;
// Get rootDSE and the schema container DN.
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (hr == S_OK)
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (hr == S_OK)
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (hr == S_OK)
    {
      /*
      Read the fsmoRoleOwner attribute to identify which server is 
      the schema master.
      */  
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (hr == S_OK)
      {
        // The fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get parent.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)&pNTDS);
        if (hr == S_OK)
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (hr == S_OK)
          {
            /*
            Bind to server object and get the DNS name of 
            the server.
            */
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION,
               IID_IADs,
               (void**)&pServer);
            if (hr == S_OK)
            {
              // Get the dns name of the server.
              hr = pServer->Get(CComBSTR("dNSHostName"), 
                  &varComputer);
              if (hr == S_OK)
              {
                    wcscpy_s(szPath,L"LDAP://");
                    wcscat_s(szPath,varComputer.bstrVal);
                    wcscat_s(szPath,L"/");
                    wcscat_s(szPath,var.bstrVal);
                    hr = ADsOpenObject(szPath,
                         NULL,
                         NULL,
                         ADS_SECURE_AUTHENTICATION,
                         IID_IADs,
                         (void**)ppSchemaMaster);
                    if (FAILED(hr))
                    {
                      if (*ppSchemaMaster)
                      {
                        (*ppSchemaMaster)->Release();
                        (*ppSchemaMaster) = NULL;
                      }
                    }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



В следующем примере кода отображается DNS-имя для компьютера, который является хозяином схемы.


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
''''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the schema
''''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the schema container
''''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the 
' schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' The fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get the parent object.
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("dNSHostName")
''''''''''''''''''''
' Display the DNS name for the computer.
''''''''''''''''''''
strText = "Schema master has the following DNS name: "& sComputer
WScript.echo strText
 
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




