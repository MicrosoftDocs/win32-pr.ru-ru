---
description: Кодировщик видео Media Foundation H. 265 — это Media Foundation преобразование, которое поддерживает кодирование содержимого в формат H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: H. 265/HEVC видео Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991380"
---
# <a name="h265--hevc-video-encoder"></a><span data-ttu-id="fc399-103">H. 265/HEVC видео Encoder</span><span class="sxs-lookup"><span data-stu-id="fc399-103">H.265 / HEVC Video Encoder</span></span>

<span data-ttu-id="fc399-104">Кодировщик видео Media Foundation H. 265 — это [Media Foundation преобразование](media-foundation-transforms.md) , которое поддерживает кодирование содержимого в формат H. 265/HEVC.</span><span class="sxs-lookup"><span data-stu-id="fc399-104">The Media Foundation H.265 video encoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports encoding content into the H.265/HEVC format.</span></span> <span data-ttu-id="fc399-105">Кодировщик поддерживает следующие профили:</span><span class="sxs-lookup"><span data-stu-id="fc399-105">The encoder supports the following profiles:</span></span>

-   <span data-ttu-id="fc399-106">Профиль Main</span><span class="sxs-lookup"><span data-stu-id="fc399-106">Main Profile</span></span>

<span data-ttu-id="fc399-107">Кодировщик видео H. 265 предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="fc399-107">The H.265 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="fc399-108">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="fc399-108">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="fc399-109">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="fc399-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="fc399-110">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="fc399-110">Input Types</span></span>

