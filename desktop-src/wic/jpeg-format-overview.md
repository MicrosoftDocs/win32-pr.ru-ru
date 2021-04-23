---
description: В этом разделе содержатся сведения о коде встроенного кода JPEG, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Общие сведения о формате JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683453"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="194d3-103">Общие сведения о формате JPEG</span><span class="sxs-lookup"><span data-stu-id="194d3-103">JPEG Format Overview</span></span>

<span data-ttu-id="194d3-104">В этом разделе содержатся сведения о коде встроенного кода JPEG, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="194d3-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="194d3-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="194d3-105">Codec Identity</span></span>

<span data-ttu-id="194d3-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="194d3-106">The following table provides codec identification information.</span></span>



|                        |                                         |
|------------------------|-----------------------------------------|
| <span data-ttu-id="194d3-107">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="194d3-107">Formal Name(s)</span></span>         | <span data-ttu-id="194d3-108">JPEG</span><span class="sxs-lookup"><span data-stu-id="194d3-108">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="194d3-109">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="194d3-109">File Name Extension(s)</span></span> | <span data-ttu-id="194d3-110">JPE, JPEG, JPG</span><span class="sxs-lookup"><span data-stu-id="194d3-110">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="194d3-111">тип MIME</span><span class="sxs-lookup"><span data-stu-id="194d3-111">MIME type</span></span>              | <span data-ttu-id="194d3-112">Image/JPEG, Image/JPE, Image/JPG</span><span class="sxs-lookup"><span data-stu-id="194d3-112">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="194d3-113">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="194d3-113">Specification Support</span></span>  | <span data-ttu-id="194d3-114">Спецификация JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="194d3-114">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="194d3-115">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека JPEG.</span><span class="sxs-lookup"><span data-stu-id="194d3-115">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="194d3-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="194d3-116">Component</span></span>        | <span data-ttu-id="194d3-117">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="194d3-117">Friendly Name</span></span>             | <span data-ttu-id="194d3-118">Код GUID</span><span class="sxs-lookup"><span data-stu-id="194d3-118">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="194d3-119">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="194d3-119">Container Format</span></span> | <span data-ttu-id="194d3-120">GUID \_ контаинерформатжпег</span><span class="sxs-lookup"><span data-stu-id="194d3-120">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="194d3-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="194d3-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="194d3-122">Показан</span><span class="sxs-lookup"><span data-stu-id="194d3-122">Decoder</span></span>          | <span data-ttu-id="194d3-123">\_ВИКЖПЕГДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="194d3-123">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="194d3-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="194d3-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="194d3-125">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="194d3-125">Encoder</span></span>          | <span data-ttu-id="194d3-126">\_ВИКЖПЕЖЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="194d3-126">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="194d3-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="194d3-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="194d3-128">Кодирование</span><span class="sxs-lookup"><span data-stu-id="194d3-128">Encoding</span></span>

<span data-ttu-id="194d3-129">API кодирования WIC разработан как независимый от кодека, а кодировка изображений для кодеков с поддержкой WIC практически одинакова.</span><span class="sxs-lookup"><span data-stu-id="194d3-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="194d3-130">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="194d3-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="194d3-131">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="194d3-131">Encoder Options</span></span>

