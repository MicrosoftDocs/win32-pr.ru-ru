---
description: В этом разделе описывается использование DirectShow для воспроизведения файлов мультимедиа, защищенных с помощью цифрового Rights Management Windows Media (DRM).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Чтение DRM-Protected файлов ASF в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105684802"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a><span data-ttu-id="93650-103">Чтение DRM-Protected файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="93650-103">Reading DRM-Protected ASF Files in DirectShow</span></span>

<span data-ttu-id="93650-104">В этом разделе описывается использование DirectShow для воспроизведения файлов мультимедиа, защищенных с помощью цифрового Rights Management Windows Media (DRM).</span><span class="sxs-lookup"><span data-stu-id="93650-104">This topic describes how to use DirectShow to play media files that are protected with Windows Media Digital Rights Management (DRM).</span></span>

## <a name="drm-concepts"></a><span data-ttu-id="93650-105">Основные понятия DRM</span><span class="sxs-lookup"><span data-stu-id="93650-105">DRM Concepts</span></span>

<span data-ttu-id="93650-106">Защита файла мультимедиа с помощью Windows Media DRM состоит из двух отдельных этапов:</span><span class="sxs-lookup"><span data-stu-id="93650-106">Protecting a media file with Windows Media DRM involves two distinct steps:</span></span>

-   <span data-ttu-id="93650-107">Поставщик содержимого упаковывает файл, то есть шифрует его и прикрепляет сведения о лицензировании к заголовку ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="93650-107">The content provider packages the file—that is, encrypts the file and attaches licensing information to the ASF file header.</span></span> <span data-ttu-id="93650-108">Сведения о лицензировании включают URL-адрес, по которому клиент может получить лицензию.</span><span class="sxs-lookup"><span data-stu-id="93650-108">The licensing information includes a URL where the client can obtain the license.</span></span>
-   <span data-ttu-id="93650-109">Клиентское приложение получает лицензию на содержимое.</span><span class="sxs-lookup"><span data-stu-id="93650-109">The client application acquires a license for the content.</span></span>

<span data-ttu-id="93650-110">Упаковка происходит перед распространением файла.</span><span class="sxs-lookup"><span data-stu-id="93650-110">Packaging happens before the file is distributed.</span></span> <span data-ttu-id="93650-111">Получение лицензии происходит, когда пользователь пытается воспроизвести или скопировать файл.</span><span class="sxs-lookup"><span data-stu-id="93650-111">License acquisition occurs when the user tries to play or copy the file.</span></span> <span data-ttu-id="93650-112">Приобретение лицензий может быть либо *скрытым* , либо *не скрытым*.</span><span class="sxs-lookup"><span data-stu-id="93650-112">License acquisition may be either *silent* or *non-silent*.</span></span> <span data-ttu-id="93650-113">При автоматическом получении не требуется никакого взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="93650-113">Silent acquisition does not require any interaction with the user.</span></span> <span data-ttu-id="93650-114">При приобретении без уведомления необходимо, чтобы приложение открывало окно браузера и отображало веб-страницу для пользователя.</span><span class="sxs-lookup"><span data-stu-id="93650-114">Non-silent acquisition requires the application to open a browser window and display a web page to the user.</span></span> <span data-ttu-id="93650-115">На этом этапе пользователю может потребоваться предоставить некоторый тип информации поставщику содержимого.</span><span class="sxs-lookup"><span data-stu-id="93650-115">At that point, the user might need to provide some kind of information to the content provider.</span></span> <span data-ttu-id="93650-116">Однако для обоих типов приобретения лицензий клиент должен отправить HTTP-запрос на сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="93650-116">However, both types of license acquisition require the client to submit an HTTP request to a license server.</span></span>

### <a name="drm-versions"></a><span data-ttu-id="93650-117">Версии DRM</span><span class="sxs-lookup"><span data-stu-id="93650-117">DRM Versions</span></span>

<span data-ttu-id="93650-118">Существует несколько версий Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="93650-118">Several versions of Windows Media DRM exist.</span></span> <span data-ttu-id="93650-119">С точки зрения клиентского приложения они могут быть сгруппированы в две категории: DRM версии 1 и DRM версии 7 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="93650-119">From the perspective of a client application, they can be grouped into two categories: DRM version 1, and DRM version 7 or later.</span></span> <span data-ttu-id="93650-120">(Вторая категория включает в себя DRM версии 9 и 10, а также версию 7.) Причина классификации версий DRM заключается в том, что лицензии версии 1 обрабатываются несколько иначе, чем лицензии версии 7 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="93650-120">(The second category includes DRM versions 9 and 10, as well as version 7.) The reason for categorizing DRM versions this way is that version 1 licenses are handled somewhat differently than version 7 or later licenses.</span></span> <span data-ttu-id="93650-121">В этой документации термин *Лицензия версии 7* означает версию 7 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="93650-121">In this documentation, the term *version 7 license* means version 7 or later.</span></span>

