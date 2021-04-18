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
# <a name="asynchronous-model"></a><span data-ttu-id="e623d-106">Асинхронная модель</span><span class="sxs-lookup"><span data-stu-id="e623d-106">Asynchronous Model</span></span>

<span data-ttu-id="e623d-107">Большинство операций в API веб-служб Windows можно выполнять синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="e623d-107">Most operations in Windows Web Services API can be performed synchronously or asynchronously.</span></span> <span data-ttu-id="e623d-108">Для синхронного вызова функции передайте значение NULL для структуры [**\_ \_ контекста WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="e623d-108">To call a function synchronously, pass a null value for the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="e623d-109">Чтобы указать, что функция может выполняться асинхронно, передайте в функцию **\_ \_ контекст WS Async** , отличный от NULL.</span><span class="sxs-lookup"><span data-stu-id="e623d-109">To specify that a function may be performed asynchronously, pass a non-null **WS\_ASYNC\_CONTEXT** to the function.</span></span>

<span data-ttu-id="e623d-110">При асинхронном вызове функция может выполняться синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="e623d-110">When called asynchronously, a function can nevertheless complete synchronously or asynchronously.</span></span> <span data-ttu-id="e623d-111">Если функция завершается синхронно, она возвращает значение, указывающее на завершение или ошибку, и это значение всегда равно значению, отличному от **WS \_ S \_** (см. раздел [возвращаемые значения веб-служб Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="e623d-111">If the function completes synchronously, it returns a value that indicates the final success or error, and this value is always something other than **WS\_S\_ASYNC** (See [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span> <span data-ttu-id="e623d-112">Однако возвращаемое значение **WS \_ S \_ Async** указывает, что функция будет асинхронно завершена.</span><span class="sxs-lookup"><span data-stu-id="e623d-112">A return value of **WS\_S\_ASYNC**, however, indicates that the function will complete asynchronously.</span></span> <span data-ttu-id="e623d-113">Когда функция завершается асинхронно, вызывается обратный вызов, чтобы сообщить о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="e623d-113">When the function completes asynchronously, a callback is invoked to signal completion of the operation.</span></span> <span data-ttu-id="e623d-114">Этот обратный вызов указывает на окончательное значение успеха или ошибки.</span><span class="sxs-lookup"><span data-stu-id="e623d-114">This callback indicates the final success or error value.</span></span> <span data-ttu-id="e623d-115">Обратный вызов не вызывается, если операция завершается синхронно.</span><span class="sxs-lookup"><span data-stu-id="e623d-115">The callback is not called if the operation completes synchronously.</span></span>

<span data-ttu-id="e623d-116">Чтобы создать асинхронный контекст, инициализируйте поля **обратного вызова** и **Каллбаккстате** структуры [**\_ \_ контекста WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="e623d-116">To create an asynchronous context, initialize the **callback** and **callbackState** fields of the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="e623d-117">Поле **каллбаккстате** используется для указания указателя на определяемые пользователем данные, которые передаются в функцию [**\_ асинхронного \_ обратного вызова WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .</span><span class="sxs-lookup"><span data-stu-id="e623d-117">The **callbackState** field is used to specify a pointer to user-defined data which is passed to the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) function.</span></span>

<span data-ttu-id="e623d-118">В следующем примере демонстрируется асинхронный вызов функции путем передачи указателя на структуру [**контекста WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , которая содержит обратный вызов и указатель на данные состояния.</span><span class="sxs-lookup"><span data-stu-id="e623d-118">The following example shows calling a function asynchronously by passing a pointer to a [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure that contains the callback and a pointer to the state data.</span></span>

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

<span data-ttu-id="e623d-119">[**\_ \_ Контекстная структура WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) используется асинхронной функцией только в течение вызова функции (не на время асинхронной операции), поэтому ее можно безопасно объявить в стеке.</span><span class="sxs-lookup"><span data-stu-id="e623d-119">The [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure is used by the asynchronous function only for the duration of the function call (not for the duration of the asynchronous operation), so you can safely declare it on the stack.</span></span>

<span data-ttu-id="e623d-120">Если какие-либо другие параметры, помимо структуры [**\_ \_ контекста WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , передаются в асинхронную функцию в качестве указателей, а функция завершается асинхронно, то ответственность за то, чтобы значения, на которые указывает эти параметры, наследуется (не освобождаются), пока не будет вызван асинхронный обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="e623d-120">If any other parameters, besides the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure, are passed to an asynchronous function as pointers and the function completes asynchronously, it is the responsibility of the caller to keep the values pointed to by these parameters alive (not freed) until the asynchronous callback is invoked.</span></span>

<span data-ttu-id="e623d-121">Существуют ограничения на операции, которые может выполнять обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="e623d-121">There are limitations on what operations a callback may perform.</span></span> <span data-ttu-id="e623d-122">Дополнительные сведения о возможных операциях см. в [**статье \_ \_ модель обратного вызова WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span><span class="sxs-lookup"><span data-stu-id="e623d-122">For more information on possible operations , see the [**WS\_CALLBACK\_MODEL**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span></span>

<span data-ttu-id="e623d-123">При реализации асинхронной функции не следует вызывать обратный вызов в том же потоке, который вызвал асинхронную функцию, прежде чем асинхронная функция вернется вызывающему объекту, так как это нарушает асинхронную модель.</span><span class="sxs-lookup"><span data-stu-id="e623d-123">When you implement an asynchronous function, do not invoke the callback on the same thread that called the asynchronous function before the asynchronous function has returned to the caller, as this disrupts the asynchronous model.</span></span>

<span data-ttu-id="e623d-124">При реализации функции, которая должна выполнять ряд асинхронных операций, рассмотрите возможность использования вспомогательной функции [**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .</span><span class="sxs-lookup"><span data-stu-id="e623d-124">When implementing a function that needs to execute a series of asynchronous operations, consider using the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) helper function.</span></span>

<span data-ttu-id="e623d-125">В [примере асинхронной функции](asyncmodelexample.md) показано, как реализовать и использовать функции, которые следуют за асинхронной моделью.</span><span class="sxs-lookup"><span data-stu-id="e623d-125">The [Asynchronous Function Example](asyncmodelexample.md) shows how to implement and consume functions that follow the asynchronous model.</span></span>

<span data-ttu-id="e623d-126">Запуск асинхронной операции ввода-вывода потребляет системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e623d-126">Starting an asynchronous IO operation consumes system resources.</span></span> <span data-ttu-id="e623d-127">Если запущено достаточно операций ввода-вывода, система может перестать отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="e623d-127">If enough IO operations are started, the system can become unresponsive.</span></span> <span data-ttu-id="e623d-128">Чтобы избежать этого, приложению необходимо ограничить число запусков асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="e623d-128">To prevent this, an application needs to limit the number of asynchronous operations that it starts.</span></span>

<span data-ttu-id="e623d-129">Асинхронная модель использует следующие элементы API.</span><span class="sxs-lookup"><span data-stu-id="e623d-129">The asynchronous model uses the following API elements.</span></span>

| <span data-ttu-id="e623d-130">Обратный вызов</span><span class="sxs-lookup"><span data-stu-id="e623d-130">Callback</span></span>                                         | <span data-ttu-id="e623d-131">Описание</span><span class="sxs-lookup"><span data-stu-id="e623d-131">Description</span></span>                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e623d-132">**\_асинхронный \_ обратный вызов WS**</span><span class="sxs-lookup"><span data-stu-id="e623d-132">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | <span data-ttu-id="e623d-133">Параметр функции обратного вызова, используемый с асинхронной моделью.</span><span class="sxs-lookup"><span data-stu-id="e623d-133">The callback function parameter used with the asynchronous model.</span></span>                                                                     |
| [<span data-ttu-id="e623d-134">**\_асинхронная \_ функция WS**</span><span class="sxs-lookup"><span data-stu-id="e623d-134">**WS\_ASYNC\_FUNCTION**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | <span data-ttu-id="e623d-135">Используется с параметром [**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) для указания следующей функции, которая будет вызываться в ряде асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="e623d-135">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |



 



| <span data-ttu-id="e623d-136">Перечисление</span><span class="sxs-lookup"><span data-stu-id="e623d-136">Enumeration</span></span>                                      | <span data-ttu-id="e623d-137">Описание</span><span class="sxs-lookup"><span data-stu-id="e623d-137">Description</span></span>                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e623d-138">**\_модель обратного вызова WS \_**</span><span class="sxs-lookup"><span data-stu-id="e623d-138">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | <span data-ttu-id="e623d-139">Задает поведение потоков обратного вызова (например, [**\_ асинхронный \_ обратный вызов WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span><span class="sxs-lookup"><span data-stu-id="e623d-139">Specifies the threading behavior of a callback (for example, a [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span></span> |



 



| <span data-ttu-id="e623d-140">Функция</span><span class="sxs-lookup"><span data-stu-id="e623d-140">Function</span></span>                                 | <span data-ttu-id="e623d-141">Описание</span><span class="sxs-lookup"><span data-stu-id="e623d-141">Description</span></span>                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e623d-142">**всасинцексекуте**</span><span class="sxs-lookup"><span data-stu-id="e623d-142">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | <span data-ttu-id="e623d-143">Вызывает пользовательский обратный вызов, который может инициировать асинхронную операцию и указывать функцию, которая должна вызываться после завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="e623d-143">Invokes a user-defined callback which can initiate an asynchronous operation and indicate a function that should be called when the asynchronous operation has been completed.</span></span> |



 



| <span data-ttu-id="e623d-144">Структура</span><span class="sxs-lookup"><span data-stu-id="e623d-144">Structure</span></span>                                          | <span data-ttu-id="e623d-145">Описание</span><span class="sxs-lookup"><span data-stu-id="e623d-145">Description</span></span>                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e623d-146">**\_асинхронный \_ контекст WS**</span><span class="sxs-lookup"><span data-stu-id="e623d-146">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | <span data-ttu-id="e623d-147">Задает асинхронный обратный вызов и указатель на определяемые пользователем данные, которые будут переданы асинхронному обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="e623d-147">Specifies the asynchronous callback and a pointer to user-defined data, which will be passed to the asynchronous callback.</span></span>            |
| [<span data-ttu-id="e623d-148">**\_асинхронная \_ Операция WS**</span><span class="sxs-lookup"><span data-stu-id="e623d-148">**WS\_ASYNC\_OPERATION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | <span data-ttu-id="e623d-149">Используется с параметром [**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) для указания следующей функции, которая будет вызываться в ряде асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="e623d-149">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |
| [<span data-ttu-id="e623d-150">**\_асинхронное \_ состояние WS**</span><span class="sxs-lookup"><span data-stu-id="e623d-150">**WS\_ASYNC\_STATE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | <span data-ttu-id="e623d-151">Используется [**всасинцексекуте**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) для управления состоянием асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="e623d-151">Used by [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to manage the state of an asynchronous operation.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e623d-152">См. также</span><span class="sxs-lookup"><span data-stu-id="e623d-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e623d-153">Пример асинхронной функции</span><span class="sxs-lookup"><span data-stu-id="e623d-153">Asynchronous Function Example</span></span>](asyncmodelexample.md)
</dt> <dt>

[<span data-ttu-id="e623d-154">**\_асинхронный \_ обратный вызов WS**</span><span class="sxs-lookup"><span data-stu-id="e623d-154">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[<span data-ttu-id="e623d-155">**\_асинхронный \_ контекст WS**</span><span class="sxs-lookup"><span data-stu-id="e623d-155">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[<span data-ttu-id="e623d-156">**\_модель обратного вызова WS \_**</span><span class="sxs-lookup"><span data-stu-id="e623d-156">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[<span data-ttu-id="e623d-157">**всасинцексекуте**</span><span class="sxs-lookup"><span data-stu-id="e623d-157">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




