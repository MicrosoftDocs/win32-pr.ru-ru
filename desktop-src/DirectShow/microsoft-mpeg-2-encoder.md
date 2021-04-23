---
description: Фильтр кодировщика Microsoft MPEG-2 кодирует аудио и видео MPEG-2 и мультиплексирование потоков для создания потока программы MPEG-2 или транспортного потока.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Кодировщик Microsoft MPEG-2 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805626"
---
# <a name="microsoft-mpeg-2-encoder"></a><span data-ttu-id="90922-103">Кодировщик Microsoft MPEG-2</span><span class="sxs-lookup"><span data-stu-id="90922-103">Microsoft MPEG-2 Encoder</span></span>

<span data-ttu-id="90922-104">Фильтр кодировщика Microsoft MPEG-2 кодирует аудио и видео MPEG-2 и мультиплексирование потоков для создания потока программы MPEG-2 или транспортного потока.</span><span class="sxs-lookup"><span data-stu-id="90922-104">The Microsoft MPEG-2 Encoder filter encodes MPEG-2 audio and video and multiplexes the streams to generate an MPEG-2 program stream or transport stream.</span></span>

> [!Note]  
> <span data-ttu-id="90922-105">Этот фильтр не поддерживается на платформах на базе IA-64.</span><span class="sxs-lookup"><span data-stu-id="90922-105">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="90922-106">Сведения о фильтре</span><span class="sxs-lookup"><span data-stu-id="90922-106">Filter Information</span></span>

<span data-ttu-id="90922-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="90922-107">Filter Interfaces</span></span>

