---
description: Показывает, как использовать обработку видео ДКСВА.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: Пример DXVA2_VideoProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342495"
---
# <a name="dxva2_videoproc-sample"></a><span data-ttu-id="adf20-103">\_Пример ВИДЕОПРОК DXVA2</span><span class="sxs-lookup"><span data-stu-id="adf20-103">DXVA2\_VideoProc Sample</span></span>

<span data-ttu-id="adf20-104">Показывает, как использовать [обработку видео дксва](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="adf20-104">Shows how to use [DXVA Video Processing](dxva-video-processing.md).</span></span>

<span data-ttu-id="adf20-105">Этот пример программно создает видео с первичным потоком и подпотоком.</span><span class="sxs-lookup"><span data-stu-id="adf20-105">This sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="adf20-106">Основной поток отображает SMPTE цветовые полосы, а подпоток — полупрозрачный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="adf20-106">The primary stream displays SMPTE color bars, and the substream is a semi-transparent rectangle.</span></span> <span data-ttu-id="adf20-107">Затем видео обрабатывается и отображается с помощью обработчика видео ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="adf20-107">The video is then processed and displayed using a DXVA video processor.</span></span> <span data-ttu-id="adf20-108">Пользователь может изменять плоские значения альфа-канала, исходные и конечные прямоугольники, настройки цветов и цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="adf20-108">The user can change the planar alpha values, source and destination rectangles, color adjustments, and color space.</span></span>

![снимок экрана примера DXVA2 \- видеопрок](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="adf20-110">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="adf20-110">APIs Demonstrated</span></span>

<span data-ttu-id="adf20-111">В этом примере демонстрируются следующие интерфейсы ДКСВА:</span><span class="sxs-lookup"><span data-stu-id="adf20-111">This sample demonstrates the following DXVA interfaces:</span></span>

-   [<span data-ttu-id="adf20-112">**идиректксвидеопроцессорсервице**</span><span class="sxs-lookup"><span data-stu-id="adf20-112">**IDirectXVideoProcessorService**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [<span data-ttu-id="adf20-113">**идиректксвидеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="adf20-113">**IDirectXVideoProcessor**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a><span data-ttu-id="adf20-114">Использование</span><span class="sxs-lookup"><span data-stu-id="adf20-114">Usage</span></span>

<span data-ttu-id="adf20-115">Пример DXVA2 \_ видеопрок создает приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="adf20-115">The DXVA2\_VideoProc sample builds a Windows application.</span></span>

<span data-ttu-id="adf20-116">Параметры командной строки:</span><span class="sxs-lookup"><span data-stu-id="adf20-116">Command line options:</span></span>



| <span data-ttu-id="adf20-117">Параметр</span><span class="sxs-lookup"><span data-stu-id="adf20-117">Option</span></span> | <span data-ttu-id="adf20-118">Описание</span><span class="sxs-lookup"><span data-stu-id="adf20-118">Description</span></span>                                                                          |
|--------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="adf20-119">-чч</span><span class="sxs-lookup"><span data-stu-id="adf20-119">-hh</span></span>    | <span data-ttu-id="adf20-120">Заставляет приложение использовать аппаратное устройство Direct3D и аппаратное устройство ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="adf20-120">Forces the application to use a hardware Direct3D device and a hardware DXVA device.</span></span> |
| <span data-ttu-id="adf20-121">-HS</span><span class="sxs-lookup"><span data-stu-id="adf20-121">-hs</span></span>    | <span data-ttu-id="adf20-122">Заставляет приложение использовать аппаратное устройство Direct3D и программное ДКСВА устройство.</span><span class="sxs-lookup"><span data-stu-id="adf20-122">Forces the application to use a hardware Direct3D device and a software DXVA device.</span></span> |
| <span data-ttu-id="adf20-123">-ss</span><span class="sxs-lookup"><span data-stu-id="adf20-123">-ss</span></span>    | <span data-ttu-id="adf20-124">Заставляет приложение использовать программное устройство Direct3D и программное ДКСВА устройство.</span><span class="sxs-lookup"><span data-stu-id="adf20-124">Forces the application to use a software Direct3D device and a software DXVA device.</span></span> |



 

<span data-ttu-id="adf20-125">Команды клавиатуры:</span><span class="sxs-lookup"><span data-stu-id="adf20-125">Keyboard commands:</span></span>



| <span data-ttu-id="adf20-126">Ключ</span><span class="sxs-lookup"><span data-stu-id="adf20-126">Key</span></span>       | <span data-ttu-id="adf20-127">Описание</span><span class="sxs-lookup"><span data-stu-id="adf20-127">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="adf20-128">ALT+ВВОД</span><span class="sxs-lookup"><span data-stu-id="adf20-128">ALT+ENTER</span></span> | <span data-ttu-id="adf20-129">Переключение между оконным режимом и полноэкранным режимом.</span><span class="sxs-lookup"><span data-stu-id="adf20-129">Switch between windowed mode and full-screen mode.</span></span>      |
| <span data-ttu-id="adf20-130">F1 — F8</span><span class="sxs-lookup"><span data-stu-id="adf20-130">F1–F8</span></span>     | <span data-ttu-id="adf20-131">Введите один из режимов, показанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="adf20-131">Enter one of the modes shown in the following table.</span></span>    |
| <span data-ttu-id="adf20-132">END</span><span class="sxs-lookup"><span data-stu-id="adf20-132">END</span></span>       | <span data-ttu-id="adf20-133">Включение или отключение ведения журнала отладки для удаленных кадров.</span><span class="sxs-lookup"><span data-stu-id="adf20-133">Enable or disable debugging logging for dropped frames.</span></span> |
| <span data-ttu-id="adf20-134">HOME</span><span class="sxs-lookup"><span data-stu-id="adf20-134">HOME</span></span>      | <span data-ttu-id="adf20-135">Сбросьте параметр в исходное значение.</span><span class="sxs-lookup"><span data-stu-id="adf20-135">Reset a parameter to its initial value.</span></span>                 |



 

<span data-ttu-id="adf20-136">Каждая функция клавиш F1 по F8 переключается в режим, в котором клавиши со стрелками используются для корректировки конкретного параметра отрисовки.</span><span class="sxs-lookup"><span data-stu-id="adf20-136">Each of the function keys F1 through F8 switches to a mode in which the arrow keys can be used to adjust a particular rendering parameter.</span></span> <span data-ttu-id="adf20-137">Кроме того, изменяется цвет подпотока.</span><span class="sxs-lookup"><span data-stu-id="adf20-137">In addition, the color of the substream changes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adf20-138">Ключ</span><span class="sxs-lookup"><span data-stu-id="adf20-138">Key</span></span></th>
<th><span data-ttu-id="adf20-139">Описание</span><span class="sxs-lookup"><span data-stu-id="adf20-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="adf20-140">F1</span><span class="sxs-lookup"><span data-stu-id="adf20-140">F1</span></span></td>
<td><span data-ttu-id="adf20-141">Настройте альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="adf20-141">Adjust the alpha values.</span></span><br/>
<ul>
<li><span data-ttu-id="adf20-142">ВВЕРХ: Увеличьте плоскую альфа-составляющую обоих потоков.</span><span class="sxs-lookup"><span data-stu-id="adf20-142">UP: Increase the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="adf20-143">ВНИЗ: уменьшение плоской альфа-составляющей обоих потоков.</span><span class="sxs-lookup"><span data-stu-id="adf20-143">DOWN: Decrease the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="adf20-144">RIGHT: увеличение пиксельного альфа-канала подпотока.</span><span class="sxs-lookup"><span data-stu-id="adf20-144">RIGHT: Increase the pixel alpha of the substream.</span></span></li>
<li><span data-ttu-id="adf20-145">LEFT: уменьшение пиксельного альфа-канала подпотока.</span><span class="sxs-lookup"><span data-stu-id="adf20-145">LEFT: Decrease the pixel alpha of the substream.</span></span></li>
</ul>
<span data-ttu-id="adf20-146">Цвет подпотока: белый</span><span class="sxs-lookup"><span data-stu-id="adf20-146">Substream color: White</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf20-147">F2</span><span class="sxs-lookup"><span data-stu-id="adf20-147">F2</span></span></td>
<td><span data-ttu-id="adf20-148">Настройте исходную область источника (масштаб) основного потока.</span><span class="sxs-lookup"><span data-stu-id="adf20-148">Adjust the primary stream's source area (zoom).</span></span><br/>
<ul>
<li><span data-ttu-id="adf20-149">ВВЕРХ: увеличение по вертикали (увеличение).</span><span class="sxs-lookup"><span data-stu-id="adf20-149">UP: Increase vertically (zoom in).</span></span></li>
<li><span data-ttu-id="adf20-150">ВНИЗ: уменьшить по вертикали (уменьшить).</span><span class="sxs-lookup"><span data-stu-id="adf20-150">DOWN: Decrease vertically (zoom out).</span></span></li>
<li><span data-ttu-id="adf20-151">СПРАВА: увеличение по горизонтали (увеличение).</span><span class="sxs-lookup"><span data-stu-id="adf20-151">RIGHT: Increase horizontally (zoom in).</span></span></li>
<li><span data-ttu-id="adf20-152">LEFT: уменьшить по горизонтали (уменьшить масштаб).</span><span class="sxs-lookup"><span data-stu-id="adf20-152">LEFT: Decrease horizontally (zoom out).</span></span></li>
</ul>
<span data-ttu-id="adf20-153">Цвет подпотока: красный</span><span class="sxs-lookup"><span data-stu-id="adf20-153">Substream color: Red</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adf20-154">F3</span><span class="sxs-lookup"><span data-stu-id="adf20-154">F3</span></span></td>
<td><span data-ttu-id="adf20-155">Переместите исходную область источника первичного потока.</span><span class="sxs-lookup"><span data-stu-id="adf20-155">Move the primary stream's source area.</span></span><br/>
<ul>
<li><span data-ttu-id="adf20-156">ВВЕРХ: переместить вверх.</span><span class="sxs-lookup"><span data-stu-id="adf20-156">UP: Move up.</span></span></li>
<li><span data-ttu-id="adf20-157">ВНИЗ: вниз.</span><span class="sxs-lookup"><span data-stu-id="adf20-157">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="adf20-158">СПРАВА: переместить вправо.</span><span class="sxs-lookup"><span data-stu-id="adf20-158">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="adf20-159">СЛЕВА: переместить влево.</span><span class="sxs-lookup"><span data-stu-id="adf20-159">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="adf20-160">Цвет подпотока: желтый</span><span class="sxs-lookup"><span data-stu-id="adf20-160">Substream color: Yellow</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf20-161">F4</span><span class="sxs-lookup"><span data-stu-id="adf20-161">F4</span></span></td>
<td><span data-ttu-id="adf20-162">Настройте область назначения основного потока.</span><span class="sxs-lookup"><span data-stu-id="adf20-162">Adjust the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="adf20-163">ВВЕРХ: увеличение по вертикали.</span><span class="sxs-lookup"><span data-stu-id="adf20-163">UP: Increase vertically.</span></span></li>
<li><span data-ttu-id="adf20-164">ВНИЗ: уменьшить по вертикали.</span><span class="sxs-lookup"><span data-stu-id="adf20-164">DOWN: Decrease vertically.</span></span></li>
<li><span data-ttu-id="adf20-165">СПРАВА: увеличить по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="adf20-165">RIGHT: Increase horizontally.</span></span></li>
<li><span data-ttu-id="adf20-166">LEFT: уменьшить по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="adf20-166">LEFT: Decrease horizontally.</span></span></li>
</ul>
<span data-ttu-id="adf20-167">Цвет подпотока: зеленый</span><span class="sxs-lookup"><span data-stu-id="adf20-167">Substream color: Green</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adf20-168">F5</span><span class="sxs-lookup"><span data-stu-id="adf20-168">F5</span></span></td>
<td><span data-ttu-id="adf20-169">Переместите область назначения основного потока.</span><span class="sxs-lookup"><span data-stu-id="adf20-169">Move the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="adf20-170">ВВЕРХ: переместить вверх.</span><span class="sxs-lookup"><span data-stu-id="adf20-170">UP: Move up.</span></span></li>
<li><span data-ttu-id="adf20-171">ВНИЗ: вниз.</span><span class="sxs-lookup"><span data-stu-id="adf20-171">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="adf20-172">СПРАВА: переместить вправо.</span><span class="sxs-lookup"><span data-stu-id="adf20-172">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="adf20-173">СЛЕВА: переместить влево.</span><span class="sxs-lookup"><span data-stu-id="adf20-173">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="adf20-174">Цвет подпотока: голубой</span><span class="sxs-lookup"><span data-stu-id="adf20-174">Substream color: Cyan</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf20-175">F6</span><span class="sxs-lookup"><span data-stu-id="adf20-175">F6</span></span></td>
<td><span data-ttu-id="adf20-176">Изменение цвета фона или цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="adf20-176">Change background color or color space.</span></span><br/>
<ul>
<li><span data-ttu-id="adf20-177">ВВЕРХ, вниз: циклический перебор цветовых пространств.</span><span class="sxs-lookup"><span data-stu-id="adf20-177">UP, DOWN: Cycle through color spaces.</span></span></li>
<li><span data-ttu-id="adf20-178">СПРАВА, слева: перебор цветов фона.</span><span class="sxs-lookup"><span data-stu-id="adf20-178">RIGHT, LEFT: Cycle through background colors.</span></span></li>
</ul>
<span data-ttu-id="adf20-179">Цвет подпотока: синий</span><span class="sxs-lookup"><span data-stu-id="adf20-179">Substream color: Blue</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="adf20-180">F7</span><span class="sxs-lookup"><span data-stu-id="adf20-180">F7</span></span></td>
<td><span data-ttu-id="adf20-181">Настройка яркости и контрастности.</span><span class="sxs-lookup"><span data-stu-id="adf20-181">Adjust brightness and contrast.</span></span><br/>
<ul>
<li><span data-ttu-id="adf20-182">ВВЕРХ: увеличение яркости.</span><span class="sxs-lookup"><span data-stu-id="adf20-182">UP: Increase brightness.</span></span></li>
<li><span data-ttu-id="adf20-183">ВНИЗ: уменьшение яркости.</span><span class="sxs-lookup"><span data-stu-id="adf20-183">DOWN: Decrease brightness.</span></span></li>
<li><span data-ttu-id="adf20-184">RIGHT: повышение контрастности.</span><span class="sxs-lookup"><span data-stu-id="adf20-184">RIGHT: Increase contrast.</span></span></li>
<li><span data-ttu-id="adf20-185">LEFT: уменьшить контрастность.</span><span class="sxs-lookup"><span data-stu-id="adf20-185">LEFT: Decrease contrast.</span></span></li>
</ul>
<span data-ttu-id="adf20-186">Цвет подпотока: пурпурный</span><span class="sxs-lookup"><span data-stu-id="adf20-186">Substream color: Magenta</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="adf20-187">F8</span><span class="sxs-lookup"><span data-stu-id="adf20-187">F8</span></span></td>
<td><span data-ttu-id="adf20-188">Настройка оттенка и насыщенности.</span><span class="sxs-lookup"><span data-stu-id="adf20-188">Adjust hue and saturation.</span></span><br/>
<ul>
<li><span data-ttu-id="adf20-189">ВВЕРХ: увеличить оттенок.</span><span class="sxs-lookup"><span data-stu-id="adf20-189">UP: Increase hue.</span></span></li>
<li><span data-ttu-id="adf20-190">ВНИЗ: уменьшить оттенок.</span><span class="sxs-lookup"><span data-stu-id="adf20-190">DOWN: Decrease hue.</span></span></li>
<li><span data-ttu-id="adf20-191">RIGHT: увеличение насыщенности.</span><span class="sxs-lookup"><span data-stu-id="adf20-191">RIGHT: Increase saturation.</span></span></li>
<li><span data-ttu-id="adf20-192">LEFT: уменьшение насыщенности.</span><span class="sxs-lookup"><span data-stu-id="adf20-192">LEFT: Decrease saturation.</span></span></li>
</ul>
<span data-ttu-id="adf20-193">Цвет подпотока: черный</span><span class="sxs-lookup"><span data-stu-id="adf20-193">Substream color: Black</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="adf20-194">В каждом режиме нажатие клавиши HOME приводит к сбросу параметров для этого режима до исходных значений.</span><span class="sxs-lookup"><span data-stu-id="adf20-194">In each mode, pressing the HOME key resets the parameters for that mode to their initial values.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf20-195">Требования</span><span class="sxs-lookup"><span data-stu-id="adf20-195">Requirements</span></span>



| <span data-ttu-id="adf20-196">Продукт</span><span class="sxs-lookup"><span data-stu-id="adf20-196">Product</span></span>                                                        | <span data-ttu-id="adf20-197">Version</span><span class="sxs-lookup"><span data-stu-id="adf20-197">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="adf20-198">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="adf20-198">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="adf20-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="adf20-199">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="adf20-200">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="adf20-200">Downloading the Sample</span></span>

<span data-ttu-id="adf20-201">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span><span class="sxs-lookup"><span data-stu-id="adf20-201">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span></span>

## <a name="related-topics"></a><span data-ttu-id="adf20-202">См. также</span><span class="sxs-lookup"><span data-stu-id="adf20-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf20-203">Ускорение видео DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="adf20-203">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="adf20-204">Обработка видео ДКСВА</span><span class="sxs-lookup"><span data-stu-id="adf20-204">DXVA Video Processing</span></span>](dxva-video-processing.md)
</dt> <dt>

[<span data-ttu-id="adf20-205">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="adf20-205">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




