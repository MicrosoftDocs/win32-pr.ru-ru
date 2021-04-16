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
# <a name="writing-an-asynchronous-method"></a>Создание асинхронного метода

В этом разделе описано, как реализовать асинхронный метод в Microsoft Media Foundation.

Асинхронные методы являются повсеместными в Media Foundation конвейере. Асинхронные методы упрощают распределение работы между несколькими потоками. Особенно важно выполнять операции ввода-вывода асинхронно, чтобы чтение из файла или сети не блокировало остальную часть конвейера.

При написании источника мультимедиа или приемника мультимедиа очень важно правильно выполнять асинхронные операции, так как производительность компонента влияет на весь конвейер.

> [!Note]  
> Media Foundation преобразования (МФТС) по умолчанию используют синхронные методы.

 

### <a name="work-queues-for-asynchronous-operations"></a>Рабочие очереди для асинхронных операций

В Media Foundation существует замкнутая связь между [асинхронными методами обратного вызова](asynchronous-callback-methods.md) и [рабочими очередями](work-queues.md). Рабочая очередь — это абстракция для перемещения работы из потока вызывающего объекта в рабочий поток. Чтобы выполнить работу в рабочей очереди, выполните следующие действия.

1.  Реализуйте интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
2.  Вызовите [**мфкреатеасинкресулт**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) , чтобы создать *результирующий* объект. Объект Result предоставляет [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult). Результирующий объект содержит три указателя:

    -   Указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) вызывающего объекта.
    -   Необязательный указатель на объект состояния. Если этот параметр указан, объект состояния должен реализовывать **IUnknown**.
    -   Необязательный указатель на закрытый объект. Если этот объект указан, он также должен реализовывать **IUnknown**.

    Последние два указателя могут иметь **значение NULL**. В противном случае используйте их для хранения сведений об асинхронной операции.

