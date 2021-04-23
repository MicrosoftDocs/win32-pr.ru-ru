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
# <a name="creating-a-service"></a><span data-ttu-id="f782d-103">Создание службы</span><span class="sxs-lookup"><span data-stu-id="f782d-103">Creating a Service</span></span>

<span data-ttu-id="f782d-104">Создание веб-службы значительно упрощено в ВВСАПИ с помощью API [модели службы](service-model-layer-overview.md) и [WsUtil.exe](wsutil-compiler-tool.md) средства.</span><span class="sxs-lookup"><span data-stu-id="f782d-104">Creating a Web service is greatly simplified in WWSAPI by the [Service Model](service-model-layer-overview.md) API and the [WsUtil.exe](wsutil-compiler-tool.md) tool.</span></span> <span data-ttu-id="f782d-105">Модель службы предоставляет API, который позволяет службе и клиенту отправлять и получать [сообщения](message.md) по [каналу](channel.md) в виде вызовов методов C.</span><span class="sxs-lookup"><span data-stu-id="f782d-105">The Service Model provides an API that enables the service and client to send and receive [messages](message.md) over a [channel](channel.md) as C method calls.</span></span> <span data-ttu-id="f782d-106">Средство Всутил создает заглушки и заголовки для реализации службы.</span><span class="sxs-lookup"><span data-stu-id="f782d-106">The WsUtil tool generates stubs and headers for implementing the service.</span></span>

## <a name="implementing-a-calculator-service-using-wwsapi"></a><span data-ttu-id="f782d-107">Реализация службы калькулятора с помощью ВВСАПИ</span><span class="sxs-lookup"><span data-stu-id="f782d-107">Implementing a Calculator Service using WWSAPI</span></span>

<span data-ttu-id="f782d-108">Используя созданные источники из средства [Wsutil.exe](wsutil-compiler-tool.md) , реализуйте службу, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f782d-108">Using the generated sources from the [Wsutil.exe](wsutil-compiler-tool.md) tool, implement the service by the following steps.</span></span>

<span data-ttu-id="f782d-109">Включите заголовки в источник приложения.</span><span class="sxs-lookup"><span data-stu-id="f782d-109">Include the headers in your application source.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="f782d-110">Реализуйте операции службы.</span><span class="sxs-lookup"><span data-stu-id="f782d-110">Implement the service operations.</span></span> <span data-ttu-id="f782d-111">В этом примере операции службы — это функции добавления и вычитания службы калькулятора.</span><span class="sxs-lookup"><span data-stu-id="f782d-111">In this example, the service operations are the Add and Subtract functions of the calculator service.</span></span>

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

<span data-ttu-id="f782d-112">Определите контракт службы, задав поля структуры [**\_ \_ контракта службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) .</span><span class="sxs-lookup"><span data-stu-id="f782d-112">Define the service contract by setting the fields of a [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure.</span></span>

``` syntax
static const DefaultBinding_ICalculatorFunctionTable calculatorFunctions = {Add, Subtract};
static const WS_SERVICE_CONTRACT calculatorContract = 
{
    &DefaultBinding_ICalculatorContractDesc, // comes from the generated header.
    NULL, // for not specifying the default contract
    &calculatorFunctions // specified by the user
};
```

<span data-ttu-id="f782d-113">Теперь создайте узел службы и откройте его для взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="f782d-113">Now, create a service host and open it for communication.</span></span>

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

<span data-ttu-id="f782d-114">Ознакомьтесь с примером кода в [хттпкалкулаторсервицеексампле](httpcalculatorserviceexample.md) для полной реализации службы калькулятора.</span><span class="sxs-lookup"><span data-stu-id="f782d-114">Please refer to the code example at [HttpCalculatorServiceExample](httpcalculatorserviceexample.md) for a full implementation of the calculator service.</span></span>

 

 




