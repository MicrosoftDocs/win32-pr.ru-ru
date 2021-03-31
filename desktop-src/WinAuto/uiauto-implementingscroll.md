---
title: Шаблон элемента управления Scroll
description: Описывает правила и соглашения для реализации Искроллпровидер, включая сведения о свойствах и методах. Шаблон элемента управления Scroll используется для поддержки элемента управления, который выступает в качестве прокручиваемого контейнера для коллекции дочерних объектов.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Scroll
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Scroll
- Модель автоматизации пользовательского интерфейса, Искроллпровидер
- IScrollProvider
- реализация шаблонов элемента управления Scroll модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Scroll
- шаблоны элементов управления, Искроллпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса прокрутка
- шаблоны элементов управления, прокрутка
- интерфейсы, Искроллпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777708"
---
# <a name="scroll-control-pattern"></a><span data-ttu-id="c1403-114">Шаблон элемента управления Scroll</span><span class="sxs-lookup"><span data-stu-id="c1403-114">Scroll Control Pattern</span></span>

<span data-ttu-id="c1403-115">Описывает правила и соглашения для реализации [**искроллпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="c1403-115">Describes guidelines and conventions for implementing [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), including information about properties and methods.</span></span> <span data-ttu-id="c1403-116">Шаблон элемента управления **Scroll** используется для поддержки элемента управления, который выступает в качестве прокручиваемого контейнера для коллекции дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="c1403-116">The **Scroll** control pattern is used to support a control that acts as a scrollable container for a collection of child objects.</span></span>

<span data-ttu-id="c1403-117">Элементу управления не требуется использовать полосы прокрутки для поддержки функций прокрутки, хотя обычно это делает.</span><span class="sxs-lookup"><span data-stu-id="c1403-117">The control is not required to use scroll bars to support the scrolling functionality, although it commonly does.</span></span> <span data-ttu-id="c1403-118">На следующем рисунке показан элемент управления прокрутки, который не использует полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="c1403-118">The following image shows a scrolling control that does not use scroll bars.</span></span> <span data-ttu-id="c1403-119">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="c1403-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![снимок экрана с элементом управления прокруткой без полос прокрутки](images/uia-scrollpattern-without-scrollbars.jpg)

<span data-ttu-id="c1403-121">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="c1403-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c1403-122">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="c1403-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c1403-123">Обязательные члены для **искроллпровидер**</span><span class="sxs-lookup"><span data-stu-id="c1403-123">Required Members for **IScrollProvider**</span></span>](#required-members-for-iscrollprovider)
-   [<span data-ttu-id="c1403-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c1403-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c1403-125">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="c1403-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c1403-126">При реализации шаблона элемента управления **Scroll** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="c1403-126">When implementing the **Scroll** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c1403-127">Дочерние элементы этого элемента управления должны реализовывать [**искроллитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span><span class="sxs-lookup"><span data-stu-id="c1403-127">The children of this control must implement [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span></span>
-   <span data-ttu-id="c1403-128">Полосы прокрутки элемента управления контейнера не поддерживают шаблон элемента управления **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="c1403-128">The scroll bars of a container control do not support the **Scroll** control pattern.</span></span> <span data-ttu-id="c1403-129">Вместо этого они должны поддерживать шаблон элемента управления [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="c1403-129">They must support the [RangeValue](uiauto-implementingrangevalue.md) control pattern instead.</span></span>
-   <span data-ttu-id="c1403-130">Если прокрутка измеряется в процентах, все значения или величины, связанные с делением шкалы прокрутки, должны быть нормализованы в диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="c1403-130">When scrolling is measured in percentages, all values or amounts related to scroll graduation must be normalized to a range of 0 to 100.</span></span>
-   <span data-ttu-id="c1403-131">Свойство [**искроллпровидер:: хоризонталлискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) и свойство [**вертикаллискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) не зависят от свойства, **включенного** .</span><span class="sxs-lookup"><span data-stu-id="c1403-131">The [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property and [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property are independent of the **IsEnabled** property.</span></span>
-   <span data-ttu-id="c1403-132">Если свойство [**искроллпровидер:: хоризонталлискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) имеет **значение false**, свойство [**хоризонталвиевсизе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) должно иметь значение 100 (100%). Свойство [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) должно иметь значение **UIA \_ скроллпаттернноскролл** (-1).</span><span class="sxs-lookup"><span data-stu-id="c1403-132">If the [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property is **FALSE**, the [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) property should be set to 100 (100%) and [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="c1403-133">Аналогично, если свойство [**вертикаллискроллабле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) имеет **значение false**, свойству [**вертикалвиевсизе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) должно быть присвоено значение 100 (100%). Свойство [**вертикалскроллперцент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) должно иметь значение **UIA \_ скроллпаттернноскролл** (-1).</span><span class="sxs-lookup"><span data-stu-id="c1403-133">Likewise, if the [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property is **FALSE**, the [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) property should be set to 100 (100%) and [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="c1403-134">Это позволяет клиенту Microsoft UI Automation использовать эти значения свойств в методе [**сетскроллперцент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) , одновременно избегая состояния гонки, если направление, в котором клиент не заинтересован в прокрутке, становится активным.</span><span class="sxs-lookup"><span data-stu-id="c1403-134">This allows a Microsoft UI Automation client to use these property values within the [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) method while avoiding a race condition if a direction the client is not interested in scrolling becomes activated.</span></span>
-   <span data-ttu-id="c1403-135">Свойство [**искроллпровидер:: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) зависит от языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="c1403-135">The [**IScrollProvider::HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property is locale-specific.</span></span> <span data-ttu-id="c1403-136">Если задать для **HorizontalScrollPercent** значение 100, расположение прокрутки элемента управления должно быть эквивалентно его крайней позиции для таких языков, как английский, чтение которых осуществляется слева направо.</span><span class="sxs-lookup"><span data-stu-id="c1403-136">Setting **HorizontalScrollPercent** to 100 must set the scrolling location of the control to the equivalent of its rightmost position for languages such as English that read left to right.</span></span> <span data-ttu-id="c1403-137">Кроме того, для таких языков, как арабский, который читается справа налево, установка **HorizontalScrollPercent** в 100 должна установить расположение прокрутки в самую левую позицию.</span><span class="sxs-lookup"><span data-stu-id="c1403-137">Alternately, for languages such as Arabic that read right to left, setting **HorizontalScrollPercent** to 100 must set the scroll location to the leftmost position.</span></span>

## <a name="required-members-for-iscrollprovider"></a><span data-ttu-id="c1403-138">Обязательные члены для **искроллпровидер**</span><span class="sxs-lookup"><span data-stu-id="c1403-138">Required Members for **IScrollProvider**</span></span>

<span data-ttu-id="c1403-139">Для реализации интерфейса [**искроллпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="c1403-139">The following properties and methods are required for implementing the [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) interface.</span></span>



| <span data-ttu-id="c1403-140">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="c1403-140">Required members</span></span>                                                                  | <span data-ttu-id="c1403-141">Тип члена</span><span class="sxs-lookup"><span data-stu-id="c1403-141">Member type</span></span> | <span data-ttu-id="c1403-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="c1403-142">Notes</span></span> |
|-----------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="c1403-143">**HorizontalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="c1403-143">**HorizontalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | <span data-ttu-id="c1403-144">Свойство</span><span class="sxs-lookup"><span data-stu-id="c1403-144">Property</span></span>    | <span data-ttu-id="c1403-145">Нет</span><span class="sxs-lookup"><span data-stu-id="c1403-145">None</span></span>  |
| [<span data-ttu-id="c1403-146">**вертикалскроллперцент**</span><span class="sxs-lookup"><span data-stu-id="c1403-146">**VerticalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | <span data-ttu-id="c1403-147">Свойство</span><span class="sxs-lookup"><span data-stu-id="c1403-147">Property</span></span>    | <span data-ttu-id="c1403-148">Нет</span><span class="sxs-lookup"><span data-stu-id="c1403-148">None</span></span>  |
| [<span data-ttu-id="c1403-149">**хоризонталвиевсизе**</span><span class="sxs-lookup"><span data-stu-id="c1403-149">**HorizontalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | <span data-ttu-id="c1403-150">Свойство</span><span class="sxs-lookup"><span data-stu-id="c1403-150">Property</span></span>    | <span data-ttu-id="c1403-151">Нет</span><span class="sxs-lookup"><span data-stu-id="c1403-151">None</span></span>  |
| [<span data-ttu-id="c1403-152">**вертикалвиевсизе**</span><span class="sxs-lookup"><span data-stu-id="c1403-152">**VerticalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | <span data-ttu-id="c1403-153">Свойство</span><span class="sxs-lookup"><span data-stu-id="c1403-153">Property</span></span>    | <span data-ttu-id="c1403-154">Нет</span><span class="sxs-lookup"><span data-stu-id="c1403-154">None</span></span>  |
| [<span data-ttu-id="c1403-155">**хоризонталлискроллабле**</span><span class="sxs-lookup"><span data-stu-id="c1403-155">**HorizontallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | <span data-ttu-id="c1403-156">Свойство</span><span class="sxs-lookup"><span data-stu-id="c1403-156">Property</span></span>    | <span data-ttu-id="c1403-157">Нет</span><span class="sxs-lookup"><span data-stu-id="c1403-157">None</span></span>  |
| [<span data-ttu-id="c1403-158">**вертикаллискроллабле**</span><span class="sxs-lookup"><span data-stu-id="c1403-158">**VerticallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | <span data-ttu-id="c1403-159">Свойство</span><span class="sxs-lookup"><span data-stu-id="c1403-159">Property</span></span>    | <span data-ttu-id="c1403-160">Нет</span><span class="sxs-lookup"><span data-stu-id="c1403-160">None</span></span>  |
| [<span data-ttu-id="c1403-161">**Scroll**</span><span class="sxs-lookup"><span data-stu-id="c1403-161">**Scroll**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | <span data-ttu-id="c1403-162">Метод</span><span class="sxs-lookup"><span data-stu-id="c1403-162">Method</span></span>      | <span data-ttu-id="c1403-163">Нет</span><span class="sxs-lookup"><span data-stu-id="c1403-163">None</span></span>  |
| [<span data-ttu-id="c1403-164">**сетскроллперцент**</span><span class="sxs-lookup"><span data-stu-id="c1403-164">**SetScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | <span data-ttu-id="c1403-165">Метод</span><span class="sxs-lookup"><span data-stu-id="c1403-165">Method</span></span>      | <span data-ttu-id="c1403-166">Нет</span><span class="sxs-lookup"><span data-stu-id="c1403-166">None</span></span>  |



 

<span data-ttu-id="c1403-167">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="c1403-167">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1403-168">См. также</span><span class="sxs-lookup"><span data-stu-id="c1403-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1403-169">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="c1403-169">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="c1403-170">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c1403-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c1403-171">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c1403-171">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




