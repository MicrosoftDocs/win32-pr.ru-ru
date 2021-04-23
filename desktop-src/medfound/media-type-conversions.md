---
description: Преобразования типов мультимедиа
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Преобразования типов мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3a72e74439251f9661e0ff27166c504e47c238
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820309"
---
# <a name="media-type-conversions"></a><span data-ttu-id="d2b66-103">Преобразования типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d2b66-103">Media Type Conversions</span></span>

<span data-ttu-id="d2b66-104">Иногда требуется выполнить преобразование между Media Foundation типами носителей и более старыми структурами типов мультимедиа из DirectShow или пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d2b66-104">Occasionally it is necessary to convert between Media Foundation media types and the older media type structures from DirectShow or the Windows Media Format SDK.</span></span>

### <a name="from-a-format-structure-to-a-media-foundation-type"></a><span data-ttu-id="d2b66-105">Из структуры формата в тип Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2b66-105">From a Format Structure to a Media Foundation Type</span></span>

<span data-ttu-id="d2b66-106">Следующие функции инициализируют Media Foundation тип носителя из структуры формата.</span><span class="sxs-lookup"><span data-stu-id="d2b66-106">The following functions initialize a Media Foundation media type from a format structure.</span></span> <span data-ttu-id="d2b66-107">Эти функции также полезны, если поток данных или заголовок файла содержит структуру формата.</span><span class="sxs-lookup"><span data-stu-id="d2b66-107">These functions are also useful if a data stream or a file header contains a format structure.</span></span> <span data-ttu-id="d2b66-108">Например, заголовок файла для звуковых файлов звукозаписи содержит структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d2b66-108">For example, the file header for WAVE audio files contains a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2b66-109">Преобразуемая структура</span><span class="sxs-lookup"><span data-stu-id="d2b66-109">Structure to Convert</span></span></th>
<th><span data-ttu-id="d2b66-110">Функция</span><span class="sxs-lookup"><span data-stu-id="d2b66-110">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2b66-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="d2b66-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span></span><br/> <span data-ttu-id="d2b66-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (объекты мультимедиа DirectX)</span><span class="sxs-lookup"><span data-stu-id="d2b66-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX Media Objects)</span></span> <br/> <span data-ttu-id="d2b66-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (пакет SDK для формата Windows Media)</span><span class="sxs-lookup"><span data-stu-id="d2b66-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK)</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2b66-114">Эти структуры эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="d2b66-114">These structures are equivalent.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="d2b66-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>мфинитмедиатипефромаммедиатипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2b66-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>битмапинфохеадер</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="d2b66-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>мфкреатевидеомедиатипефромбитмапинфохеадерекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2b66-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>мфвидеоформат</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="d2b66-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>мфинитмедиатипефроммфвидеоформат</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2b66-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="d2b66-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2b66-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="d2b66-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2b66-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span></span></td>
<td><span data-ttu-id="d2b66-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2b66-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>видеоинфохеадер</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="d2b66-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>мфинитмедиатипефромвидеоинфохеадер</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2b66-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>Вавеформатекс</strong></a> или <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>вавеформатекстенсибле</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> or <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"><strong>WAVEFORMATEXTENSIBLE</strong></a></span></span></td>
<td><span data-ttu-id="d2b66-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>мфинитмедиатипефромвавеформатекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2b66-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a><span data-ttu-id="d2b66-130">Из типа Media Foundation в структуру формата</span><span class="sxs-lookup"><span data-stu-id="d2b66-130">From a Media Foundation Type to a Format Structure</span></span>

<span data-ttu-id="d2b66-131">Следующие функции создают или инициализируют структуру формата на основе типа носителя Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d2b66-131">The following functions create or initialize a format structure from a Media Foundation media type.</span></span>



