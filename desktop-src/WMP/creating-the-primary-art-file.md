---
title: Создание основного файла изображения
description: Создание основного файла изображения
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- Создание обложек, основных графических файлов
- Обложки проигрывателя Windows Media, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложек, основные образы
- Обложки проигрывателя Windows Media, основные образы
- обложки, основные образы
- Основные образы в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104556282"
---
# <a name="creating-the-primary-art-file"></a><span data-ttu-id="5e5f1-111">Создание основного файла изображения</span><span class="sxs-lookup"><span data-stu-id="5e5f1-111">Creating the Primary Art File</span></span>

<span data-ttu-id="5e5f1-112">Основной файл картинки будет содержать рисунок, который видит пользователь обложки.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-112">The primary art file will contain the art that the user of your skin first sees.</span></span> <span data-ttu-id="5e5f1-113">В этом случае вы будете создавать изображения на разных уровнях программы Art.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-113">In this case, you will be creating images in different layers of your art program.</span></span> <span data-ttu-id="5e5f1-114">Причина использования слоев состоит в том, что позже вы будете копировать определенные слои для создания файлов карт и альтернативных графических файлов.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-114">The reason for using layers is that you will copy specific layers later to create map files and alternate art files.</span></span>

<span data-ttu-id="5e5f1-115">Чтобы создать основной файл рисунка, необходимо создать следующие слои в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="5e5f1-115">To create the primary art file, you will create the following layers in the following order:</span></span>

<span data-ttu-id="5e5f1-116">Фоновый слой обложки</span><span class="sxs-lookup"><span data-stu-id="5e5f1-116">Skin background layer</span></span>

<span data-ttu-id="5e5f1-117">Это цвет, который будет прозрачным при отображении обложки.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-117">This is the color that will be transparent when the skin is displayed.</span></span> <span data-ttu-id="5e5f1-118">Создайте слой для этого первого, но выберите окончательный цвет этого слоя после выбора цвета для слоя контейнера обложки.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-118">Create a layer for this first, but choose the final color of this layer after you chose a color for the skin container layer.</span></span> <span data-ttu-id="5e5f1-119">Этот цвет должен быть похож на слой контейнера обложки, но не тот же, что и для скрытия эффектов сглаживания.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-119">This color should be similar to, but not the same as, the skin container layer, to hide any anti-aliasing effects.</span></span>

<span data-ttu-id="5e5f1-120">Слой контейнера обложки</span><span class="sxs-lookup"><span data-stu-id="5e5f1-120">Skin container layer</span></span>

<span data-ttu-id="5e5f1-121">Это изображение, которое будет представлять контур обложки и будет отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-121">This is the image that will form the outline of your skin and will be what the user sees.</span></span> <span data-ttu-id="5e5f1-122">Он также будет контейнером для двух кнопок в этом примере.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-122">It also will be the container for the two buttons in this example.</span></span> <span data-ttu-id="5e5f1-123">Представьте себе обложку как контейнер для элементов управления пользовательского интерфейса, таких как кнопки, ползунки и т. д.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-123">Think of your skin as a container for user interface controls such as buttons, sliders, and so on.</span></span> <span data-ttu-id="5e5f1-124">В этом примере контейнер является желтым овалом.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-124">In this example, the container is a yellow oval.</span></span>

<span data-ttu-id="5e5f1-125">Слои кнопок "Воспроизвести" и "Закрыть"</span><span class="sxs-lookup"><span data-stu-id="5e5f1-125">Play and Close button layers</span></span>

<span data-ttu-id="5e5f1-126">В этом примере используются два элемента управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-126">These are the two user interface controls that this example uses.</span></span> <span data-ttu-id="5e5f1-127">Их можно разместить на разных уровнях, чтобы их можно было легко изменить или скопировать позже.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-127">You will put them in separate layers so that you can easily adjust them or copy them later.</span></span>

<span data-ttu-id="5e5f1-128">Перед созданием слоев необходимо создать файл, в котором будут храниться слои.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-128">Before you create your layers, you must create the file that will hold your layers.</span></span> <span data-ttu-id="5e5f1-129">Запустите Photoshop и создайте новый файл размером 100 пикселей в высоком и 200 пикселей в ширину.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-129">Start up Photoshop and create a new file that is 100 pixels high and 200 pixels wide.</span></span> <span data-ttu-id="5e5f1-130">Файл, используемый для создания рисунка для этого примера, называется tiny.psd и входит в состав пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-130">The file used to create the art for this sample is called tiny.psd and is included with the SDK.</span></span>

