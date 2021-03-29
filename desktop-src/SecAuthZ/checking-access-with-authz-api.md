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
# <a name="checking-access-with-authz-api"></a>Проверка доступа с помощью API-интерфейса authz

Приложения определяют, предоставлять ли доступ к защищаемым объектам, вызывая функцию [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

Функция [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) принимает в качестве параметров как [**\_ \_ запрос на доступ к авторизации**](/windows/desktop/api/Authz/ns-authz-authz_access_request) , так и структуру [**\_ дескрипторов безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) . Структура **\_ \_ запроса на авторизацию** задает запрошенный уровень доступа. Функция **аусзакцессчекк** вычисляет запрошенный доступ к указанному **\_ дескриптору безопасности** для указанного контекста клиента. Сведения о том, как дескриптор безопасности управляет доступом к объекту, см. [в статье Управление доступом](how-dacls-control-access-to-an-object.md)к объекту в DACL.

Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.

## <a name="callback-function"></a>Функция Callback

Если [*избирательный список управления доступом*](/windows/desktop/SecGloss/d-gly) (DACL) [**\_ дескриптора безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) проверяемого объекта содержит любые [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) обратного вызова (ACE), [**аусзакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) вызывает функцию [**аусзакцессчекккаллбакк**](authzaccesscheckcallback.md) для каждого элемента ACE обратного вызова, содержащегося в списке DACL. ACE обратного вызова — это любая структура ACE, Тип ACE которой содержит слово "Callback". Функция **аусзакцессчекккаллбакк** — это определяемая приложением функция, которая должна быть зарегистрирована при инициализации диспетчера ресурсов путем вызова функции [**аусзинитиализересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .

Функция обратного вызова позволяет приложению определить бизнес-логику для оценки во время выполнения. При вызове функции [**АУСЗАКЦЕССЧЕКККАЛЛБАКК**](authzaccesscheckcallback.md) ACE обратного вызова, вызвавший вызов, передается функции обратного вызова для оценки. Если для определенной приложением логики вычисляется **значение true**, ACE обратного вызова включается в проверку доступа. В других случаях он игнорируется.

## <a name="caching-access-results"></a>Кэширование результатов доступа

Результаты проверки доступа можно кэшировать и использовать в последующих вызовах функции [**аусзкачедакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) . Дополнительные сведения об использовании кэширования проверок доступа, включая пример, см. в разделе [кэширование проверок доступа](caching-access-checks.md).

## <a name="example"></a>Пример

В следующем примере создается [**\_ дескриптор безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , позволяющий **\_ управлять** доступом на чтение к встроенным администраторам. Он использует этот дескриптор безопасности для проверки доступа клиента, указанного в контексте клиента, созданного в примере при [инициализации контекста клиента](initializing-a-client-context.md).


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Добавление идентификаторов безопасности в контекст клиента](adding-sids-to-a-client-context.md)
</dt> <dt>

[Проверки доступа кэширования](caching-access-checks.md)
</dt> <dt>

[Инициализация контекста клиента](initializing-a-client-context.md)
</dt> <dt>

[Запрос контекста клиента](querying-a-client-context.md)
</dt> </dl>

 

 
