---
description: Этот фильтр декодирует видео MPEG-1, MPEG-2, H. 264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Видеодекодер Microsoft MPEG-2 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416512"
---
# <a name="microsoft-mpeg-2-video-decoder"></a><span data-ttu-id="bbc5a-103">Видеодекодер Microsoft MPEG-2 видео</span><span class="sxs-lookup"><span data-stu-id="bbc5a-103">Microsoft MPEG-2 Video Decoder</span></span>

<span data-ttu-id="bbc5a-104">Этот фильтр декодирует видео MPEG-1, MPEG-2, H. 264.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-104">This filter decodes MPEG-1, MPEG-2, H.264 video.</span></span>

> [!Note]  
> <span data-ttu-id="bbc5a-105">Для декодирования видео H. 264 требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-105">Decoding of H.264 video requires Windows 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bbc5a-106">Этот фильтр не поддерживается на платформах на базе IA-64.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-106">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="bbc5a-107">В реестре понятное имя этого фильтра — «Microsoft ДТВ-DVD Video декодер».</span><span class="sxs-lookup"><span data-stu-id="bbc5a-107">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Video Decoder".</span></span>



<span data-ttu-id="bbc5a-108">Сведения о фильтре</span><span class="sxs-lookup"><span data-stu-id="bbc5a-108">Filter Information</span></span>

<span data-ttu-id="bbc5a-109">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="bbc5a-109">Filter Interfaces</span></span>

