---
description: В этом разделе рассматриваются разработчики с рекомендациями по внедрению кодеков формата файлов изображений, которые будут работать в инфраструктуре компонента Windows Imaging Component (WIC).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Написание WIC-Enabled кодека
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910168"
---
# <a name="how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="bff8e-103">Написание WIC-Enabled кодека</span><span class="sxs-lookup"><span data-stu-id="bff8e-103">How to Write a WIC-Enabled Codec</span></span>

<span data-ttu-id="bff8e-104">В этом разделе рассматриваются разработчики с рекомендациями по внедрению кодеков формата файлов изображений, которые будут работать в инфраструктуре компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="bff8e-104">This section of topics provide developers with guidance on how to implement image file format codecs that will function within the Windows Imaging Component (WIC) framework.</span></span>

<dl>

[<span data-ttu-id="bff8e-105">Введение</span><span class="sxs-lookup"><span data-stu-id="bff8e-105">Introduction</span></span>](-wic-howtowriteacodec-intro.md)  
[<span data-ttu-id="bff8e-106">Принцип работы компонента Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="bff8e-106">How The Windows Imaging Component (WIC) Works</span></span>](-wic-howwicworks.md)  
<dl>

[<span data-ttu-id="bff8e-107">Обнаружение и арбитраж</span><span class="sxs-lookup"><span data-stu-id="bff8e-107">Discovery and Arbitration</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="bff8e-108">Декодирование</span><span class="sxs-lookup"><span data-stu-id="bff8e-108">Decoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="bff8e-109">Кодирование</span><span class="sxs-lookup"><span data-stu-id="bff8e-109">Encoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="bff8e-110">Время существования кодека</span><span class="sxs-lookup"><span data-stu-id="bff8e-110">The Lifetime of a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="bff8e-111">Как WIC — включение кодека</span><span class="sxs-lookup"><span data-stu-id="bff8e-111">How to WIC-enable a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="bff8e-112">Поддержка многопоточных подразделений в WIC</span><span class="sxs-lookup"><span data-stu-id="bff8e-112">Multi-Threaded Apartment Support in WIC</span></span>](-wic-howwicworks.md)  
<span data-ttu-id="bff8e-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Реализация декодера WIC-Enabled</a></span><span class="sxs-lookup"><span data-stu-id="bff8e-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementing a WIC-Enabled Decoder</a></span></span><dl>

[<span data-ttu-id="bff8e-114">Интерфейсы декодера</span><span class="sxs-lookup"><span data-stu-id="bff8e-114">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)<dl>

