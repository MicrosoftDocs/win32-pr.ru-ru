---
title: Обзор уровня модели службы
description: API-интерфейс модели службы ВВСАПИ моделирует связь между клиентом и службой в качестве вызовов метода, а не сообщений данных.
ms.assetid: a1ed1e3c-94ae-4383-9251-83caf2e3ebf3
keywords:
- Обзор уровня модели службы веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74861f0e2ed13b35e308d1314aec2a33dc28c31
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104351115"
---
# <a name="service-model-layer-overview"></a><span data-ttu-id="ccb23-106">Обзор уровня модели службы</span><span class="sxs-lookup"><span data-stu-id="ccb23-106">Service Model Layer Overview</span></span>

<span data-ttu-id="ccb23-107">API-интерфейс модели службы ВВСАПИ моделирует связь между клиентом и службой в качестве вызовов метода, а не сообщений данных.</span><span class="sxs-lookup"><span data-stu-id="ccb23-107">The WWSAPI Service Model API models the communication between a client and a service as method calls, rather than as data messages.</span></span> <span data-ttu-id="ccb23-108">В отличие от [уровня канала](channel-layer-overview.md), который поддерживает более традиционные обмены [сообщениями](message.md) между клиентом и службой, модель службы автоматически управляет связью с помощью прокси-сервера службы на клиенте и узла службы в службе.</span><span class="sxs-lookup"><span data-stu-id="ccb23-108">In contrast to the [channel layer](channel-layer-overview.md), which supports more traditional [message](message.md) exchanges between client and service, the Service Model automatically manages communication by means of a service proxy on the client and a service host on the service.</span></span> <span data-ttu-id="ccb23-109">Это означает, что клиент вызывает созданные функции, а сервер реализует обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="ccb23-109">This means that the client calls generated functions and the server implements callbacks.</span></span>


<span data-ttu-id="ccb23-110">Например, рассмотрим службу калькулятора, которая выполняет сложение и вычитание двух чисел.</span><span class="sxs-lookup"><span data-stu-id="ccb23-110">For example, consider a calculator service which performs addition and subtraction on two numbers.</span></span> <span data-ttu-id="ccb23-111">Сложение и вычитание — это операции, естественно представленные в виде вызовов методов.</span><span class="sxs-lookup"><span data-stu-id="ccb23-111">Addition and subtraction are operations naturally represented as method calls.</span></span>

![Диаграмма, показывающая, как служба калькулятора взаимодействует с клиентом, используя вызовы методов для сложения и вычитания.](images/servicemodelintro.png)

<span data-ttu-id="ccb23-113">Модель службы представляет взаимодействие между клиентом и службой в виде объявленных вызовов методов, поэтому скрывает сведения о связи базового уровня канала из приложения, упрощая реализацию службы.</span><span class="sxs-lookup"><span data-stu-id="ccb23-113">The service model represents the communication between client and the service as declared method calls, and so conceals the communication details of the underlying channel layer from the application, making the service easier to implement.</span></span>

## <a name="specifying-a-service"></a><span data-ttu-id="ccb23-114">Указание службы</span><span class="sxs-lookup"><span data-stu-id="ccb23-114">Specifying a Service</span></span>

<span data-ttu-id="ccb23-115">Служба должна быть указана с точки зрения его шаблонов обмена сообщениями, а также его представления данных сети.</span><span class="sxs-lookup"><span data-stu-id="ccb23-115">A service must be specified in terms of its message exchange patterns as well as its network data representation.</span></span> <span data-ttu-id="ccb23-116">Для служб эта спецификация обычно предоставляется в виде документов WSDL и XML-схем.</span><span class="sxs-lookup"><span data-stu-id="ccb23-116">For services, this specification is usually provided as WSDL and XML schema documents.</span></span>

<span data-ttu-id="ccb23-117">Документ WSDL представляет собой XML-документ, содержащий привязку канала и шаблоны обмена сообщениями службы, в то время как документ схемы XML представляет собой XML-документ, определяющий представление данных отдельных сообщений.</span><span class="sxs-lookup"><span data-stu-id="ccb23-117">The WSDL document is an XML document which contains the channel binding and the message exchange patterns of the service, whereas the XML schema document is an XML document that defines the data representation of the individual messages.</span></span>