<span data-ttu-id="5e5f1-131">Все инструкции задаются с точки зрения Photoshop, но любая другая художественная программа может использоваться для создания обложек при условии, что можно сохранить в один из форматов файлов, поддерживаемых проигрывателем Windows Media (BMP, GIF, JPG и PNG).</span><span class="sxs-lookup"><span data-stu-id="5e5f1-131">All instructions are given in terms of Photoshop, but any other art program can be used to create skins as long as you can save to one of the file formats supported by the Windows Media Player (BMP, GIF, JPG, and PNG).</span></span> <span data-ttu-id="5e5f1-132">Вы сможете упростить создание обложки, если вы используете художественную программу с такими слоями, как Adobe Photoshop, Жаск Paint Shop Pro или Жедор Вискосити.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-132">You will find skin creation easier if you use an art program that has layers, such as Adobe Photoshop, Jasc Paint Shop Pro, or Jedor Viscosity.</span></span> <span data-ttu-id="5e5f1-133">Уровни очень полезны, поскольку изображения должны быть правильно согласованы для сопоставления изображений и отображения альтернативных изображений.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-133">Layers are extremely useful because images must be properly aligned for image mapping and display of alternative images.</span></span>

## <a name="skin-background-layer"></a><span data-ttu-id="5e5f1-134">Фоновый слой обложки</span><span class="sxs-lookup"><span data-stu-id="5e5f1-134">Skin Background Layer</span></span>

<span data-ttu-id="5e5f1-135">Создайте новый слой и назовите его "фон обложки".</span><span class="sxs-lookup"><span data-stu-id="5e5f1-135">Create a new layer and name it "Skin background".</span></span> <span data-ttu-id="5e5f1-136">Это станет цветом прозрачности, который будет определен в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-136">This will become the transparency color you will define in the skin definition file.</span></span> <span data-ttu-id="5e5f1-137">Дождитесь выбора цвета для контейнера обложки, прежде чем заполнять фоновый слой обложки конкретным цветом.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-137">Wait until the color for the skin container is chosen before filling the skin background layer with a specific color.</span></span>

## <a name="skin-container-layer"></a><span data-ttu-id="5e5f1-138">Слой контейнера обложки</span><span class="sxs-lookup"><span data-stu-id="5e5f1-138">Skin Container Layer</span></span>

<span data-ttu-id="5e5f1-139">Затем создайте новый слой и назовите его "контейнер обложки".</span><span class="sxs-lookup"><span data-stu-id="5e5f1-139">Next create a new layer and call it "Skin container".</span></span> <span data-ttu-id="5e5f1-140">Он определяет края обложки и будет контейнером для кнопок.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-140">This will define the edges of your skin and will be the container for the buttons.</span></span>

<span data-ttu-id="5e5f1-141">Выберите цвет переднего плана для фигуры с помощью ползунков веб-цвета.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-141">Choose a foreground color for the shape, using the Web color sliders.</span></span> <span data-ttu-id="5e5f1-142">В этом примере был выбран цвет " \# DBDD11".</span><span class="sxs-lookup"><span data-stu-id="5e5f1-142">In this example, the color "\#DBDD11" was chosen.</span></span>

<span data-ttu-id="5e5f1-143">Затем создайте фигуру овала.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-143">Next create an oval shape.</span></span> <span data-ttu-id="5e5f1-144">Самый простой способ — воспользоваться инструментом «Елиптикал область» и создать овал.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-144">The easiest way is to use the Eliptical Marquee tool and create an oval selection.</span></span> <span data-ttu-id="5e5f1-145">После создания овала, имеющего нужный размер и форму, заполните выделенный фрагмент на цвет переднего плана и отмените выбор.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-145">When you have created an oval selection that is the size and shape you want, fill the selection with the foreground color and cancel the selection.</span></span>

<span data-ttu-id="5e5f1-146">Наконец, чтобы сделать этот вид более интересным, примените эффект слоя рельефности и приподнятости со значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-146">Finally, to make this look a bit more interesting, apply the layer effect of Bevel and Emboss with the default values.</span></span>

<span data-ttu-id="5e5f1-147">Слой контейнера обложки должен выглядеть, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-147">Your skin container layer should look like the following illustration.</span></span>

![слой контейнера обложки](images/g01cont.png)

