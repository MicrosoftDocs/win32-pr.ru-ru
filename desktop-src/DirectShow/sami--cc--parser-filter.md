---
description: Фильтр средства синтаксического анализа SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Фильтр средства синтаксического анализа SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0449bccd41a09fca952b5d84552ef919055526
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537682"
---
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="24bd2-103">Фильтр средства синтаксического анализа SAMI (CC)</span><span class="sxs-lookup"><span data-stu-id="24bd2-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="24bd2-104">Анализирует заголовки данных из синхронизированных доступных файлов обмена мультимедиа (SAMI).</span><span class="sxs-lookup"><span data-stu-id="24bd2-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="24bd2-105">Саамский является текстовым форматом, похожим на HTML, и используется для кодирования заголовков на основе времени.</span><span class="sxs-lookup"><span data-stu-id="24bd2-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="24bd2-106">Этот фильтр преобразует данные SAMIs в текстовый поток.</span><span class="sxs-lookup"><span data-stu-id="24bd2-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="24bd2-107">Каждый пример в потоке содержит одну запись заголовка, а также сведения о форматировании.</span><span class="sxs-lookup"><span data-stu-id="24bd2-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="24bd2-108">Метки времени для образцов формируются на основе сведений о времени в файле SAMI.</span><span class="sxs-lookup"><span data-stu-id="24bd2-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="24bd2-109">Этот фильтр предназначен для использования с фильтром модуля [подготовки](internal-script-command-renderer-filter.md) отчетов для внутреннего выполнения.</span><span class="sxs-lookup"><span data-stu-id="24bd2-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="24bd2-110">Модуль подготовки отчетов команды внутреннего сценария получает текстовые примеры и отправляет их в приложение в виде уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="24bd2-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="24bd2-111">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="24bd2-111">For more information, see the Remarks section.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24bd2-112">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="24bd2-112">Filter Interfaces</span></span>                        | <span data-ttu-id="24bd2-113">[**Иамстреамселект**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="24bd2-113">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="24bd2-114">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="24bd2-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="24bd2-115">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="24bd2-115">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="24bd2-116">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="24bd2-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="24bd2-117">[**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="24bd2-117">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="24bd2-118">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="24bd2-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="24bd2-119">MEDIATYPE \_ Text, медиасубтипе \_ null</span><span class="sxs-lookup"><span data-stu-id="24bd2-119">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="24bd2-120">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="24bd2-120">Output Pin Interfaces</span></span>                    | <span data-ttu-id="24bd2-121">[**Имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="24bd2-121">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="24bd2-122">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="24bd2-122">Filter CLSID</span></span>                             | <span data-ttu-id="24bd2-123">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="24bd2-123">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="24bd2-124">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="24bd2-124">Property Page CLSID</span></span>                      | <span data-ttu-id="24bd2-125">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="24bd2-125">No property page</span></span>                                                                                         |
| <span data-ttu-id="24bd2-126">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="24bd2-126">Executable</span></span>                               | <span data-ttu-id="24bd2-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="24bd2-127">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="24bd2-128">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="24bd2-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="24bd2-129">\_маловероятно</span><span class="sxs-lookup"><span data-stu-id="24bd2-129">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="24bd2-130">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="24bd2-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="24bd2-131">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="24bd2-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="24bd2-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24bd2-132">Remarks</span></span>

<span data-ttu-id="24bd2-133">Ниже приведен простой файл SAMI:</span><span class="sxs-lookup"><span data-stu-id="24bd2-133">The following is a simple SAMI file:</span></span>


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



<span data-ttu-id="24bd2-134">Тег **Style** определяет два языковых параметра: Английский (. ЕНКК) и французский (. ФРКК).</span><span class="sxs-lookup"><span data-stu-id="24bd2-134">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="24bd2-135">Он также определяет два стиля: \# обычные и \# гринтекст.</span><span class="sxs-lookup"><span data-stu-id="24bd2-135">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="24bd2-136">Каждый тег **синхронизации** определяет время начала для заголовка в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="24bd2-136">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="24bd2-137">Теги **P** содержат текст заголовка, а атрибут **Class** задает языковой параметр, к которому применяется заголовок.</span><span class="sxs-lookup"><span data-stu-id="24bd2-137">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="24bd2-138">Для каждого языка и стиля фильтр создает логический поток.</span><span class="sxs-lookup"><span data-stu-id="24bd2-138">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="24bd2-139">В любое время включается ровно один языковой поток и один поток стилей.</span><span class="sxs-lookup"><span data-stu-id="24bd2-139">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="24bd2-140">Когда фильтр формирует образец, он выбирает заголовок для текущего языка и применяет текущий стиль.</span><span class="sxs-lookup"><span data-stu-id="24bd2-140">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="24bd2-141">По умолчанию первый язык и стиль, объявленный в файле, включены.</span><span class="sxs-lookup"><span data-stu-id="24bd2-141">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="24bd2-142">Приложение может использовать метод [**иамстреамселект:: enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) для включения другого потока.</span><span class="sxs-lookup"><span data-stu-id="24bd2-142">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="24bd2-143">При использовании параметров по умолчанию первый заголовок в файле Example создает следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="24bd2-143">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="24bd2-144">Если выходные данные попадают во внутренний модуль подготовки команд сценария, этот фильтр отправляет уведомление о событии [**\_ \_ событий EC OLE**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="24bd2-144">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="24bd2-145">Второй параметр события — это BSTR с текстом заголовка.</span><span class="sxs-lookup"><span data-stu-id="24bd2-145">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="24bd2-146">Приложение может получить событие и отобразить заголовок.</span><span class="sxs-lookup"><span data-stu-id="24bd2-146">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="24bd2-147">В следующем примере показано, как отобразить файл SAMI, получить сведения о потоке, включить потоки и отобразить текст заголовка.</span><span class="sxs-lookup"><span data-stu-id="24bd2-147">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="24bd2-148">В примере предполагается, что предыдущий файл SAMId сохранен как C: \\ Sami \_ Test \_ File. Sami.</span><span class="sxs-lookup"><span data-stu-id="24bd2-148">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="24bd2-149">Для краткости в этом примере использовались жестко закодированные индексы потоков при вызове метода **иамстреамселект:: enable** .</span><span class="sxs-lookup"><span data-stu-id="24bd2-149">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="24bd2-150">Он также выполняет минимальную проверку на наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="24bd2-150">It also performs minimal error checking.</span></span>


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



<span data-ttu-id="24bd2-151">Этот фильтр использует интерфейс [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) для извлечения образцов из фильтра источника.</span><span class="sxs-lookup"><span data-stu-id="24bd2-151">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="24bd2-152">Поэтому он не поддерживает интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) на входном ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="24bd2-152">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24bd2-153">См. также</span><span class="sxs-lookup"><span data-stu-id="24bd2-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24bd2-154">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="24bd2-154">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



