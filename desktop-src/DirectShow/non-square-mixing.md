---
description: Смешение без квадрата
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Смешение без квадрата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537691"
---
# <a name="non-square-mixing"></a><span data-ttu-id="08d42-103">Смешение без квадрата</span><span class="sxs-lookup"><span data-stu-id="08d42-103">Non-Square Mixing</span></span>

<span data-ttu-id="08d42-104">Этот раздел относится к пакету обновления 2 (SP2) для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="08d42-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="08d42-105">Когда VMR-9 наследует два или более потока, существует две точки, в которых может произойти масштабирование: когда микшер передает входные потоки и когда распределитель-представление визуализирует составное изображение.</span><span class="sxs-lookup"><span data-stu-id="08d42-105">When the VMR-9 mixes two or more streams, there are two points where scaling can occur: When the mixer composites the input streams, and when the allocator-presenter renders the composited image.</span></span>

![операции смешения VMR](images/vmr-nonsquare-mixing.png)

<span data-ttu-id="08d42-107">Предыдущие версии VMR-9 всегда составируют входные потоки с помощью квадратного (1:1) пиксельного пропорций (НОМИНАЛа), даже если существовал только один видеопоток.</span><span class="sxs-lookup"><span data-stu-id="08d42-107">Previous versions of the VMR-9 always composited the input streams using a square (1:1) pixel aspect ratio (PAR), even when there was only a single video stream.</span></span> <span data-ttu-id="08d42-108">Если входной поток имел неквадратные Пиксели, это привело к ненужной операции масштабирования.</span><span class="sxs-lookup"><span data-stu-id="08d42-108">If the input stream had non-square pixels, this caused an unnecessary scaling operation.</span></span> <span data-ttu-id="08d42-109">Масштабирование следует избегать по возможности, так как оно снижает качество окончательного изображения.</span><span class="sxs-lookup"><span data-stu-id="08d42-109">Scaling should be avoided as much as possible, of course, because it degrades the final image quality.</span></span>

<span data-ttu-id="08d42-110">Начиная с Windows XP с пакетом обновления 2 (SP2), VMR-9 поддерживает два разных способа избежать проблемы двойного масштабирования:</span><span class="sxs-lookup"><span data-stu-id="08d42-110">Starting in Windows XP Service Pack 2, the VMR-9 supports two different ways to avoid the problem of double scaling:</span></span>

-   <span data-ttu-id="08d42-111">Реализуйте пользовательский распределитель-представление и поддержку интерфейса [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) .</span><span class="sxs-lookup"><span data-stu-id="08d42-111">Implement a custom allocator-presenter and support the [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) interface.</span></span>
-   <span data-ttu-id="08d42-112">Использовать режим смешения в режиме без квадрата.</span><span class="sxs-lookup"><span data-stu-id="08d42-112">Use non-square mixing mode.</span></span>

<span data-ttu-id="08d42-113">В этом разделе описывается режим смешения в квадратных отделах.</span><span class="sxs-lookup"><span data-stu-id="08d42-113">This section describes non-square mixing mode.</span></span> <span data-ttu-id="08d42-114">Приложения могут сочетать оба метода.</span><span class="sxs-lookup"><span data-stu-id="08d42-114">Applications can combine both techniques.</span></span>

<span data-ttu-id="08d42-115">**Принцип работы без квадратных смешений**</span><span class="sxs-lookup"><span data-stu-id="08d42-115">**How Non-Square Mixing Works**</span></span>

<span data-ttu-id="08d42-116">В режиме смешения с квадратом VMR-9 выбирает один входной поток в качестве целевого размера и НОМИНАЛа.</span><span class="sxs-lookup"><span data-stu-id="08d42-116">In non-square mixing mode, the VMR-9 selects one input stream to be the target size and PAR.</span></span> <span data-ttu-id="08d42-117">Микшер VMR не масштабирует видео из этого потока или из других потоков с тем же размером изображения и НОМИНАЛом.</span><span class="sxs-lookup"><span data-stu-id="08d42-117">The VMR's mixer does not scale the video from that stream or from any other streams with the same image size and PAR.</span></span> <span data-ttu-id="08d42-118">Потоки с другим размером или пропорциями масштабируются в соответствии с целевыми НОМИНАЛами и леттербоксед в соответствии с конечным размером выходного изображения.</span><span class="sxs-lookup"><span data-stu-id="08d42-118">Streams with a different size or aspect ratio are scaled to match the target PAR and letterboxed to fit the final output image size.</span></span>

