---
description: В этом разделе содержатся сведения о коде встроенного кода JPEG, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Общие сведения о формате JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444195"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="79e0b-103">Общие сведения о формате JPEG</span><span class="sxs-lookup"><span data-stu-id="79e0b-103">JPEG Format Overview</span></span>

<span data-ttu-id="79e0b-104">В этом разделе содержатся сведения о коде встроенного кода JPEG, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="79e0b-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="79e0b-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="79e0b-105">Codec Identity</span></span>

<span data-ttu-id="79e0b-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="79e0b-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="79e0b-107">Компонент</span><span class="sxs-lookup"><span data-stu-id="79e0b-107">Component</span></span>            | <span data-ttu-id="79e0b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="79e0b-108">Description</span></span>                             |
|------------------------|-----------------------------------------|
| <span data-ttu-id="79e0b-109">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="79e0b-109">Formal Name(s)</span></span>         | <span data-ttu-id="79e0b-110">JPEG</span><span class="sxs-lookup"><span data-stu-id="79e0b-110">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="79e0b-111">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="79e0b-111">File Name Extension(s)</span></span> | <span data-ttu-id="79e0b-112">JPE, JPEG, JPG</span><span class="sxs-lookup"><span data-stu-id="79e0b-112">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="79e0b-113">тип MIME</span><span class="sxs-lookup"><span data-stu-id="79e0b-113">MIME type</span></span>              | <span data-ttu-id="79e0b-114">Image/JPEG, Image/JPE, Image/JPG</span><span class="sxs-lookup"><span data-stu-id="79e0b-114">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="79e0b-115">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="79e0b-115">Specification Support</span></span>  | <span data-ttu-id="79e0b-116">Спецификация JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="79e0b-116">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="79e0b-117">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека JPEG.</span><span class="sxs-lookup"><span data-stu-id="79e0b-117">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="79e0b-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="79e0b-118">Component</span></span>        | <span data-ttu-id="79e0b-119">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="79e0b-119">Friendly Name</span></span>             | <span data-ttu-id="79e0b-120">Код GUID</span><span class="sxs-lookup"><span data-stu-id="79e0b-120">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="79e0b-121">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="79e0b-121">Container Format</span></span> | <span data-ttu-id="79e0b-122">GUID \_ контаинерформатжпег</span><span class="sxs-lookup"><span data-stu-id="79e0b-122">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="79e0b-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="79e0b-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="79e0b-124">Показан</span><span class="sxs-lookup"><span data-stu-id="79e0b-124">Decoder</span></span>          | <span data-ttu-id="79e0b-125">\_ВИКЖПЕГДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="79e0b-125">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="79e0b-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="79e0b-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="79e0b-127">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="79e0b-127">Encoder</span></span>          | <span data-ttu-id="79e0b-128">\_ВИКЖПЕЖЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="79e0b-128">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="79e0b-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="79e0b-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="79e0b-130">Кодирование</span><span class="sxs-lookup"><span data-stu-id="79e0b-130">Encoding</span></span>

<span data-ttu-id="79e0b-131">API кодирования WIC разработан как независимый от кодека, а кодировка изображений для кодеков с поддержкой WIC практически одинакова.</span><span class="sxs-lookup"><span data-stu-id="79e0b-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="79e0b-132">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="79e0b-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="79e0b-133">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="79e0b-133">Encoder Options</span></span>

