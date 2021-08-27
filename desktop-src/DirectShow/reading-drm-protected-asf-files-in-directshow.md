---
description: в этом разделе описывается использование DirectShow для воспроизведения файлов мультимедиа, защищенных с помощью Windows media Digital Rights Management (DRM).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Чтение DRM-Protected файлов ASF в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46eaafe96b00019e7c4e69741c251bc0079c459d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466581"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a>Чтение DRM-Protected файлов ASF в DirectShow

в этом разделе описывается использование DirectShow для воспроизведения файлов мультимедиа, защищенных с помощью Windows media Digital Rights Management (DRM).

## <a name="drm-concepts"></a>Основные понятия DRM

защита файла мультимедиа с помощью Windows media DRM включает два отдельных шага:

-   Поставщик содержимого упаковывает файл, то есть шифрует его и прикрепляет сведения о лицензировании к заголовку ASF-файла. Сведения о лицензировании включают URL-адрес, по которому клиент может получить лицензию.
-   Клиентское приложение получает лицензию на содержимое.

Упаковка происходит перед распространением файла. Получение лицензии происходит, когда пользователь пытается воспроизвести или скопировать файл. Приобретение лицензий может быть либо *скрытым* , либо *не скрытым*. При автоматическом получении не требуется никакого взаимодействия с пользователем. При приобретении без уведомления необходимо, чтобы приложение открывало окно браузера и отображало веб-страницу для пользователя. На этом этапе пользователю может потребоваться предоставить некоторый тип информации поставщику содержимого. Однако для обоих типов приобретения лицензий клиент должен отправить HTTP-запрос на сервер лицензирования.

### <a name="drm-versions"></a>Версии DRM

существует несколько версий Windows Media DRM. С точки зрения клиентского приложения они могут быть сгруппированы в две категории: DRM версии 1 и DRM версии 7 или более поздней. (Вторая категория включает в себя DRM версии 9 и 10, а также версию 7.) Причина классификации версий DRM заключается в том, что лицензии версии 1 обрабатываются несколько иначе, чем лицензии версии 7 или более поздней. В этой документации термин *Лицензия версии 7* означает версию 7 или более позднюю.

Также важно отличать упаковку DRM от лицензии DRM. если файл упакован с помощью Windows Media Rights Manager версии 7 или более поздней, в дополнение к url-адресу лицензии версии 7 заголовок DRM может содержать url-адрес лицензии версии 1. URL-адрес лицензии версии 1 позволяет использовать более старые проигрыватели, которые не поддерживают версию 7 для получения лицензии на содержимое. Однако наоборот не имеет значения true, поэтому файл с упаковкой версии 1 не может иметь URL-адрес лицензии версии 7.

### <a name="application-security-level"></a>Уровень безопасности приложения

Для воспроизведения файлов, защищенных с помощью DRM, клиентское приложение должно быть связано со статической библиотекой, предоставляемой корпорацией Майкрософт в двоичном формате. Эта библиотека, однозначно идентифицирующая приложение, иногда называется библиотекой заглушек. Библиотека-заглушка имеет назначенный уровень безопасности, значение которого определяется лицензионным соглашением, подписанным при получении библиотеки-заглушки.

Поставщик содержимого задает минимальный уровень безопасности, необходимый для получения лицензии. Если уровень безопасности библиотеки заглушек меньше минимального уровня безопасности, необходимого серверу лицензирования, приложение не сможет получить лицензию.

### <a name="individualization"></a>Индивидуальная

Для повышения безопасности приложение может обновить компоненты DRM на клиентском компьютере. Это обновление, называемое индивидуальной, отличает пользовательскую копию приложения от всех остальных копий того же приложения. В заголовке DRM защищенного файла может указываться минимальный уровень индивидуализации. (дополнительные сведения см. в документации по вмрмхеадер. индивидуализедверсион в пакете SDK для Windows Media Rights Manager.)

Так как служба Microsoft индивидуализации обрабатывает сведения от пользователя, необходимо отобразить политику конфиденциальности Майкрософт или указать ссылку на эту страницу на веб-сайте Майкрософт перед тем, как ваше приложение индивидуализес: <https://go.microsoft.com/fwlink/p/?linkid=10240> .