<span data-ttu-id="93650-122">Также важно отличать упаковку DRM от лицензии DRM.</span><span class="sxs-lookup"><span data-stu-id="93650-122">It is also important to distinguish the DRM packaging from the DRM license.</span></span> <span data-ttu-id="93650-123">Если файл упакован с помощью Windows Media Rights Manager версии 7 или более поздней, в дополнение к URL-адресу лицензии версии 7 заголовок DRM может содержать URL-адрес лицензии версии 1.</span><span class="sxs-lookup"><span data-stu-id="93650-123">If the file is packaged using Windows Media Rights Manager version 7 or later, the DRM header can contain a version 1 license URL in addition to the version 7 license URL.</span></span> <span data-ttu-id="93650-124">URL-адрес лицензии версии 1 позволяет использовать более старые проигрыватели, которые не поддерживают версию 7 для получения лицензии на содержимое.</span><span class="sxs-lookup"><span data-stu-id="93650-124">The version 1 license URL enables older players that do not support version 7 to obtain a license for the content.</span></span> <span data-ttu-id="93650-125">Однако наоборот не имеет значения true, поэтому файл с упаковкой версии 1 не может иметь URL-адрес лицензии версии 7.</span><span class="sxs-lookup"><span data-stu-id="93650-125">However, the converse is not true, so a file with version 1 packaging cannot have a version 7 license URL.</span></span>

### <a name="application-security-level"></a><span data-ttu-id="93650-126">Уровень безопасности приложения</span><span class="sxs-lookup"><span data-stu-id="93650-126">Application Security Level</span></span>

<span data-ttu-id="93650-127">Для воспроизведения файлов, защищенных с помощью DRM, клиентское приложение должно быть связано со статической библиотекой, предоставляемой корпорацией Майкрософт в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="93650-127">To play DRM-protected files, the client application must be linked to a static library that is provided in binary form by Microsoft.</span></span> <span data-ttu-id="93650-128">Эта библиотека, однозначно идентифицирующая приложение, иногда называется библиотекой заглушек.</span><span class="sxs-lookup"><span data-stu-id="93650-128">This library, which uniquely identifies the application, is sometimes called the stub library.</span></span> <span data-ttu-id="93650-129">Библиотека-заглушка имеет назначенный уровень безопасности, значение которого определяется лицензионным соглашением, подписанным при получении библиотеки-заглушки.</span><span class="sxs-lookup"><span data-stu-id="93650-129">The stub library has an assigned security level, the value of which is determined by the license agreement that you signed when you obtained the stub library.</span></span>

<span data-ttu-id="93650-130">Поставщик содержимого задает минимальный уровень безопасности, необходимый для получения лицензии.</span><span class="sxs-lookup"><span data-stu-id="93650-130">The content provider sets a minimum security level needed to acquire the license.</span></span> <span data-ttu-id="93650-131">Если уровень безопасности библиотеки заглушек меньше минимального уровня безопасности, необходимого серверу лицензирования, приложение не сможет получить лицензию.</span><span class="sxs-lookup"><span data-stu-id="93650-131">If the security level of your stub library is less than the minimum security level required by the license server, the application cannot obtain the license.</span></span>

### <a name="individualization"></a><span data-ttu-id="93650-132">Индивидуальная</span><span class="sxs-lookup"><span data-stu-id="93650-132">Individualization</span></span>

<span data-ttu-id="93650-133">Для повышения безопасности приложение может обновить компоненты DRM на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="93650-133">To increase security, an application may update the DRM components on the client's computer.</span></span> <span data-ttu-id="93650-134">Это обновление, называемое индивидуальной, отличает пользовательскую копию приложения от всех остальных копий того же приложения.</span><span class="sxs-lookup"><span data-stu-id="93650-134">This update, called individualization, differentiates the user's copy of the application from all other copies of the same application.</span></span> <span data-ttu-id="93650-135">В заголовке DRM защищенного файла может указываться минимальный уровень индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="93650-135">The DRM header of a protected file may specify may specify a minimum individualization level.</span></span> <span data-ttu-id="93650-136">(Дополнительные сведения см. в документации по Вмрмхеадер. Индивидуализедверсион в пакете SDK диспетчера прав Windows Media.)</span><span class="sxs-lookup"><span data-stu-id="93650-136">(For more information, see the documentation for WMRMHeader.IndividualizedVersion in the Windows Media Rights Manager SDK.)</span></span>

