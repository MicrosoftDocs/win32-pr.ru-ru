---
title: Узел службы
description: Узел службы — это среда выполнения для размещения службы в рамках процесса.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Веб-службы узла службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "105703421"
---
# <a name="service-host"></a><span data-ttu-id="d3325-106">Узел службы</span><span class="sxs-lookup"><span data-stu-id="d3325-106">Service Host</span></span>

<span data-ttu-id="d3325-107">Узел службы — это среда выполнения для размещения службы в рамках процесса.</span><span class="sxs-lookup"><span data-stu-id="d3325-107">The service host is the runtime environment for hosting a service within a process.</span></span>


<span data-ttu-id="d3325-108">Служба может настроить одну или несколько конечных точек внутри узла службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-108">A service can configure one or more endpoints inside a service host.</span></span>

![Схема, показывающая структуру узла службы, содержащего конечную точку службы.](images/servicehost.png)

## <a name="creating-a-service-host"></a><span data-ttu-id="d3325-110">Создание узла службы</span><span class="sxs-lookup"><span data-stu-id="d3325-110">Creating a service host</span></span>

<span data-ttu-id="d3325-111">Прежде чем создавать узел службы, службе необходимо определить ее конечные точки.</span><span class="sxs-lookup"><span data-stu-id="d3325-111">Before creating a service host, a service needs to define its endpoints.</span></span> <span data-ttu-id="d3325-112">Конечная точка в узле службы указывается в структуре [**\_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) и определяется следующими сведениями:</span><span class="sxs-lookup"><span data-stu-id="d3325-112">An endpoint in service host is specified in the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structure and it is defined by the following information:</span></span>

