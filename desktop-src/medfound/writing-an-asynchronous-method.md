---
description: В этом разделе описано, как реализовать асинхронный метод в Microsoft Media Foundation.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Создание асинхронного метода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348235"
---
# <a name="writing-an-asynchronous-method"></a><span data-ttu-id="e0693-103">Создание асинхронного метода</span><span class="sxs-lookup"><span data-stu-id="e0693-103">Writing an Asynchronous Method</span></span>

<span data-ttu-id="e0693-104">В этом разделе описано, как реализовать асинхронный метод в Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e0693-104">This topic describes how to implement an asynchronous method in Microsoft Media Foundation.</span></span>

<span data-ttu-id="e0693-105">Асинхронные методы являются повсеместными в Media Foundation конвейере.</span><span class="sxs-lookup"><span data-stu-id="e0693-105">Asynchronous methods are ubiquitous in the Media Foundation pipeline.</span></span> <span data-ttu-id="e0693-106">Асинхронные методы упрощают распределение работы между несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="e0693-106">Asynchronous methods make it easier to distribute work among several threads.</span></span> <span data-ttu-id="e0693-107">Особенно важно выполнять операции ввода-вывода асинхронно, чтобы чтение из файла или сети не блокировало остальную часть конвейера.</span><span class="sxs-lookup"><span data-stu-id="e0693-107">It is particularly important to perform I/O asynchronously, so that reading from a file or network does not block the rest of the pipeline.</span></span>

<span data-ttu-id="e0693-108">При написании источника мультимедиа или приемника мультимедиа очень важно правильно выполнять асинхронные операции, так как производительность компонента влияет на весь конвейер.</span><span class="sxs-lookup"><span data-stu-id="e0693-108">If you are writing a media source or media sink, it is crucial to handle asynchronous operations correctly, because your component's performance has an impact on the entire pipeline.</span></span>

> [!Note]  
> <span data-ttu-id="e0693-109">Media Foundation преобразования (МФТС) по умолчанию используют синхронные методы.</span><span class="sxs-lookup"><span data-stu-id="e0693-109">Media Foundation transforms (MFTs) use synchronous methods by default.</span></span>

 

### <a name="work-queues-for-asynchronous-operations"></a><span data-ttu-id="e0693-110">Рабочие очереди для асинхронных операций</span><span class="sxs-lookup"><span data-stu-id="e0693-110">Work Queues For Asynchronous Operations</span></span>

