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
# <a name="creating-an-authorization-policy-store-object-in-c"></a>Создание объекта хранилища политики авторизации в C++

Хранилище политик авторизации содержит сведения о политике безопасности приложения или группы приложений. Эти сведения включают в себя приложения, операции, задачи, пользователей и группы пользователей, связанных с магазином. При инициализации приложения, использующего Диспетчер авторизации, оно загружает эту информацию из хранилища. Хранилище политик авторизации должно находиться в доверенной системе, так как администраторы этой системы имеют высокий уровень доступа к хранилищу.

Диспетчер авторизации поддерживает хранение политики авторизации либо в службе каталогов Active Directory, либо в XML-файле, как показано в следующих примерах. В API диспетчера авторизации хранилище политик авторизации представлено объектом [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . В примерах показано, как создать объект **азаусоризатионсторе** для хранилища Active Directory и XML-хранилища.

-   [Создание хранилища Active Directory](#creating-an-active-directory-store)
-   [Создание хранилища SQL Server](#creating-a-sql-server-store)
-   [Создание хранилища XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Создание хранилища Active Directory

Чтобы использовать Active Directory для хранения политики авторизации, домен должен находиться на функциональном уровне домена **Windows Server 2003** . Хранилище политик авторизации не может располагаться в **контексте именования, не являющегося доменом** (также называемого секцией приложения). Рекомендуется размещать хранилище в контейнере **данных программы** в новом подразделении, созданном специально для хранилища политик авторизации. Также рекомендуется, чтобы хранилище размещалось в той же локальной сети, что и серверы приложений, использующие хранилище.

В следующем примере показано, как создать объект [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , представляющий хранилище политик авторизации в Active Directory. В этом примере предполагается, что существует Active Directory подразделение с именем Program Data в домене с именем authmanager.com.


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



## <a name="creating-a-sql-server-store"></a>Создание хранилища SQL Server

Диспетчер авторизации поддерживает создание хранилища политик авторизации на основе Microsoft SQL Server. Чтобы создать хранилище данных авторизации на основе SQL Server, используйте URL-адрес, который начинается с префикса **MSSQL://**. URL-адрес должен содержать допустимую строку подключения SQL, имя базы данных и имя хранилища политики авторизации: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _полицисторенаме_.

Если экземпляр SQL Server не содержит указанную базу данных диспетчера авторизации, диспетчер авторизации создает новую базу данных с таким именем.

> [!Note]  
> Подключения к хранилищу SQL Server не шифруются, если не задано явное шифрование SQL для подключения или не настроено шифрование сетевого трафика, использующего протокол IPsec.

 

В следующем примере показано, как создать объект [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , представляющий хранилище политик авторизации в базе данных SQL Server.


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



## <a name="creating-an-xml-store"></a>Создание хранилища XML

Диспетчер авторизации поддерживает создание хранилища политик авторизации в формате XML. Хранилище XML может располагаться на том же компьютере, где выполняется приложение, или его можно сохранить удаленно. Непосредственное изменение XML-файла не поддерживается. Чтобы изменить хранилище политик, используйте оснастку MMC диспетчера авторизации или API диспетчера авторизации.

Диспетчер авторизации не поддерживает делегирование администрирования хранилища политик XML. Сведения о делегировании см. [в разделе Делегирование определения разрешений в C++](delegating-the-defining-of-permissions-in-c--.md).

В следующем примере показано, как создать объект [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , представляющий хранилище политики авторизации в XML-файле.


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



 

 



