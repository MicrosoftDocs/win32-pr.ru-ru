---
title: Расширения файлов
description: Расширения файлов
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Метафайлы Windows Media, расширения
- Метафайлы Windows Media, расширения имен файлов
- Метафайлы, расширения
- Метафайлы, расширения имен файлов
- Windows Media, метафайлы
- расширения имен файлов для метафайлов Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691346"
---
# <a name="file-name-extensions"></a><span data-ttu-id="c84ec-109">Расширения файлов</span><span class="sxs-lookup"><span data-stu-id="c84ec-109">File Name Extensions</span></span>

<span data-ttu-id="c84ec-110">Существуют определенные рекомендации по использованию расширений имен файлов для метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c84ec-110">There are specific guidelines for the use of file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="c84ec-111">Расширения Windows Media Metafile Names используются для поиска различных типов файлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c84ec-111">Windows Media metafile name extensions are used to identify the different types of Windows Media files.</span></span> <span data-ttu-id="c84ec-112">Расширение имени файла предоставляет независимому поставщику программного обеспечения (ISV) сведения о требованиях к отрисовке приложения, использующего определенное расширение, и позволяет авторам содержимого ориентироваться на общие типы проигрывателей мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c84ec-112">A file name extension provides an Independent Software Vendor (ISV) with information about the rendering requirements of an application that uses a particular extension, and enables content authors to target general types of media players.</span></span>

<span data-ttu-id="c84ec-113">Рекомендации по расширению имени файла перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c84ec-113">The file name extension guidelines are listed in the following table.</span></span> <span data-ttu-id="c84ec-114">Рекомендуется использовать тип MIME файла, расположенный в заголовке файла, для идентификации типа файлов.</span><span class="sxs-lookup"><span data-stu-id="c84ec-114">It is recommended that a file's MIME type, located in the file header, be used for file-type identification.</span></span>



