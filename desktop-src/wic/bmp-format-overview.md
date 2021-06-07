---
description: В этом разделе содержатся сведения о коде встроенного BMP, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Обзор формата BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444965"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="f3dde-103">Обзор формата BMP</span><span class="sxs-lookup"><span data-stu-id="f3dde-103">BMP Format Overview</span></span>

<span data-ttu-id="f3dde-104">В этом разделе содержатся сведения о коде встроенного BMP, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="f3dde-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="f3dde-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="f3dde-105">Codec Identity</span></span>

<span data-ttu-id="f3dde-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="f3dde-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="f3dde-107">Компонент</span><span class="sxs-lookup"><span data-stu-id="f3dde-107">Component</span></span>              | <span data-ttu-id="f3dde-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f3dde-108">Description</span></span>           |
|------------------------|-----------------------|
| <span data-ttu-id="f3dde-109">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="f3dde-109">Formal Name(s)</span></span>         | <span data-ttu-id="f3dde-110">Формат точечных рисунков Windows</span><span class="sxs-lookup"><span data-stu-id="f3dde-110">Windows Bitmap Format</span></span> |
| <span data-ttu-id="f3dde-111">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="f3dde-111">File Name Extension(s)</span></span> | <span data-ttu-id="f3dde-112">BMP, DIB</span><span class="sxs-lookup"><span data-stu-id="f3dde-112">bmp, dib</span></span>              |
| <span data-ttu-id="f3dde-113">тип MIME</span><span class="sxs-lookup"><span data-stu-id="f3dde-113">MIME type</span></span>              | <span data-ttu-id="f3dde-114">image/bmp</span><span class="sxs-lookup"><span data-stu-id="f3dde-114">image/bmp</span></span>             |
| <span data-ttu-id="f3dde-115">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="f3dde-115">Specification Support</span></span>  | <span data-ttu-id="f3dde-116">Спецификация BMP V5</span><span class="sxs-lookup"><span data-stu-id="f3dde-116">BMP Specification v5</span></span>  |



 

<span data-ttu-id="f3dde-117">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания встроенных компонентов кодека BMP.</span><span class="sxs-lookup"><span data-stu-id="f3dde-117">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="f3dde-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="f3dde-118">Component</span></span>        | <span data-ttu-id="f3dde-119">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="f3dde-119">Friendly Name</span></span>            | <span data-ttu-id="f3dde-120">Код GUID</span><span class="sxs-lookup"><span data-stu-id="f3dde-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="f3dde-121">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="f3dde-121">Container Format</span></span> | <span data-ttu-id="f3dde-122">GUID \_ контаинерформатбмп</span><span class="sxs-lookup"><span data-stu-id="f3dde-122">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="f3dde-123">0af1d87e-фкфе-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="f3dde-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="f3dde-124">Показан</span><span class="sxs-lookup"><span data-stu-id="f3dde-124">Decoder</span></span>          | <span data-ttu-id="f3dde-125">\_ВИКБМПДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="f3dde-125">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="f3dde-126">6b462062-7cbf-400d-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="f3dde-126">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="f3dde-127">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="f3dde-127">Encoder</span></span>          | <span data-ttu-id="f3dde-128">\_ВИКБМПЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="f3dde-128">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="f3dde-129">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="f3dde-129">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="f3dde-130">Кодирование</span><span class="sxs-lookup"><span data-stu-id="f3dde-130">Encoding</span></span>

<span data-ttu-id="f3dde-131">API кодирования WIC разработан как независимый от кодека, поэтому кодировка изображения для кодеков с поддержкой WIC практически одинакова.</span><span class="sxs-lookup"><span data-stu-id="f3dde-131">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="f3dde-132">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="f3dde-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="f3dde-133">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="f3dde-133">Encoder Options</span></span>

<span data-ttu-id="f3dde-134">Кодеки с поддержкой WIC отличаются на уровне параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="f3dde-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="f3dde-135">Параметры кодировщика соответствуют возможностям кодировщика изображений, и каждый кодек машинного кода поддерживает набор этих вариантов кодировщика.</span><span class="sxs-lookup"><span data-stu-id="f3dde-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="f3dde-136">Параметры кодировщика могут быть базовыми вариантами, поддерживаемыми для всех кодов, включенных с помощью WIC (хотя и не всегда поддерживаемых), или параметров, относящихся к кодекам.</span><span class="sxs-lookup"><span data-stu-id="f3dde-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="f3dde-137">Для управления этими параметрами кодировки в процессе кодирования компонент WIC использует интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f3dde-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="f3dde-138">Дополнительные сведения об использовании интерфейса **IPropertyBag2** для кодирования WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="f3dde-138">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="f3dde-139">В следующей таблице перечислены параметры кодировщика WIC, поддерживаемые кодеком Native BMP.</span><span class="sxs-lookup"><span data-stu-id="f3dde-139">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="f3dde-140">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="f3dde-140">Property Name</span></span>               | <span data-ttu-id="f3dde-141">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f3dde-141">VARTYPE</span></span>      | <span data-ttu-id="f3dde-142">Диапазон значений:</span><span class="sxs-lookup"><span data-stu-id="f3dde-142">Value Range</span></span>                      | <span data-ttu-id="f3dde-143">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f3dde-143">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="f3dde-144">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="f3dde-144">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="f3dde-145">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="f3dde-145">**VT\_BOOL**</span></span> | <span data-ttu-id="f3dde-146">**ВАРИАНТ \_ true/Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="f3dde-146">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="f3dde-147">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="f3dde-147">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="f3dde-148">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="f3dde-148">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="f3dde-149">Указывает, разрешено ли кодирование данных в \_ формате GUID WICPixelFormat32bppBGRA пикселей.</span><span class="sxs-lookup"><span data-stu-id="f3dde-149">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="f3dde-150">Если этот параметр имеет значение **\_ true**, BMP будет записан с заголовком BITMAPV5HEADER.</span><span class="sxs-lookup"><span data-stu-id="f3dde-150">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="f3dde-151">Значение по умолчанию — **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="f3dde-151">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="f3dde-152">Если в списке параметров IPropertyBag2 есть параметр кодировщика, который не поддерживается кодеком, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f3dde-152">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="f3dde-153">Примечание для 16-разрядных и 32-разрядных файлов Windows BMP кодек BMP игнорирует любой альфа-канал, так как многие файлы образов прежних версий содержат недопустимые данные в этом дополнительный канал.</span><span class="sxs-lookup"><span data-stu-id="f3dde-153">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="f3dde-154">Начиная с Windows 8, 32-разрядные файлы Windows BMP, написанные с помощью **BITMAPV5HEADER** с допустимым содержимым альфа-канала, считываются как WICPixelFormat32bppBGRA.</span><span class="sxs-lookup"><span data-stu-id="f3dde-154">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="f3dde-155">Декодирование</span><span class="sxs-lookup"><span data-stu-id="f3dde-155">Decoding</span></span>

<span data-ttu-id="f3dde-156">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="f3dde-156">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="f3dde-157">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="f3dde-157">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="f3dde-158">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="f3dde-158">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
