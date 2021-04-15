---
description: Вызов асинхронных методов
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Вызов асинхронных методов
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539635"
---
# <a name="calling-asynchronous-methods"></a><span data-ttu-id="7e06b-103">Вызов асинхронных методов</span><span class="sxs-lookup"><span data-stu-id="7e06b-103">Calling Asynchronous Methods</span></span>

<span data-ttu-id="7e06b-104">В Media Foundation многие операции выполняются асинхронно.</span><span class="sxs-lookup"><span data-stu-id="7e06b-104">In Media Foundation, many operations are performed asynchronously.</span></span> <span data-ttu-id="7e06b-105">Асинхронные операции могут повысить производительность, так как они не блокируют вызывающий поток.</span><span class="sxs-lookup"><span data-stu-id="7e06b-105">Asynchronous operations can improve performance, because they do not block the calling thread.</span></span> <span data-ttu-id="7e06b-106">Асинхронная операция в Media Foundation определяется парой методов с соглашением об именовании **Begin..** . и **End...**.</span><span class="sxs-lookup"><span data-stu-id="7e06b-106">An asynchronous operation in Media Foundation is defined by a pair of methods with the naming convention **Begin...** and **End....**.</span></span> <span data-ttu-id="7e06b-107">Вместе эти два метода определяют асинхронную операцию чтения в потоке.</span><span class="sxs-lookup"><span data-stu-id="7e06b-107">Together, these two methods define an asynchronous read operation on the stream.</span></span>

<span data-ttu-id="7e06b-108">Чтобы запустить асинхронную операцию, вызовите метод **Begin** .</span><span class="sxs-lookup"><span data-stu-id="7e06b-108">To start an asynchronous operation, call the **Begin** method.</span></span> <span data-ttu-id="7e06b-109">Метод **Begin** всегда содержит по крайней мере два параметра:</span><span class="sxs-lookup"><span data-stu-id="7e06b-109">The **Begin** method always contains at least two parameters:</span></span>

-   <span data-ttu-id="7e06b-110">Указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="7e06b-110">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="7e06b-111">Приложение должно реализовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7e06b-111">The application must implement this interface.</span></span>
-   <span data-ttu-id="7e06b-112">Указатель на необязательный объект состояния.</span><span class="sxs-lookup"><span data-stu-id="7e06b-112">A pointer to an optional state object.</span></span>

<span data-ttu-id="7e06b-113">Интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) уведомляет приложение о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="7e06b-113">The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface notifies the application when the operation is completed.</span></span> <span data-ttu-id="7e06b-114">Пример реализации этого интерфейса см. [в разделе Реализация асинхронного обратного вызова](implementing-the-asynchronous-callback.md).</span><span class="sxs-lookup"><span data-stu-id="7e06b-114">For an example of how to implement this interface, see [Implementing the Asynchronous Callback](implementing-the-asynchronous-callback.md).</span></span> <span data-ttu-id="7e06b-115">Объект состояния является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7e06b-115">The state object is optional.</span></span> <span data-ttu-id="7e06b-116">Если он указан, он должен реализовать интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="7e06b-116">If specified, it must implement the **IUnknown** interface.</span></span> <span data-ttu-id="7e06b-117">Объект состояния можно использовать для хранения любых сведений о состоянии, необходимых для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7e06b-117">You can use the state object to store any state information that is needed by your callback.</span></span> <span data-ttu-id="7e06b-118">Если сведения о состоянии не нужны, можно присвоить этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7e06b-118">If you do not need state information, you can set this parameter to **NULL**.</span></span> <span data-ttu-id="7e06b-119">Метод **Begin** может содержать дополнительные параметры, характерные для этого метода.</span><span class="sxs-lookup"><span data-stu-id="7e06b-119">The **Begin** method might contain additional parameters that are specific to that method.</span></span>

<span data-ttu-id="7e06b-120">Если метод **Begin** возвращает код ошибки, это означает, что операция была выполнена неудачно, а обратный вызов не будет вызываться.</span><span class="sxs-lookup"><span data-stu-id="7e06b-120">If the **Begin** method returns a failure code, it means the operation has failed immediately, and the callback will not be invoked.</span></span> <span data-ttu-id="7e06b-121">Если метод **Begin** завершается удачно, это означает, что операция находится в состоянии ожидания, а обратный вызов будет вызываться после завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7e06b-121">If the **Begin** method succeeds, it means the operation is pending, and the callback will be invoked when the operation completes.</span></span>

<span data-ttu-id="7e06b-122">Например, метод [**имфбитестреам:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) запускает асинхронную операцию чтения для потока байтов:</span><span class="sxs-lookup"><span data-stu-id="7e06b-122">For example, the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) method starts an asynchronous read operation on a byte stream:</span></span>


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



