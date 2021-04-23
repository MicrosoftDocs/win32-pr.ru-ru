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
# <a name="detecting-the-schema-master"></a><span data-ttu-id="5ff26-104">Определение хозяина схемы</span><span class="sxs-lookup"><span data-stu-id="5ff26-104">Detecting the Schema Master</span></span>

<span data-ttu-id="5ff26-105">Службы домен Active Directory имеют систему обновления с несколькими хозяевами; Каждый контроллер домена содержит копию каталога, доступную для записи.</span><span class="sxs-lookup"><span data-stu-id="5ff26-105">Active Directory Domain Services have a multi-master update system; every domain controller holds a writable copy of the directory.</span></span> <span data-ttu-id="5ff26-106">Обновления схемы распространяются во все домены, принадлежащие к одному дереву или лесу.</span><span class="sxs-lookup"><span data-stu-id="5ff26-106">Schema updates are propagated to all domains that belong to the same tree or forest.</span></span> <span data-ttu-id="5ff26-107">Так как трудно выверять конфликтующие обновления схемы, обновления схемы могут выполняться только на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="5ff26-107">Because it is difficult to reconcile conflicting updates to the schema, schema updates can only be performed at a single server.</span></span> <span data-ttu-id="5ff26-108">Сервер, имеющий право на выполнение обновлений, может измениться, но только один сервер будет иметь это право в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="5ff26-108">The server with the right to perform updates can change, but only one server will have that right at any given time.</span></span> <span data-ttu-id="5ff26-109">Этот сервер называется хозяином схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-109">This server is called the schema master.</span></span> <span data-ttu-id="5ff26-110">Первый контроллер домена, установленный на предприятии, по умолчанию является хозяином схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-110">The first DC installed in an enterprise is, by default, the schema master.</span></span>

<span data-ttu-id="5ff26-111">Изменения схемы могут выполняться только на уровне хозяина схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-111">Schema changes can only be made at the schema master level.</span></span> <span data-ttu-id="5ff26-112">Чтобы определить, какой контроллер домена является хозяином схемы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5ff26-112">To detect which DC is the schema master, perform the following steps.</span></span>

<span data-ttu-id="5ff26-113">**Определение хозяина схемы контроллера домена**</span><span class="sxs-lookup"><span data-stu-id="5ff26-113">**Detecting the DC Schema Master**</span></span>

1.  <span data-ttu-id="5ff26-114">Прочтите атрибут **фсморолеовнер** контейнера schema на любом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="5ff26-114">Read the **fsmoRoleOwner** attribute of the schema container on any DC.</span></span> <span data-ttu-id="5ff26-115">Атрибут **фсморолеовнер** Возвращает различающееся имя (DN) объекта **нтдсдса** для хозяина схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-115">The **fsmoRoleOwner** attribute returns the distinguished name (DN) of the **nTDSDSA** object for the schema master.</span></span>
2.  <span data-ttu-id="5ff26-116">Выполните привязку к объекту **нтдсдса** , для которого только что ПОЛУЧЕНо различающееся имя.</span><span class="sxs-lookup"><span data-stu-id="5ff26-116">Bind to the **nTDSDSA** object whose DN you just retrieved.</span></span> <span data-ttu-id="5ff26-117">Родительским объектом этого объекта является серверный объект для контроллера домена, содержащего хозяин схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-117">The parent of this object is the server object for the DC containing the schema master.</span></span>
3.  <span data-ttu-id="5ff26-118">Получение ADsPath для родителя объекта **нтдсдса** .</span><span class="sxs-lookup"><span data-stu-id="5ff26-118">Get the ADsPath for the parent of the **nTDSDSA** object.</span></span> <span data-ttu-id="5ff26-119">Родительский объект является серверным объектом.</span><span class="sxs-lookup"><span data-stu-id="5ff26-119">The parent is a server object.</span></span>
4.  <span data-ttu-id="5ff26-120">Привязка к объекту сервера.</span><span class="sxs-lookup"><span data-stu-id="5ff26-120">Bind to the server object.</span></span>
5.  <span data-ttu-id="5ff26-121">Получите атрибут **dNSHostName** объекта Server.</span><span class="sxs-lookup"><span data-stu-id="5ff26-121">Get the **dNSHostName** attribute of the server object.</span></span> <span data-ttu-id="5ff26-122">Это DNS-имя контроллера домена, содержащего хозяин схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-122">This is the DNS name of the DC that contains the schema master.</span></span>
6.  <span data-ttu-id="5ff26-123">Укажите DNS-имя хозяина схемы в качестве сервера и DN в качестве РАЗЛИЧАЮЩЕГОСЯ имени контейнера схемы для привязки к хозяину схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-123">Specify the DNS name of the schema master as the server and the DN as the DN of the schema container to bind to the schema master.</span></span> <span data-ttu-id="5ff26-124">Например, если сервер был "dc1.fabrikam.com", а DN контейнера схемы имел значение "CN = Schema, CN = Configuration, DC = Fabrikam, DC = com", путь ADsPath будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="5ff26-124">For example, if the server was "dc1.fabrikam.com" and the schema container DN was "cn=schema,cn=configuration,dc=fabrikam,dc=com", the ADsPath would be as follows.</span></span>
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

