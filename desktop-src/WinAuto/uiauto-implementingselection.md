---
title: Шаблон элемента управления Selection
description: Описывает правила и соглашения для реализации Иселектионпровидер, включая сведения о свойствах, методах и событиях.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Selection
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Selection
- Модель автоматизации пользовательского интерфейса, Иселектионпровидер
- ISelectionProvider
- реализация шаблонов элементов управления для выбора модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления выбора
- шаблоны элементов управления, Иселектионпровидер
- шаблоны элементов управления, реализация выбора модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, выбор
- интерфейсы, Иселектионпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068033"
---
# <a name="selection-control-pattern"></a><span data-ttu-id="5c88e-113">Шаблон элемента управления Selection</span><span class="sxs-lookup"><span data-stu-id="5c88e-113">Selection Control Pattern</span></span>

<span data-ttu-id="5c88e-114">Описывает правила и соглашения для реализации [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), включая сведения о свойствах, методах и событиях.</span><span class="sxs-lookup"><span data-stu-id="5c88e-114">Describes guidelines and conventions for implementing [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="5c88e-115">Шаблон элемента управления **Selection** используется для поддержки элементов управления, которые действуют как контейнеры для коллекции выбираемых дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="5c88e-115">The **Selection** control pattern is used to support controls that act as containers for a collection of selectable child items.</span></span> <span data-ttu-id="5c88e-116">Дочерние элементы этого элемента должны реализовывать [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="5c88e-116">The children of this element must implement [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

<span data-ttu-id="5c88e-117">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="5c88e-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="5c88e-118">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="5c88e-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5c88e-119">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="5c88e-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="5c88e-120">Обязательные члены для **иселектионпровидер**</span><span class="sxs-lookup"><span data-stu-id="5c88e-120">Required Members for **ISelectionProvider**</span></span>](#required-members-for-iselectionprovider)
-   [<span data-ttu-id="5c88e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5c88e-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="5c88e-122">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="5c88e-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="5c88e-123">При реализации шаблона элемента управления **Selection** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="5c88e-123">When implementing the **Selection** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="5c88e-124">Элементы управления, реализующие [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) , позволяют выбирать как один, так и несколько дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="5c88e-124">Controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) allow either single or multiple child items to be selected.</span></span> <span data-ttu-id="5c88e-125">Например, списки, представления списков и представления в виде дерева поддерживают множественный выбор, тогда как поля со списком, ползунки и группы переключателей поддерживают одиночный выбор.</span><span class="sxs-lookup"><span data-stu-id="5c88e-125">For example, list boxes, list views, and tree views support multiple selections, whereas combo boxes, sliders, and radio button groups support single selection.</span></span>
-   <span data-ttu-id="5c88e-126">Элементы управления, имеющие минимальный, максимальный и непрерывный диапазоны, такие как элемент **управления "ползунок" в** проигрывателе мультимедиа, должны реализовывать [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) вместо [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="5c88e-126">Controls that have a minimum, maximum, and continuous range, such as the **Volume** slider control of a media player, should implement [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) instead of [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>
-   <span data-ttu-id="5c88e-127">Элементы управления с одним выбором, которые управляют дочерними элементами управления, которые реализуют [**иравелементпровидерфрагментрут**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), такие как ползунок **разрешения экрана** в диалоговом окне **свойства отображения** для Windows или элемент управления выбора **цвета** из Microsoft Word (см. следующий рисунок), должны реализовывать [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider). их дочерние элементы должны реализовывать как [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) , так и [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="5c88e-127">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, or the **Color Picker** selection control from Microsoft Word (see the following image), should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

    ![изображение, показывающее пример сопоставления строк цветовой палитры](images/uia-valuepattern-colorpicker.jpg)

-   <span data-ttu-id="5c88e-129">Меню не поддерживают шаблон элемента управления **Selection** .</span><span class="sxs-lookup"><span data-stu-id="5c88e-129">Menus do not support the **Selection** control pattern.</span></span> <span data-ttu-id="5c88e-130">Если вы работаете с элементами меню, включающими как график, так и текст (например, элементы **области предварительного просмотра** в меню **вид** в Microsoft Outlook) и необходимо передать состояние, следует реализовать [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span><span class="sxs-lookup"><span data-stu-id="5c88e-130">If you are working with menu items that include both graphics and text (such as the **Preview Pane** items in the **View** menu in Microsoft Outlook) and need to convey state, you should implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span></span>

## <a name="required-members-for-iselectionprovider"></a><span data-ttu-id="5c88e-131">Обязательные члены для **иселектионпровидер**</span><span class="sxs-lookup"><span data-stu-id="5c88e-131">Required Members for **ISelectionProvider**</span></span>

<span data-ttu-id="5c88e-132">Для реализации интерфейса [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) требуются следующие свойства, методы и события.</span><span class="sxs-lookup"><span data-stu-id="5c88e-132">The following properties, methods, and events are required for implementing the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>



| <span data-ttu-id="5c88e-133">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="5c88e-133">Required members</span></span>                                                                                | <span data-ttu-id="5c88e-134">Тип члена</span><span class="sxs-lookup"><span data-stu-id="5c88e-134">Member type</span></span> | <span data-ttu-id="5c88e-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c88e-135">Notes</span></span>                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="5c88e-136">**канселектмултипле**</span><span class="sxs-lookup"><span data-stu-id="5c88e-136">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | <span data-ttu-id="5c88e-137">Свойство</span><span class="sxs-lookup"><span data-stu-id="5c88e-137">Property</span></span>    | <span data-ttu-id="5c88e-138">Нет</span><span class="sxs-lookup"><span data-stu-id="5c88e-138">None</span></span>                                                                        |
| [<span data-ttu-id="5c88e-139">**исселектионрекуиред**</span><span class="sxs-lookup"><span data-stu-id="5c88e-139">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | <span data-ttu-id="5c88e-140">Свойство</span><span class="sxs-lookup"><span data-stu-id="5c88e-140">Property</span></span>    | <span data-ttu-id="5c88e-141">Нет</span><span class="sxs-lookup"><span data-stu-id="5c88e-141">None</span></span>                                                                        |
| [<span data-ttu-id="5c88e-142">**Выборка**</span><span class="sxs-lookup"><span data-stu-id="5c88e-142">**GetSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | <span data-ttu-id="5c88e-143">Метод</span><span class="sxs-lookup"><span data-stu-id="5c88e-143">Method</span></span>      | <span data-ttu-id="5c88e-144">Нет</span><span class="sxs-lookup"><span data-stu-id="5c88e-144">None</span></span>                                                                        |
| [<span data-ttu-id="5c88e-145">**\_Выбор UIA \_ инвалидатедевентид**</span><span class="sxs-lookup"><span data-stu-id="5c88e-145">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="5c88e-146">Событие</span><span class="sxs-lookup"><span data-stu-id="5c88e-146">Event</span></span>       | <span data-ttu-id="5c88e-147">Это событие вызывается, когда выделение в контейнере значительно изменилось.</span><span class="sxs-lookup"><span data-stu-id="5c88e-147">Raise this event when a selection in a container has changed significantly.</span></span> |



 

<span data-ttu-id="5c88e-148">Свойства [**иселектионпровидер:: исселектионрекуиред**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) и [**канселектмултипле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) могут быть динамическими.</span><span class="sxs-lookup"><span data-stu-id="5c88e-148">The [**ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) and [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) properties can be dynamic.</span></span> <span data-ttu-id="5c88e-149">Например, начальное состояние элемента управления может не иметь элементов, выбранных по умолчанию, что означает, что **исселектионрекуиред** имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="5c88e-149">For example, the initial state of a control might not have any items selected by default, indicating that **IsSelectionRequired** is false.</span></span> <span data-ttu-id="5c88e-150">Однако после выбора элемента элемент управления всегда должен иметь хотя бы один выбранный элемент.</span><span class="sxs-lookup"><span data-stu-id="5c88e-150">However, after an item is selected, the control must always have at least one item selected.</span></span> <span data-ttu-id="5c88e-151">В редких случаях элемент управления также может разрешать выбор нескольких элементов при инициализации, но впоследствии разрешает выбор только одного элемента.</span><span class="sxs-lookup"><span data-stu-id="5c88e-151">Similarly, in rare cases, a control might allow multiple items to be selected on initialization, but subsequently allow only single selections to be made.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c88e-152">См. также</span><span class="sxs-lookup"><span data-stu-id="5c88e-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c88e-153">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="5c88e-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="5c88e-154">Шаблон элемента управления SelectionItem</span><span class="sxs-lookup"><span data-stu-id="5c88e-154">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
</dt> <dt>

[<span data-ttu-id="5c88e-155">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c88e-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="5c88e-156">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5c88e-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




