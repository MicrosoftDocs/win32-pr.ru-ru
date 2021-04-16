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
# <a name="adding-sids-to-a-client-context"></a>Добавление идентификаторов безопасности в контекст клиента

Приложение может добавлять [*идентификаторы безопасности*](/windows/desktop/SecGloss/s-gly) (SID) в существующий контекст клиента путем вызова функции [**аусзаддсидстоконтекст**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) . Функция [**аусзаддсидстоконтекст**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) позволяет приложению указать как список идентификаторов безопасности, так и список с ограниченным идентификатором SID для указанного контекста клиента.

Система использует список ограниченных идентификаторов безопасности при проверке доступа маркера к защищаемому объекту. Когда ограниченный процесс или поток пытается получить доступ к защищаемому объекту, система выполняет две проверки доступа: один использует идентификаторы SID, включенные в маркер, а другой — с помощью списка ограничивающих идентификаторов безопасности. Доступ предоставляется только в том случае, если обе проверки доступа допускают запрошенные права доступа.

Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.

## <a name="example"></a>Пример

В следующем примере добавляется идентификатор безопасности и ограниченный идентификатор безопасности для контекста клиента, созданного в примере при [инициализации контекста клиента](initializing-a-client-context.md).


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Проверки доступа кэширования](caching-access-checks.md)
</dt> <dt>

[Проверка доступа с помощью API-интерфейса authz](checking-access-with-authz-api.md)
</dt> <dt>

[Инициализация контекста клиента](initializing-a-client-context.md)
</dt> <dt>

[Запрос контекста клиента](querying-a-client-context.md)
</dt> </dl>

 

 
