---
title: Состояние пользователя узла службы
description: Узел службы позволяет приложению связывать данные состояния, область действия на уровне узла Service-Host.
ms.assetid: e18c6c0c-3205-4f88-9a9b-2515a7cfc462
keywords:
- Веб-службы состояния узла пользователя для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56f43942f7743d28534e0286a45203dc01e0e7b6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105700983"
---
# <a name="service-host-user-state"></a><span data-ttu-id="226a1-106">Состояние пользователя узла службы</span><span class="sxs-lookup"><span data-stu-id="226a1-106">Service Host User State</span></span>

<span data-ttu-id="226a1-107">[Узел службы](service-host.md) позволяет приложению связывать данные состояния, область действия на уровне узла Service-Host.</span><span class="sxs-lookup"><span data-stu-id="226a1-107">The [service host](service-host.md) enables an application to associate state data that is scoped at the service-host level.</span></span> <span data-ttu-id="226a1-108">Это состояние задается структурой [**\_ \_ свойств службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) , которая передается функции [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , когда приложение создает [узел службы](service-host.md), как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="226a1-108">This state is is specified by a [**WS\_SERVICE\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) structure that is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function when the application creates a [service host](service-host.md), as illustrated in the following example.</span></span>

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


<span data-ttu-id="226a1-109">Данные состояния доступны для всех обратных вызовов узла службы и [операций службы](service-operation.md).</span><span class="sxs-lookup"><span data-stu-id="226a1-109">The state data is available to all service host callbacks and [service operations](service-operation.md).</span></span> <span data-ttu-id="226a1-110">Обратные вызовы и операции службы извлекают сведения, вызывая функцию [**всжетоператионконтекстпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) и указывая контекст, на который ссылается [Структура \_ \_ контекста операции WS](ws-operation-context.md) , и свойство Context в качестве одного из значений [**\_ \_ \_ свойства контекста \_ \_ \_ операции WS**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) еунумератион, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="226a1-110">Callbacks and service operations retrieve the information by calling the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function and specifying the context, referenced by the [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure, and the context property, as one of the values of the [**WS\_OPERATION\_CONTEXT\_PROPERTY\_HOST\_USER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) eunumeration, as illustrated in the following example.</span></span>

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




