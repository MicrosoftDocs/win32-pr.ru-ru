---
title: Контекст (веб-службы Windows)
description: Контекст используется в операциях службы Service Model и обратных вызовах для передачи релевантных данных о состоянии в операцию службы или обратный вызов при вызове.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Контекстные веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "103987095"
---
# <a name="context-windows-web-services"></a>Контекст (веб-службы Windows)

Контекст используется в [операциях службы](service-operation.md) Service Model и обратных вызовах для передачи релевантных данных о состоянии в операцию службы или обратный вызов при вызове. На контекст ссылается структура [ \_ \_ контекста операции WS](ws-operation-context.md) . Свойства контекста можно получить с помощью функции [**всжетоператионконтекстпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , как показано в следующем коде.

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

Не все свойства контекста доступны в любое заданное время. См. документацию по свойству контекста о доступности определенного свойства в обратном вызове или [операции службы](service-operation.md).

Дополнительные сведения о том, как поддерживать время существования контекста операции и потоки, см. в разделе [время существования контекста операции и работа с потоками](operation-context-lifetime-and-threading.md) .

Следующее перечисление является частью контекста:

-   [**\_ \_ \_ идентификатор свойства контекста операции \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

Следующая функция является частью контекста:

-   [**всжетоператионконтекстпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

Следующий маркер является частью контекста:

-   [\_контекст операции \_ WS](ws-operation-context.md)

 

 




