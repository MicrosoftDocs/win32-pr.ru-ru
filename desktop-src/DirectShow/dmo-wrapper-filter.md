---
description: Фильтр оболочки DMO
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: Фильтр оболочки DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29c5b86bdff4a215ec2ef5854d09a1f842dbf0e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908632"
---
# <a name="dmo-wrapper-filter"></a><span data-ttu-id="5cfe0-103">Фильтр оболочки DMO</span><span class="sxs-lookup"><span data-stu-id="5cfe0-103">DMO Wrapper Filter</span></span>

<span data-ttu-id="5cfe0-104">Фильтр оболочки DMO позволяет приложению DirectShow использовать [объект мультимедиа DirectX](directx-media-objects.md) (DMO) в графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-104">The DMO Wrapper filter enables a DirectShow application to use a [DirectX Media Object](directx-media-objects.md) (DMO) within a filter graph.</span></span> <span data-ttu-id="5cfe0-105">Фильтр создает оболочку DMO и обрабатывает все детали использования DMO, например передачу данных в DMO и обратно.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-105">The filter wraps the DMO and handles all the details of using the DMO, such as passing data to and from the DMO.</span></span> <span data-ttu-id="5cfe0-106">Кроме того, фильтр объединяет DMO, поэтому приложение может запросить фильтр для любых COM-интерфейсов, предоставляемых DMO.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-106">Also, the filter aggregates the DMO, so the application can query the filter for any COM interfaces that the DMO exposes.</span></span>



