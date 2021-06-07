---
description: В этом разделе содержатся сведения о коде встроенного GIF, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Общие сведения о формате GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf7e9924c921b7944de114f5fe667cb2aa33cae
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444455"
---
# <a name="gif-format-overview"></a><span data-ttu-id="9ba7b-103">Общие сведения о формате GIF</span><span class="sxs-lookup"><span data-stu-id="9ba7b-103">GIF Format Overview</span></span>

<span data-ttu-id="9ba7b-104">В этом разделе содержатся сведения о коде встроенного GIF, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="9ba7b-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="9ba7b-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="9ba7b-105">Codec Identity</span></span>

<span data-ttu-id="9ba7b-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="9ba7b-106">The following table provides codec identification information.</span></span>



|  <span data-ttu-id="9ba7b-107">Компонент</span><span class="sxs-lookup"><span data-stu-id="9ba7b-107">Component</span></span>             | <span data-ttu-id="9ba7b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9ba7b-108">Description</span></span>                           |
|------------------------|---------------------------------------|
| <span data-ttu-id="9ba7b-109">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="9ba7b-109">Formal Name(s)</span></span>         | <span data-ttu-id="9ba7b-110">Графический формат обмена 89A (GIF)</span><span class="sxs-lookup"><span data-stu-id="9ba7b-110">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="9ba7b-111">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="9ba7b-111">File Name Extension(s)</span></span> | <span data-ttu-id="9ba7b-112">GIF</span><span class="sxs-lookup"><span data-stu-id="9ba7b-112">gif</span></span>                                   |
| <span data-ttu-id="9ba7b-113">тип MIME</span><span class="sxs-lookup"><span data-stu-id="9ba7b-113">MIME type</span></span>              | <span data-ttu-id="9ba7b-114">image/gif</span><span class="sxs-lookup"><span data-stu-id="9ba7b-114">image/gif</span></span>                             |
| <span data-ttu-id="9ba7b-115">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="9ba7b-115">Specification Support</span></span>  | <span data-ttu-id="9ba7b-116">Спецификация GIF 89A/89m</span><span class="sxs-lookup"><span data-stu-id="9ba7b-116">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="9ba7b-117">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания встроенных компонентов кодека GIF.</span><span class="sxs-lookup"><span data-stu-id="9ba7b-117">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="9ba7b-118">Компонент</span><span class="sxs-lookup"><span data-stu-id="9ba7b-118">Component</span></span>        | <span data-ttu-id="9ba7b-119">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="9ba7b-119">Friendly Name</span></span>            | <span data-ttu-id="9ba7b-120">Код GUID</span><span class="sxs-lookup"><span data-stu-id="9ba7b-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="9ba7b-121">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="9ba7b-121">Container Format</span></span> | <span data-ttu-id="9ba7b-122">GUID \_ контаинерформатгиф</span><span class="sxs-lookup"><span data-stu-id="9ba7b-122">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="9ba7b-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="9ba7b-123">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="9ba7b-124">Показан</span><span class="sxs-lookup"><span data-stu-id="9ba7b-124">Decoder</span></span>          | <span data-ttu-id="9ba7b-125">\_ВИКГИФДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="9ba7b-125">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="9ba7b-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="9ba7b-126">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="9ba7b-127">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="9ba7b-127">Encoder</span></span>          | <span data-ttu-id="9ba7b-128">\_ВИКГИФЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="9ba7b-128">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="9ba7b-129">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="9ba7b-129">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="9ba7b-130">Кодирование</span><span class="sxs-lookup"><span data-stu-id="9ba7b-130">Encoding</span></span>

<span data-ttu-id="9ba7b-131">API кодирования WIC разработан как независимый от кодека, а кодировка изображений для кодеков с поддержкой WIC практически одинакова.</span><span class="sxs-lookup"><span data-stu-id="9ba7b-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9ba7b-132">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9ba7b-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="9ba7b-133">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="9ba7b-133">Encoder Options</span></span>

<span data-ttu-id="9ba7b-134">Кодеки с поддержкой WIC отличаются на уровне параметров кодировки.</span><span class="sxs-lookup"><span data-stu-id="9ba7b-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="9ba7b-135">Параметры кодировщика соответствуют возможностям кодировщика изображений, и каждый кодек машинного кода поддерживает набор этих вариантов кодировщика.</span><span class="sxs-lookup"><span data-stu-id="9ba7b-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="9ba7b-136">Параметры кодировщика могут быть базовыми вариантами, поддерживаемыми для всех кодов, включенных с помощью WIC (хотя и не всегда поддерживаемых), или параметров, относящихся к кодекам.</span><span class="sxs-lookup"><span data-stu-id="9ba7b-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="9ba7b-137">Для управления этими параметрами кодировки в процессе кодирования компонент WIC использует интерфейс [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9ba7b-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="9ba7b-138">Дополнительные сведения об использовании интерфейса **IPropertyBag2** для кодирования WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9ba7b-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="9ba7b-139">Кодировщик GIF не поддерживает основные параметры WIC и не предоставляет настраиваемые параметры кодировщика.</span><span class="sxs-lookup"><span data-stu-id="9ba7b-139">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="9ba7b-140">Если параметр кодировщика находится в списке параметров [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9ba7b-140">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="9ba7b-141">Декодирование</span><span class="sxs-lookup"><span data-stu-id="9ba7b-141">Decoding</span></span>

<span data-ttu-id="9ba7b-142">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="9ba7b-142">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9ba7b-143">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="9ba7b-143">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="9ba7b-144">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="9ba7b-144">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
