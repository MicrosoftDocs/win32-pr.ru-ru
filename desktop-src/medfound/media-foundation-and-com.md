---
description: Microsoft Media Foundation использует смесь конструкций COM, но не является полностью API-интерфейсом на основе COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation и COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720044"
---
# <a name="media-foundation-and-com"></a>Media Foundation и COM

Microsoft Media Foundation использует смесь конструкций COM, но не является полностью API-интерфейсом на основе COM. В этом разделе описывается взаимодействие между COM и Media Foundation. Он также определяет некоторые рекомендации по разработке компонентов подключаемых модулей Media Foundation. Следующие рекомендации помогут избежать некоторых распространенных, но незначительных ошибок программирования.

-   [Рекомендации для приложений](#best-practices-for-applications)
-   [Рекомендации по компонентам Media Foundation](#best-practices-for-media-foundation-components)
-   [Сводка](#summary)
-   [См. также](#related-topics)

## <a name="best-practices-for-applications"></a>Рекомендации для приложений

В Media Foundation асинхронная обработка и обратные вызовы обрабатываются [рабочими очередями](work-queues.md). Рабочие очереди всегда имеют потоки многопотокового подразделения (MTA), поэтому приложение будет иметь более простую реализацию, если оно работает в потоке MTA. Поэтому рекомендуется вызывать [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) с флагом для **\_ многопотоковой инициализации** .

Media Foundation не маршалирует объекты однопотокового подразделения (STA) в потоки рабочей очереди. Также не гарантирует, что инварианты STA не поддерживаются. Таким образом, приложение STA должно быть осторожным, чтобы не передавать объекты STA или прокси-серверы в Media Foundation API. В Media Foundation не поддерживаются только объекты с STA.

Если у вас есть прокси STA для MTA-или свободных потоков, объект можно маршалировать на прокси-сервер MTA с помощью обратного вызова очереди работ. Функция [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) может возвращать либо необработанный указатель, либо прокси STA в зависимости от объектной модели, определенной в реестре для этого идентификатора CLSID. Если возвращается прокси-сервер STA, не следует передавать указатель на Media Foundation API.

Например, предположим, что вы хотите передать указатель **ипропертисторе** в метод [**Имфсаурцересолвер:: бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) . Для создания указателя **ипропертисторе** можно вызвать **пскреатемеморипропертисторе** . При вызове из STA необходимо маршалировать указатель перед передачей его в **бегинкреатеобжектфромурл**.

В следующем коде показано, как маршалировать прокси STA в Media Foundation API.


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



Дополнительные сведения о таблице глобальных интерфейсов см. в разделе [**иглобалинтерфацетабле**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

При использовании Media Foundation в процессе объекты, возвращаемые из Media Foundation методов и функций, являются прямыми указателями на объект. Для межпроцессных Media Foundation эти объекты могут быть посредниками MTA и при необходимости должны быть упакованы в поток STA. Аналогичным образом объекты, полученные внутри обратного вызова (например, топология из события [месессионтопологистатус](mesessiontopologystatus.md) ), являются прямыми указателями, когда Media Foundation используется внутри процесса, но являются прокси агента передачи сообщений, если Media Foundation используется для кросс-обработки.

> [!Note]  
> Наиболее распространенный сценарий использования Media Foundation кросс-Process — с [защищенным путем к носителю](protected-media-path.md) (PMP). Однако эти замечания относятся к ситуации, когда Media Foundation API используются через RPC.

 

Все реализации [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) должны быть совместимы с MTA. Эти объекты не обязательно должны быть COM-объектами. Но если они есть, они не могут выполняться в STA. Функция [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) будет вызываться в потоке ворккуеуе агента передачи сообщений, а предоставленный объект [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) будет либо прямым указателем объекта, либо прокси агента передачи сообщений.

## <a name="best-practices-for-media-foundation-components"></a>Рекомендации по компонентам Media Foundation

Существует две категории объектов Media Foundation, которые должны быть связаны с COM. Некоторые компоненты, такие как преобразования или обработчики потока байтов, являются полными COM-объектами, созданными CLSID. Эти объекты должны соответствовать правилам для апартаментов COM, как для внутрипроцессного, так и для межпроцессного Media Foundation. Другие компоненты Media Foundation не являются полными COM-объектами, но для воспроизведения между процессами требуются прокси-серверы COM. К объектам в этой категории относятся источники мультимедиа и объект активации. Эти объекты могут игнорировать проблемы апартамента, если они будут использоваться только для внутрипроцессного Media Foundation.

Хотя не все Media Foundation объекты являются COM-объектами, все интерфейсы Media Foundation являются производными от [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Таким образом, все объекты Media Foundation должны реализовывать **IUnknown** в соответствии со спецификациями com, включая правила подсчета ссылок и [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Все объекты, подсчитанные ссылки, должны также гарантировать, что [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) не позволит выгружать модуль, пока объекты продолжают сохраняться.

Компоненты Media Foundation не могут быть объектами STA. Многие объекты Media Foundation не обязательно должны быть COM-объектами. Но если они есть, они не могут выполняться в STA. Все компоненты Media Foundation должны быть потокобезопасными. Некоторые Media Foundation объекты должны также быть независимыми от потоков или подразделений. В следующей таблице указаны требования к реализациям пользовательских интерфейсов.



| Интерфейс                                                          | Категория            | Требуемое подразделение       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Межпроцессный прокси-сервер | Бесплатный поток или нейтральный |
| [**имфбитестреамхандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | COM-объект          | MTA                      |
| [**имфконтентпротектионманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Межпроцессный прокси-сервер | Бесплатный поток или нейтральный |
| [**имфкуалитиманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | COM-объект          | Бесплатный поток или нейтральный |
| [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Межпроцессный прокси-сервер | Бесплатный поток или нейтральный |
| [**имфсчемехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | COM-объект          | MTA                      |
| [**имфтополоадер**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | COM-объект          | Бесплатный поток или нейтральный |
| [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | COM-объект          | MTA                      |



 

В зависимости от реализации могут быть дополнительные требования. Например, если приемник мультимедиа реализует другой интерфейс, позволяющий приложению выполнять прямые вызовы функций к приемнику, приемнику необходимо быть свободным или нейтральным, чтобы он мог обрабатывать прямые вызовы между процессами. Все объекты могут быть свободными потоками; в этой таблице указаны минимальные требования.

Для реализации свободных и нейтральных объектов рекомендуется выполнить статистическую обработку модуля упаковки с произвольным потоком. Дополнительные сведения см. в документации MSDN по [**кокреатефрисреадедмаршалер**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). В соответствии с требованием не передавать объекты STA или учетные записи-посредники в Media Foundation API, объекты свободных потоков не должны беспокоиться о маршалировании указателей ввода STA в свободных компонентах.

Компоненты, использующие длительную рабочую очередь (**мфасинк функция " \_ очередь обратного вызова \_ \_ \_**"), должны уделять больше времени. Потоки в функции Long ворккуеуе создают собственный STA. Компоненты, которые используют функцию Long ворккуеуе для обратных вызовов, должны избегать создания COM-объектов в этих потоках и должны быть внимательны при необходимости маршалировать прокси в STA.

## <a name="summary"></a>Сводка

Приложения будут более простыми, если бы они взаимодействовали с Media Foundation из потока MTA, но с некоторой осторожностью можно использовать Media Foundation из потока STA. Media Foundation не обрабатывает компоненты STA, и приложения должны быть осторожными, чтобы не передавать объекты STA в Media Foundation API. Некоторые объекты имеют дополнительные требования, особенно объекты, которые выполняются в межпроцессной ситуации. Соблюдение этих рекомендаций поможет избежать ошибок COM, взаимоблокировок и непредвиденных задержек при обработке мультимедиа.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Media Foundation API платформы](media-foundation-platform-apis.md)
</dt> <dt>

[Архитектура Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 
