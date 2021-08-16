---
description: Хранилище политик авторизации содержит сведения о политике авторизации для одного или нескольких приложений. Для каждого приложения, использующего это хранилище политик, необходимо создать объект Иазаппликатион и сохранить его в хранилище политик.
ms.assetid: 2bba1068-ae03-4388-be4d-9865e42e440e
title: Создание объекта приложения на C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a434bb87d064a7fe19698e78565577238f75051fbf233e36ddf2da1725987c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782628"
---
# <a name="creating-an-application-object-in-c"></a>Создание объекта приложения на C++

Хранилище политик авторизации содержит сведения о политике авторизации для одного или нескольких приложений. Для каждого приложения, использующего это хранилище политик, необходимо создать объект [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) и сохранить его в хранилище политик.

В следующем примере показано, как создать объект [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) , представляющий приложение, и как добавить объект **иазаппликатион** в хранилище политик авторизации, используемое приложением. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C.


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
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;

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
    VARIANT myVar; 
    VariantInit(&myVar);

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the existing store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
         MyHandleError("Could not allocate application name string");
    hr = pStore->CreateApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application.");

    //  Save changes to the store.
    hr = pApp->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    VariantClear(&myVar);
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



 

 



