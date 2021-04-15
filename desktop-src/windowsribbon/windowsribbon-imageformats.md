---
title: Указание ресурсов изображения ленты
description: В качестве обширной системы представления команд платформа Windows Ribbon разработана для обеспечения широкого спектра графических ресурсов на протяжении всего пользовательского интерфейса ленты. Все ресурсы изображений объявляются в разметке ленты или запрашиваются из хост-приложения ленты.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Лента Windows, ресурсы изображений
- Лента, ресурсы изображений
- Лента Windows, прозрачность
- Лента, прозрачность
- Лента Windows, глубина цвета
- Лента, глубина цвета
- Лента Windows, контрастность
- Лента, контрастность
- ресурсы изображений на ленте Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488124"
---
# <a name="specifying-ribbon-image-resources"></a><span data-ttu-id="e0297-113">Указание ресурсов изображения ленты</span><span class="sxs-lookup"><span data-stu-id="e0297-113">Specifying Ribbon Image Resources</span></span>

<span data-ttu-id="e0297-114">В качестве обширной системы представления команд платформа Windows Ribbon разработана для обеспечения широкого спектра графических ресурсов на протяжении всего пользовательского интерфейса ленты.</span><span class="sxs-lookup"><span data-stu-id="e0297-114">As a rich command presentation system, the Windows Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="e0297-115">Все ресурсы изображений объявляются в [разметке ленты](windowsribbon-schema.md) или запрашиваются из хост-приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="e0297-115">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="e0297-116">Для Windows 8 и более поздних версий платформа Ribbon поддерживает следующие форматы графики: 32-битовые растровые файлы ARGB (BMP) и PNG-файлы с прозрачностью.</span><span class="sxs-lookup"><span data-stu-id="e0297-116">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="e0297-117">Для Windows 7 и более ранних версий ресурсы образа должны соответствовать стандартному графическому формату BMP, используемому в Windows.</span><span class="sxs-lookup"><span data-stu-id="e0297-117">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="e0297-118">Если платформе предоставляется неподдерживаемый формат изображения, может возникнуть ошибка компиляции.</span><span class="sxs-lookup"><span data-stu-id="e0297-118">A compilation error may occur if an unsupported image format is supplied to the framework.</span></span>

 

## <a name="image-sizes"></a><span data-ttu-id="e0297-119">Размеры изображений</span><span class="sxs-lookup"><span data-stu-id="e0297-119">Image Sizes</span></span>

<span data-ttu-id="e0297-120">Чтобы обеспечить большую гибкость для макетов элементов управления ленты при изменении размера окна приложения, платформа Ribbon принимает и визуализирует изображения в одном из двух размеров: крупный или маленький.</span><span class="sxs-lookup"><span data-stu-id="e0297-120">To provide greater flexibility for Ribbon control layouts when resizing an application window, the Ribbon framework accepts and renders images in one of two sizes: large or small.</span></span>

<span data-ttu-id="e0297-121">На следующих рисунках показано приложение ленты, которое поддерживает несколько размеров ленты с помощью гибких макетов элементов управления и замены больших изображений с помощью небольших изображений, где они доступны.</span><span class="sxs-lookup"><span data-stu-id="e0297-121">The following images illustrate a Ribbon application that supports multiple Ribbon sizes through flexible control layouts and the replacement of large images with small images where available.</span></span>

<span data-ttu-id="e0297-122">На следующем снимке экрана показана лента с большими изображениями для элементов управления масштабом.</span><span class="sxs-lookup"><span data-stu-id="e0297-122">The following screen shot shows the Ribbon with large images for the Zoom controls.</span></span>

![снимок экрана, на котором показана лента, использующая крупные изображения для элементов управления масштабом.](images/overviews/imageresources-largeimage.png)

<span data-ttu-id="e0297-124">На следующем снимке экрана показана та же лента с мелкими изображениями для элементов управления масштабом.</span><span class="sxs-lookup"><span data-stu-id="e0297-124">The following screen shot shows the same Ribbon resized with small images for the Zoom controls</span></span>

![снимок экрана, на котором показана лента, использующая небольшие изображения для элементов управления масштабом.](images/overviews/imageresources-smallimage.png)

