---
description: Приложения определяют, предоставлять ли доступ к защищаемым объектам, вызывая функцию Аусзакцессчекк.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Проверка доступа с помощью API-интерфейса authz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e129b690a7c1f701b5f669a8f0705c5a5e9a2eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897618"
---
# <a name="checking-access-with-authz-api"></a><span data-ttu-id="3e330-103">Проверка доступа с помощью API-интерфейса authz</span><span class="sxs-lookup"><span data-stu-id="3e330-103">Checking Access with Authz API</span></span>

<span data-ttu-id="3e330-104">Приложения определяют, предоставлять ли доступ к защищаемым объектам, вызывая функцию [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="3e330-104">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

<span data-ttu-id="3e330-105">Функция [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) принимает в качестве параметров как [**\_ \_ запрос на доступ к авторизации**](/windows/desktop/api/Authz/ns-authz-authz_access_request) , так и структуру [**\_ дескрипторов безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="3e330-105">The [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function takes both [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) and [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structures as parameters.</span></span> <span data-ttu-id="3e330-106">Структура **\_ \_ запроса на авторизацию** задает запрошенный уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="3e330-106">The **AUTHZ\_ACCESS\_REQUEST** structure specifies a level of access requested.</span></span> <span data-ttu-id="3e330-107">Функция **аусзакцессчекк** вычисляет запрошенный доступ к указанному **\_ дескриптору безопасности** для указанного контекста клиента.</span><span class="sxs-lookup"><span data-stu-id="3e330-107">The **AuthzAccessCheck** function evaluates the requested access against the specified **SECURITY\_DESCRIPTOR** for a specified client context.</span></span> <span data-ttu-id="3e330-108">Сведения о том, как дескриптор безопасности управляет доступом к объекту, см. [в статье Управление доступом](how-dacls-control-access-to-an-object.md)к объекту в DACL.</span><span class="sxs-lookup"><span data-stu-id="3e330-108">For information about how a security descriptor controls access to an object, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="3e330-109">Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.</span><span class="sxs-lookup"><span data-stu-id="3e330-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="callback-function"></a><span data-ttu-id="3e330-110">Функция Callback</span><span class="sxs-lookup"><span data-stu-id="3e330-110">Callback Function</span></span>

<span data-ttu-id="3e330-111">Если [*избирательный список управления доступом*](/windows/desktop/SecGloss/d-gly) (DACL) [**\_ дескриптора безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) проверяемого объекта содержит любые [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) обратного вызова (ACE), [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) вызывает функцию [**аусзакцессчекккаллбакк**](authzaccesscheckcallback.md) для каждого элемента ACE обратного вызова, содержащегося в списке DACL.</span><span class="sxs-lookup"><span data-stu-id="3e330-111">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) of the object to be checked contains any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) calls the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function for each callback ACE contained in the DACL.</span></span> <span data-ttu-id="3e330-112">ACE обратного вызова — это любая структура ACE, Тип ACE которой содержит слово "Callback".</span><span class="sxs-lookup"><span data-stu-id="3e330-112">A callback ACE is any ACE structure whose ACE type contains the word "callback."</span></span> <span data-ttu-id="3e330-113">Функция **аусзакцессчекккаллбакк** — это определяемая приложением функция, которая должна быть зарегистрирована при инициализации диспетчера ресурсов путем вызова функции [**аусзинитиализересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="3e330-113">The **AuthzAccessCheckCallback** function is an application-defined function that must be registered when the resource manager is initialized by calling the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function.</span></span>

<span data-ttu-id="3e330-114">Функция обратного вызова позволяет приложению определить бизнес-логику для оценки во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e330-114">A callback function allows an application to define business logic to be evaluated at runtime.</span></span> <span data-ttu-id="3e330-115">При вызове функции [**АУСЗАКЦЕССЧЕКККАЛЛБАКК**](authzaccesscheckcallback.md) ACE обратного вызова, вызвавший вызов, передается функции обратного вызова для оценки.</span><span class="sxs-lookup"><span data-stu-id="3e330-115">When the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function is called, the callback ACE that caused the call is passed to the callback function for evaluation.</span></span> <span data-ttu-id="3e330-116">Если для определенной приложением логики вычисляется **значение true**, ACE обратного вызова включается в проверку доступа.</span><span class="sxs-lookup"><span data-stu-id="3e330-116">If the application-defined logic evaluates as **TRUE**, then the callback ACE is included in the access check.</span></span> <span data-ttu-id="3e330-117">В других случаях он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3e330-117">Otherwise, it is ignored.</span></span>

## <a name="caching-access-results"></a><span data-ttu-id="3e330-118">Кэширование результатов доступа</span><span class="sxs-lookup"><span data-stu-id="3e330-118">Caching Access Results</span></span>

<span data-ttu-id="3e330-119">Результаты проверки доступа можно кэшировать и использовать в последующих вызовах функции [**аусзкачедакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="3e330-119">The results of an access check can be cached and used in future calls to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="3e330-120">Дополнительные сведения об использовании кэширования проверок доступа, включая пример, см. в разделе [кэширование проверок доступа](caching-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="3e330-120">For more information about caching access checks, including an example, see [Caching Access Checks](caching-access-checks.md).</span></span>

## <a name="example"></a><span data-ttu-id="3e330-121">Пример</span><span class="sxs-lookup"><span data-stu-id="3e330-121">Example</span></span>

<span data-ttu-id="3e330-122">В следующем примере создается [**\_ дескриптор безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , позволяющий **\_ управлять** доступом на чтение к встроенным администраторам.</span><span class="sxs-lookup"><span data-stu-id="3e330-122">The following example creates a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) that allows **READ\_CONTROL** access to built-in administrators.</span></span> <span data-ttu-id="3e330-123">Он использует этот дескриптор безопасности для проверки доступа клиента, указанного в контексте клиента, созданного в примере при [инициализации контекста клиента](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="3e330-123">It uses that security descriptor to check access for the client specified by the client context created in the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL CheckAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR    pSecurityDescriptor = NULL;
    ULONG                    cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST    Request;
    CHAR                    ReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY        pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    DWORD                    AuthzError =0;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

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

    //Call AuthzAccessCheck.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        NULL))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
    
        return FALSE;
    }


    //Print results.
    if(*pReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }

  LocalFree(pSecurityDescriptor);
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="3e330-124">См. также</span><span class="sxs-lookup"><span data-stu-id="3e330-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e330-125">Добавление идентификаторов безопасности в контекст клиента</span><span class="sxs-lookup"><span data-stu-id="3e330-125">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="3e330-126">Проверки доступа кэширования</span><span class="sxs-lookup"><span data-stu-id="3e330-126">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="3e330-127">Инициализация контекста клиента</span><span class="sxs-lookup"><span data-stu-id="3e330-127">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="3e330-128">Запрос контекста клиента</span><span class="sxs-lookup"><span data-stu-id="3e330-128">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
