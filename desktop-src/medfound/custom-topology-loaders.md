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
# <a name="custom-topology-loaders"></a>Пользовательские загрузчики топологии

Когда приложение помещает в очередь частичную топологию в сеансе мультимедиа, сеанс мультимедиа использует для разрешения топологии загрузчик топологии. По умолчанию сеанс мультимедиа использует стандартную реализацию Media Foundation загрузчика топологии, но также можно предоставить пользовательскую реализацию. Это обеспечивает более полный контроль над конечной топологией. Пользовательский загрузчик топологии должен реализовывать интерфейс [**имфтополоадер**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .

Чтобы задать пользовательский загрузчик топологии для сеанса мультимедиа, выполните следующие действия.

1.  Создайте хранилище пустых атрибутов, вызвав [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Установите атрибут [**\_ \_ тополоадер сеанса MF**](mf-session-topoloader-attribute.md) в хранилище атрибутов. Значением атрибута является идентификатор CLSID пользовательского загрузчика.
3.  Вызовите [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) , чтобы создать сеанс мультимедиа для незащищенного содержимого, или [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , чтобы создать сеанс мультимедиа внутри защищенного пути к носителю (PMP).

> [!Note]  
> Чтобы использовать пользовательский загрузчик топологии внутри PMP, загрузчик топологии должен быть доверенным компонентом. Дополнительные сведения см. в разделе [путь к защищенному носителю](protected-media-path.md).

 

В следующем коде показано, как задать пользовательский загрузчик топологии для сеанса мультимедиа.


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



Не обязательно реализовывать весь алгоритм загрузки топологии в загрузчике топологии. В качестве альтернативы можно заключить Стандартный загрузчик топологии Media Foundation. В реализации метода [**имфтополоадер:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) измените топологию по мере необходимости и передайте измененную топологию в стандартный загрузчик топологии. Затем Стандартный загрузчик топологии завершает топологию. Можно также изменить завершенную топологию перед передачей ее обратно в сеанс мультимедиа.

В следующем коде показана общая структура этого подхода. В нем не отображаются сведения о методе [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , так как они зависят от конкретных требований приложения.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**мфкреатетополоадер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[Создание расширенной топологии](advanced-topology-building.md)
</dt> </dl>

 

 