[<span data-ttu-id="bff8e-115">ивикбитмапдекодер</span><span class="sxs-lookup"><span data-stu-id="bff8e-115">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)  
[<span data-ttu-id="bff8e-116">ивикбитмапкодекпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="bff8e-116">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[<span data-ttu-id="bff8e-117">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="bff8e-117">IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)  
[<span data-ttu-id="bff8e-118">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="bff8e-118">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)  
[<span data-ttu-id="bff8e-119">ивикметадатаблоккреадер</span><span class="sxs-lookup"><span data-stu-id="bff8e-119">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)  
[<span data-ttu-id="bff8e-120">ивикбитмапсаурцетрансформ</span><span class="sxs-lookup"><span data-stu-id="bff8e-120">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)  
[<span data-ttu-id="bff8e-121">ивикдевелоправ</span><span class="sxs-lookup"><span data-stu-id="bff8e-121">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)  
<span data-ttu-id="bff8e-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Реализация кодировщика WIC-Enabled</a>  
</span><span class="sxs-lookup"><span data-stu-id="bff8e-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementing a WIC-Enabled Encoder</a>  
</span></span><dl>

[<span data-ttu-id="bff8e-123">Интерфейсы кодировщика</span><span class="sxs-lookup"><span data-stu-id="bff8e-123">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)  
<dl>

[<span data-ttu-id="bff8e-124">ивикбитмапенкодер</span><span class="sxs-lookup"><span data-stu-id="bff8e-124">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)  
[<span data-ttu-id="bff8e-125">ивикбитмапкодекпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="bff8e-125">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[<span data-ttu-id="bff8e-126">ивикбитмапфраминкоде</span><span class="sxs-lookup"><span data-stu-id="bff8e-126">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)  
[<span data-ttu-id="bff8e-127">ивикметадатаблокквритер</span><span class="sxs-lookup"><span data-stu-id="bff8e-127">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)  
<span data-ttu-id="bff8e-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Установка и регистрация кодека</a>  
</span><span class="sxs-lookup"><span data-stu-id="bff8e-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Codec Installation and Registration</a>  
</span></span><dl>

[<span data-ttu-id="bff8e-129">Регистрация кодека</span><span class="sxs-lookup"><span data-stu-id="bff8e-129">Registering a Codec</span></span>](-wic-codecinstallandreg.md)  
<dl>

[<span data-ttu-id="bff8e-130">Общие записи регистров</span><span class="sxs-lookup"><span data-stu-id="bff8e-130">General Register Entries</span></span>](-wic-generalregentries.md)  
[<span data-ttu-id="bff8e-131">Записи реестра, относящиеся к кодировщику</span><span class="sxs-lookup"><span data-stu-id="bff8e-131">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)  
<dl>

[<span data-ttu-id="bff8e-132">Регистрация формата контейнера с помощью модулей записи метаданных</span><span class="sxs-lookup"><span data-stu-id="bff8e-132">Registering a Container Format with Metadata Writers</span></span>](-wic-encoderregentries.md)  
<span data-ttu-id="bff8e-133"></dl> </dd> <a href="-wic-decoderregentries.md">Записи реестра, относящиеся к кодировщику</a>  
</span><span class="sxs-lookup"><span data-stu-id="bff8e-133"></dl> </dd> <a href="-wic-decoderregentries.md">Encoder-Specific Registry Entries</a>  
</span></span><dl>

[<span data-ttu-id="bff8e-134">Регистрация нового формата контейнера с помощью средств чтения метаданных</span><span class="sxs-lookup"><span data-stu-id="bff8e-134">Registering a New Container Format with Metadata Readers</span></span>](-wic-decoderregentries.md)  
<span data-ttu-id="bff8e-135"></dl> </dd> <a href="-wic-integrationregentries.md">Интеграция с Windows Vista Фотогаллери и проводник</a>  
</span><span class="sxs-lookup"><span data-stu-id="bff8e-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integration with Windows Vista PhotoGallery and Explorer</a>  
</span></span><dl>

[<span data-ttu-id="bff8e-136">Хранилище свойств Windows</span><span class="sxs-lookup"><span data-stu-id="bff8e-136">Windows Property Store</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="bff8e-137">Фотоальбом Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bff8e-137">Windows Vista Photo Gallery</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="bff8e-138">Кэш эскизов Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bff8e-138">Windows Vista Thumbnail Cache</span></span>](-wic-integrationregentries.md)  
<span data-ttu-id="bff8e-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Обновление кэша эскизов при установке кодека,</a> [делающей WIC-Enabled кодек, доступный для пользователей](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md"></a>  
</span><span class="sxs-lookup"><span data-stu-id="bff8e-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Updating the Thumbnail Cache when Installing a Codec</a> [Making Your WIC-Enabled Codec Available to Users](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">Conclusion</a>  
</span></span></dl>

## <a name="related-topics"></a><span data-ttu-id="bff8e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="bff8e-140">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bff8e-141">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="bff8e-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bff8e-142">Введение (написание WIC-Enabled КОДЕка)</span><span class="sxs-lookup"><span data-stu-id="bff8e-142">Introduction (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[<span data-ttu-id="bff8e-143">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="bff8e-143">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



