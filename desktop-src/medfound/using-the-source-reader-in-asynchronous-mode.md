---
description: В этом разделе описывается использование модуля чтения исходного кода в асинхронном режиме.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Использование модуля чтения исходного кода в асинхронном режиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d0405cb3e594d059b7c93e793250e0be88562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080427"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a><span data-ttu-id="ff5cf-103">Использование модуля чтения исходного кода в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="ff5cf-103">Using the Source Reader in Asynchronous Mode</span></span>

<span data-ttu-id="ff5cf-104">В этом разделе описывается использование [модуля чтения исходного кода](source-reader.md) в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-104">This topic describes how to use the [Source Reader](source-reader.md) in asynchronous mode.</span></span> <span data-ttu-id="ff5cf-105">В асинхронном режиме приложение предоставляет интерфейс обратного вызова, который используется для уведомления приложения о доступности данных.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-105">In asynchronous mode, the application provides a callback interface, which is used to notify the application that data is available.</span></span>

<span data-ttu-id="ff5cf-106">В этом разделе предполагается, что вы уже прочитали раздел [Использование модуля чтения исходного кода для обработки данных мультимедиа](processing-media-data-with-the-source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="ff5cf-106">This topic assumes that you have already read the topic [Using the Source Reader to Process Media Data](processing-media-data-with-the-source-reader.md).</span></span>

## <a name="using-asynchronous-mode"></a><span data-ttu-id="ff5cf-107">Использование асинхронного режима</span><span class="sxs-lookup"><span data-stu-id="ff5cf-107">Using Asynchronous Mode</span></span>

<span data-ttu-id="ff5cf-108">Модуль чтения исходного кода работает как в синхронном, так и в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-108">The Source Reader operates either in synchronous mode or asynchronous mode.</span></span> <span data-ttu-id="ff5cf-109">В примере кода, приведенном в предыдущем разделе, предполагается, что модуль чтения источника использует синхронный режим, который является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-109">The code example shown in the previous section assumes that the Source Reader is using synchronous mode, which is the default.</span></span> <span data-ttu-id="ff5cf-110">В синхронном режиме метод [**имфсаурцереадер:: реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) блокируется, пока источник мультимедиа создает следующий образец.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-110">In synchronous mode, the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method blocks while the media source produces the next sample.</span></span> <span data-ttu-id="ff5cf-111">Источник мультимедиа обычно получает данные из какого-либо внешнего источника (например, локального файла или сетевого подключения), поэтому метод может блокировать вызывающий поток на длительное время.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-111">A media source typically acquires data from some external source (such as a local file or a network connection), so the method can block the calling thread for a noticeable amount of time.</span></span>

<span data-ttu-id="ff5cf-112">В асинхронном режиме [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) немедленно возвращает, а работа выполняется в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-112">In asynchronous mode, the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) returns immediately and the work is performed on another thread.</span></span> <span data-ttu-id="ff5cf-113">После завершения операции модуль чтения исходного кода вызывает приложение через интерфейс обратного вызова [**имфсаурцереадеркаллбакк**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) .</span><span class="sxs-lookup"><span data-stu-id="ff5cf-113">After the operation is complete, the Source Reader calls the application through the [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) callback interface.</span></span> <span data-ttu-id="ff5cf-114">Чтобы использовать асинхронный режим, необходимо предоставить указатель обратного вызова при первом создании модуля чтения исходного кода, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-114">To use asynchronous mode, you must provide a callback pointer when you first create the Source Reader, as follows:</span></span>

1.  <span data-ttu-id="ff5cf-115">Создайте хранилище атрибутов, вызвав функцию [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="ff5cf-115">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
2.  <span data-ttu-id="ff5cf-116">Установите атрибут [ \_ \_ \_ асинхронного \_ обратного вызова MF Source](mf-source-reader-async-callback.md) для хранилища атрибутов.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-116">Set the [MF\_SOURCE\_READER\_ASYNC\_CALLBACK](mf-source-reader-async-callback.md) attribute on the attribute store.</span></span> <span data-ttu-id="ff5cf-117">Значение атрибута является указателем на объект обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-117">The attribute value is a pointer to your callback object.</span></span>
3.  <span data-ttu-id="ff5cf-118">При создании модуля чтения исходного кода передайте хранилище атрибутов в функцию создания в параметре *паттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="ff5cf-118">When you create the Source Reader, pass the attribute store to the creation function in the *pAttributes* parameter.</span></span> <span data-ttu-id="ff5cf-119">Все функции, создающие модуль чтения исходного кода, имеют этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-119">All of the functions to create the Source Reader have this parameter.</span></span>

<span data-ttu-id="ff5cf-120">Следующий пример показывает эти шаги.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-120">The following example shows these steps.</span></span>


```C++
HRESULT CreateSourceReaderAsync(
    PCWSTR pszURL, 
    IMFSourceReaderCallback *pCallback, 
    IMFSourceReader **ppReader)
{
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAttributes->SetUnknown(MF_SOURCE_READER_ASYNC_CALLBACK, pCallback);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateSourceReaderFromURL(pszURL, pAttributes, ppReader);

done:
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="ff5cf-121">После создания модуля чтения исходного кода нельзя переключаться между режимами синхронного и асинхронного.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-121">After you create the Source Reader, you cannot switch modes between synchronous and asynchronous.</span></span>

<span data-ttu-id="ff5cf-122">Чтобы получить данные в асинхронном режиме, вызовите метод [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , но установите последние четыре параметра в **значение NULL**, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-122">To get data in asynchronous mode, call the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method but set the last four parameters to **NULL**, as shown in the following example.</span></span>


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



<span data-ttu-id="ff5cf-123">Когда метод [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) завершается асинхронно, модуль чтения исходного кода вызывает метод [**Имфсаурцереадеркаллбакк:: онреадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) .</span><span class="sxs-lookup"><span data-stu-id="ff5cf-123">When the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method completes asynchronously, the Source Reader calls your [**IMFSourceReaderCallback::OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method.</span></span> <span data-ttu-id="ff5cf-124">Этот метод имеет пять параметров:</span><span class="sxs-lookup"><span data-stu-id="ff5cf-124">This method has five parameters:</span></span>

-   <span data-ttu-id="ff5cf-125">*хрстатус*: содержит значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff5cf-125">*hrStatus*: Contains an **HRESULT** value.</span></span> <span data-ttu-id="ff5cf-126">Это то же значение, которое [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) бы возвратить в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-126">This is the same value that [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) would return in synchronous mode.</span></span> <span data-ttu-id="ff5cf-127">Если *хрстатус* содержит код ошибки, оставшиеся параметры можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-127">If *hrStatus* contains an error code, you can ignore the remaining parameters.</span></span>
-   <span data-ttu-id="ff5cf-128">*двстреаминдекс*, *двстреамфлагс*, ллтиместамп и *псампле*: эти три параметра эквивалентны последним трем параметрам в [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="ff5cf-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp, and *pSample*: These three parameters are equivalent to the last three parameters in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="ff5cf-129">Они содержат номер потока, флаги состояния и указатель [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) соответственно.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-129">They contain the stream number, status flags, and [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, respectively.</span></span>


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



<span data-ttu-id="ff5cf-130">Кроме того, интерфейс обратного вызова определяет два других метода:</span><span class="sxs-lookup"><span data-stu-id="ff5cf-130">In addition, the callback interface defines two other methods:</span></span>

-   <span data-ttu-id="ff5cf-131">[**Oneven**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span><span class="sxs-lookup"><span data-stu-id="ff5cf-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span></span> <span data-ttu-id="ff5cf-132">Уведомляет приложение, когда в источнике мультимедиа происходят определенные события, например буферизация или события сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-132">Notifies the application when certain events occur in media source, such as buffering or network connection events.</span></span>
-   <span data-ttu-id="ff5cf-133">[**Onflush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span><span class="sxs-lookup"><span data-stu-id="ff5cf-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span></span> <span data-ttu-id="ff5cf-134">Вызывается после завершения метода [**flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) .</span><span class="sxs-lookup"><span data-stu-id="ff5cf-134">Called when the [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) method completes.</span></span>

## <a name="implementing-the-callback-interface"></a><span data-ttu-id="ff5cf-135">Реализация интерфейса обратного вызова</span><span class="sxs-lookup"><span data-stu-id="ff5cf-135">Implementing the Callback Interface</span></span>

<span data-ttu-id="ff5cf-136">Интерфейс обратного вызова должен быть потокобезопасным, так как [**онреадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) и другие методы обратного вызова вызываются из рабочих потоков.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-136">The callback interface must be thread-safe, because [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) and the other callback methods are called from worker threads.</span></span>

<span data-ttu-id="ff5cf-137">При реализации обратного вызова можно выполнить несколько различных подходов.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-137">There are several different approaches you can take when you implement the callback.</span></span> <span data-ttu-id="ff5cf-138">Например, можно выполнить всю работу внутри обратного вызова или использовать обратный вызов, чтобы уведомить приложение (например, сообщить дескриптору события), а затем выполнить действия из потока приложения.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-138">For example, you can do all of the work inside the callback, or you can use the callback to notify the application (for example, by signaling an event handle) and then do work from the application thread.</span></span>

<span data-ttu-id="ff5cf-139">Метод [**онреадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) будет вызываться по одному разу для каждого вызова, внесенного в метод [**Имфсаурцереадер:: реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) .</span><span class="sxs-lookup"><span data-stu-id="ff5cf-139">The [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method will be called once for every call that you make to the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method.</span></span> <span data-ttu-id="ff5cf-140">Чтобы получить следующий пример, вызовите **реадсампле** еще раз.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-140">To get the next sample, call **ReadSample** again.</span></span> <span data-ttu-id="ff5cf-141">При возникновении ошибки **онреадсампле** вызывается с кодом ошибки для параметра *хрстатус* .</span><span class="sxs-lookup"><span data-stu-id="ff5cf-141">If an error occurs, **OnReadSample** is called with an error code for the *hrStatus* parameter.</span></span>

<span data-ttu-id="ff5cf-142">В следующем примере показана минимальная реализация интерфейса обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-142">The following example shows a minimal implementation of the callback interface.</span></span> <span data-ttu-id="ff5cf-143">Во-первых, ниже приведено объявление класса, реализующего интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-143">First, here is the declaration of a class that implements the interface.</span></span>


```C++
#include <shlwapi.h>

class SourceReaderCB : public IMFSourceReaderCallback
{
public:
    SourceReaderCB(HANDLE hEvent) : 
      m_nRefCount(1), m_hEvent(hEvent), m_bEOS(FALSE), m_hrStatus(S_OK)
    {
        InitializeCriticalSection(&m_critsec);
    }

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(SourceReaderCB, IMFSourceReaderCallback),
            { 0 },
        };
        return QISearch(this, qit, iid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // IMFSourceReaderCallback methods
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);

    STDMETHODIMP OnEvent(DWORD, IMFMediaEvent *)
    {
        return S_OK;
    }

    STDMETHODIMP OnFlush(DWORD)
    {
        return S_OK;
    }

public:
    HRESULT Wait(DWORD dwMilliseconds, BOOL *pbEOS)
    {
        *pbEOS = FALSE;

        DWORD dwResult = WaitForSingleObject(m_hEvent, dwMilliseconds);
        if (dwResult == WAIT_TIMEOUT)
        {
            return E_PENDING;
        }
        else if (dwResult != WAIT_OBJECT_0)
        {
            return HRESULT_FROM_WIN32(GetLastError());
        }

        *pbEOS = m_bEOS;
        return m_hrStatus;
    }
    
private:
    
    // Destructor is private. Caller should call Release.
    virtual ~SourceReaderCB() 
    {
    }

    void NotifyError(HRESULT hr)
    {
        wprintf(L"Source Reader error: 0x%X\n", hr);
    }

private:
    long                m_nRefCount;        // Reference count.
    CRITICAL_SECTION    m_critsec;
    HANDLE              m_hEvent;
    BOOL                m_bEOS;
    HRESULT             m_hrStatus;

};
```



<span data-ttu-id="ff5cf-144">В этом примере мы не будем заинтересованы в методах [**oneven**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) и [**oneven**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) , поэтому они просто возвращают **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-144">In this example, we are not interested in the [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) and [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) methods, so they simply return **S\_OK**.</span></span> <span data-ttu-id="ff5cf-145">Класс использует дескриптор события для сигнализации приложения; Этот маркер предоставляется через конструктор.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-145">The class uses an event handle to signal the application; this handle is provided through the constructor.</span></span>

<span data-ttu-id="ff5cf-146">В этом минимальном примере метод [**онреадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) просто выводит метку времени в окне консоли.</span><span class="sxs-lookup"><span data-stu-id="ff5cf-146">In this minimal example, the [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method just prints the time stamp to the console window.</span></span> <span data-ttu-id="ff5cf-147">Затем он сохраняет код состояния и флаг конца потока и сигнализирует об обработке события:</span><span class="sxs-lookup"><span data-stu-id="ff5cf-147">Then it stores the status code and the end-of-stream flag, and signals the event handle:</span></span>


```C++
HRESULT SourceReaderCB::OnReadSample(
    HRESULT hrStatus,
    DWORD /* dwStreamIndex */,
    DWORD dwStreamFlags,
    LONGLONG llTimestamp,
    IMFSample *pSample      // Can be NULL
    )
{
    EnterCriticalSection(&m_critsec);

    if (SUCCEEDED(hrStatus))
    {
        if (pSample)
        {
            // Do something with the sample.
            wprintf(L"Frame @ %I64d\n", llTimestamp);
        }
    }
    else
    {
        // Streaming error.
        NotifyError(hrStatus);
    }

    if (MF_SOURCE_READERF_ENDOFSTREAM & dwStreamFlags)
    {
        // Reached the end of the stream.
        m_bEOS = TRUE;
    }
    m_hrStatus = hrStatus;

    LeaveCriticalSection(&m_critsec);
    SetEvent(m_hEvent);
    return S_OK;
}
```



<span data-ttu-id="ff5cf-148">В следующем коде показано, как приложение будет использовать этот класс обратного вызова для чтения всех видеокадров из файла мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="ff5cf-148">The following code shows the application would use this callback class to read all of the video frames from a media file:</span></span>


```C++
HRESULT ReadMediaFile(PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    SourceReaderCB *pCallback = NULL;

    HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto done;
    }

    // Create an instance of the callback object.
    pCallback = new (std::nothrow) SourceReaderCB(hEvent);
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Create the Source Reader.
    hr = CreateSourceReaderAsync(pszURL, pCallback, &pReader);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConfigureDecoder(pReader, MF_SOURCE_READER_FIRST_VIDEO_STREAM);
    if (FAILED(hr))
    {
        goto done;
    }

    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    while (SUCCEEDED(hr))
    {
        BOOL bEOS;
        hr = pCallback->Wait(INFINITE, &bEOS);
        if (FAILED(hr) || bEOS)
        {
            break;
        }
        hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM,
            0, NULL, NULL, NULL, NULL);
    }

done:
    SafeRelease(&pReader);
    SafeRelease(&pCallback);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ff5cf-149">См. также</span><span class="sxs-lookup"><span data-stu-id="ff5cf-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff5cf-150">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="ff5cf-150">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 



