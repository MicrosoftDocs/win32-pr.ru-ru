---
description: 'В этом разделе описываются две связанные понятия: пропорции рисунка и пропорции пикселей.'
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Пропорции рисунка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263499"
---
# <a name="picture-aspect-ratio"></a><span data-ttu-id="35166-103">Пропорции рисунка</span><span class="sxs-lookup"><span data-stu-id="35166-103">Picture Aspect Ratio</span></span>

<span data-ttu-id="35166-104">В этом разделе описываются две связанные понятия: пропорции рисунка и пропорции пикселей.</span><span class="sxs-lookup"><span data-stu-id="35166-104">This topic describes two related concepts, picture aspect ratio and pixel aspect ratio.</span></span> <span data-ttu-id="35166-105">Затем он описывает, как эти понятия выражаются в Microsoft Media Foundation с помощью типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="35166-105">It then describes how these concepts are expressed in Microsoft Media Foundation using media types.</span></span>

-   [<span data-ttu-id="35166-106">Пропорции рисунка</span><span class="sxs-lookup"><span data-stu-id="35166-106">Picture Aspect Ratio</span></span>](#picture-aspect-ratio)
    -   [<span data-ttu-id="35166-107">Пустых</span><span class="sxs-lookup"><span data-stu-id="35166-107">Letterboxing</span></span>](#letterboxing)
    -   [<span data-ttu-id="35166-108">Панорамирование и сканирование</span><span class="sxs-lookup"><span data-stu-id="35166-108">Pan-and-Scan</span></span>](#pan-and-scan)
-   [<span data-ttu-id="35166-109">Пропорция в пикселях</span><span class="sxs-lookup"><span data-stu-id="35166-109">Pixel Aspect Ratio</span></span>](#pixel-aspect-ratio)
-   [<span data-ttu-id="35166-110">Работа с пропорциями</span><span class="sxs-lookup"><span data-stu-id="35166-110">Working with Aspect Ratios</span></span>](#working-with-aspect-ratios)
-   [<span data-ttu-id="35166-111">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="35166-111">Code Examples</span></span>](#code-examples)
    -   [<span data-ttu-id="35166-112">Поиск отображаемой области</span><span class="sxs-lookup"><span data-stu-id="35166-112">Finding the Display Area</span></span>](#finding-the-display-area)
    -   [<span data-ttu-id="35166-113">Преобразование между пропорциями в пикселях</span><span class="sxs-lookup"><span data-stu-id="35166-113">Converting Between Pixel Aspect Ratios</span></span>](#converting-between-pixel-aspect-ratios)
    -   [<span data-ttu-id="35166-114">Вычисление области Леттербокс</span><span class="sxs-lookup"><span data-stu-id="35166-114">Calculating the Letterbox Area</span></span>](#calculating-the-letterbox-area)
-   [<span data-ttu-id="35166-115">См. также</span><span class="sxs-lookup"><span data-stu-id="35166-115">Related topics</span></span>](#related-topics)

## <a name="picture-aspect-ratio"></a><span data-ttu-id="35166-116">Пропорции рисунка</span><span class="sxs-lookup"><span data-stu-id="35166-116">Picture Aspect Ratio</span></span>

<span data-ttu-id="35166-117">Пропорции *рисунка* определяет форму отображаемого видеоизображения.</span><span class="sxs-lookup"><span data-stu-id="35166-117">*Picture aspect ratio* defines the shape of the displayed video image.</span></span> <span data-ttu-id="35166-118">Пропорции рисунка — это КС:И, где КС:И — отношение ширины изображения к высоте изображения.</span><span class="sxs-lookup"><span data-stu-id="35166-118">Picture aspect ratio is notated X:Y, where X:Y is the ratio of picture width to picture height.</span></span> <span data-ttu-id="35166-119">Большинство стандартов видео используют пропорции изображения 4:3 или 16:9.</span><span class="sxs-lookup"><span data-stu-id="35166-119">Most video standards use either 4:3 or 16:9 picture aspect ratio.</span></span> <span data-ttu-id="35166-120">Пропорции 16:9 обычно называются *широкоформатными*.</span><span class="sxs-lookup"><span data-stu-id="35166-120">The 16:9 aspect ratio is commonly called *widescreen*.</span></span> <span data-ttu-id="35166-121">На пленке в кинотеатрах часто используется пропорции 1:85:1 или 1:66:1.</span><span class="sxs-lookup"><span data-stu-id="35166-121">Cinema film often uses a 1:85:1 or 1:66:1 aspect ratio.</span></span> <span data-ttu-id="35166-122">Пропорции изображения также называются *отображаемыми* пропорциями (Dar).</span><span class="sxs-lookup"><span data-stu-id="35166-122">Picture aspect ratio is also called *display aspect ratio* (DAR).</span></span>

![Схема, показывающая пропорции 4:3 и 16:9](images/aspect-ratio01.png)

<span data-ttu-id="35166-124">Иногда видеоизображение не имеет такой же формы, как и отображаемая область.</span><span class="sxs-lookup"><span data-stu-id="35166-124">Sometimes the video image does not have the same shape as the display area.</span></span> <span data-ttu-id="35166-125">Например, видео 4:3 может отображаться на широкоформатном телевизоре (16 × 9).</span><span class="sxs-lookup"><span data-stu-id="35166-125">For example, a 4:3 video might be shown on a widescreen (16×9) television.</span></span> <span data-ttu-id="35166-126">Видео на компьютере может отображаться в окне с произвольным размером.</span><span class="sxs-lookup"><span data-stu-id="35166-126">In computer video, the video might be shown inside a window that has an arbitrary size.</span></span> <span data-ttu-id="35166-127">В этом случае можно создать три способа размещения изображения в области экрана:</span><span class="sxs-lookup"><span data-stu-id="35166-127">In that case, there are three ways the image can be made to fit within the display area:</span></span>

-   <span data-ttu-id="35166-128">Растяните изображение вдоль одной оси в соответствии с отображаемой областью.</span><span class="sxs-lookup"><span data-stu-id="35166-128">Stretch the image along one axis to fit the display area.</span></span>
-   <span data-ttu-id="35166-129">Масштабирование изображения в соответствии с областью экрана с сохранением пропорций исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="35166-129">Scale the image to fit the display area, while maintaining the original picture aspect ratio.</span></span>
-   <span data-ttu-id="35166-130">Обрезка изображения.</span><span class="sxs-lookup"><span data-stu-id="35166-130">Crop the image.</span></span>

<span data-ttu-id="35166-131">Растяжение изображения по размеру отображаемой области почти всегда неверно, поскольку не сохраняет правильные пропорции изображения.</span><span class="sxs-lookup"><span data-stu-id="35166-131">Stretching the image to fit the display area is almost always wrong, because it does not preserve the correct picture aspect ratio.</span></span>

### <a name="letterboxing"></a><span data-ttu-id="35166-132">Пустых</span><span class="sxs-lookup"><span data-stu-id="35166-132">Letterboxing</span></span>

<span data-ttu-id="35166-133">Процесс масштабирования широкоэкранных изображений в соответствии с отображаемым 4:3 называется *пустых*, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="35166-133">The process of scaling a widescreen image to fit a 4:3 display is called *letterboxing*, shown in the next diagram.</span></span> <span data-ttu-id="35166-134">Итоговые ректанглулар области в верхней и нижней части изображения обычно заполняются черным цветом, хотя можно использовать и другие цвета.</span><span class="sxs-lookup"><span data-stu-id="35166-134">The resulting rectanglular areas at the top and bottom of the image are typically filled with black, although other colors can be used.</span></span>

![Схема, показывающая правильный способ леттербокс](images/aspect-ratio02.png)

<span data-ttu-id="35166-136">Обратная ситуация, масштабирование изображения 4:3 в соответствии с широкоэкранным дисплеем, иногда называется *пилларбоксинг*.</span><span class="sxs-lookup"><span data-stu-id="35166-136">The reverse case, scaling a 4:3 image to fit a widescreen display, is sometimes called *pillarboxing*.</span></span> <span data-ttu-id="35166-137">Однако термин *леттербокс* также используется в общем смысле, что означает Масштабирование видеоизображения в соответствии с заданной областью экрана.</span><span class="sxs-lookup"><span data-stu-id="35166-137">However, the term *letterbox* is also used in a general sense, to mean scaling a video image to fit any given display area.</span></span>

![Диаграмма, показывающая пилларбоксинг](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a><span data-ttu-id="35166-139">Панорамирование и сканирование</span><span class="sxs-lookup"><span data-stu-id="35166-139">Pan-and-Scan</span></span>

<span data-ttu-id="35166-140">Сдвиг и сканирование — это способ, с помощью которого изображение с широкоэкранным экраном обрезается до 4 × 3 прямоугольной области, отображаемой на устройстве с дисплеем 4:3.</span><span class="sxs-lookup"><span data-stu-id="35166-140">Pan-and-scan is a technique whereby a widescreen image is cropped to a 4×3 rectangular area, for display on a 4:3 display device.</span></span> <span data-ttu-id="35166-141">Полученное изображение заполняет весь экран, не требуя черной леттербокс областей, но фрагменты исходного изображения обрезаются из изображения.</span><span class="sxs-lookup"><span data-stu-id="35166-141">The resulting image fills the entire display, without requiring black letterbox areas, but portions of the original image are cropped out of the picture.</span></span> <span data-ttu-id="35166-142">Обрезанная область может перемещаться из рамки в рамку в качестве области сдвигов интересов.</span><span class="sxs-lookup"><span data-stu-id="35166-142">The area that is cropped can move from frame to frame, as the area of interest shifts.</span></span> <span data-ttu-id="35166-143">Термин «PAN» в « *сдвиге» и «сканирование* » обозначает эффекты панорамирования, вызванные перемещением области «сдвиг и сканирование».</span><span class="sxs-lookup"><span data-stu-id="35166-143">The term "pan" in *pan-and-scan* refers to the panning effect that is caused by moving the pan-and-scan area.</span></span>

![Схема, показывающая панораму и сканирование](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a><span data-ttu-id="35166-145">Пропорция в пикселях</span><span class="sxs-lookup"><span data-stu-id="35166-145">Pixel Aspect Ratio</span></span>

<span data-ttu-id="35166-146">*Попиксельное соотношение сторон* (номинал) измеряет форму пикселя.</span><span class="sxs-lookup"><span data-stu-id="35166-146">*Pixel aspect ratio* (PAR) measures the shape of a pixel.</span></span>

<span data-ttu-id="35166-147">При захвате цифрового изображения изображение выводится как по вертикали, так и по горизонтали, что приводит к выделению прямоугольного массива примеров квантования, называемых *пикселями* или *пикселей*.</span><span class="sxs-lookup"><span data-stu-id="35166-147">When a digital image is captured, the image is sampled both vertically and horizontally, resulting in a rectangular array of quantized samples, called *pixels* or *pels*.</span></span> <span data-ttu-id="35166-148">Форма сетки выборки определяет форму пикселей в разрядном изображении.</span><span class="sxs-lookup"><span data-stu-id="35166-148">The shape of the sampling grid determines the shape of the pixels in the digitized image.</span></span>

<span data-ttu-id="35166-149">Ниже приведен пример, в котором для упрощения математических вычислений используются небольшие числа.</span><span class="sxs-lookup"><span data-stu-id="35166-149">Here is an example that uses small numbers to keep the math simple.</span></span> <span data-ttu-id="35166-150">Предположим, что исходное изображение является квадратным (то есть пропорция изображения — 1:1); Предположим, что сетка выборки содержит 12 элементов, расположенных в сетке 4 × 3.</span><span class="sxs-lookup"><span data-stu-id="35166-150">Suppose that the original image is square (that is, the picture aspect ratio is 1:1); and suppose the sampling grid contains 12 elements, arranged in a 4×3 grid.</span></span> <span data-ttu-id="35166-151">Форма каждого полученного пикселя будет больше по сравнению с шириной в ширину.</span><span class="sxs-lookup"><span data-stu-id="35166-151">The shape of each resulting pixel will be taller than it is wide.</span></span> <span data-ttu-id="35166-152">В частности, форма каждого пикселя будет иметь значение 3 × 4.</span><span class="sxs-lookup"><span data-stu-id="35166-152">Specifically, the shape of each pixel will be 3×4.</span></span> <span data-ttu-id="35166-153">Пиксели, которые не являются квадратными, называются *неквадратными пикселями*.</span><span class="sxs-lookup"><span data-stu-id="35166-153">Pixels that are not square are called *non-square pixels*.</span></span>

![Схема, показывающая неквадратную сетку выборки](images/aspect-ratio05.png)

<span data-ttu-id="35166-155">Пропорции пикселя также применяются к устройству вывода.</span><span class="sxs-lookup"><span data-stu-id="35166-155">Pixel aspect ratio also applies to the display device.</span></span> <span data-ttu-id="35166-156">Физическая форма устройства вывода и разрешение физического пикселя (по горизонтали и вертикали) определяют номинал отображаемого устройства.</span><span class="sxs-lookup"><span data-stu-id="35166-156">The physical shape of the display device and the physical pixel resolution (across and down) determine the PAR of the display device.</span></span> <span data-ttu-id="35166-157">Мониторы компьютеров обычно используют квадратные пикселы.</span><span class="sxs-lookup"><span data-stu-id="35166-157">Computer monitors generally use square pixels.</span></span> <span data-ttu-id="35166-158">Если изображение имеет номинал и отображаемое значение не совпадает, изображение должно масштабироваться в одном или вертикальном или горизонтальном порядке для правильного вывода.</span><span class="sxs-lookup"><span data-stu-id="35166-158">If the image PAR and the display PAR do not match, the image must be scaled in one dimension, either vertically or horizontally, in order to display correctly.</span></span> <span data-ttu-id="35166-159">Следующая формула относится к НОМИНАЛу, отображению пропорций (DAR) и размеру изображения в пикселях:</span><span class="sxs-lookup"><span data-stu-id="35166-159">The following formula relates PAR, display aspect ratio (DAR), and image size in pixels:</span></span>

<span data-ttu-id="35166-160">*Dar* = (*Ширина изображения в пикселях*  /  *Высота изображения в пикселях*) × *номинал*</span><span class="sxs-lookup"><span data-stu-id="35166-160">*DAR* = (*image width in pixels* / *image height in pixels*) × *PAR*</span></span>

<span data-ttu-id="35166-161">Обратите внимание, что ширина и высота изображения в этой формуле относятся к изображению в памяти, а не к отображаемому изображению.</span><span class="sxs-lookup"><span data-stu-id="35166-161">Note that image width and image height in this formula refer to the image in memory, not the displayed image.</span></span>

<span data-ttu-id="35166-162">Пример практического практического примера: аналоговый видеоролик NTSC-M содержит строки сканирования 480 в активной области изображения.</span><span class="sxs-lookup"><span data-stu-id="35166-162">Here is a real-world example: NTSC-M analog video contains 480 scan lines in the active image area.</span></span> <span data-ttu-id="35166-163">ITU-R Rec. BT. 601 задает горизонтальную частоту выборки 704 видимых пикселей в строке, что приводит к получению цифрового изображения с 704 x 480 пикселей.</span><span class="sxs-lookup"><span data-stu-id="35166-163">ITU-R Rec. BT.601 specifies a horizontal sampling rate of 704 visible pixels per line, yielding a digital image with 704 x 480 pixels.</span></span> <span data-ttu-id="35166-164">Предполагаемый пропорции изображения — 4:3, что дает НОМИНАЛу 10:11.</span><span class="sxs-lookup"><span data-stu-id="35166-164">The intended picture aspect ratio is 4:3, yielding a PAR of 10:11.</span></span>

-   <span data-ttu-id="35166-165">DAR: 4:3</span><span class="sxs-lookup"><span data-stu-id="35166-165">DAR: 4:3</span></span>
-   <span data-ttu-id="35166-166">Ширина в пикселях: 704</span><span class="sxs-lookup"><span data-stu-id="35166-166">Width in pixels: 704</span></span>
-   <span data-ttu-id="35166-167">Высота в пикселях: 480</span><span class="sxs-lookup"><span data-stu-id="35166-167">Height in pixels: 480</span></span>
-   <span data-ttu-id="35166-168">НОМИНАЛ: 10/11</span><span class="sxs-lookup"><span data-stu-id="35166-168">PAR: 10/11</span></span>

<span data-ttu-id="35166-169">4/3 = (704/420) x (10/11)</span><span class="sxs-lookup"><span data-stu-id="35166-169">4/3 = (704/420) x (10/11)</span></span>

<span data-ttu-id="35166-170">Чтобы правильно отобразить это изображение на устройстве вывода с квадратными пикселами, необходимо масштабировать ширину на 10/11 или высоту на 11/10.</span><span class="sxs-lookup"><span data-stu-id="35166-170">To display this image correctly on a display device with square pixels, you must scale either the width by 10/11 or the height by 11/10.</span></span>

## <a name="working-with-aspect-ratios"></a><span data-ttu-id="35166-171">Работа с пропорциями</span><span class="sxs-lookup"><span data-stu-id="35166-171">Working with Aspect Ratios</span></span>

<span data-ttu-id="35166-172">Правильная форма видеокадра определяется *попиксельным пропорциями* (номинал) и *областью просмотра*.</span><span class="sxs-lookup"><span data-stu-id="35166-172">The correct shape of a video frame is defined by the *pixel aspect ratio* (PAR) and the *display area*.</span></span>

-   <span data-ttu-id="35166-173">Номинал определяет форму пикселей в изображении.</span><span class="sxs-lookup"><span data-stu-id="35166-173">The PAR defines the shape of the pixels in an image.</span></span> <span data-ttu-id="35166-174">Квадратные пиксели имеют пропорции 1:1.</span><span class="sxs-lookup"><span data-stu-id="35166-174">Square pixels have an aspect ratio of 1:1.</span></span> <span data-ttu-id="35166-175">Любые другие пропорции описывают неквадратные Пиксели.</span><span class="sxs-lookup"><span data-stu-id="35166-175">Any other aspect ratio describes a non-square pixel.</span></span> <span data-ttu-id="35166-176">Например, NTSC-Телевизор использует 10:11 НОМИНАЛа.</span><span class="sxs-lookup"><span data-stu-id="35166-176">For example, NTSC television uses a 10:11 PAR.</span></span> <span data-ttu-id="35166-177">Если вы проводите показ видео на мониторе компьютера, экран будет иметь квадратные пиксели (1:1 номинал).</span><span class="sxs-lookup"><span data-stu-id="35166-177">Assuming that you are presenting the video on a computer monitor, the display will have square pixels (1:1 PAR).</span></span> <span data-ttu-id="35166-178">Значение НОМИНАЛа для исходного содержимого указывается в атрибуте пропорции [**MF \_ MT \_ \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md) в типе носителя.</span><span class="sxs-lookup"><span data-stu-id="35166-178">The PAR of the source content is given in the [**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute on the media type.</span></span>
-   <span data-ttu-id="35166-179">Область отображения — это регион видеоизображения, которое должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="35166-179">The display area is the region of the video image that is intended to be shown.</span></span> <span data-ttu-id="35166-180">Существует две соответствующие области, которые можно указать в типе носителя:</span><span class="sxs-lookup"><span data-stu-id="35166-180">There are two relevant display areas that might be specified in the media type:</span></span>
    -   <span data-ttu-id="35166-181">Апертура и сканирование.</span><span class="sxs-lookup"><span data-stu-id="35166-181">Pan-and-scan aperture.</span></span> <span data-ttu-id="35166-182">Апертура "сдвиг и сканирование" — это 4 × 3 региона видео, который должен отображаться в режиме панорамирования и сканирования.</span><span class="sxs-lookup"><span data-stu-id="35166-182">The pan-and-scan aperture is a 4×3 region of video that should be displayed in pan/scan mode.</span></span> <span data-ttu-id="35166-183">Он используется для отображения содержимого на широком экране на 4 × 3 дисплее без пустых.</span><span class="sxs-lookup"><span data-stu-id="35166-183">It is used to show wide-screen content on a 4×3 display without letterboxing.</span></span> <span data-ttu-id="35166-184">Апертура «сдвиг и сканирование» задается в атрибуте [**\_ \_ \_ \_ апертуры панорамного поиска в MF**](mf-mt-pan-scan-aperture-attribute.md) , и его следует использовать только в том случае, если атрибуту « [**\_ \_ \_ \_ Включить сканирование MF в Pan**](mf-mt-pan-scan-enabled-attribute.md) » задано **значение true**.</span><span class="sxs-lookup"><span data-stu-id="35166-184">The pan-and-scan aperture is given in the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute and should be used only when the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute is **TRUE**.</span></span>
    -   <span data-ttu-id="35166-185">Отображение апертуры.</span><span class="sxs-lookup"><span data-stu-id="35166-185">Display aperture.</span></span> <span data-ttu-id="35166-186">Это Апертура определено в некоторых стандартах видео.</span><span class="sxs-lookup"><span data-stu-id="35166-186">This aperture is defined in some video standards.</span></span> <span data-ttu-id="35166-187">Все, что находится за пределами отображаемого Апертура, является областью пересканирования и не должна отображаться.</span><span class="sxs-lookup"><span data-stu-id="35166-187">Anything outside of the display aperture is the overscan region and should not be displayed.</span></span> <span data-ttu-id="35166-188">Например, NTSC-телевизор — 720 × 480 пикселей с отображаемым апертуром в 704 × 480.</span><span class="sxs-lookup"><span data-stu-id="35166-188">For example, NTSC television is 720×480 pixels with a display aperture of 704×480.</span></span> <span data-ttu-id="35166-189">Отображаемый Апертура задается в атрибуте « [**\_ \_ Минимальный \_ отображаемый \_ Апертура MF MT**](mf-mt-minimum-display-aperture-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="35166-189">The display aperture is given in the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span> <span data-ttu-id="35166-190">Если он есть, его следует использовать, если режим панорамирования и сканирования имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="35166-190">If present, it should be used when pan-and-scan mode is **FALSE**.</span></span>

<span data-ttu-id="35166-191">Если режим "сдвиг и с" имеет **значение false** и не задано окно апертуры, отображается весь видеокадр.</span><span class="sxs-lookup"><span data-stu-id="35166-191">If pan-and-can mode is **FALSE** and no display aperture is defined, the entire video frame should be displayed.</span></span> <span data-ttu-id="35166-192">На самом деле, это так для большинства видеоматериалов, отличных от телевизионных и DVD-видео.</span><span class="sxs-lookup"><span data-stu-id="35166-192">In fact, this is the case for most video content other than television and DVD video.</span></span> <span data-ttu-id="35166-193">Пропорции всего изображения рассчитывается как (*Отображаемая ширина*  /  *отображаемой области высота*) × *номинал*.</span><span class="sxs-lookup"><span data-stu-id="35166-193">The aspect ratio of the entire picture is calculated as (*display area width* / *display area height*) × *PAR*.</span></span>

## <a name="code-examples"></a><span data-ttu-id="35166-194">Примеры кода</span><span class="sxs-lookup"><span data-stu-id="35166-194">Code Examples</span></span>

### <a name="finding-the-display-area"></a><span data-ttu-id="35166-195">Поиск отображаемой области</span><span class="sxs-lookup"><span data-stu-id="35166-195">Finding the Display Area</span></span>

<span data-ttu-id="35166-196">В следующем коде показано, как получить область отображения из типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="35166-196">The following code shows how to get the display area from the media type.</span></span>


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a><span data-ttu-id="35166-197">Преобразование между пропорциями в пикселях</span><span class="sxs-lookup"><span data-stu-id="35166-197">Converting Between Pixel Aspect Ratios</span></span>

<span data-ttu-id="35166-198">В следующем коде показано, как преобразовать прямоугольник из одной пиксельной пропорции (НОМИНАЛа) в другую, сохраняя пропорции изображения.</span><span class="sxs-lookup"><span data-stu-id="35166-198">The following code shows how to convert a rectangle from one pixel aspect ratio (PAR) to another, while preserving the picture aspect ratio.</span></span>


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a><span data-ttu-id="35166-199">Вычисление области Леттербокс</span><span class="sxs-lookup"><span data-stu-id="35166-199">Calculating the Letterbox Area</span></span>

<span data-ttu-id="35166-200">Следующий код вычисляет область леттербокс с учетом исходного и целевого прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="35166-200">The following code calculates the letterbox area, given a source and destination rectangle.</span></span> <span data-ttu-id="35166-201">Предполагается, что оба прямоугольника имеют одинаковое значение НОМИНАЛа.</span><span class="sxs-lookup"><span data-stu-id="35166-201">It is assumed that both rectangles have the same PAR.</span></span>


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a><span data-ttu-id="35166-202">См. также</span><span class="sxs-lookup"><span data-stu-id="35166-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35166-203">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="35166-203">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="35166-204">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="35166-204">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="35166-205">**\_ \_ Минимальный \_ \_ Апертура экрана MF MT**</span><span class="sxs-lookup"><span data-stu-id="35166-205">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="35166-206">**\_ \_ \_ Апертура для поиска MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="35166-206">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="35166-207">**\_ \_ включена проверка панорамы MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="35166-207">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[<span data-ttu-id="35166-208">**пропорции MF \_ MT \_ пикселей \_ \_**</span><span class="sxs-lookup"><span data-stu-id="35166-208">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



