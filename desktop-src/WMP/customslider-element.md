---
title: КУСТОМСЛИДЕР, элемент
description: КУСТОМСЛИДЕР, элемент
ms.assetid: 9cba9bdd-ea5b-4a4a-a61e-e6aff29fc3e0
keywords:
- Обложки проигрывателя Windows Media, элемент КУСТОМСЛИДЕР
- обложки, элемент КУСТОМСЛИДЕР
- КУСТОМСЛИДЕР, элемент
- Справочник по обложкам, элементу КУСТОМСЛИДЕР
- элементы, КУСТОМСЛИДЕР
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f49fc6260df295e3266ae9ddf7b5b3eceee43d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330875"
---
# <a name="customslider-element"></a><span data-ttu-id="71643-108">КУСТОМСЛИДЕР, элемент</span><span class="sxs-lookup"><span data-stu-id="71643-108">CUSTOMSLIDER Element</span></span>

<span data-ttu-id="71643-109">Элемент **кустомслидер** предоставляет способ создания и управления ползунком любой фигуры, например круговой шкалы.</span><span class="sxs-lookup"><span data-stu-id="71643-109">The **CUSTOMSLIDER** element provides a way to create and manipulate a slider control of any shape, such as a circular knob.</span></span> <span data-ttu-id="71643-110">В следующих таблицах перечислены атрибуты и обработчики событий, поддерживаемые этим элементом.</span><span class="sxs-lookup"><span data-stu-id="71643-110">The following tables list the attributes and event handlers supported by this element.</span></span>

<span data-ttu-id="71643-111">Элемент **кустомслидер** поддерживает следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="71643-111">The **CUSTOMSLIDER** element supports the following attributes.</span></span>



| <span data-ttu-id="71643-112">attribute</span><span class="sxs-lookup"><span data-stu-id="71643-112">Attribute</span></span>                                               | <span data-ttu-id="71643-113">Описание</span><span class="sxs-lookup"><span data-stu-id="71643-113">Description</span></span>                                                                                                                 |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71643-114">курсор</span><span class="sxs-lookup"><span data-stu-id="71643-114">cursor</span></span>](customslider-cursor.md)                       | <span data-ttu-id="71643-115">Указывает или получает значение элемента управления "ползунок", которое появляется при наведении указателя мыши на ползунок.</span><span class="sxs-lookup"><span data-stu-id="71643-115">Specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>               |
| [<span data-ttu-id="71643-116">дисабледимаже</span><span class="sxs-lookup"><span data-stu-id="71643-116">disabledImage</span></span>](customslider-disabledimage.md)         | <span data-ttu-id="71643-117">Указывает или получает изображение ползунка, используемого при отключенном ползунке.</span><span class="sxs-lookup"><span data-stu-id="71643-117">Specifies or retrieves the image of the slider used when the slider is disabled.</span></span>                                            |
| [<span data-ttu-id="71643-118">довнимаже</span><span class="sxs-lookup"><span data-stu-id="71643-118">downImage</span></span>](customslider-downimage.md)                 | <span data-ttu-id="71643-119">Указывает или получает изображение состояния "вниз" настраиваемого ползунка.</span><span class="sxs-lookup"><span data-stu-id="71643-119">Specifies or retrieves the down state image of the custom slider.</span></span>                                                           |
| [<span data-ttu-id="71643-120">ховеримаже</span><span class="sxs-lookup"><span data-stu-id="71643-120">hoverImage</span></span>](customslider-hoverimage.md)               | <span data-ttu-id="71643-121">Указывает или получает изображение, отображаемое при наведении мыши на пользовательский ползунок.</span><span class="sxs-lookup"><span data-stu-id="71643-121">Specifies or retrieves the image that displays when the mouse is over the custom slider.</span></span>                                    |
| [<span data-ttu-id="71643-122">image</span><span class="sxs-lookup"><span data-stu-id="71643-122">image</span></span>](customslider-image.md)                         | <span data-ttu-id="71643-123">Указывает или получает имя файла, содержащего изображения, соответствующие различным состояниям настраиваемого ползунка.</span><span class="sxs-lookup"><span data-stu-id="71643-123">Specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span> |
| [<span data-ttu-id="71643-124">max</span><span class="sxs-lookup"><span data-stu-id="71643-124">max</span></span>](customslider-max.md)                             | <span data-ttu-id="71643-125">Указывает или получает максимальное значение диапазона, определенного настраиваемым ползунком.</span><span class="sxs-lookup"><span data-stu-id="71643-125">Specifies or retrieves the maximum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="71643-126">min</span><span class="sxs-lookup"><span data-stu-id="71643-126">min</span></span>](customslider-min.md)                             | <span data-ttu-id="71643-127">Указывает или получает минимальное значение диапазона, определенного настраиваемым ползунком.</span><span class="sxs-lookup"><span data-stu-id="71643-127">Specifies or retrieves the minimum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="71643-128">поситионимаже</span><span class="sxs-lookup"><span data-stu-id="71643-128">positionImage</span></span>](customslider-positionimage.md)         | <span data-ttu-id="71643-129">Указывает или получает карту изображения, используемую для определения размещения изображения из отображаемого файла **изображения** .</span><span class="sxs-lookup"><span data-stu-id="71643-129">Specifies or retrieves the image map used to determine which position image from the **image** file to display.</span></span>             |
| [<span data-ttu-id="71643-130">Сказок</span><span class="sxs-lookup"><span data-stu-id="71643-130">toolTip</span></span>](customslider-tooltip.md)                     | <span data-ttu-id="71643-131">Указывает или получает текст подсказки для ползунка.</span><span class="sxs-lookup"><span data-stu-id="71643-131">Specifies or retrieves the ToolTip text for the slider.</span></span>                                                                     |
| [<span data-ttu-id="71643-132">транспаренциколор</span><span class="sxs-lookup"><span data-stu-id="71643-132">transparencyColor</span></span>](customslider-transparencycolor.md) | <span data-ttu-id="71643-133">Указывает или получает цвет прозрачности настраиваемых изображений ползунка.</span><span class="sxs-lookup"><span data-stu-id="71643-133">Specifies or retrieves the transparency color of the custom slider images.</span></span>                                                  |
| [<span data-ttu-id="71643-134">value</span><span class="sxs-lookup"><span data-stu-id="71643-134">value</span></span>](customslider-value.md)                         | <span data-ttu-id="71643-135">Указывает или получает текущую положение ползунка.</span><span class="sxs-lookup"><span data-stu-id="71643-135">Specifies or retrieves the current position of the slider.</span></span>                                                                  |



 

