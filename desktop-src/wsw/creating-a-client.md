---
title: Создание клиента
description: Создание клиента для веб-служб значительно упрощено в ВВСАПИ с помощью API модели службы и WsUtil.exe средства.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411384"
---
# <a name="creating-a-client"></a><span data-ttu-id="bb1c0-103">Создание клиента</span><span class="sxs-lookup"><span data-stu-id="bb1c0-103">Creating a Client</span></span>

<span data-ttu-id="bb1c0-104">Создание клиента для веб-служб значительно упрощено в ВВСАПИ с помощью API [модели службы](service-model-layer-overview.md) и [WsUtil.exe](wsutil-compiler-tool.md) средства.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-104">Creating a client for Web services is greatly simplified in WWSAPI by the [Service Model](service-model-layer-overview.md) API and the [WsUtil.exe](wsutil-compiler-tool.md) tool.</span></span> <span data-ttu-id="bb1c0-105">Модель службы предоставляет API, позволяющий клиенту отправлять и получать [сообщения](message.md) по [каналу](channel.md) в виде вызовов методов C.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-105">The Service Model provides an API that enables the client to send and receive [messages](message.md) over a [channel](channel.md) as C method calls.</span></span> <span data-ttu-id="bb1c0-106">Средство Всутил создает заголовки и вспомогательные методы для реализации клиента.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-106">The WsUtil tool generates headers and helpers for implementing the client.</span></span> <span data-ttu-id="bb1c0-107">Эти заголовки содержат типы и прототипы функций для функций C, представляющих службы, предоставляемые целевой веб-службой.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-107">These headers include the types and function prototypes for C functions representing the services offered by the target Web service.</span></span> <span data-ttu-id="bb1c0-108">Вспомогательные методы используются для создания прокси службы, который содержит сведения о привязке и [адрес конечной точки](endpoint-address.md) для службы.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-108">The helpers are used to create the service proxy, which contains the binding information and [endpoint address](endpoint-address.md) for the service.</span></span>

## <a name="using-wsutil-to-generate-headers-and-helpers"></a><span data-ttu-id="bb1c0-109">Использование Всутил для создания заголовков и вспомогательных функций</span><span class="sxs-lookup"><span data-stu-id="bb1c0-109">Using WsUtil to Generate Headers and Helpers</span></span>

<span data-ttu-id="bb1c0-110">Для создания заголовков и вспомогательных функций Всутил открывает и считывает файлы метаданных для целевой службы — WSDL и XSD-файлы, а затем преобразует их в заголовки. Поэтому необходимо заранее получить файлы метаданных целевой службы, например, с помощью SvcUtil, части Windows Communication Foundation.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-110">To generate the headers and helpers, WsUtil opens and reads the metadata files for the target service — wsdl and xsd files— and converts them into headers; therefore, it is necessary to retrieve the metadata files for the target service in advance, for example by using SvcUtil, a part of the Windows Communication Foundation.</span></span> <span data-ttu-id="bb1c0-111">По соображениям безопасности крайне важно, чтобы копии этих файлов были надежными.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-111">For security reasons, it is imperative that your copies of these files are trustworthy.</span></span> <span data-ttu-id="bb1c0-112">(Дополнительные сведения см. в разделе "безопасность" в разделе [средства компилятора всутил](wsutil-compiler-tool.md) .)</span><span class="sxs-lookup"><span data-stu-id="bb1c0-112">(For more information, see the "Security" section of the [WsUtil Compiler Tool](wsutil-compiler-tool.md) topic.)</span></span>

<span data-ttu-id="bb1c0-113">Чтобы запустить Всутил, используйте следующий синтаксис командной строки, если файлы WSDL и XSD для службы находятся в собственном каталоге: `WsUtil.exe *.wsdl *.xsd` .</span><span class="sxs-lookup"><span data-stu-id="bb1c0-113">To run WsUtil, use the following command-line syntax if the WSDL and XSD files for the service are in their own directory: `WsUtil.exe *.wsdl *.xsd`.</span></span> <span data-ttu-id="bb1c0-114">Кроме того, можно указать файлы по полному имени.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-114">Alternatively, you can specify the files by full name.</span></span>

