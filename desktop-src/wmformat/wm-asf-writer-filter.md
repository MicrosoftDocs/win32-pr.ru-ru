---
title: Фильтр модуля записи WM ASF (пакет SDK для формата Windows Media 11)
description: Узнайте о фильтре модуля записи WM ASF для пакета SDK Windows Media Format 11. Просмотрите сведения о фильтре и см. связанные разделы.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, модуль записи WM ASF
- DirectShow, модуль записи WM ASF
- Фильтры КАСФ, модуль записи WM ASF
- Модуль записи WM ASF, сведения
- Расширенный формат систем (ASF), модуль записи WM ASF
- ASF (Расширенный системный формат), модуль записи WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee013b55455c3100ee23e076b767d70fb3ffda
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119669"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="5cc09-110">Фильтр модуля записи WM ASF (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="5cc09-110">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="5cc09-111">Фильтр модуля записи WM ASF принимает переменное число входных потоков и создает файл ASF.</span><span class="sxs-lookup"><span data-stu-id="5cc09-111">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="5cc09-112">Фильтр обрабатывает все сжатие и мультиплексирование (хотя механизм сжатия можно обойти).</span><span class="sxs-lookup"><span data-stu-id="5cc09-112">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="5cc09-113">Фильтр модуля записи WM ASF можно использовать в различных сценариях, включая видеозапись цифрового видео (DV), повторное сжатие звука и преобразование Audio-Video файлов с чередованием (AVI) или файлы мультимедиа MPEG для сетевой потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5cc09-113">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="5cc09-114">Этот фильтр предоставляет единственный способ создания видеофайлов Microsoft Windows Media Audio и Windows Media в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5cc09-114">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="5cc09-115">Дополнительные сведения см. [в разделе Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="5cc09-115">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="5cc09-116">В следующей таблице содержатся сведения о фильтре модуля записи WM ASF, например интерфейсах и типах носителей, которые он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="5cc09-116">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="5cc09-117">Сведения о фильтре</span><span class="sxs-lookup"><span data-stu-id="5cc09-117">Filter Information</span></span>                       |  <span data-ttu-id="5cc09-118">Типы</span><span class="sxs-lookup"><span data-stu-id="5cc09-118">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc09-119">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="5cc09-119">Filter interfaces</span></span>      | <span data-ttu-id="5cc09-120">**Иамфилтермискфлагс**, **ибасефилтер**, **иконфигасфвритер**, **IFileSinkFilter2**, Имедиасикинг, IPersistStream, IServiceProvider, испеЦифипропертипажес, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="5cc09-120">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="5cc09-121">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="5cc09-121">Input pin media types</span></span>  | <span data-ttu-id="5cc09-122">Зависит от профиля.</span><span class="sxs-lookup"><span data-stu-id="5cc09-122">Dependent on the profile.</span></span> <span data-ttu-id="5cc09-123">Обычно это несжатые типы, такие как MEDIATYPE \_ Audio или MediaType \_ Video, хотя сжатые типы могут быть приняты, если они соответствуют профилю.</span><span class="sxs-lookup"><span data-stu-id="5cc09-123">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="5cc09-124">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="5cc09-124">Input pin interfaces</span></span>   | <span data-ttu-id="5cc09-125">**Ипин**, **имеминпутпин**, **иамстреамконфиг**, **IServiceProvider**, **иамвмбуфферпасс**, **IWMStreamConfig2** (через **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="5cc09-125">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="5cc09-126">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="5cc09-126">Output pin media types</span></span> | <span data-ttu-id="5cc09-127">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="5cc09-127">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="5cc09-128">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="5cc09-128">Output pin interfaces</span></span>  | <span data-ttu-id="5cc09-129">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="5cc09-129">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="5cc09-130">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="5cc09-130">Filter CLSID</span></span>           | <span data-ttu-id="5cc09-131">\_ВМАСФВРИТЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="5cc09-131">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="5cc09-132">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="5cc09-132">Property page CLSID</span></span>    | <span data-ttu-id="5cc09-133">\_ВМАСФВРИТЕРПРОПЕРТИЕС CLSID</span><span class="sxs-lookup"><span data-stu-id="5cc09-133">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="5cc09-134">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="5cc09-134">Executable</span></span>             | <span data-ttu-id="5cc09-135">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="5cc09-135">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="5cc09-136">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="5cc09-136">Merit</span></span>                  | <span data-ttu-id="5cc09-137">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="5cc09-137">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="5cc09-138">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="5cc09-138">Filter Category</span></span>        | <span data-ttu-id="5cc09-139">Не указано</span><span class="sxs-lookup"><span data-stu-id="5cc09-139">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="5cc09-140">Remarks</span><span class="sxs-lookup"><span data-stu-id="5cc09-140">Remarks</span></span>

<span data-ttu-id="5cc09-141">Количество входных контактов фильтра зависит от профиля, который передается в фильтр.</span><span class="sxs-lookup"><span data-stu-id="5cc09-141">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="5cc09-142">Для каждого потока, определенного в профиле, создается один ПИН-код соответствующего типа носителя.</span><span class="sxs-lookup"><span data-stu-id="5cc09-142">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="5cc09-143">Входные сигналы поддерживают один метод из интерфейса **иамстреамконфиг** : **иамстреамконфиг::-Format**.</span><span class="sxs-lookup"><span data-stu-id="5cc09-143">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="5cc09-144">Все остальные методы возвращают E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="5cc09-144">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="5cc09-145">Вызовите метод **OnFormat** , чтобы запросить формат сжатия целевого объекта ПИН-кода, который определяется текущим профилем.</span><span class="sxs-lookup"><span data-stu-id="5cc09-145">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="5cc09-146">Чтобы задать профиль, используйте интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5cc09-146">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="5cc09-147">Интерфейс **IServiceProvider** фильтра позволяет приложениям получать интерфейс [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , который определен в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5cc09-147">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="5cc09-148">Интерфейс **IWMWriterAdvanced2** управляет дечередованием видео и полезен, если входные данные представляют собой [*чередующийся*](wmformat-glossary.md) источник, например DV (цифровое видео).</span><span class="sxs-lookup"><span data-stu-id="5cc09-148">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="5cc09-149">Используйте методы **жетинпутсеттинг** и **сетинпутсеттинг** для управления разчередованием.</span><span class="sxs-lookup"><span data-stu-id="5cc09-149">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="5cc09-150">Не рекомендуется, чтобы клиенты использовали другие методы этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5cc09-150">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="5cc09-151">Этот интерфейс можно получить только после добавления фильтра к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="5cc09-151">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="5cc09-152">В следующем примере показано, как запросить этот интерфейс:</span><span class="sxs-lookup"><span data-stu-id="5cc09-152">The following example shows how to query for this interface:</span></span>


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="5cc09-153">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5cc09-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cc09-154">**Справочник по КАСФ DirectShow**</span><span class="sxs-lookup"><span data-stu-id="5cc09-154">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
