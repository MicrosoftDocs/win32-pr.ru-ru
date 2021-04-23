---
description: Хранилище политик авторизации содержит сведения о политике безопасности приложения или группы приложений. Эти сведения включают в себя приложения, операции, задачи, пользователей и группы пользователей, связанных с магазином.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Создание объекта хранилища политики авторизации в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b50bfa4234f5adaf162b1499f85785a7d65f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991402"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a><span data-ttu-id="7986b-104">Создание объекта хранилища политики авторизации в C++</span><span class="sxs-lookup"><span data-stu-id="7986b-104">Creating an Authorization Policy Store Object in C++</span></span>

<span data-ttu-id="7986b-105">Хранилище политик авторизации содержит сведения о политике безопасности приложения или группы приложений.</span><span class="sxs-lookup"><span data-stu-id="7986b-105">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="7986b-106">Эти сведения включают в себя приложения, операции, задачи, пользователей и группы пользователей, связанных с магазином.</span><span class="sxs-lookup"><span data-stu-id="7986b-106">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="7986b-107">При инициализации приложения, использующего Диспетчер авторизации, оно загружает эту информацию из хранилища.</span><span class="sxs-lookup"><span data-stu-id="7986b-107">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="7986b-108">Хранилище политик авторизации должно находиться в доверенной системе, так как администраторы этой системы имеют высокий уровень доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="7986b-108">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="7986b-109">Диспетчер авторизации поддерживает хранение политики авторизации либо в службе каталогов Active Directory, либо в XML-файле, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="7986b-109">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="7986b-110">В API диспетчера авторизации хранилище политик авторизации представлено объектом [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="7986b-110">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="7986b-111">В примерах показано, как создать объект **азаусоризатионсторе** для хранилища Active Directory и XML-хранилища.</span><span class="sxs-lookup"><span data-stu-id="7986b-111">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="7986b-112">Создание хранилища Active Directory</span><span class="sxs-lookup"><span data-stu-id="7986b-112">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="7986b-113">Создание хранилища SQL Server</span><span class="sxs-lookup"><span data-stu-id="7986b-113">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="7986b-114">Создание хранилища XML</span><span class="sxs-lookup"><span data-stu-id="7986b-114">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="7986b-115">Создание хранилища Active Directory</span><span class="sxs-lookup"><span data-stu-id="7986b-115">Creating an Active Directory Store</span></span>

<span data-ttu-id="7986b-116">Чтобы использовать Active Directory для хранения политики авторизации, домен должен находиться на функциональном уровне домена **Windows Server 2003** .</span><span class="sxs-lookup"><span data-stu-id="7986b-116">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="7986b-117">Хранилище политик авторизации не может располагаться в **контексте именования, не являющегося доменом** (также называемого секцией приложения).</span><span class="sxs-lookup"><span data-stu-id="7986b-117">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="7986b-118">Рекомендуется размещать хранилище в контейнере **данных программы** в новом подразделении, созданном специально для хранилища политик авторизации.</span><span class="sxs-lookup"><span data-stu-id="7986b-118">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="7986b-119">Также рекомендуется, чтобы хранилище размещалось в той же локальной сети, что и серверы приложений, использующие хранилище.</span><span class="sxs-lookup"><span data-stu-id="7986b-119">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="7986b-120">В следующем примере показано, как создать объект [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , представляющий хранилище политик авторизации в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7986b-120">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="7986b-121">В этом примере предполагается, что существует Active Directory подразделение с именем Program Data в домене с именем authmanager.com.</span><span class="sxs-lookup"><span data-stu-id="7986b-121">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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
    
    //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in Active Directory. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    VariantClear(&myVar);
    SysFreeString(storeName);
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



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="7986b-122">Создание хранилища SQL Server</span><span class="sxs-lookup"><span data-stu-id="7986b-122">Creating a SQL Server Store</span></span>

<span data-ttu-id="7986b-123">Диспетчер авторизации поддерживает создание хранилища политик авторизации на основе Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7986b-123">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="7986b-124">Чтобы создать хранилище данных авторизации на основе SQL Server, используйте URL-адрес, который начинается с префикса **MSSQL://**.</span><span class="sxs-lookup"><span data-stu-id="7986b-124">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="7986b-125">URL-адрес должен содержать допустимую строку подключения SQL, имя базы данных и имя хранилища политики авторизации: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _полицисторенаме_.</span><span class="sxs-lookup"><span data-stu-id="7986b-125">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="7986b-126">Если экземпляр SQL Server не содержит указанную базу данных диспетчера авторизации, диспетчер авторизации создает новую базу данных с таким именем.</span><span class="sxs-lookup"><span data-stu-id="7986b-126">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="7986b-127">Подключения к хранилищу SQL Server не шифруются, если не задано явное шифрование SQL для подключения или не настроено шифрование сетевого трафика, использующего протокол IPsec.</span><span class="sxs-lookup"><span data-stu-id="7986b-127">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="7986b-128">В следующем примере показано, как создать объект [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , представляющий хранилище политик авторизации в базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7986b-128">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the SQL Server store.
    if(!(storeName = SysAllocString
   (L"MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



## <a name="creating-an-xml-store"></a><span data-ttu-id="7986b-129">Создание хранилища XML</span><span class="sxs-lookup"><span data-stu-id="7986b-129">Creating an XML Store</span></span>

<span data-ttu-id="7986b-130">Диспетчер авторизации поддерживает создание хранилища политик авторизации в формате XML.</span><span class="sxs-lookup"><span data-stu-id="7986b-130">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="7986b-131">Хранилище XML может располагаться на том же компьютере, где выполняется приложение, или его можно сохранить удаленно.</span><span class="sxs-lookup"><span data-stu-id="7986b-131">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="7986b-132">Непосредственное изменение XML-файла не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7986b-132">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="7986b-133">Чтобы изменить хранилище политик, используйте оснастку MMC диспетчера авторизации или API диспетчера авторизации.</span><span class="sxs-lookup"><span data-stu-id="7986b-133">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="7986b-134">Диспетчер авторизации не поддерживает делегирование администрирования хранилища политик XML.</span><span class="sxs-lookup"><span data-stu-id="7986b-134">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="7986b-135">Сведения о делегировании см. [в разделе Делегирование определения разрешений в C++](delegating-the-defining-of-permissions-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="7986b-135">For information about delegation, see [Delegating the Defining of Permissions in C++](delegating-the-defining-of-permissions-in-c--.md).</span></span>

<span data-ttu-id="7986b-136">В следующем примере показано, как создать объект [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , представляющий хранилище политики авторизации в XML-файле.</span><span class="sxs-lookup"><span data-stu-id="7986b-136">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the XML store.
    if(!(storeName = SysAllocString(L"msxml://C:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in an XML file. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



 

 



