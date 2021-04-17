---
description: Этот раздел содержит сведения о коде встроенного кода PNG, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Общие сведения о формате PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702780"
---
# <a name="png-format-overview"></a><span data-ttu-id="8f201-103">Общие сведения о формате PNG</span><span class="sxs-lookup"><span data-stu-id="8f201-103">PNG Format Overview</span></span>

<span data-ttu-id="8f201-104">Этот раздел содержит сведения о коде встроенного кода PNG, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="8f201-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="8f201-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="8f201-105">Codec Identity</span></span>

<span data-ttu-id="8f201-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="8f201-106">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="8f201-107">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="8f201-107">Formal Name(s)</span></span>         | <span data-ttu-id="8f201-108">PNG</span><span class="sxs-lookup"><span data-stu-id="8f201-108">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="8f201-109">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="8f201-109">File Name Extension(s)</span></span> | <span data-ttu-id="8f201-110">png</span><span class="sxs-lookup"><span data-stu-id="8f201-110">png</span></span>                             |
| <span data-ttu-id="8f201-111">тип MIME</span><span class="sxs-lookup"><span data-stu-id="8f201-111">MIME type</span></span>              | <span data-ttu-id="8f201-112">image/png</span><span class="sxs-lookup"><span data-stu-id="8f201-112">image/png</span></span>                       |
| <span data-ttu-id="8f201-113">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="8f201-113">Specification Support</span></span>  | <span data-ttu-id="8f201-114">Спецификация PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="8f201-114">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="8f201-115">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека PNG.</span><span class="sxs-lookup"><span data-stu-id="8f201-115">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="8f201-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="8f201-116">Component</span></span>        | <span data-ttu-id="8f201-117">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="8f201-117">Friendly Name</span></span>            | <span data-ttu-id="8f201-118">Код GUID</span><span class="sxs-lookup"><span data-stu-id="8f201-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="8f201-119">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="8f201-119">Container Format</span></span> | <span data-ttu-id="8f201-120">GUID \_ контаинерформатпнг</span><span class="sxs-lookup"><span data-stu-id="8f201-120">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="8f201-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="8f201-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="8f201-122">Показан</span><span class="sxs-lookup"><span data-stu-id="8f201-122">Decoder</span></span>          | <span data-ttu-id="8f201-123">\_ВИКПНГДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="8f201-123">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="8f201-124">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="8f201-124">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="8f201-125">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="8f201-125">Encoder</span></span>          | <span data-ttu-id="8f201-126">\_ВИКПНЖЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="8f201-126">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="8f201-127">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="8f201-127">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="8f201-128">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="8f201-128">Windows 8 and later</span></span>

<span data-ttu-id="8f201-129">Начиная с Windows 8 WIC предоставляет дополнительный декодер PNG</span><span class="sxs-lookup"><span data-stu-id="8f201-129">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="8f201-130">Кодирование</span><span class="sxs-lookup"><span data-stu-id="8f201-130">Encoding</span></span>

<span data-ttu-id="8f201-131">API кодирования WIC разработан как независимый от кодека, а кодировка изображений для кодеков с поддержкой WIC практически одинакова.</span><span class="sxs-lookup"><span data-stu-id="8f201-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8f201-132">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="8f201-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="8f201-133">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="8f201-133">Encoder Options</span></span>

<span data-ttu-id="8f201-134">Кодеки с поддержкой WIC отличаются на уровне параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="8f201-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="8f201-135">Параметры кодировщика соответствуют возможностям кодировщика изображений, и каждый кодек машинного кода поддерживает набор этих вариантов кодировщика.</span><span class="sxs-lookup"><span data-stu-id="8f201-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="8f201-136">Параметры кодировщика могут быть базовыми вариантами, поддерживаемыми для всех кодов, включенных с помощью WIC (хотя и не всегда поддерживаемых), или параметров, относящихся к кодекам.</span><span class="sxs-lookup"><span data-stu-id="8f201-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="8f201-137">Для управления этими параметрами кодировки в процессе кодирования компонент WIC использует интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8f201-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="8f201-138">Дополнительные сведения об использовании интерфейса **IPropertyBag2** для кодирования WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="8f201-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="8f201-139">Кодек PNG использует основные параметры кодировщика WIC.</span><span class="sxs-lookup"><span data-stu-id="8f201-139">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="8f201-140">В следующей таблице перечислены параметры кодировщика WIC, поддерживаемые кодеком машинного кода PNG.</span><span class="sxs-lookup"><span data-stu-id="8f201-140">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="8f201-141">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="8f201-141">Property Name</span></span>   | <span data-ttu-id="8f201-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8f201-142">VARTYPE</span></span>  | <span data-ttu-id="8f201-143">Диапазон значений:</span><span class="sxs-lookup"><span data-stu-id="8f201-143">Value Range</span></span>                                                 | <span data-ttu-id="8f201-144">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f201-144">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="8f201-145">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="8f201-145">InterlaceOption</span></span> | <span data-ttu-id="8f201-146">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="8f201-146">VT\_BOOL</span></span> | <span data-ttu-id="8f201-147">**Значение true** / **Значение false**</span><span class="sxs-lookup"><span data-stu-id="8f201-147">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="8f201-148">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8f201-148">**FALSE**</span></span>                                                        |
| <span data-ttu-id="8f201-149">FilterOption</span><span class="sxs-lookup"><span data-stu-id="8f201-149">FilterOption</span></span>    | <span data-ttu-id="8f201-150">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="8f201-150">VT\_UI1</span></span>  | [<span data-ttu-id="8f201-151">**викпнгфилтероптион**</span><span class="sxs-lookup"><span data-stu-id="8f201-151">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="8f201-152">**викпнгфилтерунспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="8f201-152">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="8f201-153">Если в списке параметров [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) есть параметр кодировщика, который не поддерживается кодеком, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8f201-153">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="8f201-154">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="8f201-154">InterlaceOption</span></span>

<span data-ttu-id="8f201-155">Указывает, следует ли кодировать данные изображения в виде чередования.</span><span class="sxs-lookup"><span data-stu-id="8f201-155">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="8f201-156">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="8f201-156">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="8f201-157">FilterOption</span><span class="sxs-lookup"><span data-stu-id="8f201-157">FilterOption</span></span>

<span data-ttu-id="8f201-158">Задает параметр фильтра, используемый для сжатия изображений.</span><span class="sxs-lookup"><span data-stu-id="8f201-158">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="8f201-159">Значение по умолчанию — [**викпнгфилтерунспеЦифиед**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span><span class="sxs-lookup"><span data-stu-id="8f201-159">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="8f201-160">Декодирование</span><span class="sxs-lookup"><span data-stu-id="8f201-160">Decoding</span></span>

<span data-ttu-id="8f201-161">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="8f201-161">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="8f201-162">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="8f201-162">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="8f201-163">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="8f201-163">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="8f201-164">Собственный кодек PNG также поддерживает [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) при декодировании кадров, добавляя дополнительные параметры для декодирования потока изображений.</span><span class="sxs-lookup"><span data-stu-id="8f201-164">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="8f201-165">Дополнительные сведения об этих дополнительных параметрах см. в разделе [Обзор источников битовой карты](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="8f201-165">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
