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
# <a name="server-side-service-operations"></a>Операции службы на стороне сервера

В этом разделе описываются операции службы на стороне службы.


Ниже приведена структура операции службы на стороне сервера.

-   контекст неконстантной [ \_ операции \_ WS](ws-operation-context.md) \* : [контекст](context.md)операции.
-   Параметры операций службы: параметры, относящиеся к операции службы.
-   const [**WS \_ Async \_ context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* асинкконтекст: асинхронный контекст для асинхронного выполнения операций службы.
-   [Служба WS \_ Ошибка](ws-error.md) \* : расширенный объект ошибки.

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

## <a name="fault-and-error-handling"></a>Обработка сбоев и ошибок

Серверная часть должна использовать ошибки для доставки условий ошибки клиенту. Это можно сделать, выполнив возврат HRESULT со сбоем и встроить ошибку в объект Error.

Если ошибка не задана для объекта Error и возвращено значение HRESULT сбоя, инфраструктура попытается доставить ошибку обратно клиенту. Уровень детализации, раскрывающийся с клиентом в этом случае, управляется свойством службы « [**\_ \_ \_ \_ утечка ошибок» свойства службы WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) на [узле службы](service-host.md).

## <a name="call-completion"></a>Завершение вызова

Вызов в синхронной операции службы на стороне сервера считается завершенным, когда он возвращает управление на узел службы. Для асинхронной операции службы вызов считается завершенным после отправки уведомления о обратном вызове реализацией операции службы.

## <a name="call-lifetime"></a>Время жизни вызова

При реализации операции серверной службы в течение времени его существования следует уделить особое внимание. Время существования вызова может значительно влиять на время завершения работы узла службы.

Если ожидается, что операция службы на стороне сервера блокируется из-за операции, связанной с операциями ввода-вывода, рекомендуется зарегистрировать обратный вызов отмены, чтобы он получал уведомление о том, когда происходит прерывание работы узла службы, или когда базовое соединение закрывается клиентом.

## <a name="server-side-service-operations-and-memory-consideration"></a>Операции службы на стороне сервера и вопросы памяти

Если операции службы необходимо выделить память для исходящих параметров, она должна использовать объект [WS \_ heap](ws-heap.md) , доступный для него через [ \_ \_ контекст операции WS](ws-operation-context.md).

Пример: операция службы и WS \_ heap

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

## <a name="return-values"></a>Возвращаемые значения

-   WS \_ S \_ Async: вызов будет выполнен асинхронно.
-   WS \_ S \_ End: вызов успешно завершен, сервер не ожидает от клиента [ \_ сообщения WS](ws-message.md) , которые выходят за пределы этого вызова. Если \_ поступает другое сообщение WS, сервер должен прервать канал.
-   ОШИБКА/все остальные значения HRESULT успешно выполнены: вызов успешно завершен. Обратите внимание, что для успешного завершения операции службы приложение не должно возвращать HRESULT другой, а не ошибку.
-   Все с ошибкой HRESULT: ошибка отправляется обратно клиенту, если он доступен в службе WS \_ Error. В противном случае общая ошибка отправляется обратно клиенту. См. описание ошибки выше.

См. раздел [об отмене вызова](call-cancellation.md).

 

 




