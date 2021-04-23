---
description: Разблокировка пакета SDK Windows Media Format
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: Разблокировка пакета SDK Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9807794dc7e42c563f2f7d45dcb0b1b684aad1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684777"
---
# <a name="unlocking-the-windows-media-format-sdk"></a><span data-ttu-id="037b3-103">Разблокировка пакета SDK Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="037b3-103">Unlocking the Windows Media Format SDK</span></span>

<span data-ttu-id="037b3-104">Чтобы получить доступ к версии 7 или 7,1 пакета SDK Windows Media Format, приложение должно предоставить сертификат программного обеспечения, также называемый ключом, во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="037b3-104">To access version 7 or 7.1 of the Windows Media Format SDK, an application must provide a software certificate, also called a key, at run time.</span></span> <span data-ttu-id="037b3-105">Этот ключ содержится в статической библиотеке с именем вмстуб. lib, на которую ссылается приложение во время сборки.</span><span class="sxs-lookup"><span data-stu-id="037b3-105">This key is contained in a static library called wmstub.lib to which the application links at build time.</span></span> <span data-ttu-id="037b3-106">Отдельный ключ требуется только для создания или чтения файлов, защищенных с помощью DRM.</span><span class="sxs-lookup"><span data-stu-id="037b3-106">An individualized key is only required for creating or reading DRM-protected files.</span></span> <span data-ttu-id="037b3-107">Файлы, не связанные с DRM, можно создавать с помощью статической библиотеки, поставляемой с пакетом SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="037b3-107">Non-DRM files can be created using the static library provided with the Windows Media Format SDK.</span></span> <span data-ttu-id="037b3-108">Дополнительные сведения о получении ключа DRM см. в разделе Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="037b3-108">For details on obtaining the DRM key, see the Windows Media Format SDK.</span></span> <span data-ttu-id="037b3-109">Приложение DirectShow предоставляет свой сертификат модулю записи WM ASF при добавлении в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="037b3-109">A DirectShow application provides its certificate to the WM ASF Writer when it is added to the filter graph.</span></span> <span data-ttu-id="037b3-110">Приложение должно зарегистрироваться в качестве поставщика ключей с помощью интерфейсов **IServiceProvider** и **IObjectWithSite** com.</span><span class="sxs-lookup"><span data-stu-id="037b3-110">The application must register as a key provider using the COM **IServiceProvider** and **IObjectWithSite** interfaces.</span></span> <span data-ttu-id="037b3-111">С помощью этого метода приложение реализует класс поставщика ключей, производный от **IServiceProvider**.</span><span class="sxs-lookup"><span data-stu-id="037b3-111">Using this technique, the application implements a key provider class derived from **IServiceProvider**.</span></span> <span data-ttu-id="037b3-112">Этот класс реализует три стандартных метода COM:**AddRef**, **QueryInterface** и **Release**— вместе с одним дополнительным методом **QueryService**, который вызывается диспетчером графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="037b3-112">This class implements the three standard COM methods—**AddRef**, **QueryInterface**, and **Release**—along with one additional method, **QueryService**, which is called by the filter graph manager.</span></span> <span data-ttu-id="037b3-113">**QueryService** вызывает метод пакета SDK Windows Media Format [**вмкреатецертификате**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) и возвращает в Диспетчер графа фильтров указатель на созданный сертификат.</span><span class="sxs-lookup"><span data-stu-id="037b3-113">**QueryService** calls the Windows Media Format SDK method [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) and returns to the filter graph manager a pointer to the certificate that was created.</span></span> <span data-ttu-id="037b3-114">Если сертификат действителен, диспетчер графа фильтров разрешает продолжение процесса построения графа.</span><span class="sxs-lookup"><span data-stu-id="037b3-114">If the certificate is valid, the filter graph manager allows the graph-building process to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="037b3-115">Чтобы создать приложение, включите Вмсдкидл. h в прототип для [**вмкреатецертификате**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))и свяжите с библиотекой вмстуб. lib.</span><span class="sxs-lookup"><span data-stu-id="037b3-115">To build an application, include Wmsdkidl.h for the prototype for [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)), and link to the Wmstub.lib library.</span></span>

 

<span data-ttu-id="037b3-116">В следующем примере кода показаны основные шаги этого процесса.</span><span class="sxs-lookup"><span data-stu-id="037b3-116">The following code example illustrates the basic steps in this process:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="037b3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="037b3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="037b3-118">Создание файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="037b3-118">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