<span data-ttu-id="e0297-126">На следующем снимке экрана показана лента в скрытом состоянии.</span><span class="sxs-lookup"><span data-stu-id="e0297-126">The following screen shot shows the ribbon in hidden state.</span></span> <span data-ttu-id="e0297-127">Лента скрывается, когда все возможные макеты элементов управления исчерпаны, и лента не может быть подготовлена к использованию рабочей областью приложения.</span><span class="sxs-lookup"><span data-stu-id="e0297-127">The ribbon is hidden when all potential control layouts have been exhausted and the ribbon cannot be rendered with a usable application workspace.</span></span>

![снимок экрана, показывающий свернутую ленту.](images/overviews/imageresources-noimage.png)

<span data-ttu-id="e0297-129">Для любого изображения точный размер пикселя зависит от разрешения экрана или от точек на дюйм (DPI) используемого монитора.</span><span class="sxs-lookup"><span data-stu-id="e0297-129">For any image, the exact pixel size is dependent on the display resolution, or dots per inch (dpi), of the monitor being used.</span></span> <span data-ttu-id="e0297-130">При 96 dpi крупные изображения имеют размер 32x32 пикселя, а небольшие — 16x16 пикселей в размере.</span><span class="sxs-lookup"><span data-stu-id="e0297-130">At 96 dpi, large images are 32x32 pixels in size and small images are 16x16 pixels in size.</span></span> <span data-ttu-id="e0297-131">Размеры изображений увеличиваются в линейной манере относительно dpi, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e0297-131">The image sizes increase in a linear fashion relative to dpi as illustrated in the following table.</span></span>



| <span data-ttu-id="e0297-132">DPI</span><span class="sxs-lookup"><span data-stu-id="e0297-132">DPI</span></span>     | <span data-ttu-id="e0297-133">Небольшое изображение</span><span class="sxs-lookup"><span data-stu-id="e0297-133">Small Image</span></span>  | <span data-ttu-id="e0297-134">Большое изображение</span><span class="sxs-lookup"><span data-stu-id="e0297-134">Large Image</span></span>  |
|---------|--------------|--------------|
| <span data-ttu-id="e0297-135">96 точек на дюйм</span><span class="sxs-lookup"><span data-stu-id="e0297-135">96 dpi</span></span>  | <span data-ttu-id="e0297-136">16x16 пикселей</span><span class="sxs-lookup"><span data-stu-id="e0297-136">16x16 pixels</span></span> | <span data-ttu-id="e0297-137">32x32 пикселя</span><span class="sxs-lookup"><span data-stu-id="e0297-137">32x32 pixels</span></span> |
| <span data-ttu-id="e0297-138">120 точек на дюйм</span><span class="sxs-lookup"><span data-stu-id="e0297-138">120 dpi</span></span> | <span data-ttu-id="e0297-139">20x20 пикселей</span><span class="sxs-lookup"><span data-stu-id="e0297-139">20x20 pixels</span></span> | <span data-ttu-id="e0297-140">40x40 пикселей</span><span class="sxs-lookup"><span data-stu-id="e0297-140">40x40 pixels</span></span> |
| <span data-ttu-id="e0297-141">144 точек на дюйм</span><span class="sxs-lookup"><span data-stu-id="e0297-141">144 dpi</span></span> | <span data-ttu-id="e0297-142">24x24 пикселей</span><span class="sxs-lookup"><span data-stu-id="e0297-142">24x24 pixels</span></span> | <span data-ttu-id="e0297-143">48x48 пикселей</span><span class="sxs-lookup"><span data-stu-id="e0297-143">48x48 pixels</span></span> |
| <span data-ttu-id="e0297-144">192 точек на дюйм</span><span class="sxs-lookup"><span data-stu-id="e0297-144">192 dpi</span></span> | <span data-ttu-id="e0297-145">32x32 пикселя</span><span class="sxs-lookup"><span data-stu-id="e0297-145">32x32 pixels</span></span> | <span data-ttu-id="e0297-146">64 x 64 пикселей</span><span class="sxs-lookup"><span data-stu-id="e0297-146">64x64 pixels</span></span> |



 