| <span data-ttu-id="d2b66-132">Функция</span><span class="sxs-lookup"><span data-stu-id="d2b66-132">Function</span></span>                                                                             | <span data-ttu-id="d2b66-133">Целевая структура</span><span class="sxs-lookup"><span data-stu-id="d2b66-133">Target Structure</span></span>                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2b66-134">**Имфмедиатипе::, представляющее**</span><span class="sxs-lookup"><span data-stu-id="d2b66-134">**IMFMediaType::GetRepresentation**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | <span data-ttu-id="d2b66-135">[**AM \_ \_Тип носителя**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**мфвидеоформат**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)или [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="d2b66-135">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span></span> |
| [<span data-ttu-id="d2b66-136">**мфкреатеаммедиатипефроммфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d2b66-136">**MFCreateAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [<span data-ttu-id="d2b66-137">**\_тип носителя \_ AM**</span><span class="sxs-lookup"><span data-stu-id="d2b66-137">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [<span data-ttu-id="d2b66-138">**мфкреатемфвидеоформатфроммфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d2b66-138">**MFCreateMFVideoFormatFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [<span data-ttu-id="d2b66-139">**мфвидеоформат**</span><span class="sxs-lookup"><span data-stu-id="d2b66-139">**MFVIDEOFORMAT**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [<span data-ttu-id="d2b66-140">**мфкреатевавеформатексфроммфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d2b66-140">**MFCreateWaveFormatExFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | <span data-ttu-id="d2b66-141">[**Вавеформатекс**](/previous-versions/dd757713(v=vs.85)) или [ **вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2b66-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span></span>                                                                                    |
| [<span data-ttu-id="d2b66-142">**мфинитаммедиатипефроммфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d2b66-142">**MFInitAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [<span data-ttu-id="d2b66-143">**\_тип носителя \_ AM**</span><span class="sxs-lookup"><span data-stu-id="d2b66-143">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a><span data-ttu-id="d2b66-144">Сопоставления формата</span><span class="sxs-lookup"><span data-stu-id="d2b66-144">Format Mappings</span></span>

<span data-ttu-id="d2b66-145">В следующих таблицах перечислены Media Foundation атрибуты, соответствующие различным структурам формата.</span><span class="sxs-lookup"><span data-stu-id="d2b66-145">The following tables list the Media Foundation attributes that correspond to various format structures.</span></span> <span data-ttu-id="d2b66-146">Не все эти атрибуты можно перевести напрямую.</span><span class="sxs-lookup"><span data-stu-id="d2b66-146">Not all of these attributes can be translated directly.</span></span> <span data-ttu-id="d2b66-147">Для выполнения преобразований следует использовать функции, перечисленные в предыдущем разделе. Эти таблицы предоставляются главным образом для справки.</span><span class="sxs-lookup"><span data-stu-id="d2b66-147">To perform conversions, you should use the functions listed in the previous section; these tables are provided mainly for reference.</span></span>

### <a name="am_media_type"></a><span data-ttu-id="d2b66-148">\_тип носителя \_ AM</span><span class="sxs-lookup"><span data-stu-id="d2b66-148">AM\_MEDIA\_TYPE</span></span>



| <span data-ttu-id="d2b66-149">Член</span><span class="sxs-lookup"><span data-stu-id="d2b66-149">Member</span></span>                   | <span data-ttu-id="d2b66-150">attribute</span><span class="sxs-lookup"><span data-stu-id="d2b66-150">Attribute</span></span>                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b66-151">**бтемпоралкомпрессион**</span><span class="sxs-lookup"><span data-stu-id="d2b66-151">**bTemporalCompression**</span></span> | [<span data-ttu-id="d2b66-152">**MF \_ — \_ все \_ \_ независимые примеры**</span><span class="sxs-lookup"><span data-stu-id="d2b66-152">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) |
| <span data-ttu-id="d2b66-153">**бфикседсизесамплес**</span><span class="sxs-lookup"><span data-stu-id="d2b66-153">**bFixedSizeSamples**</span></span>    | [<span data-ttu-id="d2b66-154">**\_ \_ примеры фиксированного \_ размера MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-154">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)           |
| <span data-ttu-id="d2b66-155">**лсамплесизе**</span><span class="sxs-lookup"><span data-stu-id="d2b66-155">**lSampleSize**</span></span>          | [<span data-ttu-id="d2b66-156">**\_ \_ Размер образца MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="d2b66-156">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a><span data-ttu-id="d2b66-157">ВАВЕФОРМАТЕКС, ВАВЕФОРМАТЕКСТЕНСИБЛЕ</span><span class="sxs-lookup"><span data-stu-id="d2b66-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span></span>



| <span data-ttu-id="d2b66-158">Член</span><span class="sxs-lookup"><span data-stu-id="d2b66-158">Member</span></span>                  | <span data-ttu-id="d2b66-159">attribute</span><span class="sxs-lookup"><span data-stu-id="d2b66-159">Attribute</span></span>                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b66-160">**вформаттаг**</span><span class="sxs-lookup"><span data-stu-id="d2b66-160">**wFormatTag**</span></span>          | [<span data-ttu-id="d2b66-161">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-161">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)<br/> <span data-ttu-id="d2b66-162">Если **вформаттаг** имеет \_ \_ расширяемый формат Wave, подтип находится в элементе **подформата** .</span><span class="sxs-lookup"><span data-stu-id="d2b66-162">If **wFormatTag** is WAVE\_FORMAT\_EXTENSIBLE, the subtype is found in the **SubFormat** member.</span></span><br/> |
| <span data-ttu-id="d2b66-163">**нчаннелс**</span><span class="sxs-lookup"><span data-stu-id="d2b66-163">**nChannels**</span></span>           | [<span data-ttu-id="d2b66-164">**\_ \_ каналы аудиосигнала MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-164">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| <span data-ttu-id="d2b66-165">**нсамплесперсек**</span><span class="sxs-lookup"><span data-stu-id="d2b66-165">**nSamplesPerSec**</span></span>      | [<span data-ttu-id="d2b66-166">**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="d2b66-166">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| <span data-ttu-id="d2b66-167">**навгбитесперсек**</span><span class="sxs-lookup"><span data-stu-id="d2b66-167">**nAvgBytesPerSec**</span></span>     | [<span data-ttu-id="d2b66-168">**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**</span><span class="sxs-lookup"><span data-stu-id="d2b66-168">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| <span data-ttu-id="d2b66-169">**нблоккалигн**</span><span class="sxs-lookup"><span data-stu-id="d2b66-169">**nBlockAlign**</span></span>         | [<span data-ttu-id="d2b66-170">**\_ \_ Выравнивание звукового \_ блока MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-170">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| <span data-ttu-id="d2b66-171">**вбитсперсампле**</span><span class="sxs-lookup"><span data-stu-id="d2b66-171">**wBitsPerSample**</span></span>      | [<span data-ttu-id="d2b66-172">**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**</span><span class="sxs-lookup"><span data-stu-id="d2b66-172">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| <span data-ttu-id="d2b66-173">**ввалидбитсперсампле**</span><span class="sxs-lookup"><span data-stu-id="d2b66-173">**wValidBitsPerSample**</span></span> | [<span data-ttu-id="d2b66-174">**\_ \_ \_ допустимый бит для звука MF MT \_ \_ на \_ выборку**</span><span class="sxs-lookup"><span data-stu-id="d2b66-174">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| <span data-ttu-id="d2b66-175">**всамплесперблокк**</span><span class="sxs-lookup"><span data-stu-id="d2b66-175">**wSamplesPerBlock**</span></span>    | [<span data-ttu-id="d2b66-176">**\_ \_ звуковые образцы MF MT \_ \_ на \_ блок**</span><span class="sxs-lookup"><span data-stu-id="d2b66-176">**MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK**</span></span>](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| <span data-ttu-id="d2b66-177">**двчаннелмаск**</span><span class="sxs-lookup"><span data-stu-id="d2b66-177">**dwChannelMask**</span></span>       | [<span data-ttu-id="d2b66-178">**\_ \_ \_ Маска канала MF MT \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d2b66-178">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| <span data-ttu-id="d2b66-179">**Подформат**</span><span class="sxs-lookup"><span data-stu-id="d2b66-179">**SubFormat**</span></span>           | [<span data-ttu-id="d2b66-180">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-180">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                                                                                                        |
| <span data-ttu-id="d2b66-181">Дополнительные данные</span><span class="sxs-lookup"><span data-stu-id="d2b66-181">Extra data</span></span>              | [<span data-ttu-id="d2b66-182">**\_ \_ данные пользователя MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="d2b66-182">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a><span data-ttu-id="d2b66-183">ВИДЕОИНФОХЕАДЕР, VIDEOINFOHEADER2</span><span class="sxs-lookup"><span data-stu-id="d2b66-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span></span>



| <span data-ttu-id="d2b66-184">Член</span><span class="sxs-lookup"><span data-stu-id="d2b66-184">Member</span></span>                                         | <span data-ttu-id="d2b66-185">attribute</span><span class="sxs-lookup"><span data-stu-id="d2b66-185">Attribute</span></span>                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b66-186">**двбитрате**</span><span class="sxs-lookup"><span data-stu-id="d2b66-186">**dwBitRate**</span></span>                                  | [<span data-ttu-id="d2b66-187">**\_ \_ Средняя скорость MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="d2b66-187">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="d2b66-188">**двбитерроррате**</span><span class="sxs-lookup"><span data-stu-id="d2b66-188">**dwBitErrorRate**</span></span>                             | [<span data-ttu-id="d2b66-189">**\_ \_ \_ \_ Частота погрешностей средней разрядности MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-189">**MF\_MT\_AVG\_BIT\_ERROR\_RATE**</span></span>](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| <span data-ttu-id="d2b66-190">**авгтимеперфраме**</span><span class="sxs-lookup"><span data-stu-id="d2b66-190">**AvgTimePerFrame**</span></span>                            | <span data-ttu-id="d2b66-191">[**MF \_ \_ \_ Частота кадров MT**](mf-mt-frame-rate-attribute.md); для вычисления этого значения используйте [**мфаверажетимеперфраметофрамерате**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) .</span><span class="sxs-lookup"><span data-stu-id="d2b66-191">[**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) to calculate this value.</span></span>                                                                             |
| <span data-ttu-id="d2b66-192">**двинтерлацефлагс**</span><span class="sxs-lookup"><span data-stu-id="d2b66-192">**dwInterlaceFlags**</span></span>                           | [<span data-ttu-id="d2b66-193">**\_ \_ режим чересстрочную РАЗВЕРТКи MF \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-193">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| <span data-ttu-id="d2b66-194">**двкопипротектфлагс**</span><span class="sxs-lookup"><span data-stu-id="d2b66-194">**dwCopyProtectFlags**</span></span>                         | <span data-ttu-id="d2b66-195">Нет определенного эквивалента</span><span class="sxs-lookup"><span data-stu-id="d2b66-195">No defined equivalent</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="d2b66-196">**двпиктаспектратиокс**, **двпиктаспектратиой**</span><span class="sxs-lookup"><span data-stu-id="d2b66-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span></span> | <span data-ttu-id="d2b66-197">[**MF \_ Пропорции в \_ 1 – пиксельное \_ \_ соотношение**](mf-mt-pixel-aspect-ratio-attribute.md); необходимо преобразовать пропорции изображения в пропорции рисунка.</span><span class="sxs-lookup"><span data-stu-id="d2b66-197">[**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md); must convert from picture aspect ratio to picture aspect ratio.</span></span>                                                                                                      |
| <span data-ttu-id="d2b66-198">**двконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="d2b66-198">**dwControlFlags**</span></span>                             | <span data-ttu-id="d2b66-199">[**MF \_ \_ \_ \_ Флаги элемента управления "MT Pad**](mf-mt-pad-control-flags-attribute.md)".</span><span class="sxs-lookup"><span data-stu-id="d2b66-199">[**MF\_MT\_PAD\_CONTROL\_FLAGS**](mf-mt-pad-control-flags-attribute.md).</span></span> <span data-ttu-id="d2b66-200">Если установлен флаг **амконтрол \_ колоринфо present ( \_ присутствие** ), задайте атрибуты расширенного цвета, описанные в разделе [Расширенные сведения о цвете](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="d2b66-200">If the **AMCONTROL\_COLORINFO\_PRESENT** flag is present, set the extended color attributes described in [Extended Color Information](extended-color-information.md).</span></span> |
| <span data-ttu-id="d2b66-201">**бмихеадер. бивидс**, **бмихеадер. бихеигхт**</span><span class="sxs-lookup"><span data-stu-id="d2b66-201">**bmiHeader.biWidth**, **bmiHeader.biHeight**</span></span>  | [<span data-ttu-id="d2b66-202">**\_ \_ Размер пакета MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="d2b66-202">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| <span data-ttu-id="d2b66-203">**Бмихеадер. Бибиткаунт**</span><span class="sxs-lookup"><span data-stu-id="d2b66-203">**bmiHeader.biBitCount**</span></span>                       | <span data-ttu-id="d2b66-204">Неявный в подтипе ([**MF \_ MT, \_ подтип**](mf-mt-subtype-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="d2b66-204">Implicit in the subtype ([**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md)).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="d2b66-205">**Бмихеадер. Бикомпрессион**</span><span class="sxs-lookup"><span data-stu-id="d2b66-205">**bmiHeader.biCompression**</span></span>                    | <span data-ttu-id="d2b66-206">Неявный в подтипе.</span><span class="sxs-lookup"><span data-stu-id="d2b66-206">Implicit in the subtype.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="d2b66-207">**Бмихеадер. Бисизеимаже**</span><span class="sxs-lookup"><span data-stu-id="d2b66-207">**bmiHeader.biSizeImage**</span></span>                      | [<span data-ttu-id="d2b66-208">**\_ \_ Размер образца MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="d2b66-208">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="d2b66-209">Сведения о палитре</span><span class="sxs-lookup"><span data-stu-id="d2b66-209">Palette information</span></span>                            | [<span data-ttu-id="d2b66-210">**\_ \_ Палитра MF MT**</span><span class="sxs-lookup"><span data-stu-id="d2b66-210">**MF\_MT\_PALETTE**</span></span>](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

<span data-ttu-id="d2b66-211">Следующие атрибуты могут выводиться из структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) или [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , но также требуются некоторые знания о формате.</span><span class="sxs-lookup"><span data-stu-id="d2b66-211">The following attributes can be inferred from the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure but also require some knowledge of the format details.</span></span> <span data-ttu-id="d2b66-212">Например, различные форматы YUV имеют разные требования к STRIDE.</span><span class="sxs-lookup"><span data-stu-id="d2b66-212">For example, different YUV formats have different stride requirements.</span></span>

-   [<span data-ttu-id="d2b66-213">**MF \_ , \_ шаг по умолчанию \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-213">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)
-   [<span data-ttu-id="d2b66-214">**\_ \_ Минимальный \_ \_ Апертура экрана MF MT**</span><span class="sxs-lookup"><span data-stu-id="d2b66-214">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="d2b66-215">**\_ \_ \_ Апертура для поиска MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-215">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a><span data-ttu-id="d2b66-216">MPEG1VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="d2b66-216">MPEG1VIDEOINFO</span></span>



| <span data-ttu-id="d2b66-217">Член</span><span class="sxs-lookup"><span data-stu-id="d2b66-217">Member</span></span>                                   | <span data-ttu-id="d2b66-218">attribute</span><span class="sxs-lookup"><span data-stu-id="d2b66-218">Attribute</span></span>                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d2b66-219">**двстарттимекоде**</span><span class="sxs-lookup"><span data-stu-id="d2b66-219">**dwStartTimeCode**</span></span>                      | [<span data-ttu-id="d2b66-220">**\_ \_ \_ \_ код времени начала MF MT \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="d2b66-220">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="d2b66-221">**бсекуенцехеадер**</span><span class="sxs-lookup"><span data-stu-id="d2b66-221">**bSequenceHeader**</span></span>                      | [<span data-ttu-id="d2b66-222">**\_ \_ \_ заголовок последовательного сервера MF MT MPEG \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-222">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="d2b66-223">**бикспелсперметер**, **бийпелсперметер**</span><span class="sxs-lookup"><span data-stu-id="d2b66-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span></span> | [<span data-ttu-id="d2b66-224">**пропорции MF \_ MT \_ пикселей \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-224">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a><span data-ttu-id="d2b66-225">MPEG2VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="d2b66-225">MPEG2VIDEOINFO</span></span>



| <span data-ttu-id="d2b66-226">Член</span><span class="sxs-lookup"><span data-stu-id="d2b66-226">Member</span></span>               | <span data-ttu-id="d2b66-227">attribute</span><span class="sxs-lookup"><span data-stu-id="d2b66-227">Attribute</span></span>                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d2b66-228">**двстарттимекоде**</span><span class="sxs-lookup"><span data-stu-id="d2b66-228">**dwStartTimeCode**</span></span>  | [<span data-ttu-id="d2b66-229">**\_ \_ \_ \_ код времени начала MF MT \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="d2b66-229">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="d2b66-230">**двсекуенцехеадер**</span><span class="sxs-lookup"><span data-stu-id="d2b66-230">**dwSequenceHeader**</span></span> | [<span data-ttu-id="d2b66-231">**\_ \_ \_ заголовок последовательного сервера MF MT MPEG \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-231">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="d2b66-232">**двпрофиле**</span><span class="sxs-lookup"><span data-stu-id="d2b66-232">**dwProfile**</span></span>        | [<span data-ttu-id="d2b66-233">**\_Профиль MF MT \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-233">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md)                 |
| <span data-ttu-id="d2b66-234">**двлевел**</span><span class="sxs-lookup"><span data-stu-id="d2b66-234">**dwLevel**</span></span>          | [<span data-ttu-id="d2b66-235">**\_Уровень MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-235">**MF\_MT\_MPEG2\_LEVEL**</span></span>](mf-mt-mpeg2-level-attribute.md)                     |
| <span data-ttu-id="d2b66-236">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d2b66-236">**dwFlags**</span></span>          | [<span data-ttu-id="d2b66-237">**\_ \_ Флаги MF MT MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="d2b66-237">**MF\_MT\_MPEG2\_FLAGS**</span></span>](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a><span data-ttu-id="d2b66-238">Примеры</span><span class="sxs-lookup"><span data-stu-id="d2b66-238">Examples</span></span>

<span data-ttu-id="d2b66-239">Следующий код заполняет структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) из типа видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="d2b66-239">The following code fills in a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure from a video media type.</span></span> <span data-ttu-id="d2b66-240">Обратите внимание, что при преобразовании теряются некоторые сведения о форматировании (чередование, частота кадров, Расширенные данные о цветах).</span><span class="sxs-lookup"><span data-stu-id="d2b66-240">Note that this conversions loses some of the format information (interlacing, frame rate, extended color data).</span></span> <span data-ttu-id="d2b66-241">Однако это может быть полезно при сохранении растрового изображения из видеокадра, например.</span><span class="sxs-lookup"><span data-stu-id="d2b66-241">However, it might be useful when saving a bitmap from a video frame, for example.</span></span>


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d2b66-242">См. также</span><span class="sxs-lookup"><span data-stu-id="d2b66-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2b66-243">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="d2b66-243">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
