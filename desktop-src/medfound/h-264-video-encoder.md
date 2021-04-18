---
description: 'Кодировщик видео Microsoft Media Foundation H. 264 — это преобразование Media Foundation, которое поддерживает следующие профили H. 264:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Кодировщик видео H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711356"
---
# <a name="h264-video-encoder"></a><span data-ttu-id="48fdd-103">Кодировщик видео H. 264</span><span class="sxs-lookup"><span data-stu-id="48fdd-103">H.264 Video Encoder</span></span>

<span data-ttu-id="48fdd-104">Кодировщик видео Microsoft Media Foundation H. 264 — это [преобразование Media Foundation](media-foundation-transforms.md) , которое поддерживает следующие профили H. 264:</span><span class="sxs-lookup"><span data-stu-id="48fdd-104">The Microsoft Media Foundation H.264 video encoder is a [Media Foundation transform](media-foundation-transforms.md) that supports the following H.264 profiles:</span></span>

-   <span data-ttu-id="48fdd-105">Базовый профиль</span><span class="sxs-lookup"><span data-stu-id="48fdd-105">Baseline Profile</span></span>
-   <span data-ttu-id="48fdd-106">Профиль Main</span><span class="sxs-lookup"><span data-stu-id="48fdd-106">Main Profile</span></span>
-   <span data-ttu-id="48fdd-107">Высокий профиль (требуется Windows 8)</span><span class="sxs-lookup"><span data-stu-id="48fdd-107">High profile (requires Windows 8)</span></span>

<span data-ttu-id="48fdd-108">Кодировщик видео H. 264 предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="48fdd-108">The H.264 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="48fdd-109">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="48fdd-109">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="48fdd-110">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="48fdd-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="48fdd-111">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="48fdd-111">Input Types</span></span>

<span data-ttu-id="48fdd-112">Входной тип носителя должен иметь один из следующих подтипов:</span><span class="sxs-lookup"><span data-stu-id="48fdd-112">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="48fdd-113">**MFVideoFormat_I420**</span><span class="sxs-lookup"><span data-stu-id="48fdd-113">**MFVideoFormat_I420**</span></span>
-   <span data-ttu-id="48fdd-114">**MFVideoFormat_IYUV**</span><span class="sxs-lookup"><span data-stu-id="48fdd-114">**MFVideoFormat_IYUV**</span></span>
-   <span data-ttu-id="48fdd-115">**MFVideoFormat_NV12**</span><span class="sxs-lookup"><span data-stu-id="48fdd-115">**MFVideoFormat_NV12**</span></span>
-   <span data-ttu-id="48fdd-116">**MFVideoFormat_YUY2**</span><span class="sxs-lookup"><span data-stu-id="48fdd-116">**MFVideoFormat_YUY2**</span></span>
-   <span data-ttu-id="48fdd-117">**MFVideoFormat_YV12**</span><span class="sxs-lookup"><span data-stu-id="48fdd-117">**MFVideoFormat_YV12**</span></span>

