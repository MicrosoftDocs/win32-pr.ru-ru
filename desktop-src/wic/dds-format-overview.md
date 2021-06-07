---
description: Содержит сведения о кодека машинного кода DDS, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Общие сведения о формате DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f860a5759218575acb53be5f2142e71aa34e9554
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444955"
---
# <a name="dds-format-overview"></a><span data-ttu-id="9a39d-103">Общие сведения о формате DDS</span><span class="sxs-lookup"><span data-stu-id="9a39d-103">DDS Format Overview</span></span>

<span data-ttu-id="9a39d-104">В этом разделе содержатся сведения о кодека машинного кода DDS, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="9a39d-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="9a39d-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="9a39d-105">Codec Identity</span></span>

<span data-ttu-id="9a39d-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="9a39d-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="9a39d-107">Компонент</span><span class="sxs-lookup"><span data-stu-id="9a39d-107">Component</span></span>              | <span data-ttu-id="9a39d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9a39d-108">Description</span></span>        |
|------------------------|--------------------|
| <span data-ttu-id="9a39d-109">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="9a39d-109">Formal Name(s)</span></span>         | <span data-ttu-id="9a39d-110">Поверхность DirectDraw</span><span class="sxs-lookup"><span data-stu-id="9a39d-110">DirectDraw Surface</span></span> |
| <span data-ttu-id="9a39d-111">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="9a39d-111">File Name Extension(s)</span></span> | <span data-ttu-id="9a39d-112">набора</span><span class="sxs-lookup"><span data-stu-id="9a39d-112">dds</span></span>                |
| <span data-ttu-id="9a39d-113">тип MIME</span><span class="sxs-lookup"><span data-stu-id="9a39d-113">MIME type</span></span>              | <span data-ttu-id="9a39d-114">Image/ВНД-МС. DDS</span><span class="sxs-lookup"><span data-stu-id="9a39d-114">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="9a39d-115">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека DDS.</span><span class="sxs-lookup"><span data-stu-id="9a39d-115">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="9a39d-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="9a39d-116">Component</span></span>        | <span data-ttu-id="9a39d-117">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="9a39d-117">Friendly Name</span></span>            | <span data-ttu-id="9a39d-118">Код GUID</span><span class="sxs-lookup"><span data-stu-id="9a39d-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="9a39d-119">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="9a39d-119">Container Format</span></span> | <span data-ttu-id="9a39d-120">GUID \_ контаинерформатддс</span><span class="sxs-lookup"><span data-stu-id="9a39d-120">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="9a39d-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="9a39d-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="9a39d-122">Показан</span><span class="sxs-lookup"><span data-stu-id="9a39d-122">Decoder</span></span>          | <span data-ttu-id="9a39d-123">\_ВИКДДСДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="9a39d-123">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="9a39d-124">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="9a39d-124">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="9a39d-125">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="9a39d-125">Encoder</span></span>          | <span data-ttu-id="9a39d-126">\_ВИКДДСЕНКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="9a39d-126">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="9a39d-127">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="9a39d-127">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="9a39d-128">Поддержка формата пикселей</span><span class="sxs-lookup"><span data-stu-id="9a39d-128">Pixel Format Support</span></span>

<span data-ttu-id="9a39d-129">Обратите внимание, что формат DDS поддерживает любое допустимое значение [**\_ формата DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) .</span><span class="sxs-lookup"><span data-stu-id="9a39d-129">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="9a39d-130">Однако кодек для набора WIC DDS поддерживает декодирование и кодирование файлов, содержащих следующие форматы:</span><span class="sxs-lookup"><span data-stu-id="9a39d-130">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="9a39d-131">\_Формат DXGI \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9a39d-131">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="9a39d-132">\_Формат DXGI \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9a39d-132">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="9a39d-133">\_Формат DXGI \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="9a39d-133">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="9a39d-134">Кодирование</span><span class="sxs-lookup"><span data-stu-id="9a39d-134">Encoding</span></span>

<span data-ttu-id="9a39d-135">Интерфейсы API кодирования WIC не зависят от кодека, поэтому кодирование изображений для кодеков с поддержкой WIC по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="9a39d-135">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9a39d-136">Дополнительные сведения о кодировании изображений с помощью API WIC см. в разделе [Общие сведения о кодировке](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9a39d-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="9a39d-137">Формат файла DDS имеет уникальные требования, связанные с поддержкой таких концепций, как MIP-карты и массивы текстур.</span><span class="sxs-lookup"><span data-stu-id="9a39d-137">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="9a39d-138">Чтобы полностью проделать Управление кодированием образа DDS, следует использовать интерфейс [**ивикддсенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) для установки параметров кодировки, специфичных для DDS.</span><span class="sxs-lookup"><span data-stu-id="9a39d-138">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="9a39d-139">Декодирование</span><span class="sxs-lookup"><span data-stu-id="9a39d-139">Decoding</span></span>

<span data-ttu-id="9a39d-140">Интерфейсы API декодирования WIC не зависят от кодека и декодирование изображений для кодеков с поддержкой WIC по сути являются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="9a39d-140">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9a39d-141">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="9a39d-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="9a39d-142">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="9a39d-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="9a39d-143">Блокировать доступ к сжатым данным</span><span class="sxs-lookup"><span data-stu-id="9a39d-143">Block compressed data access</span></span>

<span data-ttu-id="9a39d-144">Помимо поддержки стандартных интерфейсов кодеков WIC, декодер DDS предоставляет прямой доступ к сжатым блочным данным с помощью интерфейсов, зависящих от DDS, [**ивикддсдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) и [**ивикддсфрамедекоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span><span class="sxs-lookup"><span data-stu-id="9a39d-144">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="9a39d-145">Чтобы использовать эти интерфейсы, вызовите метод QueryInterface из [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) и [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)соответственно.</span><span class="sxs-lookup"><span data-stu-id="9a39d-145">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
