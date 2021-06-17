---
title: Форматы файлов изображений
description: Сведения о форматах файлов изображений, распознаваемых проигрывателем Windows Media для обложек. К ним относятся точечные рисунки, GIF, JPEG и PNG.
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
ms.openlocfilehash: 2b525bc316d6a9901e32e51a54b6fb938fa91208
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262216"
---
# <a name="art-file-formats"></a><span data-ttu-id="ea9f8-111">Форматы файлов изображений</span><span class="sxs-lookup"><span data-stu-id="ea9f8-111">Art File Formats</span></span>

<span data-ttu-id="ea9f8-112">Проигрыватель Windows Media распознает следующие форматы графических файлов для обложек:</span><span class="sxs-lookup"><span data-stu-id="ea9f8-112">The following art file formats are recognized by Windows Media Player for skins:</span></span>



| <span data-ttu-id="ea9f8-113">Формат</span><span class="sxs-lookup"><span data-stu-id="ea9f8-113">Format</span></span>                                  | <span data-ttu-id="ea9f8-114">Расширение</span><span class="sxs-lookup"><span data-stu-id="ea9f8-114">Extension</span></span>   | <span data-ttu-id="ea9f8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ea9f8-115">Description</span></span>                                                                                        |
|-----------------------------------------|-------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9f8-116">Bitmap</span><span class="sxs-lookup"><span data-stu-id="ea9f8-116">Bitmap</span></span>                                  | <span data-ttu-id="ea9f8-117">BMP</span><span class="sxs-lookup"><span data-stu-id="ea9f8-117">.bmp</span></span>        | <span data-ttu-id="ea9f8-118">Рекомендуется использовать битовые изображения, так как они обеспечивают наибольшее Управление точным изображением и цветами.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-118">Bitmap images are recommended because they offer the most control over the exact image and colors.</span></span> |
| <span data-ttu-id="ea9f8-119">GIF</span><span class="sxs-lookup"><span data-stu-id="ea9f8-119">Graphics Interchange Format (GIF)</span></span>       | <span data-ttu-id="ea9f8-120">.gif</span><span class="sxs-lookup"><span data-stu-id="ea9f8-120">.gif</span></span>        | <span data-ttu-id="ea9f8-121">Формат сжатого изображения, используемый для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-121">Compressed image format used for webpages.</span></span> <span data-ttu-id="ea9f8-122">Поддерживаются анимированные GIF.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-122">Animated GIFs are supported.</span></span>                            |
| <span data-ttu-id="ea9f8-123">JPEG</span><span class="sxs-lookup"><span data-stu-id="ea9f8-123">Joint Photographic Experts Group (JPEG)</span></span> | <span data-ttu-id="ea9f8-124">.jpeg, .jpg</span><span class="sxs-lookup"><span data-stu-id="ea9f8-124">.jpeg, .jpg</span></span> | <span data-ttu-id="ea9f8-125">Формат сжатого изображения, используемый для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-125">Compressed image format used for webpages.</span></span>                                                         |
| <span data-ttu-id="ea9f8-126">PNG</span><span class="sxs-lookup"><span data-stu-id="ea9f8-126">Portable Network Graphics (PNG)</span></span>         | <span data-ttu-id="ea9f8-127">.png</span><span class="sxs-lookup"><span data-stu-id="ea9f8-127">.png</span></span>        | <span data-ttu-id="ea9f8-128">Формат сжатого изображения, используемый для веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-128">Compressed image format used for webpages.</span></span>                                                         |



 

<span data-ttu-id="ea9f8-129">При использовании одного из сжатых форматов файлов, определяющих цвет как прозрачный для веб-браузера, не определяйте цвет как прозрачный в файле изображения.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-129">If you use one of the compressed file formats that defines a color as transparent to a Web browser, do not define a color as transparent in the image file.</span></span> <span data-ttu-id="ea9f8-130">Используйте видимый цвет для представления прозрачных областей изображения, а затем определите этот цвет как прозрачный в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-130">Use a visible color to represent transparent areas in your image, and then define that color as transparent in the skin definition file.</span></span> <span data-ttu-id="ea9f8-131">Например, если вы создаете GIF-файл с прозрачными областями, он не будет прозрачным в окончательном образе, и вы не сможете использовать цвет, заданный в качестве прозрачного в файле GIF, для цвета прозрачности в обложке.</span><span class="sxs-lookup"><span data-stu-id="ea9f8-131">For example, if you create a GIF file with some areas transparent, they will not be transparent in your final image and you will not be able to use the color you set as transparent in your gif file for the transparency color in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea9f8-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ea9f8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea9f8-133">**Файлы изображений**</span><span class="sxs-lookup"><span data-stu-id="ea9f8-133">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




