---
title: Файл Сиксумб
description: Файл Сиксумб
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Обложки Windows Media Player для мобильных устройств, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложек, файлы Сиксумбд
- Обложки мобильных приложений проигрывателя Windows Media, файлы Сиксумб
- обложки, файлы Сиксумб
- Сиксумб файлы в обложках
- Thumb, Сиксумб Files
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986610"
---
# <a name="seekthumb-file"></a><span data-ttu-id="75f9a-111">Файл Сиксумб</span><span class="sxs-lookup"><span data-stu-id="75f9a-111">SeekThumb File</span></span>

<span data-ttu-id="75f9a-112">Файл Сиксумб определяет изображение, которое указывает место воспроизведения в элементе мультимедиа для позиции линейки поиска.</span><span class="sxs-lookup"><span data-stu-id="75f9a-112">The SeekThumb file defines the image that indicates the playback location within the media item for a Seek trackbar.</span></span> <span data-ttu-id="75f9a-113">Можно использовать один файл и определить его для использования в Сиксумб и Волумесумб.</span><span class="sxs-lookup"><span data-stu-id="75f9a-113">You can use one file and define it for use by both SeekThumb and VolumeThumb.</span></span> <span data-ttu-id="75f9a-114">В отличие от других графических файлов, файлы Thumb определяются в разделе TrackBar файла определения обложки.</span><span class="sxs-lookup"><span data-stu-id="75f9a-114">Unlike the other art files, the thumb files are defined in the Trackbars section of the skin definition file.</span></span>

<span data-ttu-id="75f9a-115">На следующем рисунке приведен типичный файл Сиксумб.</span><span class="sxs-lookup"><span data-stu-id="75f9a-115">The following image is a typical SeekThumb file.</span></span>

![файл сиксумб](images/cesdksee.gif)

<span data-ttu-id="75f9a-117">Эти два файла кнопок выглядят одинаково, но имеют немного разные размеры.</span><span class="sxs-lookup"><span data-stu-id="75f9a-117">These two button files look the same but are slightly different sizes.</span></span> <span data-ttu-id="75f9a-118">Левое изображение — это нормальное представление, которое видит пользователь, а справа — изображение, которое видит пользователь при касании кнопки.</span><span class="sxs-lookup"><span data-stu-id="75f9a-118">The left image is the normal view that the user sees, and the right image is the Pushed image the user sees when they tap on the button.</span></span>

> [!Note]  
> <span data-ttu-id="75f9a-119">Файлы Сиксумб Art, созданные для обложек, используемых в проигрывателе Windows Media 10 Mobile или более поздней версии, должны иметь следующие три изображения (слева направо): обычные, отправленные и отключенные.</span><span class="sxs-lookup"><span data-stu-id="75f9a-119">SeekThumb art files created for skins used in Windows Media Player 10 Mobile or later must have the following three images (from left to right): normal, pushed, and disabled.</span></span>

 

<span data-ttu-id="75f9a-120">Может потребоваться сделать определенные области изображения Thumb прозрачными.</span><span class="sxs-lookup"><span data-stu-id="75f9a-120">You may want to make certain areas of the thumb images transparent.</span></span> <span data-ttu-id="75f9a-121">Это позволит создавать изображения Thumb в фигурах, отличных от прямоугольных.</span><span class="sxs-lookup"><span data-stu-id="75f9a-121">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="75f9a-122">Любая область изображения Thumb, заполняемая цветом, заданным значением RGB 255, 0, 255, будет отображаться в обложке как прозрачная.</span><span class="sxs-lookup"><span data-stu-id="75f9a-122">Any region of a thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75f9a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="75f9a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75f9a-124">**Файлы изображений**</span><span class="sxs-lookup"><span data-stu-id="75f9a-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




