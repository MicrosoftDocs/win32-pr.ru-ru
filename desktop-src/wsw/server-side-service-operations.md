---
title: Операции службы на стороне сервера
description: В этом разделе описываются операции службы на стороне службы.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Веб-службы служб на стороне сервера для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7ad5a327c1cb79278aa562bfaa1753f008a542
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414169"
---
# <a name="server-side-service-operations"></a><span data-ttu-id="6bdf8-106">Операции службы на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="6bdf8-106">Server Side Service Operations</span></span>

<span data-ttu-id="6bdf8-107">В этом разделе описываются операции службы на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-107">This section describes service side service operations.</span></span>


<span data-ttu-id="6bdf8-108">Ниже приведена структура операции службы на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-108">The following is the layout of a server side service operation</span></span>

-   <span data-ttu-id="6bdf8-109">контекст неконстантной [ \_ операции \_ WS](ws-operation-context.md) \* : [контекст](context.md)операции.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-109">const [WS\_OPERATION\_CONTEXT](ws-operation-context.md)\* context: The operation [context](context.md).</span></span>
-   <span data-ttu-id="6bdf8-110">Параметры операций службы: параметры, относящиеся к операции службы.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="6bdf8-111">const [**WS \_ Async \_ context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* асинкконтекст: асинхронный контекст для асинхронного выполнения операций службы.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-111">const [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)\* asyncContext: Async context for executing the service operations asynchronously.</span></span>
-   <span data-ttu-id="6bdf8-112">[Служба WS \_ Ошибка](ws-error.md) \* : расширенный объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-112">[WS\_ERROR](ws-error.md)\* error: Rich error object.</span></span>

``` syntax
HRESULT CALLBACK Add(const WS_OPERATION_CONTEXT* context, 
                     ULONG a, ULONG b, ULONG* result, 
                     const WS_ASYNC_CONTEXT* asyncContext, 
                     WS_ERROR* error)
{
    *result = a +b;
    return NOERROR;
}
```

## <a name="fault-and-error-handling"></a><span data-ttu-id="6bdf8-113">Обработка сбоев и ошибок</span><span class="sxs-lookup"><span data-stu-id="6bdf8-113">Fault And Error Handling</span></span>

<span data-ttu-id="6bdf8-114">Серверная часть должна использовать ошибки для доставки условий ошибки клиенту.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-114">The server side should use faults to deliver error conditions to the client.</span></span> <span data-ttu-id="6bdf8-115">Это можно сделать, выполнив возврат HRESULT со сбоем и встроить ошибку в объект Error.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-115">It can do so by returning a failing HRESULT and embedding the fault in the error object.</span></span>

<span data-ttu-id="6bdf8-116">Если ошибка не задана для объекта Error и возвращено значение HRESULT сбоя, инфраструктура попытается доставить ошибку обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-116">If the fault is not set on the error object and a failure HRESULT is returned, the infrastructure will attempt deliver a fault back to client.</span></span> <span data-ttu-id="6bdf8-117">Уровень детализации, раскрывающийся с клиентом в этом случае, управляется свойством службы « [**\_ \_ \_ \_ утечка ошибок» свойства службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) на [узле службы](service-host.md).</span><span class="sxs-lookup"><span data-stu-id="6bdf8-117">The level of details disclosed to the client in such a case is controlled by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) service property on the [Service Host](service-host.md).</span></span>

## <a name="call-completion"></a><span data-ttu-id="6bdf8-118">Завершение вызова</span><span class="sxs-lookup"><span data-stu-id="6bdf8-118">Call Completion</span></span>

<span data-ttu-id="6bdf8-119">Вызов в синхронной операции службы на стороне сервера считается завершенным, когда он возвращает управление на узел службы.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-119">A call on a synchronous server side service operation is said to be complete when either it has returned control back to the service host.</span></span> <span data-ttu-id="6bdf8-120">Для асинхронной операции службы вызов считается завершенным после отправки уведомления о обратном вызове реализацией операции службы.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-120">For an asynchronous service operation a call is considered complete once the callback notification is issued by the service operation implementation.</span></span>

## <a name="call-lifetime"></a><span data-ttu-id="6bdf8-121">Время жизни вызова</span><span class="sxs-lookup"><span data-stu-id="6bdf8-121">Call Lifetime</span></span>

<span data-ttu-id="6bdf8-122">При реализации операции серверной службы в течение времени его существования следует уделить особое внимание.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-122">Special care should be taken when implementing a server side service operation about its lifetime.</span></span> <span data-ttu-id="6bdf8-123">Время существования вызова может значительно влиять на время завершения работы узла службы.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-123">The lifetime of a call can greatly affect how long the service host takes to shutdown.</span></span>

<span data-ttu-id="6bdf8-124">Если ожидается, что операция службы на стороне сервера блокируется из-за операции, связанной с операциями ввода-вывода, рекомендуется зарегистрировать обратный вызов отмены, чтобы он получал уведомление о том, когда происходит прерывание работы узла службы, или когда базовое соединение закрывается клиентом.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-124">If a server side service operation is expected to block because of some IO bound operation, it is recommended that it registers a cancellation callback such that it is notified if when service host is being aborted, or when the underlying connection is closed by the client.</span></span>

## <a name="server-side-service-operations-and-memory-consideration"></a><span data-ttu-id="6bdf8-125">Операции службы на стороне сервера и вопросы памяти</span><span class="sxs-lookup"><span data-stu-id="6bdf8-125">Server side service operations and memory consideration</span></span>

<span data-ttu-id="6bdf8-126">Если операции службы необходимо выделить память для исходящих параметров, она должна использовать объект [WS \_ heap](ws-heap.md) , доступный для него через [ \_ \_ контекст операции WS](ws-operation-context.md).</span><span class="sxs-lookup"><span data-stu-id="6bdf8-126">If a service operation needs to allocate memory for its outgoing parameters, it should use [WS\_HEAP](ws-heap.md) object available to it through the [WS\_OPERATION\_CONTEXT](ws-operation-context.md).</span></span>

<span data-ttu-id="6bdf8-127">Пример: операция службы и WS \_ heap</span><span class="sxs-lookup"><span data-stu-id="6bdf8-127">Example: Service Operation and WS\_HEAP</span></span>

``` syntax
HRESULT CALLBACK ProcessOrder (const WS_OPERATION_CONTEXT* context, const ULONG orderNumber, OrderReceipt** orderReceipt, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    WS_HEAP* heap;
    HRESULT hr = WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HEAP, &heap, sizeof(heap), NULL, error);
    if (FAILED(hr))
        return hr;
    hr = WsAlloc(heap, sizeof (OrderReceipt), orderReceipt, error);
    if (FAILED(hr))
        return hr;
    hr = FillInReceipt(*orderReceipt);
    if (FAILED(hr))
        return hr;
    return NOERROR;
} 
```

## <a name="return-values"></a><span data-ttu-id="6bdf8-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6bdf8-128">Return Values</span></span>

-   <span data-ttu-id="6bdf8-129">WS \_ S \_ Async: вызов будет выполнен асинхронно.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-129">WS\_S\_ASYNC: Call will be completed async.</span></span>
-   <span data-ttu-id="6bdf8-130">WS \_ S \_ End: вызов успешно завершен, сервер не ожидает от клиента [ \_ сообщения WS](ws-message.md) , которые выходят за пределы этого вызова.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-130">WS\_S\_END: Call completed successfully, the server is not expecting any [WS\_MESSAGE](ws-message.md) from the client beyond this call.</span></span> <span data-ttu-id="6bdf8-131">Если \_ поступает другое сообщение WS, сервер должен прервать канал.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-131">If another WS\_MESSAGE comes in then the server should abort the channel.</span></span>
-   <span data-ttu-id="6bdf8-132">ОШИБКА/все остальные значения HRESULT успешно выполнены: вызов успешно завершен.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-132">NOERROR/All other success HRESULTS: Call completed successfully.</span></span> <span data-ttu-id="6bdf8-133">Обратите внимание, что для успешного завершения операции службы приложение не должно возвращать HRESULT другой, а не ошибку.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-133">Note that it is recommended that the application should not return HRESULT other then NOERROR for successful completion of service operation.</span></span>
-   <span data-ttu-id="6bdf8-134">Все с ошибкой HRESULT: ошибка отправляется обратно клиенту, если он доступен в службе WS \_ Error.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-134">Everything with a failure HRESULT: A fault is send back to the client if one is available in WS\_ERROR.</span></span> <span data-ttu-id="6bdf8-135">В противном случае общая ошибка отправляется обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-135">Otherwise a generic fault is send back to the client.</span></span> <span data-ttu-id="6bdf8-136">См. описание ошибки выше.</span><span class="sxs-lookup"><span data-stu-id="6bdf8-136">See fault discussion above.</span></span>

<span data-ttu-id="6bdf8-137">См. раздел [об отмене вызова](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="6bdf8-137">See, [Call cancellation](call-cancellation.md).</span></span>

 

 




