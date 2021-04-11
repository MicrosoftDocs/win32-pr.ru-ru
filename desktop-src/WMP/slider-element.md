---
title: Элемент SLIDER
description: Элемент SLIDER
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Обложки проигрывателя Windows Media, элемент SLIDER
- обложки, элемент SLIDER
- Элемент SLIDER
- Справочник по обложкам, элементу SLIDER
- элементы, ПОЛЗУНок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34607c8706fccc8f416ebc83ae483c98a784c08b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330539"
---
# <a name="slider-element"></a><span data-ttu-id="71cb3-108">Элемент SLIDER</span><span class="sxs-lookup"><span data-stu-id="71cb3-108">SLIDER Element</span></span>

<span data-ttu-id="71cb3-109">Элемент **Slider** предоставляет способ создания и управления простым горизонтальным или вертикальным ползунком.</span><span class="sxs-lookup"><span data-stu-id="71cb3-109">The **SLIDER** element provides a way to create and manipulate a simple horizontal or vertical slider control.</span></span> <span data-ttu-id="71cb3-110">Он поддерживает следующие атрибуты и обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="71cb3-110">It supports the following attributes and event handlers.</span></span> <span data-ttu-id="71cb3-111">Для удобства также предоставляются предопределенные элементы **Slider** .</span><span class="sxs-lookup"><span data-stu-id="71cb3-111">Predefined **SLIDER** elements are also provided for convenience.</span></span>

<span data-ttu-id="71cb3-112">Элемент **Slider** поддерживает следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="71cb3-112">The **SLIDER** element supports the following attributes.</span></span>