<span data-ttu-id="7e06b-123">Метод обратного вызова — [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="7e06b-123">The callback method is [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="7e06b-124">Он имеет единственный параметр *пасинкресулт*, который является указателем на интерфейс [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="7e06b-124">It has a single parameter, *pAsyncResult*, which is a pointer to the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="7e06b-125">Чтобы завершить асинхронную операцию, вызовите метод **End** , соответствующий асинхронному методу **Begin** .</span><span class="sxs-lookup"><span data-stu-id="7e06b-125">To complete the asynchronous operation, call the **End** method that matches the asynchronous **Begin** method.</span></span> <span data-ttu-id="7e06b-126">Метод **End** всегда принимает указатель **имфасинкресулт** .</span><span class="sxs-lookup"><span data-stu-id="7e06b-126">The **End** method always takes an **IMFAsyncResult** pointer.</span></span> <span data-ttu-id="7e06b-127">Всегда передавайте тот же указатель, который был получен в методе **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="7e06b-127">Always pass in the same pointer that you received in the **Invoke** method.</span></span> <span data-ttu-id="7e06b-128">Асинхронная операция не завершается, пока не будет вызван метод **End** .</span><span class="sxs-lookup"><span data-stu-id="7e06b-128">The asynchronous operation is not complete until you call the **End** method.</span></span> <span data-ttu-id="7e06b-129">Вы можете вызвать метод **End** из метода **Invoke** или вызвать его из другого потока.</span><span class="sxs-lookup"><span data-stu-id="7e06b-129">You may call the **End** method from inside the **Invoke** method, or you can call it from another thread.</span></span>

<span data-ttu-id="7e06b-130">Например, чтобы выполнить [**имфбитестреам:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) в байтовом потоке, вызовите [**Имфбитестреам:: EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span><span class="sxs-lookup"><span data-stu-id="7e06b-130">For example, to complete the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) on a byte stream, call [**IMFByteStream::EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span></span>


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



<span data-ttu-id="7e06b-131">Возвращаемое значение метода **End** указывает состояние асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="7e06b-131">The return value of the **End** method indicates the status of the asynchronous operation.</span></span> <span data-ttu-id="7e06b-132">В большинстве случаев приложение будет выполнять некоторую работу после завершения асинхронной операции, независимо от того, завершается ли она успешно.</span><span class="sxs-lookup"><span data-stu-id="7e06b-132">In most cases, your application will perform some work after the asynchronous operation completes, whether it completes successfully or not.</span></span> <span data-ttu-id="7e06b-133">Доступно несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="7e06b-133">You have several options:</span></span>

-   <span data-ttu-id="7e06b-134">Выполните работу внутри метода [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="7e06b-134">Do the work inside the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="7e06b-135">Этот подход приемлем, если приложение никогда не блокирует вызывающий поток или ожидает чего-либо внутри метода **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="7e06b-135">This approach is acceptable as long as your application never blocks the calling thread or waits for anything inside the **Invoke** method.</span></span> <span data-ttu-id="7e06b-136">При блокировке вызывающего потока поток потоковой передачи можно заблокировать.</span><span class="sxs-lookup"><span data-stu-id="7e06b-136">If you block the calling thread, you might block the streaming pipeline.</span></span> <span data-ttu-id="7e06b-137">Например, можно обновить некоторые переменные состояния, но не выполнять синхронную операцию чтения или ожидание объекта мьютекса.</span><span class="sxs-lookup"><span data-stu-id="7e06b-137">For example, you might update some state variables, but do not perform a synchronous read operation or wait on a mutex object.</span></span>
-   <span data-ttu-id="7e06b-138">В методе [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Задайте событие и немедленно возвратите значение.</span><span class="sxs-lookup"><span data-stu-id="7e06b-138">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, set an event and return immediately.</span></span> <span data-ttu-id="7e06b-139">Вызывающий поток приложения ожидает события и выполняет работу при сигнале события.</span><span class="sxs-lookup"><span data-stu-id="7e06b-139">The application's calling thread waits for the event and does the work when the event is signaled.</span></span>
-   <span data-ttu-id="7e06b-140">В методе [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Опубликуйте сообщение частного окна в окне приложения и немедленно возвратите значение.</span><span class="sxs-lookup"><span data-stu-id="7e06b-140">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, post a private window message to your application window and return immediately.</span></span> <span data-ttu-id="7e06b-141">Приложение выполняет работу над циклом обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="7e06b-141">The application does the work on its message loop.</span></span> <span data-ttu-id="7e06b-142">(Не забудьте опубликовать сообщение, вызвав **сообщение**, а не **SendMessage**, так как **SendMessage** может блокировать поток обратного вызова.)</span><span class="sxs-lookup"><span data-stu-id="7e06b-142">(Make sure to post the message by calling **PostMessage**, not **SendMessage**, because **SendMessage** can block the callback thread.)</span></span>

<span data-ttu-id="7e06b-143">Важно помнить, что [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) вызывается из другого потока.</span><span class="sxs-lookup"><span data-stu-id="7e06b-143">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from another thread.</span></span> <span data-ttu-id="7e06b-144">Приложение отвечает за то, чтобы любая работа, выполняемая внутри **вызова** , была потокобезопасной.</span><span class="sxs-lookup"><span data-stu-id="7e06b-144">Your application is responsible for ensuring that any work performed inside **Invoke** is thread-safe.</span></span>

<span data-ttu-id="7e06b-145">По умолчанию поток, вызывающий [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , не делает никаких предположений о поведении объекта обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7e06b-145">By default, the thread that calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) makes no assumptions about the behavior of your callback object.</span></span> <span data-ttu-id="7e06b-146">При необходимости можно реализовать метод [**имфасинккаллбакк:: Parameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) , чтобы получить сведения о реализации обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7e06b-146">Optionally, you can implement the [**IMFAsyncCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) method to return information about your callback implementation.</span></span> <span data-ttu-id="7e06b-147">В противном случае этот метод может возвращать **E \_ нотимпл**:</span><span class="sxs-lookup"><span data-stu-id="7e06b-147">Otherwise, this method can return **E\_NOTIMPL**:</span></span>


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



<span data-ttu-id="7e06b-148">Если в методе **Begin** указан объект состояния, его можно извлечь из метода обратного вызова, вызвав [**имфасинкресулт::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)GetObject.</span><span class="sxs-lookup"><span data-stu-id="7e06b-148">If you specified a state object in the **Begin** method, you can retrieve it from inside your callback method by calling [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e06b-149">См. также</span><span class="sxs-lookup"><span data-stu-id="7e06b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e06b-150">Асинхронные методы обратного вызова</span><span class="sxs-lookup"><span data-stu-id="7e06b-150">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