-   <span data-ttu-id="d3325-113">Адрес, представляющий собой физический универсальный код ресурса (URI), на котором будет размещена служба.</span><span class="sxs-lookup"><span data-stu-id="d3325-113">An address, which is the physical URI on which the service will be hosted.</span></span>
-   <span data-ttu-id="d3325-114">Структура [**\_ \_ типа канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , указывающая тип базового канала для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d3325-114">A [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) structure that specifies the type of the underlying channel for the endpoint.</span></span>
-   <span data-ttu-id="d3325-115">Структура [**\_ \_ привязки канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , указывающая привязку канала.</span><span class="sxs-lookup"><span data-stu-id="d3325-115">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) structure that specifies the binding of the channel.</span></span>
-   <span data-ttu-id="d3325-116">Структура [**\_ \_ описания безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , содержащая описание безопасности для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d3325-116">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure that contains the security description for the endpoint.</span></span>
-   <span data-ttu-id="d3325-117">Структура [**\_ \_ контракта службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) , представляющая [контракт службы](contract.md) для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d3325-117">A [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure that represents the [service contract](contract.md) for the endpoint.</span></span>
-   <span data-ttu-id="d3325-118">Структура [**\_ \_ \_ обратного вызова безопасности службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) , указывающая функцию обратного вызова авторизации для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d3325-118">A [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) structure that specifies an authorization callback function for the endpoint.</span></span>
-   <span data-ttu-id="d3325-119">Структура [**\_ \_ \_ свойств конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) , которая содержит массив свойств конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-119">A [**WS\_SERVICE\_ENDPOINT\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) structure that contains an array of service endpoint properties.</span></span>

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

<span data-ttu-id="d3325-120">Для SOAP через UDP поддерживаются только односторонние контракты, представленные [**\_ \_ \_ привязкой канала WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) в перечислении **\_ \_ привязки канала WS** .</span><span class="sxs-lookup"><span data-stu-id="d3325-120">Only one-way contracts are supported for SOAP over UDP, represented by [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in the **WS\_CHANNEL\_BINDING** enumeration.</span></span>

<span data-ttu-id="d3325-121">После определения конечной точки ее можно передать в функцию [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , которая принимает массив указателей на структуры [**\_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .</span><span class="sxs-lookup"><span data-stu-id="d3325-121">After an endpoint is defined, it can be passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function, which takes an array of pointers to [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures.</span></span>

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

<span data-ttu-id="d3325-122">Приложение может дополнительно предоставить массив [**свойств службы**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) для [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) для настройки пользовательских параметров на узле службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-122">An application can optionally provide an array of [**service properties**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) to [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) to configure custom settings on the service host.</span></span>

<span data-ttu-id="d3325-123">Приложение открывает узел службы, чтобы начать принимать клиентские запросы.</span><span class="sxs-lookup"><span data-stu-id="d3325-123">An application opens the service host to start accepting client requests.</span></span>

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="d3325-124">После открытия узла службы приложение может закрыть его, если для него не требуется никаких операций.</span><span class="sxs-lookup"><span data-stu-id="d3325-124">After opening the service host, the application can close it if there are no more operations that require it.</span></span> <span data-ttu-id="d3325-125">Обратите внимание, что это не освобождает ресурсы и может быть повторно открыто при последующем вызове [**всресетсервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span><span class="sxs-lookup"><span data-stu-id="d3325-125">Note that this does not release its resources, and that it can be reopened with a subsequent call to [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span></span>

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="d3325-126">После закрытия узла службы приложение может сбросить узел службы для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="d3325-126">After closing the service host, an application may reset the service host for reuse.</span></span>

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

<span data-ttu-id="d3325-127">Когда приложение выполняется с помощью узла службы, можно освободить ресурсы, связанные с узлом службы, вызвав функцию [**всфрисервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) .</span><span class="sxs-lookup"><span data-stu-id="d3325-127">When the application is done with the service host it can free the resources associated with the service host by calling the [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) function.</span></span> <span data-ttu-id="d3325-128">Обратите внимание, что перед вызовом этой функции необходимо вызвать [**всклосесервицехост**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) .</span><span class="sxs-lookup"><span data-stu-id="d3325-128">Note that [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) must be called before calling this function.</span></span>

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

<span data-ttu-id="d3325-129">Сведения о присоединении пользовательского состояния к узлу службы см. в разделе [состояние узла пользователя](user-host-state.md) .</span><span class="sxs-lookup"><span data-stu-id="d3325-129">For information on attaching a custom state to the service host, see [User Host State](user-host-state.md)</span></span>

<span data-ttu-id="d3325-130">Сведения об авторизации в узле службы для данной конечной точки см. в разделе [Авторизация служб](service-authorization.md).</span><span class="sxs-lookup"><span data-stu-id="d3325-130">For information on authorization in a service host for a given endpoint, see [Service Authorization](service-authorization.md).</span></span>

<span data-ttu-id="d3325-131">Сведения о реализации операций службы и контрактов служб для службы см. в разделах [Сервис Operations](server-side-service-operations.md) and [Service Contract](contract.md).</span><span class="sxs-lookup"><span data-stu-id="d3325-131">For iinformation on implementing service operations and service contracts for a service, see the [service operations](server-side-service-operations.md) and [service contract](contract.md)topics.</span></span>

## <a name="security"></a><span data-ttu-id="d3325-132">Безопасность</span><span class="sxs-lookup"><span data-stu-id="d3325-132">Security</span></span>

<span data-ttu-id="d3325-133">Приложение может использовать свойства для контроля за объемом ресурсов, выделяемых узлом службы от имени приложения:</span><span class="sxs-lookup"><span data-stu-id="d3325-133">An application can use the followin properties to control the amount of resources the service host allocates on behalf of the application:</span></span>

-   <span data-ttu-id="d3325-134">[**Служба WS \_ \_ \_ \_ Максимальное число \_ \_ принимаемых каналов для свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id):</span><span class="sxs-lookup"><span data-stu-id="d3325-134">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_ACCEPTING\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="d3325-135">[**Служба WS \_ \_ \_ \_ Максимальная \_ степень параллелизма для свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)</span><span class="sxs-lookup"><span data-stu-id="d3325-135">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CONCURRENCY**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="d3325-136">[**Служба WS \_ \_ \_ \_ Максимальное число \_ каналов для свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id):</span><span class="sxs-lookup"><span data-stu-id="d3325-136">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="d3325-137">[**Служба WS \_ \_ \_ \_ \_ \_ максимальный \_ Размер кучи тела свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)</span><span class="sxs-lookup"><span data-stu-id="d3325-137">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_BODY\_HEAP\_MAX\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="d3325-138">[**Служба WS \_ \_свойство конечной точки службы: \_ \_ максимальный \_ \_ \_ размер пула вызовов**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)</span><span class="sxs-lookup"><span data-stu-id="d3325-138">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CALL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="d3325-139">[**Служба WS \_ \_ \_ \_ Максимальное значение \_ \_ \_ размера пула каналов для свойства конечной точки службы**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span><span class="sxs-lookup"><span data-stu-id="d3325-139">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNEL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span></span>

<span data-ttu-id="d3325-140">Для каждого из этих свойств выбираются безопасные значения по умолчанию. приложение должно быть внимательным, если нужно изменить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="d3325-140">Secure defaults are chosen for each of these properties, an application must be careful if it wishes to modify these properties.</span></span> <span data-ttu-id="d3325-141">Помимо указанных выше свойств, свойства [канала](channel.md), [прослушивателя](listener.md) и сообщения, относящиеся к [сообщению](message.md) , также могут быть изменены приложением.</span><span class="sxs-lookup"><span data-stu-id="d3325-141">Beyond the above-mentioned properties, [channel](channel.md), [listener](listener.md) and [message](message.md) specific properties can also be modified by the application.</span></span> <span data-ttu-id="d3325-142">Прежде чем изменять эти параметры, ознакомьтесь с вопросами безопасности этих компонентов.</span><span class="sxs-lookup"><span data-stu-id="d3325-142">Refer to the security considerations of these components before modifying any of these settings.</span></span>

<span data-ttu-id="d3325-143">Кроме того, при использовании API узла службы ВВСАПИ необходимо тщательно оценить следующие аспекты разработки приложений:</span><span class="sxs-lookup"><span data-stu-id="d3325-143">In addition, the following application design considerations should be carefully evaluated when using WWSAPI service host API:</span></span>

-   <span data-ttu-id="d3325-144">При использовании MEX приложения должны быть осторожными, чтобы не раскрывать какие бы то ни было конфиденциальные данные.</span><span class="sxs-lookup"><span data-stu-id="d3325-144">When using MEX, applications should be careful not to disclose any sensitive data.</span></span> <span data-ttu-id="d3325-145">Как минимум, если характер данных, предоставляемых через MEX, является конфиденциальным, приложения могут настроить конечную точку обмена метаданными с безопасной привязкой, которая требует проверки подлинности по крайней мере и реализуют авторизацию как часть конечной точки с помощью [**\_ \_ \_ обратного вызова безопасности службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="d3325-145">As a mitigation, if the nature of the data being exposed through MEX is sensitive, applications may choose to configure the MEX endpoint with a secure binding requiring authentication at the very least and implement authorization as part of the endpoint using the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="d3325-146">По умолчанию подробные сведения об ошибках с помощью ошибок отключены для узла службы с помощью свойства [**\_ \_ \_ \_ утечки ошибки свойства службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="d3325-146">By default rich error information through faults is disabled on service host by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span> <span data-ttu-id="d3325-147">Приложение может отсылать обширные сведения об ошибках в рамках сбоя.</span><span class="sxs-lookup"><span data-stu-id="d3325-147">It is upon the discretion of the application to send rich error information as part of the fault.</span></span> <span data-ttu-id="d3325-148">Однако это может привести к раскрытию информации, поэтому рекомендуется изменить этот параметр только для сценариев отладки.</span><span class="sxs-lookup"><span data-stu-id="d3325-148">However, this can result in information disclosure and thus it is recommended that this setting is only changed for debugging scenarios.</span></span>
-   <span data-ttu-id="d3325-149">Помимо проверки, выполненной для базового профиля 2,0 и XML-сериализации, узел службы не выполняет проверку содержимого данных, полученного в составе параметров операции службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-149">Beyond validation performed for Basic Profile 2.0 and XML serialization, service host performs no validation on the data content received as part of service operation parameters.</span></span> <span data-ttu-id="d3325-150">Приложение обязано выполнять все проверки параметров самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="d3325-150">It is the responsibility of the application to perform all parameter validations on its own.</span></span>
-   <span data-ttu-id="d3325-151">Авторизация не реализована в составе узла службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-151">Authorization is not implemented as part of service host.</span></span> <span data-ttu-id="d3325-152">Однако приложения могут реализовать собственную схему авторизации, используя [**\_ \_ Описание безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) и [**\_ \_ \_ обратный вызов безопасности службы WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="d3325-152">However, applications can implement their own authorization scheme using [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) and the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="d3325-153">Приложение обязано использовать для своей конечной точки безопасные привязки.</span><span class="sxs-lookup"><span data-stu-id="d3325-153">It is the responsibility of the application to use secure bindings on its endpoint.</span></span> <span data-ttu-id="d3325-154">Узел службы не обеспечивает никакой безопасности, помимо того, что настроено в конечной точке.</span><span class="sxs-lookup"><span data-stu-id="d3325-154">Service host does not provide any security beyond what is configured on the endpoint.</span></span>

<span data-ttu-id="d3325-155">С узлом службы используются следующие элементы API.</span><span class="sxs-lookup"><span data-stu-id="d3325-155">The following API elements are used with the service host.</span></span>

| <span data-ttu-id="d3325-156">Обратный вызов</span><span class="sxs-lookup"><span data-stu-id="d3325-156">Callback</span></span>                                                                             | <span data-ttu-id="d3325-157">Описание</span><span class="sxs-lookup"><span data-stu-id="d3325-157">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="d3325-158">**\_ \_ \_ обратный вызов для приема канала службы \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d3325-158">**WS\_SERVICE\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | <span data-ttu-id="d3325-159">Вызывается, когда узел службы принимает канал на прослушиватель конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d3325-159">Invoked when a channel is accepted on an endpoint listener by the service host.</span></span> |
| [<span data-ttu-id="d3325-160">**\_ \_ \_ обратный вызов для закрытия канала службы \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d3325-160">**WS\_SERVICE\_CLOSE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | <span data-ttu-id="d3325-161">Вызывается, когда канал закрывается или прерывается в конечной точке.</span><span class="sxs-lookup"><span data-stu-id="d3325-161">Invoked when a channel is closed or aborted on an endpoint.</span></span>                     |



 



| <span data-ttu-id="d3325-162">Перечисление</span><span class="sxs-lookup"><span data-stu-id="d3325-162">Enumeration</span></span>                                                                    | <span data-ttu-id="d3325-163">Описание</span><span class="sxs-lookup"><span data-stu-id="d3325-163">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3325-164">**\_ \_ идентификатор свойства конечной точки службы \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="d3325-164">**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | <span data-ttu-id="d3325-165">Необязательные параметры для [**настройки \_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="d3325-165">Optional parameters for configuring a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span> |
| [<span data-ttu-id="d3325-166">**\_ \_ состояние узла службы \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d3325-166">**WS\_SERVICE\_HOST\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | <span data-ttu-id="d3325-167">Состояния, в которых может находиться узел службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-167">The states that a service host can be in.</span></span>                                                   |
| [<span data-ttu-id="d3325-168">**\_ \_ идентификатор свойства службы \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d3325-168">**WS\_SERVICE\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | <span data-ttu-id="d3325-169">Необязательные параметры для настройки узла службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-169">Optional parameters for configuring the service host.</span></span>                                       |



 



| <span data-ttu-id="d3325-170">Функция</span><span class="sxs-lookup"><span data-stu-id="d3325-170">Function</span></span>                                                     | <span data-ttu-id="d3325-171">Описание</span><span class="sxs-lookup"><span data-stu-id="d3325-171">Description</span></span>                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3325-172">**всабортсервицехост**</span><span class="sxs-lookup"><span data-stu-id="d3325-172">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | <span data-ttu-id="d3325-173">Прерывает и прекращает выполнение текущих операций на узле службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-173">Interrupts and discontinues current operations on the service host.</span></span>                          |
| [<span data-ttu-id="d3325-174">**всклосесервицехост**</span><span class="sxs-lookup"><span data-stu-id="d3325-174">**WsCloseServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | <span data-ttu-id="d3325-175">Закрывает все прослушиватели, чтобы новые каналы не принимались с клиента.</span><span class="sxs-lookup"><span data-stu-id="d3325-175">Closes all listeners so that no new channels are accepted from the client.</span></span>                   |
| [<span data-ttu-id="d3325-176">**WsCreateServiceHost**</span><span class="sxs-lookup"><span data-stu-id="d3325-176">**WsCreateServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | <span data-ttu-id="d3325-177">Создает узел службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-177">Creates a service host.</span></span>                                                                      |
| [<span data-ttu-id="d3325-178">**всфрисервицехост**</span><span class="sxs-lookup"><span data-stu-id="d3325-178">**WsFreeServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | <span data-ttu-id="d3325-179">Освобождает память, связанную с объектом узла службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-179">Releases the memory associated with a service host object.</span></span>                                   |
| [<span data-ttu-id="d3325-180">**всжетсервицехостпроперти**</span><span class="sxs-lookup"><span data-stu-id="d3325-180">**WsGetServiceHostProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | <span data-ttu-id="d3325-181">Извлекает указанное свойство узла службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-181">Retrieves a specified Service Host property.</span></span>                                                 |
| [<span data-ttu-id="d3325-182">**всопенсервицехост**</span><span class="sxs-lookup"><span data-stu-id="d3325-182">**WsOpenServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | <span data-ttu-id="d3325-183">Открывает узел службы для взаимодействия и запускает прослушиватели на всех конечных точках.</span><span class="sxs-lookup"><span data-stu-id="d3325-183">Opens a service host for communication and starts the listeners on all the endpoints.</span></span>        |
| [<span data-ttu-id="d3325-184">**всресетсервицехост**</span><span class="sxs-lookup"><span data-stu-id="d3325-184">**WsResetServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | <span data-ttu-id="d3325-185">Сбрасывает узел службы для повторного использования и сбрасывает базовый канал и прослушиватели для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="d3325-185">Resets the service host for reuse and resets the underlying channel and listeners for reuse.</span></span> |



 



| <span data-ttu-id="d3325-186">Дескриптор</span><span class="sxs-lookup"><span data-stu-id="d3325-186">Handle</span></span>                                       | <span data-ttu-id="d3325-187">Описание</span><span class="sxs-lookup"><span data-stu-id="d3325-187">Description</span></span>                                      |
|----------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="d3325-188">**\_узел службы \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d3325-188">**WS\_SERVICE\_HOST**</span></span>](ws-service-host.md) | <span data-ttu-id="d3325-189">Непрозрачный тип, используемый для ссылки на узел службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-189">An opaque type used to reference a service host.</span></span> |



 



| <span data-ttu-id="d3325-190">Структура</span><span class="sxs-lookup"><span data-stu-id="d3325-190">Structure</span></span>                                                                              | <span data-ttu-id="d3325-191">Описание</span><span class="sxs-lookup"><span data-stu-id="d3325-191">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="d3325-192">**\_ \_ Конечная точка службы WS**</span><span class="sxs-lookup"><span data-stu-id="d3325-192">**WS\_SERVICE\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | <span data-ttu-id="d3325-193">Представляет отдельную конечную точку на узле службы.</span><span class="sxs-lookup"><span data-stu-id="d3325-193">Represents an individual endpoint on a service host.</span></span>                            |
| [<span data-ttu-id="d3325-194">**\_ \_ свойство конечной точки службы WS \_**</span><span class="sxs-lookup"><span data-stu-id="d3325-194">**WS\_SERVICE\_ENDPOINT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | <span data-ttu-id="d3325-195">Задает зависящий от службы параметр.</span><span class="sxs-lookup"><span data-stu-id="d3325-195">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="d3325-196">**\_свойство службы \_ WS**</span><span class="sxs-lookup"><span data-stu-id="d3325-196">**WS\_SERVICE\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | <span data-ttu-id="d3325-197">Задает зависящий от службы параметр.</span><span class="sxs-lookup"><span data-stu-id="d3325-197">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="d3325-198">**\_ \_ \_ обратный вызов Accept для свойства службы WS \_**</span><span class="sxs-lookup"><span data-stu-id="d3325-198">**WS\_SERVICE\_PROPERTY\_ACCEPT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | <span data-ttu-id="d3325-199">Указывает обратный вызов, который вызывается, когда канал успешно принят.</span><span class="sxs-lookup"><span data-stu-id="d3325-199">Specifies the callback which is called when a channel is successfully accepted.</span></span> |
| [<span data-ttu-id="d3325-200">**\_ \_ \_ обратный вызов закрытия свойства службы WS \_**</span><span class="sxs-lookup"><span data-stu-id="d3325-200">**WS\_SERVICE\_PROPERTY\_CLOSE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | <span data-ttu-id="d3325-201">Указывает обратный вызов, который вызывается при закрытии канала.</span><span class="sxs-lookup"><span data-stu-id="d3325-201">Specifies the callback which is called when a channel is about to be closed.</span></span>    |



 

 

 




