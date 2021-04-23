---
description: Расширенный фильтр модуля подготовки видео (Евр) является 16-канальным видеомикшером и модулем подготовки отчетов. Она имеет те же основные функции и модель подключаемых модулей, что и Media Foundation приемника мультимедиа Евр.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Расширенный фильтр визуализатора видео
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072230"
---
# <a name="enhanced-video-renderer-filter"></a><span data-ttu-id="4675d-104">Расширенный фильтр визуализатора видео</span><span class="sxs-lookup"><span data-stu-id="4675d-104">Enhanced Video Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="4675d-105">Этот раздел относится к Windows Vista и более поздним версиям.</span><span class="sxs-lookup"><span data-stu-id="4675d-105">This topic applies to Windows Vista and later.</span></span>

 

<span data-ttu-id="4675d-106">Расширенный фильтр модуля подготовки видео (Евр) является 16-канальным видеомикшером и модулем подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="4675d-106">The Enhanced Video Renderer (EVR) filter is a 16-channel video mixer and renderer.</span></span> <span data-ttu-id="4675d-107">Она имеет те же основные функции и модель подключаемых модулей, что и Media Foundation приемника мультимедиа Евр.</span><span class="sxs-lookup"><span data-stu-id="4675d-107">It has the same core functionality and plug-in model as the Media Foundation EVR media sink.</span></span>