| <span data-ttu-id="71cb3-113">attribute</span><span class="sxs-lookup"><span data-stu-id="71cb3-113">Attribute</span></span>                                                 | <span data-ttu-id="71cb3-114">Описание</span><span class="sxs-lookup"><span data-stu-id="71cb3-114">Description</span></span>                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71cb3-115">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="71cb3-115">backgroundColor</span></span>](slider-backgroundcolor.md)             | <span data-ttu-id="71cb3-116">Указывает или получает цвет фона элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="71cb3-116">Specifies or retrieves the background color of the slider control.</span></span>                                                |
| [<span data-ttu-id="71cb3-117">баккграундендколор</span><span class="sxs-lookup"><span data-stu-id="71cb3-117">backgroundEndColor</span></span>](slider-backgroundendcolor.md)       | <span data-ttu-id="71cb3-118">Указывает или получает конечный цвет фона элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="71cb3-118">Specifies or retrieves the background ending color of the slider control.</span></span>                                         |
| [<span data-ttu-id="71cb3-119">баккграундховеримаже</span><span class="sxs-lookup"><span data-stu-id="71cb3-119">backgroundHoverImage</span></span>](slider-backgroundhoverimage.md)   | <span data-ttu-id="71cb3-120">Указывает или получает фоновое изображение ползунка, отображаемого при наведении на него указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="71cb3-120">Specifies or retrieves the background image of the slider that appears when hovering over it with the mouse.</span></span>      |
| [<span data-ttu-id="71cb3-121">backgroundImage</span><span class="sxs-lookup"><span data-stu-id="71cb3-121">backgroundImage</span></span>](slider-backgroundimage.md)             | <span data-ttu-id="71cb3-122">Указывает или получает фоновое изображение по умолчанию для ползунка.</span><span class="sxs-lookup"><span data-stu-id="71cb3-122">Specifies or retrieves the default background image of the slider.</span></span>                                                |
| [<span data-ttu-id="71cb3-123">бордерсизе</span><span class="sxs-lookup"><span data-stu-id="71cb3-123">borderSize</span></span>](slider-bordersize.md)                       | <span data-ttu-id="71cb3-124">Указывает или получает размер границы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="71cb3-124">Specifies or retrieves the border size in pixels.</span></span>                                                                 |
| [<span data-ttu-id="71cb3-125">курсор</span><span class="sxs-lookup"><span data-stu-id="71cb3-125">cursor</span></span>](slider-cursor.md)                               | <span data-ttu-id="71cb3-126">Указывает или получает значение, указывающее, какой тип курсора отображается при наведении мыши на ползунок.</span><span class="sxs-lookup"><span data-stu-id="71cb3-126">Specifies or retrieves a value indicating which type of cursor appears when the mouse is over the slider control.</span></span> |
| [<span data-ttu-id="71cb3-127">direction</span><span class="sxs-lookup"><span data-stu-id="71cb3-127">direction</span></span>](slider-direction.md)                         | <span data-ttu-id="71cb3-128">Указывает или получает направление, в котором размещаются изображения ползунка.</span><span class="sxs-lookup"><span data-stu-id="71cb3-128">Specifies or retrieves the direction that slider images are laid out.</span></span>                                             |
| [<span data-ttu-id="71cb3-129">дисабледколор</span><span class="sxs-lookup"><span data-stu-id="71cb3-129">disabledColor</span></span>](slider-disabledcolor.md)                 | <span data-ttu-id="71cb3-130">Указывает или получает отключенный цвет элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="71cb3-130">Specifies or retrieves the disabled color of the slider control.</span></span>                                                  |
| [<span data-ttu-id="71cb3-131">дисабледимаже</span><span class="sxs-lookup"><span data-stu-id="71cb3-131">disabledImage</span></span>](slider-disabledimage.md)                 | <span data-ttu-id="71cb3-132">Указывает или получает изображение ползунка, отображаемого при отключенном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="71cb3-132">Specifies or retrieves the image of the slider that appears when the control is disabled.</span></span>                         |
| [<span data-ttu-id="71cb3-133">foregroundColor</span><span class="sxs-lookup"><span data-stu-id="71cb3-133">foregroundColor</span></span>](slider-foregroundcolor.md)             | <span data-ttu-id="71cb3-134">Указывает или получает цвет переднего плана для элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="71cb3-134">Specifies or retrieves the foreground color of the slider control.</span></span>                                                |
| [<span data-ttu-id="71cb3-135">фореграундендколор</span><span class="sxs-lookup"><span data-stu-id="71cb3-135">foregroundEndColor</span></span>](slider-foregroundendcolor.md)       | <span data-ttu-id="71cb3-136">Указывает или получает конечный цвет переднего плана для элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="71cb3-136">Specifies or retrieves the foreground ending color of the slider control.</span></span>                                         |
| [<span data-ttu-id="71cb3-137">фореграундховеримаже</span><span class="sxs-lookup"><span data-stu-id="71cb3-137">foregroundHoverImage</span></span>](slider-foregroundhoverimage.md)   | <span data-ttu-id="71cb3-138">Указывает или получает фоновое изображение ползунка, отображаемого при наведении на него указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="71cb3-138">Specifies or retrieves the foreground image of the slider that appears when hovering over it with the mouse.</span></span>      |
| [<span data-ttu-id="71cb3-139">фореграундимаже</span><span class="sxs-lookup"><span data-stu-id="71cb3-139">foregroundImage</span></span>](slider-foregroundimage.md)             | <span data-ttu-id="71cb3-140">Указывает или получает изображение переднего плана по умолчанию для ползунка.</span><span class="sxs-lookup"><span data-stu-id="71cb3-140">Specifies or retrieves the default foreground image of the slider.</span></span>                                                |
| [<span data-ttu-id="71cb3-141">фореграундпрогресс</span><span class="sxs-lookup"><span data-stu-id="71cb3-141">foregroundProgress</span></span>](slider-foregroundprogress.md)       | <span data-ttu-id="71cb3-142">Указывает или получает текущую положение индикатора выполнения переднего плана в процентах от области ползунка.</span><span class="sxs-lookup"><span data-stu-id="71cb3-142">Specifies or retrieves the current position of the foreground progress bar as a percentage of the slider area.</span></span>    |
| [<span data-ttu-id="71cb3-143">max</span><span class="sxs-lookup"><span data-stu-id="71cb3-143">max</span></span>](slider-max.md)                                     | <span data-ttu-id="71cb3-144">Указывает или получает максимальное значение диапазона, определенного элементом управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="71cb3-144">Specifies or retrieves the maximum value of the range defined by the slider control.</span></span>                              |
| [<span data-ttu-id="71cb3-145">min</span><span class="sxs-lookup"><span data-stu-id="71cb3-145">min</span></span>](slider-min.md)                                     | <span data-ttu-id="71cb3-146">Указывает или получает минимальное значение диапазона, определенного элементом управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="71cb3-146">Specifies or retrieves the minimum value of the range defined by the slider control.</span></span>                              |
| [<span data-ttu-id="71cb3-147">слайд</span><span class="sxs-lookup"><span data-stu-id="71cb3-147">slide</span></span>](slider-slide.md)                                 | <span data-ttu-id="71cb3-148">Указывает или получает значение, указывающее, будет ли изображение переднего плана поверх фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="71cb3-148">Specifies or retrieves a value indicating whether the foreground image slides over the background image.</span></span>          |
| [<span data-ttu-id="71cb3-149">сумбдисабледимаже</span><span class="sxs-lookup"><span data-stu-id="71cb3-149">thumbDisabledImage</span></span>](slider-thumbdisabledimage.md)       | <span data-ttu-id="71cb3-150">Указывает или получает отключенное изображение бегунка элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="71cb3-150">Specifies or retrieves the disabled thumb image of the slider control.</span></span>                                            |
| [<span data-ttu-id="71cb3-151">сумбдовнимаже</span><span class="sxs-lookup"><span data-stu-id="71cb3-151">thumbDownImage</span></span>](slider-thumbdownimage.md)               | <span data-ttu-id="71cb3-152">Указывает или получает изображение, представляющее состояние бегунка.</span><span class="sxs-lookup"><span data-stu-id="71cb3-152">Specifies or retrieves the image representing the down state of the thumb.</span></span>                                        |
| [<span data-ttu-id="71cb3-153">сумбховеримаже</span><span class="sxs-lookup"><span data-stu-id="71cb3-153">thumbHoverImage</span></span>](slider-thumbhoverimage.md)             | <span data-ttu-id="71cb3-154">Указывает или получает изображение бегунка, которое появляется при наведении на него указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="71cb3-154">Specifies or retrieves the image of the thumb that appears when hovering over it with the mouse.</span></span>                  |
| [<span data-ttu-id="71cb3-155">сумбимаже</span><span class="sxs-lookup"><span data-stu-id="71cb3-155">thumbImage</span></span>](slider-thumbimage.md)                       | <span data-ttu-id="71cb3-156">Указывает или получает изображение, которое будет использоваться для представления текущей положения ползунка.</span><span class="sxs-lookup"><span data-stu-id="71cb3-156">Specifies or retrieves the image that will be used to represent the current position of the slider.</span></span>               |
| [<span data-ttu-id="71cb3-157">крытия</span><span class="sxs-lookup"><span data-stu-id="71cb3-157">tiled</span></span>](slider-tiled.md)                                 | <span data-ttu-id="71cb3-158">Указывает или получает значение, указывающее, будут ли изображения на ползунке перемещаться по мозаике.</span><span class="sxs-lookup"><span data-stu-id="71cb3-158">Specifies or retrieves a value indicating whether the slider images will be tiled.</span></span>                                |
| [<span data-ttu-id="71cb3-159">Сказок</span><span class="sxs-lookup"><span data-stu-id="71cb3-159">toolTip</span></span>](slider-tooltip.md)                             | <span data-ttu-id="71cb3-160">Указывает или получает текст подсказки для элемента управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="71cb3-160">Specifies or retrieves the ToolTip text for the slider control.</span></span>                                                   |
| [<span data-ttu-id="71cb3-161">транспаренциколор</span><span class="sxs-lookup"><span data-stu-id="71cb3-161">transparencyColor</span></span>](slider-transparencycolor.md)         | <span data-ttu-id="71cb3-162">Указывает или получает прозрачный цвет изображений ползунка.</span><span class="sxs-lookup"><span data-stu-id="71cb3-162">Specifies or retrieves the transparent color of the slider images.</span></span>                                                |
| [<span data-ttu-id="71cb3-163">усефореграундпрогресс</span><span class="sxs-lookup"><span data-stu-id="71cb3-163">useForegroundProgress</span></span>](slider-useforegroundprogress.md) | <span data-ttu-id="71cb3-164">Указывает или получает значение, указывающее, будет ли использоваться основной индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="71cb3-164">Specifies or retrieves a value indicating whether the foreground progress bar will be used.</span></span>                       |
| [<span data-ttu-id="71cb3-165">value</span><span class="sxs-lookup"><span data-stu-id="71cb3-165">value</span></span>](slider-value.md)                                 | <span data-ttu-id="71cb3-166">Указывает и получает текущую положение ползунка.</span><span class="sxs-lookup"><span data-stu-id="71cb3-166">Specifies and retrieves the current position of the slider.</span></span>                                                       |



 