<span data-ttu-id="ccb23-118">Для службы калькулятора и ее операций сложения и вычитания документ WSDL может выглядеть, как в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="ccb23-118">For the calculator service and its addition and subtraction operations, the WSDL document might look like the following example:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" 
xmlns:soapenc="http://schemas.xmlsoap.org/soap/encoding/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsp="http://schemas.xmlsoap.org/ws/2004/09/policy" 
xmlns:wsap="http://schemas.xmlsoap.org/ws/2004/08/addressing/policy" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
xmlns:msc="http://schemas.microsoft.com/ws/2005/12/wsdl/contract" xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" xmlns:wsa10="http://www.w3.org/2005/08/addressing" 
xmlns:wsx="http://schemas.xmlsoap.org/ws/2004/09/mex" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:portType name="ICalculator">
  <wsdl:operation name="Add">
   <wsdl:input wsaw:Action="http://Example.org/ICalculator/Add" 
   message="tns:ICalculator_Add_InputMessage" />
   <wsdl:output wsaw:Action="http://Example.org/ICalculator/AddResponse" 
   message="tns:ICalculator_Add_OutputMessage" />
  </wsdl:operation>
 </wsdl:portType>
</wsdl:definitions>
```

<span data-ttu-id="ccb23-119">Аналогичным образом ее XML-схема может быть определена следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ccb23-119">Likewise, its XML schema can be defined as follows:</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <xs:element name="Add">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="a" type="xs:int" />
    <xs:element minOccurs="0" name="b" type="xs:int" />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
 <xs:element name="AddResponse">
  <xs:complexType>
   <xs:sequence>
    <xs:element minOccurs="0" name="result" type="xs:int" 
    />
   </xs:sequence>
  </xs:complexType>
 </xs:element>
</xs:schema> 
```

## <a name="converting-metadata-to-code"></a><span data-ttu-id="ccb23-120">Преобразование метаданных в код</span><span class="sxs-lookup"><span data-stu-id="ccb23-120">Converting Metadata to Code</span></span>

<span data-ttu-id="ccb23-121">Модель службы предоставляет [WsUtil.exe](web-service-compiler-tool.md) в качестве средства для обработки этих документов метаданных, преобразования WSDL-файла в заголовок C и исходные файлы.</span><span class="sxs-lookup"><span data-stu-id="ccb23-121">The service model provides the [WsUtil.exe](web-service-compiler-tool.md) as a tool to process these metadata documents, converting a WSDL file into a C header and source files.</span></span>

![Схема, показывающая, как WsUtil.exe преобразует WSDL-файл в заголовок C и исходные файлы.](images/doctotool.png)

<span data-ttu-id="ccb23-123">[WsUtil.exe](web-service-compiler-tool.md) создает заголовок и источники для реализации службы, а также операции службы на стороне клиента для клиента.</span><span class="sxs-lookup"><span data-stu-id="ccb23-123">The [WsUtil.exe](web-service-compiler-tool.md) generates header and sources for service implementation as well as client-side service operations for the client .</span></span>

## <a name="calling-the-calculator-service-from-a-client"></a><span data-ttu-id="ccb23-124">Вызов службы калькулятора из клиента</span><span class="sxs-lookup"><span data-stu-id="ccb23-124">Calling the Calculator Service From a Client</span></span>

<span data-ttu-id="ccb23-125">Как и в случае с реализацией службы, клиент должен включать созданный заголовок или заголовки.</span><span class="sxs-lookup"><span data-stu-id="ccb23-125">As with the service implementation, the client must include the generated header or headers.</span></span>

``` syntax
#include "CalculatorProxyStub.h"
```

<span data-ttu-id="ccb23-126">Теперь клиентское приложение может создать и открыть прокси-сервер службы, чтобы начать обмен данными со службой калькулятора.</span><span class="sxs-lookup"><span data-stu-id="ccb23-126">Now, The client application can create and open a service proxy to begin communication with the calculator service.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
WS_STRING uri= WS_STRING_VALUE(L"http://localhost/example");
address.uri = uri;

if (FAILED (hr = WsCreateServiceProxy(WS_CHANNEL_TYPE_REQUEST, WS_HTTP_CHANNEL_BINDING, NULL, NULL, 0, &serviceProxy, error)))
    goto Error;

if (FAILED (hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error)))
    goto Error;
```

<span data-ttu-id="ccb23-127">Приложение может вызвать операцию добавления в службе калькулятора с помощью следующего кода:</span><span class="sxs-lookup"><span data-stu-id="ccb23-127">The application can call the Add operation on the calculator service with the following code:</span></span>

``` syntax
if (FAILED (hr = DefaultBinding_ICalculator_Add(serviceProxy, heap, 1, 2, &result, NULL, 0, NULL, error)))
    goto Error;
