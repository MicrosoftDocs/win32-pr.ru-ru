---
title: Отправленный файл
description: Отправленный файл
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Обложки Windows Media Player для мобильных устройств, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложек, отправленных файлов
- Обложки Windows Media Player для мобильных устройств, отправленные файлы
- обложки, отправленные файлы
- Отправленные файлы в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411033"
---
# <a name="pushed-file"></a><span data-ttu-id="beccd-110">Отправленный файл</span><span class="sxs-lookup"><span data-stu-id="beccd-110">Pushed File</span></span>

<span data-ttu-id="beccd-111">Помещенный файл содержит изображения, которые будут отображаться при нажатии пользователем кнопки.</span><span class="sxs-lookup"><span data-stu-id="beccd-111">The Pushed file contains the images that will be displayed when the user taps on a button.</span></span> <span data-ttu-id="beccd-112">Можно также включить обычные и помещенные изображения для состояния паузы кнопки Плайпаусе.</span><span class="sxs-lookup"><span data-stu-id="beccd-112">You can also include the normal and pushed images for the pause state of the PlayPause button.</span></span>

<span data-ttu-id="beccd-113">На следующем рисунке изображен типичный переданный файл.</span><span class="sxs-lookup"><span data-stu-id="beccd-113">The following image is a typical Pushed file.</span></span>

![Отправленный файл](images/cesdkpus.png)

<span data-ttu-id="beccd-115">Здесь хранятся изображения, которые будут отображаться при нажатии кнопок с типом попадания.</span><span class="sxs-lookup"><span data-stu-id="beccd-115">This stores the images that will be displayed when the hit-type buttons are tapped.</span></span> <span data-ttu-id="beccd-116">Кроме того, в этом файле хранятся обычные и помещенные изображения для приостановленного образа кнопки Плайпаусе.</span><span class="sxs-lookup"><span data-stu-id="beccd-116">Also stored in this file are the normal and pushed images for the paused image of the PlayPause button.</span></span> <span data-ttu-id="beccd-117">За исключением дополнительных изображений Плайпаусе справа, другие изображения кнопки выстроятся на фоне фонового изображения с использованием смещения, определенного в разделе точечные рисунки файла определения обложки.</span><span class="sxs-lookup"><span data-stu-id="beccd-117">Except for the PlayPause secondary images on the right, the other button images line up with the Background image, using the offset defined in the Bitmaps section of the skin definition file.</span></span>

<span data-ttu-id="beccd-118">Обратите внимание, что фон изображения кнопки точно соответствует соответствующей области в фоновом файле.</span><span class="sxs-lookup"><span data-stu-id="beccd-118">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="beccd-119">Это важно, поскольку когда пользователь нажмет кнопку типа "попадание", весь прямоугольник, определенный для отправленного изображения, заменит соответствующую область в фоновом файле.</span><span class="sxs-lookup"><span data-stu-id="beccd-119">This is important, because when the user taps a hit-type button, the entire rectangle defined for the pushed image will replace the matching area in the Background file.</span></span> <span data-ttu-id="beccd-120">Убедитесь, что рисунок соответствует фоновому изображению, чтобы гарантировать, что только те части кнопки, которые должны быть разными, изменятся.</span><span class="sxs-lookup"><span data-stu-id="beccd-120">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="beccd-121">См. также</span><span class="sxs-lookup"><span data-stu-id="beccd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beccd-122">**Файлы изображений**</span><span class="sxs-lookup"><span data-stu-id="beccd-122">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