<span data-ttu-id="08d42-119">Выбор потоков зависит от текущего режима смешивания:</span><span class="sxs-lookup"><span data-stu-id="08d42-119">The choice of streams depends on the current mixing mode:</span></span>

-   <span data-ttu-id="08d42-120">Режим смешения YUV ограничен одним видеопотоком на ПИН-коде 0.</span><span class="sxs-lookup"><span data-stu-id="08d42-120">YUV mixing mode is restricted to one video stream on pin 0.</span></span> <span data-ttu-id="08d42-121">(Другие ПИН-коды могут иметь подизображение или потоки закрытых титров.) Поэтому VMR-9 всегда выбирает закрепление 0 для целевого образа и НОМИНАЛа.</span><span class="sxs-lookup"><span data-stu-id="08d42-121">(The other pins may have subpicture or closed caption streams.) Therefore, the VMR-9 always selects pin 0 for the target image size and PAR.</span></span>
-   <span data-ttu-id="08d42-122">В режиме смешения RGB фильтр VMR выбирает поток с самым большим размером изображения.</span><span class="sxs-lookup"><span data-stu-id="08d42-122">In RGB mixing mode, the VMR selects the stream with the largest image size.</span></span> <span data-ttu-id="08d42-123">Если имеется более одного, он выбирается с максимальным z-порядком. Если по-прежнему есть связь, он выбирает поток с наименьшим PIN-кодом.</span><span class="sxs-lookup"><span data-stu-id="08d42-123">If there is more than one, it selects the one with the highest z-order; and if there is still a tie, it selects the stream with the lowest pin number.</span></span>

<span data-ttu-id="08d42-124">**Примеры операций**</span><span class="sxs-lookup"><span data-stu-id="08d42-124">**Examples of Operation**</span></span>

<span data-ttu-id="08d42-125">**Пример 1.**</span><span class="sxs-lookup"><span data-stu-id="08d42-125">**Example 1.**</span></span> <span data-ttu-id="08d42-126">Поток 0 — 720 x 480 пикселей с пропорциями изображения в 16:9.</span><span class="sxs-lookup"><span data-stu-id="08d42-126">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="08d42-127">Поток 1 — 640 x 480 пикселей с пропорциями изображения в 4:3.</span><span class="sxs-lookup"><span data-stu-id="08d42-127">Stream 1 is a 640 x 480 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="08d42-128">В этом примере поток 0 имеет самый крупный размер изображения, поэтому VMR выбирает этот поток независимо от режима смешения RGB или режима смешивания ЮБ.</span><span class="sxs-lookup"><span data-stu-id="08d42-128">In this example, stream 0 has the largest image size, so the VMR chooses this stream, regardless of RGB mixing mode or YUB mixing mode.</span></span> <span data-ttu-id="08d42-129">Номинал равен 32:27 (16:9/720:480). Это означает, что изображение должно растягиваться по горизонтали с помощью этого соотношения для получения правильных пропорций изображения в 16:9.</span><span class="sxs-lookup"><span data-stu-id="08d42-129">The PAR is 32:27 (16:9 / 720:480), meaning the image must be stretched horizontally by this ratio to produce the correct 16:9 picture aspect ratio.</span></span>

<span data-ttu-id="08d42-130">Чтобы сопоставить целевую НОМИНАЛу, микшер VMR масштабирует поток 1 на обратный коэффициент (27:32), что приводит к получению изображения 540 x 480.</span><span class="sxs-lookup"><span data-stu-id="08d42-130">To match the target PAR, the VMR mixer scales stream 1 by the inverse ratio (27:32), resulting in a 540 x 480 image.</span></span> <span data-ttu-id="08d42-131">Затем два потока объединяются на одной поверхности.</span><span class="sxs-lookup"><span data-stu-id="08d42-131">The two streams are then composited onto one surface.</span></span> <span data-ttu-id="08d42-132">Для правильного отображения полученного изображения распределитель должен горизонтально растянуть изображение в соответствии с пропорциями рисунка 16:9.</span><span class="sxs-lookup"><span data-stu-id="08d42-132">To display the resulting image correctly, the allocator presenter must stretch the image horizontally to fit the 16:9 picture aspect ratio.</span></span>