| <span data-ttu-id="5cfe0-107">Метка</span><span class="sxs-lookup"><span data-stu-id="5cfe0-107">Label</span></span> | <span data-ttu-id="5cfe0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5cfe0-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfe0-109">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="5cfe0-109">Filter Interfaces</span></span>                        | <span data-ttu-id="5cfe0-110">[**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**идмоврапперфилтер**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)</span><span class="sxs-lookup"><span data-stu-id="5cfe0-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)</span></span>                                                                                                                       |
| <span data-ttu-id="5cfe0-111">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="5cfe0-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="5cfe0-112">См. примечания</span><span class="sxs-lookup"><span data-stu-id="5cfe0-112">See Remarks</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="5cfe0-113">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="5cfe0-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="5cfe0-114">[**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5cfe0-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="5cfe0-115">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="5cfe0-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="5cfe0-116">См. примечания</span><span class="sxs-lookup"><span data-stu-id="5cfe0-116">See Remarks</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="5cfe0-117">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="5cfe0-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="5cfe0-118">[**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5cfe0-118">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="5cfe0-119">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="5cfe0-119">Filter CLSID</span></span>                             | <span data-ttu-id="5cfe0-120">\_ДМОВРАППЕРФИЛТЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="5cfe0-120">CLSID\_DMOWrapperFilter</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="5cfe0-121">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="5cfe0-121">Property Page CLSID</span></span>                      | <span data-ttu-id="5cfe0-122">Нет страницы свойств</span><span class="sxs-lookup"><span data-stu-id="5cfe0-122">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="5cfe0-123">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="5cfe0-123">Executable</span></span>                               | <span data-ttu-id="5cfe0-124">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="5cfe0-124">Qasf.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="5cfe0-125">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="5cfe0-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="5cfe0-126">См. примечания</span><span class="sxs-lookup"><span data-stu-id="5cfe0-126">See Remarks</span></span>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="5cfe0-127">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="5cfe0-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="5cfe0-128">См. примечания</span><span class="sxs-lookup"><span data-stu-id="5cfe0-128">See Remarks</span></span>                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="5cfe0-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cfe0-129">Remarks</span></span>

### <a name="limitations"></a><span data-ttu-id="5cfe0-130">Ограничения</span><span class="sxs-lookup"><span data-stu-id="5cfe0-130">Limitations</span></span>

<span data-ttu-id="5cfe0-131">Оболочка DMO имеет следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-131">The DMO Wrapper has the following limitations:</span></span>

-   <span data-ttu-id="5cfe0-132">Он не поддерживает дмос с нулевым числом входов, несколькими входами или нулевыми выходами.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-132">It does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span> <span data-ttu-id="5cfe0-133">(Он поддерживает дмос с одним входом и несколькими выходами.)</span><span class="sxs-lookup"><span data-stu-id="5cfe0-133">(It does support DMOs with one input and multiple outputs.)</span></span>
-   <span data-ttu-id="5cfe0-134">Он не поддерживает пользовательские транспорты.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-134">It does not support custom transports.</span></span> <span data-ttu-id="5cfe0-135">Все данные транспортного уровня выполняются через интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="5cfe0-135">All data transport is done through the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="5cfe0-136">Он не использует интерфейс **имедиаобжектинплаце** ; все операции обработки выполняются с помощью методов [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="5cfe0-136">It does not use the **IMediaObjectInPlace** interface; all processing is done using [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) methods.</span></span>

### <a name="pins"></a><span data-ttu-id="5cfe0-137">Маркеры</span><span class="sxs-lookup"><span data-stu-id="5cfe0-137">Pins</span></span>

<span data-ttu-id="5cfe0-138">Для каждого входного потока в DMO фильтр создает соответствующий входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-138">For each input stream on the DMO, the filter creates a corresponding input pin.</span></span> <span data-ttu-id="5cfe0-139">Для каждого выходного потока создается соответствующий выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-139">For each output stream, it creates a corresponding output pin.</span></span> <span data-ttu-id="5cfe0-140">Типы носителей, поддерживаемые каждым ПИН-кодом, зависят от DMO</span><span class="sxs-lookup"><span data-stu-id="5cfe0-140">The media types that each pin supports depends on the DMO</span></span>

### <a name="encoder-interfaces"></a><span data-ttu-id="5cfe0-141">Интерфейсы кодировщика</span><span class="sxs-lookup"><span data-stu-id="5cfe0-141">Encoder Interfaces</span></span>

<span data-ttu-id="5cfe0-142">Если DMO является видеокодировщиком или звуковым кодировщиком, закрепление вывода предоставляет интерфейс [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="5cfe0-142">If the DMO is a video encoder or an audio encoder, the output pin exposes the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span> <span data-ttu-id="5cfe0-143">Если DMO является видеокодировщиком, закрепление вывода также предоставляет интерфейс [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="5cfe0-143">If the DMO is a video encoder, the output pin also exposes the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="5cfe0-144">В обоих случаях, если DMO поддерживает интерфейс, ПИН-код делегирует объект DMO.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-144">In both cases, if the DMO supports the interface, the pin delegates to the DMO.</span></span> <span data-ttu-id="5cfe0-145">В противном случае ПИН-код предоставляет собственную реализацию.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-145">Otherwise, the pin provides its own implementation.</span></span>

### <a name="streaming"></a><span data-ttu-id="5cfe0-146">Потоковая передача</span><span class="sxs-lookup"><span data-stu-id="5cfe0-146">Streaming</span></span>

<span data-ttu-id="5cfe0-147">Фильтр использует интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) для управления всей потоковой передачей.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-147">The filter uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface to handle all streaming.</span></span> <span data-ttu-id="5cfe0-148">Он не поддерживает подключения [**иасинкреадер**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="5cfe0-148">It does not support [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connections.</span></span> <span data-ttu-id="5cfe0-149">Фильтр вызывает [**имедиаобжект::P роцессаутпут**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) на DMO только при получении данных из вышестоящего (включая уведомления в виде конца потока).</span><span class="sxs-lookup"><span data-stu-id="5cfe0-149">The filter calls [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) on the DMO only when it receives data from upstream (including end-of-stream notifications).</span></span> <span data-ttu-id="5cfe0-150">Поэтому он не поддерживает дмос с нулевым числом входных потоков.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-150">Therefore, it does not support DMOs with zero input streams.</span></span>

### <a name="seeking"></a><span data-ttu-id="5cfe0-151">Нужна</span><span class="sxs-lookup"><span data-stu-id="5cfe0-151">Seeking</span></span>

<span data-ttu-id="5cfe0-152">Все запросы поиска передаются в вышестоящий фильтр через первый входной ПИН-код в оболочке DMO.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-152">All seek requests are passed to the upstream filter, through the first input pin on the DMO Wrapper.</span></span> <span data-ttu-id="5cfe0-153">Для дмос нескольких выходных данных это означает, что вышестоящий фильтр может получить несколько запросов поиска при поиске приложением графа.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-153">For multiple-output DMOs, this means that the upstream filter might receive multiple seek requests when the application seeks the graph.</span></span>

### <a name="merit"></a><span data-ttu-id="5cfe0-154">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="5cfe0-154">Merit</span></span>

<span data-ttu-id="5cfe0-155">DirectShow назначает всем дмос значение по умолчанию «неполный **» + « \_** 0x800».</span><span class="sxs-lookup"><span data-stu-id="5cfe0-155">DirectShow assigns all DMOs a default merit value of **MERIT\_NORMAL** + 0x800.</span></span> <span data-ttu-id="5cfe0-156">Это значение находится между **\_ нормальным** и **\_ невысоким приоритетом**.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-156">This value falls between **MERIT\_NORMAL** and **MERIT\_PREFERRED**.</span></span> <span data-ttu-id="5cfe0-157">Фильтры декодера обычно имеют значение " **\_ нормально**".</span><span class="sxs-lookup"><span data-stu-id="5cfe0-157">Decoder filters generally have a merit value of **MERIT\_NORMAL**.</span></span> <span data-ttu-id="5cfe0-158">Таким образом, диспетчер графов фильтров обычно выбирает декодер DMO для фильтра декодера.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-158">Therefore, the filter graph manager will usually select a DMO decoder over a decoder filter.</span></span> <span data-ttu-id="5cfe0-159">Чтобы переопределить значение по умолчанию, добавьте запись реестра в раздел реестра DMO в \_ \_ корневом CLSID классов hKey \\ .</span><span class="sxs-lookup"><span data-stu-id="5cfe0-159">To override the default merit value, add a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="5cfe0-160">Включите значение **DWORD** с именем «заслуживает», значение которого указывает на неуспешный выбор.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-160">Include a **DWORD** value named "Merit" whose value specifies the merit.</span></span>

### <a name="category"></a><span data-ttu-id="5cfe0-161">Категория</span><span class="sxs-lookup"><span data-stu-id="5cfe0-161">Category</span></span>

<span data-ttu-id="5cfe0-162">Фильтр оболочки DMO не отображается ни в одной категории.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-162">The DMO Wrapper filter does not appear by itself in any category.</span></span> <span data-ttu-id="5cfe0-163">При создании оболочки DMO она отображается в категории DirectShow, соответствующей категории DMO, под именем DMO.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-163">When it wraps a DMO, it appears in the DirectShow category that corresponds to the DMO's category, under the name of the DMO.</span></span>

### <a name="buffers"></a><span data-ttu-id="5cfe0-164">Буферы</span><span class="sxs-lookup"><span data-stu-id="5cfe0-164">Buffers</span></span>

<span data-ttu-id="5cfe0-165">Фильтр оболочки DMO передает буферы мультимедиа в DMO, которые предоставляют интерфейс [**имедиабуффер**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="5cfe0-165">The DMO Wrapper filter passes media buffers to the DMO which expose the [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) interface.</span></span>

<span data-ttu-id="5cfe0-166">В Windows Vista и более поздних версиях буферы мультимедиа также предоставляют интерфейс IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-166">In Windows Vista or later, the media buffers also expose the IServiceProvider interface.</span></span> <span data-ttu-id="5cfe0-167">DMO может использовать этот интерфейс для получения указателя на пример носителя, связанного с буфером.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-167">The DMO can use this interface to get a pointer to the media sample that is associated with the buffer.</span></span> <span data-ttu-id="5cfe0-168">Используйте идентификатор службы **IID \_ имедиасампле**.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-168">Use the service identifier **IID\_IMediaSample**.</span></span> <span data-ttu-id="5cfe0-169">Видео DMO может использовать интерфейс [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) примера мультимедиа для установки флагов чересстрочную развертки в образце.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-169">A video DMO can use the media sample's [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface to set interlace flags on the sample.</span></span> <span data-ttu-id="5cfe0-170">В следующем коде показано, как получить указатель на пример мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="5cfe0-170">The following code shows how to get the pointer to the media sample:</span></span>


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



<span data-ttu-id="5cfe0-171">Дополнительные сведения о параметрах чересстрочную развертки для каждого образца см. в разделе [**\_ SAMPLE2 \_ Properties Structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).</span><span class="sxs-lookup"><span data-stu-id="5cfe0-171">For more information about per-sample interlace flags, see [**AM\_SAMPLE2\_PROPERTIES Structure**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).</span></span>

### <a name="quality-control"></a><span data-ttu-id="5cfe0-172">Контроль качества</span><span class="sxs-lookup"><span data-stu-id="5cfe0-172">Quality Control</span></span>

<span data-ttu-id="5cfe0-173">Если объекты DMO предоставляют интерфейс [**идмокуалитиконтрол**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) , то фильтр преобразует вызовы [**Икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) для своего выходного контакта в [**идмокуалитиконтрол:: сетнов**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) вызовы в DMO.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-173">If the DMO exposes the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) interface, the filter translates [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) calls on its output pin into [**IDMOQualityControl::SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) calls on the DMO.</span></span> <span data-ttu-id="5cfe0-174">Параметр *ртнов* объекта **сетнов** вычисляется как сумма **метки времени** и **последних** элементов структуры [**качества**](/windows/win32/api/strmif/ns-strmif-quality) .</span><span class="sxs-lookup"><span data-stu-id="5cfe0-174">The *rtNow* parameter of **SetNow** is calculated as the sum of the **TimeStamp** and **Late** members of the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span>

### <a name="using-the-fiter-in-graphedit"></a><span data-ttu-id="5cfe0-175">Использование фильтровать в Графедит</span><span class="sxs-lookup"><span data-stu-id="5cfe0-175">Using the Fiter in GraphEdit</span></span>

<span data-ttu-id="5cfe0-176">В Графедит фильтр оболочки DMO не отображается под собственным именем.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-176">In GraphEdit, the DMO Wrapper filter does not appear under its own name.</span></span> <span data-ttu-id="5cfe0-177">Вместо этого каждый зарегистрированный объект DMO отображается под соответствующей категорией фильтра.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-177">Instead, each registered DMO is listed under the appropriate filter category.</span></span> <span data-ttu-id="5cfe0-178">При добавлении DMO с помощью диалогового окна " **Вставить фильтры** " графедит создает фильтр оболочки DMO и настраивает его для использования этого DMO.</span><span class="sxs-lookup"><span data-stu-id="5cfe0-178">When you add a DMO through the **Insert Filters** dialog, GraphEdit creates the DMO Wrapper filter and configures it to use that DMO.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cfe0-179">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5cfe0-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cfe0-180">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="5cfe0-180">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="5cfe0-181">Объекты мультимедиа DirectX</span><span class="sxs-lookup"><span data-stu-id="5cfe0-181">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 
