---
title: Прокси-сервер службы
description: Прокси службы — это прокси-сервер на стороне клиента для службы.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Веб-службы прокси службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "105684732"
---
# <a name="service-proxy"></a><span data-ttu-id="64993-106">Прокси-сервер службы</span><span class="sxs-lookup"><span data-stu-id="64993-106">Service Proxy</span></span>

<span data-ttu-id="64993-107">Прокси службы — это прокси-сервер на стороне клиента для службы.</span><span class="sxs-lookup"><span data-stu-id="64993-107">A service proxy is the client side proxy for a service.</span></span> <span data-ttu-id="64993-108">Прокси-сервер службы позволяет приложениям отправлять и получать [сообщения](message.md) по [каналу](channel.md) в виде вызовов методов.</span><span class="sxs-lookup"><span data-stu-id="64993-108">The service proxy enables applications to send and receive [messages](message.md) over a [channel](channel.md) as method calls.</span></span>

<span data-ttu-id="64993-109">Прокси-серверы служб создаются по мере необходимости, открываются, используются для вызова службы и закрываются, когда они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="64993-109">Service proxies are created as needed, opened, used to call a service, and closed when no longer needed.</span></span> <span data-ttu-id="64993-110">Кроме того, приложение может повторно использовать прокси-сервер службы для многократного подключения к той же службе без затрат времени и ресурсов, необходимых для инитиалисинг прокси службы.</span><span class="sxs-lookup"><span data-stu-id="64993-110">Alternatively, an application may reuse a service proxy to connect repeatedly to the same service without the expenditure of time and resources required for initialising a service proxy more than once.</span></span> <span data-ttu-id="64993-111">На следующей схеме показана последовательность возможных состояний прокси-сервера службы и вызовов функций или событий, ведущих от одного состояния к другому.</span><span class="sxs-lookup"><span data-stu-id="64993-111">The following diagram illustrates the flow of the possible states of the service proxy and the function calls or events that lead from one state to another.</span></span>

![Схема, показывающая состояния прокси-сервера службы и вызовов функций или событий, ведущих от одного состояния к другому.](images/serviceproxystates.png)

