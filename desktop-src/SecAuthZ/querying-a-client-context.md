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
# <a name="querying-a-client-context"></a>Запрос контекста клиента

Приложения могут вызывать функцию [**аусзжетинформатионфромконтекст**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) для запроса сведений о существующем контексте клиента.

Параметр *Инфокласс* функции [**аусзжетинформатионфромконтекст**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) принимает значение из перечисления [**\_ \_ \_ класса сведений о контексте AUTHZ**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) , которое указывает тип информации, которую запрашивает функция.

Переменные атрибутов безопасности должны присутствовать в контексте клиента, если они ссылаются на условное выражение; в противном случае термин условного выражения, ссылающийся на них, будет оцениваться как неизвестный. Дополнительные сведения о условных выражениях см. в разделе [язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md) .

## <a name="example"></a>Пример

В следующем примере выполняется запрос к контексту клиента, созданному в примере, из [инициализации контекста клиента](initializing-a-client-context.md) для получения списка [**идентификаторов безопасности**](/windows/desktop/api/Winnt/ns-winnt-sid) групп, связанных с этим контекстом клиента.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Добавление идентификаторов безопасности в контекст клиента](adding-sids-to-a-client-context.md)
</dt> <dt>

[Проверки доступа кэширования](caching-access-checks.md)
</dt> <dt>

[Проверка доступа с помощью API-интерфейса authz](checking-access-with-authz-api.md)
</dt> <dt>

[Как работает AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Инициализация контекста клиента](initializing-a-client-context.md)
</dt> <dt>

[Язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



