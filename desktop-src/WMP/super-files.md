---
title: Супер файлы
description: Супер файлы
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Обложки Windows Media Player для мобильных устройств, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- файлы изображений для обложек, файлов Super Files
- Обложки мобильных приложений проигрывателя Windows Media, файлы Super Files
- обложки, Суперпользователи
- Надстрочные файлы в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710125"
---
# <a name="super-files"></a><span data-ttu-id="fda3c-110">Супер файлы</span><span class="sxs-lookup"><span data-stu-id="fda3c-110">Super Files</span></span>

<span data-ttu-id="fda3c-111">Суперпользователи используются для хранения отключенных изображений для значений TrackBar.</span><span class="sxs-lookup"><span data-stu-id="fda3c-111">Super files are used to store the Disabled images for trackbars.</span></span> <span data-ttu-id="fda3c-112">Так как основное изображение TrackBar отображается в фоновом файле, и пользователь отключается к изображению Thumb, а не к изображению TrackBar, для значений TrackBar требуется только отключенный образ.</span><span class="sxs-lookup"><span data-stu-id="fda3c-112">Because the main trackbar image is displayed in the Background file, and the user taps on the thumb image, not the trackbar image, only the Disabled image is needed for trackbars.</span></span> <span data-ttu-id="fda3c-113">Он хранится в файле, определенном Super, в разделе точечные рисунки файла определения обложки.</span><span class="sxs-lookup"><span data-stu-id="fda3c-113">It is stored in the file defined by Super in the Bitmaps section of the skin definition file.</span></span> <span data-ttu-id="fda3c-114">Супер-файл также может хранить отправленные и отключенные изображения для других кнопок, таких как «Выкл.», которые не являются обязательными для кнопки типа попадания.</span><span class="sxs-lookup"><span data-stu-id="fda3c-114">A Super file can also store the Pushed and Disabled images for other buttons such as Mute, which is not required to be a hit-type button.</span></span>

> [!Note]  
> <span data-ttu-id="fda3c-115">Файлы Super Art не используются в обложках проигрывателя Windows Media 10 Mobile или более поздней версии, так как отключенные изображения для значений TrackBar для поиска находятся в файле сиксумб.</span><span class="sxs-lookup"><span data-stu-id="fda3c-115">Super art files are not used in skins for Windows Media Player 10 Mobile or later because the disabled images for seek trackbars are located in the seekthumb file.</span></span>

 

<span data-ttu-id="fda3c-116">На следующем рисунке изображен типичный супер-файл.</span><span class="sxs-lookup"><span data-stu-id="fda3c-116">The following image is a typical Super file.</span></span>

![Супер файл](images/cesdksup.png)

<span data-ttu-id="fda3c-118">При этом сохраняются отключенные изображения для значений TrackBar и кнопки Выключить звук.</span><span class="sxs-lookup"><span data-stu-id="fda3c-118">This stores the disabled images for the trackbars and the mute button.</span></span> <span data-ttu-id="fda3c-119">Эти образы являются смещениями, как определено в разделе "битовые карты".</span><span class="sxs-lookup"><span data-stu-id="fda3c-119">These images are offset as defined by the Bitmaps section.</span></span>

<span data-ttu-id="fda3c-120">Область фона отключенного изображения TrackBar точно соответствует соответствующей области в фоновом файле.</span><span class="sxs-lookup"><span data-stu-id="fda3c-120">The background area of the disabled trackbar image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="fda3c-121">Это важно, так как весь прямоугольник, определенный для отключенного изображения TrackBar, заменит соответствующую область в фоновом файле.</span><span class="sxs-lookup"><span data-stu-id="fda3c-121">This is important, because the entire rectangle defined for the disabled trackbar image will replace the matching area in the Background file.</span></span> <span data-ttu-id="fda3c-122">Это гарантирует, что отключенное изображение TrackBar прозрачно смешивается с фоновым изображением.</span><span class="sxs-lookup"><span data-stu-id="fda3c-122">This ensures that the disabled trackbar image blends seamlessly into the background image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fda3c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="fda3c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fda3c-124">**Файлы изображений**</span><span class="sxs-lookup"><span data-stu-id="fda3c-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




