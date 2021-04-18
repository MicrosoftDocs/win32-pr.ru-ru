---
title: Асинхронная модель
description: Большинство операций в API веб-служб Windows можно выполнять синхронно или асинхронно.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Веб-службы асинхронной модели для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700583"
---
# <a name="asynchronous-model"></a>Асинхронная модель

Большинство операций в API веб-служб Windows можно выполнять синхронно или асинхронно. Для синхронного вызова функции передайте значение NULL для структуры [**\_ \_ контекста WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . Чтобы указать, что функция может выполняться асинхронно, передайте в функцию **\_ \_ контекст WS Async** , отличный от NULL.

При асинхронном вызове функция может выполняться синхронно или асинхронно. Если функция завершается синхронно, она возвращает значение, указывающее на завершение или ошибку, и это значение всегда равно значению, отличному от **WS \_ S \_** (см. раздел [возвращаемые значения веб-служб Windows](windows-web-services-return-values.md)). Однако возвращаемое значение **WS \_ S \_ Async** указывает, что функция будет асинхронно завершена. Когда функция завершается асинхронно, вызывается обратный вызов, чтобы сообщить о завершении операции. Этот обратный вызов указывает на окончательное значение успеха или ошибки. Обратный вызов не вызывается, если операция завершается синхронно.

Чтобы создать асинхронный контекст, инициализируйте поля **обратного вызова** и **Каллбаккстате** структуры [**\_ \_ контекста WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . Поле **каллбаккстате** используется для указания указателя на определяемые пользователем данные, которые передаются в функцию [**\_ асинхронного \_ обратного вызова WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .

В следующем примере демонстрируется асинхронный вызов функции путем передачи указателя на структуру [**контекста WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , которая содержит обратный вызов и указатель на данные состояния.

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

[**\_ \_ Контекстная структура WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) используется асинхронной функцией только в течение вызова функции (не на время асинхронной операции), поэтому ее можно безопасно объявить в стеке.

Если какие-либо другие параметры, помимо структуры [**\_ \_ контекста WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , передаются в асинхронную функцию в качестве указателей, а функция завершается асинхронно, то ответственность за то, чтобы значения, на которые указывает эти параметры, наследуется (не освобождаются), пока не будет вызван асинхронный обратный вызов.

Существуют ограничения на операции, которые может выполнять обратный вызов. Дополнительные сведения о возможных операциях см. в [**статье \_ \_ модель обратного вызова WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).

При реализации асинхронной функции не следует вызывать обратный вызов в том же потоке, который вызвал асинхронную функцию, прежде чем асинхронная функция вернется вызывающему объекту, так как это нарушает асинхронную модель.

При реализации функции, которая должна выполнять ряд асинхронных операций, рассмотрите возможность использования вспомогательной функции [**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .

В [примере асинхронной функции](asyncmodelexample.md) показано, как реализовать и использовать функции, которые следуют за асинхронной моделью.

Запуск асинхронной операции ввода-вывода потребляет системные ресурсы. Если запущено достаточно операций ввода-вывода, система может перестать отвечать на запросы. Чтобы избежать этого, приложению необходимо ограничить число запусков асинхронных операций.

Асинхронная модель использует следующие элементы API.

| Обратный вызов                                         | Описание                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_асинхронный \_ обратный вызов WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | Параметр функции обратного вызова, используемый с асинхронной моделью.                                                                     |
| [**\_асинхронная \_ функция WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | Используется с параметром [**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) для указания следующей функции, которая будет вызываться в ряде асинхронных операций. |



 



| Перечисление                                      | Описание                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**\_модель обратного вызова WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | Задает поведение потоков обратного вызова (например, [**\_ асинхронный \_ обратный вызов WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)). |



 



| Функция                                 | Описание                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | Вызывает пользовательский обратный вызов, который может инициировать асинхронную операцию и указывать функцию, которая должна вызываться после завершения асинхронной операции. |



 



| Структура                                          | Описание                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_асинхронный \_ контекст WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | Задает асинхронный обратный вызов и указатель на определяемые пользователем данные, которые будут переданы асинхронному обратному вызову.            |
| [**\_асинхронная \_ Операция WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | Используется с параметром [**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) для указания следующей функции, которая будет вызываться в ряде асинхронных операций. |
| [**\_асинхронное \_ состояние WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | Используется [**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) для управления состоянием асинхронной операции.                                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Пример асинхронной функции](asyncmodelexample.md)
</dt> <dt>

[**\_асинхронный \_ обратный вызов WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[**\_асинхронный \_ контекст WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[**\_модель обратного вызова WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