## <a name="provide-the-software-certificate"></a>Укажите сертификат программного обеспечения

чтобы разрешить приложению использовать лицензию DRM, приложение должно предоставить сертификат или *ключ* программного обеспечения для фильтра Graph Manager. Этот ключ содержится в статической библиотеке, которая является индивидуальной для приложения. сведения о получении отдельной библиотеки см. в разделе [получение необходимой библиотеки DRM](../wmformat/obtaining-the-required-drm-library.md) в документации по пакету SDK Windows Media Format.

Чтобы указать программный ключ, выполните следующие действия.

1.  Ссылка на статическую библиотеку.
2.  Реализуйте интерфейс **IServiceProvider** .
3.  запросите Graph диспетчера фильтров для интерфейса [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .
4.  Вызовите [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) с указателем на вашу реализацию **IServiceProvider**.
5.  фильтр Graph Manager вызывает **IServiceProvider:: QueryService**, указывая **IID \_ ивмреадер** для идентификатора службы.
6.  В реализации **QueryService** вызовите [**вмкреатецертификате**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) , чтобы создать ключ программного обеспечения.

В следующем коде показано, как реализовать метод **QueryService** :


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
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
```



в следующем коде показано, как вызвать [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) для фильтра Graph Manager:


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a>Создание Graph воспроизведения

Чтобы воспроизвести файл ASF, защищенный с помощью DRM, выполните следующие действия.

1.  создайте [фильтр Graph Manager](filter-graph-manager.md) и используйте интерфейс [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) для регистрации событий Graph.
2.  Вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать новый экземпляр фильтра [чтения WM ASF](wm-asf-reader-filter.md) .
3.  Вызовите [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить фильтр к графу фильтра.
4.  Запросите фильтр для интерфейса [**ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .
5.  Вызовите [**ифилесаурцефилтер:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) с URL-адресом файла.
6.  Обрабатывайте события [**\_ \_ событий EC ВМТ**](ec-wmt-event.md) .
7.  В первом событии [**EC \_ ВМТ \_ event**](ec-wmt-event.md) запросите фильтр [чтения WM ASF](wm-asf-reader-filter.md) для интерфейса **IServiceProvider** .
8.  Вызовите **IServiceProvider:: QueryService** , чтобы получить указатель на интерфейс [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .
9.  Вызовите [**играфбуилдер:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) , чтобы отобразить выходные контакты фильтра [чтения WM ASF](wm-asf-reader-filter.md) .

> [!Note]  
> При открытии файла, защищенного с помощью DRM, не вызывайте [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) для создания графа фильтра. Фильтр чтения WM ASF не может подключиться к другим фильтрам, пока не будет получена лицензия DRM. Для этого шага требуется, чтобы приложение использовало интерфейс [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , который должен быть получен из фильтра, как описано в шагах 7 – 8. Поэтому необходимо создать фильтр и добавить его в граф.

 

> [!Note]  
> Важно зарегистрировать события Graph (шаг 1) перед добавлением фильтра [чтения WM ASF](wm-asf-reader-filter.md) к графу (шаг 3), поскольку приложение должно выполнять обработку событий [**\_ \_ событий EC ВМТ**](ec-wmt-event.md) . События отправляются при вызове [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) (шаг 5).

 

В следующем коде показано, как построить граф:


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```

<span codelanguage="ManagedCPlusPlus"></span>


| C++ | 
|-----|
| <pre><code>            if (FAILED(hr))            {                goto done;            }            hr = RenderOutputPins(pGraph, m_pReader);    }    else    {        // Not a Windows Media file, so just render the standard way.        hr = pGraph-&gt;RenderFile(pwszFile, NULL);    }done:    return hr;}</code></pre> | 




В приведенном выше коде `RenderOutputPins` Функция перечисляет контакты вывода в фильтре [чтения WM ASF](wm-asf-reader-filter.md) и вызывает [**играфбуилдер:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) для каждого ПИН-кода.


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



В следующем коде показано, как получить указатель на интерфейс [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) из [модуля чтения WM ASF](wm-asf-reader-filter.md):


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
