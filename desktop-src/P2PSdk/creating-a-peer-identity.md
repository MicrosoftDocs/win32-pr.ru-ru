---
description: API диспетчера удостоверений позволяет создать одноранговый идентификатор для использования в одноранговой сети.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Создание удостоверения однорангового узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab240b9fa1265ba03bfb1ce584dabed92988620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998549"
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



 

 



