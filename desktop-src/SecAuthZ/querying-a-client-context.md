---
description: Приложения могут вызывать функцию Аусзжетинформатионфромконтекст для запроса сведений о существующем контексте клиента.
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: Запрос контекста клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101c35466e675d9ecba942089bbe7b5e82cffd90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662572"
---
# <a name="querying-a-client-context"></a><span data-ttu-id="93663-103">Запрос контекста клиента</span><span class="sxs-lookup"><span data-stu-id="93663-103">Querying a Client Context</span></span>

<span data-ttu-id="93663-104">Приложения могут вызывать функцию [**аусзжетинформатионфромконтекст**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) для запроса сведений о существующем контексте клиента.</span><span class="sxs-lookup"><span data-stu-id="93663-104">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span>

<span data-ttu-id="93663-105">Параметр *Инфокласс* функции [**аусзжетинформатионфромконтекст**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) принимает значение из перечисления [**\_ \_ \_ класса сведений о контексте AUTHZ**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) , которое указывает тип информации, которую запрашивает функция.</span><span class="sxs-lookup"><span data-stu-id="93663-105">The *InfoClass* parameter of the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function takes a value from the [**AUTHZ\_CONTEXT\_INFORMATION\_CLASS**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) enumeration that specifies what type of information the function queries.</span></span>

<span data-ttu-id="93663-106">Переменные атрибутов безопасности должны присутствовать в контексте клиента, если они ссылаются на условное выражение; в противном случае термин условного выражения, ссылающийся на них, будет оцениваться как неизвестный.</span><span class="sxs-lookup"><span data-stu-id="93663-106">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="93663-107">Дополнительные сведения о условных выражениях см. в разделе [язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="93663-107">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

## <a name="example"></a><span data-ttu-id="93663-108">Пример</span><span class="sxs-lookup"><span data-stu-id="93663-108">Example</span></span>

<span data-ttu-id="93663-109">В следующем примере выполняется запрос к контексту клиента, созданному в примере, из [инициализации контекста клиента](initializing-a-client-context.md) для получения списка [**идентификаторов безопасности**](/windows/desktop/api/Winnt/ns-winnt-sid) групп, связанных с этим контекстом клиента.</span><span class="sxs-lookup"><span data-stu-id="93663-109">The following example queries the client context created in the example from [Initializing a Client Context](initializing-a-client-context.md) to retrieve the list of [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) of groups associated with that client context.</span></span>


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="93663-110">См. также</span><span class="sxs-lookup"><span data-stu-id="93663-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93663-111">Добавление идентификаторов безопасности в контекст клиента</span><span class="sxs-lookup"><span data-stu-id="93663-111">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="93663-112">Проверки доступа кэширования</span><span class="sxs-lookup"><span data-stu-id="93663-112">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="93663-113">Проверка доступа с помощью API-интерфейса authz</span><span class="sxs-lookup"><span data-stu-id="93663-113">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="93663-114">Как работает AccessCheck</span><span class="sxs-lookup"><span data-stu-id="93663-114">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="93663-115">Инициализация контекста клиента</span><span class="sxs-lookup"><span data-stu-id="93663-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="93663-116">Язык определения дескрипторов безопасности для условных элементов ACE</span><span class="sxs-lookup"><span data-stu-id="93663-116">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