<span data-ttu-id="bb1c0-115">Для каждого файла метаданных Всутил обычно создает два файла: заголовок и файл C.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-115">WsUtil generally generates two files for each metadata file: a header and a C file.</span></span> <span data-ttu-id="bb1c0-116">Добавьте эти файлы в проект кода и используйте \# инструкции include, чтобы включить их в код для клиента.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-116">Add these files to your coding project, and use \#include statements to include them in the code for your client.</span></span> <span data-ttu-id="bb1c0-117">(XSD-файлы представляют типы, а WSDL-файлы представляют операции.)</span><span class="sxs-lookup"><span data-stu-id="bb1c0-117">(The XSD files represent types, and the WSDL files represent operations.)</span></span>

## <a name="creating-the-service-proxy"></a><span data-ttu-id="bb1c0-118">Создание прокси-сервера службы</span><span class="sxs-lookup"><span data-stu-id="bb1c0-118">Creating the Service Proxy</span></span>

<span data-ttu-id="bb1c0-119">Заголовок, формируемый Всутил, содержит вспомогательную подпрограммы для создания прокси службы с требуемой привязкой.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-119">The header generated by WsUtil contains a helper routine for creating the service proxy with the required binding.</span></span> <span data-ttu-id="bb1c0-120">Эта подпрограммы включена в раздел "подпрограммы поддержки политик" созданного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-120">This routine is included in the "Policy helper routines" section of the generated header file.</span></span> <span data-ttu-id="bb1c0-121">Например, созданный заголовок для службы калькулятора, показанный в примере [хттпкалкулаторклиентексампле](httpcalculatorclientexample.md) , будет содержать следующий прототип функции.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-121">For example, the generated header for the calculator service illustrated in the [httpcalculatorclientexample](httpcalculatorclientexample.md) example will contain the following function prototype.</span></span>


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



<span data-ttu-id="bb1c0-122">Включите этот вспомогательный метод в код и передайте ему обработчик [ \_ \_ прокси-службы WS](ws-service-proxy.md) для получения маркера созданному прокси-серверу службы.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-122">Incorporate this helper in your code and pass a [WS\_SERVICE\_PROXY](ws-service-proxy.md) handle to receive the handle to the created service proxy.</span></span> <span data-ttu-id="bb1c0-123">В простейшем сценарии, в котором функции передаются только обработчик прокси-службы и объект ошибки, вызов выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-123">In the simplest scenario, in which only a service proxy handle and an error object are passed to the function, the call looks like the following.</span></span>


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



<span data-ttu-id="bb1c0-124">Чтобы создать часть адреса прокси-сервера службы, вызовите [**всопенсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) с помощью маркера прокси-сервера службы и указателя на [**\_ \_ адрес конечной точки WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) , содержащий адрес конечной точки службы, к которой нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-124">To create the address portion of the service proxy, call [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) with a handle to the service proxy and a pointer to a [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) containing the service endpoint address to which you wish to connect.</span></span>

## <a name="implementing-the-client-with-function-prototypes"></a><span data-ttu-id="bb1c0-125">Реализация клиента с прототипами функций</span><span class="sxs-lookup"><span data-stu-id="bb1c0-125">Implementing the Client with Function Prototypes</span></span>

<span data-ttu-id="bb1c0-126">Заголовки, созданные из файлов WSDL службы, также содержат прототипы функций C, представляющие службы, доступные в веб-службе, и конкретные требуемые привязки.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-126">The headers generated from the service WSDL files also contain C function prototypes representing the services available from the Web service and specific to the binding required.</span></span> <span data-ttu-id="bb1c0-127">Например, заголовок, созданный для службы калькулятора, показанный в Хттпкалкулаторсервицеексампле, будет содержать следующий прототип для операции умножения этой службы.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-127">For example, a header generated for the calculator service illustrated in HttpCalculatorServiceExample will contain the following prototype for that service's multiplication operation.</span></span>

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

<span data-ttu-id="bb1c0-128">Вы можете скопировать прототипы и использовать их в качестве шаблонов для кодирования вызовов функций в клиенте, каждый из которых передает этот обработчик прокси-серверу службы.</span><span class="sxs-lookup"><span data-stu-id="bb1c0-128">You can copy the prototypes and use them as templates for coding the function calls in your client, in each case passing the handle to service proxy.</span></span> <span data-ttu-id="bb1c0-129">По завершении работы с прокси-сервером службы вызовите [**всклосесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="bb1c0-129">When you are finished with the service proxy, call [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).</span></span>

 

 