[<span data-ttu-id="bbc5a-110">**иамдекодеркапс**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-110">**IAMDecoderCaps**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [<span data-ttu-id="bbc5a-111">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="bbc5a-112">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-112">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="bbc5a-113">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="bbc5a-113">Input Pin Media Types</span></span>

<span data-ttu-id="bbc5a-114">ПИН-код входного видео:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-114">Video input pin:</span></span>

-   <span data-ttu-id="bbc5a-115">МУЛЬТИМЕДИА \_ - \_ зашифрованный \_ пакет MEDIATYPE \_ , \_ видео медиасубтипе MPEG2</span><span class="sxs-lookup"><span data-stu-id="bbc5a-115">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="bbc5a-116">\_Формат MEDIATYPE MPEG2 \_ PES, \_ видео медиасубтипе MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="bbc5a-116">MEDIATYPE\_MPEG2\_PES, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="bbc5a-117">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="bbc5a-117">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Packet</span></span>
-   <span data-ttu-id="bbc5a-118">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="bbc5a-118">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Payload</span></span>
-   <span data-ttu-id="bbc5a-119">\_Видео MEDIATYPE, \_ видео медиасубтипе MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="bbc5a-119">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>

<span data-ttu-id="bbc5a-120">ПИН-код входных данных субтитров:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-120">Subpicture input pin:</span></span><br/>

-   <span data-ttu-id="bbc5a-121">\_диск MEDIATYPE \_ , зашифрованный с DVD-диска \_ , медиасубтипе \_ DVD \_</span><span class="sxs-lookup"><span data-stu-id="bbc5a-121">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_DVD\_SUBPICTURE</span></span>

<span data-ttu-id="bbc5a-122">Начиная с Windows 7, ПИН-код ввода видео также поддерживает следующие типы входных данных:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-122">Starting in Windows 7, the video input pin also supports the following input types:</span></span><br/>

-   <span data-ttu-id="bbc5a-123">**MEDIATYPE \_ Видео**, **медиасубтипе \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-123">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_AVC1**</span></span>
-   <span data-ttu-id="bbc5a-124">**MEDIATYPE \_ Видео**, **медиасубтипе \_ H264 Single bitrate**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-124">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_H264**</span></span>
-   <span data-ttu-id="bbc5a-125">**MEDIATYPE \_ Видео**, **медиасубтипе \_ H264 Single bitrate**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-125">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_h264**</span></span>
-   <span data-ttu-id="bbc5a-126">**MEDIATYPE \_ Видео**, **медиасубтипе \_ X264**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-126">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_X264**</span></span>
-   <span data-ttu-id="bbc5a-127">**MEDIATYPE \_ Видео**, **медиасубтипе \_ x264**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-127">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_x264**</span></span>

<span data-ttu-id="bbc5a-128">Дополнительные сведения см. в разделе [типы видео H. 264](h-264-video-types.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc5a-128">See [H.264 Video Types](h-264-video-types.md) for more information.</span></span> <span data-ttu-id="bbc5a-129">Тип входного носителя может динамически изменяться между типами MPEG2 и H. 264.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-129">The input media type can change dynamically between MPEG2 and H.264 types.</span></span><br/>

<span data-ttu-id="bbc5a-130">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="bbc5a-130">Input Pin Interfaces</span></span>

[<span data-ttu-id="bbc5a-131">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-131">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="bbc5a-132">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-132">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="bbc5a-133">**имеминпутпин**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-133">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="bbc5a-134">**имфсамплепротектион**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-134">**IMFSampleProtection**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [<span data-ttu-id="bbc5a-135">**ипин**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-135">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="bbc5a-136">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-136">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="bbc5a-137">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="bbc5a-137">Output Pin Media Types</span></span>

<span data-ttu-id="bbc5a-138">ПИН-код вывода видео:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-138">Video output pin:</span></span>

-   <span data-ttu-id="bbc5a-139">МУЛЬТИМЕДИЙное \_ видео, дксва \_ ModeMPEG2 \_ A (дксва 1,0)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-139">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_A (DXVA 1.0)</span></span>
-   <span data-ttu-id="bbc5a-140">МУЛЬТИМЕДИЙное \_ видео, дксва \_ ModeMPEG2 \_ C (дксва 1,0)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-140">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_C (DXVA 1.0)</span></span>
-   <span data-ttu-id="bbc5a-141">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ I420 (программный декодирование или дксва 2.0)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-141">MEDIATYPE\_Video, MEDIASUBTYPE\_I420 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="bbc5a-142">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ NV12 (программный декодирование или дксва 2.0)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-142">MEDIATYPE\_Video, MEDIASUBTYPE\_NV12 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="bbc5a-143">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ YUY2 (программный декодирование или дксва 2.0)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-143">MEDIATYPE\_Video, MEDIASUBTYPE\_YUY2 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="bbc5a-144">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ IMC3 (только для дксва 2.0)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-144">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC3 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="bbc5a-145">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ IMC4 (только для дксва 2.0)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-145">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC4 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="bbc5a-146">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ S340 (только для дксва 2.0)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-146">MEDIATYPE\_Video, MEDIASUBTYPE\_S340 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="bbc5a-147">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ YV12 (только для дксва 2.0)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-147">MEDIATYPE\_Video, MEDIASUBTYPE\_YV12 (DXVA2.0 only)</span></span>

<span data-ttu-id="bbc5a-148">Выходной ПИН-код линии 21:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-148">Line-21 output pin:</span></span><br/>

-   <span data-ttu-id="bbc5a-149">MEDIATYPE \_ AUXLine21Data, медиасубтипе \_ Line21 \_ гоппаккет</span><span class="sxs-lookup"><span data-stu-id="bbc5a-149">MEDIATYPE\_AUXLine21Data, MEDIASUBTYPE\_Line21\_GOPPacket</span></span>

<span data-ttu-id="bbc5a-150">Закрепление вывода субтитров:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-150">Subpicture output pin:</span></span><br/>

-   <span data-ttu-id="bbc5a-151">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ AI44</span><span class="sxs-lookup"><span data-stu-id="bbc5a-151">MEDIATYPE\_Video, MEDIASUBTYPE\_AI44</span></span>
-   <span data-ttu-id="bbc5a-152">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="bbc5a-152">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="bbc5a-153">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="bbc5a-153">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="bbc5a-154">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ айув</span><span class="sxs-lookup"><span data-stu-id="bbc5a-154">MEDIATYPE\_Video, MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="bbc5a-155">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="bbc5a-155">Output Pin Interfaces</span></span>

<span data-ttu-id="bbc5a-156">[**Иамвидеоакцелераторнотифи**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (только ПИН-код вывода видео)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (video output pin only)</span></span><br/> [<span data-ttu-id="bbc5a-157">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-157">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="bbc5a-158">**имедиасикинг**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-158">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="bbc5a-159">**ипин**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-159">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="bbc5a-160">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-160">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [<span data-ttu-id="bbc5a-161">**ивпконфиг**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-161">**IVPConfig**</span></span>](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

<span data-ttu-id="bbc5a-162">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="bbc5a-162">Filter CLSID</span></span>

<span data-ttu-id="bbc5a-163">**Идентификатор CLSID \_ CMPEG2VidDecoderDS** (определяется в вмкодекдсп. h)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-163">**CLSID\_CMPEG2VidDecoderDS** (defined in wmcodecdsp.h)</span></span>

<span data-ttu-id="bbc5a-164">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="bbc5a-164">Executable</span></span>

<span data-ttu-id="bbc5a-165">msmpeg2vdec.dll</span><span class="sxs-lookup"><span data-stu-id="bbc5a-165">msmpeg2vdec.dll</span></span>

[<span data-ttu-id="bbc5a-166">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="bbc5a-166">Merit</span></span>](merit.md)

<span data-ttu-id="bbc5a-167">**Неуспешный \_ Обычная** — 1</span><span class="sxs-lookup"><span data-stu-id="bbc5a-167">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="bbc5a-168">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="bbc5a-168">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="bbc5a-169">**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-169">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="bbc5a-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbc5a-170">Remarks</span></span>

<span data-ttu-id="bbc5a-171">Этот фильтр имеет два входа и три контакта вывода.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-171">This filter has two input pins and three output pins.</span></span>

<span data-ttu-id="bbc5a-172">ПИН-коды входа:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-172">Input pins:</span></span>

-   <span data-ttu-id="bbc5a-173">Видеовход</span><span class="sxs-lookup"><span data-stu-id="bbc5a-173">Video input</span></span>
-   <span data-ttu-id="bbc5a-174">Входные данные подизображения</span><span class="sxs-lookup"><span data-stu-id="bbc5a-174">Subpicture input</span></span>

<span data-ttu-id="bbc5a-175">Выходные сигналы:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-175">Output pins:</span></span>

-   <span data-ttu-id="bbc5a-176">Выходные данные видео</span><span class="sxs-lookup"><span data-stu-id="bbc5a-176">Video output</span></span>
-   <span data-ttu-id="bbc5a-177">Line-21 вывод</span><span class="sxs-lookup"><span data-stu-id="bbc5a-177">Line-21 output</span></span>
-   <span data-ttu-id="bbc5a-178">Выходные данные подизображения</span><span class="sxs-lookup"><span data-stu-id="bbc5a-178">Subpicture output</span></span>

<span data-ttu-id="bbc5a-179">Фильтр не создает выходного ПИН-кода субтитров, если только входной ПИН-код не подключен к типу носителя с **\_ \_ \_ зашифрованным DVD-диском MEDIATYPE** .</span><span class="sxs-lookup"><span data-stu-id="bbc5a-179">The filter does not create the subpicture output pin unless the video input pin is connected with a **MEDIATYPE\_DVD\_ENCRYPTED\_PACK** media type.</span></span>

### <a name="mpeg-12-support"></a><span data-ttu-id="bbc5a-180">Поддержка MPEG-1/2</span><span class="sxs-lookup"><span data-stu-id="bbc5a-180">MPEG-1/2 Support</span></span>

<span data-ttu-id="bbc5a-181">Для MPEG-1 и MPEG-2 декодер поддерживает следующие форматы:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-181">For MPEG-1 and MPEG-2, the decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbc5a-182">Профили и уровни</span><span class="sxs-lookup"><span data-stu-id="bbc5a-182">Profiles/Levels</span></span></td>
<td><span data-ttu-id="bbc5a-183">Любое сочетание следующих профилей и уровней:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-183">Any combination of the following profiles and levels:</span></span><br/>
<ul>
<li><span data-ttu-id="bbc5a-184">Профили: простой, основной</span><span class="sxs-lookup"><span data-stu-id="bbc5a-184">Profiles: Simple, Main</span></span></li>
<li><span data-ttu-id="bbc5a-185">Уровни: низкий, основной, высокий, высокий 1440</span><span class="sxs-lookup"><span data-stu-id="bbc5a-185">Levels: Low, Main, High, High 1440</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbc5a-186">Форматы чрома</span><span class="sxs-lookup"><span data-stu-id="bbc5a-186">Chroma Formats</span></span></td>
<td><span data-ttu-id="bbc5a-187">4:2:0 чрома</span><span class="sxs-lookup"><span data-stu-id="bbc5a-187">4:2:0 chroma</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbc5a-188">Максимальное разрешение</span><span class="sxs-lookup"><span data-stu-id="bbc5a-188">Maximum Resolution</span></span></td>
<td><span data-ttu-id="bbc5a-189">1920 × 1088 пикселей</span><span class="sxs-lookup"><span data-stu-id="bbc5a-189">1920 × 1088 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbc5a-190">дксва</span><span class="sxs-lookup"><span data-stu-id="bbc5a-190">DXVA</span></span></td>
<td><span data-ttu-id="bbc5a-191">Декодер поддерживает ускорение видео DirectX (ДКСВА) версии 1 и версии 2.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-191">The decoder supports DirectX Video Acceleration (DXVA) version 1 and version 2.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bbc5a-192">Декодер не поддерживает масштабируемые битстреамс.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-192">The decoder does not support scalable bitstreams.</span></span> <span data-ttu-id="bbc5a-193">Входные данные должны представлять собой простейший поток видео.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-193">The input must be an elementary video stream.</span></span>

<span data-ttu-id="bbc5a-194">Декодер не поддерживает форматы 4:2:2 чрома.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-194">The decoder does not support 4:2:2 chroma formats.</span></span>

### <a name="h264-support"></a><span data-ttu-id="bbc5a-195">Поддержка H. 264</span><span class="sxs-lookup"><span data-stu-id="bbc5a-195">H.264 Support</span></span>

<span data-ttu-id="bbc5a-196">Для H. 264 декодер поддерживает следующие форматы:</span><span class="sxs-lookup"><span data-stu-id="bbc5a-196">For H.264, the decoder supports the following formats:</span></span>



| <span data-ttu-id="bbc5a-197">Требование</span><span class="sxs-lookup"><span data-stu-id="bbc5a-197">Requirement</span></span> | <span data-ttu-id="bbc5a-198">Значение</span><span class="sxs-lookup"><span data-stu-id="bbc5a-198">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc5a-199">Профили и уровни</span><span class="sxs-lookup"><span data-stu-id="bbc5a-199">Profiles/Levels</span></span>    | <span data-ttu-id="bbc5a-200">Базовый, основной и высокий профили, вплоть до уровня 5,1.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-200">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="bbc5a-201">(Дополнительные сведения см. в спецификации ITU-T H. 264.)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-201">(See ITU-T H.264 specification for details.)</span></span>                                                                                                                                                                          |
| <span data-ttu-id="bbc5a-202">Форматы чрома</span><span class="sxs-lookup"><span data-stu-id="bbc5a-202">Chroma Formats</span></span>     | <span data-ttu-id="bbc5a-203">4:2:0 чрома или монохромный</span><span class="sxs-lookup"><span data-stu-id="bbc5a-203">4:2:0 chroma or monochrome</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="bbc5a-204">Минимальное разрешение</span><span class="sxs-lookup"><span data-stu-id="bbc5a-204">Minimum Resolution</span></span> | <span data-ttu-id="bbc5a-205">48 × 48 пикселей</span><span class="sxs-lookup"><span data-stu-id="bbc5a-205">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="bbc5a-206">Максимальное разрешение</span><span class="sxs-lookup"><span data-stu-id="bbc5a-206">Maximum Resolution</span></span> | <span data-ttu-id="bbc5a-207">1920 × 1088 пикселей</span><span class="sxs-lookup"><span data-stu-id="bbc5a-207">1920 × 1088 pixels</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="bbc5a-208">дксва</span><span class="sxs-lookup"><span data-stu-id="bbc5a-208">DXVA</span></span>               | <span data-ttu-id="bbc5a-209">Декодер поддерживает ДКСВА версии 2, но не ДКСВА версии 1.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-209">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="bbc5a-210">Декодирование ДКСВА поддерживается только для основных параметров, совместимых с базовым, главным и высоким профилями битстреамс.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-210">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="bbc5a-211">(Базовые битстреамс, совместимые с main, определяются как **профиль \_ idc**= 66 и **\_ \_ флаг ограниченных set1**= 1.)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-211">(Main-compatible Baseline bitstreams are defined as **profile\_idc**=66 and **constrained\_set1\_flag**=1.)</span></span> |



 

<span data-ttu-id="bbc5a-212">Декодер не поддерживает технологию зернистой пленки.</span><span class="sxs-lookup"><span data-stu-id="bbc5a-212">The decoder does not support Film Grain Technology.</span></span>

<span data-ttu-id="bbc5a-213">Дополнительные сведения о типах носителей H. 264 см. в разделе [типы видео h. 264](h-264-video-types.md).</span><span class="sxs-lookup"><span data-stu-id="bbc5a-213">For information about the H.264 media types, see [H.264 Video Types](h-264-video-types.md).</span></span>

### <a name="codec-properties"></a><span data-ttu-id="bbc5a-214">Свойства кодека</span><span class="sxs-lookup"><span data-stu-id="bbc5a-214">Codec Properties</span></span>

<span data-ttu-id="bbc5a-215">Входные контакты поддерживают следующие наборы свойств с помощью [**икспропертисет**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="bbc5a-215">The input pins support the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="bbc5a-216">**Набор свойств защиты копирования DVD-дисков**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-216">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="bbc5a-217">[**Набор свойств "подизображение DVD-диска**](dvd-subpicture-property-set.md) " (только для ПИН-кода подизображения)</span><span class="sxs-lookup"><span data-stu-id="bbc5a-217">[**DVD Subpicture Property Set**](dvd-subpicture-property-set.md) (subpicture pin only)</span></span>

<span data-ttu-id="bbc5a-218">Входные контакты поддерживают следующие свойства с помощью [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="bbc5a-218">The input pins support the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="bbc5a-219">Свойство</span><span class="sxs-lookup"><span data-stu-id="bbc5a-219">Property</span></span>                                                                  | <span data-ttu-id="bbc5a-220">Требуется</span><span class="sxs-lookup"><span data-stu-id="bbc5a-220">Requires</span></span>      |
|---------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="bbc5a-221">**авдеккоммонинпутформат**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md)         | <span data-ttu-id="bbc5a-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbc5a-222">Windows Vista</span></span> |
| [<span data-ttu-id="bbc5a-223">**авдеквидеоинпутскантипе**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-223">**AVDecVideoInputScanType**</span></span>](avdecvideoinputscantype-property.md)       | <span data-ttu-id="bbc5a-224">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbc5a-224">Windows Vista</span></span> |
| [<span data-ttu-id="bbc5a-225">**авдеквидеопикселаспектратио**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-225">**AVDecVideoPixelAspectRatio**</span></span>](avdecvideopixelaspectratio-property.md) | <span data-ttu-id="bbc5a-226">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbc5a-226">Windows Vista</span></span> |



 

<span data-ttu-id="bbc5a-227">Фильтр поддерживает следующие свойства с помощью [**икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="bbc5a-227">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="bbc5a-228">Свойство</span><span class="sxs-lookup"><span data-stu-id="bbc5a-228">Property</span></span>                                                                                | <span data-ttu-id="bbc5a-229">Требуется</span><span class="sxs-lookup"><span data-stu-id="bbc5a-229">Requires</span></span>      |
|-----------------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="bbc5a-230">**авдекммксскласс**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-230">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                          | <span data-ttu-id="bbc5a-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbc5a-231">Windows Vista</span></span> |
| [<span data-ttu-id="bbc5a-232">**Авдеквидеоакцелератион \_ H264 Single bitrate**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-232">**AVDecVideoAcceleration\_H264**</span></span>](avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="bbc5a-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbc5a-233">Windows 7</span></span>     |
| [<span data-ttu-id="bbc5a-234">**Авдеквидеоакцелератион \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-234">**AVDecVideoAcceleration\_MPEG2**</span></span>](avdecvideoacceleration-mpeg2-property.md)          | <span data-ttu-id="bbc5a-235">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbc5a-235">Windows 7</span></span>     |
| [<span data-ttu-id="bbc5a-236">**авдеквидеодроппиквисмиссингреф**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-236">**AVDecVideoDropPicWithMissingRef**</span></span>](avdecvideodroppicwithmissingref-property.md)     | <span data-ttu-id="bbc5a-237">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbc5a-237">Windows 7</span></span>     |
| [<span data-ttu-id="bbc5a-238">**авдеквидеофастдекодемоде**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-238">**AVDecVideoFastDecodeMode**</span></span>](avdecvideofastdecodemode.md)                            | <span data-ttu-id="bbc5a-239">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbc5a-239">Windows 7</span></span>     |
| [<span data-ttu-id="bbc5a-240">**авдеквидеоимажесизе**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-240">**AVDecVideoImageSize**</span></span>](avdecvideoimagesize.md)                                      | <span data-ttu-id="bbc5a-241">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbc5a-241">Windows 7</span></span>     |
| [<span data-ttu-id="bbc5a-242">**авдеквидеософтваредеинтерлацемоде**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-242">**AVDecVideoSoftwareDeinterlaceMode**</span></span>](avdecvideosoftwaredeinterlacemode-property.md) | <span data-ttu-id="bbc5a-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbc5a-243">Windows 7</span></span>     |
| [<span data-ttu-id="bbc5a-244">**авдеквидеосумбнаилженератионмоде**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-244">**AVDecVideoThumbnailGenerationMode**</span></span>](avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="bbc5a-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbc5a-245">Windows 7</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="bbc5a-246">Требования</span><span class="sxs-lookup"><span data-stu-id="bbc5a-246">Requirements</span></span>



| <span data-ttu-id="bbc5a-247">Требование</span><span class="sxs-lookup"><span data-stu-id="bbc5a-247">Requirement</span></span> | <span data-ttu-id="bbc5a-248">Значение</span><span class="sxs-lookup"><span data-stu-id="bbc5a-248">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc5a-249">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbc5a-249">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc5a-250">Windows Vista Домашняя расширенная, Windows Vista Ultimate, Windows 7 Домашняя расширенная, Windows 7 Профессиональная, Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="bbc5a-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bbc5a-251">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbc5a-251">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc5a-252">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bbc5a-252">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="bbc5a-253">Header</span><span class="sxs-lookup"><span data-stu-id="bbc5a-253">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbc5a-254"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbc5a-254"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="bbc5a-255">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbc5a-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc5a-256">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="bbc5a-256">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="bbc5a-257">**Типы носителей DVD**</span><span class="sxs-lookup"><span data-stu-id="bbc5a-257">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> <dt>

[<span data-ttu-id="bbc5a-258">Типы видео H. 264</span><span class="sxs-lookup"><span data-stu-id="bbc5a-258">H.264 Video Types</span></span>](h-264-video-types.md)
</dt> </dl>

 

 