<span data-ttu-id="48fdd-118">Дополнительные сведения об этих подтипах см. в разделе [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="48fdd-118">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="48fdd-119">Тип выходных данных должен быть задан перед входным типом.</span><span class="sxs-lookup"><span data-stu-id="48fdd-119">The output type must be set before the input type.</span></span> <span data-ttu-id="48fdd-120">Пока тип выходных данных не задан, метод [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) кодировщика возвращает **MF_E_TRANSFORM_TYPE_NOT_SET**.</span><span class="sxs-lookup"><span data-stu-id="48fdd-120">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF_E_TRANSFORM_TYPE_NOT_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="48fdd-121">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="48fdd-121">Output Types</span></span>

<span data-ttu-id="48fdd-122">Кодировщик поддерживает один выходной подтип:</span><span class="sxs-lookup"><span data-stu-id="48fdd-122">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="48fdd-123">**MFVideoFormat_H264**</span><span class="sxs-lookup"><span data-stu-id="48fdd-123">**MFVideoFormat_H264**</span></span>

<span data-ttu-id="48fdd-124">Задайте следующие атрибуты для выходного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="48fdd-124">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48fdd-125">attribute</span><span class="sxs-lookup"><span data-stu-id="48fdd-125">Attribute</span></span></th>
<th><span data-ttu-id="48fdd-126">Описание</span><span class="sxs-lookup"><span data-stu-id="48fdd-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48fdd-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="48fdd-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="48fdd-128">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="48fdd-128">Major type.</span></span> <span data-ttu-id="48fdd-129">Необходимо <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-129">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="48fdd-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="48fdd-131">Подтип видео.</span><span class="sxs-lookup"><span data-stu-id="48fdd-131">Video subtype.</span></span> <span data-ttu-id="48fdd-132">Необходимо <strong>MFVideoFormat_H264</strong>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-132">Must be <strong>MFVideoFormat_H264</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="48fdd-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="48fdd-134">Средняя скорость кодирования (бит в секунду).</span><span class="sxs-lookup"><span data-stu-id="48fdd-134">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="48fdd-135">Должен быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="48fdd-135">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="48fdd-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="48fdd-137">Частота кадров.</span><span class="sxs-lookup"><span data-stu-id="48fdd-137">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="48fdd-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="48fdd-139">Размер кадра.</span><span class="sxs-lookup"><span data-stu-id="48fdd-139">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="48fdd-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="48fdd-141">Режим чередования.</span><span class="sxs-lookup"><span data-stu-id="48fdd-141">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="48fdd-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span></span></td>
<td><span data-ttu-id="48fdd-143">Профиль кодирования H. 264.</span><span class="sxs-lookup"><span data-stu-id="48fdd-143">H.264 encoding profile.</span></span><br/> <span data-ttu-id="48fdd-144">Поддерживаются такие значения:</span><span class="sxs-lookup"><span data-stu-id="48fdd-144">The supported values are:</span></span><br/>
<ul>
<li><span data-ttu-id="48fdd-145"><strong>eAVEncH264VProfile_Base</strong> (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48fdd-145"><strong>eAVEncH264VProfile_Base</strong> (default)</span></span></li>
<li><span data-ttu-id="48fdd-146"><strong>eAVEncH264VProfile_Main</strong></span><span class="sxs-lookup"><span data-stu-id="48fdd-146"><strong>eAVEncH264VProfile_Main</strong></span></span></li>
<li><span data-ttu-id="48fdd-147"><strong>eAVEncH264VProfile_High</strong> (требуется Windows 8)</span><span class="sxs-lookup"><span data-stu-id="48fdd-147"><strong>eAVEncH264VProfile_High</strong> (requires Windows 8)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="48fdd-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="48fdd-149">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="48fdd-149">Optional.</span></span> <span data-ttu-id="48fdd-150">Задает уровень кодирования H. 264.</span><span class="sxs-lookup"><span data-stu-id="48fdd-150">Specifies the H.264 encoding level.</span></span><br/> <span data-ttu-id="48fdd-151">Значение по умолчанию равно – 1, что означает, что кодировщик выбирает уровень кодирования.</span><span class="sxs-lookup"><span data-stu-id="48fdd-151">The default value is –1, indicating that the encoder will select the encoding level.</span></span><br/> <span data-ttu-id="48fdd-152">Не рекомендуется задавать уровень в типе носителя и разрешать кодировщику выбирать уровень.</span><span class="sxs-lookup"><span data-stu-id="48fdd-152">It is recommended not to set the level in the media type, and allow the encoder to select the level.</span></span> <span data-ttu-id="48fdd-153">Кодировщик может наследовать соответствующий уровень для данного видеопотока, учитывая ограничения формата и характеристики видео.</span><span class="sxs-lookup"><span data-stu-id="48fdd-153">The encoder can derive the proper level for a given video stream, taking into account the format constraints and the characteristics of the video.</span></span> <span data-ttu-id="48fdd-154">Дополнительные сведения об ограничениях профиля и уровня см. в приложении A из ITU-T H. 264.</span><span class="sxs-lookup"><span data-stu-id="48fdd-154">For more information about profile and level constraints, refer to Annex A of ITU-T H.264.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="48fdd-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="48fdd-156">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="48fdd-156">Optional.</span></span> <span data-ttu-id="48fdd-157">Задает пропорцию в пикселях.</span><span class="sxs-lookup"><span data-stu-id="48fdd-157">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="48fdd-158">Значение по умолчанию — 1:1.</span><span class="sxs-lookup"><span data-stu-id="48fdd-158">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="48fdd-159">После установки типа выходных данных кодировщик видео обновляет тип, добавляя атрибут [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="48fdd-159">After the output type is set, the video encoder updates the type by adding the [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="48fdd-160">Этот атрибут содержит заголовок последовательности.</span><span class="sxs-lookup"><span data-stu-id="48fdd-160">This attribute contains the sequence header.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="48fdd-161">Свойства кодека</span><span class="sxs-lookup"><span data-stu-id="48fdd-161">Codec Properties</span></span>

<span data-ttu-id="48fdd-162">Кодировщик H. 264 реализует интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) для установки параметров кодирования.</span><span class="sxs-lookup"><span data-stu-id="48fdd-162">The H.264 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="48fdd-163">Он поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="48fdd-163">It supports the following properties.</span></span>

<span data-ttu-id="48fdd-164">Требования к кодеку для ХКК кодировщика см. в разделе " **сертифицированный аппаратный кодировщик** " ниже.</span><span class="sxs-lookup"><span data-stu-id="48fdd-164">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>

<span data-ttu-id="48fdd-165">В Windows 7 поддерживаются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="48fdd-165">The following properties are supported in Windows 7.</span></span>



| <span data-ttu-id="48fdd-166">Свойство</span><span class="sxs-lookup"><span data-stu-id="48fdd-166">Property</span></span>                                                                              | <span data-ttu-id="48fdd-167">Описание</span><span class="sxs-lookup"><span data-stu-id="48fdd-167">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48fdd-168">**CODECAPI_AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="48fdd-168">**CODECAPI_AVEncCommonRateControlMode**</span></span>](../directshow/avenccommonratecontrolmode-property.md) | <span data-ttu-id="48fdd-169">Задает режим управления скоростью.</span><span class="sxs-lookup"><span data-stu-id="48fdd-169">Sets the rate control mode.</span></span> <span data-ttu-id="48fdd-170">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="48fdd-170">See Remarks.</span></span> <span data-ttu-id="48fdd-171">Режим по умолчанию — это неограниченная переменная с битовой скоростью (VBR).</span><span class="sxs-lookup"><span data-stu-id="48fdd-171">The default mode is unconstrained variable bit rate (VBR).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="48fdd-172">**CODECAPI_AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="48fdd-172">**CODECAPI_AVEncCommonQuality**</span></span>](../directshow/avenccommonquality-property.md)                 | <span data-ttu-id="48fdd-173">Задает уровень качества.</span><span class="sxs-lookup"><span data-stu-id="48fdd-173">Sets the quality level.</span></span> <span data-ttu-id="48fdd-174">Это свойство применяется, когда режим управления скоростью имеет значение VBR на основе качества (**eAVEncCommonRateControlMode_Quality**).</span><span class="sxs-lookup"><span data-stu-id="48fdd-174">This property applies when the rate control mode is quality-based VBR (**eAVEncCommonRateControlMode_Quality**).</span></span> <span data-ttu-id="48fdd-175">Допустимый диапазон: 1 – 100.</span><span class="sxs-lookup"><span data-stu-id="48fdd-175">The valid range is 1–100.</span></span> <span data-ttu-id="48fdd-176">Значение по умолчанию — 70.</span><span class="sxs-lookup"><span data-stu-id="48fdd-176">The default value is 70.</span></span> <br/> <span data-ttu-id="48fdd-177">Чтобы задать этот параметр, задайте свойство перед вызовом [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="48fdd-177">To set this parameter, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <br/> <span data-ttu-id="48fdd-178">Чтобы задать этот параметр в Windows 7, задайте свойство перед вызовом [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="48fdd-178">To set this parameter in Windows 7, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="48fdd-179">Кодировщик игнорирует изменения после установки типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="48fdd-179">The encoder ignores changes after the output type is set.</span></span> <br/> <span data-ttu-id="48fdd-180">В Windows 8 это свойство можно задать в любое время во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="48fdd-180">In Windows 8, this property can be set at any time during encoding.</span></span> <span data-ttu-id="48fdd-181">Изменения применяются, начиная со следующего входного кадра.</span><span class="sxs-lookup"><span data-stu-id="48fdd-181">Changes are applied starting at the next input frame.</span></span> <br/> <span data-ttu-id="48fdd-182">Внутренне кодировщик преобразует это свойство в значение [авенквидеоенкодекп](codecapi-avencvideoencodeqp.md) .</span><span class="sxs-lookup"><span data-stu-id="48fdd-182">Internally, the encoder converts this property to an [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) value.</span></span> <br/> |



 

<span data-ttu-id="48fdd-183">Для следующих свойств требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="48fdd-183">The following properties require Windows 8.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48fdd-184">Свойство</span><span class="sxs-lookup"><span data-stu-id="48fdd-184">Property</span></span></th>
<th><span data-ttu-id="48fdd-185">Описание</span><span class="sxs-lookup"><span data-stu-id="48fdd-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48fdd-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span></span></td>
<td><span data-ttu-id="48fdd-187">Задает режим адаптивной кодировки.</span><span class="sxs-lookup"><span data-stu-id="48fdd-187">Sets the adaptive encoding mode.</span></span> <span data-ttu-id="48fdd-188">Кодировщик H. 264 поддерживает следующие режимы в Windows 8:</span><span class="sxs-lookup"><span data-stu-id="48fdd-188">The H.264 encoder supports the following modes in Windows 8:</span></span>
<ul>
<li><span data-ttu-id="48fdd-189"><strong>eAVEncAdaptiveMode_None</strong>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-189"><strong>eAVEncAdaptiveMode_None</strong>.</span></span> <span data-ttu-id="48fdd-190">Адаптивная кодировка отсутствует.</span><span class="sxs-lookup"><span data-stu-id="48fdd-190">No adaptive encoding.</span></span> <span data-ttu-id="48fdd-191">(по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="48fdd-191">(Default.)</span></span></li>
<li><span data-ttu-id="48fdd-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span></span> <span data-ttu-id="48fdd-193">Адаптивное изменение частоты кадров.</span><span class="sxs-lookup"><span data-stu-id="48fdd-193">Adaptively change the frame rate.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="48fdd-195">Задает размер буфера (в байтах) для кодирования с постоянной скоростью (CBR).</span><span class="sxs-lookup"><span data-stu-id="48fdd-195">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="48fdd-196">Допустимый диапазон: [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="48fdd-196">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="48fdd-197">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="48fdd-197">Requires Windows 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="48fdd-199">Для кодирования с ограниченным числом VBR указывает скорость, с которой &quot; &quot; происходит сток утечки, в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="48fdd-199">For constrained VBR encoding, specifies the rate at which the &quot;leaky bucket&quot; is drained, in bits per second.</span></span> <span data-ttu-id="48fdd-200">Это свойство применяется, когда режим управления скоростью <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-200">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span></span> <br/> <span data-ttu-id="48fdd-201">Допустимый диапазон: [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="48fdd-201">The valid range is [1 ... 2³²–1].</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="48fdd-203">Задает среднюю скорость потока в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="48fdd-203">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <span data-ttu-id="48fdd-204">Это свойство не учитывается, если режим управления скоростью имеет значение <strong>eAVEncCommonRateControlMode_Quality</strong>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-204">This property is ignored if the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="48fdd-205">Допустимый диапазон: [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="48fdd-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="48fdd-206">В режимах CBR и неограниченных VBR средняя скорость определяет конечный размер файла.</span><span class="sxs-lookup"><span data-stu-id="48fdd-206">In CBR and unconstrained VBR modes, the average bit rate determines the final size of the file.</span></span> <span data-ttu-id="48fdd-207">В режиме CBR средняя скорость потока — это также скорость, с которой сжатые биты преобразуются из &quot; сегмента утечки. &quot; (Дополнительные сведения см. в разделе <a href="the-leaky-bucket-buffer-model.md">модель буфера для сегмента утечки</a>.)</span><span class="sxs-lookup"><span data-stu-id="48fdd-207">In CBR mode, the average bit rate is also the rate at which compressed bits are drained from the &quot;leaky bucket.&quot; (For more information, see <a href="the-leaky-bucket-buffer-model.md">The Leaky Bucket Buffer Model</a>.)</span></span> <br/> <span data-ttu-id="48fdd-208">В Windows 7 средняя скорость потока определяется атрибутом <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> типа носителя.</span><span class="sxs-lookup"><span data-stu-id="48fdd-208">In Windows 7, the average bit rate is specified by the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute on the media type.</span></span> <br/> <span data-ttu-id="48fdd-209">В Windows 8 можно задать среднюю скорость потока, используя либо атрибут <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> , либо свойство <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> .</span><span class="sxs-lookup"><span data-stu-id="48fdd-209">In Windows 8, you can set the average bit rate using either the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute or the <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> property.</span></span> <span data-ttu-id="48fdd-210">Если заданы оба значения, CODECAPI_AVEncCommonMeanBitRate переопределений.</span><span class="sxs-lookup"><span data-stu-id="48fdd-210">If both are set, CODECAPI_AVEncCommonMeanBitRate overrides.</span></span> <span data-ttu-id="48fdd-211">В Windows 8 можно задать среднюю скорость потока во время кодирования.</span><span class="sxs-lookup"><span data-stu-id="48fdd-211">In Windows 8, you can set the average bit rate during encoding.</span></span> <span data-ttu-id="48fdd-212">При изменении частоты разрядов кодировщик использует адаптивную кодировку.</span><span class="sxs-lookup"><span data-stu-id="48fdd-212">If the bit rate changes, the encoder uses adaptive encoding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="48fdd-214">Задает компромисс качества и скорости.</span><span class="sxs-lookup"><span data-stu-id="48fdd-214">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="48fdd-215">Допустимый диапазон:</span><span class="sxs-lookup"><span data-stu-id="48fdd-215">Valid range:</span></span>
<ul>
<li><span data-ttu-id="48fdd-216">0 – 33: низкая сложность</span><span class="sxs-lookup"><span data-stu-id="48fdd-216">0–33: Low complexity</span></span></li>
<li><span data-ttu-id="48fdd-217">34 – 66: средняя сложность (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48fdd-217">34–66: Medium complexity (default)</span></span></li>
<li><span data-ttu-id="48fdd-218">67 – 100: высокая сложность</span><span class="sxs-lookup"><span data-stu-id="48fdd-218">67–100: High complexity</span></span></li>
</ul>
<br/> <span data-ttu-id="48fdd-219">Это значение влияет на то, как кодировщик выполняет различные операции кодирования, такие как компенсация движения.</span><span class="sxs-lookup"><span data-stu-id="48fdd-219">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="48fdd-220">На более высоких уровнях сложности кодировщик работает медленнее, но обеспечивает лучшее качество с той же скоростью.</span><span class="sxs-lookup"><span data-stu-id="48fdd-220">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span></span></td>
<td><span data-ttu-id="48fdd-222">Включает или отключает кабак (Адаптивное двоичное арифметическое кодирование) для H. 264-кода энтропии.</span><span class="sxs-lookup"><span data-stu-id="48fdd-222">Enables or disables CABAC (context-adaptive binary arithmetic coding) for H.264 entropy coding.</span></span> <span data-ttu-id="48fdd-223">Значение по умолчанию — <strong>VARIANT_FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-223">The default value is <strong>VARIANT_FALSE</strong>.</span></span> <br/> <span data-ttu-id="48fdd-224">Кабак не используется для базового профиля.</span><span class="sxs-lookup"><span data-stu-id="48fdd-224">CABAC is not used for Baseline profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span></span></td>
<td><span data-ttu-id="48fdd-226">Задает значение <strong>seq_parameter_set_id</strong> в ЕДИНИЦЕ SPS NAL для H. 264 битовый поток.</span><span class="sxs-lookup"><span data-stu-id="48fdd-226">Sets the value of <strong>seq_parameter_set_id</strong> in the SPS NAL unit of the H.264 bitstream.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span></span></td>
<td><span data-ttu-id="48fdd-228">Задает максимальное число последовательных кадров B в выходном битовый поток.</span><span class="sxs-lookup"><span data-stu-id="48fdd-228">Sets the maximum number of consecutive B frames in the output bitstream.</span></span> <span data-ttu-id="48fdd-229">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="48fdd-229">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="48fdd-230">0: не использовать кадры B (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="48fdd-230">0: Do not use B frames (default).</span></span></li>
<li><span data-ttu-id="48fdd-231">1. Используйте один кадр B.</span><span class="sxs-lookup"><span data-stu-id="48fdd-231">1: Use one B frame.</span></span></li>
<li><span data-ttu-id="48fdd-232">2: используйте два кадра B.</span><span class="sxs-lookup"><span data-stu-id="48fdd-232">2: Use two B frames.</span></span></li>
</ul>
<span data-ttu-id="48fdd-233">Чтобы задать этот параметр, задайте свойство перед вызовом <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>имфтрансформ:: сетаутпуттипе</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-233">To set this parameter, set the property before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform::SetOutputType</strong></a>.</span></span> <br/> <span data-ttu-id="48fdd-234">Для базового профиля число кадров B всегда равно нулю.</span><span class="sxs-lookup"><span data-stu-id="48fdd-234">For Baseline profile, the number of B frames is always zero.</span></span> <span data-ttu-id="48fdd-235">Кодировщик будет переопределять ненулевые значения.</span><span class="sxs-lookup"><span data-stu-id="48fdd-235">The encoder will override nonzero values.</span></span><br/> <span data-ttu-id="48fdd-236">Для других профилей H. 264, если это свойство не равно нулю, шаблон кодировки — ИББПББП, где максимальное число последовательных кадров B равно <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-236">For other H.264 profiles, if this property is nonzero, the encoding pattern is IBBPBBP, where the maximum number of consecutive B frames is equal to <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="48fdd-238">Задает число изображений из одного заголовка GOP к следующему, включая начальную привязку, но не следующую.</span><span class="sxs-lookup"><span data-stu-id="48fdd-238">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="48fdd-239">Допустимый диапазон: [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="48fdd-239">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="48fdd-240">Если значение равно нулю, кодировщик выбирает размер GOP.</span><span class="sxs-lookup"><span data-stu-id="48fdd-240">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="48fdd-241">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="48fdd-241">The default value is zero.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="48fdd-243">Задает число рабочих потоков, используемых кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="48fdd-243">Sets the number of worker threads used by a encoder.</span></span><br/> <span data-ttu-id="48fdd-244">Допустимый диапазон — 0 – 16.</span><span class="sxs-lookup"><span data-stu-id="48fdd-244">The valid range is 0–16.</span></span> <span data-ttu-id="48fdd-245">Если значение равно нулю, кодировщик выбирает число потоков.</span><span class="sxs-lookup"><span data-stu-id="48fdd-245">If zero, the encoder selects the number of threads.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span></span></td>
<td><span data-ttu-id="48fdd-247">Указывает тип видеосодержимого.</span><span class="sxs-lookup"><span data-stu-id="48fdd-247">Indicates the type of video content.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="48fdd-249">Допустимый диапазон: 16 – 51.</span><span class="sxs-lookup"><span data-stu-id="48fdd-249">Valid range: 16–51.</span></span> <span data-ttu-id="48fdd-250">Значение по умолчанию — 24.</span><span class="sxs-lookup"><span data-stu-id="48fdd-250">The default value is 24.</span></span> <br/> <span data-ttu-id="48fdd-251">Это свойство применяется, когда режим управления скоростью <strong>eAVEncCommonRateControlMode_Quality</strong>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-251">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="48fdd-252">Это свойство настраивает тот же параметр кодировки, что и <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>авенккоммонкуалити</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="48fdd-252">This property configures the same encoding setting as <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span></span> <span data-ttu-id="48fdd-253">Однако <a href="codecapi-avencvideoencodeqp.md">авенквидеоенкодекп</a> позволяет приложению напрямую ЗАДАВАТЬ значение QP.</span><span class="sxs-lookup"><span data-stu-id="48fdd-253">However, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> enables the application to specify the value of QP directly.</span></span> <span data-ttu-id="48fdd-254">Если заданы оба свойства, Авенквидеоенкодекп переопределяет.</span><span class="sxs-lookup"><span data-stu-id="48fdd-254">If both properties are set, AVEncVideoEncodeQP overrides.</span></span> <br/> <span data-ttu-id="48fdd-255">Значение по умолчанию, равное 24, соответствует значению по умолчанию 70 для параметра <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>авенккоммонкуалити</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="48fdd-255">The default value of 24 corresponds to the default value of 70 for the <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="48fdd-257">Заставляет кодировщик кодировать следующий кадр как ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="48fdd-257">Forces the encoder to code the next frame as a key frame.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48fdd-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="48fdd-259">Допустимый диапазон: 0 – 51.</span><span class="sxs-lookup"><span data-stu-id="48fdd-259">Valid range: 0–51.</span></span> <span data-ttu-id="48fdd-260">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="48fdd-260">The default value is 0.</span></span> <br/> <span data-ttu-id="48fdd-261">Это свойство применяется ко всем режимам управления скоростью.</span><span class="sxs-lookup"><span data-stu-id="48fdd-261">This property applies to all rate control modes.</span></span> <span data-ttu-id="48fdd-262">Кодировщик не должен создавать значение QP ниже, чем указано в свойстве <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .</span><span class="sxs-lookup"><span data-stu-id="48fdd-262">The encoder should not produce a QP value lower than what is specified by the <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48fdd-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="48fdd-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="48fdd-264">Включает или отключает режим низкой задержки.</span><span class="sxs-lookup"><span data-stu-id="48fdd-264">Enables or disables low-latency mode.</span></span> <span data-ttu-id="48fdd-265">См &quot; . раздел о многопоточности &quot; в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="48fdd-265">See &quot;Multithreading&quot; in the Remarks section.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="48fdd-266">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48fdd-266">Remarks</span></span>

<span data-ttu-id="48fdd-267">Кодировщик поддерживает следующие режимы управления скоростью.</span><span class="sxs-lookup"><span data-stu-id="48fdd-267">The encoder supports the following rate control modes.</span></span>



| <span data-ttu-id="48fdd-268">Режим</span><span class="sxs-lookup"><span data-stu-id="48fdd-268">Mode</span></span>                                  | <span data-ttu-id="48fdd-269">Константа</span><span class="sxs-lookup"><span data-stu-id="48fdd-269">Constant</span></span>                                            | <span data-ttu-id="48fdd-270">Описание</span><span class="sxs-lookup"><span data-stu-id="48fdd-270">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48fdd-271">Постоянная скорость (CBR)</span><span class="sxs-lookup"><span data-stu-id="48fdd-271">Constant bit rate (CBR)</span></span>               | <span data-ttu-id="48fdd-272">**eAVEncCommonRateControlMode_CBR**</span><span class="sxs-lookup"><span data-stu-id="48fdd-272">**eAVEncCommonRateControlMode_CBR**</span></span>                | <span data-ttu-id="48fdd-273">Кодировщик пытается достичь постоянной скорости потока, используя модель "сегмент утечки".</span><span class="sxs-lookup"><span data-stu-id="48fdd-273">The encoder tries to achieve a constant bit rate, using a "leaky bucket" model.</span></span> <span data-ttu-id="48fdd-274">Целевая скорость потока задается свойством [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="48fdd-274">The target bit rate is given by the [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="48fdd-275">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="48fdd-275">Requires Windows 8.</span></span> <br/> |
| <span data-ttu-id="48fdd-276">Переменная с ограничением скорости (VBR)</span><span class="sxs-lookup"><span data-stu-id="48fdd-276">Constrained variable bit rate (VBR)</span></span>   | <span data-ttu-id="48fdd-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="48fdd-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span></span> | <span data-ttu-id="48fdd-278">Кодировщик использует модель "сегмент утечки" с пиковой скоростью.</span><span class="sxs-lookup"><span data-stu-id="48fdd-278">The encoder uses a "leaky bucket" model with a peak bit rate.</span></span> <span data-ttu-id="48fdd-279">Скорость очистки для сегмента утечки задается свойством [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="48fdd-279">The drain rate for the leaky bucket is given by the [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="48fdd-280">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="48fdd-280">Requires Windows 8.</span></span> <br/>     |
| <span data-ttu-id="48fdd-281">Битовая скорость переменной на основе качества (VBR)</span><span class="sxs-lookup"><span data-stu-id="48fdd-281">Quality-based variable bit rate (VBR)</span></span> | <span data-ttu-id="48fdd-282">**eAVEncCommonRateControlMode_Quality**</span><span class="sxs-lookup"><span data-stu-id="48fdd-282">**eAVEncCommonRateControlMode_Quality**</span></span>            | <span data-ttu-id="48fdd-283">Кодировщик пытается достичь постоянного уровня качества, заданного свойством [**авенккоммонкуалити**](../directshow/avenccommonquality-property.md) .</span><span class="sxs-lookup"><span data-stu-id="48fdd-283">The encoder tries to achieve a constant quality level, given by the [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) property.</span></span>                                                                                                           |
| <span data-ttu-id="48fdd-284">Неограниченная VBR</span><span class="sxs-lookup"><span data-stu-id="48fdd-284">Unconstrained VBR</span></span>                     | <span data-ttu-id="48fdd-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="48fdd-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span></span>   | <span data-ttu-id="48fdd-286">Кодировщик пытается достичь скорости назначения, заданной атрибутом [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) в выходном типе носителя.</span><span class="sxs-lookup"><span data-stu-id="48fdd-286">The encoder tries to achieve the target bitrate given by the [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute in the output media type.</span></span> <span data-ttu-id="48fdd-287">Это режим по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="48fdd-287">This is the default mode.</span></span>                                                              |



 

<span data-ttu-id="48fdd-288">Для CBR и режима с ограничением VBR требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="48fdd-288">CBR and constrained VBR modes require Windows 8.</span></span>

<span data-ttu-id="48fdd-289">В Windows 8 кодировщик устанавливает следующие атрибуты в выходных данных:</span><span class="sxs-lookup"><span data-stu-id="48fdd-289">In Windows 8, the encoder sets the following attributes on the output samples:</span></span>

-   [<span data-ttu-id="48fdd-290">MFSampleExtension_DecodeTimestamp</span><span class="sxs-lookup"><span data-stu-id="48fdd-290">MFSampleExtension_DecodeTimestamp</span></span>](mfsampleextension-decodetimestamp.md)
-   [<span data-ttu-id="48fdd-291">MFSampleExtension_VideoEncodePictureType</span><span class="sxs-lookup"><span data-stu-id="48fdd-291">MFSampleExtension_VideoEncodePictureType</span></span>](mfsampleextension-videoencodepicturetype.md)
-   [<span data-ttu-id="48fdd-292">MFSampleExtension_VideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="48fdd-292">MFSampleExtension_VideoEncodeQP</span></span>](mfsampleextension-videoencodeqp.md)

> [!Note]  
> <span data-ttu-id="48fdd-293">Предыдущая версия документации неправильно объявила, что кодировщик поддерживается в Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="48fdd-293">A previous version of the documentation incorrectly stated that the encoder is supported on Windows Server 2008 R2.</span></span>

 

### <a name="multithreading"></a><span data-ttu-id="48fdd-294">Многопоточность</span><span class="sxs-lookup"><span data-stu-id="48fdd-294">Multithreading</span></span>

<span data-ttu-id="48fdd-295">В Windows 8 кодировщик поддерживает два режима кодирования:</span><span class="sxs-lookup"><span data-stu-id="48fdd-295">In Windows 8, the encoder supports two encoding modes:</span></span>

-   <span data-ttu-id="48fdd-296">**Кодирование фрагмента.**</span><span class="sxs-lookup"><span data-stu-id="48fdd-296">**Slice encoding.**</span></span> <span data-ttu-id="48fdd-297">В этом режиме срезы кодируются параллельно.</span><span class="sxs-lookup"><span data-stu-id="48fdd-297">In this mode, slices are encoded in parallel.</span></span> <span data-ttu-id="48fdd-298">Каждый срез кодируется в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="48fdd-298">Each slice is encoded on a different thread.</span></span> <span data-ttu-id="48fdd-299">Этот режим имеет низкую задержку, так как один рисунок кодируется параллельно.</span><span class="sxs-lookup"><span data-stu-id="48fdd-299">This mode has low latency, because a single picture is encoded in parallel.</span></span> <span data-ttu-id="48fdd-300">Однако этот подход не масштабируется по мере увеличения числа ядер, так как количество срезов ограничено количеством макроблокк строк во входном изображении.</span><span class="sxs-lookup"><span data-stu-id="48fdd-300">However, this approach does not scale as the number of cores increases, because the number of slices is bounded by the number of macroblock rows in the input picture.</span></span>
-   <span data-ttu-id="48fdd-301">**Многокадровая кодировка.**</span><span class="sxs-lookup"><span data-stu-id="48fdd-301">**Multi-frame encoding.**</span></span> <span data-ttu-id="48fdd-302">В этом режиме кодировщик принимает несколько кадров входных данных и кодирует их параллельно.</span><span class="sxs-lookup"><span data-stu-id="48fdd-302">In this mode, the encoder accepts multiple frames of input and encodes them in parallel.</span></span> <span data-ttu-id="48fdd-303">Этот режим лучше масштабируется в многоядерной среде, но в нем появились дополнительные задержки.</span><span class="sxs-lookup"><span data-stu-id="48fdd-303">This mode scales better in a multicore environment, but introduces more latency.</span></span>

<span data-ttu-id="48fdd-304">Кодировщик по умолчанию кодирует кодирование, чтобы максимально сокращать задержку.</span><span class="sxs-lookup"><span data-stu-id="48fdd-304">The encoder defaults to slice encoding, to minimize latency.</span></span> <span data-ttu-id="48fdd-305">Чтобы включить многокадровое кодирование, задайте для свойства [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) значение **VARIANT_FALSE**.</span><span class="sxs-lookup"><span data-stu-id="48fdd-305">To enable multi-frame encoding, set the [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) property to **VARIANT_FALSE**.</span></span>

<span data-ttu-id="48fdd-306">Чтобы задать число рабочих потоков, используемых кодировщиком, задайте свойство [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="48fdd-306">To set the number of worker threads used by the encoder, set the [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) property.</span></span>

<span data-ttu-id="48fdd-307">В Windows 7 кодировщик всегда использует кодирование среза.</span><span class="sxs-lookup"><span data-stu-id="48fdd-307">In Windows 7, the encoder always uses slice encoding.</span></span>

### <a name="certified-hardware-encoder"></a><span data-ttu-id="48fdd-308">Сертифицированный аппаратный кодировщик</span><span class="sxs-lookup"><span data-stu-id="48fdd-308">Certified Hardware Encoder</span></span>

<span data-ttu-id="48fdd-309">Если имеется сертифицированный аппаратный кодировщик, он обычно используется вместо кодировщика системы входящей почты для Media Foundation связанных сценариев.</span><span class="sxs-lookup"><span data-stu-id="48fdd-309">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="48fdd-310">Сертифицированные кодировщики требуются для поддержки определенного набора свойств **икодекапи** и могут дополнительно поддерживать другой набор свойств.</span><span class="sxs-lookup"><span data-stu-id="48fdd-310">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="48fdd-311">Процесс сертификации должен гарантировать, что требуемые свойства должным образом поддерживались, и, если необязательное свойство поддерживается, оно также должно поддерживаться надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="48fdd-311">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="48fdd-312">Ниже приведен набор обязательных и необязательных свойств **икодекапи** для кодировщиков, которые проходят сертификацию кодировщика ХКК.</span><span class="sxs-lookup"><span data-stu-id="48fdd-312">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

<span data-ttu-id="48fdd-313">Следующие свойства **икодекапи** для Windows 8 и Windows 8.1 являются обязательными:</span><span class="sxs-lookup"><span data-stu-id="48fdd-313">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are required:</span></span>

-   [<span data-ttu-id="48fdd-314">CODECAPI_AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="48fdd-314">CODECAPI_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="48fdd-315">CODECAPI_AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="48fdd-315">CODECAPI_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="48fdd-316">CODECAPI_AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="48fdd-316">CODECAPI_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="48fdd-317">CODECAPI_AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="48fdd-317">CODECAPI_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="48fdd-318">CODECAPI_AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="48fdd-318">CODECAPI_AVEncCommonMaxBitRate</span></span>](../directshow/avenccommonmaxbitrate-property.md)
-   [<span data-ttu-id="48fdd-319">CODECAPI_AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="48fdd-319">CODECAPI_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="48fdd-320">CODECAPI_AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="48fdd-320">CODECAPI_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="48fdd-321">CODECAPI_AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="48fdd-321">CODECAPI_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="48fdd-322">CODECAPI_AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="48fdd-322">CODECAPI_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

<span data-ttu-id="48fdd-323">Следующие свойства Windows 8.1 **икодекапи** являются необязательными, но проверяются в ХКК, если они поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="48fdd-323">The following Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   [<span data-ttu-id="48fdd-324">CODECAPI_AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="48fdd-324">CODECAPI_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
-   [<span data-ttu-id="48fdd-325">CODECAPI_AVEncVideoLTRBufferControl</span><span class="sxs-lookup"><span data-stu-id="48fdd-325">CODECAPI_AVEncVideoLTRBufferControl</span></span>](codecapi-avencvideoltrbuffercontrol.md)
-   [<span data-ttu-id="48fdd-326">CODECAPI_AVEncVideoMarkLTRFrame</span><span class="sxs-lookup"><span data-stu-id="48fdd-326">CODECAPI_AVEncVideoMarkLTRFrame</span></span>](codecapi-avencvideomarkltrframe.md)
-   [<span data-ttu-id="48fdd-327">CODECAPI_AVEncVideoUseLTRFrame</span><span class="sxs-lookup"><span data-stu-id="48fdd-327">CODECAPI_AVEncVideoUseLTRFrame</span></span>](codecapi-avencvideouseltrframe.md)
-   [<span data-ttu-id="48fdd-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span><span class="sxs-lookup"><span data-stu-id="48fdd-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span></span>](codecapi-avencvideoencodeframetypeqp.md)
-   [<span data-ttu-id="48fdd-329">CODECAPI_AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="48fdd-329">CODECAPI_AVEncSliceControlMode</span></span>](codecapi-avencslicecontrolmode.md)
-   [<span data-ttu-id="48fdd-330">CODECAPI_AVEncSliceControlSize</span><span class="sxs-lookup"><span data-stu-id="48fdd-330">CODECAPI_AVEncSliceControlSize</span></span>](codecapi-avencslicecontrolsize.md)
-   [<span data-ttu-id="48fdd-331">CODECAPI_AVEncVideoMaxNumRefFrame</span><span class="sxs-lookup"><span data-stu-id="48fdd-331">CODECAPI_AVEncVideoMaxNumRefFrame</span></span>](codecapi-avencvideomaxnumrefframe.md)
-   [<span data-ttu-id="48fdd-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span><span class="sxs-lookup"><span data-stu-id="48fdd-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span></span>](codecapi-avencvideomeanabsolutedifference.md)
-   [<span data-ttu-id="48fdd-333">CODECAPI_AVEncVideoMaxQP</span><span class="sxs-lookup"><span data-stu-id="48fdd-333">CODECAPI_AVEncVideoMaxQP</span></span>](codecapi-avencvideomaxqp.md)
-   [<span data-ttu-id="48fdd-334">CODECAPI_AVEncVideoROIEnabled</span><span class="sxs-lookup"><span data-stu-id="48fdd-334">CODECAPI_AVEncVideoROIEnabled</span></span>](codecapi-avencvideoroienabled.md)
-   <span data-ttu-id="48fdd-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (динамический)</span><span class="sxs-lookup"><span data-stu-id="48fdd-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Dynamic)</span></span>
-   [<span data-ttu-id="48fdd-336">CODECAPI_AVEncH264CABACEnable</span><span class="sxs-lookup"><span data-stu-id="48fdd-336">CODECAPI_AVEncH264CABACEnable</span></span>](codecapi-avench264cabacenable.md)

<span data-ttu-id="48fdd-337">Следующие свойства **икодекапи** для Windows 8 и Windows 8.1 являются необязательными, но проверяются в ХКК, если они поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="48fdd-337">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   <span data-ttu-id="48fdd-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (статический)</span><span class="sxs-lookup"><span data-stu-id="48fdd-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Static)</span></span>
-   [<span data-ttu-id="48fdd-339">CODECAPI_AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="48fdd-339">CODECAPI_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

<span data-ttu-id="48fdd-340">Следующие свойства **икодекапи** являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="48fdd-340">The following **ICodecAPI** properties are optional.</span></span> <span data-ttu-id="48fdd-341">Они не проверяются в ХКК.</span><span class="sxs-lookup"><span data-stu-id="48fdd-341">They are not tested in HCK.</span></span>

-   [<span data-ttu-id="48fdd-342">CODECAPI_AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="48fdd-342">CODECAPI_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a><span data-ttu-id="48fdd-343">Требования</span><span class="sxs-lookup"><span data-stu-id="48fdd-343">Requirements</span></span>



| <span data-ttu-id="48fdd-344">Требование</span><span class="sxs-lookup"><span data-stu-id="48fdd-344">Requirement</span></span> | <span data-ttu-id="48fdd-345">Значение</span><span class="sxs-lookup"><span data-stu-id="48fdd-345">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48fdd-346">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48fdd-346">Minimum supported client</span></span><br/> | <span data-ttu-id="48fdd-347">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="48fdd-347">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="48fdd-348">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48fdd-348">Minimum supported server</span></span><br/> | <span data-ttu-id="48fdd-349">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="48fdd-349">None supported</span></span><br/>                                                                |
| <span data-ttu-id="48fdd-350">DLL</span><span class="sxs-lookup"><span data-stu-id="48fdd-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48fdd-351"><dt>Mfh264enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48fdd-351"><dt>Mfh264enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48fdd-352">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48fdd-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48fdd-353">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="48fdd-353">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="48fdd-354">Поддержка MPEG-4 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="48fdd-354">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="48fdd-355">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="48fdd-355">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="48fdd-356">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="48fdd-356">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
