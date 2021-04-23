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
# <a name="media-foundation-and-com"></a><span data-ttu-id="ab5a6-103">Media Foundation и COM</span><span class="sxs-lookup"><span data-stu-id="ab5a6-103">Media Foundation and COM</span></span>

<span data-ttu-id="ab5a6-104">Microsoft Media Foundation использует смесь конструкций COM, но не является полностью API-интерфейсом на основе COM.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-104">Microsoft Media Foundation uses a mix of COM constructs, but is not a fully COM-based API.</span></span> <span data-ttu-id="ab5a6-105">В этом разделе описывается взаимодействие между COM и Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-105">This topic describes the interaction between COM and Media Foundation.</span></span> <span data-ttu-id="ab5a6-106">Он также определяет некоторые рекомендации по разработке компонентов подключаемых модулей Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-106">It also defines some best practices for developing Media Foundation plug-in components.</span></span> <span data-ttu-id="ab5a6-107">Следующие рекомендации помогут избежать некоторых распространенных, но незначительных ошибок программирования.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-107">Following these practices can help you to avoid some common but subtle programming errors.</span></span>

-   [<span data-ttu-id="ab5a6-108">Рекомендации для приложений</span><span class="sxs-lookup"><span data-stu-id="ab5a6-108">Best Practices for Applications</span></span>](#best-practices-for-applications)
-   [<span data-ttu-id="ab5a6-109">Рекомендации по компонентам Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab5a6-109">Best Practices for Media Foundation Components</span></span>](#best-practices-for-media-foundation-components)
-   [<span data-ttu-id="ab5a6-110">Сводка</span><span class="sxs-lookup"><span data-stu-id="ab5a6-110">Summary</span></span>](#summary)
-   [<span data-ttu-id="ab5a6-111">См. также</span><span class="sxs-lookup"><span data-stu-id="ab5a6-111">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-applications"></a><span data-ttu-id="ab5a6-112">Рекомендации для приложений</span><span class="sxs-lookup"><span data-stu-id="ab5a6-112">Best Practices for Applications</span></span>

<span data-ttu-id="ab5a6-113">В Media Foundation асинхронная обработка и обратные вызовы обрабатываются [рабочими очередями](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-113">In Media Foundation, asynchronous processing and callbacks are handled by [work queues](work-queues.md).</span></span> <span data-ttu-id="ab5a6-114">Рабочие очереди всегда имеют потоки многопотокового подразделения (MTA), поэтому приложение будет иметь более простую реализацию, если оно работает в потоке MTA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-114">Work queues always have multithreaded apartment (MTA) threads, so an application will have a simpler implementation if it runs on an MTA thread as well.</span></span> <span data-ttu-id="ab5a6-115">Поэтому рекомендуется вызывать [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) с флагом для **\_ многопотоковой инициализации** .</span><span class="sxs-lookup"><span data-stu-id="ab5a6-115">Therefore, it is recommended to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="ab5a6-116">Media Foundation не маршалирует объекты однопотокового подразделения (STA) в потоки рабочей очереди.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-116">Media Foundation does not marshal single-threaded apartment (STA) objects to work queue threads.</span></span> <span data-ttu-id="ab5a6-117">Также не гарантирует, что инварианты STA не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-117">Nor does it ensure that STA invariants are maintained.</span></span> <span data-ttu-id="ab5a6-118">Таким образом, приложение STA должно быть осторожным, чтобы не передавать объекты STA или прокси-серверы в Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-118">Therefore, an STA application must be careful to not pass STA objects or proxies to Media Foundation APIs.</span></span> <span data-ttu-id="ab5a6-119">В Media Foundation не поддерживаются только объекты с STA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-119">Objects that are STA-only are not supported in Media Foundation.</span></span>

<span data-ttu-id="ab5a6-120">Если у вас есть прокси STA для MTA-или свободных потоков, объект можно маршалировать на прокси-сервер MTA с помощью обратного вызова очереди работ.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-120">If you have an STA proxy to an MTA or free-threaded object, the object can be marshaled to an MTA proxy by using a work-queue callback.</span></span> <span data-ttu-id="ab5a6-121">Функция [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) может возвращать либо необработанный указатель, либо прокси STA в зависимости от объектной модели, определенной в реестре для этого идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-121">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function can return either a raw pointer or an STA proxy, depending on the object model defined in the registry for that CLSID.</span></span> <span data-ttu-id="ab5a6-122">Если возвращается прокси-сервер STA, не следует передавать указатель на Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-122">If an STA proxy is returned, you must not pass the pointer to a Media Foundation API.</span></span>

<span data-ttu-id="ab5a6-123">Например, предположим, что вы хотите передать указатель **ипропертисторе** в метод [**Имфсаурцересолвер:: бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="ab5a6-123">For example, suppose that you want to pass an **IPropertyStore** pointer to the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span> <span data-ttu-id="ab5a6-124">Для создания указателя **ипропертисторе** можно вызвать **пскреатемеморипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="ab5a6-124">You might call **PSCreateMemoryPropertyStore** to create the **IPropertyStore** pointer.</span></span> <span data-ttu-id="ab5a6-125">При вызове из STA необходимо маршалировать указатель перед передачей его в **бегинкреатеобжектфромурл**.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-125">If you are calling from an STA, you must marshal the pointer before passing it to **BeginCreateObjectFromURL**.</span></span>

<span data-ttu-id="ab5a6-126">В следующем коде показано, как маршалировать прокси STA в Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-126">The following code shows how to marshal an STA proxy to a Media Foundation API.</span></span>


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



<span data-ttu-id="ab5a6-127">Дополнительные сведения о таблице глобальных интерфейсов см. в разделе [**иглобалинтерфацетабле**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-127">For more information about the global interface table, see [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="ab5a6-128">При использовании Media Foundation в процессе объекты, возвращаемые из Media Foundation методов и функций, являются прямыми указателями на объект.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-128">If you are using Media Foundation in-process, objects returned from Media Foundation methods and functions are direct pointers to the object.</span></span> <span data-ttu-id="ab5a6-129">Для межпроцессных Media Foundation эти объекты могут быть посредниками MTA и при необходимости должны быть упакованы в поток STA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-129">For cross-process Media Foundation, these objects may be MTA proxies, and should be marshaled into an STA thread if needed there.</span></span> <span data-ttu-id="ab5a6-130">Аналогичным образом объекты, полученные внутри обратного вызова (например, топология из события [месессионтопологистатус](mesessiontopologystatus.md) ), являются прямыми указателями, когда Media Foundation используется внутри процесса, но являются прокси агента передачи сообщений, если Media Foundation используется для кросс-обработки.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-130">Similarly, objects obtained inside a callback — for example, a topology from the [MESessionTopologyStatus](mesessiontopologystatus.md) event — are direct pointers when Media Foundation is used in-process, but are MTA proxies when Media Foundation is used cross-process.</span></span>

> [!Note]  
> <span data-ttu-id="ab5a6-131">Наиболее распространенный сценарий использования Media Foundation кросс-Process — с [защищенным путем к носителю](protected-media-path.md) (PMP).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-131">The most common scenario for using Media Foundation cross-process is with the [Protected Media Path](protected-media-path.md) (PMP).</span></span> <span data-ttu-id="ab5a6-132">Однако эти замечания относятся к ситуации, когда Media Foundation API используются через RPC.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-132">However, these remarks apply to any situation when Media Foundation APIs are used through RPC.</span></span>

 

<span data-ttu-id="ab5a6-133">Все реализации [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) должны быть совместимы с MTA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-133">All implementations of [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) should be MTA-compatible.</span></span> <span data-ttu-id="ab5a6-134">Эти объекты не обязательно должны быть COM-объектами.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-134">These objects do not need to be COM objects at all.</span></span> <span data-ttu-id="ab5a6-135">Но если они есть, они не могут выполняться в STA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-135">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="ab5a6-136">Функция [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) будет вызываться в потоке ворккуеуе агента передачи сообщений, а предоставленный объект [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) будет либо прямым указателем объекта, либо прокси агента передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-136">The [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) function will be invoked on an MTA workqueue thread, and the provided [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) object will be either a direct object pointer or an MTA proxy.</span></span>

## <a name="best-practices-for-media-foundation-components"></a><span data-ttu-id="ab5a6-137">Рекомендации по компонентам Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab5a6-137">Best Practices for Media Foundation Components</span></span>

<span data-ttu-id="ab5a6-138">Существует две категории объектов Media Foundation, которые должны быть связаны с COM.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-138">There are two categories of Media Foundation objects that need to be concerned about COM.</span></span> <span data-ttu-id="ab5a6-139">Некоторые компоненты, такие как преобразования или обработчики потока байтов, являются полными COM-объектами, созданными CLSID.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-139">Some components, such as transforms or byte stream handlers, are full COM objects created by CLSID.</span></span> <span data-ttu-id="ab5a6-140">Эти объекты должны соответствовать правилам для апартаментов COM, как для внутрипроцессного, так и для межпроцессного Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-140">These objects must follow the rules for COM apartments, for both in-process and cross-process Media Foundation.</span></span> <span data-ttu-id="ab5a6-141">Другие компоненты Media Foundation не являются полными COM-объектами, но для воспроизведения между процессами требуются прокси-серверы COM.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-141">Other Media Foundation components are not full COM objects, but do need COM proxies for cross-process playback.</span></span> <span data-ttu-id="ab5a6-142">К объектам в этой категории относятся источники мультимедиа и объект активации.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-142">Objects in this category include media sources and activation object.</span></span> <span data-ttu-id="ab5a6-143">Эти объекты могут игнорировать проблемы апартамента, если они будут использоваться только для внутрипроцессного Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-143">These objects can ignore apartment issues if they will be used only for in-process Media Foundation.</span></span>

<span data-ttu-id="ab5a6-144">Хотя не все Media Foundation объекты являются COM-объектами, все интерфейсы Media Foundation являются производными от [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-144">Although not all Media Foundation objects are COM objects, all Media Foundation interfaces derive from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="ab5a6-145">Таким образом, все объекты Media Foundation должны реализовывать **IUnknown** в соответствии со спецификациями com, включая правила подсчета ссылок и [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-145">Therefore, all Media Foundation objects must implement **IUnknown** according to COM specifications, including the rules for reference counting and [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="ab5a6-146">Все объекты, подсчитанные ссылки, должны также гарантировать, что [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) не позволит выгружать модуль, пока объекты продолжают сохраняться.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-146">All reference counted objects should also ensure that [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) will not allow the module to be unloaded while the objects still persist.</span></span>

<span data-ttu-id="ab5a6-147">Компоненты Media Foundation не могут быть объектами STA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-147">Media Foundation components cannot be STA objects.</span></span> <span data-ttu-id="ab5a6-148">Многие объекты Media Foundation не обязательно должны быть COM-объектами.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-148">Many Media Foundation objects do not need to be COM objects at all.</span></span> <span data-ttu-id="ab5a6-149">Но если они есть, они не могут выполняться в STA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-149">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="ab5a6-150">Все компоненты Media Foundation должны быть потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-150">All Media Foundation components must be thread-safe.</span></span> <span data-ttu-id="ab5a6-151">Некоторые Media Foundation объекты должны также быть независимыми от потоков или подразделений.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-151">Some Media Foundation objects must be free-threaded or apartment-neutral as well.</span></span> <span data-ttu-id="ab5a6-152">В следующей таблице указаны требования к реализациям пользовательских интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-152">The following table specifies the requirements for custom interface implementations:</span></span>



| <span data-ttu-id="ab5a6-153">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ab5a6-153">Interface</span></span>                                                          | <span data-ttu-id="ab5a6-154">Категория</span><span class="sxs-lookup"><span data-stu-id="ab5a6-154">Category</span></span>            | <span data-ttu-id="ab5a6-155">Требуемое подразделение</span><span class="sxs-lookup"><span data-stu-id="ab5a6-155">Required apartment</span></span>       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [<span data-ttu-id="ab5a6-156">**имфактивате**</span><span class="sxs-lookup"><span data-stu-id="ab5a6-156">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | <span data-ttu-id="ab5a6-157">Межпроцессный прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="ab5a6-157">Cross-process proxy</span></span> | <span data-ttu-id="ab5a6-158">Бесплатный поток или нейтральный</span><span class="sxs-lookup"><span data-stu-id="ab5a6-158">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ab5a6-159">**имфбитестреамхандлер**</span><span class="sxs-lookup"><span data-stu-id="ab5a6-159">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | <span data-ttu-id="ab5a6-160">COM-объект</span><span class="sxs-lookup"><span data-stu-id="ab5a6-160">COM object</span></span>          | <span data-ttu-id="ab5a6-161">MTA</span><span class="sxs-lookup"><span data-stu-id="ab5a6-161">MTA</span></span>                      |
| [<span data-ttu-id="ab5a6-162">**имфконтентпротектионманажер**</span><span class="sxs-lookup"><span data-stu-id="ab5a6-162">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | <span data-ttu-id="ab5a6-163">Межпроцессный прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="ab5a6-163">Cross-process proxy</span></span> | <span data-ttu-id="ab5a6-164">Бесплатный поток или нейтральный</span><span class="sxs-lookup"><span data-stu-id="ab5a6-164">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ab5a6-165">**имфкуалитиманажер**</span><span class="sxs-lookup"><span data-stu-id="ab5a6-165">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | <span data-ttu-id="ab5a6-166">COM-объект</span><span class="sxs-lookup"><span data-stu-id="ab5a6-166">COM object</span></span>          | <span data-ttu-id="ab5a6-167">Бесплатный поток или нейтральный</span><span class="sxs-lookup"><span data-stu-id="ab5a6-167">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ab5a6-168">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="ab5a6-168">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | <span data-ttu-id="ab5a6-169">Межпроцессный прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="ab5a6-169">Cross-process proxy</span></span> | <span data-ttu-id="ab5a6-170">Бесплатный поток или нейтральный</span><span class="sxs-lookup"><span data-stu-id="ab5a6-170">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ab5a6-171">**имфсчемехандлер**</span><span class="sxs-lookup"><span data-stu-id="ab5a6-171">**IMFSchemeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | <span data-ttu-id="ab5a6-172">COM-объект</span><span class="sxs-lookup"><span data-stu-id="ab5a6-172">COM object</span></span>          | <span data-ttu-id="ab5a6-173">MTA</span><span class="sxs-lookup"><span data-stu-id="ab5a6-173">MTA</span></span>                      |
| [<span data-ttu-id="ab5a6-174">**имфтополоадер**</span><span class="sxs-lookup"><span data-stu-id="ab5a6-174">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | <span data-ttu-id="ab5a6-175">COM-объект</span><span class="sxs-lookup"><span data-stu-id="ab5a6-175">COM object</span></span>          | <span data-ttu-id="ab5a6-176">Бесплатный поток или нейтральный</span><span class="sxs-lookup"><span data-stu-id="ab5a6-176">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="ab5a6-177">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="ab5a6-177">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | <span data-ttu-id="ab5a6-178">COM-объект</span><span class="sxs-lookup"><span data-stu-id="ab5a6-178">COM object</span></span>          | <span data-ttu-id="ab5a6-179">MTA</span><span class="sxs-lookup"><span data-stu-id="ab5a6-179">MTA</span></span>                      |



 

<span data-ttu-id="ab5a6-180">В зависимости от реализации могут быть дополнительные требования.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-180">There may be additional requirements depending upon the implementation.</span></span> <span data-ttu-id="ab5a6-181">Например, если приемник мультимедиа реализует другой интерфейс, позволяющий приложению выполнять прямые вызовы функций к приемнику, приемнику необходимо быть свободным или нейтральным, чтобы он мог обрабатывать прямые вызовы между процессами.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-181">For example, if a media sink implements another interface that enables the application to make direct function calls to the sink, the sink would need to be free-threaded or neutral, so that it could handle direct cross-process calls.</span></span> <span data-ttu-id="ab5a6-182">Все объекты могут быть свободными потоками; в этой таблице указаны минимальные требования.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-182">Any object may be free-threaded; this table specifies the minimum requirements.</span></span>

<span data-ttu-id="ab5a6-183">Для реализации свободных и нейтральных объектов рекомендуется выполнить статистическую обработку модуля упаковки с произвольным потоком.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-183">The recommended way to implement free-threaded or neutral objects is by aggregating the free-threaded marshaler.</span></span> <span data-ttu-id="ab5a6-184">Дополнительные сведения см. в документации MSDN по [**кокреатефрисреадедмаршалер**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-184">For more details, see the MSDN documentation on [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span></span> <span data-ttu-id="ab5a6-185">В соответствии с требованием не передавать объекты STA или учетные записи-посредники в Media Foundation API, объекты свободных потоков не должны беспокоиться о маршалировании указателей ввода STA в свободных компонентах.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-185">In accordance with the requirement not to pass STA objects or proxies to Media Foundation APIs, free-threaded objects do not need to worry about marshaling STA input pointers in free-threaded components.</span></span>

<span data-ttu-id="ab5a6-186">Компоненты, использующие длительную рабочую очередь (**мфасинк функция " \_ очередь обратного вызова \_ \_ \_**"), должны уделять больше времени.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-186">Components that use the long-function work queue (**MFASYNC\_CALLBACK\_QUEUE\_LONG\_FUNCTION**) must exercise more care.</span></span> <span data-ttu-id="ab5a6-187">Потоки в функции Long ворккуеуе создают собственный STA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-187">Threads in the long function workqueue create their own STA.</span></span> <span data-ttu-id="ab5a6-188">Компоненты, которые используют функцию Long ворккуеуе для обратных вызовов, должны избегать создания COM-объектов в этих потоках и должны быть внимательны при необходимости маршалировать прокси в STA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-188">Components that use the long function workqueue for callbacks should avoid creating COM objects on these threads, and need to be careful to marshal proxies to the STA as necessary.</span></span>

## <a name="summary"></a><span data-ttu-id="ab5a6-189">Сводка</span><span class="sxs-lookup"><span data-stu-id="ab5a6-189">Summary</span></span>

<span data-ttu-id="ab5a6-190">Приложения будут более простыми, если бы они взаимодействовали с Media Foundation из потока MTA, но с некоторой осторожностью можно использовать Media Foundation из потока STA.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-190">Applications will have an easier time if they interact with Media Foundation from an MTA thread, but it is possible with some care to use Media Foundation from an STA thread.</span></span> <span data-ttu-id="ab5a6-191">Media Foundation не обрабатывает компоненты STA, и приложения должны быть осторожными, чтобы не передавать объекты STA в Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-191">Media Foundation does not handle STA components, and applications should be careful not to pass STA objects to Media Foundation APIs.</span></span> <span data-ttu-id="ab5a6-192">Некоторые объекты имеют дополнительные требования, особенно объекты, которые выполняются в межпроцессной ситуации.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-192">Some objects have additional requirements, especially objects that run in a cross-process situation.</span></span> <span data-ttu-id="ab5a6-193">Соблюдение этих рекомендаций поможет избежать ошибок COM, взаимоблокировок и непредвиденных задержек при обработке мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-193">Following these guidelines will help avoid COM errors, deadlocks, and unexpected delays in media processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab5a6-194">См. также</span><span class="sxs-lookup"><span data-stu-id="ab5a6-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab5a6-195">Media Foundation API платформы</span><span class="sxs-lookup"><span data-stu-id="ab5a6-195">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> <dt>

[<span data-ttu-id="ab5a6-196">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab5a6-196">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 