<span data-ttu-id="4675d-108">Фильтр Евр для DirectShow описан в документации по пакету SDK для Media Foundation. Дополнительные сведения см. в разделе [Улучшенный обработчик видео](../medfound/enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="4675d-108">The DirectShow EVR filter is documented in the Media Foundation SDK documentation; for more information, see [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4675d-109">Фильтровать интерфейсы (с помощью <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="4675d-109">Filter Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="4675d-110">Интерфейсы DirectShow:</span><span class="sxs-lookup"><span data-stu-id="4675d-110">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="4675d-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>иамцертифиедаутпутпротектион</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="4675d-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>иамфилтермискфлагс</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="4675d-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="4675d-114"><a href="ikspropertyset.md"><strong>икспропертисет</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="4675d-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>имедиаевентсинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span></span></li>
<li><span data-ttu-id="4675d-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="4675d-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="4675d-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>икуалпроп</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
</ul>
<span data-ttu-id="4675d-119">Media Foundation интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="4675d-119">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="4675d-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>иеврфилтерконфиг</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="4675d-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>имфжетсервице</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
<li><span data-ttu-id="4675d-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>имфвидеопоситионмаппер</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span></span></li>
<li><span data-ttu-id="4675d-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>имфвидеорендерер</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4675d-124">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="4675d-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="4675d-125">Переменная в зависимости от графического драйвера.</span><span class="sxs-lookup"><span data-stu-id="4675d-125">Variable, depending on the graphics driver.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4675d-126">Интерфейсы входных закрепления (через <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="4675d-126">Input Pin Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="4675d-127">Интерфейсы DirectShow:</span><span class="sxs-lookup"><span data-stu-id="4675d-127">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="4675d-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="4675d-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="4675d-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="4675d-131">Media Foundation интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="4675d-131">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="4675d-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>идиректксвидеомемориконфигуратион</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span></span></li>
<li><span data-ttu-id="4675d-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>иеврвидеостреамконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span></span></li>
<li><span data-ttu-id="4675d-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>имфжетсервице</strong></a></span><span class="sxs-lookup"><span data-stu-id="4675d-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4675d-135">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="4675d-135">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="4675d-136">Не применяется</span><span class="sxs-lookup"><span data-stu-id="4675d-136">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4675d-137">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="4675d-137">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="4675d-138">Не применяется</span><span class="sxs-lookup"><span data-stu-id="4675d-138">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4675d-139">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="4675d-139">Filter CLSID</span></span></td>
<td><span data-ttu-id="4675d-140">CLSID_EnhancedVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="4675d-140">CLSID_EnhancedVideoRenderer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4675d-141">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="4675d-141">Executable</span></span></td>
<td><span data-ttu-id="4675d-142">evr.dll</span><span class="sxs-lookup"><span data-stu-id="4675d-142">evr.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4675d-143"><a href="merit.md">Заслуживают</a></span><span class="sxs-lookup"><span data-stu-id="4675d-143"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="4675d-144">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="4675d-144">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4675d-145"><a href="filter-categories.md">Категория фильтра</a></span><span class="sxs-lookup"><span data-stu-id="4675d-145"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="4675d-146">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="4675d-146">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="4675d-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4675d-147">Remarks</span></span>

<span data-ttu-id="4675d-148">В дополнение к интерфейсам, предоставляемым через **QueryInterface**, ЕВР предоставляет другие интерфейсы через метод [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) .</span><span class="sxs-lookup"><span data-stu-id="4675d-148">In addition to the interfaces exposed through **QueryInterface**, the EVR exposes other interfaces through the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="4675d-149">Некоторые из этих интерфейсов реализуются средством Евр Presenter или Евр, а не Евр.</span><span class="sxs-lookup"><span data-stu-id="4675d-149">Some of these interfaces are implemented by the EVR presenter or the EVR mixer, rather than the EVR itself.</span></span> <span data-ttu-id="4675d-150">Если приложение устанавливает настраиваемый Presenter или микшер на евр, то пользовательские версии могут предоставлять другой набор интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="4675d-150">If the application sets a custom presenter or mixer on the EVR, the custom versions might expose a different set of interfaces.</span></span>



| <span data-ttu-id="4675d-151">Объект</span><span class="sxs-lookup"><span data-stu-id="4675d-151">Object</span></span>     | <span data-ttu-id="4675d-152">Идентификатор службы</span><span class="sxs-lookup"><span data-stu-id="4675d-152">Service Identifier</span></span>                                              | <span data-ttu-id="4675d-153">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="4675d-153">Interfaces</span></span>                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4675d-154">Фильтр Евр</span><span class="sxs-lookup"><span data-stu-id="4675d-154">EVR filter</span></span> | <span data-ttu-id="4675d-155">\_ \_ Служба прорисовки видео Mr \_ (запросы Евр или Presenter)</span><span class="sxs-lookup"><span data-stu-id="4675d-155">MR\_VIDEO\_RENDER\_SERVICE(Queries EVR or presenter)</span></span><br/> | [<span data-ttu-id="4675d-156">**имфвидеодевицеид**</span><span class="sxs-lookup"><span data-stu-id="4675d-156">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="4675d-157">**имфвидеодисплайконтрол**</span><span class="sxs-lookup"><span data-stu-id="4675d-157">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [<span data-ttu-id="4675d-158">**имфвидеопоситионмаппер**</span><span class="sxs-lookup"><span data-stu-id="4675d-158">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="4675d-159">**имфвидеопресентер**</span><span class="sxs-lookup"><span data-stu-id="4675d-159">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| <span data-ttu-id="4675d-160">Фильтр Евр</span><span class="sxs-lookup"><span data-stu-id="4675d-160">EVR filter</span></span> | <span data-ttu-id="4675d-161">\_ \_ Служба ускорения видео Mr \_ (выступающие запросы)</span><span class="sxs-lookup"><span data-stu-id="4675d-161">MR\_VIDEO\_ACCELERATION\_SERVICE(Queries presenter)</span></span><br/>  | [<span data-ttu-id="4675d-162">**IDirect3DDeviceManager9**</span><span class="sxs-lookup"><span data-stu-id="4675d-162">**IDirect3DDeviceManager9**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4675d-163">Фильтр Евр</span><span class="sxs-lookup"><span data-stu-id="4675d-163">EVR filter</span></span> | <span data-ttu-id="4675d-164">\_ \_ Служба видеомикшера MR \_ (микшер запросов)</span><span class="sxs-lookup"><span data-stu-id="4675d-164">MR\_VIDEO\_MIXER\_SERVICE(Queries mixer)</span></span><br/>             | [<span data-ttu-id="4675d-165">**имфвидеодевицеид**</span><span class="sxs-lookup"><span data-stu-id="4675d-165">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="4675d-166">**имфвидеомиксербитмап**</span><span class="sxs-lookup"><span data-stu-id="4675d-166">**IMFVideoMixerBitmap**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [<span data-ttu-id="4675d-167">**имфвидеомиксерконтрол**</span><span class="sxs-lookup"><span data-stu-id="4675d-167">**IMFVideoMixerControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [<span data-ttu-id="4675d-168">**имфвидеопоситионмаппер**</span><span class="sxs-lookup"><span data-stu-id="4675d-168">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="4675d-169">**имфвидеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="4675d-169">**IMFVideoProcessor**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| <span data-ttu-id="4675d-170">Входные контакты</span><span class="sxs-lookup"><span data-stu-id="4675d-170">Input pins</span></span> | <span data-ttu-id="4675d-171">\_ \_ Служба ускорения видео Mr \_</span><span class="sxs-lookup"><span data-stu-id="4675d-171">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>                                | [<span data-ttu-id="4675d-172">**идиректксвидеомемориконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="4675d-172">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

<span data-ttu-id="4675d-173">Евр может сочетать до 16 потоков видео.</span><span class="sxs-lookup"><span data-stu-id="4675d-173">The EVR can mix up to 16 video streams.</span></span> <span data-ttu-id="4675d-174">Первый входной поток (ПИН-код 0) называется *ссылочным потоком*.</span><span class="sxs-lookup"><span data-stu-id="4675d-174">The first input stream (pin 0) is called the *reference stream*.</span></span> <span data-ttu-id="4675d-175">Ссылочный поток всегда отображается первым в z-порядке.</span><span class="sxs-lookup"><span data-stu-id="4675d-175">The reference stream always appears first in the z-order.</span></span> <span data-ttu-id="4675d-176">Любые дополнительные потоки называются подпотоками и смешиваются поверх потока ссылок.</span><span class="sxs-lookup"><span data-stu-id="4675d-176">Any additional streams are called substreams, and are mixed on top of the reference stream.</span></span> <span data-ttu-id="4675d-177">Приложение может изменить z-порядок для подпотоков, но ни один из подпотоков не может быть первым в z-порядке.</span><span class="sxs-lookup"><span data-stu-id="4675d-177">The application can change the z-order of the substreams, but no substream can be first in the z-order.</span></span>

<span data-ttu-id="4675d-178">Графический драйвер определяет поддерживаемые форматы видео, но обычно они ограничены следующими элементами:</span><span class="sxs-lookup"><span data-stu-id="4675d-178">The graphics driver determines which video formats are supported, but typically they are limited to the following:</span></span>

-   <span data-ttu-id="4675d-179">Ссылочный поток: прогрессивное или чередование YUV без альфа-составляющей для каждого пикселя (например, NV12 или YUY2); или прогрессивный RGB.</span><span class="sxs-lookup"><span data-stu-id="4675d-179">Reference stream: Progressive or interlaced YUV with no per-pixel alpha (such as NV12 or YUY2); or progressive RGB.</span></span>
-   <span data-ttu-id="4675d-180">Подпотоки: прогрессивное YUV с поддержкой отдельных пикселей, например АЙУВ или AI44.</span><span class="sxs-lookup"><span data-stu-id="4675d-180">Substreams: Progressive YUV with per-pixel-alpha, such as AYUV or AI44.</span></span>

<span data-ttu-id="4675d-181">Доступные форматы подпотока могут зависеть от формата потока ссылок.</span><span class="sxs-lookup"><span data-stu-id="4675d-181">The available substream formats might depend on the format of the reference stream.</span></span>

<span data-ttu-id="4675d-182">Евр пересылает команды Seek через ПИН-код 0.</span><span class="sxs-lookup"><span data-stu-id="4675d-182">The EVR forwards seek commands upstream through pin 0.</span></span> <span data-ttu-id="4675d-183">ПИН-коды подпотока не выполняют команд прямого поиска.</span><span class="sxs-lookup"><span data-stu-id="4675d-183">The substream pins do not forward seek commands.</span></span> <span data-ttu-id="4675d-184">С помощью фильтра источника или разделителя можно синхронизировать подпотоки со ссылочным потоком.</span><span class="sxs-lookup"><span data-stu-id="4675d-184">It is the responsibility of the source or splitter filter to keep the substreams synchronized with the reference stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="4675d-185">Требования</span><span class="sxs-lookup"><span data-stu-id="4675d-185">Requirements</span></span>



| <span data-ttu-id="4675d-186">Требование</span><span class="sxs-lookup"><span data-stu-id="4675d-186">Requirement</span></span> | <span data-ttu-id="4675d-187">Значение</span><span class="sxs-lookup"><span data-stu-id="4675d-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4675d-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4675d-188">Minimum supported client</span></span><br/> | <span data-ttu-id="4675d-189">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4675d-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4675d-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4675d-190">Minimum supported server</span></span><br/> | <span data-ttu-id="4675d-191">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4675d-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4675d-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4675d-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4675d-193">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="4675d-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

