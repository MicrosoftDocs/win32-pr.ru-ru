---
title: Использование COM-интерфейса
description: Использование COM-интерфейса
ms.assetid: 44e1aeac-585c-4856-8c4d-1adb5b307b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ddf507be3a71d3b00f99574b2153dafd21a6558ee20fa5c3f2108675bf9b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308931"
---
# <a name="using-a-com-interface"></a>Использование COM-интерфейса

Клиентский код — это пользователь COM-интерфейса. Чтобы использовать любой COM-интерфейс, настраиваемый или стандартный, клиент должен иметь свой идентификатор IID. В следующем примере драйвер, вызывающий Кустомрпт, передает ему имя объекта, который преобразуется в формат расширенных символов. Имя объекта подается в [**креатефилемоникер**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) , чтобы можно было создать моникер файла, а клиент мог выполнить привязку к выполняющемуся объекту. После запуска объекта Кустомрпт может получить доступ к указателю на интерфейс в стандартном прокси-сервере или заглушке, например [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile), или в настраиваемый интерфейс икустоминтерфаце.


```C++
void CustomRpt(char *pszObject) 
{ 
    HRESULT             hr; 
    WCHAR               wszObject[128]; 
    WCHAR               wszMsg[128] = {L"Your Message Here...\n"}; 
    IMoniker            *pmkObject = NULL; 
    IUnknown            *pIUnk = NULL; 
    IPersistFile        *pIPersistFile = NULL; 
    ICustomInterface    *pICustomInterface = NULL; 
 
    // Create a wide-character version of the object's file name. 
    StringCchPrintf(wszObject, 128, L"%hs", pszObject); 
 
    // Get a file moniker for the object (a *.smp file). 
    hr = CreateFileMoniker(wszObject, &pmkObject); 
 
    if(FAILED(hr)) 
    { 
        printf("Client: CreateFileMoniker for Object failed"); 
        return; 
    } 
 
    // BindMoniker is equivalent to calling CreateBindCtx() followed by 
    // a call to BindToObject(). It has the net result of binding the 
    // interface (specified by the IID) to the moniker. 
 
    hr = BindMoniker(pmkObject, 0, IID_IUnknown, (void **)&pIUnk); 
    if (FAILED(hr)) 
    { 
        printf("Client: BindMoniker failed (%x)\n", hr); 
        return; 
    } 
 
    // Try a couple QueryInterface calls into the object code; first a 
    // QueryInterface to IPersistFile... 
 
    hr = pIUnk->QueryInterface(IID_IPersistFile, (void **)&pIPersistFile); 
 
    if (FAILED(hr)) { 
        printf("Client: QueryInterface IPersistFile failed (%x)\n", hr); 
        pIUnk->Release(); 
        return; 
    } 
 
    // Followed by a QueryInterface to ICustomInterface. 
    hr = pIUnk->QueryInterface(IID_ICustomInterface, (void **)&pICustomInterface); 
 
    if (FAILED(hr)) { 
        printf("Client: QueryInterface failed (%x)\n", hr); 
        pIUnk->Release(); 
        pIPersistFile->Release(); 
        return; 
    } 
 
    // CustomReport() is the object function that displays the time and 
    // date information on the object. 
    hr = pICustomInterface->CustomReport(); 
 
    if (FAILED(hr)) 
    { 
        printf("Client: pICustomInterface->CustomReport failed (%x)\n", hr); 
        pIUnk->Release(); 
        pIPersistFile->Release(); 
        return; 
    } 
 
    // Clean up resources by calling release on each of the interfaces. 
    pIPersistFile->Release(); 
    pICustomInterface->Release(); 
    pIUnk->Release(); 
    return; 
} 
```



 

 




