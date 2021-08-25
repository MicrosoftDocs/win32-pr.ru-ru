---
description: API диспетчера удостоверений позволяет создать одноранговый идентификатор для использования в одноранговой сети.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Создание удостоверения однорангового узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d7e2a1bfba386ede4bf3f10e8b009794c3e17676abc65d797d42e203f214f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887824"
---
# <a name="creating-a-peer-identity"></a>Создание удостоверения однорангового узла

API диспетчера удостоверений позволяет создать одноранговый идентификатор для использования в одноранговой сети.

При создании удостоверения однорангового узла можно указать следующие дополнительные сведения.

-   [Классификатор](peer-names.md)
-   Понятное имя
-   Поставщик служб шифрования

> [!Note]  
> Везде, где это возможно, повторно используйте одноранговый идентификатор.

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a>Пример создания и удаления однорангового удостоверения

В следующем фрагменте кода показано, как создать и удалить одноранговый идентификатор с помощью классификатора и понятного имени.


```C++
#define UNICODE
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: CreateIdentity
//
// Purpose:  Creates a new Identity.
//
// Returns:  HRESULT
//
HRESULT CreateIdentity(PWSTR pwzFriendlyName)
{
    HRESULT     hr              = S_OK;   
    PWSTR       pwzClassifier   = L"GroupMember";
    PWSTR       pwzIdentity     = NULL;

    hr = PeerIdentityCreate(pwzClassifier, pwzFriendlyName, 0, &pwzIdentity);
    if (FAILED(hr))
    {            
        printf("Failed to create identity.");
    }
    else
    {
        printf("Identity: %s", pwzFriendlyName);
    }
       
    PeerFreeData(pwzIdentity);    

    return hr;
}


//-----------------------------------------------------------------------------
// Function: DeleteIdentity
//
// Purpose:  Delete the identity created by CreateIdentity
//
// Returns:  HRESULT
//
HRESULT DeleteIdentity()
{
    HRESULT hr = S_OK;

    if (g_pwzIdentity)
    {
        hr = PeerIdentityDelete(g_pwzIdentity);
        g_pwzIdentity = NULL;
    }

    return hr;
}
```



 

 