<span data-ttu-id="79e0b-134">Кодеки с поддержкой WIC отличаются на уровне параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="79e0b-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="79e0b-135">Параметры кодировщика соответствуют возможностям кодировщика изображений, и каждый кодек машинного кода поддерживает набор этих вариантов кодировщика.</span><span class="sxs-lookup"><span data-stu-id="79e0b-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="79e0b-136">Параметры кодировщика могут быть базовыми вариантами, поддерживаемыми для всех кодов, включенных с помощью WIC (хотя и не всегда поддерживаемых), или параметров, относящихся к кодекам.</span><span class="sxs-lookup"><span data-stu-id="79e0b-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="79e0b-137">Для управления этими параметрами кодировки в процессе кодирования компонент WIC использует интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="79e0b-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="79e0b-138">Дополнительные сведения об использовании интерфейса **IPropertyBag2** для кодирования WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="79e0b-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="79e0b-139">Кодек JPEG использует основные параметры WIC.</span><span class="sxs-lookup"><span data-stu-id="79e0b-139">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="79e0b-140">В следующей таблице перечислены параметры кодировщика WIC, поддерживаемые кодеком машинного кода JPEG.</span><span class="sxs-lookup"><span data-stu-id="79e0b-140">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="79e0b-141">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="79e0b-141">Property Name</span></span>                                        | <span data-ttu-id="79e0b-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="79e0b-142">VARTYPE</span></span>           | <span data-ttu-id="79e0b-143">Диапазон значений:</span><span class="sxs-lookup"><span data-stu-id="79e0b-143">Value Range</span></span>                                                                       | <span data-ttu-id="79e0b-144">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="79e0b-144">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="79e0b-145">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="79e0b-145">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="79e0b-146">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="79e0b-146">VT\_R4</span></span>            | <span data-ttu-id="79e0b-147">0 — 1,0</span><span class="sxs-lookup"><span data-stu-id="79e0b-147">0 - 1.0</span></span>                                                                           | <span data-ttu-id="79e0b-148">0,9</span><span class="sxs-lookup"><span data-stu-id="79e0b-148">0.9</span></span>                                                                            |
| [<span data-ttu-id="79e0b-149">битмаптрансформ</span><span class="sxs-lookup"><span data-stu-id="79e0b-149">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="79e0b-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="79e0b-150">VT\_UI1</span></span>           | [<span data-ttu-id="79e0b-151">**викбитмаптрансформоптионс**</span><span class="sxs-lookup"><span data-stu-id="79e0b-151">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="79e0b-152">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="79e0b-152">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="79e0b-153">Освещенность</span><span class="sxs-lookup"><span data-stu-id="79e0b-153">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="79e0b-154">VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="79e0b-154">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="79e0b-155">64 записей (ДКТ)</span><span class="sxs-lookup"><span data-stu-id="79e0b-155">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="79e0b-156">Таблица освещенности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79e0b-156">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="79e0b-157">Chrominance</span><span class="sxs-lookup"><span data-stu-id="79e0b-157">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="79e0b-158">VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="79e0b-158">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="79e0b-159">64 записей (ДКТ)</span><span class="sxs-lookup"><span data-stu-id="79e0b-159">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="79e0b-160">Таблица чроминанце по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79e0b-160">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="79e0b-161">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="79e0b-161">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="79e0b-162">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="79e0b-162">VT\_UI1</span></span>           | [<span data-ttu-id="79e0b-163">**викжпегикркбсубсамплингоптион**</span><span class="sxs-lookup"><span data-stu-id="79e0b-163">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="79e0b-164">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="79e0b-164">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="79e0b-165">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="79e0b-165">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="79e0b-166">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="79e0b-166">VT\_BOOL</span></span>          | <span data-ttu-id="79e0b-167">**Значение true** / **Значение false**</span><span class="sxs-lookup"><span data-stu-id="79e0b-167">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="79e0b-168">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="79e0b-168">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="79e0b-169">Если в списке параметров [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) есть параметр кодировщика, который не поддерживается кодеком, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="79e0b-169">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="79e0b-170">Имажекуалити, параметр</span><span class="sxs-lookup"><span data-stu-id="79e0b-170">ImageQuality Option</span></span>

<span data-ttu-id="79e0b-171">Задает нужную точность изображения.</span><span class="sxs-lookup"><span data-stu-id="79e0b-171">Specifies the desired image fidelity.</span></span> <span data-ttu-id="79e0b-172">0,0 указывает наименьшую возможную точность, а 1,0 — наивысшую достоверность.</span><span class="sxs-lookup"><span data-stu-id="79e0b-172">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="79e0b-173">Значение по умолчанию — 0,9.</span><span class="sxs-lookup"><span data-stu-id="79e0b-173">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="79e0b-174">Битмаптрансформ, параметр</span><span class="sxs-lookup"><span data-stu-id="79e0b-174">BitmapTransform Option</span></span>

<span data-ttu-id="79e0b-175">Указывает способ преобразования изображения во время декодирования изображения.</span><span class="sxs-lookup"><span data-stu-id="79e0b-175">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="79e0b-176">Для этого параметра необходимо задать одно из значений перечисления [**викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="79e0b-176">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="79e0b-177">Значение по умолчанию — [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span><span class="sxs-lookup"><span data-stu-id="79e0b-177">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="79e0b-178">Параметр освещенности</span><span class="sxs-lookup"><span data-stu-id="79e0b-178">Luminance Option</span></span>

<span data-ttu-id="79e0b-179">Задает таблицу уровня яркости оттенков серого, используемую для кодирования.</span><span class="sxs-lookup"><span data-stu-id="79e0b-179">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="79e0b-180">Чроминанце, параметр</span><span class="sxs-lookup"><span data-stu-id="79e0b-180">Chrominance Option</span></span>

<span data-ttu-id="79e0b-181">Указывает таблицу чроминанце, используемую для кодирования.</span><span class="sxs-lookup"><span data-stu-id="79e0b-181">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="79e0b-182">Жпегикркбсубсамплинг, параметр</span><span class="sxs-lookup"><span data-stu-id="79e0b-182">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="79e0b-183">Указывает отношение подвыборки, используемое для кодирования Икркб.</span><span class="sxs-lookup"><span data-stu-id="79e0b-183">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="79e0b-184">Значение по умолчанию — [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span><span class="sxs-lookup"><span data-stu-id="79e0b-184">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="79e0b-185">SuppressApp0, параметр</span><span class="sxs-lookup"><span data-stu-id="79e0b-185">SuppressApp0 Option</span></span>

<span data-ttu-id="79e0b-186">Указывает, следует ли подавлять запись метаданных APP0 при кодировании данных изображения.</span><span class="sxs-lookup"><span data-stu-id="79e0b-186">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="79e0b-187">Значение по умолчанию — **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="79e0b-187">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="79e0b-188">Декодирование</span><span class="sxs-lookup"><span data-stu-id="79e0b-188">Decoding</span></span>

<span data-ttu-id="79e0b-189">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="79e0b-189">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="79e0b-190">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="79e0b-190">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="79e0b-191">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="79e0b-191">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="79e0b-192">Встроенный кодек JPEG также поддерживает [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) при декодировании кадров, добавляя параметры раскрывающемся для декодирования потока изображений.</span><span class="sxs-lookup"><span data-stu-id="79e0b-192">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="79e0b-193">Дополнительные сведения об этих дополнительных параметрах см. в разделе [Обзор источников битовой карты](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="79e0b-193">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
