---
description: Поддержка метаданных
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Поддержка метаданных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702737"
---
# <a name="metadata-support"></a><span data-ttu-id="049d5-103">Поддержка метаданных</span><span class="sxs-lookup"><span data-stu-id="049d5-103">Metadata Support</span></span>

<span data-ttu-id="049d5-104">Форматы RAW также должны поддерживать общие сценарии чтения и записи метаданных для изображений в Windows.</span><span class="sxs-lookup"><span data-stu-id="049d5-104">RAW formats should also support the common metadata read and write scenarios for images in Windows.</span></span> <span data-ttu-id="049d5-105">Корпорация Майкрософт разработала набор собственных поставщиков метаданных для файла с файлами изображений (EXIF), Международного Совета по Прессским коммуникациям (IPTC) и метаданных XMP, которые в настоящее время вызываются только для контейнеров TIFF и JPEG.</span><span class="sxs-lookup"><span data-stu-id="049d5-105">Microsoft has developed a set of native metadata providers for exchangeable image file (EXIF), International Press Telecommunications Council (IPTC), and Extensible Metadata Platform (XMP) metadata that are currently invoked only for TIFF and JPEG containers.</span></span> <span data-ttu-id="049d5-106">Если необработанный образ хранится в одном из этих форматов контейнеров, рекомендуется использовать встроенные поставщики метаданных Windows.</span><span class="sxs-lookup"><span data-stu-id="049d5-106">If the RAW image is stored in one of these container formats, it is recommended to use the Windows built-in metadata providers.</span></span> <span data-ttu-id="049d5-107">Однако автор кодека отвечает за правильную настройку.</span><span class="sxs-lookup"><span data-stu-id="049d5-107">However, the codec author is responsible for configuring this properly.</span></span> <span data-ttu-id="049d5-108">Для необработанных файлов, которые не основаны на контейнере TIFF, может потребоваться реализовать модули записи EXIF, IPTC или XMP, так как встроенные средства чтения и записи предполагают, что данные будут соответствовать спецификациям макета на диске EXIF, IPTC и XMP.</span><span class="sxs-lookup"><span data-stu-id="049d5-108">For RAW files that are not based on a TIFF container, it might be necessary to implement EXIF, IPTC, or XMP writers because the built-in readers and writers expect the data to conform to EXIF, IPTC, and XMP on-disk layout specifications.</span></span> <span data-ttu-id="049d5-109">Авторы кодеков также могут реализовать собственные поставщики для любых пользовательских метаданных.</span><span class="sxs-lookup"><span data-stu-id="049d5-109">Codec authors can also implement their own providers for any custom metadata.</span></span>

<span data-ttu-id="049d5-110">Из-за архитектуры компонента Windows Imaging Component (WIC) средства записи метаданных могут вызываться только через экземпляр кодировщика изображений.</span><span class="sxs-lookup"><span data-stu-id="049d5-110">Because of the architecture of Windows Imaging Component (WIC), metadata writers can be invoked only through an instance of an image encoder.</span></span> <span data-ttu-id="049d5-111">Поэтому владельцы формата RAW должны создать по крайней мере "заглушку" [**викравпараметерсет. викаутоаджустедпараметерсет**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) кодировщик, даже если фактическая кодировка пикселей в необработанном формате не реализована.</span><span class="sxs-lookup"><span data-stu-id="049d5-111">Therefore, RAW format owners should create at least a "stub" [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) encoder, even if the actual encoding of pixels into a RAW format is not implemented.</span></span> <span data-ttu-id="049d5-112">Автор кодека должен вызывать правильные обработчики метаданных:</span><span class="sxs-lookup"><span data-stu-id="049d5-112">The codec author must invoke the proper metadata handlers:</span></span>

-   <span data-ttu-id="049d5-113">[**Ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) как для декодера, так и для декодера кадров.</span><span class="sxs-lookup"><span data-stu-id="049d5-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on both the decoder and frame decoder as appropriate.</span></span>
-   <span data-ttu-id="049d5-114">[**Ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) кодировщика и кодировщика фреймов соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="049d5-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on both the encoder and frame encoder as appropriate.</span></span>

<span data-ttu-id="049d5-115">Для поддержки всех ожидаемых сценариев в приложениях для работы с образами в Windows Vista рекомендуется, чтобы поставщики кодеков поддерживали следующее как минимум:</span><span class="sxs-lookup"><span data-stu-id="049d5-115">To support all of the anticipated scenarios in imaging applications in Windows Vista, it is recommended that codec vendors support the following at a minimum:</span></span>

-   <span data-ttu-id="049d5-116">Чтение EXIF</span><span class="sxs-lookup"><span data-stu-id="049d5-116">EXIF read</span></span>
-   <span data-ttu-id="049d5-117">Частичная запись EXIF (для разрешения обновления даты и времени записи)</span><span class="sxs-lookup"><span data-stu-id="049d5-117">Partial EXIF write (to permit updates to capture date and time)</span></span>
-   <span data-ttu-id="049d5-118">Чтение и запись XMP (включая, возможно, IPTC Core для XMP)</span><span class="sxs-lookup"><span data-stu-id="049d5-118">XMP read and write (including optionally IPTC Core for XMP)</span></span>
-   <span data-ttu-id="049d5-119">Чтение и запись IPTC IIMv4</span><span class="sxs-lookup"><span data-stu-id="049d5-119">IPTC IIMv4 read and write</span></span>

<span data-ttu-id="049d5-120">Большая часть доступа к метаданным (как для чтения, так и для записи) в Windows Vista осуществляется через интерфейс [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) или [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="049d5-120">Most of the metadata access (both read and write) in Windows Vista occurs through the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) or [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interface.</span></span> <span data-ttu-id="049d5-121">Таким образом, чтобы участвовать в работе с метаданными в Windows Vista, авторы необработанных кодеков должны реализовать методы [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) и [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="049d5-121">Therefore, to participate in the Windows Vista metadata experiences, RAW codec authors must implement the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="049d5-122">См. также</span><span class="sxs-lookup"><span data-stu-id="049d5-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="049d5-123">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="049d5-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="049d5-124">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="049d5-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="049d5-125">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="049d5-125">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="049d5-126">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="049d5-126">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



