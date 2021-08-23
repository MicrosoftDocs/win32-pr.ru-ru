---
description: Чтобы установить контекст клиента в C++, приложение может создать клиентский контекст с маркером, именем домена и пользователя или строковым представлением идентификатора безопасности клиента.
ms.assetid: 765cd702-a1a8-4ff6-bea5-54de9fb62c0b
title: Установка контекста клиента с помощью диспетчера авторизации в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1b74cab7d6c113f5120a682250f85dca772e1764acf432317049da27ec091d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672124"
---
# <a name="establishing-a-client-context-with-authorization-manager-in-c"></a>Установка контекста клиента с помощью диспетчера авторизации в C++

В диспетчере авторизации приложение определяет, получает ли клиент доступ к операции, вызывая метод [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , который представляет контекст клиента.

Приложение может создать клиентский контекст с маркером, именем домена и пользователя или строковым представлением [*идентификатора безопасности*](/windows/desktop/SecGloss/s-gly) (SID) клиента.

Используйте методы [**инитиализеклиентконтекстфромтокен**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**инитиализеклиентконтекстфромнаме**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)и [**инитиализеклиентконтекстфромстрингсид**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) интерфейса [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) для создания контекста клиента.

В следующем примере показано, как создать объект [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) на основе маркера клиента. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C, что в этом хранилище содержится приложение с именем "расходы" и переменная Хтокен содержит допустимый маркер клиента.


```C++
#include <windows.h>

void ExpenseCheck(ULONGLONG hToken)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
 
 //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

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

    //  Allocate a string for the policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(0, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a client context from a token handle.
    hr = pApp->InitializeClientContextFromToken(hToken, myVar,
                &pClientContext);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create client context.");

    //  Use the client context as needed.

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pClientContext->Release();
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



 

 
