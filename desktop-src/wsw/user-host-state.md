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
# <a name="service-host-user-state"></a>Состояние пользователя узла службы

[Узел службы](service-host.md) позволяет приложению связывать данные состояния, область действия на уровне узла Service-Host. Это состояние задается структурой [**\_ \_ свойств службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) , которая передается функции [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , когда приложение создает [узел службы](service-host.md), как показано в следующем примере.

``` syntax
void* quotePtr = (void*) quotes;
WS_SERVICE_PROPERTY serviceProperties[1] = {0};
serviceProperties[0].id = WS_SERVICE_PROPERTY_HOST_USER_STATE;
serviceProperties[0].value = &quotePtr; // assume this is some state that you want to associate with the service host
serviceProperties[0].valueSize = sizeof(quotePtr);
```


Данные состояния доступны для всех обратных вызовов узла службы и [операций службы](service-operation.md). Обратные вызовы и операции службы извлекают сведения, вызывая функцию [**всжетоператионконтекстпроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) и указывая контекст, на который ссылается [Структура \_ \_ контекста операции WS](ws-operation-context.md) , и свойство Context в качестве одного из значений [**\_ \_ \_ свойства контекста \_ \_ \_ операции WS**](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id) еунумератион, как показано в следующем примере.

``` syntax
QuoteTable* table = NULL;
HRESULT hr = NOERROR;
if (FAILED (WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HOST_USER_STATE, &table, sizeof(table), NULL, error)))
    return hr;
```

 

 




