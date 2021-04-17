---
description: Приемник файлов MPEG-4 создает файлы MP4.
ms.assetid: 069b8e72-d081-466e-ac8d-c3f81c8a6f35
title: Приемник файлов MPEG-4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c27517463bca7dfa88fdbc09d77f7a6512c896d
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105651230"
---
# <a name="mpeg-4-file-sink"></a><span data-ttu-id="06f19-103">Приемник файлов MPEG-4</span><span class="sxs-lookup"><span data-stu-id="06f19-103">MPEG-4 File Sink</span></span>

<span data-ttu-id="06f19-104">Приемник файлов MPEG-4 создает файлы MP4.</span><span class="sxs-lookup"><span data-stu-id="06f19-104">The MPEG-4 file sink creates MP4 files.</span></span> <span data-ttu-id="06f19-105">Дополнительные сведения о формате файла MP4 см. в следующих документах по стандартам:</span><span class="sxs-lookup"><span data-stu-id="06f19-105">For more information about the MP4 file format, refer to the following standards documents:</span></span>

-   <span data-ttu-id="06f19-106">ISO/IEC 14496-12: *информационные технологии — Программирование звуковых визуальных объектов — часть 12: формат файла основного носителя ISO*</span><span class="sxs-lookup"><span data-stu-id="06f19-106">ISO/IEC 14496-12: *Information technology -- Coding of audio-visual objects -- Part 12: ISO Base Media File Format*</span></span>
-   <span data-ttu-id="06f19-107">ISO/IEC 14496-14: *информационные технологии — Программирование звуковых визуальных объектов — часть 14: формат файла MP4*</span><span class="sxs-lookup"><span data-stu-id="06f19-107">ISO/IEC 14496-14: *Information technology -- Coding of audio-visual objects -- Part 14: MP4 File Format*</span></span>

