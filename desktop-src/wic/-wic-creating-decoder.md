---
description: В разделе описывается декодер точечных рисунков — основной компонент кодека Windows Imaging Component (WIC), используемый для декодирования файлов изображений из потока.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Общие сведения о декодировании
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349872"
---
# <a name="decoding-overview"></a><span data-ttu-id="14123-103">Общие сведения о декодировании</span><span class="sxs-lookup"><span data-stu-id="14123-103">Decoding Overview</span></span>

<span data-ttu-id="14123-104">В разделе описывается декодер точечных рисунков — основной компонент кодека Windows Imaging Component (WIC), используемый для декодирования файлов изображений из потока.</span><span class="sxs-lookup"><span data-stu-id="14123-104">The topic introduces the bitmap decoder, a core Windows Imaging Component (WIC) codec component used to decode image files from a stream.</span></span>

<span data-ttu-id="14123-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="14123-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="14123-106">Введение</span><span class="sxs-lookup"><span data-stu-id="14123-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="14123-107">Встроенные декодеры битовой карты</span><span class="sxs-lookup"><span data-stu-id="14123-107">Native Bitmap Decoders</span></span>](#native-bitmap-decoders)
-   [<span data-ttu-id="14123-108">Создание растрового декодера</span><span class="sxs-lookup"><span data-stu-id="14123-108">Creating a Bitmap Decoder</span></span>](#creating-a-bitmap-decoder)
-   [<span data-ttu-id="14123-109">Расширяемость декодера</span><span class="sxs-lookup"><span data-stu-id="14123-109">Decoder Extensibility</span></span>](#decoder-extensibility)
-   [<span data-ttu-id="14123-110">См. также</span><span class="sxs-lookup"><span data-stu-id="14123-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="14123-111">Введение</span><span class="sxs-lookup"><span data-stu-id="14123-111">Introduction</span></span>

<span data-ttu-id="14123-112">Растровые декодеры можно просматривать как внешний контейнер цифрового изображения и предоставлять доступ к глобальным свойствам и кадрам изображений.</span><span class="sxs-lookup"><span data-stu-id="14123-112">Bitmap decoders can be viewed as the outer container of a digital image and provides access to global properties and image frames.</span></span> <span data-ttu-id="14123-113">Некоторые форматы изображений поддерживают глобальные эскизы, обзоры, контексты цвета или метаданные, а другие предоставляют эти свойства только на уровне фрейма.</span><span class="sxs-lookup"><span data-stu-id="14123-113">Some image formats support global thumbnails, previews, color contexts, or metadata, while others provide these properties only at the frame level.</span></span> <span data-ttu-id="14123-114">Однако обратите внимание, что многие стандартные форматы изображений не поддерживают эти глобальные свойства.</span><span class="sxs-lookup"><span data-stu-id="14123-114">Note, however, many of the standard image formats do not support these global properties.</span></span> <span data-ttu-id="14123-115">Таким образом, многие реализации собственных кодеков, предоставляемые компонентом WIC, не поддерживают большинство этих глобальных свойств.</span><span class="sxs-lookup"><span data-stu-id="14123-115">As such, many of the native codec implementations provided by WIC do not support the majority of these global properties.</span></span> <span data-ttu-id="14123-116">Сведения о поддержке глобальных свойств см. в таблице в разделе декодеры машинного кода в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="14123-116">See the table in the Native Bitmap Decoders section of this topic for information about global property support.</span></span>

<span data-ttu-id="14123-117">В WIC декодеры битовой карты представлены интерфейсом [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) и предоставляют доступ к этим глобальным свойствам точечного рисунка и, что более важно, к кадрам, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="14123-117">In WIC, bitmap decoders are represented by the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface and provides access to these global properties of the bitmap and, more importantly, the frames it contains.</span></span> <span data-ttu-id="14123-118">Интерфейс [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) представляет отдельный кадр точечного рисунка, который подробно обсуждается в разделе [Общие сведения об источниках битовой карты](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="14123-118">The [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface represents an individual bitmap frame and is discussed in detail in the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="native-bitmap-decoders"></a><span data-ttu-id="14123-119">Встроенные декодеры битовой карты</span><span class="sxs-lookup"><span data-stu-id="14123-119">Native Bitmap Decoders</span></span>

<span data-ttu-id="14123-120">WIC предоставляет несколько собственных реализаций интерфейса [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) для стандартных форматов веб-изображений и высокоскоростного формата Фото HD.</span><span class="sxs-lookup"><span data-stu-id="14123-120">WIC provides several native implementations of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface for the standard web image formats and the high dynamic range HD Photo format.</span></span> <span data-ttu-id="14123-121">В следующей таблице перечислены доступные встроенные декодеры, имя идентификатора класса и поддержка глобальных свойств.</span><span class="sxs-lookup"><span data-stu-id="14123-121">The following table lists the available native decoders, class identifier name, and support for global properties.</span></span> <span data-ttu-id="14123-122">Хотя функция может не поддерживать такие свойства, как эскизы на глобальном уровне, формат изображения может поддерживать такие свойства на уровне отдельных кадров.</span><span class="sxs-lookup"><span data-stu-id="14123-122">Though a feature may not support a property such as thumbnails at the global level, the image format may support such properties at the individual frame level.</span></span>



| <span data-ttu-id="14123-123">Формат образа</span><span class="sxs-lookup"><span data-stu-id="14123-123">Image Format</span></span> | <span data-ttu-id="14123-124">Имя CLSID</span><span class="sxs-lookup"><span data-stu-id="14123-124">CLSID Name</span></span>            | <span data-ttu-id="14123-125">Эскизы</span><span class="sxs-lookup"><span data-stu-id="14123-125">Thumbnails</span></span> | <span data-ttu-id="14123-126">Предварительный просмотр</span><span class="sxs-lookup"><span data-stu-id="14123-126">Previews</span></span> | <span data-ttu-id="14123-127">Контексты цвета</span><span class="sxs-lookup"><span data-stu-id="14123-127">Color Contexts</span></span> | <span data-ttu-id="14123-128">Метаданные</span><span class="sxs-lookup"><span data-stu-id="14123-128">Metadata</span></span> |
|--------------|-----------------------|------------|----------|----------------|----------|
| <span data-ttu-id="14123-129">BMP</span><span class="sxs-lookup"><span data-stu-id="14123-129">BMP</span></span>          | <span data-ttu-id="14123-130">\_ВИКБМПДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="14123-130">CLSID\_WICBmpDecoder</span></span>  | <span data-ttu-id="14123-131">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-131">No</span></span>         | <span data-ttu-id="14123-132">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-132">No</span></span>       | <span data-ttu-id="14123-133">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-133">No</span></span>             | <span data-ttu-id="14123-134">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-134">No</span></span>       |
| <span data-ttu-id="14123-135">GIF</span><span class="sxs-lookup"><span data-stu-id="14123-135">GIF</span></span>          | <span data-ttu-id="14123-136">\_ВИКГИФДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="14123-136">CLSID\_WICGifDecoder</span></span>  | <span data-ttu-id="14123-137">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-137">No</span></span>         | <span data-ttu-id="14123-138">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-138">No</span></span>       | <span data-ttu-id="14123-139">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-139">No</span></span>             | <span data-ttu-id="14123-140">Да</span><span class="sxs-lookup"><span data-stu-id="14123-140">Yes</span></span>      |
| <span data-ttu-id="14123-141">ICO</span><span class="sxs-lookup"><span data-stu-id="14123-141">ICO</span></span>          | <span data-ttu-id="14123-142">\_ВИЦИКОДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="14123-142">CLSID\_WICIcoDecoder</span></span>  | <span data-ttu-id="14123-143">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-143">No</span></span>         | <span data-ttu-id="14123-144">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-144">No</span></span>       | <span data-ttu-id="14123-145">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-145">No</span></span>             | <span data-ttu-id="14123-146">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-146">No</span></span>       |
| <span data-ttu-id="14123-147">JPEG</span><span class="sxs-lookup"><span data-stu-id="14123-147">JPEG</span></span>         | <span data-ttu-id="14123-148">\_ВИКЖПЕГДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="14123-148">CLSID\_WICJpegDecoder</span></span> | <span data-ttu-id="14123-149">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-149">No</span></span>         | <span data-ttu-id="14123-150">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-150">No</span></span>       | <span data-ttu-id="14123-151">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-151">No</span></span>             | <span data-ttu-id="14123-152">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-152">No</span></span>       |
| <span data-ttu-id="14123-153">PNG</span><span class="sxs-lookup"><span data-stu-id="14123-153">PNG</span></span>          | <span data-ttu-id="14123-154">\_ВИКПНГДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="14123-154">CLSID\_WICPngDecoder</span></span>  | <span data-ttu-id="14123-155">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-155">No</span></span>         | <span data-ttu-id="14123-156">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-156">No</span></span>       | <span data-ttu-id="14123-157">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-157">No</span></span>             | <span data-ttu-id="14123-158">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-158">No</span></span>       |
| <span data-ttu-id="14123-159">TIFF</span><span class="sxs-lookup"><span data-stu-id="14123-159">TIFF</span></span>         | <span data-ttu-id="14123-160">\_ВИКТИФФДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="14123-160">CLSID\_WICTiffDecoder</span></span> | <span data-ttu-id="14123-161">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-161">No</span></span>         | <span data-ttu-id="14123-162">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-162">No</span></span>       | <span data-ttu-id="14123-163">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-163">No</span></span>             | <span data-ttu-id="14123-164">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-164">No</span></span>       |
| <span data-ttu-id="14123-165">Фото HD</span><span class="sxs-lookup"><span data-stu-id="14123-165">HD Photo</span></span>     | <span data-ttu-id="14123-166">\_ВИКВМПДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="14123-166">CLSID\_WICWmpDecoder</span></span>  | <span data-ttu-id="14123-167">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-167">No</span></span>         | <span data-ttu-id="14123-168">Да</span><span class="sxs-lookup"><span data-stu-id="14123-168">Yes</span></span>      | <span data-ttu-id="14123-169">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-169">No</span></span>             | <span data-ttu-id="14123-170">Нет</span><span class="sxs-lookup"><span data-stu-id="14123-170">No</span></span>       |



 

## <a name="creating-a-bitmap-decoder"></a><span data-ttu-id="14123-171">Создание растрового декодера</span><span class="sxs-lookup"><span data-stu-id="14123-171">Creating a Bitmap Decoder</span></span>

<span data-ttu-id="14123-172">Чтобы декодировать изображение с помощью WIC, сначала необходимо создать экземпляр [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) для целевого формата образа.</span><span class="sxs-lookup"><span data-stu-id="14123-172">To decode an image using WIC, you first need to create an instance of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) for the targeted image format.</span></span> <span data-ttu-id="14123-173">Экземпляр декодера позволяет получить доступ к глобальным свойствам и метаданным, если они поддерживаются, а также к кадрам изображений.</span><span class="sxs-lookup"><span data-stu-id="14123-173">The decoder instance enables you to access the global properties and metadata, if supported, as well as the image frames.</span></span> <span data-ttu-id="14123-174">Фабрика обработки изображений WIC, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), предоставляет несколько методов для создания декодеров битовой карты.</span><span class="sxs-lookup"><span data-stu-id="14123-174">The WIC imaging factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), provides several methods for creating bitmap decoders.</span></span> <span data-ttu-id="14123-175">Для создания декодеров точечных рисунков предоставляются следующие заводские методы.</span><span class="sxs-lookup"><span data-stu-id="14123-175">The following factory methods are provided to create bitmap decoders.</span></span>

-   [<span data-ttu-id="14123-176">**креатедекодер**</span><span class="sxs-lookup"><span data-stu-id="14123-176">**CreateDecoder**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [<span data-ttu-id="14123-177">**креатедекодерфромфилехандле**</span><span class="sxs-lookup"><span data-stu-id="14123-177">**CreateDecoderFromFileHandle**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [<span data-ttu-id="14123-178">**креатедекодерфромфиленаме**</span><span class="sxs-lookup"><span data-stu-id="14123-178">**CreateDecoderFromFilename**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [<span data-ttu-id="14123-179">**креатедекодерфромстреам**</span><span class="sxs-lookup"><span data-stu-id="14123-179">**CreateDecoderFromStream**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

<span data-ttu-id="14123-180">В следующем коде показано, как создать растровый декодер с помощью имени файла изображения и получить первый кадр изображения.</span><span class="sxs-lookup"><span data-stu-id="14123-180">The following code demonstrates the how to create a bitmap decoder using an image filename and retrieve the first frame of the image.</span></span>


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a><span data-ttu-id="14123-181">Расширяемость декодера</span><span class="sxs-lookup"><span data-stu-id="14123-181">Decoder Extensibility</span></span>

<span data-ttu-id="14123-182">Одной из основных функций WIC является инфраструктура расширяемости, которая позволяет разработчикам кодеков разрабатывать собственные кодеки изображений и получать ту же поддержку платформ, что и собственные реализации кодеков изображений.</span><span class="sxs-lookup"><span data-stu-id="14123-182">One of the core features of WIC is an extensibility framework that enables codec developers to develop their own image codecs and get the same platform support as the native implementations of image codecs.</span></span> <span data-ttu-id="14123-183">Один последовательный набор интерфейсов используется для обработки изображений независимо от формата изображения.</span><span class="sxs-lookup"><span data-stu-id="14123-183">A single, consistent set of interfaces is used for all image processing, regardless of image format.</span></span> <span data-ttu-id="14123-184">Любое приложение, использующее WIC, получает автоматическую поддержку новых форматов изображений сразу после установки кодека.</span><span class="sxs-lookup"><span data-stu-id="14123-184">Any application using WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="14123-185">Дополнительные сведения о разработке кодеков см. в разделах, посвященных [разработке компонентов](-wic-component-development.md).</span><span class="sxs-lookup"><span data-stu-id="14123-185">For more information on codec development, see the topics in [Component Development](-wic-component-development.md).</span></span> <span data-ttu-id="14123-186">Дополнительные сведения о разработке декодеров см. в разделе [Реализация декодера WIC-Enabled](-wic-implementingwicdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="14123-186">For more information on decoder development, see [Implementing a WIC-Enabled Decoder](-wic-implementingwicdecoder.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14123-187">См. также</span><span class="sxs-lookup"><span data-stu-id="14123-187">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="14123-188">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="14123-188">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="14123-189">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="14123-189">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="14123-190">Общие сведения о кодировке</span><span class="sxs-lookup"><span data-stu-id="14123-190">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> <dt>

[<span data-ttu-id="14123-191">Разработка компонентов</span><span class="sxs-lookup"><span data-stu-id="14123-191">Component Development</span></span>](-wic-component-development.md)
</dt> </dl>

 

 



