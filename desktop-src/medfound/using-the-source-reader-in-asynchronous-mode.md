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
# <a name="using-the-source-reader-in-asynchronous-mode"></a>Использование модуля чтения исходного кода в асинхронном режиме

В этом разделе описывается использование [модуля чтения исходного кода](source-reader.md) в асинхронном режиме. В асинхронном режиме приложение предоставляет интерфейс обратного вызова, который используется для уведомления приложения о доступности данных.

В этом разделе предполагается, что вы уже прочитали раздел [Использование модуля чтения исходного кода для обработки данных мультимедиа](processing-media-data-with-the-source-reader.md).

## <a name="using-asynchronous-mode"></a>Использование асинхронного режима

Модуль чтения исходного кода работает как в синхронном, так и в асинхронном режиме. В примере кода, приведенном в предыдущем разделе, предполагается, что модуль чтения источника использует синхронный режим, который является значением по умолчанию. В синхронном режиме метод [**имфсаурцереадер:: реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) блокируется, пока источник мультимедиа создает следующий образец. Источник мультимедиа обычно получает данные из какого-либо внешнего источника (например, локального файла или сетевого подключения), поэтому метод может блокировать вызывающий поток на длительное время.

В асинхронном режиме [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) немедленно возвращает, а работа выполняется в другом потоке. После завершения операции модуль чтения исходного кода вызывает приложение через интерфейс обратного вызова [**имфсаурцереадеркаллбакк**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) . Чтобы использовать асинхронный режим, необходимо предоставить указатель обратного вызова при первом создании модуля чтения исходного кода, как показано ниже.

1.  Создайте хранилище атрибутов, вызвав функцию [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .
2.  Установите атрибут [ \_ \_ \_ асинхронного \_ обратного вызова MF Source](mf-source-reader-async-callback.md) для хранилища атрибутов. Значение атрибута является указателем на объект обратного вызова.
3.  При создании модуля чтения исходного кода передайте хранилище атрибутов в функцию создания в параметре *паттрибутес* . Все функции, создающие модуль чтения исходного кода, имеют этот параметр.

Следующий пример показывает эти шаги.


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



После создания модуля чтения исходного кода нельзя переключаться между режимами синхронного и асинхронного.

Чтобы получить данные в асинхронном режиме, вызовите метод [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , но установите последние четыре параметра в **значение NULL**, как показано в следующем примере.


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



Когда метод [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) завершается асинхронно, модуль чтения исходного кода вызывает метод [**Имфсаурцереадеркаллбакк:: онреадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) . Этот метод имеет пять параметров:

-   *хрстатус*: содержит значение **HRESULT** . Это то же значение, которое [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) бы возвратить в синхронном режиме. Если *хрстатус* содержит код ошибки, оставшиеся параметры можно игнорировать.
-   *двстреаминдекс*, *двстреамфлагс*, ллтиместамп и *псампле*: эти три параметра эквивалентны последним трем параметрам в [**реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Они содержат номер потока, флаги состояния и указатель [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) соответственно.


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



Кроме того, интерфейс обратного вызова определяет два других метода:

-   [**Oneven**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent). Уведомляет приложение, когда в источнике мультимедиа происходят определенные события, например буферизация или события сетевого подключения.
-   [**Onflush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush). Вызывается после завершения метода [**flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) .

## <a name="implementing-the-callback-interface"></a>Реализация интерфейса обратного вызова

Интерфейс обратного вызова должен быть потокобезопасным, так как [**онреадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) и другие методы обратного вызова вызываются из рабочих потоков.

При реализации обратного вызова можно выполнить несколько различных подходов. Например, можно выполнить всю работу внутри обратного вызова или использовать обратный вызов, чтобы уведомить приложение (например, сообщить дескриптору события), а затем выполнить действия из потока приложения.

Метод [**онреадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) будет вызываться по одному разу для каждого вызова, внесенного в метод [**Имфсаурцереадер:: реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) . Чтобы получить следующий пример, вызовите **реадсампле** еще раз. При возникновении ошибки **онреадсампле** вызывается с кодом ошибки для параметра *хрстатус* .

В следующем примере показана минимальная реализация интерфейса обратного вызова. Во-первых, ниже приведено объявление класса, реализующего интерфейс.


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



В этом примере мы не будем заинтересованы в методах [**oneven**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) и [**oneven**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) , поэтому они просто возвращают **S \_ ОК**. Класс использует дескриптор события для сигнализации приложения; Этот маркер предоставляется через конструктор.

В этом минимальном примере метод [**онреадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) просто выводит метку времени в окне консоли. Затем он сохраняет код состояния и флаг конца потока и сигнализирует об обработке события:


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



В следующем коде показано, как приложение будет использовать этот класс обратного вызова для чтения всех видеокадров из файла мультимедиа:


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Модуль чтения исходного кода](source-reader.md)
</dt> </dl>

 

 