```

<span data-ttu-id="ccb23-128">Ознакомьтесь с примером кода в [хттпкалкулаторклиентексампле](httpcalculatorclientexample.md) для полной реализации службы калькулятора.</span><span class="sxs-lookup"><span data-stu-id="ccb23-128">Please refer to the code example at [HttpCalculatorClientExample](httpcalculatorclientexample.md) for full implementation of the calculator service.</span></span>

## <a name="service-model-components"></a><span data-ttu-id="ccb23-129">Компоненты модели службы</span><span class="sxs-lookup"><span data-stu-id="ccb23-129">Service Model Components</span></span>

<span data-ttu-id="ccb23-130">Взаимодействие отдельных компонентов модели службы ВВСАПИ в примере калькулятора выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ccb23-130">The interaction of the individual WWSAPI Service Model components within the Calculator example is as follows:</span></span>

-   <span data-ttu-id="ccb23-131">Клиент создает [прокси-сервер службы](service-proxy.md) и открывает его.</span><span class="sxs-lookup"><span data-stu-id="ccb23-131">The client creates a [service proxy](service-proxy.md) and opens it.</span></span>
-   <span data-ttu-id="ccb23-132">Клиент вызывает функцию добавления службы и передает прокси-сервер службы.</span><span class="sxs-lookup"><span data-stu-id="ccb23-132">The client calls the Add function of the service, and passes in the service proxy.</span></span>
-   <span data-ttu-id="ccb23-133">Сообщение сериализуется в соответствии с метаданными сериализации в заголовке и исходных файлах, созданных средством метаданных ([WsUtil.exe](web-service-compiler-tool.md)).</span><span class="sxs-lookup"><span data-stu-id="ccb23-133">The message is serialized according to the serialization metadata in the header and source files generated by the metadata tool ([WsUtil.exe](web-service-compiler-tool.md)).</span></span>
-   <span data-ttu-id="ccb23-134">Сообщение записывается в канал и передается по сети службе.</span><span class="sxs-lookup"><span data-stu-id="ccb23-134">The message is written to the channel and is transmitted over the network to the service.</span></span>
-   <span data-ttu-id="ccb23-135">На стороне сервера служба размещается внутри узла службы и имеет конечную точку, которая прослушивает контракт ICalculator.</span><span class="sxs-lookup"><span data-stu-id="ccb23-135">On the server side, the service is hosted inside a service host, and has an endpoint listening for the ICalculator contract.</span></span>
-   <span data-ttu-id="ccb23-136">Используя метаданные модели службы в заглушке, служба десериализует сообщение от клиента и отправляет его в заглушку.</span><span class="sxs-lookup"><span data-stu-id="ccb23-136">Using the Service Model metadata in the stub, the service deserializes the message from the client and dispatches it to the stub.</span></span>
-   <span data-ttu-id="ccb23-137">Служба на стороне сервера вызывает метод Add, передавая ему контекст операции.</span><span class="sxs-lookup"><span data-stu-id="ccb23-137">The server-side service calls the Add method, passing it the operation context.</span></span> <span data-ttu-id="ccb23-138">Этот контекст операции содержит ссылку на входящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="ccb23-138">This operation context contains the reference to the incoming message.</span></span>

![Схема, демонстрирующая взаимодействие отдельных компонентов модели службы ВВСАПИ.](images/servicemodellayout.png)

<span data-ttu-id="ccb23-140">Компоненты</span><span class="sxs-lookup"><span data-stu-id="ccb23-140">Components</span></span>

-   <span data-ttu-id="ccb23-141">[Узел службы](service-host.md): размещает службу.</span><span class="sxs-lookup"><span data-stu-id="ccb23-141">[Service host](service-host.md): Hosts a service.</span></span>
-   <span data-ttu-id="ccb23-142">[Прокси-сервер службы](service-proxy.md): определяет, как клиент взаимодействует со службой.</span><span class="sxs-lookup"><span data-stu-id="ccb23-142">[Service proxy](service-proxy.md): Defines how a client communicates with a service.</span></span>
-   <span data-ttu-id="ccb23-143">[Контекст](context.md): контейнер свойств, предназначенный для предоставления сведений о состоянии для операции службы.</span><span class="sxs-lookup"><span data-stu-id="ccb23-143">[Context](context.md): Property bag for making state-specific information available to a service operation.</span></span>
-   <span data-ttu-id="ccb23-144">[Контракт](contract.md): определение интерфейса службы.</span><span class="sxs-lookup"><span data-stu-id="ccb23-144">[Contract](contract.md): The interface definition of a service.</span></span> <span data-ttu-id="ccb23-145">Например, ICalculator представляет контракт для службы калькулятора в нашем примере кода.</span><span class="sxs-lookup"><span data-stu-id="ccb23-145">For example, ICalculator represents a contract for the calculator service in our example code.</span></span>
-   <span data-ttu-id="ccb23-146">[WsUtil.exe](web-service-compiler-tool.md): средство метаданных модели службы для создания прокси-серверов и заглушек.</span><span class="sxs-lookup"><span data-stu-id="ccb23-146">[WsUtil.exe](web-service-compiler-tool.md): The Service Model metadata tool for generating proxies and stubs.</span></span>

 

 