<span data-ttu-id="71cb3-167">Элемент **Slider** может реализовывать следующие обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="71cb3-167">The **SLIDER** element can implement the following event handlers.</span></span>



| <span data-ttu-id="71cb3-168">Обработчик событий</span><span class="sxs-lookup"><span data-stu-id="71cb3-168">Event handler</span></span>                                   | <span data-ttu-id="71cb3-169">Описание</span><span class="sxs-lookup"><span data-stu-id="71cb3-169">Description</span></span>                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71cb3-170">ондрагбегин</span><span class="sxs-lookup"><span data-stu-id="71cb3-170">onDragBegin</span></span>](slider-ondragbegin.md)           | <span data-ttu-id="71cb3-171">Обрабатывает событие, возникающее, когда пользователь нажимает и удерживает левую кнопку мыши вниз и начинает перетаскивание мышью.</span><span class="sxs-lookup"><span data-stu-id="71cb3-171">Handles an event that occurs when the user clicks and holds the left mouse button down and begins to drag the mouse.</span></span> |
| [<span data-ttu-id="71cb3-172">ондраженд</span><span class="sxs-lookup"><span data-stu-id="71cb3-172">onDragEnd</span></span>](slider-ondragend.md)               | <span data-ttu-id="71cb3-173">Обрабатывает событие, возникающее при отпускании левой кнопки мыши после операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="71cb3-173">Handles an event that occurs when the left mouse button is released after a dragging operation.</span></span>                      |
| [<span data-ttu-id="71cb3-174">онпоситиончанже</span><span class="sxs-lookup"><span data-stu-id="71cb3-174">onPositionChange</span></span>](slider-onpositionchange.md) | <span data-ttu-id="71cb3-175">Обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем.</span><span class="sxs-lookup"><span data-stu-id="71cb3-175">Handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>   |



 

