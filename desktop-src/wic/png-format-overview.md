---
description: Этот раздел содержит сведения о коде встроенного кода PNG, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Общие сведения о формате PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444445"
---
# <a name="png-format-overview"></a><span data-ttu-id="c7040-103">Общие сведения о формате PNG</span><span class="sxs-lookup"><span data-stu-id="c7040-103">PNG Format Overview</span></span>

<span data-ttu-id="c7040-104">Этот раздел содержит сведения о коде встроенного кода PNG, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="c7040-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="c7040-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="c7040-105">Codec Identity</span></span>

<span data-ttu-id="c7040-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="c7040-106">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="c7040-107">Компонент</span><span class="sxs-lookup"><span data-stu-id="c7040-107">Component</span></span>          | <span data-ttu-id="c7040-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c7040-108">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="c7040-109">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="c7040-109">Formal Name(s)</span></span>         | <span data-ttu-id="c7040-110">PNG</span><span class="sxs-lookup"><span data-stu-id="c7040-110">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="c7040-111">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="c7040-111">File Name Extension(s)</span></span> | <span data-ttu-id="c7040-112">png</span><span class="sxs-lookup"><span data-stu-id="c7040-112">png</span></span>                             |
| <span data-ttu-id="c7040-113">тип MIME</span><span class="sxs-lookup"><span data-stu-id="c7040-113">MIME type</span></span>              | <span data-ttu-id="c7040-114">image/png</span><span class="sxs-lookup"><span data-stu-id="c7040-114">image/png</span></span>                       |
| <span data-ttu-id="c7040-115">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="c7040-115">Specification Support</span></span>  | <span data-ttu-id="c7040-116">Спецификация PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="c7040-116">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="c7040-117">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека PNG.</span><span class="sxs-lookup"><span data-stu-id="c7040-117">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="c7040-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="c7040-118">Component</span></span>        | <span data-ttu-id="c7040-119">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="c7040-119">Friendly Name</span></span>            | <span data-ttu-id="c7040-120">Код GUID</span><span class="sxs-lookup"><span data-stu-id="c7040-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="c7040-121">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="c7040-121">Container Format</span></span> | <span data-ttu-id="c7040-122">GUID \_ контаинерформатпнг</span><span class="sxs-lookup"><span data-stu-id="c7040-122">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="c7040-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="c7040-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="c7040-124">Показан</span><span class="sxs-lookup"><span data-stu-id="c7040-124">Decoder</span></span>          | <span data-ttu-id="c7040-125">\_ВИКПНГДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="c7040-125">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="c7040-126">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="c7040-126">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="c7040-127">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="c7040-127">Encoder</span></span>          | <span data-ttu-id="c7040-128">\_ВИКПНЖЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="c7040-128">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="c7040-129">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="c7040-129">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="c7040-130">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="c7040-130">Windows 8 and later</span></span>

<span data-ttu-id="c7040-131">Начиная с Windows 8 WIC предоставляет дополнительный декодер PNG</span><span class="sxs-lookup"><span data-stu-id="c7040-131">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="c7040-132">Кодирование</span><span class="sxs-lookup"><span data-stu-id="c7040-132">Encoding</span></span>

<span data-ttu-id="c7040-133">API кодирования WIC разработан как независимый от кодека, а кодировка изображений для кодеков с поддержкой WIC практически одинакова.</span><span class="sxs-lookup"><span data-stu-id="c7040-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="c7040-134">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c7040-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="c7040-135">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="c7040-135">Encoder Options</span></span>

<span data-ttu-id="c7040-136">Кодеки с поддержкой WIC отличаются на уровне параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="c7040-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="c7040-137">Параметры кодировщика соответствуют возможностям кодировщика изображений, и каждый кодек машинного кода поддерживает набор этих вариантов кодировщика.</span><span class="sxs-lookup"><span data-stu-id="c7040-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="c7040-138">Параметры кодировщика могут быть базовыми вариантами, поддерживаемыми для всех кодов, включенных с помощью WIC (хотя и не всегда поддерживаемых), или параметров, относящихся к кодекам.</span><span class="sxs-lookup"><span data-stu-id="c7040-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="c7040-139">Для управления этими параметрами кодировки в процессе кодирования компонент WIC использует интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c7040-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="c7040-140">Дополнительные сведения об использовании интерфейса **IPropertyBag2** для кодирования WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c7040-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="c7040-141">Кодек PNG использует основные параметры кодировщика WIC.</span><span class="sxs-lookup"><span data-stu-id="c7040-141">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="c7040-142">В следующей таблице перечислены параметры кодировщика WIC, поддерживаемые кодеком машинного кода PNG.</span><span class="sxs-lookup"><span data-stu-id="c7040-142">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="c7040-143">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="c7040-143">Property Name</span></span>   | <span data-ttu-id="c7040-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c7040-144">VARTYPE</span></span>  | <span data-ttu-id="c7040-145">Диапазон значений:</span><span class="sxs-lookup"><span data-stu-id="c7040-145">Value Range</span></span>                                                 | <span data-ttu-id="c7040-146">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c7040-146">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c7040-147">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="c7040-147">InterlaceOption</span></span> | <span data-ttu-id="c7040-148">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="c7040-148">VT\_BOOL</span></span> | <span data-ttu-id="c7040-149">**Значение true** / **Значение false**</span><span class="sxs-lookup"><span data-stu-id="c7040-149">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="c7040-150">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c7040-150">**FALSE**</span></span>                                                        |
| <span data-ttu-id="c7040-151">FilterOption</span><span class="sxs-lookup"><span data-stu-id="c7040-151">FilterOption</span></span>    | <span data-ttu-id="c7040-152">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="c7040-152">VT\_UI1</span></span>  | [<span data-ttu-id="c7040-153">**викпнгфилтероптион**</span><span class="sxs-lookup"><span data-stu-id="c7040-153">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="c7040-154">**викпнгфилтерунспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="c7040-154">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="c7040-155">Если в списке параметров [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) есть параметр кодировщика, который не поддерживается кодеком, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c7040-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="c7040-156">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="c7040-156">InterlaceOption</span></span>

<span data-ttu-id="c7040-157">Указывает, следует ли кодировать данные изображения в виде чередования.</span><span class="sxs-lookup"><span data-stu-id="c7040-157">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="c7040-158">Значение по умолчанию — **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="c7040-158">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="c7040-159">FilterOption</span><span class="sxs-lookup"><span data-stu-id="c7040-159">FilterOption</span></span>

<span data-ttu-id="c7040-160">Задает параметр фильтра, используемый для сжатия изображений.</span><span class="sxs-lookup"><span data-stu-id="c7040-160">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="c7040-161">Значение по умолчанию — [**викпнгфилтерунспеЦифиед**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span><span class="sxs-lookup"><span data-stu-id="c7040-161">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="c7040-162">Декодирование</span><span class="sxs-lookup"><span data-stu-id="c7040-162">Decoding</span></span>

<span data-ttu-id="c7040-163">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="c7040-163">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="c7040-164">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="c7040-164">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="c7040-165">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="c7040-165">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="c7040-166">Собственный кодек PNG также поддерживает [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) при декодировании кадров, добавляя дополнительные параметры для декодирования потока изображений.</span><span class="sxs-lookup"><span data-stu-id="c7040-166">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="c7040-167">Дополнительные сведения об этих дополнительных параметрах см. в разделе [Обзор источников битовой карты](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="c7040-167">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
