---
description: Видеодекодер Media Foundation H. 264 — это Media Foundation преобразование, которое поддерживает декодирование базовых, основных и высококачественных профилей до уровня 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Декодер видео H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496794"
---
# <a name="h264-video-decoder"></a><span data-ttu-id="e0867-103">Декодер видео H. 264</span><span class="sxs-lookup"><span data-stu-id="e0867-103">H.264 Video Decoder</span></span>

<span data-ttu-id="e0867-104">Видеодекодер Media Foundation H. 264 — это [Media Foundation преобразование](media-foundation-transforms.md) , которое поддерживает декодирование базовых, основных и высококачественных профилей до уровня 5,1.</span><span class="sxs-lookup"><span data-stu-id="e0867-104">The Media Foundation H.264 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding of Baseline, Main, and High profiles, up to level 5.1.</span></span>

<span data-ttu-id="e0867-105">Декодер видео H. 264 предоставляет следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="e0867-105">The H.264 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="e0867-106">[**Икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) (поддерживается в Windows 8)</span><span class="sxs-lookup"><span data-stu-id="e0867-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="e0867-107">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="e0867-107">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="e0867-108">**имфкуалитядвисе**</span><span class="sxs-lookup"><span data-stu-id="e0867-108">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="e0867-109">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="e0867-109">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="e0867-110">**имфратеконтрол**</span><span class="sxs-lookup"><span data-stu-id="e0867-110">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="e0867-111">**имфратесуппорт**</span><span class="sxs-lookup"><span data-stu-id="e0867-111">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="e0867-112">**имфреалтимеклиент**</span><span class="sxs-lookup"><span data-stu-id="e0867-112">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="e0867-113">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="e0867-113">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="e0867-114">Чтобы создать экземпляр декодера, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="e0867-114">To create an instance of the decoder, do one of the following:</span></span>

