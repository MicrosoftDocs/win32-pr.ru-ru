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
# <a name="context-windows-web-services"></a><span data-ttu-id="f69f3-106">Контекст (веб-службы Windows)</span><span class="sxs-lookup"><span data-stu-id="f69f3-106">Context (Windows Web Services)</span></span>

<span data-ttu-id="f69f3-107">Контекст используется в [операциях службы](service-operation.md) Service Model и обратных вызовах для передачи релевантных данных о состоянии в операцию службы или обратный вызов при вызове.</span><span class="sxs-lookup"><span data-stu-id="f69f3-107">A context is used in Service Model [service operations](service-operation.md) and callbacks to pass relevant state data to the service operation or callback when it is invoked.</span></span> <span data-ttu-id="f69f3-108">На контекст ссылается структура [ \_ \_ контекста операции WS](ws-operation-context.md) .</span><span class="sxs-lookup"><span data-stu-id="f69f3-108">A context is referenced by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure.</span></span> <span data-ttu-id="f69f3-109">Свойства контекста можно получить с помощью функции [**всжетоператионконтекстпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="f69f3-109">The properties of a context can be retrieved with the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function, as illustrated in the following code.</span></span>

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

<span data-ttu-id="f69f3-110">Не все свойства контекста доступны в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="f69f3-110">Not all the context properties are available at any given time.</span></span> <span data-ttu-id="f69f3-111">См. документацию по свойству контекста о доступности определенного свойства в обратном вызове или [операции службы](service-operation.md).</span><span class="sxs-lookup"><span data-stu-id="f69f3-111">See the context property documentation regarding availability of a specific property in a callback or a [service operation](service-operation.md).</span></span>

<span data-ttu-id="f69f3-112">Дополнительные сведения о том, как поддерживать время существования контекста операции и потоки, см. в разделе [время существования контекста операции и работа с потоками](operation-context-lifetime-and-threading.md) .</span><span class="sxs-lookup"><span data-stu-id="f69f3-112">For more information on how to maintain operation context lifetime and threading, see the [Operation Context Lifetime and Threading](operation-context-lifetime-and-threading.md) topic.</span></span>

<span data-ttu-id="f69f3-113">Следующее перечисление является частью контекста:</span><span class="sxs-lookup"><span data-stu-id="f69f3-113">The following enumeration is part of the context:</span></span>

-   [<span data-ttu-id="f69f3-114">**\_ \_ \_ идентификатор свойства контекста операции \_ WS**</span><span class="sxs-lookup"><span data-stu-id="f69f3-114">**WS\_OPERATION\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

<span data-ttu-id="f69f3-115">Следующая функция является частью контекста:</span><span class="sxs-lookup"><span data-stu-id="f69f3-115">The following function is part of the context:</span></span>

-   [<span data-ttu-id="f69f3-116">**всжетоператионконтекстпроперти**</span><span class="sxs-lookup"><span data-stu-id="f69f3-116">**WsGetOperationContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

<span data-ttu-id="f69f3-117">Следующий маркер является частью контекста:</span><span class="sxs-lookup"><span data-stu-id="f69f3-117">The following handle is part of the context:</span></span>

-   [<span data-ttu-id="f69f3-118">\_контекст операции \_ WS</span><span class="sxs-lookup"><span data-stu-id="f69f3-118">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)

 

 




