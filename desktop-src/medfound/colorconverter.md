---
description: Преобразует видеопоток между цветовыми форматами.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: DSP цветового преобразователя (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496833"
---
# <a name="color-converter-dsp"></a><span data-ttu-id="419d8-103">DSP цветового преобразователя</span><span class="sxs-lookup"><span data-stu-id="419d8-103">Color Converter DSP</span></span>

<span data-ttu-id="419d8-104">Преобразует видеопоток между цветовыми форматами.</span><span class="sxs-lookup"><span data-stu-id="419d8-104">Converts a video stream between color formats.</span></span>

## <a name="clsid"></a><span data-ttu-id="419d8-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="419d8-105">CLSID</span></span>

<span data-ttu-id="419d8-106">\_ККОЛОРКОНВЕРТДМО CLSID</span><span class="sxs-lookup"><span data-stu-id="419d8-106">CLSID\_CColorConvertDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="419d8-107">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="419d8-107">Interfaces</span></span>

-   [<span data-ttu-id="419d8-108">**имедиаобжект**</span><span class="sxs-lookup"><span data-stu-id="419d8-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="419d8-109">**имфреалтимеклиент**</span><span class="sxs-lookup"><span data-stu-id="419d8-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="419d8-110">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="419d8-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="419d8-111">**ипропертисторе**</span><span class="sxs-lookup"><span data-stu-id="419d8-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="419d8-112">ивмколорконвпропс</span><span class="sxs-lookup"><span data-stu-id="419d8-112">IWMColorConvProps</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a><span data-ttu-id="419d8-113">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="419d8-113">Input Formats</span></span>

-   <span data-ttu-id="419d8-114">RGB 24</span><span class="sxs-lookup"><span data-stu-id="419d8-114">RGB 24</span></span>
-   <span data-ttu-id="419d8-115">RGB 32</span><span class="sxs-lookup"><span data-stu-id="419d8-115">RGB 32</span></span>
-   <span data-ttu-id="419d8-116">RGB 555</span><span class="sxs-lookup"><span data-stu-id="419d8-116">RGB 555</span></span>
-   <span data-ttu-id="419d8-117">RGB 565</span><span class="sxs-lookup"><span data-stu-id="419d8-117">RGB 565</span></span>
-   <span data-ttu-id="419d8-118">RGB 8</span><span class="sxs-lookup"><span data-stu-id="419d8-118">RGB 8</span></span>
-   <span data-ttu-id="419d8-119">айув</span><span class="sxs-lookup"><span data-stu-id="419d8-119">AYUV</span></span>
-   <span data-ttu-id="419d8-120">I420</span><span class="sxs-lookup"><span data-stu-id="419d8-120">I420</span></span>
-   <span data-ttu-id="419d8-121">ийув</span><span class="sxs-lookup"><span data-stu-id="419d8-121">IYUV</span></span>
-   <span data-ttu-id="419d8-122">NV11</span><span class="sxs-lookup"><span data-stu-id="419d8-122">NV11</span></span>
-   <span data-ttu-id="419d8-123">NV12</span><span class="sxs-lookup"><span data-stu-id="419d8-123">NV12</span></span>
-   <span data-ttu-id="419d8-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="419d8-124">UYVY</span></span>
-   <span data-ttu-id="419d8-125">V216</span><span class="sxs-lookup"><span data-stu-id="419d8-125">V216</span></span>
-   <span data-ttu-id="419d8-126">V410</span><span class="sxs-lookup"><span data-stu-id="419d8-126">V410</span></span>
-   <span data-ttu-id="419d8-127">Y41P</span><span class="sxs-lookup"><span data-stu-id="419d8-127">Y41P</span></span>
-   <span data-ttu-id="419d8-128">Y41T</span><span class="sxs-lookup"><span data-stu-id="419d8-128">Y41T</span></span>
-   <span data-ttu-id="419d8-129">Y42T</span><span class="sxs-lookup"><span data-stu-id="419d8-129">Y42T</span></span>
-   <span data-ttu-id="419d8-130">YUY2</span><span class="sxs-lookup"><span data-stu-id="419d8-130">YUY2</span></span>
-   <span data-ttu-id="419d8-131">YV12</span><span class="sxs-lookup"><span data-stu-id="419d8-131">YV12</span></span>
-   <span data-ttu-id="419d8-132">YVU9</span><span class="sxs-lookup"><span data-stu-id="419d8-132">YVU9</span></span>
-   <span data-ttu-id="419d8-133">ивю</span><span class="sxs-lookup"><span data-stu-id="419d8-133">YVYU</span></span>

## <a name="output-formats"></a><span data-ttu-id="419d8-134">Форматы выходных данных</span><span class="sxs-lookup"><span data-stu-id="419d8-134">Output Formats</span></span>

-   <span data-ttu-id="419d8-135">RGB 24</span><span class="sxs-lookup"><span data-stu-id="419d8-135">RGB 24</span></span>
-   <span data-ttu-id="419d8-136">RGB 32</span><span class="sxs-lookup"><span data-stu-id="419d8-136">RGB 32</span></span>
-   <span data-ttu-id="419d8-137">RGB 555</span><span class="sxs-lookup"><span data-stu-id="419d8-137">RGB 555</span></span>
-   <span data-ttu-id="419d8-138">RGB 565</span><span class="sxs-lookup"><span data-stu-id="419d8-138">RGB 565</span></span>
-   <span data-ttu-id="419d8-139">RGB 8</span><span class="sxs-lookup"><span data-stu-id="419d8-139">RGB 8</span></span>
-   <span data-ttu-id="419d8-140">айув</span><span class="sxs-lookup"><span data-stu-id="419d8-140">AYUV</span></span>
-   <span data-ttu-id="419d8-141">I420</span><span class="sxs-lookup"><span data-stu-id="419d8-141">I420</span></span>
-   <span data-ttu-id="419d8-142">ийув</span><span class="sxs-lookup"><span data-stu-id="419d8-142">IYUV</span></span>
-   <span data-ttu-id="419d8-143">NV11</span><span class="sxs-lookup"><span data-stu-id="419d8-143">NV11</span></span>
-   <span data-ttu-id="419d8-144">NV12</span><span class="sxs-lookup"><span data-stu-id="419d8-144">NV12</span></span>
-   <span data-ttu-id="419d8-145">UYVY</span><span class="sxs-lookup"><span data-stu-id="419d8-145">UYVY</span></span>
-   <span data-ttu-id="419d8-146">V216</span><span class="sxs-lookup"><span data-stu-id="419d8-146">V216</span></span>
-   <span data-ttu-id="419d8-147">V410</span><span class="sxs-lookup"><span data-stu-id="419d8-147">V410</span></span>
-   <span data-ttu-id="419d8-148">YUY2</span><span class="sxs-lookup"><span data-stu-id="419d8-148">YUY2</span></span>
-   <span data-ttu-id="419d8-149">YV12</span><span class="sxs-lookup"><span data-stu-id="419d8-149">YV12</span></span>
-   <span data-ttu-id="419d8-150">ивю</span><span class="sxs-lookup"><span data-stu-id="419d8-150">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="419d8-151">Свойства</span><span class="sxs-lookup"><span data-stu-id="419d8-151">Properties</span></span>

-   [<span data-ttu-id="419d8-152">МФПКЭЙ \_ колорконв \_ срклефт</span><span class="sxs-lookup"><span data-stu-id="419d8-152">MFPKEY\_COLORCONV\_SRCLEFT</span></span>](mfpkey-colorconv-srcleft.md)
-   [<span data-ttu-id="419d8-153">МФПКЭЙ \_ колорконв \_ срктоп</span><span class="sxs-lookup"><span data-stu-id="419d8-153">MFPKEY\_COLORCONV\_SRCTOP</span></span>](mfpkey-colorconv-srctop.md)
-   [<span data-ttu-id="419d8-154">МФПКЭЙ \_ колорконв \_ дстлефт</span><span class="sxs-lookup"><span data-stu-id="419d8-154">MFPKEY\_COLORCONV\_DSTLEFT</span></span>](mfpkey-colorconv-dstleft.md)
-   [<span data-ttu-id="419d8-155">МФПКЭЙ \_ колорконв \_ дсттоп</span><span class="sxs-lookup"><span data-stu-id="419d8-155">MFPKEY\_COLORCONV\_DSTTOP</span></span>](mfpkey-colorconv-dsttop.md)
-   [<span data-ttu-id="419d8-156">\_Ширина мфпкэй колорконв \_</span><span class="sxs-lookup"><span data-stu-id="419d8-156">MFPKEY\_COLORCONV\_WIDTH</span></span>](mfpkey-colorconv-width.md)
-   [<span data-ttu-id="419d8-157">\_Высота мфпкэй колорконв \_</span><span class="sxs-lookup"><span data-stu-id="419d8-157">MFPKEY\_COLORCONV\_HEIGHT</span></span>](mfpkey-colorconv-height.md)
-   [<span data-ttu-id="419d8-158">\_режим КОЛОРКОНВ \_ мфпкэй</span><span class="sxs-lookup"><span data-stu-id="419d8-158">MFPKEY\_COLORCONV\_MODE</span></span>](mfpkey-colorconv-mode.md)

## <a name="remarks"></a><span data-ttu-id="419d8-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="419d8-159">Remarks</span></span>

<span data-ttu-id="419d8-160">DSP цветового преобразователя реализован в виде COM-объекта, который может использоваться в качестве объекта Директксмедиа (DMO) или преобразования Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="419d8-160">The Color Converter DSP is implemented as a COM object that can act as a DirectXMedia Object (DMO) or a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="419d8-161">Объект имеет один идентификатор класса (CLSID), независимо от того, действует ли он как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="419d8-161">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="419d8-162">Сведения о том, когда DSP выступает в качестве DMO или MFT, см. в разделе [обработчики цифровых сигналов](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="419d8-162">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="419d8-163">Глобальные уникальные идентификаторы (GUID) для подтипов мультимедиа RGB различаются в зависимости от того, выступает ли DSP в роли DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="419d8-163">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="419d8-164">Идентификаторы GUID для подтипов мультимедиа, отличных от RGB, одинаковы, независимо от того, выступает ли DSP в роли DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="419d8-164">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="419d8-165">Сведения об идентификаторах GUID, представляющих подтипы мультимедиа, см. в разделе [GUID для подтипов видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="419d8-165">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="419d8-166">По умолчанию этот DSP копирует все исходное изображение в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="419d8-166">By default, this DSP copies the entire source image to the output buffer.</span></span> <span data-ttu-id="419d8-167">При необходимости можно указать исходные и конечные прямоугольники.</span><span class="sxs-lookup"><span data-stu-id="419d8-167">Optionally, you can specify source and destination rectangles.</span></span> <span data-ttu-id="419d8-168">DSP копирует часть исходного изображения, определенное исходным прямоугольником, и записывает его в прямоугольник назначения в выходном буфере.</span><span class="sxs-lookup"><span data-stu-id="419d8-168">The DSP copies the portion of the source image defined by source rectangle, and writes it into the destination rectangle on the output buffer.</span></span> <span data-ttu-id="419d8-169">DSP не выполняет масштабирования. исходный и конечный прямоугольники должны иметь одинаковый размер.</span><span class="sxs-lookup"><span data-stu-id="419d8-169">The DSP does not perform any scaling; the source and destination rectangles must be the same size.</span></span> <span data-ttu-id="419d8-170">Исходный и конечный прямоугольники не могут превышать границы видеокадра.</span><span class="sxs-lookup"><span data-stu-id="419d8-170">The source and destination rectangles cannot exceed the boundaries of the video frame.</span></span>

<span data-ttu-id="419d8-171">Все свойства, кроме [**\_ \_ режима колорконв мфпкэй**](mfpkey-colorconv-mode.md) , должны быть заданы в группе.</span><span class="sxs-lookup"><span data-stu-id="419d8-171">All of the properties except [**MFPKEY\_COLORCONV\_MODE**](mfpkey-colorconv-mode.md) must be set in a group.</span></span> <span data-ttu-id="419d8-172">Если задать любое из этих свойств, необходимо задать все остальные.</span><span class="sxs-lookup"><span data-stu-id="419d8-172">If you set any of these properties, you must set all of the others.</span></span> <span data-ttu-id="419d8-173">В противном случае исходный и конечный прямоугольники могут быть недопустимыми. в этом случае методы [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) и [**Имедиаобжект::P роцессаутпут**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) будут возвращать **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="419d8-173">Otherwise, the source and destination rectangles might be invalid, in which case both the [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) and [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) methods will return **E\_INVALIDARG**.</span></span>

<span data-ttu-id="419d8-174">Преобразователь цветов не поддерживает все сочетания входного и выходного форматов.</span><span class="sxs-lookup"><span data-stu-id="419d8-174">The color converter does not support every combination of input format and output format.</span></span> <span data-ttu-id="419d8-175">Как правило, следует задать формат мультимедиа, известный как ввод или вывод, а затем перечислить доступные форматы в противоположном потоке.</span><span class="sxs-lookup"><span data-stu-id="419d8-175">Usually, you should set the media format that you know, either input or output, and then enumerate the available formats on the opposite stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="419d8-176">Требования</span><span class="sxs-lookup"><span data-stu-id="419d8-176">Requirements</span></span>



| <span data-ttu-id="419d8-177">Требование</span><span class="sxs-lookup"><span data-stu-id="419d8-177">Requirement</span></span> | <span data-ttu-id="419d8-178">Значение</span><span class="sxs-lookup"><span data-stu-id="419d8-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="419d8-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="419d8-179">Minimum supported client</span></span><br/> | <span data-ttu-id="419d8-180">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="419d8-180">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="419d8-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="419d8-181">Minimum supported server</span></span><br/> | <span data-ttu-id="419d8-182">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="419d8-182">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="419d8-183">Header</span><span class="sxs-lookup"><span data-stu-id="419d8-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="419d8-184"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="419d8-184"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="419d8-185">DLL</span><span class="sxs-lookup"><span data-stu-id="419d8-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="419d8-186"><dt>Colorcnv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="419d8-186"><dt>Colorcnv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="419d8-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="419d8-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419d8-188">Обработчики цифровых сигналов</span><span class="sxs-lookup"><span data-stu-id="419d8-188">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
