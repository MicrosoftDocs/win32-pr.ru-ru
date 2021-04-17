---
description: В этом разделе содержатся сведения о коде кодеков TIFF, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Общие сведения о формате TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702903"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="3edb2-103">Общие сведения о формате TIFF</span><span class="sxs-lookup"><span data-stu-id="3edb2-103">TIFF Format Overview</span></span>

<span data-ttu-id="3edb2-104">В этом разделе содержатся сведения о коде кодеков TIFF, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="3edb2-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="3edb2-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="3edb2-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="3edb2-106">Кодирование</span><span class="sxs-lookup"><span data-stu-id="3edb2-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="3edb2-107">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="3edb2-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="3edb2-108">Декодирование</span><span class="sxs-lookup"><span data-stu-id="3edb2-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="3edb2-109">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="3edb2-109">Codec Identity</span></span>

<span data-ttu-id="3edb2-110">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="3edb2-110">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="3edb2-111">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="3edb2-111">Formal Name(s)</span></span>         | <span data-ttu-id="3edb2-112">TIFF</span><span class="sxs-lookup"><span data-stu-id="3edb2-112">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="3edb2-113">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="3edb2-113">File Name Extension(s)</span></span> | <span data-ttu-id="3edb2-114">TIFF, TIF</span><span class="sxs-lookup"><span data-stu-id="3edb2-114">tiff, tif</span></span>                       |
| <span data-ttu-id="3edb2-115">Типы MIME</span><span class="sxs-lookup"><span data-stu-id="3edb2-115">MIME type(s)</span></span>           | <span data-ttu-id="3edb2-116">Image/TIFF, Image/TIF</span><span class="sxs-lookup"><span data-stu-id="3edb2-116">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="3edb2-117">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="3edb2-117">Specification Support</span></span>  | <span data-ttu-id="3edb2-118">Спецификация TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="3edb2-118">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="3edb2-119">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека TIFF.</span><span class="sxs-lookup"><span data-stu-id="3edb2-119">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="3edb2-120">Компонент</span><span class="sxs-lookup"><span data-stu-id="3edb2-120">Component</span></span>        | <span data-ttu-id="3edb2-121">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="3edb2-121">Friendly Name</span></span>             | <span data-ttu-id="3edb2-122">Код GUID</span><span class="sxs-lookup"><span data-stu-id="3edb2-122">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="3edb2-123">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="3edb2-123">Container Format</span></span> | <span data-ttu-id="3edb2-124">GUID \_ контаинерформаттифф</span><span class="sxs-lookup"><span data-stu-id="3edb2-124">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="3edb2-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="3edb2-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="3edb2-126">Показан</span><span class="sxs-lookup"><span data-stu-id="3edb2-126">Decoder</span></span>          | <span data-ttu-id="3edb2-127">\_ВИКТИФФДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="3edb2-127">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="3edb2-128">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="3edb2-128">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="3edb2-129">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="3edb2-129">Encoder</span></span>          | <span data-ttu-id="3edb2-130">\_ВИКТИФФЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="3edb2-130">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="3edb2-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="3edb2-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="3edb2-132">Кодирование</span><span class="sxs-lookup"><span data-stu-id="3edb2-132">Encoding</span></span>

<span data-ttu-id="3edb2-133">API кодирования WIC разработан как независимый от кодека, а кодировка изображений для кодеков с поддержкой WIC практически одинакова.</span><span class="sxs-lookup"><span data-stu-id="3edb2-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3edb2-134">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="3edb2-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="3edb2-135">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="3edb2-135">Encoder Options</span></span>