<span data-ttu-id="64993-113">Эти состояния прокси-службы перечисляются в перечислении [**\_ \_ \_ состояния прокси-службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="64993-113">These service proxy states are enumerated in the [**WS\_SERVICE\_PROXY\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) enumeration.</span></span>

<span data-ttu-id="64993-114">Как показано на предыдущей схеме и следующем коде, прокси службы создается путем вызова функции [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="64993-114">As the preceding diagram and the following code illustrate, a service proxy is created by a call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span> <span data-ttu-id="64993-115">В качестве параметров для этого вызова ВВСАПИ предоставляет следующие перечисления:</span><span class="sxs-lookup"><span data-stu-id="64993-115">As parameters for this call, WWSAPI provides the following enumerations:</span></span>

-   [<span data-ttu-id="64993-116">**\_Тип канала \_ WS**</span><span class="sxs-lookup"><span data-stu-id="64993-116">**WS\_CHANNEL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [<span data-ttu-id="64993-117">**\_Привязка канала \_ WS**</span><span class="sxs-lookup"><span data-stu-id="64993-117">**WS\_CHANNEL\_BINDING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

<span data-ttu-id="64993-118">Он также принимает необязательные параметры, используя следующие типы данных:</span><span class="sxs-lookup"><span data-stu-id="64993-118">It also accepts optional parameters using the following data types:</span></span>

-   [<span data-ttu-id="64993-119">**\_идентификатор свойства прокси-сервера WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64993-119">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [<span data-ttu-id="64993-120">**\_Описание безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="64993-120">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

<span data-ttu-id="64993-121">После создания прокси-сервера службы функция **вскреатесервицепрокси** возвращает ссылку на прокси-сервер службы [WS \_ \_ -proxy](ws-service-proxy.md)с помощью параметра out.</span><span class="sxs-lookup"><span data-stu-id="64993-121">When the service proxy has been created, the **WsCreateServiceProxy** function returns a reference to the service proxy, [WS\_SERVICE\_PROXY](ws-service-proxy.md), through an out parameter.</span></span>

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

<span data-ttu-id="64993-122">После создания прокси-сервера службы приложение может открыть прокси-сервер службы для взаимодействия со службой, вызвав функцию [**всопенсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , передав структуру [**адресов**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) , содержащую сетевой адрес конечной точки службы для подключения.</span><span class="sxs-lookup"><span data-stu-id="64993-122">When the service proxy has been created, the application can open the service proxy for communication to a service by calling the [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) function, passing an [**address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure containing the network address of the service endpoint to connect to.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

<span data-ttu-id="64993-123">При открытии прокси-сервера службы приложение может использовать его для выполнения вызовов к службе.</span><span class="sxs-lookup"><span data-stu-id="64993-123">When the service proxy has been opened, the application can use it to make calls to the service.</span></span>

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

<span data-ttu-id="64993-124">Если приложению больше не требуется прокси-сервер службы, он закрывает прокси-сервер службы, вызывая функцию [**всклосесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="64993-124">When the application no longer needs the service proxy, it closes the service proxy by calling the [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) function.</span></span> <span data-ttu-id="64993-125">Он также освобождает связанную память путем вызова [**всфрисервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="64993-125">It also frees the associated memory by calling [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span></span>

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a><span data-ttu-id="64993-126">Повторное использование прокси-сервера службы</span><span class="sxs-lookup"><span data-stu-id="64993-126">Reusing the Service Proxy</span></span>

<span data-ttu-id="64993-127">Кроме того, после вызова [**всклосесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) приложение может повторно использовать прокси-сервер службы, вызвав функцию [**всресетсервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="64993-127">Alternatively, after calling [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) an application can reuse the service proxy by calling the [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) function.</span></span>

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

<span data-ttu-id="64993-128">Дополнительные сведения о том, как прокси-серверы служб используются в разных контекстах, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="64993-128">For more information on how service proxies are used in different contexts, see the following topics:</span></span>

-   [<span data-ttu-id="64993-129">Прокси-сервер службы и сеансы</span><span class="sxs-lookup"><span data-stu-id="64993-129">Service Proxy and Sessions</span></span>](service-proxy-and-sessions.md)
-   [<span data-ttu-id="64993-130">Операция службы</span><span class="sxs-lookup"><span data-stu-id="64993-130">Service Operation</span></span>](service-operation.md)
-   [<span data-ttu-id="64993-131">Операции службы на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="64993-131">Client Side Service Operations</span></span>](client-side-service-operations.md)
-   [<span data-ttu-id="64993-132">хттпкалкулаторклиентексампле</span><span class="sxs-lookup"><span data-stu-id="64993-132">HttpCalculatorClientExample</span></span>](httpcalculatorclientexample.md)

### <a name="security"></a><span data-ttu-id="64993-133">Безопасность</span><span class="sxs-lookup"><span data-stu-id="64993-133">Security</span></span>

<span data-ttu-id="64993-134">При использовании API прокси-сервера службы ВВСАПИ следует внимательно отметить следующие аспекты проектирования приложений:</span><span class="sxs-lookup"><span data-stu-id="64993-134">Following application design considerations should be carefully noted when you use the WWSAPI service proxy API:</span></span>

-   <span data-ttu-id="64993-135">Прокси-сервер службы не будет выполнять проверку данных после проверки базового профиля 2,0 и сериализации XML.</span><span class="sxs-lookup"><span data-stu-id="64993-135">The service proxy will not perform any validation of the data beyond Basic Profile 2.0 validation and XML serialization.</span></span> <span data-ttu-id="64993-136">Это приложение отвечает за проверку данных, содержащихся в параметрах, которые они получают обратно в рамках вызова.</span><span class="sxs-lookup"><span data-stu-id="64993-136">It is the responsibility of the application to validate the data contained in the parameters it receives back as part of the call.</span></span>
-   <span data-ttu-id="64993-137">Настройка максимального количества ожидающих вызовов на прокси-сервере службы с помощью значения перечисления [**\_ \_ \_ идентификатора свойства прокси-**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) сервера WS **\_ Максимальное число \_ \_ \_ ожидающих \_ вызовов**, обеспечивающее защиту от сервера, на котором выполняется задержка.</span><span class="sxs-lookup"><span data-stu-id="64993-137">Configuring the maximum number of pending calls on the service proxy, by using the [**WS\_PROXY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) enumeration value **WS\_PROXY\_PROPERTY\_MAX\_PENDING\_CALLS**, provides protection against a slow running server.</span></span> <span data-ttu-id="64993-138">Максимальное значение по умолчанию — 100.</span><span class="sxs-lookup"><span data-stu-id="64993-138">The default maximum is 100.</span></span> <span data-ttu-id="64993-139">Приложения должны соблюдать осторожность при изменении значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64993-139">Applications must be careful in modifying the defaults.</span></span>
-   <span data-ttu-id="64993-140">Прокси-сервер службы не предоставляет гарантий безопасности, кроме тех, которые указаны в структуре [**\_ \_ описания безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , используемой для взаимодействия с сервером.</span><span class="sxs-lookup"><span data-stu-id="64993-140">The service proxy provides no security guarantees beyond those specified in the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure used to communicate with the server.</span></span>
-   <span data-ttu-id="64993-141">Следите за внесением изменений в [сообщения](message.md) и [каналы](channel.md) по умолчанию на прокси-сервере службы.</span><span class="sxs-lookup"><span data-stu-id="64993-141">Take care when you modifying [message](message.md) and [channel](channel.md) defaults on the service proxy.</span></span> <span data-ttu-id="64993-142">Прежде чем изменять какие либо связанные свойства, прочтите вопросы безопасности, связанные с сообщениями и каналами.</span><span class="sxs-lookup"><span data-stu-id="64993-142">Read the security considerations associated with messages and channels before you modify any of the related properties.</span></span>
-   <span data-ttu-id="64993-143">Прокси-сервер службы шифрует все учетные данные, которые он хранит в памяти.</span><span class="sxs-lookup"><span data-stu-id="64993-143">Service proxy encrypts all credentials that it keeps in memory.</span></span>

<span data-ttu-id="64993-144">Следующие элементы API связаны с прокси-серверами служб.</span><span class="sxs-lookup"><span data-stu-id="64993-144">The following API elements relate to service proxies.</span></span>

| <span data-ttu-id="64993-145">Обратный вызов</span><span class="sxs-lookup"><span data-stu-id="64993-145">Callback</span></span>                                                          | <span data-ttu-id="64993-146">Описание</span><span class="sxs-lookup"><span data-stu-id="64993-146">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64993-147">**\_ \_ обратный вызов сообщения прокси-сервера WS \_**</span><span class="sxs-lookup"><span data-stu-id="64993-147">**WS\_PROXY\_MESSAGE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | <span data-ttu-id="64993-148">Вызывается при отправке заголовков входного сообщения или при получении только тех выходных заголовков сообщений.</span><span class="sxs-lookup"><span data-stu-id="64993-148">Invoked when the headers of the input message are about to be sent through or when an output message headers are just received.</span></span> |



 



| <span data-ttu-id="64993-149">Перечисление</span><span class="sxs-lookup"><span data-stu-id="64993-149">Enumeration</span></span>                                                 | <span data-ttu-id="64993-150">Описание</span><span class="sxs-lookup"><span data-stu-id="64993-150">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64993-151">**\_ \_ идентификатор свойства вызова \_ WS**</span><span class="sxs-lookup"><span data-stu-id="64993-151">**WS\_CALL\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | <span data-ttu-id="64993-152">Перечисляет необязательные параметры для настройки вызова в операции службы на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="64993-152">Enumerates optional parameters for configuring a call on a client side service operation.</span></span> |
| [<span data-ttu-id="64993-153">**\_идентификатор свойства прокси-сервера WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64993-153">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | <span data-ttu-id="64993-154">Перечисляет необязательные параметры для настройки прокси-сервера службы.</span><span class="sxs-lookup"><span data-stu-id="64993-154">Enumerates optional parameters for configuring the service proxy.</span></span>                         |
| [<span data-ttu-id="64993-155">**\_ \_ состояние прокси-сервера службы WS \_**</span><span class="sxs-lookup"><span data-stu-id="64993-155">**WS\_SERVICE\_PROXY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | <span data-ttu-id="64993-156">Состояние прокси-сервера службы.</span><span class="sxs-lookup"><span data-stu-id="64993-156">The state of the service proxy.</span></span>                                                           |



 



| <span data-ttu-id="64993-157">Функция</span><span class="sxs-lookup"><span data-stu-id="64993-157">Function</span></span>                                                       | <span data-ttu-id="64993-158">Описание</span><span class="sxs-lookup"><span data-stu-id="64993-158">Description</span></span>                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="64993-159">**всабандонкалл**</span><span class="sxs-lookup"><span data-stu-id="64993-159">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | <span data-ttu-id="64993-160">Прерывает указанный вызов для указанного прокси-сервера службы.</span><span class="sxs-lookup"><span data-stu-id="64993-160">Abandons a specified call on a specified service proxy.</span></span>                           |
| [<span data-ttu-id="64993-161">**всабортсервицепрокси**</span><span class="sxs-lookup"><span data-stu-id="64993-161">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | <span data-ttu-id="64993-162">Отменяет все ожидающие входные и выходные данные для указанного прокси-сервера службы.</span><span class="sxs-lookup"><span data-stu-id="64993-162">Cancels all pending input and output on a specified service proxy.</span></span>                |
| [<span data-ttu-id="64993-163">**вскалл**</span><span class="sxs-lookup"><span data-stu-id="64993-163">**WsCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | <span data-ttu-id="64993-164">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="64993-164">Internal only.</span></span> <span data-ttu-id="64993-165">Сериализует аргументы в сообщение и отправляет их по каналу.</span><span class="sxs-lookup"><span data-stu-id="64993-165">Serializes arguments into a message and sends it over the channel.</span></span> |
| [<span data-ttu-id="64993-166">**всклосесервицепрокси**</span><span class="sxs-lookup"><span data-stu-id="64993-166">**WsCloseServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | <span data-ttu-id="64993-167">Закрывает прокси-сервер службы для связи.</span><span class="sxs-lookup"><span data-stu-id="64993-167">Closes a service proxy for communication.</span></span>                                         |
| [<span data-ttu-id="64993-168">**вскреатесервицепрокси**</span><span class="sxs-lookup"><span data-stu-id="64993-168">**WsCreateServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | <span data-ttu-id="64993-169">Создает прокси-сервер службы.</span><span class="sxs-lookup"><span data-stu-id="64993-169">Creates a service proxy.</span></span>                                                          |
| [<span data-ttu-id="64993-170">**всфрисервицепрокси**</span><span class="sxs-lookup"><span data-stu-id="64993-170">**WsFreeServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | <span data-ttu-id="64993-171">Освобождает память, связанную с прокси-сервером службы.</span><span class="sxs-lookup"><span data-stu-id="64993-171">Releases the memory associated with a service proxy.</span></span>                              |
| [<span data-ttu-id="64993-172">**всжетсервицепроксипроперти**</span><span class="sxs-lookup"><span data-stu-id="64993-172">**WsGetServiceProxyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | <span data-ttu-id="64993-173">Извлекает указанное свойство прокси-сервера службы.</span><span class="sxs-lookup"><span data-stu-id="64993-173">Retrieves a specified service proxy property.</span></span>                                     |
| [<span data-ttu-id="64993-174">**всопенсервицепрокси**</span><span class="sxs-lookup"><span data-stu-id="64993-174">**WsOpenServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | <span data-ttu-id="64993-175">Открывает прокси-сервер службы для конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="64993-175">Opens a service proxy to a service endpoint.</span></span>                                      |
| [<span data-ttu-id="64993-176">**всресетсервицепрокси**</span><span class="sxs-lookup"><span data-stu-id="64993-176">**WsResetServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | <span data-ttu-id="64993-177">Сбрасывает прокси-сервер службы.</span><span class="sxs-lookup"><span data-stu-id="64993-177">Resets service proxy.</span></span>                                                             |



 



| <span data-ttu-id="64993-178">Дескриптор</span><span class="sxs-lookup"><span data-stu-id="64993-178">Handle</span></span>                                     | <span data-ttu-id="64993-179">Описание</span><span class="sxs-lookup"><span data-stu-id="64993-179">Description</span></span>                                       |
|--------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="64993-180">\_ \_ прокси-сервер службы WS</span><span class="sxs-lookup"><span data-stu-id="64993-180">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md) | <span data-ttu-id="64993-181">Непрозрачный тип, используемый для ссылки на прокси-сервер службы.</span><span class="sxs-lookup"><span data-stu-id="64993-181">An opaque type used to reference a service proxy.</span></span> |



 



| <span data-ttu-id="64993-182">Структура</span><span class="sxs-lookup"><span data-stu-id="64993-182">Structure</span></span>                                         | <span data-ttu-id="64993-183">Описание</span><span class="sxs-lookup"><span data-stu-id="64993-183">Description</span></span>                 |
|---------------------------------------------------|-----------------------------|
| [<span data-ttu-id="64993-184">**\_свойство Call вызова WS \_**</span><span class="sxs-lookup"><span data-stu-id="64993-184">**WS\_CALL\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | <span data-ttu-id="64993-185">Задает свойство Call.</span><span class="sxs-lookup"><span data-stu-id="64993-185">Specifies a call property.</span></span>  |
| <span data-ttu-id="64993-186">[**Служба WS \_ \_свойство прокси-сервера**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span><span class="sxs-lookup"><span data-stu-id="64993-186">[**WS\_PROXY\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span></span> | <span data-ttu-id="64993-187">Задает свойство прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="64993-187">Specifies a proxy property.</span></span> |



 

 

 




