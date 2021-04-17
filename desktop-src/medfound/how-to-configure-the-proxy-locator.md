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
# <a name="how-to-configure-the-proxy-locator"></a>Настройка локатора прокси-сервера

Приложение может изменить конфигурацию локатора прокси-сервера по умолчанию, задав для свойства [мфнетсаурце \_ проксилокаторфактори](mfnetsource-proxylocatorfactory-property.md) объект фабрики прокси-сервера, реализуемый приложением. Когда приложение вызывает методы сопоставителя источника для создания сетевого источника, Media Foundation вызывает фабрику локатора прокси-сервера. Этот объект создает прокси-локатор с настраиваемой конфигурацией.

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a>Изменение параметра конфигурации по умолчанию для локатора прокси-сервера

1.  Реализуйте интерфейс [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .
2.  В методе [**имфнетпроксилокаторфактори:: креатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) выполните следующие действия.
    1.  Создайте хранилище свойств.
    2.  Задайте параметры конфигурации для локатора прокси-сервера. Дополнительные сведения об этих параметрах см. в разделе [Параметры конфигурации локатора прокси-сервера](proxy-locator-configuration-settings.md).
    3.  Вызовите функцию [**мфкреатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . Передайте хранилище свойств и протокол. Протокол указывается в параметре *псзпротокол* объекта [**креатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).
3.  Создайте экземпляр класса фабрики локатора прокси-сервера и получите указатель на его интерфейс [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .
4.  Создайте еще одно хранилище свойств и установите значение свойства [**мфнетсаурце \_ проксилокаторфактори**](mfnetsource-proxylocatorfactory-property.md) , равное указателю [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) из шага 3.
5.  При создании сетевого источника передайте хранилище свойств в параметре *ппропс* методов сопоставителя источника, таких как [**Имфсаурцересолвер:: бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

## <a name="example"></a>Пример

В следующем примере кода реализуется интерфейс [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) . Метод [**имфнетпроксилокаторфактори:: креатепроксилокатор**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) создает экземпляр локатора прокси-сервера по умолчанию и настраивает его для работы в режиме автоматического обнаружения.


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



В следующем примере показано, как передать указатель [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) в сетевой источник.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Поддержка прокси-сервера для сетевых источников](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