3.  Вызовите [**мфпутворкитемекс**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) , чтобы поставить в очередь рабочий элемент.
4.  Поток рабочей очереди вызывает метод [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .
5.  Выполните работу внутри метода [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Параметр *пасинкресулт* этого метода является указателем [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) из шага 2. Используйте этот указатель для получения объекта состояния и закрытого объекта:
    -   Чтобы получить объект состояния, вызовите [**имфасинкресулт::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)GetObject.
    -   Чтобы получить закрытый объект, вызовите метод [**имфасинкресулт:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).

В качестве альтернативы можно объединить шаги 2 и 3, вызвав функцию [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) . На внутреннем уровне эта функция вызывает [**мфкреатеасинкресулт**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) для создания результирующего объекта.

На следующей диаграмме показаны связи между вызывающим объектом, результирующий объект, объект состояния и закрытый объект.

![Схема, показывающая объект асинхронного результата](images/workqueues01.png)

На следующей схеме последовательностей показано, как объект помещает рабочий элемент в очередь. Когда поток рабочей очереди вызывает [**вызов**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), объект выполняет асинхронную операцию в этом потоке.

![Диаграмма, показывающая, как объект помещает рабочий элемент в очередь](images/workqueues02.png)

Важно помнить, что [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) вызывается из потока, который принадлежит рабочей очереди. Реализация **Invoke** должна быть потокобезопасной. Кроме того, при использовании рабочей очереди платформы (**\_ \_ \_ стандартная очередь обратного вызова мфасинк**) крайне важно, чтобы поток не блокировался, так как он может блокировать обработку данных на весь конвейер Media Foundation. Если необходимо выполнить операцию, которая будет блокироваться или занять длительное время, используйте частную рабочую очередь. Чтобы создать частную рабочую очередь, вызовите [**мфаллокатеворккуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Любой компонент конвейера, выполняющий операции ввода-вывода, должен избегать блокирования вызовов ввода-вывода по той же причине. Интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) предоставляет полезную абстракцию для асинхронного файлового ввода-вывода.

### <a name="implementing-the-beginend-pattern"></a>Реализация Begin. ../енд... Пакет

Как описано в разделе [Вызов асинхронных методов](calling-asynchronous-methods.md), асинхронные методы в Media Foundation часто используют инструкцию **Begin...** / **Конец....** пакет. В этом шаблоне асинхронная операция использует два метода с сигнатурами, аналогичные следующим:

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

Чтобы сделать метод действительно асинхронным, реализация **бегинкс** должна выполнить фактическую работу в другом потоке. Именно здесь на изображении поступают рабочие очереди. В следующих шагах *вызывающий объект* является кодом, который вызывает **бегинкс** и **ендкс**. Это может быть приложение или конвейер Media Foundation. *Компонент* — это код, реализующий **бегинкс** и **ендкс**.

1.  Вызывающий объект вызывает **Begin...**, передавая указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) вызывающего объекта.
2.  Компонент создает новый объект асинхронного результата. Этот объект хранит интерфейс обратного вызова и объект состояния вызывающего объекта. Как правило, он также хранит все сведения о закрытом состоянии, необходимые компоненту для выполнения операции. Результирующий объект этого шага помечается как "result 1" на следующей схеме.
3.  Компонент создает второй результирующий объект. В этом результирующем объекте хранятся два указателя: первый результирующий объект и интерфейс обратного вызова вызываемого объекта. Этот результирующий объект помечается как "результат 2" на следующей схеме.
4.  Компонент вызывает [**мфпутворкитемекс**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) для постановки в очередь нового рабочего элемента.
5.  В методе [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) компонент выполняет асинхронную работу.
6.  Компонент вызывает [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) для вызова метода обратного вызова вызывающего объекта.
7.  Вызывающий объект вызывает метод **ендкс** .

![Схема, показывающая, как объект реализует шаблон начала/окончания](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>Пример асинхронного метода

Чтобы проиллюстрировать это обсуждение, мы будем использовать пример надуманный. Рассмотрим асинхронный метод для вычисления квадратного корня:


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



Параметр *x* аргумента `BeginSquareRoot` — это значение, для которого вычисляется квадратный корень. Квадратный корень возвращается в параметре *Pval* объекта `EndSquareRoot` .

Ниже приведено объявление класса, который реализует эти два метода:


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



`SqrRoot`Класс реализует [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , чтобы он мог поместить операцию с квадратным корнем в рабочую очередь. `DoCalculateSquareRoot`Метод является закрытым методом класса, который вычисляет квадратный корень. Этот метод будет вызван из потока рабочей очереди.

Во-первых, нам нужен способ сохранить значение *x*, чтобы его можно было извлечь при вызове потока рабочей очереди `SqrRoot::Invoke` . Ниже приведен простой класс, в котором хранится информация:


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



Этот класс реализует **IUnknown** , чтобы его можно было сохранить в результирующем объекте.

Следующий код реализует `BeginSquareRoot` метод:


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



Этот код делает следующее:

1.  Создает новый экземпляр `AsyncOp` класса для хранения значения *x*.
2.  Вызывает [**мфкреатеасинкресулт**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) для создания результирующего объекта. Этот объект содержит несколько указателей:
    -   Указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) вызывающего объекта.
    -   Указатель на объект состояния вызывающего объекта (*пстате*).
    -   Указатель на объект `AsyncOp`.
3.  Вызывает [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) для постановки нового рабочего элемента в очередь. Этот вызов неявно создает внешний результирующий объект, содержащий следующие указатели:
    -   Указатель на `SqrRoot` интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) объекта.
    -   Указатель на объект внутреннего результата из шага 2.

Следующий код реализует `SqrRoot::Invoke` метод:


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



Этот метод получает объект внутреннего результата и `AsyncOp` объект. Затем он передает `AsyncOp` объект в `DoCalculateSquareRoot` . Наконец, он вызывает [**имфасинкресулт:: SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) , чтобы задать код состояния и [**мфинвокекаллбакк**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) для вызова метода обратного вызова вызывающего объекта.

`DoCalculateSquareRoot`Метод выполняет именно то, что вы бы хотели:


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



Когда вызывается метод обратного вызова вызывающего метода, он отвечает за вызов метода **End...** , в данном случае — `EndSquareRoot` . `EndSquareRoot`— Это то, как вызывающий объект получает результат асинхронной операции, в данном примере — вычисленный квадратный корень. Эти сведения хранятся в объекте result:


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



## <a name="operation-queues"></a>Очереди операций

До сих пор таЦитли предполагается, что асинхронная операция может быть выполнена в любое время независимо от текущего состояния объекта. Например, рассмотрим, что происходит, если приложение вызывает `BeginSquareRoot` , пока предыдущий вызов того же метода все еще находится в состоянии ожидания. `SqrRoot`Класс может поставить новый рабочий элемент в очередь перед выполнением предыдущего рабочего элемента. Однако в рабочих очередях не гарантируется сериализация рабочих элементов. Помните, что Рабочая очередь может использовать более одного потока для диспетчеризации рабочих элементов. В многопоточной среде рабочий элемент может быть вызван до завершения предыдущего. Рабочие элементы можно даже вызывать неупорядоченно, если переключение контекста происходит непосредственно перед вызовом обратного вызова.

По этой причине объект отвечает за сериализацию операций, если это необходимо. Иными словами, если для работы объекта требуется операция *а* , прежде чем операция *б* может быть запущена, объект не должен ставить в очередь рабочий элемент для *B* до завершения операции *A* . Объект может удовлетворить это требование, используя собственную очередь ожидающих операций. При вызове асинхронного метода для объекта объект помещает запрос в собственную очередь. По мере завершения каждой асинхронной операции объект извлекает следующий запрос из очереди. В примере [MPEG1Source](mpeg1source-sample.md) показан пример реализации такой очереди.

Один метод может содержать несколько асинхронных операций, особенно при использовании вызовов ввода-вывода. При реализации асинхронных методов следует тщательно продумать требования сериализации. Например, является ли объект допустимым для запуска новой операции, когда предыдущий запрос ввода-вывода все еще находится в состоянии ожидания? Если новая операция изменяет внутреннее состояние объекта, что происходит при завершении предыдущего запроса ввода-вывода и возвращает данные, которые теперь могут быть устаревшими? Хорошая Схема состояний может помочь определить допустимые переходы между состояниями.

## <a name="cross-thread-and-cross-process-considerations"></a>Рекомендации между потоками и между процессами

Рабочие очереди не используют упаковку COM для маршалирования указателей на интерфейсы через границы потоков. Таким образом, даже если объект зарегистрирован как потоковое подразделение или поток приложения вошел в однопотоковое подразделение (STA), обратные вызовы [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) будут вызываться из другого потока. В любом случае все компоненты конвейера Media Foundation должны использовать модель потоков "both".

Некоторые интерфейсы в Media Foundation определяют удаленные версии некоторых асинхронных методов. Когда один из этих методов вызывается через границы процесса, Библиотека DLL прокси Media Foundation/заглушка вызывает удаленную версию метода, который выполняет настраиваемый маршалирование параметров метода. В удаленном процессе заглушка преобразует обратный вызов в локальный метод объекта. Этот процесс прозрачен как для приложения, так и для удаленного объекта. Эти пользовательские методы маршалирования предоставляются в основном для объектов, загруженных в пути к защищенному носителю (PMP). Дополнительные сведения о PMP см. в разделе [путь к защищенному носителю](protected-media-path.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Асинхронные методы обратного вызова](asynchronous-callback-methods.md)
</dt> <dt>

[Рабочие очереди](work-queues.md)
</dt> </dl>

 

 



