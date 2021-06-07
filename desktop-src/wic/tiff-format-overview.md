---
description: В этом разделе содержатся сведения о коде кодеков TIFF, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Общие сведения о формате TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444425"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="9afee-103">Общие сведения о формате TIFF</span><span class="sxs-lookup"><span data-stu-id="9afee-103">TIFF Format Overview</span></span>

<span data-ttu-id="9afee-104">В этом разделе содержатся сведения о коде кодеков TIFF, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="9afee-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="9afee-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="9afee-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="9afee-106">Кодирование</span><span class="sxs-lookup"><span data-stu-id="9afee-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="9afee-107">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="9afee-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="9afee-108">Декодирование</span><span class="sxs-lookup"><span data-stu-id="9afee-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="9afee-109">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="9afee-109">Codec Identity</span></span>

<span data-ttu-id="9afee-110">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="9afee-110">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="9afee-111">Компонент</span><span class="sxs-lookup"><span data-stu-id="9afee-111">Component</span></span>            |   <span data-ttu-id="9afee-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9afee-112">Description</span></span>                   |
|------------------------|---------------------------------|
| <span data-ttu-id="9afee-113">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="9afee-113">Formal Name(s)</span></span>         | <span data-ttu-id="9afee-114">TIFF</span><span class="sxs-lookup"><span data-stu-id="9afee-114">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="9afee-115">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="9afee-115">File Name Extension(s)</span></span> | <span data-ttu-id="9afee-116">TIFF, TIF</span><span class="sxs-lookup"><span data-stu-id="9afee-116">tiff, tif</span></span>                       |
| <span data-ttu-id="9afee-117">Типы MIME</span><span class="sxs-lookup"><span data-stu-id="9afee-117">MIME type(s)</span></span>           | <span data-ttu-id="9afee-118">Image/TIFF, Image/TIF</span><span class="sxs-lookup"><span data-stu-id="9afee-118">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="9afee-119">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="9afee-119">Specification Support</span></span>  | <span data-ttu-id="9afee-120">Спецификация TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="9afee-120">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="9afee-121">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека TIFF.</span><span class="sxs-lookup"><span data-stu-id="9afee-121">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="9afee-122">Компонент</span><span class="sxs-lookup"><span data-stu-id="9afee-122">Component</span></span>        | <span data-ttu-id="9afee-123">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="9afee-123">Friendly Name</span></span>             | <span data-ttu-id="9afee-124">Код GUID</span><span class="sxs-lookup"><span data-stu-id="9afee-124">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="9afee-125">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="9afee-125">Container Format</span></span> | <span data-ttu-id="9afee-126">GUID \_ контаинерформаттифф</span><span class="sxs-lookup"><span data-stu-id="9afee-126">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="9afee-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="9afee-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="9afee-128">Показан</span><span class="sxs-lookup"><span data-stu-id="9afee-128">Decoder</span></span>          | <span data-ttu-id="9afee-129">\_ВИКТИФФДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="9afee-129">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="9afee-130">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="9afee-130">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="9afee-131">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="9afee-131">Encoder</span></span>          | <span data-ttu-id="9afee-132">\_ВИКТИФФЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="9afee-132">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="9afee-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="9afee-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="9afee-134">Кодирование</span><span class="sxs-lookup"><span data-stu-id="9afee-134">Encoding</span></span>

<span data-ttu-id="9afee-135">API кодирования WIC разработан как независимый от кодека, а кодировка изображений для кодеков с поддержкой WIC практически одинакова.</span><span class="sxs-lookup"><span data-stu-id="9afee-135">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9afee-136">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9afee-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="9afee-137">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="9afee-137">Encoder Options</span></span>