<span data-ttu-id="3edb2-136">Кодеки с поддержкой WIC отличаются на уровне параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="3edb2-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="3edb2-137">Параметры кодировщика соответствуют возможностям кодировщика изображений, и каждый кодек машинного кода поддерживает набор этих вариантов кодировщика.</span><span class="sxs-lookup"><span data-stu-id="3edb2-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="3edb2-138">Параметры кодировщика могут быть базовыми вариантами, поддерживаемыми для всех кодов, включенных с помощью WIC (хотя и не всегда поддерживаемых), или параметров, относящихся к кодекам.</span><span class="sxs-lookup"><span data-stu-id="3edb2-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="3edb2-139">Для управления этими параметрами кодировки в процессе кодирования компонент WIC использует интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3edb2-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="3edb2-140">Дополнительные сведения об использовании интерфейса **IPropertyBag2** для кодирования WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="3edb2-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="3edb2-141">Кодек TIFF использует основные параметры WIC.</span><span class="sxs-lookup"><span data-stu-id="3edb2-141">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="3edb2-142">В следующей таблице перечислены параметры кодировщика WIC, поддерживаемые кодеком Native TIFF.</span><span class="sxs-lookup"><span data-stu-id="3edb2-142">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="3edb2-143">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="3edb2-143">Property Name</span></span>         | <span data-ttu-id="3edb2-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3edb2-144">VARTYPE</span></span> | <span data-ttu-id="3edb2-145">Диапазон значений:</span><span class="sxs-lookup"><span data-stu-id="3edb2-145">Value Range</span></span> | <span data-ttu-id="3edb2-146">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3edb2-146">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="3edb2-147">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="3edb2-147">CompressionQuality</span></span>    | <span data-ttu-id="3edb2-148">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="3edb2-148">VT\_R4</span></span>  | <span data-ttu-id="3edb2-149">0 — 1,0</span><span class="sxs-lookup"><span data-stu-id="3edb2-149">0 - 1.0</span></span>     | <span data-ttu-id="3edb2-150">0</span><span class="sxs-lookup"><span data-stu-id="3edb2-150">0</span></span>                |
| <span data-ttu-id="3edb2-151">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="3edb2-151">TiffCompressionMethod</span></span> | <span data-ttu-id="3edb2-152">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="3edb2-152">VT\_UI1</span></span> | [<span data-ttu-id="3edb2-153">**виктиффкомпрессионоптион**</span><span class="sxs-lookup"><span data-stu-id="3edb2-153">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="3edb2-154">**виктиффкомпрессиондонткаре**</span><span class="sxs-lookup"><span data-stu-id="3edb2-154">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="3edb2-155">Если в списке параметров [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) есть параметр кодировщика, который не поддерживается кодеком, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3edb2-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="3edb2-156">Компрессионкуалити, параметр</span><span class="sxs-lookup"><span data-stu-id="3edb2-156">CompressionQuality Option</span></span>

<span data-ttu-id="3edb2-157">Задает требуемое качество сжатия.</span><span class="sxs-lookup"><span data-stu-id="3edb2-157">Specifies the desired compression quality.</span></span> <span data-ttu-id="3edb2-158">0,0 — это наименее эффективная доступная схема сжатия.</span><span class="sxs-lookup"><span data-stu-id="3edb2-158">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="3edb2-159">Как правило, эта схема приводит к более быстрой кодировке, но большему результату.</span><span class="sxs-lookup"><span data-stu-id="3edb2-159">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="3edb2-160">Значение 1,0 указывает наиболее эффективную схему сжатия.</span><span class="sxs-lookup"><span data-stu-id="3edb2-160">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="3edb2-161">Как правило, эта схема приводит к более длинному кодированию, но создает меньший объем выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3edb2-161">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="3edb2-162">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="3edb2-162">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="3edb2-163">Тиффкомпрессионмесод, параметр</span><span class="sxs-lookup"><span data-stu-id="3edb2-163">TiffCompressionMethod Option</span></span>

<span data-ttu-id="3edb2-164">Задает метод сжатия TIFF.</span><span class="sxs-lookup"><span data-stu-id="3edb2-164">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="3edb2-165">Значение по умолчанию — [**виктиффкомпрессиондонткаре**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span><span class="sxs-lookup"><span data-stu-id="3edb2-165">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="3edb2-166">Декодирование</span><span class="sxs-lookup"><span data-stu-id="3edb2-166">Decoding</span></span>

<span data-ttu-id="3edb2-167">Интерфейсы API декодирования WIC не зависят от кодека и декодирование изображений для кодеков с поддержкой WIC по сути являются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="3edb2-167">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3edb2-168">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="3edb2-168">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="3edb2-169">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="3edb2-169">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
