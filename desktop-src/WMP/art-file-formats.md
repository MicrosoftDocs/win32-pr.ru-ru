---
title: Форматы файлов изображений
description: Форматы файлов изображений
ms.assetid: 803479e8-0e00-4724-80b7-9d86709c43db
keywords:
- Обложки проигрывателя Windows Media, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложек, форматы файлов
- Обложки проигрывателя Windows Media, форматы файлов для иллюстрации
- обложки, форматы файлов для иллюстрации
- форматы файлов для обложки Art
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35af72fd502cb23e81063fe9513b4a9311f9557
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332435"
---
# <a name="art-file-formats"></a><span data-ttu-id="3efa8-110">Форматы файлов изображений</span><span class="sxs-lookup"><span data-stu-id="3efa8-110">Art File Formats</span></span>

<span data-ttu-id="3efa8-111">Проигрыватель Windows Media распознает следующие форматы графических файлов для обложек:</span><span class="sxs-lookup"><span data-stu-id="3efa8-111">The following art file formats are recognized by Windows Media Player for skins:</span></span>



| <span data-ttu-id="3efa8-112">Формат</span><span class="sxs-lookup"><span data-stu-id="3efa8-112">Format</span></span>                                  | <span data-ttu-id="3efa8-113">Расширение</span><span class="sxs-lookup"><span data-stu-id="3efa8-113">Extension</span></span>   | <span data-ttu-id="3efa8-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3efa8-114">Description</span></span>                                                                                        |
|-----------------------------------------|-------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3efa8-115">Bitmap</span><span class="sxs-lookup"><span data-stu-id="3efa8-115">Bitmap</span></span>                                  | <span data-ttu-id="3efa8-116">BMP</span><span class="sxs-lookup"><span data-stu-id="3efa8-116">.bmp</span></span>        | <span data-ttu-id="3efa8-117">Рекомендуется использовать битовые изображения, так как они обеспечивают наибольшее Управление точным изображением и цветами.</span><span class="sxs-lookup"><span data-stu-id="3efa8-117">Bitmap images are recommended because they offer the most control over the exact image and colors.</span></span> |
| <span data-ttu-id="3efa8-118">GIF</span><span class="sxs-lookup"><span data-stu-id="3efa8-118">Graphics Interchange Format (GIF)</span></span>       | <span data-ttu-id="3efa8-119">.gif</span><span class="sxs-lookup"><span data-stu-id="3efa8-119">.gif</span></span>        | <span data-ttu-id="3efa8-120">Формат сжатого изображения, используемый для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="3efa8-120">Compressed image format used for webpages.</span></span> <span data-ttu-id="3efa8-121">Поддерживаются анимированные GIF.</span><span class="sxs-lookup"><span data-stu-id="3efa8-121">Animated GIFs are supported.</span></span>                            |
| <span data-ttu-id="3efa8-122">JPEG</span><span class="sxs-lookup"><span data-stu-id="3efa8-122">Joint Photographic Experts Group (JPEG)</span></span> | <span data-ttu-id="3efa8-123">.jpeg, .jpg</span><span class="sxs-lookup"><span data-stu-id="3efa8-123">.jpeg, .jpg</span></span> | <span data-ttu-id="3efa8-124">Формат сжатого изображения, используемый для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="3efa8-124">Compressed image format used for webpages.</span></span>                                                         |
| <span data-ttu-id="3efa8-125">PNG</span><span class="sxs-lookup"><span data-stu-id="3efa8-125">Portable Network Graphics (PNG)</span></span>         | <span data-ttu-id="3efa8-126">.png</span><span class="sxs-lookup"><span data-stu-id="3efa8-126">.png</span></span>        | <span data-ttu-id="3efa8-127">Формат сжатого изображения, используемый для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="3efa8-127">Compressed image format used for webpages.</span></span>                                                         |



 

<span data-ttu-id="3efa8-128">При использовании одного из сжатых форматов файлов, определяющих цвет как прозрачный для веб-браузера, не определяйте цвет как прозрачный в файле изображения.</span><span class="sxs-lookup"><span data-stu-id="3efa8-128">If you use one of the compressed file formats that defines a color as transparent to a Web browser, do not define a color as transparent in the image file.</span></span> <span data-ttu-id="3efa8-129">Используйте видимый цвет для представления прозрачных областей изображения, а затем определите этот цвет как прозрачный в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="3efa8-129">Use a visible color to represent transparent areas in your image, and then define that color as transparent in the skin definition file.</span></span> <span data-ttu-id="3efa8-130">Например, если вы создаете GIF-файл с прозрачными областями, он не будет прозрачным в окончательном образе, и вы не сможете использовать цвет, заданный в качестве прозрачного в файле GIF, для цвета прозрачности в обложке.</span><span class="sxs-lookup"><span data-stu-id="3efa8-130">For example, if you create a GIF file with some areas transparent, they will not be transparent in your final image and you will not be able to use the color you set as transparent in your gif file for the transparency color in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3efa8-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3efa8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3efa8-132">**Файлы изображений**</span><span class="sxs-lookup"><span data-stu-id="3efa8-132">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




