---
title: Преобразование шаблона элемента управления
description: Описывает правила и соглашения для реализации Итрансформпровидер и ITransformProvider2, включая сведения о свойствах и методах.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Transform
- Модель автоматизации пользовательского интерфейса, шаблон элемента Transform
- Модель автоматизации пользовательского интерфейса, Итрансформпровидер
- ITransformProvider
- реализация шаблонов элементов управления преобразования модели автоматизации пользовательского интерфейса
- Преобразование шаблонов элементов управления
- шаблоны элементов управления, Итрансформпровидер
- шаблоны элементов управления, реализация преобразования модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, преобразование
- интерфейсы, Итрансформпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533344"
---
# <a name="transform-control-pattern"></a><span data-ttu-id="889a9-113">Преобразование шаблона элемента управления</span><span class="sxs-lookup"><span data-stu-id="889a9-113">Transform Control Pattern</span></span>

<span data-ttu-id="889a9-114">Описывает правила и соглашения для реализации [**итрансформпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) и [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="889a9-114">Describes guidelines and conventions for implementing [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) and [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), including information about properties and methods.</span></span> <span data-ttu-id="889a9-115">Шаблон элемента управления Transform используется для поддержки элементов управления, которые можно перемещать, изменять их размер или вращать в двухмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="889a9-115">The Transform control pattern is used to support controls that can be moved, resized, or rotated within a two-dimensional space.</span></span>

<span data-ttu-id="889a9-116">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="889a9-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="889a9-117">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="889a9-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="889a9-118">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="889a9-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="889a9-119">Обязательные члены для **итрансформпровидер**</span><span class="sxs-lookup"><span data-stu-id="889a9-119">Required Members for **ITransformProvider**</span></span>](#required-members-for-itransformprovider)
-   [<span data-ttu-id="889a9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="889a9-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="889a9-121">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="889a9-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="889a9-122">При реализации шаблона элемента управления **Transform** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="889a9-122">When implementing the **Transform** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="889a9-123">Поддержка этого шаблона элемента управления не ограничена объектами на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="889a9-123">Support for this control pattern is not limited to objects on the desktop.</span></span> <span data-ttu-id="889a9-124">Этот шаблон элемента управления также должен поддерживаться дочерними элементами объекта контейнера, если эти дочерние элементы можно перемещать, изменять их размер или свободно поворачивать в пределах контейнера.</span><span class="sxs-lookup"><span data-stu-id="889a9-124">This control pattern must also be supported by the children of a container object if the children can be moved, resized, or rotated freely within the boundaries of the container.</span></span>
-   <span data-ttu-id="889a9-125">Объект нельзя перемещать, изменять его размер или поворачивать таким образом, что его итоговое положение на экране окажется полностью вне координат своего контейнера и поэтому он станет недоступным для клавиатуры или мыши (например, когда окно верхнего уровня перемещается за пределы экрана или дочерний объект перемещается за пределы границ окна просмотра контейнера).</span><span class="sxs-lookup"><span data-stu-id="889a9-125">An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and therefore inaccessible to the keyboard or mouse (for example, when a top-level window is moved off-screen or a child object is moved outside the boundaries of the container's viewport).</span></span> <span data-ttu-id="889a9-126">В этих случаях объект помещается максимально близко к запрошенным экранным координатам с переопределением верхней или левой координаты, чтобы они находились в границах контейнера.</span><span class="sxs-lookup"><span data-stu-id="889a9-126">In these cases, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.</span></span>
-   <span data-ttu-id="889a9-127">Для систем с несколькими мониторами при перемещении объекта, изменении его размера или повороте полностью за пределами координат объединенного рабочего стола объект помещается на основном мониторе максимально близко к запрошенным координатам.</span><span class="sxs-lookup"><span data-stu-id="889a9-127">For multi-monitor systems, if an object is moved, resized, or rotated completely outside the combined desktop screen coordinates, the object is placed on the primary monitor as close to the requested coordinates as possible.</span></span>
-   <span data-ttu-id="889a9-128">Все параметры и значения свойств являются абсолютными и не зависят от языка и региональных параметров.</span><span class="sxs-lookup"><span data-stu-id="889a9-128">All parameters and property values are absolute and independent of locale.</span></span>

## <a name="required-members-for-itransformprovider"></a><span data-ttu-id="889a9-129">Обязательные члены для **итрансформпровидер**</span><span class="sxs-lookup"><span data-stu-id="889a9-129">Required Members for **ITransformProvider**</span></span>

<span data-ttu-id="889a9-130">Для реализации интерфейса [**итрансформпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="889a9-130">The following properties and methods are required for implementing the [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="889a9-131">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="889a9-131">Required members</span></span>                                         | <span data-ttu-id="889a9-132">Тип члена</span><span class="sxs-lookup"><span data-stu-id="889a9-132">Member type</span></span> | <span data-ttu-id="889a9-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="889a9-133">Notes</span></span> |
|----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="889a9-134">**канмове**</span><span class="sxs-lookup"><span data-stu-id="889a9-134">**CanMove**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | <span data-ttu-id="889a9-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="889a9-135">Property</span></span>    | <span data-ttu-id="889a9-136">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-136">None</span></span>  |
| [<span data-ttu-id="889a9-137">**канресизе**</span><span class="sxs-lookup"><span data-stu-id="889a9-137">**CanResize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | <span data-ttu-id="889a9-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="889a9-138">Property</span></span>    | <span data-ttu-id="889a9-139">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-139">None</span></span>  |
| [<span data-ttu-id="889a9-140">**канротате**</span><span class="sxs-lookup"><span data-stu-id="889a9-140">**CanRotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | <span data-ttu-id="889a9-141">Свойство</span><span class="sxs-lookup"><span data-stu-id="889a9-141">Property</span></span>    | <span data-ttu-id="889a9-142">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-142">None</span></span>  |
| [<span data-ttu-id="889a9-143">**Переместить**</span><span class="sxs-lookup"><span data-stu-id="889a9-143">**Move**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | <span data-ttu-id="889a9-144">Метод</span><span class="sxs-lookup"><span data-stu-id="889a9-144">Method</span></span>      | <span data-ttu-id="889a9-145">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-145">None</span></span>  |
| [<span data-ttu-id="889a9-146">**Изменить размер**</span><span class="sxs-lookup"><span data-stu-id="889a9-146">**Resize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | <span data-ttu-id="889a9-147">Метод</span><span class="sxs-lookup"><span data-stu-id="889a9-147">Method</span></span>      | <span data-ttu-id="889a9-148">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-148">None</span></span>  |
| [<span data-ttu-id="889a9-149">**Поворот**</span><span class="sxs-lookup"><span data-stu-id="889a9-149">**Rotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | <span data-ttu-id="889a9-150">Метод</span><span class="sxs-lookup"><span data-stu-id="889a9-150">Method</span></span>      | <span data-ttu-id="889a9-151">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-151">None</span></span>  |



 

<span data-ttu-id="889a9-152">Для реализации интерфейса [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) требуются следующие дополнительные свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="889a9-152">The following additional properties and methods are required for implementing the [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="889a9-153">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="889a9-153">Required members</span></span>                                              | <span data-ttu-id="889a9-154">Тип члена</span><span class="sxs-lookup"><span data-stu-id="889a9-154">Member type</span></span> | <span data-ttu-id="889a9-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="889a9-155">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="889a9-156">**канзум**</span><span class="sxs-lookup"><span data-stu-id="889a9-156">**CanZoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | <span data-ttu-id="889a9-157">Свойство</span><span class="sxs-lookup"><span data-stu-id="889a9-157">Property</span></span>    | <span data-ttu-id="889a9-158">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-158">None</span></span>  |
| [<span data-ttu-id="889a9-159">**Масштаб**</span><span class="sxs-lookup"><span data-stu-id="889a9-159">**Zoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | <span data-ttu-id="889a9-160">Метод</span><span class="sxs-lookup"><span data-stu-id="889a9-160">Method</span></span>      | <span data-ttu-id="889a9-161">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-161">None</span></span>  |
| [<span data-ttu-id="889a9-162">**зумбюнит**</span><span class="sxs-lookup"><span data-stu-id="889a9-162">**ZoomByUnit**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | <span data-ttu-id="889a9-163">Метод</span><span class="sxs-lookup"><span data-stu-id="889a9-163">Method</span></span>      | <span data-ttu-id="889a9-164">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-164">None</span></span>  |
| [<span data-ttu-id="889a9-165">**зумлевел**</span><span class="sxs-lookup"><span data-stu-id="889a9-165">**ZoomLevel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | <span data-ttu-id="889a9-166">Свойство</span><span class="sxs-lookup"><span data-stu-id="889a9-166">Property</span></span>    | <span data-ttu-id="889a9-167">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-167">None</span></span>  |
| [<span data-ttu-id="889a9-168">**зуммаксимум**</span><span class="sxs-lookup"><span data-stu-id="889a9-168">**ZoomMaximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | <span data-ttu-id="889a9-169">Свойство</span><span class="sxs-lookup"><span data-stu-id="889a9-169">Property</span></span>    | <span data-ttu-id="889a9-170">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-170">None</span></span>  |
| [<span data-ttu-id="889a9-171">**зумминимум**</span><span class="sxs-lookup"><span data-stu-id="889a9-171">**ZoomMinimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | <span data-ttu-id="889a9-172">Свойство</span><span class="sxs-lookup"><span data-stu-id="889a9-172">Property</span></span>    | <span data-ttu-id="889a9-173">Нет</span><span class="sxs-lookup"><span data-stu-id="889a9-173">None</span></span>  |



 

<span data-ttu-id="889a9-174">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="889a9-174">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="889a9-175">См. также</span><span class="sxs-lookup"><span data-stu-id="889a9-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="889a9-176">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="889a9-176">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="889a9-177">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="889a9-177">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="889a9-178">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="889a9-178">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 