-   <span data-ttu-id="e0867-115">Вызовите функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) или [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="e0867-115">Call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>
-   <span data-ttu-id="e0867-116">Вызов [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="e0867-116">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="e0867-117">Идентификатором CLSID для декодера является **CLSID \_ CMSH264DecoderMFT**, объявленный в вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="e0867-117">The CLSID for the decoder is **CLSID\_CMSH264DecoderMFT**, declared in wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="e0867-118">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="e0867-118">Input Types</span></span>

<span data-ttu-id="e0867-119">Входной тип должен содержать по крайней мере два следующих атрибута:</span><span class="sxs-lookup"><span data-stu-id="e0867-119">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="e0867-120">attribute</span><span class="sxs-lookup"><span data-stu-id="e0867-120">Attribute</span></span>                                                 | <span data-ttu-id="e0867-121">Описание</span><span class="sxs-lookup"><span data-stu-id="e0867-121">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0867-122">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="e0867-122">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="e0867-123">**\_Видео мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="e0867-123">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="e0867-124">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="e0867-124">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="e0867-125">[Мфвидеоформат \_ H264 Single bitrate](video-subtype-guids.md) или мфвидеоформат \_ H264 Single bitrate \_ ES</span><span class="sxs-lookup"><span data-stu-id="e0867-125">[MFVideoFormat\_H264](video-subtype-guids.md) or MFVideoFormat\_H264\_ES</span></span> |



 

<span data-ttu-id="e0867-126">Если тип входных данных содержит только эти два атрибута, декодер будет предлагать тип выхода по умолчанию, который выступает в качестве заполнителя.</span><span class="sxs-lookup"><span data-stu-id="e0867-126">If the input type contains only these two attributes, the decoder will offer a default output type, which acts as a placeholder.</span></span> <span data-ttu-id="e0867-127">Когда декодер получает достаточное количество входных образцов для создания выходного фрейма, он сигнализирует об изменении формата, возвращая значение **MF \_ E \_ Преобразование \_ потока \_ преобразования** из [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="e0867-127">When the decoder receives enough input samples to produce an output frame, it signals a format change by returning **MF\_E\_TRANSFORM\_STREAM\_CHANGE** from [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="e0867-128">Дополнительные сведения об обработке изменений формата см. в документации по **ProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="e0867-128">See the **ProcessOutput** documentation for details about handling format changes.</span></span>

<span data-ttu-id="e0867-129">Чтобы избежать первоначального изменения формата, укажите как можно больше информации в типе входных данных, в том числе:</span><span class="sxs-lookup"><span data-stu-id="e0867-129">To avoid an initial format change, provide as much information in the input type as possible, including:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0867-130">attribute</span><span class="sxs-lookup"><span data-stu-id="e0867-130">Attribute</span></span></th>
<th><span data-ttu-id="e0867-131">Описание</span><span class="sxs-lookup"><span data-stu-id="e0867-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0867-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0867-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="e0867-133">Частота кадров.</span><span class="sxs-lookup"><span data-stu-id="e0867-133">Frame rate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0867-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0867-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="e0867-135">Размеры рамки.</span><span class="sxs-lookup"><span data-stu-id="e0867-135">Frame dimensions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0867-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0867-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="e0867-137">Режим чередования.</span><span class="sxs-lookup"><span data-stu-id="e0867-137">Interlace mode.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0867-138">В видео H. 264 структура чересстрочную развертки может динамически изменяться, поэтому рекомендуемое значение этого атрибута — <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0867-138">In H.264 video, the interlace structure can change dynamically, so the recommended value of this attribute is <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span></span> <span data-ttu-id="e0867-139">Сведения о развертке в потоке простейшего видео имеют приоритет над типом носителя.</span><span class="sxs-lookup"><span data-stu-id="e0867-139">Interlace information in the video elementary stream takes precedence over the media type.</span></span> <span data-ttu-id="e0867-140">Дополнительные сведения см. в статье <a href="video-interlacing.md">чередование видео</a>.</span><span class="sxs-lookup"><span data-stu-id="e0867-140">For more information, see <a href="video-interlacing.md">Video Interlacing</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0867-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0867-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="e0867-142">Пропорция в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e0867-142">Pixel aspect ratio.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e0867-143">Входной тип должен быть задан перед типом выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e0867-143">The input type must be set before the output type.</span></span> <span data-ttu-id="e0867-144">Пока тип входных данных не задан, метод [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) кодировщика возвращает **\_ тип преобразования MF E \_ \_ \_ не \_ задан**.</span><span class="sxs-lookup"><span data-stu-id="e0867-144">Until the input type is set, the encoder's [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="e0867-145">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="e0867-145">Output Types</span></span>

<span data-ttu-id="e0867-146">Декодер поддерживает следующие выходные типы выходных данных:</span><span class="sxs-lookup"><span data-stu-id="e0867-146">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="e0867-147">**Мфвидеоформат \_ I420**</span><span class="sxs-lookup"><span data-stu-id="e0867-147">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="e0867-148">**Мфвидеоформат \_ ийув**</span><span class="sxs-lookup"><span data-stu-id="e0867-148">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="e0867-149">**Мфвидеоформат \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="e0867-149">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="e0867-150">**Мфвидеоформат \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="e0867-150">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="e0867-151">**Мфвидеоформат \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="e0867-151">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="e0867-152">Дополнительные сведения об этих подтипах см. в разделе [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e0867-152">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="e0867-153">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="e0867-153">Transform Attributes</span></span>

<span data-ttu-id="e0867-154">Декодер H. 264 реализует метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="e0867-154">The H.264 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="e0867-155">Приложения могут использовать этот метод для получения или установки следующих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e0867-155">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="e0867-156">attribute</span><span class="sxs-lookup"><span data-stu-id="e0867-156">Attribute</span></span>                                                                                       | <span data-ttu-id="e0867-157">Описание</span><span class="sxs-lookup"><span data-stu-id="e0867-157">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0867-158">КОДЕКАПИ \_ авдеквидеоакцелератион \_ H264 Single bitrate</span><span class="sxs-lookup"><span data-stu-id="e0867-158">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="e0867-159">Включает или отключает аппаратное ускорение.</span><span class="sxs-lookup"><span data-stu-id="e0867-159">Enables or disables hardware acceleration.</span></span>                                                 |
| [<span data-ttu-id="e0867-160">КОДЕКАПИ \_ авдеквидеосумбнаилженератионмоде</span><span class="sxs-lookup"><span data-stu-id="e0867-160">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="e0867-161">Включает или отключает режим формирования эскизов.</span><span class="sxs-lookup"><span data-stu-id="e0867-161">Enables or disables thumbnail generation mode.</span></span>                                             |
| [<span data-ttu-id="e0867-162">С \_ \_ поддержкой D3D \_ SA</span><span class="sxs-lookup"><span data-stu-id="e0867-162">MF\_SA\_D3D\_AWARE</span></span>](mf-sa-d3d-aware-attribute.md)                                             | <span data-ttu-id="e0867-163">Указывает, что декодер поддерживает ускорение видео DirectX (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="e0867-163">Indicates that the decoder supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="e0867-164">Рассматривать как доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e0867-164">Treat as read-only.</span></span> |



 

<span data-ttu-id="e0867-165">В Windows 8 декодер H. 264 также поддерживает следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="e0867-165">In Windows 8, the H.264 decoder also supports the following attributes.</span></span>



| <span data-ttu-id="e0867-166">attribute</span><span class="sxs-lookup"><span data-stu-id="e0867-166">Attribute</span></span>                                                                                                     | <span data-ttu-id="e0867-167">Описание</span><span class="sxs-lookup"><span data-stu-id="e0867-167">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0867-168">КОДЕКАПИ \_ авловлатенцимоде</span><span class="sxs-lookup"><span data-stu-id="e0867-168">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="e0867-169">Включает или отключает режим декодирования с низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="e0867-169">Enables or disables low-latency decoding mode.</span></span>                                                              |
| [<span data-ttu-id="e0867-170">КОДЕКАПИ \_ авдекнумворкерсреадс</span><span class="sxs-lookup"><span data-stu-id="e0867-170">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                                         | <span data-ttu-id="e0867-171">Задает число рабочих потоков, используемых декодером.</span><span class="sxs-lookup"><span data-stu-id="e0867-171">Sets the number of worker threads used by the decoder.</span></span>                                                      |
| [<span data-ttu-id="e0867-172">КОДЕКАПИ \_ авдеквидеомакскодедвидс</span><span class="sxs-lookup"><span data-stu-id="e0867-172">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)                                     | <span data-ttu-id="e0867-173">Задает максимальную ширину изображения, которую декодер будет принимать в качестве входного типа.</span><span class="sxs-lookup"><span data-stu-id="e0867-173">Sets the maximum picture width that the decoder will accept as an input type.</span></span>                               |
| [<span data-ttu-id="e0867-174">КОДЕКАПИ \_ авдеквидеомакскодедхеигхт</span><span class="sxs-lookup"><span data-stu-id="e0867-174">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)                                   | <span data-ttu-id="e0867-175">Задает максимальную высоту изображения, которую декодер будет принимать в качестве входного типа.</span><span class="sxs-lookup"><span data-stu-id="e0867-175">Sets the maximum picture height that the decoder will accept as an input type.</span></span>                              |
| [<span data-ttu-id="e0867-176">\_ \_ минимальное \_ \_ число образцов выходных данных SA MF \_</span><span class="sxs-lookup"><span data-stu-id="e0867-176">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                               | <span data-ttu-id="e0867-177">Указывает максимальное число выборок выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e0867-177">Specifies the maximum number of output samples.</span></span>                                                             |
| [<span data-ttu-id="e0867-178">\_декодер MFT \_ предоставляют \_ типы выходных данных \_ \_ в \_ собственном \_ порядке</span><span class="sxs-lookup"><span data-stu-id="e0867-178">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="e0867-179">Указывает, предоставляет ли декодер выходные типы ИЙУВ/I420 (подходящие для перекодирования) перед другими форматами.</span><span class="sxs-lookup"><span data-stu-id="e0867-179">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span> |



 

<span data-ttu-id="e0867-180">В Windows 8 декодер H. 264 поддерживает интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="e0867-180">In Windows 8, the H.264 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="e0867-181">Этот интерфейс предоставляет API алтернативате для установки следующих свойств кодека.</span><span class="sxs-lookup"><span data-stu-id="e0867-181">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="e0867-182">КОДЕКАПИ \_ авдеквидеомакскодедвидс</span><span class="sxs-lookup"><span data-stu-id="e0867-182">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="e0867-183">КОДЕКАПИ \_ авдеквидеоакцелератион \_ H264 Single bitrate</span><span class="sxs-lookup"><span data-stu-id="e0867-183">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)
-   [<span data-ttu-id="e0867-184">КОДЕКАПИ \_ авдеквидеомакскодедхеигхт</span><span class="sxs-lookup"><span data-stu-id="e0867-184">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)
-   [<span data-ttu-id="e0867-185">КОДЕКАПИ \_ авдеквидеомакскодедвидс</span><span class="sxs-lookup"><span data-stu-id="e0867-185">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="e0867-186">КОДЕКАПИ \_ авдеквидеосумбнаилженератионмоде</span><span class="sxs-lookup"><span data-stu-id="e0867-186">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a><span data-ttu-id="e0867-187">Ограничения формата</span><span class="sxs-lookup"><span data-stu-id="e0867-187">Format Constraints</span></span>

<span data-ttu-id="e0867-188">Декодер поддерживает следующие форматы:</span><span class="sxs-lookup"><span data-stu-id="e0867-188">The decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0867-189">Профили и уровни</span><span class="sxs-lookup"><span data-stu-id="e0867-189">Profiles/Levels</span></span></td>
<td><span data-ttu-id="e0867-190">Базовый, основной и высокий профили, вплоть до уровня 5,1.</span><span class="sxs-lookup"><span data-stu-id="e0867-190">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="e0867-191">(Дополнительные сведения см. в спецификации ITU-T H. 264.)</span><span class="sxs-lookup"><span data-stu-id="e0867-191">(See ITU-T H.264 specification for details.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0867-192">Форматы чрома</span><span class="sxs-lookup"><span data-stu-id="e0867-192">Chroma Formats</span></span></td>
<td><span data-ttu-id="e0867-193">4:2:0 чрома или монохромный</span><span class="sxs-lookup"><span data-stu-id="e0867-193">4:2:0 chroma or monochrome</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0867-194">Минимальное разрешение</span><span class="sxs-lookup"><span data-stu-id="e0867-194">Minimum Resolution</span></span></td>
<td><span data-ttu-id="e0867-195">48 × 48 пикселей</span><span class="sxs-lookup"><span data-stu-id="e0867-195">48 × 48 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0867-196">Максимальное разрешение</span><span class="sxs-lookup"><span data-stu-id="e0867-196">Maximum Resolution</span></span></td>
<td><span data-ttu-id="e0867-197">4096 × 2304 пикселей</span><span class="sxs-lookup"><span data-stu-id="e0867-197">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="e0867-198">Максимальное гарантированное разрешение для ускорения ДКСВА — 1920 × 1088 пикселей; при более высоком разрешении Декодирование выполняется с помощью ДКСВА, если оно поддерживается базовым оборудованием, в противном случае Декодирование выполняется с помощью программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e0867-198">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0867-199">В Windows 7 максимальное поддерживаемое разрешение составляет 1920 × 1088 пикселей как для программного обеспечения, так и для декодирования ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="e0867-199">In Windows 7, the maximum supported resolution is 1920 × 1088 pixels for both software and DXVA decoding.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0867-200">дксва</span><span class="sxs-lookup"><span data-stu-id="e0867-200">DXVA</span></span></td>
<td><span data-ttu-id="e0867-201">Декодер поддерживает ДКСВА версии 2, но не ДКСВА версии 1.</span><span class="sxs-lookup"><span data-stu-id="e0867-201">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="e0867-202">Декодирование ДКСВА поддерживается только для основных параметров, совместимых с базовым, главным и высоким профилями битстреамс.</span><span class="sxs-lookup"><span data-stu-id="e0867-202">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="e0867-203">(Базовые битстреамс, совместимые с main, определяются как <strong>profile_idc</strong>= 66 и <strong>constrained_set1_flag</strong>= 1.)</span><span class="sxs-lookup"><span data-stu-id="e0867-203">(Main-compatible Baseline bitstreams are defined as <strong>profile_idc</strong>=66 and <strong>constrained_set1_flag</strong>=1.)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e0867-204">Входные данные должны соответствовать приложению B из ISO/IEC 14496-10.</span><span class="sxs-lookup"><span data-stu-id="e0867-204">Input data must conform to Annex B of ISO/IEC 14496-10.</span></span> <span data-ttu-id="e0867-205">Данные должны включать начальные коды.</span><span class="sxs-lookup"><span data-stu-id="e0867-205">The data must include the start codes.</span></span> <span data-ttu-id="e0867-206">Декодер пропускает байты, пока не найдет допустимый набор параметров последовательности (SPS) и набор параметров изображения (PPS) в байтовом потоке.</span><span class="sxs-lookup"><span data-stu-id="e0867-206">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

<span data-ttu-id="e0867-207">Декодер не поддерживает технологию зернистой пленки.</span><span class="sxs-lookup"><span data-stu-id="e0867-207">The decoder does not support Film Grain Technology.</span></span>

> [!Note]  
> <span data-ttu-id="e0867-208">Предыдущая версия документации неправильно объявила, что декодер поддерживается в Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e0867-208">A previous version of the documentation incorrectly stated that the decoder is supported on Windows Server 2008 R2.</span></span>

 

<span data-ttu-id="e0867-209">Если установлено обновление платформы для Windows Vista, видеодекодер H. 264 доступен в Windows Vista, но доступен только в Windows Vista с помощью [средства чтения исходного кода](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="e0867-209">If Platform Update Supplement for Windows Vista is installed, the H.264 video decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0867-210">Требования</span><span class="sxs-lookup"><span data-stu-id="e0867-210">Requirements</span></span>



| <span data-ttu-id="e0867-211">Требование</span><span class="sxs-lookup"><span data-stu-id="e0867-211">Requirement</span></span> | <span data-ttu-id="e0867-212">Значение</span><span class="sxs-lookup"><span data-stu-id="e0867-212">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0867-213">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0867-213">Minimum supported client</span></span><br/> | <span data-ttu-id="e0867-214">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e0867-214">Windows 7 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e0867-215">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0867-215">Minimum supported server</span></span><br/> | <span data-ttu-id="e0867-216">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e0867-216">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="e0867-217">DLL</span><span class="sxs-lookup"><span data-stu-id="e0867-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0867-218"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0867-218"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0867-219">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0867-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0867-220">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="e0867-220">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="e0867-221">Поддержка MPEG-4 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0867-221">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e0867-222">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0867-222">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e0867-223">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="e0867-223">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