## <a name="background-skin-color"></a><span data-ttu-id="5e5f1-149">Цвет обложки фона</span><span class="sxs-lookup"><span data-stu-id="5e5f1-149">Background Skin Color</span></span>

<span data-ttu-id="5e5f1-150">Теперь, когда вы выбрали цвет переднего плана для фигуры контейнера обложки, можно выбрать аналогичный цвет для фонового слоя обложки.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-150">Now that you have chosen a foreground color for your skin container shape, you can choose a similar color for your skin background layer.</span></span> <span data-ttu-id="5e5f1-151">Вы не хотите точно тот же цвет, или контейнер обложки будет также прозрачным.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-151">You do not want the exact same color, or your skin container will be transparent also.</span></span> <span data-ttu-id="5e5f1-152">На самом деле, убедитесь, что вы не используете этот точный цвет в любом месте обложки, даже в случае, если этот цвет отображается, вместо него отображается изображение рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-152">In fact, be sure you do not use this exact color anywhere else in your skin, even in photographs, because wherever this color appears, the desktop image will appear instead.</span></span>

<span data-ttu-id="5e5f1-153">Необходимо, чтобы цвет контейнера обложки был близко к цвету, чтобы избежать эффектов сглаживания.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-153">You want a color close to the skin container color to avoid anti-aliasing effects.</span></span> <span data-ttu-id="5e5f1-154">Например, если у вас есть черный фон, некоторые биты черного цвета будут отображаться вокруг края обложки.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-154">For example, if you have a black background, some bits of black may show up around the edge of your skin.</span></span> <span data-ttu-id="5e5f1-155">При выборе цвета, близкого к цвету контейнера обложки, все случайные Пиксели, отображаемые в процессе сглаживания, будут незамеченными.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-155">By choosing a color close to the color of the skin container, any stray pixels that show up in the anti-aliasing process will be unnoticed.</span></span>

<span data-ttu-id="5e5f1-156">Сглаживание — это процесс сглаживания краев наклонных или изогнутых фигур.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-156">Anti-aliasing is the process of smoothing the edges of slanted or curved shapes.</span></span> <span data-ttu-id="5e5f1-157">Сглаживание создает новые цвета для пикселов вдоль краев фигуры, которые являются смесью цвета переднего плана и цвета фона.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-157">Anti-aliasing creates new colors, for pixels along the edges of a shape, that are a blend of the foreground color and the background color.</span></span> <span data-ttu-id="5e5f1-158">Некоторые из этих встроенных цветов могут вызвать пропуск пикселов, когда цвет фона становится прозрачным.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-158">Some of these in-between colors can cause pixels to be missed when the background color is made transparent.</span></span>

<span data-ttu-id="5e5f1-159">Фоновый слой обложки должен выглядеть, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-159">Your skin background layer should look like the following illustration.</span></span>

![фоновый слой обложки](images/g01backg.png)

## <a name="play-and-close-button-layers"></a><span data-ttu-id="5e5f1-161">Слои кнопок "Воспроизвести" и "Закрыть"</span><span class="sxs-lookup"><span data-stu-id="5e5f1-161">Play and Close Button Layers</span></span>

<span data-ttu-id="5e5f1-162">Создайте новый слой и назовите его "Кнопка" Закрыть ".</span><span class="sxs-lookup"><span data-stu-id="5e5f1-162">Create a new layer and name it "Close button".</span></span> <span data-ttu-id="5e5f1-163">Снова с помощью инструмента выделения области Елиптикал создайте окружность и поместите его в левой части общего изображения.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-163">Using the Eliptical Marquee selection tool again, create a circle and position it on the left side of the overall image.</span></span> <span data-ttu-id="5e5f1-164">Включите видимость файла контейнера обложки, чтобы упростить размещение выделенного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-164">Turn on the visibility of the skin container file to help place the selection.</span></span>

<span data-ttu-id="5e5f1-165">Когда вы удовлетворены размещением, заполните выделенный фрагмент любым цветом (за исключением цвета контейнера обложки или фона обложки).</span><span class="sxs-lookup"><span data-stu-id="5e5f1-165">When you are satisfied with the placement, fill the selection with any color (except the color of the skin container or the skin background).</span></span> <span data-ttu-id="5e5f1-166">В этом примере выбран сиреневый цвет.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-166">In this example, a purple color was chosen.</span></span> <span data-ttu-id="5e5f1-167">Вам не нужно запоминать номер цвета.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-167">You do not need to remember the number of the color.</span></span> <span data-ttu-id="5e5f1-168">Затем отмените выбор и примените другой эффект скоса и рельефа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-168">Then cancel the selection and apply another default Bevel and Emboss layer effect.</span></span> <span data-ttu-id="5e5f1-169">Если вы хотите применить к кнопке эффекты, не относящиеся к слою, создайте копию оригинала для последующего использования в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-169">If you want to apply non-layer effects to your button, make a copy of the original for later use in mapping.</span></span>

