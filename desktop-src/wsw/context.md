---
title: контекст (Windows веб-служб)
description: Контекст используется в операциях службы Service Model и обратных вызовах для передачи релевантных данных о состоянии в операцию службы или обратный вызов при вызове.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Контекстные веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd7863f22193dd1496134afff991ff54efbee5026f2a11e52359b2b016c878c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026632"
---
# <a name="context-windows-web-services"></a>контекст (Windows веб-служб)

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

 

 




