---
description: Приложение должно создать контекст клиента, прежде чем он сможет использовать API-интерфейс authz для выполнения проверок доступа или аудита.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Инициализация контекста клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be229a60a12e33ab0c2bbd3e52fc533cf29ed1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664304"
---
# <a name="initializing-a-client-context"></a><span data-ttu-id="b0f77-103">Инициализация контекста клиента</span><span class="sxs-lookup"><span data-stu-id="b0f77-103">Initializing a Client Context</span></span>

<span data-ttu-id="b0f77-104">Приложение должно создать контекст клиента, прежде чем он сможет использовать API-интерфейс authz для выполнения проверок доступа или аудита.</span><span class="sxs-lookup"><span data-stu-id="b0f77-104">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span>

<span data-ttu-id="b0f77-105">Приложение должно вызвать функцию [**аусзинитиализересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) для инициализации диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0f77-105">An application must call the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function to initialize the resource manager.</span></span> <span data-ttu-id="b0f77-106">Затем приложение может вызвать одну из нескольких функций для создания контекста клиента.</span><span class="sxs-lookup"><span data-stu-id="b0f77-106">The application can then call one of several functions to create a client context.</span></span> <span data-ttu-id="b0f77-107">Кроме того, если вы выполняете проверку доступа или аудит удаленно, необходимо использовать функцию [**аусзинитиализеремотересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="b0f77-107">Additionally, if you are performing access checks or auditing remotely, you must use the [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) function.</span></span>

<span data-ttu-id="b0f77-108">Чтобы создать контекст клиента на основе существующего контекста клиента, вызовите функцию [**аусзинитиализеконтекстфромаусзконтекст**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .</span><span class="sxs-lookup"><span data-stu-id="b0f77-108">To create a client context based on an existing client context, call the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) function.</span></span>

<span data-ttu-id="b0f77-109">Функция [**аусзинитиализеконтекстфромтокен**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) создает новый контекст клиента, используя сведения в маркере входа.</span><span class="sxs-lookup"><span data-stu-id="b0f77-109">The [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function creates a new client context by using information in a logon token.</span></span> <span data-ttu-id="b0f77-110">Функция [**аусзинитиализеконтекстфромсид**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) создает новый контекст клиента, используя указанный [**идентификатор безопасности**](/windows/desktop/api/Winnt/ns-winnt-sid).</span><span class="sxs-lookup"><span data-stu-id="b0f77-110">The [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) function creates a new client context by using the specified [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid).</span></span>

<span data-ttu-id="b0f77-111">Если это возможно, вызовите функцию [**аусзинитиализеконтекстфромтокен**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) вместо [**аусзинитиализеконтекстфромсид**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span><span class="sxs-lookup"><span data-stu-id="b0f77-111">If possible, call the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function instead of [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span></span> <span data-ttu-id="b0f77-112">**Аусзинитиализеконтекстфромсид** пытается получить сведения, доступные в маркере входа, если клиент действительно вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="b0f77-112">**AuthzInitializeContextFromSid** attempts to retrieve the information available in a logon token had the client actually logged on.</span></span> <span data-ttu-id="b0f77-113">Фактический маркер входа предоставляет дополнительные сведения, такие как тип входа и свойства входа в систему, и отражает поведение пакета проверки подлинности, используемого для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="b0f77-113">An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon.</span></span> <span data-ttu-id="b0f77-114">Контекст клиента, созданный с помощью **аусзинитиализеконтекстфромтокен** , использует маркер входа, а результирующий контекст клиента более полный и точный, чем контекст клиента, созданный **аусзинитиализеконтекстфромсид**.</span><span class="sxs-lookup"><span data-stu-id="b0f77-114">The client context created by **AuthzInitializeContextFromToken** uses a logon token, and the resulting client context is more complete and accurate than a client context created by **AuthzInitializeContextFromSid**.</span></span>

> [!Note]  
> <span data-ttu-id="b0f77-115">Переменные атрибутов безопасности должны присутствовать в контексте клиента, если они ссылаются на условное выражение; в противном случае термин условного выражения, ссылающийся на них, будет оцениваться как неизвестный.</span><span class="sxs-lookup"><span data-stu-id="b0f77-115">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="b0f77-116">Дополнительные сведения о условных выражениях см. в разделе [язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="b0f77-116">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

 

## <a name="example"></a><span data-ttu-id="b0f77-117">Пример</span><span class="sxs-lookup"><span data-stu-id="b0f77-117">Example</span></span>

<span data-ttu-id="b0f77-118">В следующем примере инициализируется диспетчер ресурсов authz и вызывается функция [**аусзинитиализеконтекстфромтокен**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) для создания контекста клиента из маркера входа, связанного с текущим процессом.</span><span class="sxs-lookup"><span data-stu-id="b0f77-118">The following example initializes the Authz resource manager and calls the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function to create a client context from the logon token associated with the current process.</span></span>


```C++
BOOL AuthzInitFromToken(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{

    HANDLE                            hToken = NULL;
    LUID                            Luid = {0, 0};

    
    ULONG                            uFlags = 0;


    //Initialize Resource Manager
    if(!AuthzInitializeResourceManager(
        AUTHZ_RM_FLAG_NO_AUDIT,
        NULL,
        NULL,
        NULL,
        L"My Resource Manager",
        &g_hResourceManager
        ))
    {
        printf_s("AuthzInitializeResourceManager failed with %d\n", GetLastError);
        return FALSE;
    }
    

    //Get the current token.

    if(!OpenProcessToken(GetCurrentProcess(), TOKEN_ALL_ACCESS, &hToken))
    {
        printf_s("OpenProcessToken failed with %d\n", GetLastError);
        return FALSE;
    }


    //Initialize the client context

    if(!AuthzInitializeContextFromToken(
        0,
        hToken,
        g_hResourceManager,
        NULL,
        Luid,
        NULL,
        phClientContext
        ))
    {    
        printf_s("AuthzInitializeContextFromToken failed with %d\n", GetLastError);
        return FALSE;
    }

    
    printf_s("Initialized client context. \n");
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="b0f77-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b0f77-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f77-120">Добавление идентификаторов безопасности в контекст клиента</span><span class="sxs-lookup"><span data-stu-id="b0f77-120">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="b0f77-121">Проверки доступа кэширования</span><span class="sxs-lookup"><span data-stu-id="b0f77-121">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="b0f77-122">Проверка доступа с помощью API-интерфейса authz</span><span class="sxs-lookup"><span data-stu-id="b0f77-122">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="b0f77-123">Как работает AccessCheck</span><span class="sxs-lookup"><span data-stu-id="b0f77-123">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="b0f77-124">Запрос контекста клиента</span><span class="sxs-lookup"><span data-stu-id="b0f77-124">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="b0f77-125">Язык определения дескрипторов безопасности для условных элементов ACE</span><span class="sxs-lookup"><span data-stu-id="b0f77-125">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="b0f77-126">**аусзинитиализеремотересаурцеманажер**</span><span class="sxs-lookup"><span data-stu-id="b0f77-126">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="b0f77-127">**аусзинитиализересаурцеманажер**</span><span class="sxs-lookup"><span data-stu-id="b0f77-127">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