| <span data-ttu-id="c84ec-115">Расширение имени файла</span><span class="sxs-lookup"><span data-stu-id="c84ec-115">File name extension</span></span> | <span data-ttu-id="c84ec-116">тип MIME</span><span class="sxs-lookup"><span data-stu-id="c84ec-116">MIME type</span></span>      | <span data-ttu-id="c84ec-117">содержимое файла;</span><span class="sxs-lookup"><span data-stu-id="c84ec-117">File content</span></span>                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84ec-118">.wma</span><span class="sxs-lookup"><span data-stu-id="c84ec-118">.wma</span></span>                | <span data-ttu-id="c84ec-119">аудио/x-MS-WMA</span><span class="sxs-lookup"><span data-stu-id="c84ec-119">audio/x-ms-wma</span></span> | <span data-ttu-id="c84ec-120">Файл Windows Media с только звуковым содержимым.</span><span class="sxs-lookup"><span data-stu-id="c84ec-120">Windows Media file with audio content only.</span></span> <span data-ttu-id="c84ec-121">Обычно используется для загрузки и воспроизведения файлов или потокового содержимого.</span><span class="sxs-lookup"><span data-stu-id="c84ec-121">Typically used to download and play files or to stream content.</span></span>                                                                             |
| <span data-ttu-id="c84ec-122">.wmv</span><span class="sxs-lookup"><span data-stu-id="c84ec-122">.wmv</span></span>                | <span data-ttu-id="c84ec-123">видео/x — MS-WMV</span><span class="sxs-lookup"><span data-stu-id="c84ec-123">video/x-ms-wmv</span></span> | <span data-ttu-id="c84ec-124">Файл Windows Media с аудио-или видеосодержимым.</span><span class="sxs-lookup"><span data-stu-id="c84ec-124">Windows Media file with audio and/or video content.</span></span> <span data-ttu-id="c84ec-125">Обычно используется для загрузки и воспроизведения файлов или потокового содержимого.</span><span class="sxs-lookup"><span data-stu-id="c84ec-125">Typically used to download and play files or to stream content.</span></span>                                                                     |
| <span data-ttu-id="c84ec-126">.asf</span><span class="sxs-lookup"><span data-stu-id="c84ec-126">.asf</span></span>                | <span data-ttu-id="c84ec-127">видео/x — MS-ASF</span><span class="sxs-lookup"><span data-stu-id="c84ec-127">video/x-ms-asf</span></span> | <span data-ttu-id="c84ec-128">Устаревшее содержимое.</span><span class="sxs-lookup"><span data-stu-id="c84ec-128">Legacy content.</span></span> <span data-ttu-id="c84ec-129">Обычно используется для загрузки и воспроизведения файлов или потокового содержимого.</span><span class="sxs-lookup"><span data-stu-id="c84ec-129">Typically used to download and play files or to stream content.</span></span> <span data-ttu-id="c84ec-130">Может содержать аудио-и видеоматериалы.</span><span class="sxs-lookup"><span data-stu-id="c84ec-130">May contain audio and/or video content.</span></span> <span data-ttu-id="c84ec-131">Обычно используется для загрузки и воспроизведения файлов или потокового содержимого.</span><span class="sxs-lookup"><span data-stu-id="c84ec-131">Typically used to download and play files or to stream content.</span></span> |
| <span data-ttu-id="c84ec-132">.wm</span><span class="sxs-lookup"><span data-stu-id="c84ec-132">.wm</span></span>                 | <span data-ttu-id="c84ec-133">видео/x — MS-WM</span><span class="sxs-lookup"><span data-stu-id="c84ec-133">video/x-ms-wm</span></span>  | <span data-ttu-id="c84ec-134">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="c84ec-134">Reserved</span></span>                                                                                                                                                                                |
| <span data-ttu-id="c84ec-135">. мастика</span><span class="sxs-lookup"><span data-stu-id="c84ec-135">.wax</span></span>                | <span data-ttu-id="c84ec-136">Audio/x — MS-мастика</span><span class="sxs-lookup"><span data-stu-id="c84ec-136">audio/x-ms-wax</span></span> | <span data-ttu-id="c84ec-137">Метафайлы, которые ссылаются на файлы Windows Media с расширением ASF, WMA или мастика.</span><span class="sxs-lookup"><span data-stu-id="c84ec-137">Metafiles that reference Windows Media files with .asf, .wma, or .wax file name extensions.</span></span>                                                                                             |
| <span data-ttu-id="c84ec-138">. ввкс</span><span class="sxs-lookup"><span data-stu-id="c84ec-138">.wvx</span></span>                | <span data-ttu-id="c84ec-139">видео/x — MS-ввкс</span><span class="sxs-lookup"><span data-stu-id="c84ec-139">video/x-ms-wvx</span></span> | <span data-ttu-id="c84ec-140">Метафайлы, которые ссылаются на файлы Windows Media с расширением. WMA,. WMV,. ввкс или. мастика.</span><span class="sxs-lookup"><span data-stu-id="c84ec-140">Metafiles that reference Windows Media files with .wma, .wmv, .wvx, or .wax file name extensions.</span></span>                                                                                       |
| <span data-ttu-id="c84ec-141">.asx</span><span class="sxs-lookup"><span data-stu-id="c84ec-141">.asx</span></span>                | <span data-ttu-id="c84ec-142">видео/x — MS-ASF</span><span class="sxs-lookup"><span data-stu-id="c84ec-142">video/x-ms-asf</span></span> | <span data-ttu-id="c84ec-143">Метафайлы, которые ссылаются на файлы Windows Media с расширением. WMA,. мастика,. WMV,. ввкс,. ASF или. ASX.</span><span class="sxs-lookup"><span data-stu-id="c84ec-143">Metafiles that reference Windows Media files with .wma, .wax, .wmv, .wvx, .asf, or .asx file name extensions.</span></span>                                                                           |
| <span data-ttu-id="c84ec-144">. ВМКС</span><span class="sxs-lookup"><span data-stu-id="c84ec-144">.wmx</span></span>                | <span data-ttu-id="c84ec-145">видео/x — MS-ввкс</span><span class="sxs-lookup"><span data-stu-id="c84ec-145">video/x-ms-wvx</span></span> | <span data-ttu-id="c84ec-146">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c84ec-146">Reserved.</span></span>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="c84ec-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c84ec-147">Remarks</span></span>

<span data-ttu-id="c84ec-148">Поддержка сценариев и управления цифровыми правами (DRM) должна поддерживаться любым приложением, которое отображает файлы Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c84ec-148">Scripting and digital rights management (DRM) must be supported by any application that renders Windows Media files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c84ec-149">См. также</span><span class="sxs-lookup"><span data-stu-id="c84ec-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c84ec-150">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c84ec-150">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="c84ec-151">**Путеводитель по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c84ec-151">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="c84ec-152">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c84ec-152">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 