![Пример 1.](images/vmr-nonsquare-mixing2.png)

<span data-ttu-id="08d42-134">**Пример 2.**</span><span class="sxs-lookup"><span data-stu-id="08d42-134">**Example 2.**</span></span> <span data-ttu-id="08d42-135">Поток 0 — 720 x 480 пикселей с пропорциями изображения в 16:9.</span><span class="sxs-lookup"><span data-stu-id="08d42-135">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="08d42-136">Поток 1 — 1024 x 768 пикселей с пропорциями изображения в 4:3.</span><span class="sxs-lookup"><span data-stu-id="08d42-136">Stream 1 is a 1024 x 768 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="08d42-137">Если VMR-9 использует режим смешения YUV, он всегда выбирает поток 0.</span><span class="sxs-lookup"><span data-stu-id="08d42-137">If the VMR-9 is using YUV mixing mode, it always selects stream 0.</span></span> <span data-ttu-id="08d42-138">Таким образом, он растягивает поток 1 до 540 x 480 пикселей в соответствии с НОМИНАЛом потока 0.</span><span class="sxs-lookup"><span data-stu-id="08d42-138">Therefore, it stretches stream 1 to 540 x 480 pixels, to match the PAR of stream 0.</span></span>

<span data-ttu-id="08d42-139">Если фильтр VMR-9 использует режим смешения RGB, то в качестве целевого объекта выбирается Stream 1, так как этот поток имеет самый крупный размер изображения.</span><span class="sxs-lookup"><span data-stu-id="08d42-139">If the VMR-9 is using RGB mixing mode, it selects stream 1 as the target, because that stream has the largest image size.</span></span> <span data-ttu-id="08d42-140">Он растягивает поток 0 до размера изображения 1024 x 576 пикселей.</span><span class="sxs-lookup"><span data-stu-id="08d42-140">It stretches stream 0 to an image size of 1024 x 576 pixels.</span></span> <span data-ttu-id="08d42-141">Обратите внимание, что в этом случае составной образ имеет значение 1:1, поэтому распределитель-представление не нужно исправлять для неквадратных пикселей.</span><span class="sxs-lookup"><span data-stu-id="08d42-141">Note that in this case, the composited image has a PAR of 1:1, so the allocator-presenter does not have to correct for non-square pixels.</span></span> <span data-ttu-id="08d42-142">(По-прежнему может потребоваться растяжение видео для учетной записи конечного прямоугольника.)</span><span class="sxs-lookup"><span data-stu-id="08d42-142">(It might still need to stretch the video to account for the destination rectangle.)</span></span>

<span data-ttu-id="08d42-143">**Использование режима смешивания без квадрата**</span><span class="sxs-lookup"><span data-stu-id="08d42-143">**Using Non-Square Mixing Mode**</span></span>

<span data-ttu-id="08d42-144">Если выполняется одно из следующих условий, рекомендуется использовать режим смешения, не являющийся квадратным.</span><span class="sxs-lookup"><span data-stu-id="08d42-144">Non-square mixing mode is recommended if either of the following conditions are true:</span></span>

-   <span data-ttu-id="08d42-145">Приложение никогда не отправляет более одного видеопотока на VMR-9.</span><span class="sxs-lookup"><span data-stu-id="08d42-145">Your application never sends more than one video stream to the VMR-9.</span></span>
-   <span data-ttu-id="08d42-146">Приложение визуализирует файлы DVD, телепередач или MS-DVR.</span><span class="sxs-lookup"><span data-stu-id="08d42-146">Your application renders DVD, television, or ms-dvr files.</span></span> <span data-ttu-id="08d42-147">В этом случае следует также использовать режим микширования YUV, если графическое оборудование его поддерживает.</span><span class="sxs-lookup"><span data-stu-id="08d42-147">You should also use YUV mixing mode in this case, if the graphics hardware supports it.</span></span>

<span data-ttu-id="08d42-148">Если приложение смешивает несколько потоков видео, которые могут иметь различные размеры изображения или пропорции пикселей, рекомендуется использовать режим смешения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="08d42-148">If your application mixes multiple video streams that may have varying image sizes or pixel aspect ratios, the default square mixing mode is recommended.</span></span>

