---
title: Фильтр модуля записи WM ASF (пакет SDK для формата Windows Media 11)
description: Узнайте о фильтре модуля записи WM ASF.
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
ms.openlocfilehash: d0fbd6e36a8178f6ebd1943cdaac214597e0ba4e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444705"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="fe343-109">Фильтр модуля записи WM ASF (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="fe343-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="fe343-110">Фильтр модуля записи WM ASF принимает переменное число входных потоков и создает файл ASF.</span><span class="sxs-lookup"><span data-stu-id="fe343-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="fe343-111">Фильтр обрабатывает все сжатие и мультиплексирование (хотя механизм сжатия можно обойти).</span><span class="sxs-lookup"><span data-stu-id="fe343-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="fe343-112">Фильтр модуля записи WM ASF можно использовать в различных сценариях, включая видеозапись цифрового видео (DV), повторное сжатие звука и преобразование Audio-Video файлов с чередованием (AVI) или файлы мультимедиа MPEG для сетевой потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="fe343-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="fe343-113">Этот фильтр предоставляет единственный способ создания видеофайлов Microsoft Windows Media Audio и Windows Media в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fe343-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="fe343-114">Дополнительные сведения см. [в разделе Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="fe343-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="fe343-115">В следующей таблице содержатся сведения о фильтре модуля записи WM ASF, например интерфейсах и типах носителей, которые он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="fe343-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="fe343-116">Сведения о фильтре</span><span class="sxs-lookup"><span data-stu-id="fe343-116">Filter Information</span></span>                       |  <span data-ttu-id="fe343-117">Типы</span><span class="sxs-lookup"><span data-stu-id="fe343-117">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe343-118">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="fe343-118">Filter interfaces</span></span>      | <span data-ttu-id="fe343-119">**Иамфилтермискфлагс**, **ибасефилтер**, **иконфигасфвритер**, **IFileSinkFilter2**, Имедиасикинг, IPersistStream, IServiceProvider, испеЦифипропертипажес, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="fe343-119">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="fe343-120">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="fe343-120">Input pin media types</span></span>  | <span data-ttu-id="fe343-121">Зависит от профиля.</span><span class="sxs-lookup"><span data-stu-id="fe343-121">Dependent on the profile.</span></span> <span data-ttu-id="fe343-122">Обычно это несжатые типы, такие как MEDIATYPE \_ Audio или MediaType \_ Video, хотя сжатые типы могут быть приняты, если они соответствуют профилю.</span><span class="sxs-lookup"><span data-stu-id="fe343-122">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="fe343-123">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="fe343-123">Input pin interfaces</span></span>   | <span data-ttu-id="fe343-124">**Ипин**, **имеминпутпин**, **иамстреамконфиг**, **IServiceProvider**, **иамвмбуфферпасс**, **IWMStreamConfig2** (через **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="fe343-124">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="fe343-125">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="fe343-125">Output pin media types</span></span> | <span data-ttu-id="fe343-126">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fe343-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="fe343-127">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="fe343-127">Output pin interfaces</span></span>  | <span data-ttu-id="fe343-128">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="fe343-128">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="fe343-129">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="fe343-129">Filter CLSID</span></span>           | <span data-ttu-id="fe343-130">\_ВМАСФВРИТЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="fe343-130">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="fe343-131">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="fe343-131">Property page CLSID</span></span>    | <span data-ttu-id="fe343-132">\_ВМАСФВРИТЕРПРОПЕРТИЕС CLSID</span><span class="sxs-lookup"><span data-stu-id="fe343-132">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="fe343-133">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="fe343-133">Executable</span></span>             | <span data-ttu-id="fe343-134">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="fe343-134">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="fe343-135">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="fe343-135">Merit</span></span>                  | <span data-ttu-id="fe343-136">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="fe343-136">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="fe343-137">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="fe343-137">Filter Category</span></span>        | <span data-ttu-id="fe343-138">Не указано</span><span class="sxs-lookup"><span data-stu-id="fe343-138">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="fe343-139">Remarks</span><span class="sxs-lookup"><span data-stu-id="fe343-139">Remarks</span></span>

<span data-ttu-id="fe343-140">Количество входных контактов фильтра зависит от профиля, который передается в фильтр.</span><span class="sxs-lookup"><span data-stu-id="fe343-140">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="fe343-141">Для каждого потока, определенного в профиле, создается один ПИН-код соответствующего типа носителя.</span><span class="sxs-lookup"><span data-stu-id="fe343-141">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="fe343-142">Входные сигналы поддерживают один метод из интерфейса **иамстреамконфиг** : **иамстреамконфиг::-Format**.</span><span class="sxs-lookup"><span data-stu-id="fe343-142">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="fe343-143">Все остальные методы возвращают E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="fe343-143">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="fe343-144">Вызовите метод **OnFormat** , чтобы запросить формат сжатия целевого объекта ПИН-кода, который определяется текущим профилем.</span><span class="sxs-lookup"><span data-stu-id="fe343-144">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="fe343-145">Чтобы задать профиль, используйте интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fe343-145">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="fe343-146">Интерфейс **IServiceProvider** фильтра позволяет приложениям получать интерфейс [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , который определен в пакете SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fe343-146">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="fe343-147">Интерфейс **IWMWriterAdvanced2** управляет дечередованием видео и полезен, если входные данные представляют собой [*чередующийся*](wmformat-glossary.md) источник, например DV (цифровое видео).</span><span class="sxs-lookup"><span data-stu-id="fe343-147">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="fe343-148">Используйте методы **жетинпутсеттинг** и **сетинпутсеттинг** для управления разчередованием.</span><span class="sxs-lookup"><span data-stu-id="fe343-148">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="fe343-149">Не рекомендуется, чтобы клиенты использовали другие методы этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fe343-149">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="fe343-150">Этот интерфейс можно получить только после добавления фильтра к графу фильтра.</span><span class="sxs-lookup"><span data-stu-id="fe343-150">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="fe343-151">В следующем примере показано, как запросить этот интерфейс:</span><span class="sxs-lookup"><span data-stu-id="fe343-151">The following example shows how to query for this interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fe343-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="fe343-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe343-153">**Справочник по КАСФ DirectShow**</span><span class="sxs-lookup"><span data-stu-id="fe343-153">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