<span data-ttu-id="9afee-138">Кодеки с поддержкой WIC отличаются на уровне параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="9afee-138">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="9afee-139">Параметры кодировщика соответствуют возможностям кодировщика изображений, и каждый кодек машинного кода поддерживает набор этих вариантов кодировщика.</span><span class="sxs-lookup"><span data-stu-id="9afee-139">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="9afee-140">Параметры кодировщика могут быть базовыми вариантами, поддерживаемыми для всех кодов, включенных с помощью WIC (хотя и не всегда поддерживаемых), или параметров, относящихся к кодекам.</span><span class="sxs-lookup"><span data-stu-id="9afee-140">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="9afee-141">Для управления этими параметрами кодировки в процессе кодирования компонент WIC использует интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9afee-141">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="9afee-142">Дополнительные сведения об использовании интерфейса **IPropertyBag2** для кодирования WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9afee-142">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="9afee-143">Кодек TIFF использует основные параметры WIC.</span><span class="sxs-lookup"><span data-stu-id="9afee-143">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="9afee-144">В следующей таблице перечислены параметры кодировщика WIC, поддерживаемые кодеком Native TIFF.</span><span class="sxs-lookup"><span data-stu-id="9afee-144">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="9afee-145">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="9afee-145">Property Name</span></span>         | <span data-ttu-id="9afee-146">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9afee-146">VARTYPE</span></span> | <span data-ttu-id="9afee-147">Диапазон значений:</span><span class="sxs-lookup"><span data-stu-id="9afee-147">Value Range</span></span> | <span data-ttu-id="9afee-148">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9afee-148">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="9afee-149">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="9afee-149">CompressionQuality</span></span>    | <span data-ttu-id="9afee-150">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="9afee-150">VT\_R4</span></span>  | <span data-ttu-id="9afee-151">0 — 1,0</span><span class="sxs-lookup"><span data-stu-id="9afee-151">0 - 1.0</span></span>     | <span data-ttu-id="9afee-152">0</span><span class="sxs-lookup"><span data-stu-id="9afee-152">0</span></span>                |
| <span data-ttu-id="9afee-153">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="9afee-153">TiffCompressionMethod</span></span> | <span data-ttu-id="9afee-154">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="9afee-154">VT\_UI1</span></span> | [<span data-ttu-id="9afee-155">**виктиффкомпрессионоптион**</span><span class="sxs-lookup"><span data-stu-id="9afee-155">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="9afee-156">**виктиффкомпрессиондонткаре**</span><span class="sxs-lookup"><span data-stu-id="9afee-156">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="9afee-157">Если в списке параметров [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) есть параметр кодировщика, который не поддерживается кодеком, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9afee-157">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="9afee-158">Компрессионкуалити, параметр</span><span class="sxs-lookup"><span data-stu-id="9afee-158">CompressionQuality Option</span></span>

<span data-ttu-id="9afee-159">Задает требуемое качество сжатия.</span><span class="sxs-lookup"><span data-stu-id="9afee-159">Specifies the desired compression quality.</span></span> <span data-ttu-id="9afee-160">0,0 — это наименее эффективная доступная схема сжатия.</span><span class="sxs-lookup"><span data-stu-id="9afee-160">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="9afee-161">Как правило, эта схема приводит к более быстрой кодировке, но большему результату.</span><span class="sxs-lookup"><span data-stu-id="9afee-161">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="9afee-162">Значение 1,0 указывает наиболее эффективную схему сжатия.</span><span class="sxs-lookup"><span data-stu-id="9afee-162">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="9afee-163">Как правило, эта схема приводит к более длинному кодированию, но создает меньший объем выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9afee-163">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="9afee-164">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="9afee-164">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="9afee-165">Тиффкомпрессионмесод, параметр</span><span class="sxs-lookup"><span data-stu-id="9afee-165">TiffCompressionMethod Option</span></span>

<span data-ttu-id="9afee-166">Задает метод сжатия TIFF.</span><span class="sxs-lookup"><span data-stu-id="9afee-166">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="9afee-167">Значение по умолчанию — [**виктиффкомпрессиондонткаре**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span><span class="sxs-lookup"><span data-stu-id="9afee-167">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="9afee-168">Декодирование</span><span class="sxs-lookup"><span data-stu-id="9afee-168">Decoding</span></span>

<span data-ttu-id="9afee-169">Интерфейсы API декодирования WIC не зависят от кодека и декодирование изображений для кодеков с поддержкой WIC по сути являются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="9afee-169">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9afee-170">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="9afee-170">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="9afee-171">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="9afee-171">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
