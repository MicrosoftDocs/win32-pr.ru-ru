---
description: Когда приложение выполняет проверку доступа путем вызова функции Аусзакцессчекк, результаты проверки доступа могут быть кэшированы.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Проверки доступа кэширования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83659c35fb9334e55bd7dfcd2368275dc16eb0d4836b8d6fa69a6ed8d713d953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783559"
---
# <a name="caching-access-checks"></a>Проверки доступа кэширования

Когда приложение выполняет проверку доступа путем вызова функции [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , результаты проверки доступа могут быть кэшированы. Если параметр *паусзандле* функции [**Аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) не равен **null**, функция выполняет отдельную проверку доступа с запрошенной [**\_ маской доступа**](access-mask.md) **максимально \_ допустимой** и кэширует результаты этой проверки. Затем можно передать результат проверки в качестве параметра *аусзандле* в функцию [**аусзкачедакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) . Это обеспечивает более быструю проверку доступа для заданных клиентов и [*дескрипторов безопасности*](/windows/desktop/SecGloss/s-gly).

Можно кэшировать только статическую часть проверки доступа. Все [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) или ACE, содержащие идентификаторы **безопасности \_ основного участника** , должны оцениваться для каждой проверки доступа.

Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.

## <a name="example"></a>Пример

В следующем примере проверяется доступ к кэшированному результату из предыдущей проверки доступа. Предыдущая проверка доступа была выполнена в примере [проверки доступа с помощью API authz](checking-access-with-authz-api.md).


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Добавление идентификаторов безопасности в контекст клиента](adding-sids-to-a-client-context.md)
</dt> <dt>

[Проверка доступа с помощью API-интерфейса authz](checking-access-with-authz-api.md)
</dt> <dt>

[Инициализация контекста клиента](initializing-a-client-context.md)
</dt> <dt>

[Запрос контекста клиента](querying-a-client-context.md)
</dt> </dl>

 

 
