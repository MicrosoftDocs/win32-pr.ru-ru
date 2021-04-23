---
title: Отключенный файл
description: Отключенный файл
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Обложки Windows Media Player для мобильных устройств, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложек, отключенные файлы
- Обложки Windows Media Player для мобильных устройств, отключенные файлы
- обложки, отключенные файлы
- Отключенные файлы в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068224"
---
# <a name="disabled-file"></a><span data-ttu-id="d898f-110">Отключенный файл</span><span class="sxs-lookup"><span data-stu-id="d898f-110">Disabled File</span></span>

<span data-ttu-id="d898f-111">Отключенный файл содержит изображения, которые будут отображаться, если не удается использовать определенную функцию кнопки или состояние кнопки — OFF.</span><span class="sxs-lookup"><span data-stu-id="d898f-111">The Disabled file contains the images that will be displayed when a particular button function cannot be used or a button state is off.</span></span> <span data-ttu-id="d898f-112">Например, если определен пустой список воспроизведения, отображаются кнопки **Далее** и **назад** , которые должны отображаться с помощью отключенного изображения.</span><span class="sxs-lookup"><span data-stu-id="d898f-112">For example, if an empty playlist is defined, the **Next** and **Prev** buttons will be displayed, and they should be displayed using a disabled image.</span></span> <span data-ttu-id="d898f-113">Кроме того, для выключателей используется отключенный образ, указывающий, что состояние — OFF.</span><span class="sxs-lookup"><span data-stu-id="d898f-113">Also, for toggle buttons, the Disabled image is used to indicate that the state is off.</span></span>

<span data-ttu-id="d898f-114">На следующем рисунке изображен типичный отключенный файл.</span><span class="sxs-lookup"><span data-stu-id="d898f-114">The following image is a typical Disabled file.</span></span>

![Отключенный файл](images/cesdkdis.png)

<span data-ttu-id="d898f-116">При этом сохраняются изображения для отключенных кнопок типа "попадание".</span><span class="sxs-lookup"><span data-stu-id="d898f-116">This stores the images for hit-type buttons that are disabled.</span></span> <span data-ttu-id="d898f-117">Изображения похожи на фоновый файл, но цвета более светлы.</span><span class="sxs-lookup"><span data-stu-id="d898f-117">The images are similar to the Background file, but the colors are lighter.</span></span> <span data-ttu-id="d898f-118">С помощью смещения, определенного в разделе точечные рисунки файла определения обложки, изображения кнопки выдаются с фоновым изображением файла.</span><span class="sxs-lookup"><span data-stu-id="d898f-118">Using the offset defined in the Bitmaps section of the skin definition file, the button images line up with the Background file image.</span></span>

<span data-ttu-id="d898f-119">Обратите внимание, что фон изображения кнопки точно соответствует соответствующей области в фоновом файле.</span><span class="sxs-lookup"><span data-stu-id="d898f-119">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="d898f-120">Это важно, так как если кнопка типа попадания недоступна, весь прямоугольник, определенный для отключенного изображения, заменит соответствующую область в фоновом файле.</span><span class="sxs-lookup"><span data-stu-id="d898f-120">This is important, because when a hit-type button is unavailable, the entire rectangle defined for the disabled image will replace the matching area in the Background file.</span></span> <span data-ttu-id="d898f-121">Убедитесь, что рисунок соответствует фоновому изображению, чтобы гарантировать, что только те части кнопки, которые должны быть разными, изменятся.</span><span class="sxs-lookup"><span data-stu-id="d898f-121">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d898f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d898f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d898f-123">**Файлы изображений**</span><span class="sxs-lookup"><span data-stu-id="d898f-123">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




