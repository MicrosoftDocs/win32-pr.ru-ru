---
description: Чтобы установить контекст клиента в C++, приложение может создать клиентский контекст с маркером, именем домена и пользователя или строковым представлением идентификатора безопасности клиента.
ms.assetid: 765cd702-a1a8-4ff6-bea5-54de9fb62c0b
title: Установка контекста клиента с помощью диспетчера авторизации в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79afa31db547b28d129c5b8e90dcf3e4ba1e91c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545874"
---
# <a name="establishing-a-client-context-with-authorization-manager-in-c"></a><span data-ttu-id="f755d-103">Установка контекста клиента с помощью диспетчера авторизации в C++</span><span class="sxs-lookup"><span data-stu-id="f755d-103">Establishing a Client Context with Authorization Manager in C++</span></span>

<span data-ttu-id="f755d-104">В диспетчере авторизации приложение определяет, получает ли клиент доступ к операции, вызывая метод [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , который представляет контекст клиента.</span><span class="sxs-lookup"><span data-stu-id="f755d-104">In Authorization Manager, an application determines whether a client is given access to an operation by calling the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object, which represents a client context.</span></span>

<span data-ttu-id="f755d-105">Приложение может создать клиентский контекст с маркером, именем домена и пользователя или строковым представлением [*идентификатора безопасности*](/windows/desktop/SecGloss/s-gly) (SID) клиента.</span><span class="sxs-lookup"><span data-stu-id="f755d-105">An application can create a client context with a handle to a token, a domain and user name, or a string representation of the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the client.</span></span>

<span data-ttu-id="f755d-106">Используйте методы [**инитиализеклиентконтекстфромтокен**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**инитиализеклиентконтекстфромнаме**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)и [**инитиализеклиентконтекстфромстрингсид**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) интерфейса [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) для создания контекста клиента.</span><span class="sxs-lookup"><span data-stu-id="f755d-106">Use the [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname), and [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) methods of the [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) interface to create a client context.</span></span>

<span data-ttu-id="f755d-107">В следующем примере показано, как создать объект [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) на основе маркера клиента.</span><span class="sxs-lookup"><span data-stu-id="f755d-107">The following example shows how to create an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object from a client token.</span></span> <span data-ttu-id="f755d-108">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C, что в этом хранилище содержится приложение с именем "расходы" и переменная Хтокен содержит допустимый маркер клиента.</span><span class="sxs-lookup"><span data-stu-id="f755d-108">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that the variable hToken contains a valid client token.</span></span>


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



 

 
