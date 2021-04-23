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
# <a name="delegating-the-defining-of-permissions-in-c"></a><span data-ttu-id="3fe21-103">Делегирование определения разрешений в C++</span><span class="sxs-lookup"><span data-stu-id="3fe21-103">Delegating the Defining of Permissions in C++</span></span>

<span data-ttu-id="3fe21-104">Хранилища политик авторизации, хранящиеся в Active Directory, поддерживают делегирование администрирования.</span><span class="sxs-lookup"><span data-stu-id="3fe21-104">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="3fe21-105">Администрирование может быть делегировано пользователям и группам на уровне хранилища, приложения или области.</span><span class="sxs-lookup"><span data-stu-id="3fe21-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="3fe21-106">На каждом уровне имеется список администраторов и читателей.</span><span class="sxs-lookup"><span data-stu-id="3fe21-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="3fe21-107">Администраторы хранилища, приложения или области могут читать и изменять хранилище политик на делегированном уровне.</span><span class="sxs-lookup"><span data-stu-id="3fe21-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="3fe21-108">Читатели могут читать хранилище политик на делегированном уровне, но не изменять хранилище.</span><span class="sxs-lookup"><span data-stu-id="3fe21-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="3fe21-109">Пользователь или группа, которые являются либо администратором, либо средством чтения приложения, также должны быть добавлены в качестве делегированного пользователя хранилища политик, содержащего это приложение.</span><span class="sxs-lookup"><span data-stu-id="3fe21-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="3fe21-110">Аналогичным образом пользователь или группа, являющиеся администратором или читательом области, должны быть добавлены в качестве делегированного пользователя приложения, содержащего эту область.</span><span class="sxs-lookup"><span data-stu-id="3fe21-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="3fe21-111">Например, чтобы делегировать администрирование области, сначала добавьте пользователя или группу в список делегированных пользователей хранилища, содержащего область, вызвав метод [**иазаусоризатионсторе:: аддделегатедполициусер**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="3fe21-111">For example, to delegate administration of a scope, first add the user or group to the list of delegated users of the store that contains the scope by calling the [**IAzAuthorizationStore::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="3fe21-112">Затем добавьте пользователя или группу в список делегированных пользователей приложения, содержащего область, вызвав метод [**иазаппликатион:: аддделегатедполициусер**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="3fe21-112">Then add the user or group to the list of delegated users of the application that contains the scope by calling the [**IAzApplication::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="3fe21-113">Наконец, добавьте пользователя или группу в список администраторов области, вызвав метод [**иазскопе:: аддполициадминистратор**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) .</span><span class="sxs-lookup"><span data-stu-id="3fe21-113">Finally, add the user or group to the list of administrators of the scope by calling the [**IAzScope::AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method.</span></span>

<span data-ttu-id="3fe21-114">Хранилища политик на основе XML не поддерживают делегирование на любом уровне.</span><span class="sxs-lookup"><span data-stu-id="3fe21-114">XML-based policy stores do not support delegation at any level.</span></span>

<span data-ttu-id="3fe21-115">Область в хранилище данных авторизации, которая хранится в Active Directory, не может быть делегирована, если область содержит определения задач, включающие правила авторизации или определения ролей, включающие правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="3fe21-115">A scope within an authorization store that is stored in Active Directory cannot be delegated if the scope contains task definitions that include authorization rules or role definitions that include authorization rules.</span></span>

<span data-ttu-id="3fe21-116">В следующем примере показано, как делегировать администрирование приложения.</span><span class="sxs-lookup"><span data-stu-id="3fe21-116">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="3fe21-117">В этом примере предполагается, что в указанном расположении имеется хранилище политик авторизации Active Directory, которое содержит приложение с именем "расходы" и не содержит задач с сценариями бизнес-правил.</span><span class="sxs-lookup"><span data-stu-id="3fe21-117">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


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



 

 