<span data-ttu-id="93650-137">Так как служба Microsoft индивидуализации обрабатывает сведения от пользователя, необходимо отобразить политику конфиденциальности Майкрософт или указать ссылку на эту страницу на веб-сайте Майкрософт перед тем, как ваше приложение индивидуализес: <https://go.microsoft.com/fwlink/p/?linkid=10240> .</span><span class="sxs-lookup"><span data-stu-id="93650-137">Because the Microsoft Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft website before your application individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240>.</span></span>

## <a name="provide-the-software-certificate"></a><span data-ttu-id="93650-138">Укажите сертификат программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="93650-138">Provide the Software Certificate</span></span>

<span data-ttu-id="93650-139">Чтобы разрешить приложению использовать лицензию DRM, приложение должно предоставить сертификат или *ключ* программного обеспечения для диспетчера графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="93650-139">To enable the application to use the DRM license, the application must provide a software certificate or *key* to the Filter Graph Manager.</span></span> <span data-ttu-id="93650-140">Этот ключ содержится в статической библиотеке, которая является индивидуальной для приложения.</span><span class="sxs-lookup"><span data-stu-id="93650-140">This key is contained in a static library that is individualized for the application.</span></span> <span data-ttu-id="93650-141">Сведения о получении отдельной библиотеки см. в разделе [получение необходимой библиотеки DRM](../wmformat/obtaining-the-required-drm-library.md) в документации по пакету SDK для Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="93650-141">For information about obtaining the individualized library, see [Obtaining the Required DRM Library](../wmformat/obtaining-the-required-drm-library.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="93650-142">Чтобы указать программный ключ, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="93650-142">To provide the software key, perform the following steps:</span></span>

1.  <span data-ttu-id="93650-143">Ссылка на статическую библиотеку.</span><span class="sxs-lookup"><span data-stu-id="93650-143">Link to the static library.</span></span>
2.  <span data-ttu-id="93650-144">Реализуйте интерфейс **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="93650-144">Implement the **IServiceProvider** interface.</span></span>
3.  <span data-ttu-id="93650-145">Запросите диспетчер графов фильтров для интерфейса [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .</span><span class="sxs-lookup"><span data-stu-id="93650-145">Query the Filter Graph Manager for the [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) interface.</span></span>
4.  <span data-ttu-id="93650-146">Вызовите [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) с указателем на вашу реализацию **IServiceProvider**.</span><span class="sxs-lookup"><span data-stu-id="93650-146">Call [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) with a pointer to your implementation of **IServiceProvider**.</span></span>
5.  <span data-ttu-id="93650-147">Диспетчер графа фильтров будет вызывать **IServiceProvider:: QueryService**, указывая **IID \_ ивмреадер** для идентификатора службы.</span><span class="sxs-lookup"><span data-stu-id="93650-147">The Filter Graph Manager will call **IServiceProvider::QueryService**, specifying **IID\_IWMReader** for the service identifier.</span></span>
6.  <span data-ttu-id="93650-148">В реализации **QueryService** вызовите [**вмкреатецертификате**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) , чтобы создать ключ программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="93650-148">In your implementation of **QueryService**, call [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) to create the software key.</span></span>

<span data-ttu-id="93650-149">В следующем коде показано, как реализовать метод **QueryService** :</span><span class="sxs-lookup"><span data-stu-id="93650-149">The following code shows how to implement the **QueryService** method:</span></span>


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



<span data-ttu-id="93650-150">В следующем коде показано, как вызвать [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) в диспетчере графов фильтров:</span><span class="sxs-lookup"><span data-stu-id="93650-150">The following code shows how to call [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) on the Filter Graph Manager:</span></span>


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





## <a name="building-the-playback-graph"></a><span data-ttu-id="93650-151">Создание графа воспроизведения</span><span class="sxs-lookup"><span data-stu-id="93650-151">Building the Playback Graph</span></span>

<span data-ttu-id="93650-152">Чтобы воспроизвести файл ASF, защищенный с помощью DRM, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="93650-152">To play a DRM-protected ASF file, perform the following steps:</span></span>

1.  <span data-ttu-id="93650-153">Создайте [Диспетчер графов фильтров](filter-graph-manager.md) и используйте интерфейс [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) для регистрации событий Graph.</span><span class="sxs-lookup"><span data-stu-id="93650-153">Create the [Filter Graph Manager](filter-graph-manager.md) and use the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to register for graph events.</span></span>
2.  <span data-ttu-id="93650-154">Вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать новый экземпляр фильтра [чтения WM ASF](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="93650-154">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>
3.  <span data-ttu-id="93650-155">Вызовите [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить фильтр к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="93650-155">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph.</span></span>
4.  <span data-ttu-id="93650-156">Запросите фильтр для интерфейса [**ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="93650-156">Query the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface.</span></span>
5.  <span data-ttu-id="93650-157">Вызовите [**ифилесаурцефилтер:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) с URL-адресом файла.</span><span class="sxs-lookup"><span data-stu-id="93650-157">Call [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) with the URL of the file.</span></span>
6.  <span data-ttu-id="93650-158">Обрабатывайте события [**\_ \_ событий EC ВМТ**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="93650-158">Handle [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span>
7.  <span data-ttu-id="93650-159">В первом событии [**EC \_ ВМТ \_ event**](ec-wmt-event.md) запросите фильтр [чтения WM ASF](wm-asf-reader-filter.md) для интерфейса **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="93650-159">On the first [**EC\_WMT\_EVENT**](ec-wmt-event.md) event, query the [WM ASF Reader](wm-asf-reader-filter.md) filter for the **IServiceProvider** interface.</span></span>
8.  <span data-ttu-id="93650-160">Вызовите **IServiceProvider:: QueryService** , чтобы получить указатель на интерфейс [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="93650-160">Call **IServiceProvider::QueryService** to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
9.  <span data-ttu-id="93650-161">Вызовите [**играфбуилдер:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) , чтобы отобразить выходные контакты фильтра [чтения WM ASF](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="93650-161">Call [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) to render the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="93650-162">При открытии файла, защищенного с помощью DRM, не вызывайте [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) для создания графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="93650-162">When opening a DRM-protected file, do not call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) to create the filter graph.</span></span> <span data-ttu-id="93650-163">Фильтр чтения WM ASF не может подключиться к другим фильтрам, пока не будет получена лицензия DRM.</span><span class="sxs-lookup"><span data-stu-id="93650-163">The WM ASF Reader filter cannot connect to any other filters until the DRM license is acquired.</span></span> <span data-ttu-id="93650-164">Для этого шага требуется, чтобы приложение использовало интерфейс [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , который должен быть получен из фильтра, как описано в шагах 7 – 8.</span><span class="sxs-lookup"><span data-stu-id="93650-164">This step requires the application to use the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface, which must be obtained from the filter, as described in steps 7–8.</span></span> <span data-ttu-id="93650-165">Поэтому необходимо создать фильтр и добавить его в граф.</span><span class="sxs-lookup"><span data-stu-id="93650-165">Therefore, you must create the filter and add it to the graph</span></span>

 

> [!Note]  
> <span data-ttu-id="93650-166">Важно зарегистрировать события Graph (шаг 1) перед добавлением фильтра [чтения WM ASF](wm-asf-reader-filter.md) к графу (шаг 3), поскольку приложение должно выполнять обработку событий [**\_ \_ событий EC ВМТ**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="93650-166">It is important to register for graph events (step 1) before adding the [WM ASF Reader](wm-asf-reader-filter.md) filter to the graph (step 3), because the application must handle the [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span> <span data-ttu-id="93650-167">События отправляются при вызове [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) (шаг 5).</span><span class="sxs-lookup"><span data-stu-id="93650-167">The events are sent when [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) is called (step 5).</span></span>

 

<span data-ttu-id="93650-168">В следующем коде показано, как построить граф:</span><span class="sxs-lookup"><span data-stu-id="93650-168">The following code shows how to build the graph:</span></span>


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

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93650-169">C++</span><span class="sxs-lookup"><span data-stu-id="93650-169">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="93650-170">В приведенном выше коде `RenderOutputPins` Функция перечисляет контакты вывода в фильтре [чтения WM ASF](wm-asf-reader-filter.md) и вызывает [**играфбуилдер:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) для каждого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="93650-170">In the previous code, the `RenderOutputPins` function enumerates the output pins on the [WM ASF Reader](wm-asf-reader-filter.md) filter and calls [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) for each pin.</span></span>


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



<span data-ttu-id="93650-171">В следующем коде показано, как получить указатель на интерфейс [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) из [модуля чтения WM ASF](wm-asf-reader-filter.md):</span><span class="sxs-lookup"><span data-stu-id="93650-171">The following code shows how to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md):</span></span>


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





## <a name="related-topics"></a><span data-ttu-id="93650-172">См. также</span><span class="sxs-lookup"><span data-stu-id="93650-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93650-173">Чтение файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="93650-173">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
