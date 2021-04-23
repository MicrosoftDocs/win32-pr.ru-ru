---
description: Фильтр средства синтаксического анализа SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Фильтр средства синтаксического анализа SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77f0aa2d913b7f0295a078c8174ae483bb1cb62
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909682"
---
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="190d4-103">Фильтр средства синтаксического анализа SAMI (CC)</span><span class="sxs-lookup"><span data-stu-id="190d4-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="190d4-104">Анализирует заголовки данных из синхронизированных доступных файлов обмена мультимедиа (SAMI).</span><span class="sxs-lookup"><span data-stu-id="190d4-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="190d4-105">Саамский является текстовым форматом, похожим на HTML, и используется для кодирования заголовков на основе времени.</span><span class="sxs-lookup"><span data-stu-id="190d4-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="190d4-106">Этот фильтр преобразует данные SAMIs в текстовый поток.</span><span class="sxs-lookup"><span data-stu-id="190d4-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="190d4-107">Каждый пример в потоке содержит одну запись заголовка, а также сведения о форматировании.</span><span class="sxs-lookup"><span data-stu-id="190d4-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="190d4-108">Метки времени для образцов формируются на основе сведений о времени в файле SAMI.</span><span class="sxs-lookup"><span data-stu-id="190d4-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="190d4-109">Этот фильтр предназначен для использования с фильтром модуля [подготовки](internal-script-command-renderer-filter.md) отчетов для внутреннего выполнения.</span><span class="sxs-lookup"><span data-stu-id="190d4-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="190d4-110">Модуль подготовки отчетов команды внутреннего сценария получает текстовые примеры и отправляет их в приложение в виде уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="190d4-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="190d4-111">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="190d4-111">For more information, see the Remarks section.</span></span>



| <span data-ttu-id="190d4-112">Метка</span><span class="sxs-lookup"><span data-stu-id="190d4-112">Label</span></span> | <span data-ttu-id="190d4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="190d4-113">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="190d4-114">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="190d4-114">Filter Interfaces</span></span>                        | <span data-ttu-id="190d4-115">[**Иамстреамселект**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="190d4-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="190d4-116">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="190d4-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="190d4-117">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="190d4-117">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="190d4-118">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="190d4-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="190d4-119">[**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="190d4-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="190d4-120">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="190d4-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="190d4-121">MEDIATYPE \_ Text, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="190d4-121">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="190d4-122">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="190d4-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="190d4-123">[**Имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="190d4-123">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="190d4-124">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="190d4-124">Filter CLSID</span></span>                             | <span data-ttu-id="190d4-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="190d4-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="190d4-126">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="190d4-126">Property Page CLSID</span></span>                      | <span data-ttu-id="190d4-127">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="190d4-127">No property page</span></span>                                                                                         |
| <span data-ttu-id="190d4-128">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="190d4-128">Executable</span></span>                               | <span data-ttu-id="190d4-129">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="190d4-129">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="190d4-130">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="190d4-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="190d4-131">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="190d4-131">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="190d4-132">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="190d4-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="190d4-133">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="190d4-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="190d4-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="190d4-134">Remarks</span></span>

<span data-ttu-id="190d4-135">Ниже приведен простой файл SAMI:</span><span class="sxs-lookup"><span data-stu-id="190d4-135">The following is a simple SAMI file:</span></span>


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



<span data-ttu-id="190d4-136">Тег **Style** определяет два языковых параметра: Английский (. ЕНКК) и французский (. ФРКК).</span><span class="sxs-lookup"><span data-stu-id="190d4-136">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="190d4-137">Он также определяет два стиля: \# обычные и \# гринтекст.</span><span class="sxs-lookup"><span data-stu-id="190d4-137">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="190d4-138">Каждый тег **синхронизации** определяет время начала для заголовка в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="190d4-138">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="190d4-139">Теги **P** содержат текст заголовка, а атрибут **Class** задает языковой параметр, к которому применяется заголовок.</span><span class="sxs-lookup"><span data-stu-id="190d4-139">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="190d4-140">Для каждого языка и стиля фильтр создает логический поток.</span><span class="sxs-lookup"><span data-stu-id="190d4-140">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="190d4-141">В любое время включается ровно один языковой поток и один поток стилей.</span><span class="sxs-lookup"><span data-stu-id="190d4-141">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="190d4-142">Когда фильтр формирует образец, он выбирает заголовок для текущего языка и применяет текущий стиль.</span><span class="sxs-lookup"><span data-stu-id="190d4-142">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="190d4-143">По умолчанию первый язык и стиль, объявленный в файле, включены.</span><span class="sxs-lookup"><span data-stu-id="190d4-143">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="190d4-144">Приложение может использовать метод [**иамстреамселект:: enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) для включения другого потока.</span><span class="sxs-lookup"><span data-stu-id="190d4-144">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="190d4-145">При использовании параметров по умолчанию первый заголовок в файле Example создает следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="190d4-145">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="190d4-146">Если выходные данные попадают во внутренний модуль подготовки команд сценария, этот фильтр отправляет уведомление о событии [**\_ \_ событий EC OLE**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="190d4-146">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="190d4-147">Второй параметр события — это BSTR с текстом заголовка.</span><span class="sxs-lookup"><span data-stu-id="190d4-147">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="190d4-148">Приложение может получить событие и отобразить заголовок.</span><span class="sxs-lookup"><span data-stu-id="190d4-148">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="190d4-149">В следующем примере показано, как отобразить файл SAMI, получить сведения о потоке, включить потоки и отобразить текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="190d4-149">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="190d4-150">В примере предполагается, что предыдущий файл SAMId сохранен как C: \\ Sami \_ Test \_ File. Sami.</span><span class="sxs-lookup"><span data-stu-id="190d4-150">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="190d4-151">Для краткости в этом примере использовались жестко закодированные индексы потоков при вызове метода **иамстреамселект:: enable** .</span><span class="sxs-lookup"><span data-stu-id="190d4-151">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="190d4-152">Он также выполняет минимальную проверку на наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="190d4-152">It also performs minimal error checking.</span></span>


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



<span data-ttu-id="190d4-153">Этот фильтр использует интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) для извлечения образцов из фильтра источника.</span><span class="sxs-lookup"><span data-stu-id="190d4-153">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="190d4-154">Поэтому он не поддерживает интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) на входном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="190d4-154">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="190d4-155">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="190d4-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="190d4-156">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="190d4-156">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



