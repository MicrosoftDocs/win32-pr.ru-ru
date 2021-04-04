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
# <a name="creating-a-peer-identity"></a><span data-ttu-id="f2dc1-103">Создание удостоверения однорангового узла</span><span class="sxs-lookup"><span data-stu-id="f2dc1-103">Creating a Peer Identity</span></span>

<span data-ttu-id="f2dc1-104">API диспетчера удостоверений позволяет создать одноранговый идентификатор для использования в одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="f2dc1-104">The Identity Manager API allows you to create a peer identity to use in a peer network.</span></span>

<span data-ttu-id="f2dc1-105">При создании удостоверения однорангового узла можно указать следующие дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f2dc1-105">When you create a peer identity, you can provide the following optional information:</span></span>

-   [<span data-ttu-id="f2dc1-106">Классификатор</span><span class="sxs-lookup"><span data-stu-id="f2dc1-106">Classifier</span></span>](peer-names.md)
-   <span data-ttu-id="f2dc1-107">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="f2dc1-107">Friendly name</span></span>
-   <span data-ttu-id="f2dc1-108">Поставщик служб шифрования</span><span class="sxs-lookup"><span data-stu-id="f2dc1-108">Cryptographic service provider</span></span>

> [!Note]  
> <span data-ttu-id="f2dc1-109">Везде, где это возможно, повторно используйте одноранговый идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f2dc1-109">Whenever possible, re-use a peer identity.</span></span>

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a><span data-ttu-id="f2dc1-110">Пример создания и удаления однорангового удостоверения</span><span class="sxs-lookup"><span data-stu-id="f2dc1-110">Example of Creating and Deleting a Peer Identity</span></span>

<span data-ttu-id="f2dc1-111">В следующем фрагменте кода показано, как создать и удалить одноранговый идентификатор с помощью классификатора и понятного имени.</span><span class="sxs-lookup"><span data-stu-id="f2dc1-111">The following code snippet shows you how to create and delete a peer identity by using a classifier and friendly name.</span></span>


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



 

 



