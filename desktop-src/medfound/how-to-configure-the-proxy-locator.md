---
description: Настройка локатора прокси-сервера
ms.assetid: ddc28add-ebf5-4a68-bdf4-dc5f33ab74da
title: Настройка локатора прокси-сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6b383dda9ac78b2c62aa8481a09cc5c0d7b3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711351"
---
# <a name="how-to-configure-the-proxy-locator"></a><span data-ttu-id="6713d-103">Настройка локатора прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="6713d-103">How to Configure the Proxy Locator</span></span>

<span data-ttu-id="6713d-104">Приложение может изменить конфигурацию локатора прокси-сервера по умолчанию, задав для свойства [мфнетсаурце \_ проксилокаторфактори](mfnetsource-proxylocatorfactory-property.md) объект фабрики прокси-сервера, реализуемый приложением.</span><span class="sxs-lookup"><span data-stu-id="6713d-104">The application can change the default configuration of the proxy locator by setting the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property to the proxy locator factory object that is implemented by the application.</span></span> <span data-ttu-id="6713d-105">Когда приложение вызывает методы сопоставителя источника для создания сетевого источника, Media Foundation вызывает фабрику локатора прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="6713d-105">When the application calls source resolver methods to create the network source, Media Foundation calls the proxy locator factory.</span></span> <span data-ttu-id="6713d-106">Этот объект создает прокси-локатор с настраиваемой конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="6713d-106">This object creates the proxy locator with custom configuration.</span></span>

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a><span data-ttu-id="6713d-107">Изменение параметра конфигурации по умолчанию для локатора прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="6713d-107">To change the default configuration setting of the proxy locator</span></span>

1.  <span data-ttu-id="6713d-108">Реализуйте интерфейс [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="6713d-108">Implement the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
2.  <span data-ttu-id="6713d-109">В методе [**имфнетпроксилокаторфактори:: креатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6713d-109">In the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method, do the following:</span></span>
    1.  <span data-ttu-id="6713d-110">Создайте хранилище свойств.</span><span class="sxs-lookup"><span data-stu-id="6713d-110">Create a property store.</span></span>
    2.  <span data-ttu-id="6713d-111">Задайте параметры конфигурации для локатора прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="6713d-111">Set the configuration settings for the proxy locator.</span></span> <span data-ttu-id="6713d-112">Дополнительные сведения об этих параметрах см. в разделе [Параметры конфигурации локатора прокси-сервера](proxy-locator-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="6713d-112">For information about these settings, see [Proxy Locator Configuration Settings](proxy-locator-configuration-settings.md).</span></span>
    3.  <span data-ttu-id="6713d-113">Вызовите функцию [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="6713d-113">Call the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="6713d-114">Передайте хранилище свойств и протокол.</span><span class="sxs-lookup"><span data-stu-id="6713d-114">Pass in the property store and the protocol.</span></span> <span data-ttu-id="6713d-115">Протокол указывается в параметре *псзпротокол* объекта [**креатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).</span><span class="sxs-lookup"><span data-stu-id="6713d-115">The protocol is specified in the *pszProtocol* parameter of [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).</span></span>
3.  <span data-ttu-id="6713d-116">Создайте экземпляр класса фабрики локатора прокси-сервера и получите указатель на его интерфейс [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="6713d-116">Create an instance of your proxy locator factory class and get a pointer to its [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
4.  <span data-ttu-id="6713d-117">Создайте еще одно хранилище свойств и установите значение свойства [**мфнетсаурце \_ проксилокаторфактори**](mfnetsource-proxylocatorfactory-property.md) , равное указателю [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) из шага 3.</span><span class="sxs-lookup"><span data-stu-id="6713d-117">Create another property store and set the value of the [**MFNETSOURCE\_PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) property equal to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer from step 3.</span></span>
5.  <span data-ttu-id="6713d-118">При создании сетевого источника передайте хранилище свойств в параметре *ппропс* методов сопоставителя источника, таких как [**Имфсаурцересолвер:: бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="6713d-118">When you create the network source, pass the property store in the *pProps* parameter of the source resolver methods such as [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

## <a name="example"></a><span data-ttu-id="6713d-119">Пример</span><span class="sxs-lookup"><span data-stu-id="6713d-119">Example</span></span>

<span data-ttu-id="6713d-120">В следующем примере кода реализуется интерфейс [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="6713d-120">The following code example implements the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span> <span data-ttu-id="6713d-121">Метод [**имфнетпроксилокаторфактори:: креатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) создает экземпляр локатора прокси-сервера по умолчанию и настраивает его для работы в режиме автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="6713d-121">The [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method creates an instance of the default proxy locator, and configures it to operate in auto-detect mode.</span></span>


```C++
class CProxyLocatorFactory : public IMFNetProxyLocatorFactory 
{
    LONG m_cRef;

public:

    CProxyLocatorFactory() : m_cRef(1)
    {
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CProxyLocatorFactory, IMFNetProxyLocatorFactory),
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

    STDMETHODIMP CreateProxyLocator(
        LPCWSTR pszProtocol, 
        IMFNetProxyLocator **ppProxyLocator
        )
    {
        *ppProxyLocator = NULL;

        //Create the property store object
        IPropertyStore *pProp = NULL;

        HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pProp));

        if(SUCCEEDED(hr))
        {
            // Property key for proxy settings.
            PROPERTYKEY key;
            key.fmtid = MFNETSOURCE_PROXYSETTINGS;        
            key.pid = 0;

            // Proxy settings
            PROPVARIANT var;
            var.vt = VT_I4;
            var.lVal = MFNET_PROXYSETTING_AUTO;

            hr = pProp->SetValue(key, var);
        }

        //Create the default proxy locator.

        if(SUCCEEDED(hr))
        {
            hr = MFCreateProxyLocator(pszProtocol, pProp, ppProxyLocator);
        }

        SafeRelease(&pProp);
        return hr;
    }
};
```



<span data-ttu-id="6713d-122">В следующем примере показано, как передать указатель [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) в сетевой источник.</span><span class="sxs-lookup"><span data-stu-id="6713d-122">The next example shows how to pass the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer to the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set a proxy locator on the network source.

HRESULT CreateMediaSourceWithProxyLocator(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    IMFNetProxyLocatorFactory *pFactory = new (std::nothrow) CProxyLocatorFactory();

    if (pFactory == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_PROXYLOCATORFACTORY;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        var.punkVal = pFactory;

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6713d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6713d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6713d-124">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="6713d-124">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