<span data-ttu-id="71643-136">Элемент **кустомслидер** может реализовывать следующие обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="71643-136">The **CUSTOMSLIDER** element can implement the following event handlers.</span></span>



| <span data-ttu-id="71643-137">Обработчик событий</span><span class="sxs-lookup"><span data-stu-id="71643-137">Event handler</span></span>                                         | <span data-ttu-id="71643-138">Описание</span><span class="sxs-lookup"><span data-stu-id="71643-138">Description</span></span>                                                                                                          |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71643-139">ондрагбегин</span><span class="sxs-lookup"><span data-stu-id="71643-139">onDragBegin</span></span>](customslider-ondragbegin.md)           | <span data-ttu-id="71643-140">Обрабатывает событие, возникающее, когда пользователь нажимает и удерживает левую кнопку мыши вниз и начинает перетаскивание мышью.</span><span class="sxs-lookup"><span data-stu-id="71643-140">Handles an event that occurs when the user clicks and holds the left mouse button down and begins to drag the mouse.</span></span> |
| [<span data-ttu-id="71643-141">ондраженд</span><span class="sxs-lookup"><span data-stu-id="71643-141">onDragEnd</span></span>](customslider-ondragend.md)               | <span data-ttu-id="71643-142">Обрабатывает событие, возникающее при отпускании левой кнопки мыши после операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="71643-142">Handles an event that occurs when the left mouse button is released after a dragging operation.</span></span>                      |
| [<span data-ttu-id="71643-143">онпоситиончанже</span><span class="sxs-lookup"><span data-stu-id="71643-143">onPositionChange</span></span>](customslider-onpositionchange.md) | <span data-ttu-id="71643-144">Обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем.</span><span class="sxs-lookup"><span data-stu-id="71643-144">Handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>   |



 

<span data-ttu-id="71643-145">Элемент **кустомслидер** поддерживает атрибуты окружения и может реализовывать обработчики событий окружения.</span><span class="sxs-lookup"><span data-stu-id="71643-145">The **CUSTOMSLIDER** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="71643-146">Дополнительные сведения см. в разделе [атрибуты окружения](ambient-attributes.md) и [обработчики событий окружения](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="71643-146">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71643-147">См. также</span><span class="sxs-lookup"><span data-stu-id="71643-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71643-148">**Справочник по программированию для обложки**</span><span class="sxs-lookup"><span data-stu-id="71643-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




