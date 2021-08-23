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
ms.openlocfilehash: e73ccbb0c742d0be09570b0959c9c1a663d7f4d0f054cc88070d842ac6d954ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657304"
---
# <a name="client-side-service-operations"></a>Операции службы на стороне клиента

Ниже приведена структура операции службы на стороне клиента.

-   [Служба WS \_ \_Прокси-сервер службы](ws-service-proxy.md) \* serviceProxy: [прокси-сервер службы](service-proxy.md) для вызова.
-   [Служба WS \_ Куча КУЧИ](ws-heap.md) \* . Обязательная куча, используемая для сериализации тела и десериализации [ \_ сообщения WS](ws-message.md).
-   Параметры операций службы: параметры, относящиеся к операции службы.
-   [**Вызовите свойства и их количество**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): массив свойств Call.
-   Число свойств [**вызова**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : количество свойств вызова.
-   [**Служба WS \_ АСИНХРОНный \_ контекст**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Асинкконтекст: асинхронный контекст для асинхронного исполнения вызова.
-   [Служба WS \_ Ошибка:](ws-error.md) расширенный объект ошибки.


### <a name="signature-for-client-side-service-operations"></a>Подпись для операций службы на стороне клиента

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a>Требования к памяти для операций службы на стороне клиента

Вызов операции службы принимает в качестве параметра [WS \_ heap](ws-heap.md) \* . Это обязательный параметр, используемый для сериализации и десериализации тела сообщений в параметры.

Приложение должно вызвать [**всресесеап**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) , если вызов прошел. Если вызов выполнен успешно и у него есть исходящие параметры, приложение должно вызвать **всресесеап** сразу после завершения работы с исходящими параметрами.

Приложение должно выделить память для параметров In и out с помощью [**всаллок**](/windows/desktop/api/WebServices/nf-webservices-wsalloc). Прокси-серверу службы может потребоваться перераспределить их, чтобы указанные указатели были перезаписаны. Попытка освободить такую память приведет к сбою приложения.

### <a name="client-side-service-operation-and-ws_heap"></a>Операция службы на стороне клиента и WS- \_ куча

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

### <a name="error-parameter"></a>Параметр ошибки

Приложение всегда должно передавать параметр ошибки в:

-   Получение обширных сведений об ошибках в случае сбоя во время вызова операции службы.
-   Возвращает объект сбоя, если служба вернула ошибку. Ошибка содержится в объекте Error. в этом случае значение **HRESULT** , возвращенное операцией службы, — **это \_ \_ ошибка конечной \_ точки \_ WS E** (см. [Windows возвращаемые значения веб-служб](windows-web-services-return-values.md)).

### <a name="call-properties-for-client-side-service-operations"></a>Вызов свойств для операций службы на стороне клиента

Свойства вызова позволяют приложению указать пользовательские параметры для данного вызова. В настоящее время в модели службы доступно только одно свойство Call, [**\_ \_ \_ \_ идентификатор вызова свойства WS Call**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).

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

### <a name="abandoning-a-call"></a>Прекращение вызова

Часто желательно отказаться от результатов вызова, чтобы перевернуть элемент управления в приложение, чтобы фактическое завершение вызова было обработано инфраструктурой. Прокси-сервер службы предоставляет это средство через [**всабандонкалл**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).

Обратите внимание, что элемент управления для вызывающего объекта может быть не передан обратно, но он гарантирует, что среда выполнения прокси-сервера службы не будет ждать завершения любой операции, связанной с вводом-выводом, прежде чем она предоставит управление обратно вызывающему объекту.

Вызовы в операции службы на стороне клиента могут быть прерваны посредством вызова [**всабандонкалл**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall). Он принимает прокси-сервер службы и идентификатор вызова. Идентификатор вызова задается как часть свойств вызова операции службы.

Если идентификатор вызова равен 0, прокси-сервер службы отменяет все ожидающие вызовы в этом экземпляре.

### <a name="call-timeouts"></a>Время ожидания вызова

По умолчанию для каждого вызова прокси-сервер службы имеет время ожидания в 30 секунд. Время ожидания вызова можно изменить с помощью свойства прокси-сервера службы [**\_ \_ \_ \_ времени ожидания вызова свойства прокси-сервера**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) при создании прокси службы через [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).

По истечении времени ожидания вызов будет прерван.

### <a name="return-values"></a>Возвращаемые значения

Все успешные значения **HRESULT** должны считаться успешными, а все значения сбоев должны рассматриваться как сбои. Ниже приведены некоторые значения **HRESULT** , которые может заждать приложение.

-   **Служба WS \_ S \_ Async**: вызов будет выполнен асинхронно.
-   Ошибка: вызов успешно завершен.
-   **Служба WS \_ \_Операция E \_ прервана**: Вызов прерван. Объект Error содержит причину прерывания.
-   **Служба WS \_ E \_ Недопустимая \_ Операция**: прокси-сервер службы не находится в надлежащем состоянии для выполнения вызова, проверьте состояние прокси-сервера службы, чтобы выяснить состояние прокси-сервера службы.

полный список возвращаемых значений см. в разделе [Windows возвращаемые значения веб-служб](windows-web-services-return-values.md).

### <a name="code-examples"></a>Примеры кода

Примеры кода см. в следующих статьях:

-   [каллабандонексампле](callabandonexample.md)
-   [**всабандонкалл**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




