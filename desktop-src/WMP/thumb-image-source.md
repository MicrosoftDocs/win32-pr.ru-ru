---
title: Источник изображения Thumb
description: Источник изображения Thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, линейки воспроизведения
- обложки, TrackBar
- Справочник по обложек, TrackBar
- линейки воспроизведения в обложках, источник изображения
- линейки воспроизведения в обложках, источник изображения Thumb
- Источник изображения для обложек, TrackBar
- бегунок, источник изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067636"
---
# <a name="thumb-image-source"></a><span data-ttu-id="75ff2-110">Источник изображения Thumb</span><span class="sxs-lookup"><span data-stu-id="75ff2-110">Thumb Image Source</span></span>

<span data-ttu-id="75ff2-111">Необходимо определить имя файла, содержащего изображение Thumb.</span><span class="sxs-lookup"><span data-stu-id="75ff2-111">You must define the name of the file that contains the thumb image.</span></span> <span data-ttu-id="75ff2-112">Это должно быть допустимое имя файла с расширением BMP, GIF, JPG или PNG.</span><span class="sxs-lookup"><span data-stu-id="75ff2-112">This must be a valid file name with the extension .bmp, .gif, .jpg, or .png.</span></span> <span data-ttu-id="75ff2-113">Файл должен содержать три параллельных изображения одинакового размера.</span><span class="sxs-lookup"><span data-stu-id="75ff2-113">The file must contain three side-by-side images of identical size.</span></span> <span data-ttu-id="75ff2-114">Они должны находиться рядом друг с другом без пробела между ними.</span><span class="sxs-lookup"><span data-stu-id="75ff2-114">They must be adjacent to each other with no space between.</span></span> <span data-ttu-id="75ff2-115">Левый верхний угол левого изображения должен находиться в левом верхнем углу файла.</span><span class="sxs-lookup"><span data-stu-id="75ff2-115">The top-left position of the left image must be at the top-left corner of the file.</span></span> <span data-ttu-id="75ff2-116">Изображение слева является обычным изображением для изображения Thumb, а изображение в средней части отображает состояние "Отправлено", а изображение справа отображает отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="75ff2-116">The image on the left side is the normal image for the thumb image, and the image in the middle depicts the pushed state and the image on the right depicts the disabled state.</span></span>


```C++
SeekThumb.bmp

```



<span data-ttu-id="75ff2-117">Может потребоваться сделать определенные области изображения Thumb прозрачными.</span><span class="sxs-lookup"><span data-stu-id="75ff2-117">You may want to make certain areas of the thumb image transparent.</span></span> <span data-ttu-id="75ff2-118">Это позволит создавать изображения Thumb в фигурах, отличных от прямоугольных.</span><span class="sxs-lookup"><span data-stu-id="75ff2-118">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="75ff2-119">Любая область изображения Thumb, заполняемая цветом, заданным значением RGB 255, 0, 255, будет отображаться в обложке как прозрачная.</span><span class="sxs-lookup"><span data-stu-id="75ff2-119">Any region of the thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75ff2-120">См. также</span><span class="sxs-lookup"><span data-stu-id="75ff2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ff2-121">**Линейки воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="75ff2-121">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