<span data-ttu-id="08d42-149">Чтобы настроить режим смешения друг от друга, граф фильтра должен быть остановлен и все входные контакты отключены на VMR-9.</span><span class="sxs-lookup"><span data-stu-id="08d42-149">To configure non-square mixing mode, the filter graph must be stopped and all input pins disconnected on the VMR-9.</span></span> <span data-ttu-id="08d42-150">Затем вызовите [**IVMRMixerControl9:: сетмиксингпрефс**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) с \_ флагом MixerPref9 нонскуаремиксинг:</span><span class="sxs-lookup"><span data-stu-id="08d42-150">Then call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_NonSquareMixing flag:</span></span>


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> <span data-ttu-id="08d42-151">Если вы объединяете \_ флаг MixerPref9 нонскуаремиксинг с \_ флагом MixerPref9 АРАДЖУСТКСОРИ, VMR-9 игнорирует \_ флаг MixerPref9 араджустксори.</span><span class="sxs-lookup"><span data-stu-id="08d42-151">If you combine the MixerPref9\_NonSquareMixing flag with the MixerPref9\_ARAdjustXorY flag, the VMR-9 ignores the MixerPref9\_ARAdjustXorY flag.</span></span>

 

<span data-ttu-id="08d42-152">Если приложение использует пользовательский распределитель-представление с неквадратным режимом смешения, имейте в виду, что составное изображение может иметь неквадратные НОМИНАЛы.</span><span class="sxs-lookup"><span data-stu-id="08d42-152">If your application uses a custom allocator-presenter with non-square mixing mode, be aware that the composited image may have a non-square PAR.</span></span> <span data-ttu-id="08d42-153">Распределитель-выступающий должен масштабировать изображение до квадрата (1:1) номинал.</span><span class="sxs-lookup"><span data-stu-id="08d42-153">The allocator-presenter must scale the image to a square (1:1) PAR.</span></span>

<span data-ttu-id="08d42-154">**Статические растровые изображения**</span><span class="sxs-lookup"><span data-stu-id="08d42-154">**Static Bitmaps**</span></span>

<span data-ttu-id="08d42-155">Если вы используете интерфейс [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) для смешения статического растрового изображения на видео, вы должны считать, что точечный рисунок является вторым видеопотоком в целях смешения в режиме VMR.</span><span class="sxs-lookup"><span data-stu-id="08d42-155">If you use the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface to blend a static bitmap onto the video, you should consider the bitmap to be a second video stream for purposes of the VMR mixing mode.</span></span>

<span data-ttu-id="08d42-156">VMR считает, что точечный рисунок имеет то же значение номинал, что и целевой объект.</span><span class="sxs-lookup"><span data-stu-id="08d42-156">The VMR treats the bitmap as having the same PAR as the target.</span></span> <span data-ttu-id="08d42-157">Он не масштабирует точечный рисунок для настройки пропорций целевого пикселя.</span><span class="sxs-lookup"><span data-stu-id="08d42-157">It does not scale the bitmap to adjust for the target's pixel aspect ratio.</span></span> <span data-ttu-id="08d42-158">В конфигурации VMR по умолчанию у целевого объекта есть 1:1 номинал, который соответствует большинству точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="08d42-158">In the VMR's default configuration, the target has a 1:1 PAR, which matches most bitmaps.</span></span> <span data-ttu-id="08d42-159">В режиме неквадратной смешения целевой объект может иметь неквадратные Пиксели.</span><span class="sxs-lookup"><span data-stu-id="08d42-159">In non-square mixing mode, the target might have non-square pixels.</span></span> <span data-ttu-id="08d42-160">Чтобы обеспечить правильное отображение точечного рисунка, приложение должно предоставить изображение, номинал которого соответствует целевому НОМИНАЛу.</span><span class="sxs-lookup"><span data-stu-id="08d42-160">To ensure that the bitmap is displayed correctly, the application should supply an image whose PAR matches the target PAR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08d42-161">См. также</span><span class="sxs-lookup"><span data-stu-id="08d42-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08d42-162">Использование режима смешения VMR</span><span class="sxs-lookup"><span data-stu-id="08d42-162">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



