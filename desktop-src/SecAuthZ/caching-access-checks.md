---
description: Когда приложение выполняет проверку доступа путем вызова функции Аусзакцессчекк, результаты проверки доступа могут быть кэшированы.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Проверки доступа кэширования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967e0a5398d93c1715d7d08e5c7c75695e4120ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350585"
---
# <a name="caching-access-checks"></a><span data-ttu-id="1f4fc-103">Проверки доступа кэширования</span><span class="sxs-lookup"><span data-stu-id="1f4fc-103">Caching Access Checks</span></span>

<span data-ttu-id="1f4fc-104">Когда приложение выполняет проверку доступа путем вызова функции [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , результаты проверки доступа могут быть кэшированы.</span><span class="sxs-lookup"><span data-stu-id="1f4fc-104">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span> <span data-ttu-id="1f4fc-105">Если параметр *паусзандле* функции [**Аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) не равен **null**, функция выполняет отдельную проверку доступа с запрошенной [**\_ маской доступа**](access-mask.md) **максимально \_ допустимой** и кэширует результаты этой проверки.</span><span class="sxs-lookup"><span data-stu-id="1f4fc-105">When the *pAuthzHandle* parameter of the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function is not **NULL**, the function performs a separate access check, with a requested [**ACCESS\_MASK**](access-mask.md) of **MAXIMUM\_ALLOWED**, and caches the results of that check.</span></span> <span data-ttu-id="1f4fc-106">Затем можно передать результат проверки в качестве параметра *аусзандле* в функцию [**аусзкачедакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="1f4fc-106">A handle to the results of that check can then be passed as the *AuthzHandle* parameter to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="1f4fc-107">Это обеспечивает более быструю проверку доступа для заданных клиентов и [*дескрипторов безопасности*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="1f4fc-107">This allows faster access checking for a given client and [*security descriptors*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="1f4fc-108">Можно кэшировать только статическую часть проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="1f4fc-108">Only the static portion of an access check can be cached.</span></span> <span data-ttu-id="1f4fc-109">Все [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) или ACE, содержащие идентификаторы **безопасности \_ основного участника** , должны оцениваться для каждой проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="1f4fc-109">Any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) or ACEs that contain the **PRINCIPAL\_SELF** SID must be evaluated for each access check.</span></span>

<span data-ttu-id="1f4fc-110">Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.</span><span class="sxs-lookup"><span data-stu-id="1f4fc-110">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="1f4fc-111">Пример</span><span class="sxs-lookup"><span data-stu-id="1f4fc-111">Example</span></span>

<span data-ttu-id="1f4fc-112">В следующем примере проверяется доступ к кэшированному результату из предыдущей проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="1f4fc-112">The following example checks access against a cached result from a previous access check.</span></span> <span data-ttu-id="1f4fc-113">Предыдущая проверка доступа была выполнена в примере [проверки доступа с помощью API authz](checking-access-with-authz-api.md).</span><span class="sxs-lookup"><span data-stu-id="1f4fc-113">The previous access check was performed in the example in [Checking Access with Authz API](checking-access-with-authz-api.md).</span></span>


```C++
BOOL CheckCachedAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR                pSecurityDescriptor = NULL;
    ULONG                                cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST                Request;
    CHAR                                ReplyBuffer[MY_MAX];
    CHAR                                CachedReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY                    pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    PAUTHZ_ACCESS_REPLY                    pCachedReply = (PAUTHZ_ACCESS_REPLY)CachedReplyBuffer;
    DWORD                                AuthzError =0;
    AUTHZ_ACCESS_CHECK_RESULTS_HANDLE    hCached;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the initial access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Allocate memory for the cached access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the cached access reply structure.
    pCachedReply->ResultListLength = 1;
    pCachedReply->Error = (PDWORD) ((PCHAR) pCachedReply + sizeof(AUTHZ_ACCESS_REPLY));
    pCachedReply->GrantedAccessMask = (PACCESS_MASK) (pCachedReply->Error + pCachedReply->ResultListLength);
    pCachedReply->SaclEvaluationResults = NULL;

    //Create security descriptor.
    if(!ConvertStringSecurityDescriptorToSecurityDescriptor(
        L"O:LAG:BAD:(A;;RC;;;BA)",
        SDDL_REVISION_1,
        &pSecurityDescriptor,
        NULL))
    {
        printf_s("ConvertStringSecurityDescriptorToSecurityDescriptor failed with %d\n", GetLastError()); 
        return FALSE;
    }

    //Call AuthzAccessCheck and cache results.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        &hCached))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
        
        return FALSE;
    }

    //Call AuthzCachedAccessCheck with the cached result from the previous call.
    if(!AuthzCachedAccessCheck(
        0,
        hCached,
        &Request,
        NULL,
        pCachedReply))
    {
        printf_s("AuthzCachedAccessCheck failed with %d\n", GetLastError());
        
        LocalFree(pSecurityDescriptor);
    AuthzFreeHandle(hCached);
    
        return FALSE;
    }

    //Print results.
    if(*pCachedReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }


  LocalFree(pSecurityDescriptor);
  AuthzFreeHandle(hCached);
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="1f4fc-114">См. также</span><span class="sxs-lookup"><span data-stu-id="1f4fc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f4fc-115">Добавление идентификаторов безопасности в контекст клиента</span><span class="sxs-lookup"><span data-stu-id="1f4fc-115">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="1f4fc-116">Проверка доступа с помощью API-интерфейса authz</span><span class="sxs-lookup"><span data-stu-id="1f4fc-116">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="1f4fc-117">Инициализация контекста клиента</span><span class="sxs-lookup"><span data-stu-id="1f4fc-117">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="1f4fc-118">Запрос контекста клиента</span><span class="sxs-lookup"><span data-stu-id="1f4fc-118">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
