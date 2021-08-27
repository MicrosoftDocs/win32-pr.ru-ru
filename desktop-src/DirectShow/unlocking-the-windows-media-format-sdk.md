---
description: разблокировка пакета SDK для Windows Media Format
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: разблокировка пакета SDK для Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1f332711e9fd12c9b0ff1f789438d051487b81711f157ae1024a8e47973386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078664"
---
# <a name="unlocking-the-windows-media-format-sdk"></a>разблокировка пакета SDK для Windows Media Format

чтобы получить доступ к версии 7 или 7,1 пакета SDK Windows Media Format, приложение должно предоставить сертификат программного обеспечения, также называемый ключом, во время выполнения. Этот ключ содержится в статической библиотеке с именем вмстуб. lib, на которую ссылается приложение во время сборки. Отдельный ключ требуется только для создания или чтения файлов, защищенных с помощью DRM. файлы, не связанные с DRM, можно создать с помощью статической библиотеки, поставляемой с пакетом SDK для Windows Media Format. дополнительные сведения о получении ключа DRM см. в разделе Windows Media Format SDK. приложение DirectShow предоставляет свой сертификат модулю записи WM ASF при добавлении в граф фильтра. Приложение должно зарегистрироваться в качестве поставщика ключей с помощью интерфейсов **IServiceProvider** и **IObjectWithSite** com. С помощью этого метода приложение реализует класс поставщика ключей, производный от **IServiceProvider**. Этот класс реализует три стандартных метода COM:**AddRef**, **QueryInterface** и **Release**— вместе с одним дополнительным методом **QueryService**, который вызывается диспетчером графа фильтров. **QueryService** вызывает метод пакета SDK Windows Media Format [**вмкреатецертификате**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) и возвращает в диспетчер графа фильтра указатель на созданный сертификат. Если сертификат действителен, диспетчер графа фильтров разрешает продолжение процесса построения графа.

> [!Note]  
> Чтобы создать приложение, включите Вмсдкидл. h в прототип для [**вмкреатецертификате**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))и свяжите с библиотекой вмстуб. lib.

 

В следующем примере кода показаны основные шаги этого процесса.


```C++
// Declare and implement a key provider class derived from IServiceProvider.

class CKeyProvider : public IServiceProvider {
public:
    // IUnknown interface
    STDMETHODIMP QueryInterface(REFIID riid, void ** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    CKeyProvider();

    // IServiceProvider
    STDMETHODIMP QueryService(REFIID siid, REFIID riid, void **ppv);
    
private:
    ULONG m_cRef;
};

CKeyProvider::CKeyProvider() : m_cRef(0)
{
}

// IUnknown methods
ULONG CKeyProvider::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

ULONG CKeyProvider::Release()
{
    ASSERT(m_cRef > 0);

    ULONG lCount = InterlockedDecrement(&m_cRef);
    if (m_cRef == 0) 
    {
        delete this;
        return (ULONG)0;
    }
    return (ULONG)lCount;
}

// We only support IUnknown and IServiceProvider.
HRESULT CKeyProvider::QueryInterface(REFIID riid, void ** ppv)
{
    if (!ppv) return E_POINTER;

    if (riid == IID_IUnknown) 
    {
        *ppv = (void *) static_cast<IUnknown *>(this);
        AddRef();
        return S_OK;
    }
    if (riid == IID_IServiceProvider) 
    {
        *ppv = (void *) static_cast<IServiceProvider *>(this);
        AddRef();
        return S_OK;
    }

    return E_NOINTERFACE;
}

STDMETHODIMP CKeyProvider::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (!ppv) return E_POINTER;

    if (siid == __uuidof(IWMReader) && riid == IID_IUnknown) 
    {
        IUnknown *punkCert;
        HRESULT hr = WMCreateCertificate(&punkCert);
        if (SUCCEEDED(hr)) 
        {
            *ppv = (void *) punkCert;
        }
        return hr;
    }
    return E_NOINTERFACE;
}

////////////////////////////////////////////////////////////////////
//
// These examples illustrate the sequence of method calls
// in your application. Error checking is omitted for brevity.
//
///////////////////////////////////////////////////////////////////

// Create the filter graph manager, but don't add any filters.
IGraphBuilder *pGraph;
hr = CreateFilterGraph(&pGraph);

...

// Instantiate the key provider class, and AddRef it
// so that COM doesn't try to free our static object.

CKeyProvider prov;
prov.AddRef();  // Don't let COM try to free our static object.

// Give the graph an IObjectWithSite pointer for callbacks and QueryService.
IObjectWithSite* pObjectWithSite = NULL;

hr = pGraph->QueryInterface(IID_IObjectWithSite, (void**)&pObjectWithSite);
if (SUCCEEDED(hr))
{
    // Use the IObjectWithSite pointer to specify our key provider object.
    // The filter graph manager will use this pointer to call
    // QueryService to do the unlocking.
    // If the unlocking succeeds, then we can build our graph.

    pObjectWithSite->SetSite((IUnknown *) (IServiceProvider *) &prov);
    pObjectWithSite->Release();
}

// Now build the graph.
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
