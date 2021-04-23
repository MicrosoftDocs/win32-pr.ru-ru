---
title: Операции службы на стороне клиента
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: 'Дополнительные сведения: операции службы на стороне клиента'
keywords:
- Службы на стороне клиента веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd00bfbd832db12a722363bf5b1af8f7298345
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265429"
---
# <a name="client-side-service-operations"></a><span data-ttu-id="d347a-106">Операции службы на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="d347a-106">Client-side Service Operations</span></span>

<span data-ttu-id="d347a-107">Ниже приведена структура операции службы на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="d347a-107">The following is the layout of a client-side service operation:</span></span>

-   <span data-ttu-id="d347a-108">[Служба WS \_ \_Прокси-сервер службы](ws-service-proxy.md) \* serviceProxy: [прокси-сервер службы](service-proxy.md) для вызова.</span><span class="sxs-lookup"><span data-stu-id="d347a-108">[WS\_SERVICE\_PROXY](ws-service-proxy.md)\* serviceProxy: The [service proxy](service-proxy.md) for the call.</span></span>
-   <span data-ttu-id="d347a-109">[Служба WS \_ Куча КУЧИ](ws-heap.md) \* . Обязательная куча, используемая для сериализации тела и десериализации [ \_ сообщения WS](ws-message.md).</span><span class="sxs-lookup"><span data-stu-id="d347a-109">[WS\_HEAP](ws-heap.md)\* heap: A required heap used for body serialization and deserialization of the [WS\_MESSAGE](ws-message.md).</span></span>
-   <span data-ttu-id="d347a-110">Параметры операций службы: параметры, относящиеся к операции службы.</span><span class="sxs-lookup"><span data-stu-id="d347a-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="d347a-111">[**Вызовите свойства и их количество**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): массив свойств Call.</span><span class="sxs-lookup"><span data-stu-id="d347a-111">[**Call Properties and their count**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): An array of call properties.</span></span>
-   <span data-ttu-id="d347a-112">Число свойств [**вызова**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : количество свойств вызова.</span><span class="sxs-lookup"><span data-stu-id="d347a-112">[**Call**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) property count: The count of call properties.</span></span>
-   <span data-ttu-id="d347a-113">[**Служба WS \_ АСИНХРОНный \_ контекст**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Асинкконтекст: асинхронный контекст для асинхронного исполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="d347a-113">[**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: Async context for executing the call asynchronously.</span></span>
-   <span data-ttu-id="d347a-114">[Служба WS \_ Ошибка:](ws-error.md) расширенный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="d347a-114">[WS\_ERROR](ws-error.md) error: Rich error object.</span></span>


### <a name="signature-for-client-side-service-operations"></a><span data-ttu-id="d347a-115">Подпись для операций службы на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="d347a-115">Signature for Client-side Service Operations</span></span>

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a><span data-ttu-id="d347a-116">Требования к памяти для операций службы на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="d347a-116">Memory Considerations for Client-side Service Operations</span></span>

<span data-ttu-id="d347a-117">Вызов операции службы принимает в качестве параметра [WS \_ heap](ws-heap.md) \* .</span><span class="sxs-lookup"><span data-stu-id="d347a-117">The call to the service operation takes a [WS\_HEAP](ws-heap.md)\* as parameter.</span></span> <span data-ttu-id="d347a-118">Это обязательный параметр, используемый для сериализации и десериализации тела сообщений в параметры.</span><span class="sxs-lookup"><span data-stu-id="d347a-118">This is a required parameter used for serialization/deserialization of message bodies to parameters.</span></span>

<span data-ttu-id="d347a-119">Приложение должно вызвать [**всресесеап**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) , если вызов прошел.</span><span class="sxs-lookup"><span data-stu-id="d347a-119">The application must call [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) whether the call succeeded or not.</span></span> <span data-ttu-id="d347a-120">Если вызов выполнен успешно и у него есть исходящие параметры, приложение должно вызвать **всресесеап** сразу после завершения работы с исходящими параметрами.</span><span class="sxs-lookup"><span data-stu-id="d347a-120">If the call succeeded and it has outgoing parameters, the application should call **WsResetHeap** immediately after it is finished with the outgoing parameters.</span></span>

<span data-ttu-id="d347a-121">Приложение должно выделить память для параметров In и out с помощью [**всаллок**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span><span class="sxs-lookup"><span data-stu-id="d347a-121">The application should allocate memory for in and out parameters with [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span></span> <span data-ttu-id="d347a-122">Прокси-серверу службы может потребоваться перераспределить их, чтобы указанные указатели были перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="d347a-122">The service proxy may need to reallocate them so provided pointers will be overwritten.</span></span> <span data-ttu-id="d347a-123">Попытка освободить такую память приведет к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="d347a-123">An attempt to free such memory will cause the application to crash.</span></span>

### <a name="client-side-service-operation-and-ws_heap"></a><span data-ttu-id="d347a-124">Операция службы на стороне клиента и WS- \_ куча</span><span class="sxs-lookup"><span data-stu-id="d347a-124">Client-side Service Operation and WS\_HEAP</span></span>

``` syntax
HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessReceipt(orderReceipt);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderMemo, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessMemo(orderMemo);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
```

### <a name="error-parameter"></a><span data-ttu-id="d347a-125">Параметр ошибки</span><span class="sxs-lookup"><span data-stu-id="d347a-125">Error parameter</span></span>

<span data-ttu-id="d347a-126">Приложение всегда должно передавать параметр ошибки в:</span><span class="sxs-lookup"><span data-stu-id="d347a-126">The application should always pass in the error parameter to:</span></span>

-   <span data-ttu-id="d347a-127">Получение обширных сведений об ошибках в случае сбоя во время вызова операции службы.</span><span class="sxs-lookup"><span data-stu-id="d347a-127">Get rich error information if a failure occurs during the service operation call.</span></span>
-   <span data-ttu-id="d347a-128">Возвращает объект сбоя, если служба вернула ошибку.</span><span class="sxs-lookup"><span data-stu-id="d347a-128">Get the fault object if the service returned back a fault.</span></span> <span data-ttu-id="d347a-129">Ошибка содержится в объекте Error.</span><span class="sxs-lookup"><span data-stu-id="d347a-129">The fault is contained in the error object.</span></span> <span data-ttu-id="d347a-130">В этом случае значение **HRESULT** , возвращенное операцией службы, — **это \_ \_ Ошибка конечной \_ точки \_ WS E** (см. [возвращаемые значения веб-служб Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="d347a-130">In this case, the **HRESULT** value returned from the service operation is **WS\_E\_ENDPOINT\_FAULT\_RECEIVED** (see [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span>

### <a name="call-properties-for-client-side-service-operations"></a><span data-ttu-id="d347a-131">Вызов свойств для операций службы на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="d347a-131">Call Properties for Client-side Service Operations</span></span>

<span data-ttu-id="d347a-132">Свойства вызова позволяют приложению указать пользовательские параметры для данного вызова.</span><span class="sxs-lookup"><span data-stu-id="d347a-132">Call properties allow an application to specify custom settings for a given call.</span></span> <span data-ttu-id="d347a-133">В настоящее время в модели службы доступно только одно свойство Call, [**\_ \_ \_ \_ идентификатор вызова свойства WS Call**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span><span class="sxs-lookup"><span data-stu-id="d347a-133">Currently, only one call property is available with the service model, [**WS\_CALL\_PROPERTY\_CALL\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span></span>

``` syntax
WS_CALL_PROPERTY callProperties[1] = {0};
callProperties[0].id = WS_CALL_PROPERTY_CALL_ID;
callProperties[0].value = 5;

HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt,  callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;
//:
//:
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderReceipt, callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;

//:
//:
//:
// On a separate thread 
// In this case both the calls belong to call group 5, and will abandon as a result of the call to WsAbandonCall. 
hr = WsAbandonCall(serviceProxy, 5, error);
```

### <a name="abandoning-a-call"></a><span data-ttu-id="d347a-134">Прекращение вызова</span><span class="sxs-lookup"><span data-stu-id="d347a-134">Abandoning a Call</span></span>

<span data-ttu-id="d347a-135">Часто желательно отказаться от результатов вызова, чтобы перевернуть элемент управления в приложение, чтобы фактическое завершение вызова было обработано инфраструктурой.</span><span class="sxs-lookup"><span data-stu-id="d347a-135">It is often desirable to abandon the results of a call in order to relinquish the control back to the application, such that the actual call completion is handled by the infrastructure.</span></span> <span data-ttu-id="d347a-136">Прокси-сервер службы предоставляет это средство через [**всабандонкалл**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="d347a-136">Service proxy provides this facility through [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span>

<span data-ttu-id="d347a-137">Обратите внимание, что элемент управления для вызывающего объекта может быть не передан обратно, но он гарантирует, что среда выполнения прокси-сервера службы не будет ждать завершения любой операции, связанной с вводом-выводом, прежде чем она предоставит управление обратно вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="d347a-137">Note that the control to the caller may not be given back immediately, the only guarantee that the service proxy runtime gives is that it would not wait for any I/O bound operation to complete before it gives control back to the caller.</span></span>

<span data-ttu-id="d347a-138">Вызовы в операции службы на стороне клиента могут быть прерваны посредством вызова [**всабандонкалл**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="d347a-138">Calls on a client side service operation can be abandoned by means of a call to [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span> <span data-ttu-id="d347a-139">Он принимает прокси-сервер службы и идентификатор вызова. Идентификатор вызова задается как часть свойств вызова операции службы.</span><span class="sxs-lookup"><span data-stu-id="d347a-139">It takes a service proxy and a call id. A call Id is given as part of a call properties on a service operation.</span></span>

<span data-ttu-id="d347a-140">Если идентификатор вызова равен 0, прокси-сервер службы отменяет все ожидающие вызовы в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="d347a-140">If the call Id is 0, then the service proxy will abandon all pending calls at that instance.</span></span>

### <a name="call-timeouts"></a><span data-ttu-id="d347a-141">Время ожидания вызова</span><span class="sxs-lookup"><span data-stu-id="d347a-141">Call Timeouts</span></span>

<span data-ttu-id="d347a-142">По умолчанию для каждого вызова прокси-сервер службы имеет время ожидания в 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="d347a-142">By default a service proxy has a 30 second timeout for every call.</span></span> <span data-ttu-id="d347a-143">Время ожидания вызова можно изменить с помощью свойства прокси-сервера службы [**\_ \_ \_ \_ времени ожидания вызова свойства прокси-сервера**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) при создании прокси службы через [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="d347a-143">The timeout on a call can be changed by [**WS\_PROXY\_PROPERTY\_CALL\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) service proxy property when creating a service proxy through [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span></span>

<span data-ttu-id="d347a-144">По истечении времени ожидания вызов будет прерван.</span><span class="sxs-lookup"><span data-stu-id="d347a-144">After a timeout is reached, the call is abandoned.</span></span>

### <a name="return-values"></a><span data-ttu-id="d347a-145">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d347a-145">Return Values</span></span>

<span data-ttu-id="d347a-146">Все успешные значения **HRESULT** должны считаться успешными, а все значения сбоев должны рассматриваться как сбои.</span><span class="sxs-lookup"><span data-stu-id="d347a-146">All success **HRESULT** values must be treated as success, and all failure values must be treated as failures.</span></span> <span data-ttu-id="d347a-147">Ниже приведены некоторые значения **HRESULT** , которые может заждать приложение.</span><span class="sxs-lookup"><span data-stu-id="d347a-147">The following are some of the **HRESULT** values that an application can expect:</span></span>

-   <span data-ttu-id="d347a-148">**Служба WS \_ S \_ Async**: вызов будет выполнен асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d347a-148">**WS\_S\_ASYNC**: Call will be completed asynchronously.</span></span>
-   <span data-ttu-id="d347a-149">Ошибка: вызов успешно завершен.</span><span class="sxs-lookup"><span data-stu-id="d347a-149">NOERROR: Call completed successfully.</span></span>
-   <span data-ttu-id="d347a-150">**Служба WS \_ \_Операция E \_ прервана**: Вызов прерван.</span><span class="sxs-lookup"><span data-stu-id="d347a-150">**WS\_E\_OPERATION\_ABANDONED**: The call has been abandoned.</span></span> <span data-ttu-id="d347a-151">Объект Error содержит причину прерывания.</span><span class="sxs-lookup"><span data-stu-id="d347a-151">The error object contains the reason for abandon.</span></span>
-   <span data-ttu-id="d347a-152">**Служба WS \_ E \_ Недопустимая \_ Операция**: прокси-сервер службы не находится в надлежащем состоянии для выполнения вызова, проверьте состояние прокси-сервера службы, чтобы выяснить состояние прокси-сервера службы.</span><span class="sxs-lookup"><span data-stu-id="d347a-152">**WS\_E\_INVALID\_OPERATION**: The service proxy is not in an appropriate state to make a call, check the service proxy state to figure out the state of the service proxy.</span></span>

<span data-ttu-id="d347a-153">Полный список возвращаемых значений см. в статье [возвращаемые значения веб-служб Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d347a-153">For a complete list of return values, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

### <a name="code-examples"></a><span data-ttu-id="d347a-154">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="d347a-154">Code Examples</span></span>

<span data-ttu-id="d347a-155">Примеры кода см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="d347a-155">For code examples, see the following:</span></span>

-   [<span data-ttu-id="d347a-156">каллабандонексампле</span><span class="sxs-lookup"><span data-stu-id="d347a-156">CallAbandonExample</span></span>](callabandonexample.md)
-   [<span data-ttu-id="d347a-157">**всабандонкалл**</span><span class="sxs-lookup"><span data-stu-id="d347a-157">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




