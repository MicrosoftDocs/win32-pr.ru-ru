---
description: Компонент Windows Imaging Component (WIC) предоставляет расширяемую платформу для работы с изображениями и метаданными изображений.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Общие сведения о компоненте создания образов Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264875"
---
# <a name="windows-imaging-component-overview"></a><span data-ttu-id="ff153-103">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="ff153-103">Windows Imaging Component Overview</span></span>

<span data-ttu-id="ff153-104">Компонент Windows Imaging Component (WIC) предоставляет расширяемую платформу для работы с изображениями и метаданными изображений.</span><span class="sxs-lookup"><span data-stu-id="ff153-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="ff153-105">WIC позволяет независимым поставщикам программного обеспечения и независимым поставщикам оборудования (IHV) разрабатывать собственные кодеки изображений и поддерживать ту же самую платформу, что и стандартные форматы изображений (например, TIFF, JPEG, PNG, GIF, BMP и Хдфото).</span><span class="sxs-lookup"><span data-stu-id="ff153-105">WIC makes it possible for independent software vendors (ISVs) and independent hardware vendors (IHVs) to develop their own image codecs and get the same platform support as standard image formats (for example, TIFF, JPEG, PNG, GIF, BMP, and HDPhoto).</span></span> <span data-ttu-id="ff153-106">Один последовательный набор интерфейсов используется для обработки изображений независимо от формата изображения, поэтому любое приложение, использующее WIC, получает автоматическую поддержку новых форматов изображений сразу после установки кодека.</span><span class="sxs-lookup"><span data-stu-id="ff153-106">A single, consistent set of interfaces is used for all image processing, regardless of image format, so any application using the WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="ff153-107">Расширяемая платформа метаданных позволяет приложениям считывать и записывать собственные конфиденциальные метаданные непосредственно в файлы изображений, поэтому метаданные никогда не теряются или не отделяются от изображения.</span><span class="sxs-lookup"><span data-stu-id="ff153-107">The extensible metadata framework makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata never gets lost or separated from the image.</span></span>