<span data-ttu-id="71cb3-176">Элемент **Slider** поддерживает атрибуты окружения и может реализовывать обработчики событий окружения.</span><span class="sxs-lookup"><span data-stu-id="71cb3-176">The **SLIDER** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="71cb3-177">Дополнительные сведения см. в разделе [атрибуты окружения](ambient-attributes.md) и [обработчики событий окружения](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="71cb3-177">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

<span data-ttu-id="71cb3-178">Стандартные ползунки являются обычными элементами **Slider** с различными параметрами общих атрибутов, заданными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71cb3-178">Predefined sliders are normal **SLIDER** elements with various common attribute settings specified by default.</span></span> <span data-ttu-id="71cb3-179">Доступны следующие стандартные ползунки.</span><span class="sxs-lookup"><span data-stu-id="71cb3-179">The following predefined sliders are available.</span></span>



| <span data-ttu-id="71cb3-180">Предопределенный ПОЛЗУНок</span><span class="sxs-lookup"><span data-stu-id="71cb3-180">Predefined SLIDER</span></span>                  | <span data-ttu-id="71cb3-181">Описание</span><span class="sxs-lookup"><span data-stu-id="71cb3-181">Description</span></span>                                                    |
|------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="71cb3-182">баланцеслидер</span><span class="sxs-lookup"><span data-stu-id="71cb3-182">BALANCESLIDER</span></span>](balanceslider.md) | <span data-ttu-id="71cb3-183">**Ползунок** , используемый для настройки баланса звука.</span><span class="sxs-lookup"><span data-stu-id="71cb3-183">A **SLIDER** used to set audio balance.</span></span>                        |
| [<span data-ttu-id="71cb3-184">сикслидер</span><span class="sxs-lookup"><span data-stu-id="71cb3-184">SEEKSLIDER</span></span>](seekslider.md)       | <span data-ttu-id="71cb3-185">**Ползунок** , используемый для поиска любой позицией в файле мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="71cb3-185">A **SLIDER** used to seek to any position within a media file.</span></span> |
| [<span data-ttu-id="71cb3-186">волумеслидер</span><span class="sxs-lookup"><span data-stu-id="71cb3-186">VOLUMESLIDER</span></span>](volumeslider.md)   | <span data-ttu-id="71cb3-187">**Ползунок** , используемый для настройки громкости звука.</span><span class="sxs-lookup"><span data-stu-id="71cb3-187">A **SLIDER** used to set audio volume.</span></span>                         |



 

## <a name="related-topics"></a><span data-ttu-id="71cb3-188">См. также</span><span class="sxs-lookup"><span data-stu-id="71cb3-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71cb3-189">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="71cb3-189">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