> [!Note]  
> <span data-ttu-id="06f19-108">(Эти ресурсы могут быть недоступны в некоторых языках и странах.)</span><span class="sxs-lookup"><span data-stu-id="06f19-108">(These resources may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="06f19-109">Приемник файлов MPEG-4 не инкапсулирует функциональность кодирования.</span><span class="sxs-lookup"><span data-stu-id="06f19-109">The MPEG-4 file sink does not encapsulate encoding functionality.</span></span>

<span data-ttu-id="06f19-110">Чтобы создать приемник файлов MPEG-4, вызовите функцию [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) .</span><span class="sxs-lookup"><span data-stu-id="06f19-110">To create the MPEG-4 file sink, call the [**MFCreateMPEG4MediaSink**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatempeg4mediasink) function.</span></span> <span data-ttu-id="06f19-111">Приемник файлов MPEG-4 предоставляет следующие интерфейсы через **QueryInterface**:</span><span class="sxs-lookup"><span data-stu-id="06f19-111">The MPEG-4 file sink exposes the following interfaces through **QueryInterface**:</span></span>

-   [<span data-ttu-id="06f19-112">**имфклоккстатесинк**</span><span class="sxs-lookup"><span data-stu-id="06f19-112">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="06f19-113">**имффинализаблемедиасинк**</span><span class="sxs-lookup"><span data-stu-id="06f19-113">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [<span data-ttu-id="06f19-114">**имфжетсервице**</span><span class="sxs-lookup"><span data-stu-id="06f19-114">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="06f19-115">**имфмедиаевентженератор**</span><span class="sxs-lookup"><span data-stu-id="06f19-115">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="06f19-116">**имфмедиасинк**</span><span class="sxs-lookup"><span data-stu-id="06f19-116">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="sample-description-box"></a><span data-ttu-id="06f19-117">Пример окна описания</span><span class="sxs-lookup"><span data-stu-id="06f19-117">Sample Description Box</span></span>

<span data-ttu-id="06f19-118">MP4 — это расширяемый формат контейнеров.</span><span class="sxs-lookup"><span data-stu-id="06f19-118">MP4 is an extensible container format.</span></span> <span data-ttu-id="06f19-119">Спецификация MP4 не определяет фиксированную структуру для описания типов мультимедиа в контейнере MP4.</span><span class="sxs-lookup"><span data-stu-id="06f19-119">The MP4 specification does not define a fixed structure for describing media types in an MP4 container.</span></span> <span data-ttu-id="06f19-120">Вместо этого он определяет иерархию объектов, позволяющую определять пользовательские структуры для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="06f19-120">Instead, it defines an object hierarchy that allows custom structures to be defined for each format.</span></span> <span data-ttu-id="06f19-121">Описание формата хранится в поле "пример описания" ("стсд") для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="06f19-121">The format description is stored in the sample description ('stsd') box for each stream.</span></span> <span data-ttu-id="06f19-122">В поле Описание примера содержится список образцов записей.</span><span class="sxs-lookup"><span data-stu-id="06f19-122">The sample description box contains a list of sample entries.</span></span> <span data-ttu-id="06f19-123">Для каждой записи примера 4-байтовый код, аналогичный набору FOURCC, определяет структуру формата.</span><span class="sxs-lookup"><span data-stu-id="06f19-123">For each sample entry, a 4-byte code, similar to a FOURCC, defines the format structure.</span></span>

<span data-ttu-id="06f19-124">Приемник файлов MPEG-4 может создавать образец окна описания для следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="06f19-124">The MPEG-4 File Sink can generate the sample description box for the following formats:</span></span>

-   <span data-ttu-id="06f19-125">H. 264/видео с AVC</span><span class="sxs-lookup"><span data-stu-id="06f19-125">H.264/AVC video</span></span>
-   <span data-ttu-id="06f19-126">AAC аудио</span><span class="sxs-lookup"><span data-stu-id="06f19-126">AAC audio</span></span>
-   <span data-ttu-id="06f19-127">Звуковые файлы в формате MP3</span><span class="sxs-lookup"><span data-stu-id="06f19-127">MP3 audio</span></span>

<span data-ttu-id="06f19-128">В других форматах поле Описание образца должно быть указано в типе носителя для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="06f19-128">For other formats, the sample description box must be provided in the media type for each stream.</span></span> <span data-ttu-id="06f19-129">Чтобы указать поле Описание образца, задайте следующие атрибуты типа носителя:</span><span class="sxs-lookup"><span data-stu-id="06f19-129">To specify the sample description box, set the following attributes on the media type:</span></span>



| <span data-ttu-id="06f19-130">attribute</span><span class="sxs-lookup"><span data-stu-id="06f19-130">Attribute</span></span>                                                                     | <span data-ttu-id="06f19-131">Описание</span><span class="sxs-lookup"><span data-stu-id="06f19-131">Description</span></span>                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06f19-132">\_ \_ \_ Описание образца MPEG4 \_ MF</span><span class="sxs-lookup"><span data-stu-id="06f19-132">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)      | <span data-ttu-id="06f19-133">Содержит пример поля описания как двоичный BLOB-объект.</span><span class="sxs-lookup"><span data-stu-id="06f19-133">Contains the sample description box as a binary blob.</span></span>                                                                                                         |
| [<span data-ttu-id="06f19-134">\_ \_ \_ \_ Запись текущего примера \_ в MF MT</span><span class="sxs-lookup"><span data-stu-id="06f19-134">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY</span></span>](mf-mt-mpeg4-current-sample-entry.md) | <span data-ttu-id="06f19-135">Указывает, какие из образцов записей в поле Образец описания активны в данный момент.</span><span class="sxs-lookup"><span data-stu-id="06f19-135">Specifies which of the sample entries in the sample description box is currently active.</span></span> <span data-ttu-id="06f19-136">(Необязательно.)</span><span class="sxs-lookup"><span data-stu-id="06f19-136">(Optional.)</span></span><br/> <span data-ttu-id="06f19-137">В настоящее время значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="06f19-137">Currently, the value must be zero.</span></span><br/> |



 

<span data-ttu-id="06f19-138">В некоторых случаях невозможно создать образец поля описания до тех пор, пока не будут закодированы все данные.</span><span class="sxs-lookup"><span data-stu-id="06f19-138">In some cases, it is not possible to generate a sample description box until all of the data has been encoded.</span></span> <span data-ttu-id="06f19-139">Например, такие сведения, как средняя скорость потока, могут быть не известны заранее.</span><span class="sxs-lookup"><span data-stu-id="06f19-139">For example, information such as the average bit rate might not be known ahead of time.</span></span> <span data-ttu-id="06f19-140">В этом случае можно обновить тип мультимедиа с помощью интерфейса [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) в приемнике файлов MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-140">In that case, you can update the media type by using the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the MPEG-4 file sink.</span></span> <span data-ttu-id="06f19-141">Это необходимо сделать до завершения воспроизведения приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="06f19-141">This must be done before the media sink is finalized.</span></span>

<span data-ttu-id="06f19-142">Обычно тип мультимедиа создается вышестоящим кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="06f19-142">Typically the media type is created by an upstream encoder.</span></span> <span data-ttu-id="06f19-143">Кодировщик может создать новый тип мультимедиа во время потоковой передачи, используя динамическое изменение формата.</span><span class="sxs-lookup"><span data-stu-id="06f19-143">The encoder can generate a new media type during streaming, through a dynamic format change.</span></span> <span data-ttu-id="06f19-144">Дополнительные сведения см. в разделе [динамические изменения формата](basic-mft-processing-model.md).</span><span class="sxs-lookup"><span data-stu-id="06f19-144">For more information, see [Dynamic Format Changes](basic-mft-processing-model.md).</span></span>

## <a name="h264avc-video"></a><span data-ttu-id="06f19-145">H. 264/видео с AVC</span><span class="sxs-lookup"><span data-stu-id="06f19-145">H.264/AVC Video</span></span>

<span data-ttu-id="06f19-146">Приемник файлов MPEG-4 поддерживает версию потока AVC, имеющего простейший видеопоток, с набором параметров Sequence (SPS) и набором параметров Picture (PPS) Налус, которые содержатся в 5,1 разделе «Пример описания», как определено в части 15 ISO/IEC 14496.</span><span class="sxs-lookup"><span data-stu-id="06f19-146">The MPEG-4 file sink supports the version of the AVC stream that has an elementary video stream, with sequence parameter set (SPS) and picture parameter set (PPS) NALUs contained in the sample description box, as defined in ISO/IEC 14496 part 15 section 5.1.</span></span> <span data-ttu-id="06f19-147">Приемник файлов не поддерживает альтернативный метод хранения SPS/PPS Налус как отдельный простой поток набора параметров.</span><span class="sxs-lookup"><span data-stu-id="06f19-147">The file sink does not support the alternate method of storing SPS/PPS NALUs as a separate parameter-set elementary stream.</span></span>

<span data-ttu-id="06f19-148">Приемник файлов MPEG-4 может создать поле описания, но должно быть предоставлено с помощью SPS и PPS Налус.</span><span class="sxs-lookup"><span data-stu-id="06f19-148">The MPEG-4 file sink can generate the sample description box, but must be provided with the SPS and PPS NALUs.</span></span> <span data-ttu-id="06f19-149">Укажите эти сведения в типе носителя, задав атрибут [**\_ \_ \_ \_ заголовка последовательностей MF MT MPEG**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="06f19-149">Specify this information in the media type by setting the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="06f19-150">Значением атрибута является заголовок последовательности H. 264.</span><span class="sxs-lookup"><span data-stu-id="06f19-150">The value of the attribute is the H.264 sequence header.</span></span> <span data-ttu-id="06f19-151">Заголовок последовательности должен содержать Налусы SPS и PPS, разделенные на 3-байтовые или 4-байтовые начальные коды.</span><span class="sxs-lookup"><span data-stu-id="06f19-151">The sequence header must consist of the SPS and PPS NALUs delimited by either 3-byte or 4-byte start codes.</span></span>

<span data-ttu-id="06f19-152">При необходимости при настройке приемника файла можно опустить атрибут [**\_ \_ \_ \_ заголовков последовательностей MF в формате MPEG MT**](mf-mt-mpeg-sequence-header-attribute.md) от исходного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="06f19-152">Optionally, when you configure the file sink, you can omit the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute from the initial media type.</span></span> <span data-ttu-id="06f19-153">В этом случае необходимо позднее обновить тип носителя, чтобы включить заголовок последовательности.</span><span class="sxs-lookup"><span data-stu-id="06f19-153">In that case, you must update the media type later to include the sequence header.</span></span>

<span data-ttu-id="06f19-154">Приемник файлов MPEG-4 имеет следующие требования к битстреамсу AVC:</span><span class="sxs-lookup"><span data-stu-id="06f19-154">The MPEG-4 file sink has the following requirements for AVC bitstreams:</span></span>

-   <span data-ttu-id="06f19-155">Битовый поток должен соответствовать спецификации формата H. 264 в приложении B.</span><span class="sxs-lookup"><span data-stu-id="06f19-155">The bitstream must conform to the H.264 Annex B format specification.</span></span> <span data-ttu-id="06f19-156">В частности, Налус необходимо разделять либо с помощью 3-байтового, либо из 4-байтового начального кода.</span><span class="sxs-lookup"><span data-stu-id="06f19-156">In particular, NALUs must be delimited with either 3-byte or 4-byte start codes.</span></span>
-   <span data-ttu-id="06f19-157">Примеры носителей должны содержать все Налус срезов и данных, которые соответствуют одному времени презентации.</span><span class="sxs-lookup"><span data-stu-id="06f19-157">Media samples must contain all slice and data NALUs that correspond to a single presentation time.</span></span>
-   <span data-ttu-id="06f19-158">При записи B-кадров в файл MP4 необходимо задать метку времени презентации и отметку времени декодирования.</span><span class="sxs-lookup"><span data-stu-id="06f19-158">When writing B-frames into an MP4 file, you must set both the presentation time stamp and the decode time stamp.</span></span> <span data-ttu-id="06f19-159">Если в потоке есть кадр B, а метка времени декодирования не задана, модуль записи MP4 будет видеть время кадра в обратном направлении, а кадр будет удален.</span><span class="sxs-lookup"><span data-stu-id="06f19-159">If stream has a B frame and the decode timestamp is not set, the MP4 writer will see the frame time going backwards and will drop the frame.</span></span> 

## <a name="aac-audio"></a><span data-ttu-id="06f19-160">Звук в формате AAC</span><span class="sxs-lookup"><span data-stu-id="06f19-160">AAC Audio</span></span>

<span data-ttu-id="06f19-161">Для AAC Audio приемник файлов MPEG-4 может создать образец окна описания для следующих подтипов:</span><span class="sxs-lookup"><span data-stu-id="06f19-161">For AAC audio, the MPEG-4 file sink can generate the sample description box for the following subtypes:</span></span>

-   <span data-ttu-id="06f19-162">**Мфаудиоформат \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="06f19-162">**MFAudioFormat\_AAC**</span></span>
-   <span data-ttu-id="06f19-163">**МЕДИАСУБТИПЕ \_ RAW \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="06f19-163">**MEDIASUBTYPE\_RAW\_AAC1**</span></span>

<span data-ttu-id="06f19-164">Дополнительные сведения об этих субстипесх см. в разделе [AAC Media Types](aac-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="06f19-164">For more information about these substypes, see [AAC Media Types](aac-media-types.md).</span></span>

<span data-ttu-id="06f19-165">Для подтипа **мфаудиоформат \_ AAC** тип мультимедиа дополнительно содержит атрибут [**\_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="06f19-165">For the **MFAudioFormat\_AAC** subtype, the media type optionally contains the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="06f19-166">При наличии этот атрибут является частью структуры [**хеааквавеинфо**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) , которая отображается после структуры **вавеформатекс** (то есть после элемента **вфкс** ).</span><span class="sxs-lookup"><span data-stu-id="06f19-166">If present, this attribute the portion of the [**HEAACWAVEINFO**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveinfo) structure that appears after the **WAVEFORMATEX** structure (that is, after the **wfx** member).</span></span> <span data-ttu-id="06f19-167">За ним следуют данные АудиоспеЦификконфиг () в соответствии с определением ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="06f19-167">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span> <span data-ttu-id="06f19-168">Если отсутствует **атрибут \_ \_ \_ данных пользователя MF MT** , предполагается, что используется профиль AAC с низким уровнем сложности (LC), а приемник файла MPEG-4 создает подходящий пример окна описания.</span><span class="sxs-lookup"><span data-stu-id="06f19-168">If the **MF\_MT\_USER\_DATA** attribute is not present, the stream is assumed to be AAC Low Complexity (LC) profile, and the MPEG-4 file sink generates a suitable sample description box.</span></span>

<span data-ttu-id="06f19-169">Для подтипа **медиасубтипе \_ RAW \_ AAC1** приемник мультимедиа должен содержать атрибут [**\_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) , а атрибут должен содержать данные аудиоспеЦификконфиг ().</span><span class="sxs-lookup"><span data-stu-id="06f19-169">For the **MEDIASUBTYPE\_RAW\_AAC1** subtype, the media sink must contain the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute, and the attribute must contain the AudioSpecificConfig() data.</span></span>

<span data-ttu-id="06f19-170">Приемник файлов MPEG-4 создает вариант образца AAC в формате MPEG-4 с помощью записи примера "mp4a" с Обжекттипеиндикатион = 0x40.</span><span class="sxs-lookup"><span data-stu-id="06f19-170">The MPEG-4 file sink creates the MPEG-4 variant of the AAC sample description box, using an 'mp4a' sample entry with objectTypeIndication = 0x40.</span></span> <span data-ttu-id="06f19-171">В нем не используются типы объектов MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="06f19-171">It does not use MPEG-2 object types.</span></span>

## <a name="mp3-audio"></a><span data-ttu-id="06f19-172">Аудио в формате MP3</span><span class="sxs-lookup"><span data-stu-id="06f19-172">MP3 Audio</span></span>

<span data-ttu-id="06f19-173">Для MP3 Audio приемник файлов MPEG-4 может создать пример поля описания на основе стандартного типа аудио Media.</span><span class="sxs-lookup"><span data-stu-id="06f19-173">For MP3 audio, the MPEG-4 file sink can generate the sample description box from a standard audio media type.</span></span> <span data-ttu-id="06f19-174">(См. раздел [типы звуковых носителей](audio-media-types.md).)</span><span class="sxs-lookup"><span data-stu-id="06f19-174">(See [Audio Media Types](audio-media-types.md).)</span></span>

<span data-ttu-id="06f19-175">Приемник файлов MPEG-4 создает вариант с образцом MPEG-4 в поле описания образца MP3 с помощью записи примера "mp4a" с Обжекттипеиндикатион = 0x6B для звука MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="06f19-175">The MPEG-4 file sink creates the MPEG-4 variant of the MP3 sample description box, using an 'mp4a' sample entry with objectTypeIndication = 0x6b for MPEG-1 audio.</span></span>

## <a name="limitations"></a><span data-ttu-id="06f19-176">Ограничения</span><span class="sxs-lookup"><span data-stu-id="06f19-176">Limitations</span></span>

-   <span data-ttu-id="06f19-177">Максимальный размер созданного файла составляет 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="06f19-177">The maximum size of the authored file is 4 GB.</span></span> <span data-ttu-id="06f19-178">В Windows 8 поддерживаются файлы размером более 4 ГБГБ.</span><span class="sxs-lookup"><span data-stu-id="06f19-178">In Windows 8, files large than 4 GBGB are supported.</span></span>
-   <span data-ttu-id="06f19-179">Приемник файлов MPEG-4 не поддерживает списки редактирования ("едтс" и "елст").</span><span class="sxs-lookup"><span data-stu-id="06f19-179">The MPEG-4 file sink does not support edit lists ('edts' and 'elst' boxes).</span></span>

## <a name="windows-8-updates-to-mpeg-4-source-and-sink"></a><span data-ttu-id="06f19-180">Обновления Windows 8 для источника и приемника MPEG-4</span><span class="sxs-lookup"><span data-stu-id="06f19-180">Windows 8 updates to MPEG-4 source and sink</span></span>

-   <span data-ttu-id="06f19-181">Поддержка вращения чтения и записи добавлена в источнике и приемнике Windows 8 MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-181">Rotation read and write support added in Windows 8 MPEG-4 source and sink.</span></span> <span data-ttu-id="06f19-182">Это не поддерживается в источнике и приемнике Windows 7 MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-182">This is not supported in the Windows 7 MPEG-4 source and sink.</span></span>

    <span data-ttu-id="06f19-183">Источник MPEG-4 считывает угол поворота для активной видеодорожки в виде суммы угла вращения из "мвхд" и из "ткхд".</span><span class="sxs-lookup"><span data-stu-id="06f19-183">MPEG-4 source reads the rotation angle for an active video track as the sum of the rotation angle from ‘mvhd’ and from ‘tkhd’.</span></span>

    <span data-ttu-id="06f19-184">Приемник Microsoft MPEG-4 записывает угол вращения в "ткхд", но записывает матрицу 0 градусов (Identity) в "мвхд".</span><span class="sxs-lookup"><span data-stu-id="06f19-184">Microsoft MPEG-4 sink writes the rotation angle in ‘tkhd’ but writes 0 degree (identity) matrix in ‘mvhd’.</span></span> <span data-ttu-id="06f19-185">Обратите внимание, что приемник Microsoft MPEG-4 поддерживает только одну видеодорожку.</span><span class="sxs-lookup"><span data-stu-id="06f19-185">Note, Microsoft MPEG-4 sink only supports single video track.</span></span>

    <span data-ttu-id="06f19-186">Ипропертисторе считывает угол поворота только для первой видеодорожки в виде суммы угла вращения из "мвхд" и из "ткхд".</span><span class="sxs-lookup"><span data-stu-id="06f19-186">IPropertyStore reads the rotation angle for only the first video track as the sum of the rotation angle from ‘mvhd’ and from ‘tkhd’.</span></span>

    <span data-ttu-id="06f19-187">Ипропертисторе записывает угол поворота только для первой видеодорожки в "ткхд" после того, как угол вращения изменяется в соответствии с углом вращения в "мвхд", если он существует.</span><span class="sxs-lookup"><span data-stu-id="06f19-187">IPropertyStore writes the rotation angle for only the first video track in ‘tkhd’ after the rotation angle is adjusted according to the rotation angle in ‘mvhd’, if it exists.</span></span>

-   <span data-ttu-id="06f19-188">Фрагменты роликов ("moof") поддерживаются в источнике и приемнике Windows 8 MPEG-4, но "mfra" — нет.</span><span class="sxs-lookup"><span data-stu-id="06f19-188">Movie fragments ('moof') is supported in Windows 8 MPEG-4 source and sink, but 'mfra' is not.</span></span>
-   <span data-ttu-id="06f19-189">H. 263 поддерживается в источнике Windows 8 MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-189">H.263 is supported in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="06f19-190">Источник MPEG-4 теперь сопоставляет два объекта FourCC "H263" и 263 "в формате MPEG-4 с типом мультимедиа **мфвидеоформат \_ H263**.</span><span class="sxs-lookup"><span data-stu-id="06f19-190">MPEG-4 source now maps two fourcc’s of ‘h263’ and ‘s263’ in MPEG-4 file format to the media type of **MFVideoFormat\_H263**.</span></span>

-   <span data-ttu-id="06f19-191">Дополнительная поддержка FourCC добавлена для МЖПЕГ в источнике Windows 8 MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-191">More fourcc support added for MJPEG in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="06f19-192">Источник MPEG-4 сопоставляет фаукк из "DMB1" с типом мультимедиа **мфвидеоформат \_ мжпг**.</span><span class="sxs-lookup"><span data-stu-id="06f19-192">MPEG-4 source maps foucc of ‘dmb1’ to the media type of **MFVideoFormat\_MJPG**.</span></span>

-   <span data-ttu-id="06f19-193">Поддержка метаданных фуригана добавлена в источник Windows 8 MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-193">Furigana metadata support added in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="06f19-194">Источник MPEG-4 считывает метаданные фуригана из "СОАЛ", "взлетел", "соаа", "сонм" и "Соко".</span><span class="sxs-lookup"><span data-stu-id="06f19-194">MPEG-4 source reads Furigana metadata from ’soal’, ‘soar’, ‘soaa’, ‘sonm’, and ‘soco’.</span></span> <span data-ttu-id="06f19-195">Ипропертисторе считывает метаданные Фуригнана через набор соответствующих PKEY.</span><span class="sxs-lookup"><span data-stu-id="06f19-195">IPropertyStore reads Furignana metadata through the set of corresponding PKEYs.</span></span>

    <span data-ttu-id="06f19-196">В следующей таблице показано сопоставление канонического имени оболочки, ключа свойства и идентификатора поля/тега в формате файла MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-196">The following table shows the mapping between the shell canonical name, the property key, and the box/tag ID in MPEG-4 file format.</span></span>

    

    | <span data-ttu-id="06f19-197">Поле</span><span class="sxs-lookup"><span data-stu-id="06f19-197">Field</span></span>                                | <span data-ttu-id="06f19-198">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="06f19-198">Property Key</span></span>                         | <span data-ttu-id="06f19-199">ИДЕНТИФИКАТОР тега или Box</span><span class="sxs-lookup"><span data-stu-id="06f19-199">Tag/Box ID</span></span> |
    |--------------------------------------|--------------------------------------|------------|
    | <span data-ttu-id="06f19-200">System. Music. Албумтитлесортоверриде</span><span class="sxs-lookup"><span data-stu-id="06f19-200">System.Music.AlbumTitleSortOverride</span></span>  | <span data-ttu-id="06f19-201">\_ \_ Албумтитлесортоверриденая музыка PKEY</span><span class="sxs-lookup"><span data-stu-id="06f19-201">PKEY\_Music\_AlbumTitleSortOverride</span></span>  | <span data-ttu-id="06f19-202">соал</span><span class="sxs-lookup"><span data-stu-id="06f19-202">soal</span></span>       |
    | <span data-ttu-id="06f19-203">System. Music. Артистсортоверриде</span><span class="sxs-lookup"><span data-stu-id="06f19-203">System.Music.ArtistSortOverride</span></span>      | <span data-ttu-id="06f19-204">\_ \_ Артистсортоверриденая музыка PKEY</span><span class="sxs-lookup"><span data-stu-id="06f19-204">PKEY\_Music\_ArtistSortOverride</span></span>      | <span data-ttu-id="06f19-205">взлетел</span><span class="sxs-lookup"><span data-stu-id="06f19-205">soar</span></span>       |
    | <span data-ttu-id="06f19-206">System. Music. Албумартистсортоверриде</span><span class="sxs-lookup"><span data-stu-id="06f19-206">System.Music.AlbumArtistSortOverride</span></span> | <span data-ttu-id="06f19-207">\_ \_ Албумартистсортоверриденая музыка PKEY</span><span class="sxs-lookup"><span data-stu-id="06f19-207">PKEY\_Music\_AlbumArtistSortOverride</span></span> | <span data-ttu-id="06f19-208">соаа</span><span class="sxs-lookup"><span data-stu-id="06f19-208">soaa</span></span>       |
    | <span data-ttu-id="06f19-209">System. Титлесортоверриде</span><span class="sxs-lookup"><span data-stu-id="06f19-209">System.TitleSortOverride</span></span>             | <span data-ttu-id="06f19-210">PKEY \_ титлесортоверриде</span><span class="sxs-lookup"><span data-stu-id="06f19-210">PKEY \_TitleSortOverride</span></span>             | <span data-ttu-id="06f19-211">сонм</span><span class="sxs-lookup"><span data-stu-id="06f19-211">sonm</span></span>       |
    | <span data-ttu-id="06f19-212">System. Music. Компосерсортоверриде</span><span class="sxs-lookup"><span data-stu-id="06f19-212">System.Music.ComposerSortOverride</span></span>    | <span data-ttu-id="06f19-213">\_ \_ Компосерсортоверриденая музыка PKEY</span><span class="sxs-lookup"><span data-stu-id="06f19-213">PKEY\_Music\_ComposerSortOverride</span></span>    | <span data-ttu-id="06f19-214">соко</span><span class="sxs-lookup"><span data-stu-id="06f19-214">soco</span></span>       |

    

     

-   <span data-ttu-id="06f19-215">Поддержка стерео 3D Atom добавлена в источнике Windows 8 MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-215">Stereo 3D atom support added in Windows 8 MPEG-4 source.</span></span>

-   <span data-ttu-id="06f19-216">Поддержка AC3 и DD + добавлена в источник и приемник Windows 8 MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-216">AC3 and DD+ support added in Windows 8 MPEG-4 source and sink.</span></span>
-   <span data-ttu-id="06f19-217">Файлы размером более 4 ГБ поддерживаются в приемнике MPEG-4 Windows 8 для нефрагментированного MP4.</span><span class="sxs-lookup"><span data-stu-id="06f19-217">Files larger than 4 GB are supported in Windows 8 MPEG-4 sink for non-fragmental MP4.</span></span>
-   <span data-ttu-id="06f19-218">Очистка оптимизирована в источнике Windows 8 MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-218">Scrubbing has been optimized in Windows 8 MPEG-4 source.</span></span>

    <span data-ttu-id="06f19-219">Чтобы сократить задержку, сведения о двух ближайших ключевых кадрах для конкретной должности предоставляются через [**имфсикинфо:: жетнеаресткэйфрамес**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes).</span><span class="sxs-lookup"><span data-stu-id="06f19-219">To reduce latency, information for the two nearest key frames for a particular seek position are exposed through [**IMFSeekInfo::GetNearestKeyFrames**](/windows/desktop/api/mfidl/nf-mfidl-imfseekinfo-getnearestkeyframes).</span></span> <span data-ttu-id="06f19-220">Так как ключевой кадр не имеет зависимых кадров, он представляет кадр после декодирования только одного кадра.</span><span class="sxs-lookup"><span data-stu-id="06f19-220">Since the key frame does not have dependent frames, it presents the frame after decoding only one frame.</span></span> <span data-ttu-id="06f19-221">Используйте [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) для получения этого интерфейса через источник мультимедиа, конвейер или приложение.</span><span class="sxs-lookup"><span data-stu-id="06f19-221">Use [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to obtain this interface through the media source, pipeline, or application.</span></span>

    <span data-ttu-id="06f19-222">Задайте для параметра rate (нулевое значение) в источнике MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-222">Set rate to zero in MPEG-4 source.</span></span> <span data-ttu-id="06f19-223">Если конвейер находится в режиме очистки, скорость равна нулю.</span><span class="sxs-lookup"><span data-stu-id="06f19-223">When the pipeline is in scrubbing mode, the rate is zero.</span></span>

-   <span data-ttu-id="06f19-224">SPS и PPS могут храниться в образцах данных в приемнике MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-224">SPS and PPS can be stored in sample data in MPEG-4 sink.</span></span>

    <span data-ttu-id="06f19-225">[MF \_ Атрибут \_ \_ транзитного спсппс MPEG4SINK](mf-mpeg4sink-spspps-passthrough.md) в приемнике MPEG-4 определен, чтобы разрешить сохранение SPS и PPS вместе со входными образцами (H. 264 Video Data).</span><span class="sxs-lookup"><span data-stu-id="06f19-225">[MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH](mf-mpeg4sink-spspps-passthrough.md) attribute on MPEG-4 sink is defined to allow SPS’s and PPS’s to be saved together with input samples (H.264 video data).</span></span> <span data-ttu-id="06f19-226">Созданные зажимы MP4 воспроизводятся с помощью Windows 7 MPEG-4 и других источников.</span><span class="sxs-lookup"><span data-stu-id="06f19-226">The produced mp4 clips are play-able by Windows 7 MPEG-4 source and others.</span></span>

-   <span data-ttu-id="06f19-227">SPS и PPS можно извлечь из примеров входных данных в приемнике MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="06f19-227">SPS and PPS can be extracted from input samples in MPEG-4 sink.</span></span>

    <span data-ttu-id="06f19-228">Если в качестве входного носителя для приемника MPEG-4 не заданы протоколы SPS и PPS с использованием [ \_ \_ \_ \_ заголовка последовательного входа MPEG MT](mf-mt-mpeg-sequence-header-attribute.md) , приемник MPEG-4 попытается извлечь SPS и PPS из входных образцов.</span><span class="sxs-lookup"><span data-stu-id="06f19-228">When SPS and PPS are not set through [MF\_MT\_MPEG\_SEQUENCE\_HEADER](mf-mt-mpeg-sequence-header-attribute.md) on input media type of the MPEG-4 sink, MPEG-4 sink will try to extract SPS and PPS from input samples.</span></span> <span data-ttu-id="06f19-229">Приемник MPEG-4 игнорирует все входные образцы, пока не найдет первый сервер SPS и PPS, так как все входные образцы без SPS и PPS не поддерживают декодирование.</span><span class="sxs-lookup"><span data-stu-id="06f19-229">MPEG-4 sink ignores any input samples until it finds the first SPS and PPS, because all input samples without SPS and PPS are not decode-able.</span></span>

-   <span data-ttu-id="06f19-230">Объемная информация в записи конфигурации AVC поддерживается для нефрагментированного MP4.</span><span class="sxs-lookup"><span data-stu-id="06f19-230">3D information in AVC configuration record is supported for non-fragmental MP4.</span></span>
-   <span data-ttu-id="06f19-231">НАЛУ длина предоставляется для сжатых образцов H. 264 для оптимизации H. 264 ВЛД ДКСВА декодирования.</span><span class="sxs-lookup"><span data-stu-id="06f19-231">NALU length is exposed for H.264 compressed samples to optimize H.264 VLD DXVA decoding.</span></span>

    <span data-ttu-id="06f19-232">Набор исходных файлов MPEG- [4 \_ имеет длину MF налу, \_ \_ установленную](mf-nalu-length-set.md) на выходном типе носителя **мфвидеоформат \_ H264 Single bitrate** или **мфвидеоформат \_ H264 Single bitrate**.</span><span class="sxs-lookup"><span data-stu-id="06f19-232">MPEG-4 source sets [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) on the output media type of **MFVideoFormat\_H264** or **MFVideoFormat\_h264**.</span></span> <span data-ttu-id="06f19-233">Он задает большой двоичный [объект \_ налу \_ длины \_ MF](mf-nalu-length-information.md) для каждого выходного образца с 4-байтовой длиной налу для разных налу в одном сжатом примере.</span><span class="sxs-lookup"><span data-stu-id="06f19-233">It sets the blob of [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) on each output sample, with four-byte NALU length for different NALU’s in one compressed sample.</span></span>

-   <span data-ttu-id="06f19-234">Добавлена поддержка для звука MPEG2 ADTS в источнике MP4.</span><span class="sxs-lookup"><span data-stu-id="06f19-234">Support added for MPEG2 ADTS audio in MP4 source.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f19-235">Требования</span><span class="sxs-lookup"><span data-stu-id="06f19-235">Requirements</span></span>



| <span data-ttu-id="06f19-236">Требование</span><span class="sxs-lookup"><span data-stu-id="06f19-236">Requirement</span></span> | <span data-ttu-id="06f19-237">Значение</span><span class="sxs-lookup"><span data-stu-id="06f19-237">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="06f19-238">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06f19-238">Minimum supported client</span></span><br/> | <span data-ttu-id="06f19-239">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="06f19-239">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="06f19-240">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06f19-240">Minimum supported server</span></span><br/> | <span data-ttu-id="06f19-241">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="06f19-241">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06f19-242">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06f19-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f19-243">Источники и приемники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="06f19-243">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="06f19-244">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="06f19-244">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="06f19-245">Поддержка MPEG-4 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06f19-245">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="06f19-246">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06f19-246">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