<span data-ttu-id="ff153-108">Этот раздел включает следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="ff153-108">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="ff153-109">Компоненты компонента работы с образами Windows</span><span class="sxs-lookup"><span data-stu-id="ff153-109">Windows Imaging Component Features</span></span>](#windows-imaging-component-features)
-   [<span data-ttu-id="ff153-110">Собственные кодеки</span><span class="sxs-lookup"><span data-stu-id="ff153-110">Native Codecs</span></span>](#native-codecs)
-   [<span data-ttu-id="ff153-111">См. также</span><span class="sxs-lookup"><span data-stu-id="ff153-111">Related topics</span></span>](#related-topics)

## <a name="windows-imaging-component-features"></a><span data-ttu-id="ff153-112">Компоненты компонента работы с образами Windows</span><span class="sxs-lookup"><span data-stu-id="ff153-112">Windows Imaging Component Features</span></span>

<span data-ttu-id="ff153-113">Основные возможности WIC:</span><span class="sxs-lookup"><span data-stu-id="ff153-113">The primary features of WIC are:</span></span>

-   <span data-ttu-id="ff153-114">Позволяет разработчикам приложений выполнять операции обработки изображений в любом формате изображения через единый последовательный набор общих интерфейсов, не требуя перед этим знания о конкретных форматах изображений.</span><span class="sxs-lookup"><span data-stu-id="ff153-114">Enables application developers to perform image processing operations on any image format through a single, consistent set of common interfaces, without requiring prior knowledge of specific image formats.</span></span>
-   <span data-ttu-id="ff153-115">Предоставляет расширяемую архитектуру "Plug and Play" для кодеков изображений, форматов пикселей и метаданных с автоматическим обнаружением новых форматов во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="ff153-115">Provides an extensible "plug and play" architecture for image codecs, pixel formats, and metadata, with automatic run-time discovery of new formats.</span></span>
-   <span data-ttu-id="ff153-116">Поддерживает чтение и запись произвольных метаданных в файлах изображений с возможностью сохранять нераспознанные метаданные во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="ff153-116">Supports reading and writing of arbitrary metadata in image files, with the ability to preserve unrecognized metadata during editing.</span></span>
-   <span data-ttu-id="ff153-117">Сохраняет данные изображений с высоким уровнем глубины, до 32 бит на канал в течение всего конвейера обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="ff153-117">Preserves high bit depth image data, up to 32 bits per channel, throughout the image processing pipeline.</span></span>
-   <span data-ttu-id="ff153-118">Предоставляет встроенную поддержку для большинства популярных форматов изображений, форматов пикселей и схем метаданных.</span><span class="sxs-lookup"><span data-stu-id="ff153-118">Provides built-in support for most popular image formats, pixel formats, and metadata schemas.</span></span>

## <a name="native-codecs"></a><span data-ttu-id="ff153-119">Собственные кодеки</span><span class="sxs-lookup"><span data-stu-id="ff153-119">Native Codecs</span></span>

<span data-ttu-id="ff153-120">Компонент WIC включает несколько встроенных кодеков.</span><span class="sxs-lookup"><span data-stu-id="ff153-120">WIC includes several built-in codecs.</span></span> <span data-ttu-id="ff153-121">С платформой поставляются следующие стандартные кодеки.</span><span class="sxs-lookup"><span data-stu-id="ff153-121">The following standard codecs are provided with the platform.</span></span> 

| <span data-ttu-id="ff153-122">Кодек</span><span class="sxs-lookup"><span data-stu-id="ff153-122">Codec</span></span>                                                                                             | <span data-ttu-id="ff153-123">Типы MIME</span><span class="sxs-lookup"><span data-stu-id="ff153-123">Mime Types</span></span>                       | <span data-ttu-id="ff153-124">Декодеров</span><span class="sxs-lookup"><span data-stu-id="ff153-124">Decoders</span></span> | <span data-ttu-id="ff153-125">Кодировщики</span><span class="sxs-lookup"><span data-stu-id="ff153-125">Encoders</span></span> |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| <span data-ttu-id="ff153-126">BMP (формат точечного рисунка Windows), спецификация BMP V5.</span><span class="sxs-lookup"><span data-stu-id="ff153-126">BMP (Windows Bitmap Format), BMP Specification v5.</span></span>                                                | <span data-ttu-id="ff153-127">image/bmp</span><span class="sxs-lookup"><span data-stu-id="ff153-127">image/bmp</span></span>                        | <span data-ttu-id="ff153-128">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-128">Yes</span></span>      | <span data-ttu-id="ff153-129">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-129">Yes</span></span>      |
| <span data-ttu-id="ff153-130">GIF (формат для обмена изображениями 89A), спецификация GIF 89A/89m</span><span class="sxs-lookup"><span data-stu-id="ff153-130">GIF (Graphics Interchange Format 89a), GIF Specification 89a/89m</span></span>                                  | <span data-ttu-id="ff153-131">image/gif</span><span class="sxs-lookup"><span data-stu-id="ff153-131">image/gif</span></span>                        | <span data-ttu-id="ff153-132">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-132">Yes</span></span>      | <span data-ttu-id="ff153-133">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-133">Yes</span></span>      |
| <span data-ttu-id="ff153-134">ICO (формат значка)</span><span class="sxs-lookup"><span data-stu-id="ff153-134">ICO (Icon Format)</span></span>                                                                                 | <span data-ttu-id="ff153-135">изображение или ICO</span><span class="sxs-lookup"><span data-stu-id="ff153-135">image/ico</span></span>                        | <span data-ttu-id="ff153-136">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-136">Yes</span></span>      | <span data-ttu-id="ff153-137">Нет</span><span class="sxs-lookup"><span data-stu-id="ff153-137">No</span></span>       |
| <span data-ttu-id="ff153-138">JPEG (совместная группа экспертов), спецификация JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="ff153-138">JPEG (Joint Photographic Experts Group), JFIF Specification 1.02</span></span>                                  | <span data-ttu-id="ff153-139">Image/JPEG, Image/JPE, Image/JPG</span><span class="sxs-lookup"><span data-stu-id="ff153-139">image/jpeg, image/jpe, image/jpg</span></span> | <span data-ttu-id="ff153-140">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-140">Yes</span></span>      | <span data-ttu-id="ff153-141">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-141">Yes</span></span>      |
| <span data-ttu-id="ff153-142">PNG (переносимая сетевая графика), спецификация PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="ff153-142">PNG (Portable Network Graphics), PNG Specification 1.2</span></span>                                            | <span data-ttu-id="ff153-143">image/png</span><span class="sxs-lookup"><span data-stu-id="ff153-143">image/png</span></span>                        | <span data-ttu-id="ff153-144">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-144">Yes</span></span>      | <span data-ttu-id="ff153-145">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-145">Yes</span></span>      |
| <span data-ttu-id="ff153-146">TIFF (формат файла изображения с тегами), спецификация TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="ff153-146">TIFF (Tagged Image File Format), TIFF Specification 6.0</span></span>                                           | <span data-ttu-id="ff153-147">Image/TIFF, Image/TIF</span><span class="sxs-lookup"><span data-stu-id="ff153-147">image/tiff, image/tif</span></span>            | <span data-ttu-id="ff153-148">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-148">Yes</span></span>      | <span data-ttu-id="ff153-149">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-149">Yes</span></span>      |
| <span data-ttu-id="ff153-150">Фото Windows Media, [Спецификация HD фото 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span><span class="sxs-lookup"><span data-stu-id="ff153-150">Windows Media Photo, [HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span></span> | <span data-ttu-id="ff153-151">Image/vnd. МС-фот</span><span class="sxs-lookup"><span data-stu-id="ff153-151">image/vnd.ms-phot</span></span>                | <span data-ttu-id="ff153-152">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-152">Yes</span></span>      | <span data-ttu-id="ff153-153">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-153">Yes</span></span>      |
| <span data-ttu-id="ff153-154">DDS (поверхность DirectDraw)</span><span class="sxs-lookup"><span data-stu-id="ff153-154">DDS (DirectDraw Surface)</span></span>                                                                          | <span data-ttu-id="ff153-155">Image/vnd. МС-ДДС</span><span class="sxs-lookup"><span data-stu-id="ff153-155">image/vnd.ms-dds</span></span>                 | <span data-ttu-id="ff153-156">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-156">Yes</span></span>      | <span data-ttu-id="ff153-157">Да</span><span class="sxs-lookup"><span data-stu-id="ff153-157">Yes</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="ff153-158">См. также</span><span class="sxs-lookup"><span data-stu-id="ff153-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ff153-159">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ff153-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff153-160">Общие сведения о метаданных компонента WIC</span><span class="sxs-lookup"><span data-stu-id="ff153-160">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

<span data-ttu-id="ff153-161">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="ff153-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ff153-162">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="ff153-162">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

<span data-ttu-id="ff153-163">[Образец КОДЕка Аиткодек](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ff153-163">[AITCodec Sample CODEC](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span></span>
</dt> </dl>

 

 