[<span data-ttu-id="90922-108">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="90922-108">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="90922-109">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="90922-109">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="90922-110">**иенкодерапи**</span><span class="sxs-lookup"><span data-stu-id="90922-110">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="90922-111">**имедиасикинг**</span><span class="sxs-lookup"><span data-stu-id="90922-111">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="90922-112">**ивидеоенкодер**</span><span class="sxs-lookup"><span data-stu-id="90922-112">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="90922-113">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="90922-113">Input Pin Media Types</span></span>

<span data-ttu-id="90922-114">См. примечания</span><span class="sxs-lookup"><span data-stu-id="90922-114">See Remarks</span></span>

<span data-ttu-id="90922-115">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="90922-115">Input Pin Interfaces</span></span>

[<span data-ttu-id="90922-116">**имеминпутпин**</span><span class="sxs-lookup"><span data-stu-id="90922-116">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="90922-117">**ипин**</span><span class="sxs-lookup"><span data-stu-id="90922-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="90922-118">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="90922-118">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="90922-119">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="90922-119">Output Pin Media Types</span></span>

<span data-ttu-id="90922-120">См. примечания</span><span class="sxs-lookup"><span data-stu-id="90922-120">See Remarks</span></span>

<span data-ttu-id="90922-121">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="90922-121">Output Pin Interfaces</span></span>

[<span data-ttu-id="90922-122">**имедиасикинг**</span><span class="sxs-lookup"><span data-stu-id="90922-122">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="90922-123">**ипин**</span><span class="sxs-lookup"><span data-stu-id="90922-123">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="90922-124">**икуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="90922-124">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="90922-125">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="90922-125">Filter CLSID</span></span>

<span data-ttu-id="90922-126">**Идентификатор CLSID \_ CMPEG2EncoderDS** (объявлено в вмкодекдсп. h)</span><span class="sxs-lookup"><span data-stu-id="90922-126">**CLSID\_CMPEG2EncoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="90922-127">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="90922-127">Executable</span></span>

<span data-ttu-id="90922-128">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="90922-128">msmpeg2enc.dll</span></span>

[<span data-ttu-id="90922-129">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="90922-129">Merit</span></span>](merit.md)

<span data-ttu-id="90922-130">**\_ \_ не \_ использовать**</span><span class="sxs-lookup"><span data-stu-id="90922-130">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="90922-131">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="90922-131">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="90922-132">**\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**</span><span class="sxs-lookup"><span data-stu-id="90922-132">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="90922-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90922-133">Remarks</span></span>

<span data-ttu-id="90922-134">Этот фильтр сочетает в себе функции кодирования двух других фильтров:</span><span class="sxs-lookup"><span data-stu-id="90922-134">This filter combines the encoding functionality of two other filters:</span></span>

-   [<span data-ttu-id="90922-135">**Кодировщик Microsoft MPEG-2 Audio Encoder**</span><span class="sxs-lookup"><span data-stu-id="90922-135">**Microsoft MPEG-2 Audio Encoder**</span></span>](microsoft-mpeg-2-audio-encoder.md)
-   [<span data-ttu-id="90922-136">**Видеокодировщик Microsoft MPEG-2 видео**</span><span class="sxs-lookup"><span data-stu-id="90922-136">**Microsoft MPEG-2 Video Encoder**</span></span>](microsoft-mpeg-2-video-encoder.md)

<span data-ttu-id="90922-137">Если не указано иное, этот фильтр поддерживает те же функции кодирования, что и эти два кодировщика.</span><span class="sxs-lookup"><span data-stu-id="90922-137">Except as noted, this filter supports the same encoding features as those two encoders.</span></span>

<span data-ttu-id="90922-138">Изначально фильтр имеет один входной ПИН-код, который может принимать звук или видео.</span><span class="sxs-lookup"><span data-stu-id="90922-138">Initially the filter has one input pin, which can accept audio or video input.</span></span> <span data-ttu-id="90922-139">Когда этот ПИН-код подключен, фильтр создает второй входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="90922-139">When that pin is connected, the filter creates a second input pin.</span></span> <span data-ttu-id="90922-140">Если первый входной ПИН-код получает звук, второй входной ПИН-код принимает только видео и наоборот.</span><span class="sxs-lookup"><span data-stu-id="90922-140">If the first input pin receives audio, the second input pin accepts only video, and vice versa.</span></span> <span data-ttu-id="90922-141">Каждый входной ПИН-код поддерживает те же типы носителей, что и соответствующий фильтр кодировщика.</span><span class="sxs-lookup"><span data-stu-id="90922-141">Each input pin supports the same media types as the corresponding encoder filter.</span></span>

<span data-ttu-id="90922-142">Если подключен только один входной ПИН-код, фильтр поддерживает те же выходные типы, что и соответствующий звуковой или видеокодировщик.</span><span class="sxs-lookup"><span data-stu-id="90922-142">If only one input pin is connected, the filter supports the same output types as the corresponding audio or video encoder.</span></span> <span data-ttu-id="90922-143">Если оба контакта подключены, фильтр поддерживает следующие типы выходных данных:</span><span class="sxs-lookup"><span data-stu-id="90922-143">If both pins are connected, the filter supports the following kinds of output:</span></span>

-   <span data-ttu-id="90922-144">Звук — визуальный элемент в потоке программы MPEG-2</span><span class="sxs-lookup"><span data-stu-id="90922-144">Audio-visual in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="90922-145">Звук — визуальный элемент в потоке транспорта MPEG-2</span><span class="sxs-lookup"><span data-stu-id="90922-145">Audio-visual in an MPEG-2 transport stream</span></span>

<span data-ttu-id="90922-146">Они соответствуют следующим типам выходных данных:</span><span class="sxs-lookup"><span data-stu-id="90922-146">These correspond to the following output types:</span></span>

-   <span data-ttu-id="90922-147">**MEDIATYPE \_ Stream**, **\_ \_ Программа медиасубтипе MPEG2**</span><span class="sxs-lookup"><span data-stu-id="90922-147">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>
-   <span data-ttu-id="90922-148">**MEDIATYPE \_ Поток**, **\_ \_ транспорт медиасубтипе MPEG2**</span><span class="sxs-lookup"><span data-stu-id="90922-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>

<span data-ttu-id="90922-149">Этот фильтр не может мультиплексировать потоки, которые были ранее закодированы.</span><span class="sxs-lookup"><span data-stu-id="90922-149">This filter cannot multiplex streams that were previously encoded.</span></span> <span data-ttu-id="90922-150">Входные потоки должны быть распакованными аудио-и видеозаписями, которые фильтр кодирует перед мультиплексированием.</span><span class="sxs-lookup"><span data-stu-id="90922-150">The input streams must be uncompressed audio/video, which the filter encodes before multiplexing.</span></span> <span data-ttu-id="90922-151">Мультиплексированный поток ограничен одной программой, которая содержит до одного аудио и одного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="90922-151">The multiplexed stream is limited to one program, containing up to one audio and one video stream.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="90922-152">Свойства кодека</span><span class="sxs-lookup"><span data-stu-id="90922-152">Codec Properties</span></span>

<span data-ttu-id="90922-153">Фильтр поддерживает комбинированные свойства фильтров [**MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) и [**кодировщиков видео MPEG-2**](microsoft-mpeg-2-video-encoder.md) со следующими отличиями.</span><span class="sxs-lookup"><span data-stu-id="90922-153">The filter supports the combined properties of the [**MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) and [**MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filters, with the following difference:</span></span>

-   <span data-ttu-id="90922-154">Свойство [**авенккоммонмеанбитрате**](avenccommonmeanbitrate-property.md) задает среднюю скорость потока видео.</span><span class="sxs-lookup"><span data-stu-id="90922-154">The [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property sets the average bit rate for the video stream.</span></span>
-   <span data-ttu-id="90922-155">Свойство [**авенкаудиомеанбитрате**](avencaudiomeanbitrate.md) задает среднюю скорость потока для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="90922-155">The [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) property sets the average bit rate for the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="90922-156">Требования</span><span class="sxs-lookup"><span data-stu-id="90922-156">Requirements</span></span>



| <span data-ttu-id="90922-157">Требование</span><span class="sxs-lookup"><span data-stu-id="90922-157">Requirement</span></span> | <span data-ttu-id="90922-158">Значение</span><span class="sxs-lookup"><span data-stu-id="90922-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90922-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90922-159">Minimum supported client</span></span><br/> | <span data-ttu-id="90922-160">Windows Vista Домашняя расширенная, Windows Vista Ultimate, Windows 7 Домашняя расширенная, Windows 7 Профессиональная, Windows 7 Корпоративная, \[ только классические приложения Windows 7 Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="90922-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90922-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90922-161">Minimum supported server</span></span><br/> | <span data-ttu-id="90922-162">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="90922-162">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="90922-163">Header</span><span class="sxs-lookup"><span data-stu-id="90922-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="90922-164"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="90922-164"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="90922-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90922-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90922-166">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="90922-166">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