<span data-ttu-id="e0297-147">Платформа Ribbon масштабирует ресурсы изображения по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="e0297-147">The Ribbon framework scales image resources as required.</span></span> <span data-ttu-id="e0297-148">Однако, поскольку изменение размера может привести к нежелательным артефактам и ухудшению изображения, настоятельно рекомендуется, чтобы приложение преддавало небольшой набор графических ресурсов, которые охватывают различные часто используемые параметры dpi.</span><span class="sxs-lookup"><span data-stu-id="e0297-148">However, because resizing may yield undesirable artifacts and image degradation, it is highly recommended that the application provide a small set of image resources that span various commonly used dpi settings.</span></span> <span data-ttu-id="e0297-149">Если точное соответствие не найдено, то ближайшее изображение будет масштабироваться вверх или вниз.</span><span class="sxs-lookup"><span data-stu-id="e0297-149">If an exact match is not found, the nearest image will be scaled up or down.</span></span>

<span data-ttu-id="e0297-150">Чтобы упростить это, ресурсы изображения можно объявить в разметке ленты, используя набор элементов [**Image**](windowsribbon-element-image.md) для каждого элемента [**Command**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="e0297-150">To facilitate this, image resources can be declared in Ribbon markup by using a set of [**Image**](windowsribbon-element-image.md) elements for each [**Command**](windowsribbon-element-command.md) element.</span></span> <span data-ttu-id="e0297-151">Во время выполнения платформа выбирает изображение для вывода на основе атрибута *миндпи* каждого элемента **Image** .</span><span class="sxs-lookup"><span data-stu-id="e0297-151">At run time, the framework selects the image to display based on the *MinDPI* attribute of each **Image** element.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e0297-152">Если коллекция графических ресурсов, предназначенная для поддержки конкретных параметров dpi на экране, предоставляется для платформы Ribbon через набор элементов [**Image**](windowsribbon-element-image.md) , платформа использует **изображение** со значением атрибута *миндпи* , которое соответствует текущему значению dpi на экране.</span><span class="sxs-lookup"><span data-stu-id="e0297-152">When a collection of image resources that are designed to support specific screen dpi settings is supplied to the Ribbon framework through a set of [**Image**](windowsribbon-element-image.md) elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>
>
> <span data-ttu-id="e0297-153">Если элемент [**Image**](windowsribbon-element-image.md) не объявлен со значением *миндпи* , совпадающим с текущим параметром dpi на экране, платформа выбирает **изображение** с ближайшим значением *миндпи* , которое меньше текущего значения DPI на экране, и масштабирует ресурс изображения.</span><span class="sxs-lookup"><span data-stu-id="e0297-153">If no [**Image**](windowsribbon-element-image.md) element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="e0297-154">В противном случае, если ни один из элементов **изображения** не объявлен с атрибутом *миндпи* , значение которого меньше текущего значения DPI экрана, платформа выбирает ближайшее значение *миндпи* , превышающее текущий параметр dpi на экране, и масштабирует ресурс изображения вниз.</span><span class="sxs-lookup"><span data-stu-id="e0297-154">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

 

<span data-ttu-id="e0297-155">В следующем примере показано, как объявить набор изображений для размещения различных размеров ленты и системных параметров.</span><span class="sxs-lookup"><span data-stu-id="e0297-155">The following example illustrates how to declare a set of images to accommodate various Ribbon sizes and system settings.</span></span>


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



<span data-ttu-id="e0297-156">Если изображения, объявленные в разметке, становятся недействительными во время выполнения по какой-либо причине, ведущее приложение запрашивает новые образы.</span><span class="sxs-lookup"><span data-stu-id="e0297-156">If images declared in markup are invalidated at run time for any reason, the host application is queried for new images.</span></span> <span data-ttu-id="e0297-157">Когда эти образы создаются и загружаются программно, приложение должно попытаться вернуть изображения, размер которых изменяется в соответствии с размерами системных значков по умолчанию, определенными [ \_ системным показателем SM кксикон](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span><span class="sxs-lookup"><span data-stu-id="e0297-157">When these images are generated and loaded programmatically, the application should attempt to return images that are sized according to the default system icon sizes determined by the [SM\_CXICON system metric](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span></span>

> [!Note]  
> <span data-ttu-id="e0297-158">Крупные образы имеют размер SM \_ кксикон на SM кксикон, \_ а небольшие образы имеют размер SM \_ кксикон/2 на SM \_ кксикон/2.</span><span class="sxs-lookup"><span data-stu-id="e0297-158">Large images have a size of SM\_CXICON by SM\_CXICON and small images have a size of SM\_CXICON/2 by SM\_CXICON/2.</span></span>

 

## <a name="color-depth-transparency-and-contrast"></a><span data-ttu-id="e0297-159">Глубина цвета, прозрачность и контрастность</span><span class="sxs-lookup"><span data-stu-id="e0297-159">Color Depth, Transparency, and Contrast</span></span>

<span data-ttu-id="e0297-160">Предполагается, что обычные образы находятся в формате 32 бит на пиксель (бит в пикселах) ARGB и масштабируются до размера значка системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0297-160">Regular images are expected to be in 32 bits per pixel (BPP) ARGB pixel format and scaled to the default system icon size.</span></span> <span data-ttu-id="e0297-161">Этот формат поддерживает как прозрачность, так и сглаживание (по 8 бит на канал).</span><span class="sxs-lookup"><span data-stu-id="e0297-161">This format supports both transparency and antialiasing (using 8 bits per channel).</span></span>

> [!WARNING]
> <span data-ttu-id="e0297-162">Многие инструменты для редактирования изображений не сохраняют самый высокий 8-разрядный канал альфа при загрузке или сохранении образов 32 бит/с.</span><span class="sxs-lookup"><span data-stu-id="e0297-162">Many image editing tools do not preserve the highest order 8-bit alpha channel when loading or saving 32 BPP images.</span></span>

 

<span data-ttu-id="e0297-163">Чтобы изображение отображалось правильно в режиме высокой контрастности, оно должно иметь формат пикселей с размером в 4 пиксела.</span><span class="sxs-lookup"><span data-stu-id="e0297-163">For an image to display correctly in high-contrast mode, it must be in a 4 BPP palletized pixel format.</span></span> <span data-ttu-id="e0297-164">При отрисовке изображения платформа Ribbon сопоставляет определенные цвета на основе контекста с высокой контрастностью изображения.</span><span class="sxs-lookup"><span data-stu-id="e0297-164">When the image is rendered, the Ribbon framework remaps specific colors based on the high-contrast context of the image.</span></span>

<span data-ttu-id="e0297-165">В следующей таблице приводится описание поведения платформы с высокой контрастностью для отрисовки цветов.</span><span class="sxs-lookup"><span data-stu-id="e0297-165">The following table lists the high-contrast color rendering behavior of the framework.</span></span>



<span data-ttu-id="e0297-166">Цвет пикселя</span><span class="sxs-lookup"><span data-stu-id="e0297-166">Pixel color</span></span>

<span data-ttu-id="e0297-167">Значение RGB</span><span class="sxs-lookup"><span data-stu-id="e0297-167">RGB value</span></span>

<span data-ttu-id="e0297-168">Поведение</span><span class="sxs-lookup"><span data-stu-id="e0297-168">Behavior</span></span>

<span data-ttu-id="e0297-169">Белый фон</span><span class="sxs-lookup"><span data-stu-id="e0297-169">White background</span></span>

<span data-ttu-id="e0297-170">Темный фон</span><span class="sxs-lookup"><span data-stu-id="e0297-170">Dark Background</span></span>

<span data-ttu-id="e0297-171">ЦВЕТ</span><span class="sxs-lookup"><span data-stu-id="e0297-171">MAGENTA</span></span>

<span data-ttu-id="e0297-172">800080</span><span class="sxs-lookup"><span data-stu-id="e0297-172">800080</span></span>

<span data-ttu-id="e0297-173">Прозрачный</span><span class="sxs-lookup"><span data-stu-id="e0297-173">Transparent</span></span>

<span data-ttu-id="e0297-174">Прозрачный</span><span class="sxs-lookup"><span data-stu-id="e0297-174">Transparent</span></span>

<span data-ttu-id="e0297-175">ЭКРАН</span><span class="sxs-lookup"><span data-stu-id="e0297-175">BLACK</span></span>

<span data-ttu-id="e0297-176">000000</span><span class="sxs-lookup"><span data-stu-id="e0297-176">000000</span></span>

<span data-ttu-id="e0297-177">ЦВЕТная \_ WINDOWTEXT</span><span class="sxs-lookup"><span data-stu-id="e0297-177">COLOR\_WINDOWTEXT</span></span>

<span data-ttu-id="e0297-178">Белый</span><span class="sxs-lookup"><span data-stu-id="e0297-178">WHITE</span></span>

<span data-ttu-id="e0297-179">Белый</span><span class="sxs-lookup"><span data-stu-id="e0297-179">WHITE</span></span>

<span data-ttu-id="e0297-180">FFFFFF</span><span class="sxs-lookup"><span data-stu-id="e0297-180">FFFFFF</span></span>

<span data-ttu-id="e0297-181">\_окно цвета</span><span class="sxs-lookup"><span data-stu-id="e0297-181">COLOR\_WINDOW</span></span>

<span data-ttu-id="e0297-182">ЭКРАН</span><span class="sxs-lookup"><span data-stu-id="e0297-182">BLACK</span></span>

<span data-ttu-id="e0297-183">ТЕМНО-СЕРЫЙ</span><span class="sxs-lookup"><span data-stu-id="e0297-183">DARK GRAY</span></span>

<span data-ttu-id="e0297-184">808080</span><span class="sxs-lookup"><span data-stu-id="e0297-184">808080</span></span>

<span data-ttu-id="e0297-185">ЦВЕТ \_ 3DSHADOW</span><span class="sxs-lookup"><span data-stu-id="e0297-185">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="e0297-186">ЦВЕТ \_ 3DSHADOW</span><span class="sxs-lookup"><span data-stu-id="e0297-186">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="e0297-187">GRAY</span><span class="sxs-lookup"><span data-stu-id="e0297-187">GRAY</span></span>

<span data-ttu-id="e0297-188">C0C0C0</span><span class="sxs-lookup"><span data-stu-id="e0297-188">C0C0C0</span></span>

<span data-ttu-id="e0297-189">ЦВЕТ \_ 3DFACE</span><span class="sxs-lookup"><span data-stu-id="e0297-189">COLOR\_3DFACE</span></span>

<span data-ttu-id="e0297-190">ЦВЕТ \_ 3DFACE</span><span class="sxs-lookup"><span data-stu-id="e0297-190">COLOR\_3DFACE</span></span>

<span data-ttu-id="e0297-191">СВЕТЛО-СЕРЫЙ</span><span class="sxs-lookup"><span data-stu-id="e0297-191">LIGHT GRAY</span></span>

<span data-ttu-id="e0297-192">дфдфдф</span><span class="sxs-lookup"><span data-stu-id="e0297-192">DFDFDF</span></span>

<span data-ttu-id="e0297-193">ЦВЕТ \_ 3DLIGHT</span><span class="sxs-lookup"><span data-stu-id="e0297-193">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="e0297-194">ЦВЕТ \_ 3DLIGHT</span><span class="sxs-lookup"><span data-stu-id="e0297-194">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="e0297-195">ТЕМНО-СИНИЙ</span><span class="sxs-lookup"><span data-stu-id="e0297-195">DARK BLUE</span></span>

<span data-ttu-id="e0297-196">000080</span><span class="sxs-lookup"><span data-stu-id="e0297-196">000080</span></span>

<span data-ttu-id="e0297-197">Недоступно</span><span class="sxs-lookup"><span data-stu-id="e0297-197">n/a</span></span>

<span data-ttu-id="e0297-198">Белый</span><span class="sxs-lookup"><span data-stu-id="e0297-198">WHITE</span></span>



 

<span data-ttu-id="e0297-199">Дополнительные сведения о форматах изображений, поддерживаемых платформой Ribbon, см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="e0297-199">For more information on the image formats supported by the Ribbon framework, see the following:</span></span>

-   <span data-ttu-id="e0297-200">[Структура битмапинфохеадер](/previous-versions//dd183376(v=vs.85)) . описывает формат пикселей ARGB в 32 бит.</span><span class="sxs-lookup"><span data-stu-id="e0297-200">[BITMAPINFOHEADER structure](/previous-versions//dd183376(v=vs.85)) - describes the 32 BPP ARGB pixel format.</span></span>
-   <span data-ttu-id="e0297-201">[Функция креатедибсектион](/windows/win32/api/wingdi/nf-wingdi-createdibsection) — описывает создание изображения формата пикселей ARGB в 32 бит на пиксель.</span><span class="sxs-lookup"><span data-stu-id="e0297-201">[CreateDIBSection function](/windows/win32/api/wingdi/nf-wingdi-createdibsection) - describes how to create a 32 BPP ARGB pixel format image.</span></span>
-   <span data-ttu-id="e0297-202">[Функция лоадимаже](/windows/win32/api/winuser/nf-winuser-loadimagea) — описывает, как загрузить изображение формата пикселей ARGB в 32 бит на пиксель.</span><span class="sxs-lookup"><span data-stu-id="e0297-202">[LoadImage function](/windows/win32/api/winuser/nf-winuser-loadimagea) - describes how to load a 32 BPP ARGB pixel format image.</span></span>

## <a name="accessibility"></a><span data-ttu-id="e0297-203">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="e0297-203">Accessibility</span></span>

<span data-ttu-id="e0297-204">Использование ресурсов изображений для предоставления информации, передачи функций управления и предоставления состояния приложения увеличивает потребность в требованиях к специальным возможностям во время проектирования и разработки приложений.</span><span class="sxs-lookup"><span data-stu-id="e0297-204">Relying on image resources to provide information, convey control functionality, and expose application state, increases the need for accessibility requirements during application design and development.</span></span>

<span data-ttu-id="e0297-205">Для базовой поддержки высокой контрастности лента позволяет отображать отдельный набор файлов изображений, когда активна тема с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="e0297-205">For basic high contrast support, the Ribbon allows for a separate set of image files to be displayed when a high-contrast theme is active.</span></span> <span data-ttu-id="e0297-206">Эти изображения могут составлять 32 бит/4 бит, с цветами, сопоставленными с специальной палитрой, в которой темные и легкие цвета инвертированы в зависимости от цвета переднего плана и фона активной темы с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="e0297-206">These images can be 32 BPP or 4 BPP, with colors mapped to a special palette where dark and light colors are inverted depending on the foreground and background colors of the active high-contrast theme.</span></span>

<span data-ttu-id="e0297-207">В следующем примере показано, как ресурсы изображения с высокой контрастностью объявляются в разметке ленты.</span><span class="sxs-lookup"><span data-stu-id="e0297-207">The following example demonstrates how high-contrast image resources are declared in Ribbon markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="e0297-208">См. также</span><span class="sxs-lookup"><span data-stu-id="e0297-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0297-209">**Command. Смаллимажес**</span><span class="sxs-lookup"><span data-stu-id="e0297-209">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[<span data-ttu-id="e0297-210">UI \_ PKEY \_ смаллимаже</span><span class="sxs-lookup"><span data-stu-id="e0297-210">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[<span data-ttu-id="e0297-211">**Command. Ларжеимажес**</span><span class="sxs-lookup"><span data-stu-id="e0297-211">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[<span data-ttu-id="e0297-212">UI \_ PKEY \_ ларжеимаже</span><span class="sxs-lookup"><span data-stu-id="e0297-212">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[<span data-ttu-id="e0297-213">**Command. Смаллхигхконтрастимажес**</span><span class="sxs-lookup"><span data-stu-id="e0297-213">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="e0297-214">UI \_ PKEY \_ смаллхигхконтрастимаже</span><span class="sxs-lookup"><span data-stu-id="e0297-214">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[<span data-ttu-id="e0297-215">**Command. Ларжехигхконтрастимажес**</span><span class="sxs-lookup"><span data-stu-id="e0297-215">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="e0297-216">UI \_ PKEY \_ ларжехигхконтрастимаже</span><span class="sxs-lookup"><span data-stu-id="e0297-216">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 