<span data-ttu-id="fc399-111">Входной тип носителя должен иметь один из следующих подтипов:</span><span class="sxs-lookup"><span data-stu-id="fc399-111">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="fc399-112">**Мфвидеоформат \_ ийув**</span><span class="sxs-lookup"><span data-stu-id="fc399-112">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="fc399-113">**Мфвидеоформат \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="fc399-113">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="fc399-114">**Мфвидеоформат \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="fc399-114">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="fc399-115">**Мфвидеоформат \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="fc399-115">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="fc399-116">Дополнительные сведения об этих подтипах см. в разделе [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="fc399-116">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="fc399-117">Тип выходных данных должен быть задан перед входным типом.</span><span class="sxs-lookup"><span data-stu-id="fc399-117">The output type must be set before the input type.</span></span> <span data-ttu-id="fc399-118">Пока тип выходных данных не задан, метод [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) кодировщика возвращает **\_ \_ \_ \_ не \_ установленный тип преобразования MF E**.</span><span class="sxs-lookup"><span data-stu-id="fc399-118">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="fc399-119">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="fc399-119">Output Types</span></span>

<span data-ttu-id="fc399-120">Кодировщик поддерживает один выходной подтип:</span><span class="sxs-lookup"><span data-stu-id="fc399-120">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="fc399-121">**Мфвидеоформат \_ H265**</span><span class="sxs-lookup"><span data-stu-id="fc399-121">**MFVideoFormat\_H265**</span></span>

<span data-ttu-id="fc399-122">Задайте следующие атрибуты для выходного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="fc399-122">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc399-123">attribute</span><span class="sxs-lookup"><span data-stu-id="fc399-123">Attribute</span></span></th>
<th><span data-ttu-id="fc399-124">Описание</span><span class="sxs-lookup"><span data-stu-id="fc399-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc399-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc399-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="fc399-126">Основной тип.</span><span class="sxs-lookup"><span data-stu-id="fc399-126">Major type.</span></span> <span data-ttu-id="fc399-127">Необходимо <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc399-127">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc399-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="fc399-129">Подтип видео.</span><span class="sxs-lookup"><span data-stu-id="fc399-129">Video subtype.</span></span> <span data-ttu-id="fc399-130">Необходимо <strong>MFVideoFormat_HEVC</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc399-130">Must be <strong>MFVideoFormat_HEVC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc399-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="fc399-132">Средняя скорость кодирования (бит в секунду).</span><span class="sxs-lookup"><span data-stu-id="fc399-132">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="fc399-133">Должен быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="fc399-133">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc399-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="fc399-135">Частота кадров.</span><span class="sxs-lookup"><span data-stu-id="fc399-135">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc399-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="fc399-137">Размер кадра.</span><span class="sxs-lookup"><span data-stu-id="fc399-137">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc399-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="fc399-139">Режим чередования.</span><span class="sxs-lookup"><span data-stu-id="fc399-139">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span><span class="sxs-lookup"><span data-stu-id="fc399-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span></span></td>
<td><span data-ttu-id="fc399-141">Профиль кодирования H. 265.</span><span class="sxs-lookup"><span data-stu-id="fc399-141">H.265 encoding profile.</span></span><br/> <span data-ttu-id="fc399-142">Поддерживаются такие значения:</span><span class="sxs-lookup"><span data-stu-id="fc399-142">The supported values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="fc399-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span><span class="sxs-lookup"><span data-stu-id="fc399-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc399-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="fc399-145">Задает уровень закодированного видео.</span><span class="sxs-lookup"><span data-stu-id="fc399-145">Specifies the level of the coded video.</span></span> <span data-ttu-id="fc399-146">Дополнительные сведения об ограничениях профиля и уровня см. в приложении A из ITU-T H. 265.</span><span class="sxs-lookup"><span data-stu-id="fc399-146">For more information about profile and level constraints, refer to Annex A of ITU-T H.265.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc399-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="fc399-148">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fc399-148">Optional.</span></span> <span data-ttu-id="fc399-149">Задает пропорцию в пикселях.</span><span class="sxs-lookup"><span data-stu-id="fc399-149">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="fc399-150">Значение по умолчанию — 1:1.</span><span class="sxs-lookup"><span data-stu-id="fc399-150">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fc399-151">После установки типа выходных данных кодировщик видео обновляет тип, добавляя атрибут [**\_ \_ \_ \_ заголовка последовательностей MF MT MPEG**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="fc399-151">After the output type is set, the video encoder updates the type by adding the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="fc399-152">Этот атрибут содержит заголовок последовательности.</span><span class="sxs-lookup"><span data-stu-id="fc399-152">This attribute contains the sequence header.</span></span>

## <a name="supported-imftransform-methods"></a><span data-ttu-id="fc399-153">Поддерживаемые методы Имфтрансформ</span><span class="sxs-lookup"><span data-stu-id="fc399-153">Supported IMFTransform methods</span></span>

<span data-ttu-id="fc399-154">Для кодировщика H. 265/HEVC поддерживаются следующие методы интерфейса [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) :</span><span class="sxs-lookup"><span data-stu-id="fc399-154">The following methods of the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="fc399-155">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="fc399-155">**GetAttributes**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [<span data-ttu-id="fc399-156">**жетинпутаваилаблетипе**</span><span class="sxs-lookup"><span data-stu-id="fc399-156">**GetInputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [<span data-ttu-id="fc399-157">**жетинпуткурренттипе**</span><span class="sxs-lookup"><span data-stu-id="fc399-157">**GetInputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [<span data-ttu-id="fc399-158">**жетинпутстатус**</span><span class="sxs-lookup"><span data-stu-id="fc399-158">**GetInputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [<span data-ttu-id="fc399-159">**жетинпутстреаминфо**</span><span class="sxs-lookup"><span data-stu-id="fc399-159">**GetInputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [<span data-ttu-id="fc399-160">**жетаутпутаваилаблетипе**</span><span class="sxs-lookup"><span data-stu-id="fc399-160">**GetOutputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [<span data-ttu-id="fc399-161">**жетаутпуткурренттипе**</span><span class="sxs-lookup"><span data-stu-id="fc399-161">**GetOutputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [<span data-ttu-id="fc399-162">**жетаутпутстатус**</span><span class="sxs-lookup"><span data-stu-id="fc399-162">**GetOutputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [<span data-ttu-id="fc399-163">**жетаутпутстреаминфо**</span><span class="sxs-lookup"><span data-stu-id="fc399-163">**GetOutputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [<span data-ttu-id="fc399-164">**жетстреамкаунт**</span><span class="sxs-lookup"><span data-stu-id="fc399-164">**GetStreamCount**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [<span data-ttu-id="fc399-165">**жетстреамлимитс**</span><span class="sxs-lookup"><span data-stu-id="fc399-165">**GetStreamLimits**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [<span data-ttu-id="fc399-166">**процессевент**</span><span class="sxs-lookup"><span data-stu-id="fc399-166">**ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [<span data-ttu-id="fc399-167">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="fc399-167">**ProcessMessage**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [<span data-ttu-id="fc399-168">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="fc399-168">**ProcessInput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [<span data-ttu-id="fc399-169">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="fc399-169">**ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [<span data-ttu-id="fc399-170">**сетинпуттипе**</span><span class="sxs-lookup"><span data-stu-id="fc399-170">**SetInputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [<span data-ttu-id="fc399-171">**сетаутпуттипе**</span><span class="sxs-lookup"><span data-stu-id="fc399-171">**SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [<span data-ttu-id="fc399-172">**сетаутпутбаундс**</span><span class="sxs-lookup"><span data-stu-id="fc399-172">**SetOutputBounds**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

<span data-ttu-id="fc399-173">Все остальные методы [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) будут возвращать ошибку E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="fc399-173">All other [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods will return the error E\_NOTIMPL.</span></span>

## <a name="supported-icodecapi-methods"></a><span data-ttu-id="fc399-174">Поддерживаемые методы Икодекапи</span><span class="sxs-lookup"><span data-stu-id="fc399-174">Supported ICodecAPI methods</span></span>

<span data-ttu-id="fc399-175">Для кодировщика H. 265/HEVC поддерживаются следующие методы интерфейса [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="fc399-175">The following methods of the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="fc399-176">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="fc399-176">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="fc399-177">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="fc399-177">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [<span data-ttu-id="fc399-178">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="fc399-178">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="fc399-179">**жетпараметерранже**</span><span class="sxs-lookup"><span data-stu-id="fc399-179">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="fc399-180">**жетпараметервалуес**</span><span class="sxs-lookup"><span data-stu-id="fc399-180">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

<span data-ttu-id="fc399-181">Все остальные методы [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) будут возвращать ошибку E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="fc399-181">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods will return the error E\_NOTIMPL.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="fc399-182">Свойства кодека</span><span class="sxs-lookup"><span data-stu-id="fc399-182">Codec Properties</span></span>

<span data-ttu-id="fc399-183">Кодировщик H. 265 реализует интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) для установки параметров кодирования.</span><span class="sxs-lookup"><span data-stu-id="fc399-183">The H.265 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="fc399-184">Он поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="fc399-184">It supports the following properties.</span></span>

<span data-ttu-id="fc399-185">Требования к кодеку для ХКК кодировщика см. в разделе " **сертифицированный аппаратный кодировщик** " ниже.</span><span class="sxs-lookup"><span data-stu-id="fc399-185">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc399-186">Свойство</span><span class="sxs-lookup"><span data-stu-id="fc399-186">Property</span></span></th>
<th><span data-ttu-id="fc399-187">Описание</span><span class="sxs-lookup"><span data-stu-id="fc399-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc399-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc399-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span></span></td>
<td><span data-ttu-id="fc399-189">Задает режим управления скоростью.</span><span class="sxs-lookup"><span data-stu-id="fc399-189">Sets the rate control mode.</span></span> <span data-ttu-id="fc399-190">Ниже приведены поддерживаемые режимы.</span><span class="sxs-lookup"><span data-stu-id="fc399-190">The supported modes are:</span></span><br/>
<ul>
<li><span data-ttu-id="fc399-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span><span class="sxs-lookup"><span data-stu-id="fc399-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span></span></li>
<li><span data-ttu-id="fc399-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span><span class="sxs-lookup"><span data-stu-id="fc399-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span></span></li>
</ul>
<span data-ttu-id="fc399-193">Если указаны другие режимы, будет использоваться контроль скорости <strong>eAVEncCommonRateControlMode_CBR</strong> .</span><span class="sxs-lookup"><span data-stu-id="fc399-193">If other modes are specified, the <strong>eAVEncCommonRateControlMode_CBR</strong> rate control will be used.</span></span><br/> <span data-ttu-id="fc399-194">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-194">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="fc399-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="fc399-196">Задает среднюю скорость потока в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="fc399-196">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <br/> <span data-ttu-id="fc399-197">Допустимый диапазон: [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="fc399-197">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="fc399-198">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-198">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="fc399-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="fc399-200">Задает размер буфера (в байтах) для кодирования с постоянной скоростью (CBR).</span><span class="sxs-lookup"><span data-stu-id="fc399-200">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="fc399-201">Допустимый диапазон: [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="fc399-201">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="fc399-202">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-202">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="fc399-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="fc399-204">Задает максимальную скорость для режимов управления скоростью, которая обеспечивает пиковую скорость.</span><span class="sxs-lookup"><span data-stu-id="fc399-204">Sets the maximum bitrate for rate control modes that allow a peak bitrate.</span></span> <br/> <span data-ttu-id="fc399-205">Допустимый диапазон: [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="fc399-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="fc399-206">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-206">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="fc399-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="fc399-208">Задает число изображений из одного заголовка GOP к следующему, включая начальную привязку, но не следующую.</span><span class="sxs-lookup"><span data-stu-id="fc399-208">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="fc399-209">Допустимый диапазон: [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="fc399-209">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="fc399-210">Если значение равно нулю, кодировщик выбирает размер GOP.</span><span class="sxs-lookup"><span data-stu-id="fc399-210">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="fc399-211">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fc399-211">The default value is zero.</span></span> <br/> <span data-ttu-id="fc399-212">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-212">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="fc399-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="fc399-214">Включает или отключает режим низкой задержки.</span><span class="sxs-lookup"><span data-stu-id="fc399-214">Enables or disables low-latency mode.</span></span> <br/> <span data-ttu-id="fc399-215">Это VT_BOOL значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-215">This is a VT_BOOL value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="fc399-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="fc399-217">Задает компромисс качества и скорости.</span><span class="sxs-lookup"><span data-stu-id="fc399-217">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="fc399-218">Это значение влияет на то, как кодировщик выполняет различные операции кодирования, такие как компенсация движения.</span><span class="sxs-lookup"><span data-stu-id="fc399-218">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="fc399-219">На более высоких уровнях сложности кодировщик работает медленнее, но обеспечивает лучшее качество с той же скоростью.</span><span class="sxs-lookup"><span data-stu-id="fc399-219">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span> <br/> <span data-ttu-id="fc399-220">Допустимый диапазон: 0 – 100.</span><span class="sxs-lookup"><span data-stu-id="fc399-220">The valid range is 0 – 100.</span></span> <span data-ttu-id="fc399-221">На внутреннем уровне это значение сопоставляется с небольшим набором уровней качества и скорости, поддерживаемых кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="fc399-221">Internally, this value is mapped to a smaller set of quality/speed levels supported by the encoder.</span></span><br/> <span data-ttu-id="fc399-222">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-222">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="fc399-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="fc399-224">Заставляет кодировщик кодировать следующий кадр как ключевой кадр.</span><span class="sxs-lookup"><span data-stu-id="fc399-224">Forces the encoder to code the next frame as a key frame.</span></span><br/> <span data-ttu-id="fc399-225">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-225">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="fc399-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="fc399-227">Если это свойство задано, кодировщик будет использовать указанный обработчик запросов для кодирования следующего кадра и всех последующих кадров до тех пор, пока не будет указан новый элемент QP.</span><span class="sxs-lookup"><span data-stu-id="fc399-227">When this property is set it will cause the encoder to use the specified QP to encode the next frame and all subsequent frames until a new QP is specified.</span></span> <br/> <span data-ttu-id="fc399-228">Допустимый диапазон: 0 – 51, включительно</span><span class="sxs-lookup"><span data-stu-id="fc399-228">Valid range: 0–51, inclusive</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="fc399-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="fc399-230">Это свойство установит ограничение на минимальное количество запросов, которое кодировщик может использовать во время CBR ратеконтрол.</span><span class="sxs-lookup"><span data-stu-id="fc399-230">This property will set a limit on the minimum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="fc399-231">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-231">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span><span class="sxs-lookup"><span data-stu-id="fc399-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span></span></td>
<td><span data-ttu-id="fc399-233">Это свойство установит ограничение на максимальное количество запросов на использование, которое кодировщик может использовать во время CBR ратеконтрол.</span><span class="sxs-lookup"><span data-stu-id="fc399-233">This property will set a limit on the maximum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="fc399-234">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-234">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc399-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span><span class="sxs-lookup"><span data-stu-id="fc399-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span></span></td>
<td><span data-ttu-id="fc399-236">Определяет, является ли содержимое полноэкранным, в отличие от содержимого экрана, которое может иметь меньшее окно видео или вообще не иметь видео.</span><span class="sxs-lookup"><span data-stu-id="fc399-236">Sets whether the content is full-screen video, as opposed to screen content that might have a smaller window of video or have no video at all.</span></span><br/> <span data-ttu-id="fc399-237">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-237">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc399-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="fc399-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="fc399-239">Задает число потоков, используемых для выполнения операции сжатия.</span><span class="sxs-lookup"><span data-stu-id="fc399-239">Sets the number of threads used to perform the compression operation.</span></span> <span data-ttu-id="fc399-240">Кодировщик будет разделять фрейм на плитки таким, что число потоков равно числу плиток.</span><span class="sxs-lookup"><span data-stu-id="fc399-240">The encoder will divide the frame into tiles such that the number of threads equals the number of tiles.</span></span><br/>
<ul>
<li><span data-ttu-id="fc399-241">Число логических процессоров.</span><span class="sxs-lookup"><span data-stu-id="fc399-241">The number of logical processors.</span></span> <span data-ttu-id="fc399-242">Число потоков должно быть меньше или равно числу логических процессоров.</span><span class="sxs-lookup"><span data-stu-id="fc399-242">The number of threads must be less than or equal to the number of logical processors.</span></span></li>
<li><span data-ttu-id="fc399-243">Размер рамки.</span><span class="sxs-lookup"><span data-stu-id="fc399-243">The size of the frame.</span></span> <span data-ttu-id="fc399-244">Размер плитки должен быть больше или равен 265x64 пикселей.</span><span class="sxs-lookup"><span data-stu-id="fc399-244">The size of a tile must bigger than or equal to 265x64 pixels.</span></span></li>
<li><span data-ttu-id="fc399-245">С контролем четности.</span><span class="sxs-lookup"><span data-stu-id="fc399-245">Parity.</span></span> <span data-ttu-id="fc399-246">Число потоков должно быть четным.</span><span class="sxs-lookup"><span data-stu-id="fc399-246">The number of threads must be an even value.</span></span> <span data-ttu-id="fc399-247">Если указанное значение нечетное, будет использоваться следующее меньшее четное значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-247">If the specified value is odd then the next lower even value will be used.</span></span></li>
</ul>
<span data-ttu-id="fc399-248">Это VT_UI4 значение.</span><span class="sxs-lookup"><span data-stu-id="fc399-248">This is a VT_UI4 value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a><span data-ttu-id="fc399-249">Сертифицированный аппаратный кодировщик</span><span class="sxs-lookup"><span data-stu-id="fc399-249">Certified Hardware Encoder</span></span>

<span data-ttu-id="fc399-250">Если имеется сертифицированный аппаратный кодировщик, он обычно используется вместо кодировщика системы входящей почты для Media Foundation связанных сценариев.</span><span class="sxs-lookup"><span data-stu-id="fc399-250">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="fc399-251">Сертифицированные кодировщики требуются для поддержки определенного набора свойств **икодекапи** и могут дополнительно поддерживать другой набор свойств.</span><span class="sxs-lookup"><span data-stu-id="fc399-251">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="fc399-252">Процесс сертификации должен гарантировать, что требуемые свойства должным образом поддерживались, и, если необязательное свойство поддерживается, оно также должно поддерживаться надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="fc399-252">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="fc399-253">Ниже приведен набор обязательных и необязательных свойств **икодекапи** для кодировщиков, которые проходят сертификацию кодировщика ХКК.</span><span class="sxs-lookup"><span data-stu-id="fc399-253">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

-   [<span data-ttu-id="fc399-254">КОДЕКАПИ \_ авенккоммонратеконтролмоде</span><span class="sxs-lookup"><span data-stu-id="fc399-254">CODECAPI\_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="fc399-255">КОДЕКАПИ \_ авенккоммонкуалити</span><span class="sxs-lookup"><span data-stu-id="fc399-255">CODECAPI\_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="fc399-256">КОДЕКАПИ \_ авенккоммонмеанбитрате</span><span class="sxs-lookup"><span data-stu-id="fc399-256">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="fc399-257">КОДЕКАПИ \_ авенккоммонбуфферсизе</span><span class="sxs-lookup"><span data-stu-id="fc399-257">CODECAPI\_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="fc399-258">КОДЕКАПИ \_ авенкмпвгопсизе</span><span class="sxs-lookup"><span data-stu-id="fc399-258">CODECAPI\_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="fc399-259">КОДЕКАПИ \_ авенквидеоенкодекп</span><span class="sxs-lookup"><span data-stu-id="fc399-259">CODECAPI\_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="fc399-260">КОДЕКАПИ \_ авенквидеофорцекэйфраме</span><span class="sxs-lookup"><span data-stu-id="fc399-260">CODECAPI\_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a><span data-ttu-id="fc399-261">Требования</span><span class="sxs-lookup"><span data-stu-id="fc399-261">Requirements</span></span>



| <span data-ttu-id="fc399-262">Требование</span><span class="sxs-lookup"><span data-stu-id="fc399-262">Requirement</span></span> | <span data-ttu-id="fc399-263">Значение</span><span class="sxs-lookup"><span data-stu-id="fc399-263">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc399-264">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc399-264">Minimum supported client</span></span><br/> | <span data-ttu-id="fc399-265">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fc399-265">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="fc399-266">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc399-266">Minimum supported server</span></span><br/> | <span data-ttu-id="fc399-267">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fc399-267">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fc399-268">DLL</span><span class="sxs-lookup"><span data-stu-id="fc399-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc399-269"><dt>Mfh265enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc399-269"><dt>Mfh265enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc399-270">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc399-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc399-271">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="fc399-271">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