<span data-ttu-id="5ff26-125">Рекомендуется найти хозяин схемы и выполнить привязку к нему, чтобы внести изменения в схему.</span><span class="sxs-lookup"><span data-stu-id="5ff26-125">It is recommended that you find the schema master and bind to it to make schema changes.</span></span> <span data-ttu-id="5ff26-126">Однако можно переместить хозяин схемы на другой сервер.</span><span class="sxs-lookup"><span data-stu-id="5ff26-126">However, you can move the schema master to another server.</span></span>

<span data-ttu-id="5ff26-127">Чтобы сделать другой сервер хозяином схемы, пользователь с соответствующим уровнем привилегий может:</span><span class="sxs-lookup"><span data-stu-id="5ff26-127">To make another server the schema master, a suitably privileged user can:</span></span>

-   <span data-ttu-id="5ff26-128">Используйте оснастку MMC диспетчера схем.</span><span class="sxs-lookup"><span data-stu-id="5ff26-128">Use the Schema Manager MMC snap-in.</span></span>
    > [!Note]
    > <span data-ttu-id="5ff26-129">Оснастку MMC для Active Directory схемы необходимо зарегистрировать вручную.</span><span class="sxs-lookup"><span data-stu-id="5ff26-129">The Active Directory Schema MMC snap-in must be registered manually.</span></span> <span data-ttu-id="5ff26-130">Чтобы зарегистрировать оснастку схемы, необходимо выполнить следующую команду из командной строки в каталоге Windows System32.</span><span class="sxs-lookup"><span data-stu-id="5ff26-130">To register the Schema snap-in, you must run the following command from the command prompt in the Windows System32 directory.</span></span>
    >
    > <span data-ttu-id="5ff26-131">**regsvr32.exe schmmgmt.dll**</span><span class="sxs-lookup"><span data-stu-id="5ff26-131">**regsvr32.exe schmmgmt.dll**</span></span>

     

-   <span data-ttu-id="5ff26-132">Используйте служебную программу командной строки NTDSUTIL.</span><span class="sxs-lookup"><span data-stu-id="5ff26-132">Use the NTDSUTIL command-line utility.</span></span>
-   <span data-ttu-id="5ff26-133">Используйте стороннее приложение (приложение, которое выдает соответствующую запись LDAP).</span><span class="sxs-lookup"><span data-stu-id="5ff26-133">Use a third-party application (an application that issues the appropriate LDAP write).</span></span>

<span data-ttu-id="5ff26-134">Чтобы стать хозяином схемы программным способом, приложение, выполняемое в контексте подходящим образом привилегированного пользователя, может выдать LDAP-запись атрибута эксплуатации **бекомесчемамастер** в RootDSE на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="5ff26-134">To become the schema master programmatically, an application running in the context of a suitably privileged user can issue an LDAP write of the operational attribute **becomeSchemaMaster** to the rootDSE on that DC.</span></span> <span data-ttu-id="5ff26-135">Это инициирует атомарную пересылку хозяина схемы непосредственно от текущего владельца к локальному контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="5ff26-135">This initiates an atomic transfer of the schema master right from the current holder to the local DC.</span></span>

<span data-ttu-id="5ff26-136">В следующем примере кода выполняется поиск хозяина схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-136">The following code example finds the schema master.</span></span> <span data-ttu-id="5ff26-137">Следующая функция выполняет привязку к контейнеру схемы на компьютере, который является хозяином схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-137">The following function binds to the schema container on the computer that is the schema master.</span></span>


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



<span data-ttu-id="5ff26-138">В следующем примере кода отображается DNS-имя для компьютера, который является хозяином схемы.</span><span class="sxs-lookup"><span data-stu-id="5ff26-138">The following code example displays the DNS name for the computer that is the schema master.</span></span>


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



 

 




