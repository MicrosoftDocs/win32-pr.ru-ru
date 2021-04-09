---
title: Создание службы
description: Создание веб-службы значительно упрощено в ВВСАПИ с помощью API модели службы и WsUtil.exe средства.
ms.assetid: 3536d1c6-6179-4f69-9cc8-27fe6ae30826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4700324a84962047f403ca7ad090adc3e9f4e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889132"
---
# <a name="creating-a-service"></a>Создание службы

Создание веб-службы значительно упрощено в ВВСАПИ с помощью API [модели службы](service-model-layer-overview.md) и [WsUtil.exe](wsutil-compiler-tool.md) средства. Модель службы предоставляет API, который позволяет службе и клиенту отправлять и получать [сообщения](message.md) по [каналу](channel.md) в виде вызовов методов C. Средство Всутил создает заглушки и заголовки для реализации службы.

## <a name="implementing-a-calculator-service-using-wwsapi"></a>Реализация службы калькулятора с помощью ВВСАПИ

Используя созданные источники из средства [Wsutil.exe](wsutil-compiler-tool.md) , реализуйте службу, выполнив следующие действия.

Включите заголовки в источник приложения.

``` syntax
#include "CalculatorProxyStub.h"
```

Реализуйте операции службы. В этом примере операции службы — это функции добавления и вычитания службы калькулятора.

``` syntax
HRESULT CALLBACK Add (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a + b;
    printf ("%d + %d = %d\n", a, b, *result);
    return NOERROR;
}

HRESULT CALLBACK Subtract (const WS_OPERATION_CONTEXT* context, 
                  int a, int b, int* result, 
                  const WS_ASYNC_CONTEXT* asyncContext, 
                  WS_ERROR* error)
{
    *result = a - b;
    printf ("%d - %d = %d\n", a, b, *result);
    return NOERROR;
}
```

Определите контракт службы, задав поля структуры [**\_ \_ контракта службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) .

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

Теперь создайте узел службы и откройте его для взаимодействия.

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
serviceEndpoint.uri.chars = L"https://+:80/example"; // address given as uri
serviceEndpoint.binding.channelBinding =  WS_HTTP_CHANNEL_BINDING; // channel binding for the endpoint
serviceEndpoint.channelType = WS_CHANNEL_TYPE_REPLY; // the channel type
serviceEndpoint.uri.length = (ULONG)wcslen(serviceEndpoint.uri.chars);
serviceEndpoint.contract = (WS_SERVICE_CONTRACT*)&calculatorContract;  // the contract
serviceEndpoint.properties = serviceProperties;
serviceEndpoint.propertyCount = WsCountOf(serviceProperties);

if (FAILED (hr = WsCreateServiceHost (&serviceEndpoint, 1, NULL, 0, &host, error)))
    goto Error;

// WsOpenServiceHost  to start the listeners in the service host 
if (FAILED (hr = WsOpenServiceHost (host, NULL, error)))
    goto Error;
```

Ознакомьтесь с примером кода в [хттпкалкулаторсервицеексампле](httpcalculatorserviceexample.md) для полной реализации службы калькулятора.

 

 