<span data-ttu-id="5e5f1-170">Кнопка Закрыть должна выглядеть, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-170">Your Close button should look like the following illustration.</span></span>

![кнопка закрытия](images/g01qbut.png)

<span data-ttu-id="5e5f1-172">Создайте новый слой и назовите его "Кнопка воспроизведения".</span><span class="sxs-lookup"><span data-stu-id="5e5f1-172">Create a new layer and name it "Play button".</span></span> <span data-ttu-id="5e5f1-173">Используйте те же методы, что и для кнопки Закрыть, но присвойте ему другой цвет.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-173">Use the same techniques you did for the Close button, but give it a different color.</span></span> <span data-ttu-id="5e5f1-174">В этом случае выбран розовый цвет кнопки, но можно использовать любой цвет, если он не совпадает с цветом контейнера обложки (так как он смешивается с контейнером) или фоновый цвет обложки (так как он станет прозрачным).</span><span class="sxs-lookup"><span data-stu-id="5e5f1-174">In this case, a pink button color was chosen, but any color can be used as long as it is not the same color as the skin container (because it would blend into the container) or the skin background color (because it would become transparent).</span></span>

<span data-ttu-id="5e5f1-175">Кнопка воспроизведения должна выглядеть, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-175">Your Play button should look like the following illustration.</span></span>

![Кнопка "Воспроизвести"](images/g01pbut.png)

## <a name="combine-layers-and-save"></a><span data-ttu-id="5e5f1-177">Объединение слоев и сохранение</span><span class="sxs-lookup"><span data-stu-id="5e5f1-177">Combine Layers and Save</span></span>

<span data-ttu-id="5e5f1-178">Теперь все готово для создания основного файла изображения.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-178">You are now ready to create the primary art file.</span></span> <span data-ttu-id="5e5f1-179">Скрыть все слои и показать только следующие слои в указанном порядке (сверху вниз):</span><span class="sxs-lookup"><span data-stu-id="5e5f1-179">Hide all layers and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="5e5f1-180">Кнопка "Воспроизвести"</span><span class="sxs-lookup"><span data-stu-id="5e5f1-180">Play button</span></span>

<span data-ttu-id="5e5f1-181">Кнопка "Закрыть"</span><span class="sxs-lookup"><span data-stu-id="5e5f1-181">Close button</span></span>

<span data-ttu-id="5e5f1-182">Контейнер обложки</span><span class="sxs-lookup"><span data-stu-id="5e5f1-182">Skin container</span></span>

<span data-ttu-id="5e5f1-183">Фон обложки</span><span class="sxs-lookup"><span data-stu-id="5e5f1-183">Skin background</span></span>

<span data-ttu-id="5e5f1-184">Сохраните в новый файл с помощью команды сохранить копию в меню файл.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-184">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="5e5f1-185">Выберите параметр BMP в части сохранить как диалогового окна Сохранить копию и введите имя файла, который будет ссылаться позже в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-185">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="5e5f1-186">В идеале следует сохранить его в том же каталоге, что и файл определения обложки.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-186">Ideally you should save this in the same directory as your skin definition file.</span></span> <span data-ttu-id="5e5f1-187">Например, можно вызвать этот background.bmp.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-187">For example, you could call this background.bmp.</span></span> <span data-ttu-id="5e5f1-188">Выберите параметры по умолчанию и сохраните файл.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-188">Choose the default settings and save the file.</span></span>

<span data-ttu-id="5e5f1-189">Основной файл изображения должен выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5e5f1-189">Your primary art file should look like this:</span></span>

![основной файл изображения](images/g01prime.png)

<span data-ttu-id="5e5f1-191">Это имя файла будет использоваться как значение атрибута **backgroundImage** элемента **View** в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="5e5f1-191">You will use this file name as the value for the **backgroundImage** attribute of the **VIEW** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e5f1-192">См. также</span><span class="sxs-lookup"><span data-stu-id="5e5f1-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e5f1-193">**Создание первой обложки**</span><span class="sxs-lookup"><span data-stu-id="5e5f1-193">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




