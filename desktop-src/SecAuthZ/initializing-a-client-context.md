---
description: Приложение должно создать контекст клиента, прежде чем он сможет использовать API-интерфейс authz для выполнения проверок доступа или аудита.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Инициализация контекста клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da8a3c3191f323cf6ce35fda90f4bd75299dac67183986998cf21a80c0ee6995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908044"
---
# <a name="initializing-a-client-context"></a>Инициализация контекста клиента

Приложение должно создать контекст клиента, прежде чем он сможет использовать API-интерфейс authz для выполнения проверок доступа или аудита.

Приложение должно вызвать функцию [**аусзинитиализересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) для инициализации диспетчера ресурсов. Затем приложение может вызвать одну из нескольких функций для создания контекста клиента. Кроме того, если вы выполняете проверку доступа или аудит удаленно, необходимо использовать функцию [**аусзинитиализеремотересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .

Чтобы создать контекст клиента на основе существующего контекста клиента, вызовите функцию [**аусзинитиализеконтекстфромаусзконтекст**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .

Функция [**аусзинитиализеконтекстфромтокен**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) создает новый контекст клиента, используя сведения в маркере входа. Функция [**аусзинитиализеконтекстфромсид**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) создает новый контекст клиента, используя указанный [**идентификатор безопасности**](/windows/desktop/api/Winnt/ns-winnt-sid).

Если это возможно, вызовите функцию [**аусзинитиализеконтекстфромтокен**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) вместо [**аусзинитиализеконтекстфромсид**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid). **Аусзинитиализеконтекстфромсид** пытается получить сведения, доступные в маркере входа, если клиент действительно вошел в систему. Фактический маркер входа предоставляет дополнительные сведения, такие как тип входа и свойства входа в систему, и отражает поведение пакета проверки подлинности, используемого для входа в систему. Контекст клиента, созданный с помощью **аусзинитиализеконтекстфромтокен** , использует маркер входа, а результирующий контекст клиента более полный и точный, чем контекст клиента, созданный **аусзинитиализеконтекстфромсид**.

> [!Note]  
> Переменные атрибутов безопасности должны присутствовать в контексте клиента, если они ссылаются на условное выражение; в противном случае термин условного выражения, ссылающийся на них, будет оцениваться как неизвестный. Дополнительные сведения о условных выражениях см. в разделе [язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md) .

 

## <a name="example"></a>Пример

В следующем примере инициализируется диспетчер ресурсов authz и вызывается функция [**аусзинитиализеконтекстфромтокен**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) для создания контекста клиента из маркера входа, связанного с текущим процессом.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Добавление идентификаторов безопасности в контекст клиента](adding-sids-to-a-client-context.md)
</dt> <dt>

[Проверки доступа кэширования](caching-access-checks.md)
</dt> <dt>

[Проверка доступа с помощью API-интерфейса authz](checking-access-with-authz-api.md)
</dt> <dt>

[Как работает AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Запрос контекста клиента](querying-a-client-context.md)
</dt> <dt>

[Язык определения дескрипторов безопасности для условных элементов ACE](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**аусзинитиализеремотересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**аусзинитиализересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



