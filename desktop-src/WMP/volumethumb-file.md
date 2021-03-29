---
title: Файл Волумесумб
description: Файл Волумесумб
ms.assetid: de6abfed-a811-44c4-8db2-f3b55ea38756
keywords:
- Обложки Windows Media Player для мобильных устройств, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложек, файлы Волумесумб
- Обложки мобильных приложений проигрывателя Windows Media, файлы Волумесумб
- обложки, файлы Волумесумб
- Волумесумб файлы в обложках
- Thumb, Волумесумб Files
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b7ba87723025c91b3bdfb5af5fd233197dedb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775095"
---
# <a name="volumethumb-file"></a><span data-ttu-id="a2789-111">Файл Волумесумб</span><span class="sxs-lookup"><span data-stu-id="a2789-111">VolumeThumb File</span></span>

<span data-ttu-id="a2789-112">Файл Волумесумб определяет изображение, указывающее уровень громкости воспроизведения для ползунка громкости.</span><span class="sxs-lookup"><span data-stu-id="a2789-112">The VolumeThumb file defines the image that indicates the playback volume level for a Volume trackbar.</span></span> <span data-ttu-id="a2789-113">Можно использовать один файл и определить его для использования в Сиксумб и Волумесумб.</span><span class="sxs-lookup"><span data-stu-id="a2789-113">You can use one file and define it for use by both SeekThumb and VolumeThumb.</span></span> <span data-ttu-id="a2789-114">В отличие от других графических файлов, файлы Thumb определяются в разделе TrackBar файла определения обложки.</span><span class="sxs-lookup"><span data-stu-id="a2789-114">Unlike the other art files, the thumb files are defined in the Trackbars section of the skin definition file.</span></span>

<span data-ttu-id="a2789-115">На следующем рисунке приведен типичный файл Волумесумб.</span><span class="sxs-lookup"><span data-stu-id="a2789-115">The following image is a typical VolumeThumb file.</span></span>

![файл волумесумб](images/cesdkvol.png)

<span data-ttu-id="a2789-117">Эти два файла кнопок выглядят одинаково, но имеют немного разные размеры.</span><span class="sxs-lookup"><span data-stu-id="a2789-117">These two button files look the same but are slightly different sizes.</span></span> <span data-ttu-id="a2789-118">Левое изображение — это нормальное представление, которое видит пользователь, а справа — изображение, которое видит пользователь при касании кнопки.</span><span class="sxs-lookup"><span data-stu-id="a2789-118">The left image is the normal view that the user sees, and the right image is the Pushed image the user sees when they tap on the button.</span></span>

<span data-ttu-id="a2789-119">Может потребоваться сделать определенные области изображения Thumb прозрачными.</span><span class="sxs-lookup"><span data-stu-id="a2789-119">You may want to make certain areas of the thumb images transparent.</span></span> <span data-ttu-id="a2789-120">Это позволит создавать изображения Thumb в фигурах, отличных от прямоугольных.</span><span class="sxs-lookup"><span data-stu-id="a2789-120">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="a2789-121">Любая область изображения Thumb, заполняемая цветом, заданным значением RGB 255, 0, 255, будет отображаться в обложке как прозрачная.</span><span class="sxs-lookup"><span data-stu-id="a2789-121">Any region of a thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2789-122">См. также</span><span class="sxs-lookup"><span data-stu-id="a2789-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2789-123">**Файлы изображений**</span><span class="sxs-lookup"><span data-stu-id="a2789-123">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




