---
description: Декодер видео Media Foundation H. 265 — это Media Foundation преобразование, которое поддерживает декодирование содержимого H. 265/HEVC в формате приложение б и может использоваться при воспроизведении файлов MP4 и M2TS.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Декодер видео H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543623"
---
# <a name="h265--hevc-video-decoder"></a><span data-ttu-id="36396-103">Декодер видео H. 265/HEVC</span><span class="sxs-lookup"><span data-stu-id="36396-103">H.265 / HEVC Video Decoder</span></span>

<span data-ttu-id="36396-104">Декодер видео Media Foundation H. 265 — это [Media Foundation преобразование](media-foundation-transforms.md) , которое поддерживает декодирование содержимого H. 265/HEVC в формате приложение б и может использоваться при воспроизведении файлов MP4 и M2TS.</span><span class="sxs-lookup"><span data-stu-id="36396-104">The Media Foundation H.265 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding H.265/HEVC content in Annex B format and can be used in playback of mp4 and m2ts files.</span></span>

<span data-ttu-id="36396-105">Декодер видео H. 265 предоставляет следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="36396-105">The H.265 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="36396-106">[**Икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) (поддерживается в Windows 8)</span><span class="sxs-lookup"><span data-stu-id="36396-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="36396-107">**имфаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="36396-107">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="36396-108">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="36396-108">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="36396-109">**имфкуалитядвисе**</span><span class="sxs-lookup"><span data-stu-id="36396-109">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="36396-110">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="36396-110">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="36396-111">**имфратеконтрол**</span><span class="sxs-lookup"><span data-stu-id="36396-111">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="36396-112">**имфратесуппорт**</span><span class="sxs-lookup"><span data-stu-id="36396-112">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="36396-113">**имфреалтимеклиент**</span><span class="sxs-lookup"><span data-stu-id="36396-113">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="36396-114">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="36396-114">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="36396-115">Чтобы создать экземпляр декодера, вызовите функцию [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) или [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="36396-115">To create an instance of the decoder call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="input-types"></a><span data-ttu-id="36396-116">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="36396-116">Input Types</span></span>

<span data-ttu-id="36396-117">Входной тип должен содержать по крайней мере два следующих атрибута:</span><span class="sxs-lookup"><span data-stu-id="36396-117">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="36396-118">attribute</span><span class="sxs-lookup"><span data-stu-id="36396-118">Attribute</span></span>                                                 | <span data-ttu-id="36396-119">Описание</span><span class="sxs-lookup"><span data-stu-id="36396-119">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36396-120">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="36396-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="36396-121">**\_Видео мфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="36396-121">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="36396-122">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="36396-122">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="36396-123">[Мфвидеоформат \_ HEVC](video-subtype-guids.md) или мфвидеоформат \_ HEVC \_ ES</span><span class="sxs-lookup"><span data-stu-id="36396-123">[MFVideoFormat\_HEVC](video-subtype-guids.md) or MFVideoFormat\_HEVC\_ES</span></span> |



 

<span data-ttu-id="36396-124">Первый подтип носителя, Мфвидеоформат \_ HEVC, указывает, что образцы мультимедиа содержат H. 265 битовый поток с начальными кодами, а поток — с чередованием SPS/PPS.</span><span class="sxs-lookup"><span data-stu-id="36396-124">The first media subtype, MFVideoFormat\_HEVC, indicates that the media samples carry H.265 bitstream with start codes, and the stream has interleaved SPS/PPS.</span></span> <span data-ttu-id="36396-125">Предполагается наличие одного кадра на выборку.</span><span class="sxs-lookup"><span data-stu-id="36396-125">It assumes one frame per sample.</span></span>

<span data-ttu-id="36396-126">Подтип носителя Мфвидеоформат HEVC ES означает, что \_ \_ примеры мультимедиа содержат элементарное значение H. 265 битовый поток, где каждый пример может содержать частичное изображение, несколько изображений, некоторые рисунки и часть изображения.</span><span class="sxs-lookup"><span data-stu-id="36396-126">The media subtype MFVideoFormat\_ HEVC\_ES is to indicate the media samples carry elementary H.265 bitstream, where each sample may contain a partial picture, multiple pictures, some pictures plus a partial picture.</span></span>

<span data-ttu-id="36396-127">Входные типы носителей не могут динамически изменяться между двумя типами.</span><span class="sxs-lookup"><span data-stu-id="36396-127">The input media types cannot change dynamically between two types.</span></span> <span data-ttu-id="36396-128">Декодер может обнаруживать изменения в выходном формате на основе простейшего синтаксиса потока (пропорции, измерения, флаги развертки, сведения о колориметрие) и запускать соответствующие изменения типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="36396-128">The decoder can detect in-flight output format changes based on the elementary stream syntax (aspect ratio, dimension, interlace flags, colorimetry information) and trigger corresponding output media type changes.</span></span>

