---
title: Шаблон элемента управления SelectionItem
description: Описывает правила и соглашения для реализации Иселектионитемпровидер, включая сведения о свойствах, методах и событиях.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления SelectionItem
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления SelectionItem
- Модель автоматизации пользовательского интерфейса, Иселектионитемпровидер
- ISelectionItemProvider
- реализация шаблонов элементов управления SelectionItem модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления SelectionItem
- шаблоны элементов управления, Иселектионитемпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса SelectionItem
- шаблоны элементов управления, SelectionItem
- интерфейсы, Иселектионитемпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700487"
---
# <a name="selectionitem-control-pattern"></a><span data-ttu-id="eb121-113">Шаблон элемента управления SelectionItem</span><span class="sxs-lookup"><span data-stu-id="eb121-113">SelectionItem Control Pattern</span></span>

<span data-ttu-id="eb121-114">Описывает правила и соглашения для реализации [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), включая сведения о свойствах, методах и событиях.</span><span class="sxs-lookup"><span data-stu-id="eb121-114">Describes guidelines and conventions for implementing [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="eb121-115">Шаблон элемента управления **SelectionItem** используется для поддержки элементов управления, которые действуют как отдельные, выбираемые дочерние элементы элементов управления контейнера, реализующие [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="eb121-115">The **SelectionItem** control pattern is used to support controls that act as individual, selectable child items of container controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>

<span data-ttu-id="eb121-116">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="eb121-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="eb121-117">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="eb121-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="eb121-118">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="eb121-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="eb121-119">Обязательные члены для **иселектионитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="eb121-119">Required Members for **ISelectionItemProvider**</span></span>](#required-members-for-iselectionitemprovider)
-   [<span data-ttu-id="eb121-120">См. также</span><span class="sxs-lookup"><span data-stu-id="eb121-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="eb121-121">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="eb121-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="eb121-122">При реализации шаблона элемента управления **SelectionItem** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="eb121-122">When implementing the **SelectionItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="eb121-123">Элементы управления с одним выбором, которые управляют дочерними элементами управления, которые реализуют [**иравелементпровидерфрагментрут**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), такие как ползунок **разрешения экрана** в диалоговом окне **свойства отображения** для Windows, должны реализовывать [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider). их дочерние элементы должны реализовывать как [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) , так и [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="eb121-123">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

## <a name="required-members-for-iselectionitemprovider"></a><span data-ttu-id="eb121-124">Обязательные члены для **иселектионитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="eb121-124">Required Members for **ISelectionItemProvider**</span></span>

<span data-ttu-id="eb121-125">Для реализации интерфейса [**иселектионитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) требуются следующие свойства, методы и события.</span><span class="sxs-lookup"><span data-stu-id="eb121-125">The following properties, methods, and events are required for implementing the [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) interface.</span></span>



| <span data-ttu-id="eb121-126">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="eb121-126">Required members</span></span>                                                                                                                        | <span data-ttu-id="eb121-127">Тип члена</span><span class="sxs-lookup"><span data-stu-id="eb121-127">Member type</span></span> | <span data-ttu-id="eb121-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="eb121-128">Notes</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="eb121-129">**аддтоселектион**</span><span class="sxs-lookup"><span data-stu-id="eb121-129">**AddToSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | <span data-ttu-id="eb121-130">Метод</span><span class="sxs-lookup"><span data-stu-id="eb121-130">Method</span></span>      | <span data-ttu-id="eb121-131">Нет</span><span class="sxs-lookup"><span data-stu-id="eb121-131">None</span></span>  |
| [<span data-ttu-id="eb121-132">**IsSelected**</span><span class="sxs-lookup"><span data-stu-id="eb121-132">**IsSelected**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | <span data-ttu-id="eb121-133">Свойство</span><span class="sxs-lookup"><span data-stu-id="eb121-133">Property</span></span>    | <span data-ttu-id="eb121-134">Нет</span><span class="sxs-lookup"><span data-stu-id="eb121-134">None</span></span>  |
| [<span data-ttu-id="eb121-135">**ремовефромселектион**</span><span class="sxs-lookup"><span data-stu-id="eb121-135">**RemoveFromSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | <span data-ttu-id="eb121-136">Метод</span><span class="sxs-lookup"><span data-stu-id="eb121-136">Method</span></span>      | <span data-ttu-id="eb121-137">Нет</span><span class="sxs-lookup"><span data-stu-id="eb121-137">None</span></span>  |
| [<span data-ttu-id="eb121-138">**Метьте**</span><span class="sxs-lookup"><span data-stu-id="eb121-138">**Select**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | <span data-ttu-id="eb121-139">Метод</span><span class="sxs-lookup"><span data-stu-id="eb121-139">Method</span></span>      | <span data-ttu-id="eb121-140">Нет</span><span class="sxs-lookup"><span data-stu-id="eb121-140">None</span></span>  |
| [<span data-ttu-id="eb121-141">**селектионконтаинер**</span><span class="sxs-lookup"><span data-stu-id="eb121-141">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | <span data-ttu-id="eb121-142">Свойство</span><span class="sxs-lookup"><span data-stu-id="eb121-142">Property</span></span>    | <span data-ttu-id="eb121-143">Нет</span><span class="sxs-lookup"><span data-stu-id="eb121-143">None</span></span>  |
| [<span data-ttu-id="eb121-144">**UIA \_ SelectionItem \_ елементаддедтоселектионевентид**</span><span class="sxs-lookup"><span data-stu-id="eb121-144">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)         | <span data-ttu-id="eb121-145">Событие</span><span class="sxs-lookup"><span data-stu-id="eb121-145">Event</span></span>       | <span data-ttu-id="eb121-146">Нет</span><span class="sxs-lookup"><span data-stu-id="eb121-146">None</span></span>  |
| [<span data-ttu-id="eb121-147">**UIA \_ SelectionItem \_ елементремоведфромселектионевентид**</span><span class="sxs-lookup"><span data-stu-id="eb121-147">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="eb121-148">Событие</span><span class="sxs-lookup"><span data-stu-id="eb121-148">Event</span></span>       | <span data-ttu-id="eb121-149">Нет</span><span class="sxs-lookup"><span data-stu-id="eb121-149">None</span></span>  |
| [<span data-ttu-id="eb121-150">**UIA \_ SelectionItem \_ елементселектедевентид**</span><span class="sxs-lookup"><span data-stu-id="eb121-150">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="eb121-151">Событие</span><span class="sxs-lookup"><span data-stu-id="eb121-151">Event</span></span>       | <span data-ttu-id="eb121-152">Нет</span><span class="sxs-lookup"><span data-stu-id="eb121-152">None</span></span>  |



 

<span data-ttu-id="eb121-153">Если результат [**SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), [**аддтоселектион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)или [**ремовефромселектион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) является одним выбранным элементом, должно быть создано событие **елементселектед** ([**UIA \_ SelectionItem \_ елементселектедевентид**](uiauto-event-ids.md)). в противном случае создайте события **елементаддедтоселектион** ([**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)) или **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) соответственно.</span><span class="sxs-lookup"><span data-stu-id="eb121-153">If the result of a [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), an [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection), or a [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) is a single selected item, an **ElementSelected** event ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)) should be raised; otherwise raise **ElementAddedToSelection** ([**UIA\_SelectionItem\_ElementAddedToSelectionEventId**](uiauto-event-ids.md)) or **ElementRemovedFromSelection** ([**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) events as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb121-154">См. также</span><span class="sxs-lookup"><span data-stu-id="eb121-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb121-155">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="eb121-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="eb121-156">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="eb121-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="eb121-157">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="eb121-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




