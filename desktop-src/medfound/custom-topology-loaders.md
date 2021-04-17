---
description: Пользовательские загрузчики топологии
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Пользовательские загрузчики топологии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a8f9e24b207d43620e7b2d09080d244b0a9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710836"
---
# <a name="custom-topology-loaders"></a><span data-ttu-id="49e1c-103">Пользовательские загрузчики топологии</span><span class="sxs-lookup"><span data-stu-id="49e1c-103">Custom Topology Loaders</span></span>

<span data-ttu-id="49e1c-104">Когда приложение помещает в очередь частичную топологию в сеансе мультимедиа, сеанс мультимедиа использует для разрешения топологии загрузчик топологии.</span><span class="sxs-lookup"><span data-stu-id="49e1c-104">When an application queues a partial topology on the Media Session, the Media Session uses a topology loader to resolve the topology.</span></span> <span data-ttu-id="49e1c-105">По умолчанию сеанс мультимедиа использует стандартную реализацию Media Foundation загрузчика топологии, но также можно предоставить пользовательскую реализацию.</span><span class="sxs-lookup"><span data-stu-id="49e1c-105">By default, the Media Session uses the standard Media Foundation implementation of the topology loader, but you can also provide a custom implementation.</span></span> <span data-ttu-id="49e1c-106">Это обеспечивает более полный контроль над конечной топологией.</span><span class="sxs-lookup"><span data-stu-id="49e1c-106">This gives you more control over the final topology.</span></span> <span data-ttu-id="49e1c-107">Пользовательский загрузчик топологии должен реализовывать интерфейс [**имфтополоадер**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="49e1c-107">A custom topology loader must implement the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="49e1c-108">Чтобы задать пользовательский загрузчик топологии для сеанса мультимедиа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="49e1c-108">To set a custom topology loader on the Media Session, do the following:</span></span>

1.  <span data-ttu-id="49e1c-109">Создайте хранилище пустых атрибутов, вызвав [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="49e1c-109">Create an empty attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="49e1c-110">Установите атрибут [**\_ \_ тополоадер сеанса MF**](mf-session-topoloader-attribute.md) в хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="49e1c-110">Set the [**MF\_SESSION\_TOPOLOADER**](mf-session-topoloader-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="49e1c-111">Значением атрибута является идентификатор CLSID пользовательского загрузчика.</span><span class="sxs-lookup"><span data-stu-id="49e1c-111">The value of the attribute is the CLSID of your custom loader.</span></span>
3.  <span data-ttu-id="49e1c-112">Вызовите [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) , чтобы создать сеанс мультимедиа для незащищенного содержимого, или [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , чтобы создать сеанс мультимедиа внутри защищенного пути к носителю (PMP).</span><span class="sxs-lookup"><span data-stu-id="49e1c-112">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session for unprotected content, or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session inside the protected media path (PMP).</span></span>

> [!Note]  
> <span data-ttu-id="49e1c-113">Чтобы использовать пользовательский загрузчик топологии внутри PMP, загрузчик топологии должен быть доверенным компонентом.</span><span class="sxs-lookup"><span data-stu-id="49e1c-113">To use a custom topology loader inside the PMP, the topology loader must be a trusted component.</span></span> <span data-ttu-id="49e1c-114">Дополнительные сведения см. в разделе [путь к защищенному носителю](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="49e1c-114">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

 

<span data-ttu-id="49e1c-115">В следующем коде показано, как задать пользовательский загрузчик топологии для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49e1c-115">The following code shows how to set a custom topology loader on the Media Session.</span></span>


```C++
HRESULT CreateSession_CustomTopoLoader(REFCLSID clsid, IMFMediaSession **ppSession)
{
    *ppSession = NULL;

    IMFMediaSession *pSession = NULL;
    IMFAttributes *pConfig = NULL;

    // Create an attribute store to configure the media session.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Set the CLSID of the custom topology loader.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(MF_SESSION_TOPOLOADER, clsid);
    }

    // Create the media session.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaSession(pConfig, &pSession);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSession = pSession;
        (*ppSession)->AddRef();
    }

    SafeRelease(&pSession);
    SafeRelease(&pConfig);

    return hr;
}
```



<span data-ttu-id="49e1c-116">Не обязательно реализовывать весь алгоритм загрузки топологии в загрузчике топологии.</span><span class="sxs-lookup"><span data-stu-id="49e1c-116">It is not necessary to implement the entire topology-loading algorithm in your topology loader.</span></span> <span data-ttu-id="49e1c-117">В качестве альтернативы можно заключить Стандартный загрузчик топологии Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="49e1c-117">As an alternative, you can wrap the standard Media Foundation topology loader.</span></span> <span data-ttu-id="49e1c-118">В реализации метода [**имфтополоадер:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) измените топологию по мере необходимости и передайте измененную топологию в стандартный загрузчик топологии.</span><span class="sxs-lookup"><span data-stu-id="49e1c-118">In your implementation of the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, modify the topology as needed and pass the modified topology to the standard topology loader.</span></span> <span data-ttu-id="49e1c-119">Затем Стандартный загрузчик топологии завершает топологию.</span><span class="sxs-lookup"><span data-stu-id="49e1c-119">Then the standard topology loader completes the topology.</span></span> <span data-ttu-id="49e1c-120">Можно также изменить завершенную топологию перед передачей ее обратно в сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="49e1c-120">You can also modify the completed topology before passing it back to the Media Session.</span></span>

<span data-ttu-id="49e1c-121">В следующем коде показана общая структура этого подхода.</span><span class="sxs-lookup"><span data-stu-id="49e1c-121">The following code shows the general outline of this approach.</span></span> <span data-ttu-id="49e1c-122">В нем не отображаются сведения о методе [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , так как они зависят от конкретных требований приложения.</span><span class="sxs-lookup"><span data-stu-id="49e1c-122">It does not show any details of the [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, because these will depend on the particular requirements of your application.</span></span>


```C++
class CTopoLoader : public IMFTopoLoader
{
public:

    static HRESULT CreateInstance(REFIID iid, void **ppv)
    {
        HRESULT hr = S_OK;

        CTopoLoader *pTopoLoader = new (std::nothrow) CTopoLoader(&hr);
        
        if (pTopoLoader == NULL)
        {
            return E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
            hr = pTopoLoader->QueryInterface(iid, ppv);
        }

        SafeRelease(&pTopoLoader);
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CTopoLoader, IMFTopoLoader),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMTopoLoader methods.
    STDMETHODIMP Load(
        IMFTopology *pInput, 
        IMFTopology **ppOutput, 
        IMFTopology *pCurrent
        )
    {
        HRESULT hr = S_OK;

        // TODO: Add custom topology-building code here.
        //       Modify pInput as needed.

        if (SUCCEEDED(hr))
        {
            hr = m_pTopoLoader->Load(pInput, ppOutput, pCurrent);
        }

        // TODO: Add custom topology-building code here.
        //       Modify ppOutput as needed.

        return hr;
    }

private:
    CTopoLoader(HRESULT *phr) : m_cRef(1), m_pTopoLoader(NULL)
    {
        *phr = MFCreateTopoLoader(&m_pTopoLoader);
    }

    virtual ~CTopoLoader()
    {
        SafeRelease(&m_pTopoLoader);
    }

private:
    long            m_cRef;          // Reference count.
    IMFTopoLoader   *m_pTopoLoader;  // Standard topoloader.
};
```



## <a name="related-topics"></a><span data-ttu-id="49e1c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="49e1c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49e1c-124">**мфкреатетополоадер**</span><span class="sxs-lookup"><span data-stu-id="49e1c-124">**MFCreateTopoLoader**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[<span data-ttu-id="49e1c-125">Создание расширенной топологии</span><span class="sxs-lookup"><span data-stu-id="49e1c-125">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> </dl>

 

 