<span data-ttu-id="36396-129">Для входного типа мультимедиа декодер ожидает, что источник задает правильный профиль.</span><span class="sxs-lookup"><span data-stu-id="36396-129">For input media type, the decoder expects the source to set the correct Profile.</span></span> <span data-ttu-id="36396-130">Например, если содержимое будет 10 бит, тип носителя input должен указать профиль как Main10.</span><span class="sxs-lookup"><span data-stu-id="36396-130">For example if the content is going to be 10bit, input media type should specify the profile as Main10.</span></span>

## <a name="output-types"></a><span data-ttu-id="36396-131">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="36396-131">Output Types</span></span>

<span data-ttu-id="36396-132">Декодер поддерживает следующие выходные типы выходных данных:</span><span class="sxs-lookup"><span data-stu-id="36396-132">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="36396-133">**Мфвидеоформат \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="36396-133">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="36396-134">**Мфвидеоформат \_ P010**</span><span class="sxs-lookup"><span data-stu-id="36396-134">**MFVideoFormat\_P010**</span></span>

<span data-ttu-id="36396-135">Дополнительные сведения об этих подтипах см. в разделе [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="36396-135">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="36396-136">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="36396-136">Transform Attributes</span></span>

<span data-ttu-id="36396-137">Декодер H. 265 реализует метод [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="36396-137">The H.265 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="36396-138">Приложения могут использовать этот метод для получения или установки следующих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="36396-138">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="36396-139">attribute</span><span class="sxs-lookup"><span data-stu-id="36396-139">Attribute</span></span>                                                                                       | <span data-ttu-id="36396-140">Описание</span><span class="sxs-lookup"><span data-stu-id="36396-140">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36396-141">КОДЕКАПИ \_ авловлатенцимоде</span><span class="sxs-lookup"><span data-stu-id="36396-141">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                     | <span data-ttu-id="36396-142">Включает или отключает режим декодирования с низкой задержкой.</span><span class="sxs-lookup"><span data-stu-id="36396-142">Enables or disables low-latency decoding mode.</span></span>                                                                                |
| [<span data-ttu-id="36396-143">КОДЕКАПИ \_ авдекнумворкерсреадс</span><span class="sxs-lookup"><span data-stu-id="36396-143">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                           | <span data-ttu-id="36396-144">Задает число рабочих потоков, используемых декодером.</span><span class="sxs-lookup"><span data-stu-id="36396-144">Sets the number of worker threads used by the decoder.</span></span>                                                                        |
| [<span data-ttu-id="36396-145">КОДЕКАПИ \_ авдеквидеосумбнаилженератионмоде</span><span class="sxs-lookup"><span data-stu-id="36396-145">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="36396-146">Включает или отключает режим формирования эскизов.</span><span class="sxs-lookup"><span data-stu-id="36396-146">Enables or disables thumbnail generation mode.</span></span>                                                                                |
| [<span data-ttu-id="36396-147">\_ \_ задана длина налу MF \_</span><span class="sxs-lookup"><span data-stu-id="36396-147">MF\_NALU\_LENGTH\_SET</span></span>](mf-nalu-length-set.md)                                                 | <span data-ttu-id="36396-148">Указывает, что сведения о длине налу будут отправляться в виде большого двоичного объекта в каждом сжатом образце H. 265.</span><span class="sxs-lookup"><span data-stu-id="36396-148">Indicates that NALU length information will be sent as a BLOB with each compressed H.265 sample.</span></span>                              |
| [<span data-ttu-id="36396-149">\_ \_ сведения о длине MF налу \_</span><span class="sxs-lookup"><span data-stu-id="36396-149">MF\_NALU\_LENGTH\_INFORMATION</span></span>](mf-nalu-length-information.md)                                 | <span data-ttu-id="36396-150">Указывает длину Налус в образце.</span><span class="sxs-lookup"><span data-stu-id="36396-150">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="36396-151">Это большой двоичный объект MF, заданный в сжатых примерах входных данных для декодера H. 265.</span><span class="sxs-lookup"><span data-stu-id="36396-151">This is a MF BLOB that is set on compressed input samples to the H.265 decoder.</span></span> |
| [<span data-ttu-id="36396-152">\_ \_ минимальное \_ \_ число образцов выходных данных SA MF \_</span><span class="sxs-lookup"><span data-stu-id="36396-152">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                 | <span data-ttu-id="36396-153">Указывает максимальное число выборок выходных данных.</span><span class="sxs-lookup"><span data-stu-id="36396-153">Specifies the maximum number of output samples.</span></span>                                                                               |



 

<span data-ttu-id="36396-154">Декодер H. 265 поддерживает интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="36396-154">The H.265 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="36396-155">Этот интерфейс предоставляет API алтернативате для установки следующих свойств кодека.</span><span class="sxs-lookup"><span data-stu-id="36396-155">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="36396-156">КОДЕКАПИ \_ авдекнумворкерсреадс</span><span class="sxs-lookup"><span data-stu-id="36396-156">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)
-   [<span data-ttu-id="36396-157">КОДЕКАПИ \_ авдеквидеосумбнаилженератионмоде</span><span class="sxs-lookup"><span data-stu-id="36396-157">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="36396-158">КОДЕКАПИ \_ авловлатенцимоде</span><span class="sxs-lookup"><span data-stu-id="36396-158">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a><span data-ttu-id="36396-159">Ограничения формата</span><span class="sxs-lookup"><span data-stu-id="36396-159">Format Constraints</span></span>

<span data-ttu-id="36396-160">Декодер поддерживает следующие форматы:</span><span class="sxs-lookup"><span data-stu-id="36396-160">The decoder supports the following formats:</span></span>



| <span data-ttu-id="36396-161">Требование</span><span class="sxs-lookup"><span data-stu-id="36396-161">Requirement</span></span> | <span data-ttu-id="36396-162">Значение</span><span class="sxs-lookup"><span data-stu-id="36396-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36396-163">Профили и уровни</span><span class="sxs-lookup"><span data-stu-id="36396-163">Profiles/Levels</span></span>    | <span data-ttu-id="36396-164">Main, Главная по-прежнему рисунок и профили Main10</span><span class="sxs-lookup"><span data-stu-id="36396-164">Main, Main Still Picture, and Main10 profiles</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="36396-165">Форматы чрома</span><span class="sxs-lookup"><span data-stu-id="36396-165">Chroma Formats</span></span>     | <span data-ttu-id="36396-166">4:2:0 чрома</span><span class="sxs-lookup"><span data-stu-id="36396-166">4:2:0 chroma</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="36396-167">Минимальное разрешение</span><span class="sxs-lookup"><span data-stu-id="36396-167">Minimum Resolution</span></span> | <span data-ttu-id="36396-168">48 × 48 пикселей</span><span class="sxs-lookup"><span data-stu-id="36396-168">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="36396-169">Максимальное разрешение</span><span class="sxs-lookup"><span data-stu-id="36396-169">Maximum Resolution</span></span> | <span data-ttu-id="36396-170">4096 × 2304 пикселей</span><span class="sxs-lookup"><span data-stu-id="36396-170">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="36396-171">Максимальное гарантированное разрешение для ускорения ДКСВА — 1920 × 1088 пикселей; при более высоком разрешении Декодирование выполняется с помощью ДКСВА, если оно поддерживается базовым оборудованием, в противном случае Декодирование выполняется с помощью программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="36396-171">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/> |
| <span data-ttu-id="36396-172">дксва</span><span class="sxs-lookup"><span data-stu-id="36396-172">DXVA</span></span>               | <span data-ttu-id="36396-173">Декодер поддерживает DX11 и DX12 ДКСВА, но не ДКСВА версии 2 или ДКСВА версии 1.</span><span class="sxs-lookup"><span data-stu-id="36396-173">The decoder supports DX11 and DX12 DXVA, but not DXVA version 2 or DXVA version 1.</span></span>                                                                                                                                                                                                         |



 

<span data-ttu-id="36396-174">Входные данные должны соответствовать приложению B из ITU-T H. 265 \| ISO/IEC 23008-2.</span><span class="sxs-lookup"><span data-stu-id="36396-174">Input data must conform to Annex B of ITU-T H.265 \| ISO/IEC 23008-2.</span></span> <span data-ttu-id="36396-175">Данные должны включать начальные коды.</span><span class="sxs-lookup"><span data-stu-id="36396-175">The data must include the start codes.</span></span> <span data-ttu-id="36396-176">Декодер пропускает байты, пока не найдет допустимый набор параметров последовательности (SPS) и набор параметров изображения (PPS) в байтовом потоке.</span><span class="sxs-lookup"><span data-stu-id="36396-176">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="36396-177">Требования</span><span class="sxs-lookup"><span data-stu-id="36396-177">Requirements</span></span>



| <span data-ttu-id="36396-178">Требование</span><span class="sxs-lookup"><span data-stu-id="36396-178">Requirement</span></span> | <span data-ttu-id="36396-179">Значение</span><span class="sxs-lookup"><span data-stu-id="36396-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="36396-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36396-180">Minimum supported client</span></span><br/> | <span data-ttu-id="36396-181">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="36396-181">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="36396-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36396-182">Minimum supported server</span></span><br/> | <span data-ttu-id="36396-183">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="36396-183">None supported</span></span><br/>                                                                |
| <span data-ttu-id="36396-184">DLL</span><span class="sxs-lookup"><span data-stu-id="36396-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36396-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36396-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36396-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36396-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36396-187">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="36396-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