<span data-ttu-id="e0693-111">В Media Foundation существует замкнутая связь между [асинхронными методами обратного вызова](asynchronous-callback-methods.md) и [рабочими очередями](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="e0693-111">In Media Foundation, there is a close relationship between [Asynchronous Callback Methods](asynchronous-callback-methods.md) and [Work Queues](work-queues.md).</span></span> <span data-ttu-id="e0693-112">Рабочая очередь — это абстракция для перемещения работы из потока вызывающего объекта в рабочий поток.</span><span class="sxs-lookup"><span data-stu-id="e0693-112">A work queue is an abstraction for moving work from the caller's thread to a worker thread.</span></span> <span data-ttu-id="e0693-113">Чтобы выполнить работу в рабочей очереди, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e0693-113">To perform work on a work queue, do the following:</span></span>

1.  <span data-ttu-id="e0693-114">Реализуйте интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="e0693-114">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="e0693-115">Вызовите [**мфкреатеасинкресулт**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) , чтобы создать *результирующий* объект.</span><span class="sxs-lookup"><span data-stu-id="e0693-115">Call [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a *result* object.</span></span> <span data-ttu-id="e0693-116">Объект Result предоставляет [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span><span class="sxs-lookup"><span data-stu-id="e0693-116">The result object exposes the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span></span> <span data-ttu-id="e0693-117">Результирующий объект содержит три указателя:</span><span class="sxs-lookup"><span data-stu-id="e0693-117">The result object contains three pointers:</span></span>

    -   <span data-ttu-id="e0693-118">Указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-118">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="e0693-119">Необязательный указатель на объект состояния.</span><span class="sxs-lookup"><span data-stu-id="e0693-119">An optional pointer to a state object.</span></span> <span data-ttu-id="e0693-120">Если этот параметр указан, объект состояния должен реализовывать **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="e0693-120">If specified, the state object must implement **IUnknown**.</span></span>
    -   <span data-ttu-id="e0693-121">Необязательный указатель на закрытый объект.</span><span class="sxs-lookup"><span data-stu-id="e0693-121">An optional pointer to a private object.</span></span> <span data-ttu-id="e0693-122">Если этот объект указан, он также должен реализовывать **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="e0693-122">If specified, this object also must implement **IUnknown**.</span></span>

    <span data-ttu-id="e0693-123">Последние два указателя могут иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0693-123">The last two pointers can be **NULL**.</span></span> <span data-ttu-id="e0693-124">В противном случае используйте их для хранения сведений об асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="e0693-124">Otherwise, use them to hold information about the asynchronous operation.</span></span>

3.  <span data-ttu-id="e0693-125">Вызовите [**мфпутворкитемекс**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) , чтобы поставить в очередь рабочий элемент.</span><span class="sxs-lookup"><span data-stu-id="e0693-125">Call [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue to the work item.</span></span>
4.  <span data-ttu-id="e0693-126">Поток рабочей очереди вызывает метод [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="e0693-126">The work-queue thread calls your [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span>
5.  <span data-ttu-id="e0693-127">Выполните работу внутри метода [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="e0693-127">Do the work inside your [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="e0693-128">Параметр *пасинкресулт* этого метода является указателем [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) из шага 2.</span><span class="sxs-lookup"><span data-stu-id="e0693-128">The *pAsyncResult* parameter of this method is the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) pointer from step 2.</span></span> <span data-ttu-id="e0693-129">Используйте этот указатель для получения объекта состояния и закрытого объекта:</span><span class="sxs-lookup"><span data-stu-id="e0693-129">Use this pointer to get the state object and private object:</span></span>
    -   <span data-ttu-id="e0693-130">Чтобы получить объект состояния, вызовите [**имфасинкресулт::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)GetObject.</span><span class="sxs-lookup"><span data-stu-id="e0693-130">To get the state object, call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>
    -   <span data-ttu-id="e0693-131">Чтобы получить закрытый объект, вызовите метод [**имфасинкресулт:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span><span class="sxs-lookup"><span data-stu-id="e0693-131">To get the private object, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span></span>

<span data-ttu-id="e0693-132">В качестве альтернативы можно объединить шаги 2 и 3, вызвав функцию [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) .</span><span class="sxs-lookup"><span data-stu-id="e0693-132">As an alternative, you can combine steps 2 and 3 by calling the [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) function.</span></span> <span data-ttu-id="e0693-133">На внутреннем уровне эта функция вызывает [**мфкреатеасинкресулт**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) для создания результирующего объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-133">Internally, this function calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create the result object.</span></span>

<span data-ttu-id="e0693-134">На следующей диаграмме показаны связи между вызывающим объектом, результирующий объект, объект состояния и закрытый объект.</span><span class="sxs-lookup"><span data-stu-id="e0693-134">The following diagram shows the relationships between the caller, the result object, the state object, and the private object.</span></span>

![Схема, показывающая объект асинхронного результата](images/workqueues01.png)

<span data-ttu-id="e0693-136">На следующей схеме последовательностей показано, как объект помещает рабочий элемент в очередь.</span><span class="sxs-lookup"><span data-stu-id="e0693-136">The following sequence diagram shows how an object queues a work item.</span></span> <span data-ttu-id="e0693-137">Когда поток рабочей очереди вызывает [**вызов**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), объект выполняет асинхронную операцию в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="e0693-137">When the work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), the object performs the asynchronous operation on that thread.</span></span>

![Диаграмма, показывающая, как объект помещает рабочий элемент в очередь](images/workqueues02.png)

<span data-ttu-id="e0693-139">Важно помнить, что [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) вызывается из потока, который принадлежит рабочей очереди.</span><span class="sxs-lookup"><span data-stu-id="e0693-139">It is important to remember [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from a thread that is owned by the work queue.</span></span> <span data-ttu-id="e0693-140">Реализация **Invoke** должна быть потокобезопасной.</span><span class="sxs-lookup"><span data-stu-id="e0693-140">Your implementation of **Invoke** must be thread safe.</span></span> <span data-ttu-id="e0693-141">Кроме того, при использовании рабочей очереди платформы (**\_ \_ \_ стандартная очередь обратного вызова мфасинк**) крайне важно, чтобы поток не блокировался, так как он может блокировать обработку данных на весь конвейер Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e0693-141">In addition, if you use the platform work queue (**MFASYNC\_CALLBACK\_QUEUE\_STANDARD**), it is critical that you never block the thread, because that can block the entire Media Foundation pipeline from processing data.</span></span> <span data-ttu-id="e0693-142">Если необходимо выполнить операцию, которая будет блокироваться или занять длительное время, используйте частную рабочую очередь.</span><span class="sxs-lookup"><span data-stu-id="e0693-142">If you need to perform an operation that will block or take a long time to complete, use a private work queue.</span></span> <span data-ttu-id="e0693-143">Чтобы создать частную рабочую очередь, вызовите [**мфаллокатеворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="e0693-143">To create a private work queue, call [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span> <span data-ttu-id="e0693-144">Любой компонент конвейера, выполняющий операции ввода-вывода, должен избегать блокирования вызовов ввода-вывода по той же причине.</span><span class="sxs-lookup"><span data-stu-id="e0693-144">Any pipeline component that performs I/O operations should avoid blocking I/O calls for the same reason.</span></span> <span data-ttu-id="e0693-145">Интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) предоставляет полезную абстракцию для асинхронного файлового ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e0693-145">The [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface provides a useful abstraction for asynchronous file I/O.</span></span>

### <a name="implementing-the-beginend-pattern"></a><span data-ttu-id="e0693-146">Реализация Begin. ../енд... Пакет</span><span class="sxs-lookup"><span data-stu-id="e0693-146">Implementing the Begin.../End... Pattern</span></span>

<span data-ttu-id="e0693-147">Как описано в разделе [Вызов асинхронных методов](calling-asynchronous-methods.md), асинхронные методы в Media Foundation часто используют инструкцию **Begin...** / **Конец....** пакет.</span><span class="sxs-lookup"><span data-stu-id="e0693-147">As described in [Calling Asynchronous Methods](calling-asynchronous-methods.md), asynchronous methods in Media Foundation often use the **Begin...**/**End....** pattern.</span></span> <span data-ttu-id="e0693-148">В этом шаблоне асинхронная операция использует два метода с сигнатурами, аналогичные следующим:</span><span class="sxs-lookup"><span data-stu-id="e0693-148">In this pattern, an asynchronous operation uses two methods with signatures similar to the following:</span></span>

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

<span data-ttu-id="e0693-149">Чтобы сделать метод действительно асинхронным, реализация **бегинкс** должна выполнить фактическую работу в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="e0693-149">To make the method truly asynchronous, the implementation of **BeginX** must perform the actual work on another thread.</span></span> <span data-ttu-id="e0693-150">Именно здесь на изображении поступают рабочие очереди.</span><span class="sxs-lookup"><span data-stu-id="e0693-150">This is where work queues come into the picture.</span></span> <span data-ttu-id="e0693-151">В следующих шагах *вызывающий объект* является кодом, который вызывает **бегинкс** и **ендкс**.</span><span class="sxs-lookup"><span data-stu-id="e0693-151">In the steps that follow, the *caller* is the code that calls **BeginX** and **EndX**.</span></span> <span data-ttu-id="e0693-152">Это может быть приложение или конвейер Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e0693-152">This might be an application or the Media Foundation pipeline.</span></span> <span data-ttu-id="e0693-153">*Компонент* — это код, реализующий **бегинкс** и **ендкс**.</span><span class="sxs-lookup"><span data-stu-id="e0693-153">The *component* is the code that implements **BeginX** and **EndX**.</span></span>

1.  <span data-ttu-id="e0693-154">Вызывающий объект вызывает **Begin...**, передавая указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-154">The caller calls **Begin...**, passing in a pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="e0693-155">Компонент создает новый объект асинхронного результата.</span><span class="sxs-lookup"><span data-stu-id="e0693-155">The component creates a new asynchronous result object.</span></span> <span data-ttu-id="e0693-156">Этот объект хранит интерфейс обратного вызова и объект состояния вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-156">This object stores the caller's callback interface and state object.</span></span> <span data-ttu-id="e0693-157">Как правило, он также хранит все сведения о закрытом состоянии, необходимые компоненту для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="e0693-157">Typically, it also stores any private state information that the component needs to complete the operation.</span></span> <span data-ttu-id="e0693-158">Результирующий объект этого шага помечается как "result 1" на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="e0693-158">The result object from this step is labeled "Result 1" in the next diagram.</span></span>
3.  <span data-ttu-id="e0693-159">Компонент создает второй результирующий объект.</span><span class="sxs-lookup"><span data-stu-id="e0693-159">The component creates a second result object.</span></span> <span data-ttu-id="e0693-160">В этом результирующем объекте хранятся два указателя: первый результирующий объект и интерфейс обратного вызова вызываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-160">This result object stores two pointers: The first result object, and the callback interface of the callee.</span></span> <span data-ttu-id="e0693-161">Этот результирующий объект помечается как "результат 2" на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="e0693-161">This result object is labeled "Result 2" in the next diagram.</span></span>
4.  <span data-ttu-id="e0693-162">Компонент вызывает [**мфпутворкитемекс**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) для постановки в очередь нового рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="e0693-162">The component calls [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue a new work item.</span></span>
5.  <span data-ttu-id="e0693-163">В методе [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) компонент выполняет асинхронную работу.</span><span class="sxs-lookup"><span data-stu-id="e0693-163">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the component does the asynchronous work.</span></span>
6.  <span data-ttu-id="e0693-164">Компонент вызывает [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) для вызова метода обратного вызова вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-164">The component calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>
7.  <span data-ttu-id="e0693-165">Вызывающий объект вызывает метод **ендкс** .</span><span class="sxs-lookup"><span data-stu-id="e0693-165">The caller calls the **EndX** method.</span></span>

![Схема, показывающая, как объект реализует шаблон начала/окончания](images/workqueues03.png)

## <a name="asynchronous-method-example"></a><span data-ttu-id="e0693-167">Пример асинхронного метода</span><span class="sxs-lookup"><span data-stu-id="e0693-167">Asynchronous Method Example</span></span>

<span data-ttu-id="e0693-168">Чтобы проиллюстрировать это обсуждение, мы будем использовать пример надуманный.</span><span class="sxs-lookup"><span data-stu-id="e0693-168">To illustrate this discussion, we will use a contrived example.</span></span> <span data-ttu-id="e0693-169">Рассмотрим асинхронный метод для вычисления квадратного корня:</span><span class="sxs-lookup"><span data-stu-id="e0693-169">Consider an asynchronous method for computing a square root:</span></span>


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



<span data-ttu-id="e0693-170">Параметр *x* аргумента `BeginSquareRoot` — это значение, для которого вычисляется квадратный корень.</span><span class="sxs-lookup"><span data-stu-id="e0693-170">The *x* parameter of `BeginSquareRoot` is the value whose square root will be calculated.</span></span> <span data-ttu-id="e0693-171">Квадратный корень возвращается в параметре *Pval* объекта `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="e0693-171">The square root is returned in the *pVal* parameter of `EndSquareRoot`.</span></span>

<span data-ttu-id="e0693-172">Ниже приведено объявление класса, который реализует эти два метода:</span><span class="sxs-lookup"><span data-stu-id="e0693-172">Here is the declaration of a class that implements these two methods:</span></span>


```C++
class SqrRoot : public IMFAsyncCallback
{
    LONG    m_cRef;
    double  m_sqrt;

    HRESULT DoCalculateSquareRoot(AsyncOp *pOp);

public:

    SqrRoot() : m_cRef(1)
    {

    }

    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(SqrRoot, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMFAsyncCallback methods.

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;  
    }
    // Invoke is where the work is performed.
    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



<span data-ttu-id="e0693-173">`SqrRoot`Класс реализует [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , чтобы он мог поместить операцию с квадратным корнем в рабочую очередь.</span><span class="sxs-lookup"><span data-stu-id="e0693-173">The `SqrRoot` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) so that it can put the square root operation on a work queue.</span></span> <span data-ttu-id="e0693-174">`DoCalculateSquareRoot`Метод является закрытым методом класса, который вычисляет квадратный корень.</span><span class="sxs-lookup"><span data-stu-id="e0693-174">The `DoCalculateSquareRoot` method is the private class method that calculates the square root.</span></span> <span data-ttu-id="e0693-175">Этот метод будет вызван из потока рабочей очереди.</span><span class="sxs-lookup"><span data-stu-id="e0693-175">This method will be called from the work queue thread.</span></span>

<span data-ttu-id="e0693-176">Во-первых, нам нужен способ сохранить значение *x*, чтобы его можно было извлечь при вызове потока рабочей очереди `SqrRoot::Invoke` .</span><span class="sxs-lookup"><span data-stu-id="e0693-176">First, we need a way to store the value of *x*, so that it can be retrieved when the work queue thread calls `SqrRoot::Invoke`.</span></span> <span data-ttu-id="e0693-177">Ниже приведен простой класс, в котором хранится информация:</span><span class="sxs-lookup"><span data-stu-id="e0693-177">Here is a simple class that stores the information:</span></span>


```C++
class AsyncOp : public IUnknown
{
    LONG    m_cRef;

public:

    double  m_value;

    AsyncOp(double val) : m_cRef(1), m_value(val) { }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(AsyncOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



<span data-ttu-id="e0693-178">Этот класс реализует **IUnknown** , чтобы его можно было сохранить в результирующем объекте.</span><span class="sxs-lookup"><span data-stu-id="e0693-178">This class implements **IUnknown** so that it can be stored in a result object.</span></span>

<span data-ttu-id="e0693-179">Следующий код реализует `BeginSquareRoot` метод:</span><span class="sxs-lookup"><span data-stu-id="e0693-179">The following code implements the `BeginSquareRoot` method:</span></span>


```C++
HRESULT SqrRoot::BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState)
{
    AsyncOp *pOp = new (std::nothrow) AsyncOp(x);
    if (pOp == NULL)
    {
        return E_OUTOFMEMORY;
    }

    IMFAsyncResult *pResult = NULL;

    // Create the inner result object. This object contains pointers to:
    // 
    //   1. The caller's callback interface and state object. 
    //   2. The AsyncOp object, which contains the operation data.
    //

    HRESULT hr = MFCreateAsyncResult(pOp, pCB, pState, &pResult);

    if (SUCCEEDED(hr))
    {
        // Queue a work item. The work item contains pointers to:
        // 
        // 1. The callback interface of the SqrRoot object.
        // 2. The inner result object.

        hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_STANDARD, this, pResult);

        pResult->Release();
    }

    return hr;
}
```



<span data-ttu-id="e0693-180">Этот код делает следующее:</span><span class="sxs-lookup"><span data-stu-id="e0693-180">This code does the following:</span></span>

1.  <span data-ttu-id="e0693-181">Создает новый экземпляр `AsyncOp` класса для хранения значения *x*.</span><span class="sxs-lookup"><span data-stu-id="e0693-181">Creates a new instance of the `AsyncOp` class to hold the value of *x*.</span></span>
2.  <span data-ttu-id="e0693-182">Вызывает [**мфкреатеасинкресулт**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) для создания результирующего объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-182">Calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a result object.</span></span> <span data-ttu-id="e0693-183">Этот объект содержит несколько указателей:</span><span class="sxs-lookup"><span data-stu-id="e0693-183">This object holds several pointers:</span></span>
    -   <span data-ttu-id="e0693-184">Указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-184">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="e0693-185">Указатель на объект состояния вызывающего объекта (*пстате*).</span><span class="sxs-lookup"><span data-stu-id="e0693-185">A pointer to the caller's state object (*pState*).</span></span>
    -   <span data-ttu-id="e0693-186">Указатель на объект `AsyncOp`.</span><span class="sxs-lookup"><span data-stu-id="e0693-186">A pointer to the `AsyncOp` object.</span></span>
3.  <span data-ttu-id="e0693-187">Вызывает [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) для постановки нового рабочего элемента в очередь.</span><span class="sxs-lookup"><span data-stu-id="e0693-187">Calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item.</span></span> <span data-ttu-id="e0693-188">Этот вызов неявно создает внешний результирующий объект, содержащий следующие указатели:</span><span class="sxs-lookup"><span data-stu-id="e0693-188">This call implicitly creates an outer result object, which holds the following pointers:</span></span>
    -   <span data-ttu-id="e0693-189">Указатель на `SqrRoot` интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-189">A pointer to the `SqrRoot` object's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="e0693-190">Указатель на объект внутреннего результата из шага 2.</span><span class="sxs-lookup"><span data-stu-id="e0693-190">A pointer to the inner result object from step 2.</span></span>

<span data-ttu-id="e0693-191">Следующий код реализует `SqrRoot::Invoke` метод:</span><span class="sxs-lookup"><span data-stu-id="e0693-191">The following code implements the `SqrRoot::Invoke` method:</span></span>


```C++
// Invoke is called by the work queue. This is where the object performs the
// asynchronous operation.

STDMETHODIMP SqrRoot::Invoke(IMFAsyncResult* pResult)
{
    HRESULT hr = S_OK;

    IUnknown *pState = NULL;
    IUnknown *pUnk = NULL;
    IMFAsyncResult *pCallerResult = NULL;

    AsyncOp *pOp = NULL; 

    // Get the asynchronous result object for the application callback. 

    hr = pResult->GetState(&pState);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pState->QueryInterface(IID_PPV_ARGS(&pCallerResult));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the object that holds the state information for the asynchronous method.
    hr = pCallerResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    pOp = static_cast<AsyncOp*>(pUnk);

    // Do the work.

    hr = DoCalculateSquareRoot(pOp);

done:
    // Signal the application.
    if (pCallerResult)
    {
        pCallerResult->SetStatus(hr);
        MFInvokeCallback(pCallerResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pUnk);
    SafeRelease(&pCallerResult);
    return S_OK;
}
```



<span data-ttu-id="e0693-192">Этот метод получает объект внутреннего результата и `AsyncOp` объект.</span><span class="sxs-lookup"><span data-stu-id="e0693-192">This method gets the inner result object and the `AsyncOp` object.</span></span> <span data-ttu-id="e0693-193">Затем он передает `AsyncOp` объект в `DoCalculateSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="e0693-193">Then it passes the `AsyncOp` object to `DoCalculateSquareRoot`.</span></span> <span data-ttu-id="e0693-194">Наконец, он вызывает [**имфасинкресулт:: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) , чтобы задать код состояния и [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) для вызова метода обратного вызова вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-194">Finally, it calls [**IMFAsyncResult::SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) to set the status code and [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>

<span data-ttu-id="e0693-195">`DoCalculateSquareRoot`Метод выполняет именно то, что вы бы хотели:</span><span class="sxs-lookup"><span data-stu-id="e0693-195">The `DoCalculateSquareRoot` method does exactly what you would expect:</span></span>


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



<span data-ttu-id="e0693-196">Когда вызывается метод обратного вызова вызывающего метода, он отвечает за вызов метода **End...** , в данном случае — `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="e0693-196">When the caller's callback method is invoked, it is the caller's responsibility to call the **End...** method—in this case, `EndSquareRoot`.</span></span> <span data-ttu-id="e0693-197">`EndSquareRoot`— Это то, как вызывающий объект получает результат асинхронной операции, в данном примере — вычисленный квадратный корень.</span><span class="sxs-lookup"><span data-stu-id="e0693-197">The `EndSquareRoot` is how the caller retrieves the result of the asynchronous operation, which in this example is the computed square root.</span></span> <span data-ttu-id="e0693-198">Эти сведения хранятся в объекте result:</span><span class="sxs-lookup"><span data-stu-id="e0693-198">This information is stored in the result object:</span></span>


```C++
HRESULT SqrRoot::EndSquareRoot(IMFAsyncResult *pResult, double *pVal)
{
    *pVal = 0;

    IUnknown *pUnk = NULL;

    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    AsyncOp *pOp = static_cast<AsyncOp*>(pUnk);

    // Get the result.
    *pVal = pOp->m_value;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="operation-queues"></a><span data-ttu-id="e0693-199">Очереди операций</span><span class="sxs-lookup"><span data-stu-id="e0693-199">Operation Queues</span></span>

<span data-ttu-id="e0693-200">До сих пор таЦитли предполагается, что асинхронная операция может быть выполнена в любое время независимо от текущего состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-200">So far, it has been tacitly assumed that an asynchronous operation could be done at any time, regardless of the object's current state.</span></span> <span data-ttu-id="e0693-201">Например, рассмотрим, что происходит, если приложение вызывает `BeginSquareRoot` , пока предыдущий вызов того же метода все еще находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="e0693-201">For example, consider what happens if an application calls `BeginSquareRoot` while an earlier call to the same method is still pending.</span></span> <span data-ttu-id="e0693-202">`SqrRoot`Класс может поставить новый рабочий элемент в очередь перед выполнением предыдущего рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="e0693-202">The `SqrRoot` class might queue the new work item before the previous work item is done.</span></span> <span data-ttu-id="e0693-203">Однако в рабочих очередях не гарантируется сериализация рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="e0693-203">However, work queues are not guaranteed to serialize work items.</span></span> <span data-ttu-id="e0693-204">Помните, что Рабочая очередь может использовать более одного потока для диспетчеризации рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="e0693-204">Recall that a work queue can use more than one thread to dispatch work items.</span></span> <span data-ttu-id="e0693-205">В многопоточной среде рабочий элемент может быть вызван до завершения предыдущего.</span><span class="sxs-lookup"><span data-stu-id="e0693-205">In a multithreaded environment, a work item might be invoked before the previous one has completed.</span></span> <span data-ttu-id="e0693-206">Рабочие элементы можно даже вызывать неупорядоченно, если переключение контекста происходит непосредственно перед вызовом обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e0693-206">Work items can even be invoked out of order, if a context switch happens to occur just before the callback is invoked.</span></span>

<span data-ttu-id="e0693-207">По этой причине объект отвечает за сериализацию операций, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="e0693-207">For this reason, it is the object's responsibility to serialize operations on itself, if required.</span></span> <span data-ttu-id="e0693-208">Иными словами, если для работы объекта требуется операция *а* , прежде чем операция *б* может быть запущена, объект не должен ставить в очередь рабочий элемент для *B* до завершения операции *A* .</span><span class="sxs-lookup"><span data-stu-id="e0693-208">In other words, if the object requires operation *A* to finish before operation *B* can start, the object must not queue a work item for *B* until operation *A* has completed.</span></span> <span data-ttu-id="e0693-209">Объект может удовлетворить это требование, используя собственную очередь ожидающих операций.</span><span class="sxs-lookup"><span data-stu-id="e0693-209">An object can meet this requirement by having its own queue of pending operations.</span></span> <span data-ttu-id="e0693-210">При вызове асинхронного метода для объекта объект помещает запрос в собственную очередь.</span><span class="sxs-lookup"><span data-stu-id="e0693-210">When an asynchronous method is called on the object, the object puts the request on its own queue.</span></span> <span data-ttu-id="e0693-211">По мере завершения каждой асинхронной операции объект извлекает следующий запрос из очереди.</span><span class="sxs-lookup"><span data-stu-id="e0693-211">As each asynchronous operation is completed, the object pulls the next request from the queue.</span></span> <span data-ttu-id="e0693-212">В примере [MPEG1Source](mpeg1source-sample.md) показан пример реализации такой очереди.</span><span class="sxs-lookup"><span data-stu-id="e0693-212">The [MPEG1Source Sample](mpeg1source-sample.md) shows an example of how to implement such a queue.</span></span>

<span data-ttu-id="e0693-213">Один метод может содержать несколько асинхронных операций, особенно при использовании вызовов ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e0693-213">A single method might involve several asynchronous operations, particularly when I/O calls are used.</span></span> <span data-ttu-id="e0693-214">При реализации асинхронных методов следует тщательно продумать требования сериализации.</span><span class="sxs-lookup"><span data-stu-id="e0693-214">When you implement asynchronous methods, think carefully about serialization requirements.</span></span> <span data-ttu-id="e0693-215">Например, является ли объект допустимым для запуска новой операции, когда предыдущий запрос ввода-вывода все еще находится в состоянии ожидания?</span><span class="sxs-lookup"><span data-stu-id="e0693-215">For example, is it valid for the object to start a new operation while a previous I/O request is still pending?</span></span> <span data-ttu-id="e0693-216">Если новая операция изменяет внутреннее состояние объекта, что происходит при завершении предыдущего запроса ввода-вывода и возвращает данные, которые теперь могут быть устаревшими?</span><span class="sxs-lookup"><span data-stu-id="e0693-216">If the new operation changes the object's internal state, what happens when a previous I/O request completes and returns data that might now be stale?</span></span> <span data-ttu-id="e0693-217">Хорошая Схема состояний может помочь определить допустимые переходы между состояниями.</span><span class="sxs-lookup"><span data-stu-id="e0693-217">A good state diagram can help to identify the valid state transitions.</span></span>

## <a name="cross-thread-and-cross-process-considerations"></a><span data-ttu-id="e0693-218">Рекомендации между потоками и между процессами</span><span class="sxs-lookup"><span data-stu-id="e0693-218">Cross-Thread and Cross-Process Considerations</span></span>

<span data-ttu-id="e0693-219">Рабочие очереди не используют упаковку COM для маршалирования указателей на интерфейсы через границы потоков.</span><span class="sxs-lookup"><span data-stu-id="e0693-219">Work queues do not use COM marshaling to marshal interface pointers across thread boundaries.</span></span> <span data-ttu-id="e0693-220">Таким образом, даже если объект зарегистрирован как потоковое подразделение или поток приложения вошел в однопотоковое подразделение (STA), обратные вызовы [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) будут вызываться из другого потока.</span><span class="sxs-lookup"><span data-stu-id="e0693-220">Therefore, even if an object is registered as apartment-threaded or the application thread has entered a single-threaded apartment (STA), [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callbacks will be invoked from a different thread.</span></span> <span data-ttu-id="e0693-221">В любом случае все компоненты конвейера Media Foundation должны использовать модель потоков "both".</span><span class="sxs-lookup"><span data-stu-id="e0693-221">In any case, all Media Foundation pipeline components should use the "Both" threading model.</span></span>

<span data-ttu-id="e0693-222">Некоторые интерфейсы в Media Foundation определяют удаленные версии некоторых асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="e0693-222">Some interfaces in Media Foundation define remote versions of some asynchronous methods.</span></span> <span data-ttu-id="e0693-223">Когда один из этих методов вызывается через границы процесса, Библиотека DLL прокси Media Foundation/заглушка вызывает удаленную версию метода, который выполняет настраиваемый маршалирование параметров метода.</span><span class="sxs-lookup"><span data-stu-id="e0693-223">When one of these methods is called across process boundaries, the Media Foundation proxy/stub DLL calls the remote version of the method, which performs custom marshaling of the method parameters.</span></span> <span data-ttu-id="e0693-224">В удаленном процессе заглушка преобразует обратный вызов в локальный метод объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-224">In the remote process, the stub translates the call back into the local method on the object.</span></span> <span data-ttu-id="e0693-225">Этот процесс прозрачен как для приложения, так и для удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="e0693-225">This process is transparent to both the application and the remote object.</span></span> <span data-ttu-id="e0693-226">Эти пользовательские методы маршалирования предоставляются в основном для объектов, загруженных в пути к защищенному носителю (PMP).</span><span class="sxs-lookup"><span data-stu-id="e0693-226">These custom marshaling methods are provided primarily for objects that are loaded in the protected media path (PMP).</span></span> <span data-ttu-id="e0693-227">Дополнительные сведения о PMP см. в разделе [путь к защищенному носителю](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="e0693-227">For more information about the PMP, see [Protected Media Path](protected-media-path.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0693-228">См. также</span><span class="sxs-lookup"><span data-stu-id="e0693-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0693-229">Асинхронные методы обратного вызова</span><span class="sxs-lookup"><span data-stu-id="e0693-229">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> <dt>

[<span data-ttu-id="e0693-230">Рабочие очереди</span><span class="sxs-lookup"><span data-stu-id="e0693-230">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 



