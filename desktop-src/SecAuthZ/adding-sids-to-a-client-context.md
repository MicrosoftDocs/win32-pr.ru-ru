---
description: Приложение может добавлять идентификаторы безопасности (SID) в существующий контекст клиента путем вызова функции Аусзаддсидстоконтекст.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Добавление идентификаторов безопасности в контекст клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a601f485110ddacea0fdb54cb7dcef587a25cb9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546330"
---
# <a name="adding-sids-to-a-client-context"></a><span data-ttu-id="1ed24-103">Добавление идентификаторов безопасности в контекст клиента</span><span class="sxs-lookup"><span data-stu-id="1ed24-103">Adding SIDs to a Client Context</span></span>

<span data-ttu-id="1ed24-104">Приложение может добавлять [*идентификаторы безопасности*](/windows/desktop/SecGloss/s-gly) (SID) в существующий контекст клиента путем вызова функции [**аусзаддсидстоконтекст**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="1ed24-104">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span> <span data-ttu-id="1ed24-105">Функция [**аусзаддсидстоконтекст**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) позволяет приложению указать как список идентификаторов безопасности, так и список с ограниченным идентификатором SID для указанного контекста клиента.</span><span class="sxs-lookup"><span data-stu-id="1ed24-105">The [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function allows an application to specify both a list of SIDs and a list of restricting SIDs to the specified client context.</span></span>

<span data-ttu-id="1ed24-106">Система использует список ограниченных идентификаторов безопасности при проверке доступа маркера к защищаемому объекту.</span><span class="sxs-lookup"><span data-stu-id="1ed24-106">The system uses the list of restricting SIDs when it checks the token's access to a securable object.</span></span> <span data-ttu-id="1ed24-107">Когда ограниченный процесс или поток пытается получить доступ к защищаемому объекту, система выполняет две проверки доступа: один использует идентификаторы SID, включенные в маркер, а другой — с помощью списка ограничивающих идентификаторов безопасности.</span><span class="sxs-lookup"><span data-stu-id="1ed24-107">When a restricted process or thread tries to access a securable object, the system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs.</span></span> <span data-ttu-id="1ed24-108">Доступ предоставляется только в том случае, если обе проверки доступа допускают запрошенные права доступа.</span><span class="sxs-lookup"><span data-stu-id="1ed24-108">Access is granted only if both access checks allow the requested access rights.</span></span>

<span data-ttu-id="1ed24-109">Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.</span><span class="sxs-lookup"><span data-stu-id="1ed24-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="1ed24-110">Пример</span><span class="sxs-lookup"><span data-stu-id="1ed24-110">Example</span></span>

<span data-ttu-id="1ed24-111">В следующем примере добавляется идентификатор безопасности и ограниченный идентификатор безопасности для контекста клиента, созданного в примере при [инициализации контекста клиента](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="1ed24-111">The following example adds a SID and a restricting SID to the client context created by the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL AddSidsToContext(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{
    AUTHZ_CLIENT_CONTEXT_HANDLE        NewContext = NULL;
    PSID                            pEveryoneSid = NULL;
    PSID                            pLocalSid = NULL;
    SID_AND_ATTRIBUTES                Sids;
    SID_AND_ATTRIBUTES                RestrictedSids;
    DWORD                            SidCount = 0;
    DWORD                            RestrictedSidCount = 0;

    //Create a PSID from the "Everyone" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-1-0", &pEveryoneSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError());
        return FALSE;
    }

    //Create a PSID from the "Local" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-2-0", &pLocalSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError);
        return FALSE;
    }

    //Set the members of the SID_AND_ATTRIBUTES structure to be added.
    Sids.Sid = pEveryoneSid;
    Sids.Attributes = SE_GROUP_ENABLED;

    //Set the members of the SID_AND_ATTRIBUTES structure for the restricting SID.
    RestrictedSids.Sid = pLocalSid;
    RestrictedSids.Attributes = SE_GROUP_ENABLED;

    

    //Create a new context with the new "Everyone" SID and "Local" restricting SID.
    if(!AuthzAddSidsToContext(
        *phClientContext,
        &Sids,
        1,
        &RestrictedSids,
        1,
        &NewContext))
    {
        printf_s("AuthzAddSidsToContext failed with %d\n", GetLastError());
        if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        return FALSE;
    }

    if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        
        AuthzFreeContext(*phClientContext);
        *phClientContext = NewContext;

    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="1ed24-112">См. также</span><span class="sxs-lookup"><span data-stu-id="1ed24-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ed24-113">Проверки доступа кэширования</span><span class="sxs-lookup"><span data-stu-id="1ed24-113">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="1ed24-114">Проверка доступа с помощью API-интерфейса authz</span><span class="sxs-lookup"><span data-stu-id="1ed24-114">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="1ed24-115">Инициализация контекста клиента</span><span class="sxs-lookup"><span data-stu-id="1ed24-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="1ed24-116">Запрос контекста клиента</span><span class="sxs-lookup"><span data-stu-id="1ed24-116">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
