---
description: Хранилища политик авторизации, хранящиеся в Active Directory, поддерживают делегирование администрирования.
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: Делегирование определения разрешений в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc299e3506300da1f0db2b4a9bacfce60def1c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651011"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a>Делегирование определения разрешений в C++

Хранилища политик авторизации, хранящиеся в Active Directory, поддерживают делегирование администрирования. Администрирование может быть делегировано пользователям и группам на уровне хранилища, приложения или области.

На каждом уровне имеется список администраторов и читателей. Администраторы хранилища, приложения или области могут читать и изменять хранилище политик на делегированном уровне. Читатели могут читать хранилище политик на делегированном уровне, но не изменять хранилище.

Пользователь или группа, которые являются либо администратором, либо средством чтения приложения, также должны быть добавлены в качестве делегированного пользователя хранилища политик, содержащего это приложение. Аналогичным образом пользователь или группа, являющиеся администратором или читательом области, должны быть добавлены в качестве делегированного пользователя приложения, содержащего эту область.

Например, чтобы делегировать администрирование области, сначала добавьте пользователя или группу в список делегированных пользователей хранилища, содержащего область, вызвав метод [**иазаусоризатионсторе:: аддделегатедполициусер**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) . Затем добавьте пользователя или группу в список делегированных пользователей приложения, содержащего область, вызвав метод [**иазаппликатион:: аддделегатедполициусер**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) . Наконец, добавьте пользователя или группу в список администраторов области, вызвав метод [**иазскопе:: аддполициадминистратор**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) .

Хранилища политик на основе XML не поддерживают делегирование на любом уровне.

Область в хранилище данных авторизации, которая хранится в Active Directory, не может быть делегирована, если область содержит определения задач, включающие правила авторизации или определения ролей, включающие правила авторизации.

В следующем примере показано, как делегировать администрирование приложения. В этом примере предполагается, что в указанном расположении имеется хранилище политик авторизации Active Directory, которое содержит приложение с именем "расходы" и не содержит задач с сценариями бизнес-правил.


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR userName = NULL;
    VARIANT myVar;
    
    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create null VARIANT for parameters.
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize
   (AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Add a delegated policy user to the store.
    if (!(userName = SysAllocString(L"ExampleDomain\\UserName")))
        MyHandleError("Could not allocate username string.");
    hr = pStore->AddDelegatedPolicyUserName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to store as delegated policy user.");

    //  Add the user as an administrator of the application.
    hr = pApp->AddPolicyAdministratorName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to application as administrator.");

    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(userName);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



