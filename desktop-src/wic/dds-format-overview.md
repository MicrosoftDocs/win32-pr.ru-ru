---
description: Содержит сведения о кодека машинного кода DDS, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Общие сведения о формате DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693130"
---
# <a name="dds-format-overview"></a><span data-ttu-id="9cf78-103">Общие сведения о формате DDS</span><span class="sxs-lookup"><span data-stu-id="9cf78-103">DDS Format Overview</span></span>

<span data-ttu-id="9cf78-104">В этом разделе содержатся сведения о кодека машинного кода DDS, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="9cf78-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="9cf78-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="9cf78-105">Codec Identity</span></span>

<span data-ttu-id="9cf78-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="9cf78-106">The following table provides codec identification information.</span></span>



|                        |                    |
|------------------------|--------------------|
| <span data-ttu-id="9cf78-107">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="9cf78-107">Formal Name(s)</span></span>         | <span data-ttu-id="9cf78-108">Поверхность DirectDraw</span><span class="sxs-lookup"><span data-stu-id="9cf78-108">DirectDraw Surface</span></span> |
| <span data-ttu-id="9cf78-109">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="9cf78-109">File Name Extension(s)</span></span> | <span data-ttu-id="9cf78-110">набора</span><span class="sxs-lookup"><span data-stu-id="9cf78-110">dds</span></span>                |
| <span data-ttu-id="9cf78-111">тип MIME</span><span class="sxs-lookup"><span data-stu-id="9cf78-111">MIME type</span></span>              | <span data-ttu-id="9cf78-112">Image/ВНД-МС. DDS</span><span class="sxs-lookup"><span data-stu-id="9cf78-112">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="9cf78-113">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека DDS.</span><span class="sxs-lookup"><span data-stu-id="9cf78-113">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="9cf78-114">Компонент</span><span class="sxs-lookup"><span data-stu-id="9cf78-114">Component</span></span>        | <span data-ttu-id="9cf78-115">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="9cf78-115">Friendly Name</span></span>            | <span data-ttu-id="9cf78-116">Код GUID</span><span class="sxs-lookup"><span data-stu-id="9cf78-116">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="9cf78-117">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="9cf78-117">Container Format</span></span> | <span data-ttu-id="9cf78-118">GUID \_ контаинерформатддс</span><span class="sxs-lookup"><span data-stu-id="9cf78-118">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="9cf78-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="9cf78-119">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="9cf78-120">Показан</span><span class="sxs-lookup"><span data-stu-id="9cf78-120">Decoder</span></span>          | <span data-ttu-id="9cf78-121">\_ВИКДДСДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="9cf78-121">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="9cf78-122">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="9cf78-122">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="9cf78-123">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="9cf78-123">Encoder</span></span>          | <span data-ttu-id="9cf78-124">\_ВИКДДСЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="9cf78-124">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="9cf78-125">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="9cf78-125">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="9cf78-126">Поддержка формата пикселей</span><span class="sxs-lookup"><span data-stu-id="9cf78-126">Pixel Format Support</span></span>

<span data-ttu-id="9cf78-127">Обратите внимание, что формат DDS поддерживает любое допустимое значение [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="9cf78-127">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="9cf78-128">Однако кодек для набора WIC DDS поддерживает декодирование и кодирование файлов, содержащих следующие форматы:</span><span class="sxs-lookup"><span data-stu-id="9cf78-128">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="9cf78-129">\_Формат DXGI \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9cf78-129">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="9cf78-130">\_Формат DXGI \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9cf78-130">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="9cf78-131">\_Формат DXGI \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9cf78-131">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="9cf78-132">Кодирование</span><span class="sxs-lookup"><span data-stu-id="9cf78-132">Encoding</span></span>

<span data-ttu-id="9cf78-133">Интерфейсы API кодирования WIC не зависят от кодека, поэтому кодирование изображений для кодеков с поддержкой WIC по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="9cf78-133">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9cf78-134">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9cf78-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="9cf78-135">Формат файла DDS имеет уникальные требования, связанные с поддержкой таких концепций, как MIP-карты и массивы текстур.</span><span class="sxs-lookup"><span data-stu-id="9cf78-135">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="9cf78-136">Чтобы полностью проделать Управление кодированием образа DDS, следует использовать интерфейс [**ивикддсенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) для установки параметров кодировки, специфичных для DDS.</span><span class="sxs-lookup"><span data-stu-id="9cf78-136">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="9cf78-137">Декодирование</span><span class="sxs-lookup"><span data-stu-id="9cf78-137">Decoding</span></span>

<span data-ttu-id="9cf78-138">Интерфейсы API декодирования WIC не зависят от кодека и декодирование изображений для кодеков с поддержкой WIC по сути являются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="9cf78-138">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9cf78-139">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="9cf78-139">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="9cf78-140">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="9cf78-140">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="9cf78-141">Блокировать доступ к сжатым данным</span><span class="sxs-lookup"><span data-stu-id="9cf78-141">Block compressed data access</span></span>

<span data-ttu-id="9cf78-142">Помимо поддержки стандартных интерфейсов кодеков WIC, декодер DDS предоставляет прямой доступ к сжатым блочным данным с помощью интерфейсов, зависящих от DDS, [**ивикддсдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) и [**ивикддсфрамедекоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span><span class="sxs-lookup"><span data-stu-id="9cf78-142">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="9cf78-143">Чтобы использовать эти интерфейсы, вызовите метод QueryInterface из [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) и [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)соответственно.</span><span class="sxs-lookup"><span data-stu-id="9cf78-143">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