<span data-ttu-id="194d3-132">Кодеки с поддержкой WIC отличаются на уровне параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="194d3-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="194d3-133">Параметры кодировщика соответствуют возможностям кодировщика изображений, и каждый кодек машинного кода поддерживает набор этих вариантов кодировщика.</span><span class="sxs-lookup"><span data-stu-id="194d3-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="194d3-134">Параметры кодировщика могут быть базовыми вариантами, поддерживаемыми для всех кодов, включенных с помощью WIC (хотя и не всегда поддерживаемых), или параметров, относящихся к кодекам.</span><span class="sxs-lookup"><span data-stu-id="194d3-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="194d3-135">Для управления этими параметрами кодировки в процессе кодирования компонент WIC использует интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="194d3-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="194d3-136">Дополнительные сведения об использовании интерфейса **IPropertyBag2** для кодирования WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="194d3-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="194d3-137">Кодек JPEG использует основные параметры WIC.</span><span class="sxs-lookup"><span data-stu-id="194d3-137">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="194d3-138">В следующей таблице перечислены параметры кодировщика WIC, поддерживаемые кодеком машинного кода JPEG.</span><span class="sxs-lookup"><span data-stu-id="194d3-138">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="194d3-139">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="194d3-139">Property Name</span></span>                                        | <span data-ttu-id="194d3-140">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="194d3-140">VARTYPE</span></span>           | <span data-ttu-id="194d3-141">Диапазон значений:</span><span class="sxs-lookup"><span data-stu-id="194d3-141">Value Range</span></span>                                                                       | <span data-ttu-id="194d3-142">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="194d3-142">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="194d3-143">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="194d3-143">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="194d3-144">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="194d3-144">VT\_R4</span></span>            | <span data-ttu-id="194d3-145">0 — 1,0</span><span class="sxs-lookup"><span data-stu-id="194d3-145">0 - 1.0</span></span>                                                                           | <span data-ttu-id="194d3-146">0,9</span><span class="sxs-lookup"><span data-stu-id="194d3-146">0.9</span></span>                                                                            |
| [<span data-ttu-id="194d3-147">битмаптрансформ</span><span class="sxs-lookup"><span data-stu-id="194d3-147">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="194d3-148">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="194d3-148">VT\_UI1</span></span>           | [<span data-ttu-id="194d3-149">**викбитмаптрансформоптионс**</span><span class="sxs-lookup"><span data-stu-id="194d3-149">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="194d3-150">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="194d3-150">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="194d3-151">Освещенность</span><span class="sxs-lookup"><span data-stu-id="194d3-151">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="194d3-152">VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="194d3-152">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="194d3-153">64 записей (ДКТ)</span><span class="sxs-lookup"><span data-stu-id="194d3-153">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="194d3-154">Таблица освещенности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="194d3-154">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="194d3-155">Chrominance</span><span class="sxs-lookup"><span data-stu-id="194d3-155">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="194d3-156">VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="194d3-156">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="194d3-157">64 записей (ДКТ)</span><span class="sxs-lookup"><span data-stu-id="194d3-157">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="194d3-158">Таблица чроминанце по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="194d3-158">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="194d3-159">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="194d3-159">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="194d3-160">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="194d3-160">VT\_UI1</span></span>           | [<span data-ttu-id="194d3-161">**викжпегикркбсубсамплингоптион**</span><span class="sxs-lookup"><span data-stu-id="194d3-161">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="194d3-162">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="194d3-162">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="194d3-163">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="194d3-163">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="194d3-164">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="194d3-164">VT\_BOOL</span></span>          | <span data-ttu-id="194d3-165">**Значение true** / **Значение false**</span><span class="sxs-lookup"><span data-stu-id="194d3-165">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="194d3-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="194d3-166">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="194d3-167">Если в списке параметров [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) есть параметр кодировщика, который не поддерживается кодеком, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="194d3-167">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="194d3-168">Имажекуалити, параметр</span><span class="sxs-lookup"><span data-stu-id="194d3-168">ImageQuality Option</span></span>

<span data-ttu-id="194d3-169">Задает нужную точность изображения.</span><span class="sxs-lookup"><span data-stu-id="194d3-169">Specifies the desired image fidelity.</span></span> <span data-ttu-id="194d3-170">0,0 указывает наименьшую возможную точность, а 1,0 — наивысшую достоверность.</span><span class="sxs-lookup"><span data-stu-id="194d3-170">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="194d3-171">Значение по умолчанию — 0,9.</span><span class="sxs-lookup"><span data-stu-id="194d3-171">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="194d3-172">Битмаптрансформ, параметр</span><span class="sxs-lookup"><span data-stu-id="194d3-172">BitmapTransform Option</span></span>

<span data-ttu-id="194d3-173">Указывает способ преобразования изображения во время декодирования изображения.</span><span class="sxs-lookup"><span data-stu-id="194d3-173">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="194d3-174">Для этого параметра необходимо задать одно из значений перечисления [**викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="194d3-174">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="194d3-175">Значение по умолчанию — [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span><span class="sxs-lookup"><span data-stu-id="194d3-175">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="194d3-176">Параметр освещенности</span><span class="sxs-lookup"><span data-stu-id="194d3-176">Luminance Option</span></span>

<span data-ttu-id="194d3-177">Задает таблицу уровня яркости оттенков серого, используемую для кодирования.</span><span class="sxs-lookup"><span data-stu-id="194d3-177">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="194d3-178">Чроминанце, параметр</span><span class="sxs-lookup"><span data-stu-id="194d3-178">Chrominance Option</span></span>

<span data-ttu-id="194d3-179">Указывает таблицу чроминанце, используемую для кодирования.</span><span class="sxs-lookup"><span data-stu-id="194d3-179">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="194d3-180">Жпегикркбсубсамплинг, параметр</span><span class="sxs-lookup"><span data-stu-id="194d3-180">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="194d3-181">Указывает отношение подвыборки, используемое для кодирования Икркб.</span><span class="sxs-lookup"><span data-stu-id="194d3-181">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="194d3-182">Значение по умолчанию — [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span><span class="sxs-lookup"><span data-stu-id="194d3-182">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="194d3-183">SuppressApp0, параметр</span><span class="sxs-lookup"><span data-stu-id="194d3-183">SuppressApp0 Option</span></span>

<span data-ttu-id="194d3-184">Указывает, следует ли подавлять запись метаданных APP0 при кодировании данных изображения.</span><span class="sxs-lookup"><span data-stu-id="194d3-184">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="194d3-185">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="194d3-185">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="194d3-186">Декодирование</span><span class="sxs-lookup"><span data-stu-id="194d3-186">Decoding</span></span>

<span data-ttu-id="194d3-187">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="194d3-187">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="194d3-188">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="194d3-188">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="194d3-189">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="194d3-189">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="194d3-190">Встроенный кодек JPEG также поддерживает [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) при декодировании кадров, добавляя параметры раскрывающемся для декодирования потока изображений.</span><span class="sxs-lookup"><span data-stu-id="194d3-190">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="194d3-191">Дополнительные сведения об этих дополнительных параметрах см. в разделе [Обзор источников битовой карты](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="194d3-191">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
