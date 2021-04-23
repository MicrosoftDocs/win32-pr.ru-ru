---
title: Вызвать шаблон элемента управления
description: Описывает правила и соглашения для реализации IInvokeProvider, включая сведения о методах.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Invoke
- Модель автоматизации пользовательского интерфейса, вызов шаблона элемента управления
- Модель автоматизации пользовательского интерфейса, IInvokeProvider
- IInvokeProvider
- реализация шаблонов элементов управления, вызывающих автоматизацию пользовательского интерфейса
- Вызов шаблонов элементов управления
- шаблоны элементов управления, IInvokeProvider
- шаблоны элементов управления, реализация вызова модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, Invoke
- интерфейсы, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888159"
---
# <a name="invoke-control-pattern"></a><span data-ttu-id="137c0-113">Вызвать шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="137c0-113">Invoke Control Pattern</span></span>

<span data-ttu-id="137c0-114">Описывает правила и соглашения для реализации [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), включая сведения о методах.</span><span class="sxs-lookup"><span data-stu-id="137c0-114">Describes guidelines and conventions for implementing [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), including information about methods.</span></span> <span data-ttu-id="137c0-115">Шаблон элемента управления **Invoke** используется для поддержки элементов управления, которые не сохраняют состояние при активации, а инициируют или выполняют одно однозначное действие.</span><span class="sxs-lookup"><span data-stu-id="137c0-115">The **Invoke** control pattern is used to support controls that do not maintain state when activated but rather initiate or perform a single, unambiguous action.</span></span>

<span data-ttu-id="137c0-116">Элементы управления, которые сохраняют состояние, такие как флажки и переключатели, должны вместо этого реализовывать [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) и [**иселектионпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) соответственно.</span><span class="sxs-lookup"><span data-stu-id="137c0-116">Controls that do maintain state, such as check boxes and radio buttons, must instead implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) and [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectively.</span></span> <span data-ttu-id="137c0-117">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="137c0-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="137c0-118">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="137c0-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="137c0-119">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="137c0-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="137c0-120">Обязательные члены для **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="137c0-120">Required Members for **IInvokeProvider**</span></span>](#required-members-for-iinvokeprovider)
-   [<span data-ttu-id="137c0-121">См. также</span><span class="sxs-lookup"><span data-stu-id="137c0-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="137c0-122">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="137c0-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="137c0-123">При реализации шаблона элемента управления **Invoke** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="137c0-123">When implementing the **Invoke** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="137c0-124">Элементы управления реализуют [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) , если такое же поведение не предоставляется через другой поставщик шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="137c0-124">Controls implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) if the same behavior is not exposed through another control pattern provider.</span></span> <span data-ttu-id="137c0-125">Например, если метод [**иуиаутоматионинвокепаттерн:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) в элементе управления выполняет то же действие, что и метод [**Иуиаутоматионекспандколлапсепаттерн:: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) или [**сворачивания**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) , элемент управления не должен реализовывать **IInvokeProvider**.</span><span class="sxs-lookup"><span data-stu-id="137c0-125">For example, if the [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) method on a control performs the same action as the [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) or [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) method, the control should not implement **IInvokeProvider**.</span></span>
-   <span data-ttu-id="137c0-126">Обычно для вызова элемента управления нужно щелкнуть, дважды щелкнуть, нажать клавишу ВВОД, нажать стандартное сочетание клавиш или нажать некоторое другую другое сочетание клавиш.</span><span class="sxs-lookup"><span data-stu-id="137c0-126">Invoking a control is generally performed by clicking or double-clicking or pressing ENTER, a predefined keyboard shortcut, or some alternate combination of keystrokes.</span></span>
-   <span data-ttu-id="137c0-127">Событие **вызванного** события ([**UIA \_ Invoke \_ инвокедевентид**](uiauto-event-ids.md)) вызывается для элемента управления, который был активирован (как ответ на элемент управления, выполняющий связанное действие).</span><span class="sxs-lookup"><span data-stu-id="137c0-127">The **Invoked** event ([**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md)) event is raised on a control that has been activated (as a response to a control carrying out its associated action).</span></span> <span data-ttu-id="137c0-128">Если это возможно, событие должно вызываться после завершения действия элементом управления и его возврата без блокировки.</span><span class="sxs-lookup"><span data-stu-id="137c0-128">If possible, the event should be raised after the control has completed the action and returned without blocking.</span></span> <span data-ttu-id="137c0-129">**Вызываемое** событие (**UIA \_ Invoke \_ инвокедевентид**) должно быть создано перед обслуживанием запроса **Invoke** в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="137c0-129">The **Invoked** event (**UIA\_Invoke\_InvokedEventId**) should be raised before servicing the **Invoke** request in the following scenarios:</span></span>
    -   <span data-ttu-id="137c0-130">невозможно или нецелесообразно ожидать завершения действия;</span><span class="sxs-lookup"><span data-stu-id="137c0-130">It is not possible or practical to wait until the action is complete.</span></span>
    -   <span data-ttu-id="137c0-131">действие требует взаимодействия с пользователем;</span><span class="sxs-lookup"><span data-stu-id="137c0-131">The action requires user interaction.</span></span>
    -   <span data-ttu-id="137c0-132">действие занимает много времени и приведет к блокировке вызывающего клиента на значительное время.</span><span class="sxs-lookup"><span data-stu-id="137c0-132">The action is time-consuming and will cause the calling client to block for a significant amount of time.</span></span>
-   <span data-ttu-id="137c0-133">Если вызов элемента управления имеет существенные побочные эффекты, эти побочные эффекты должны предоставляться через свойство **HELPTEXT** .</span><span class="sxs-lookup"><span data-stu-id="137c0-133">If invoking the control has significant side-effects, those side-effects should be exposed through the **HelpText** property.</span></span> <span data-ttu-id="137c0-134">Например, несмотря на то, что [**иуиаутоматионинвокепаттерн:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) не связан с выделением, **Invoke** может привести к тому, что другой элемент управления станет выбранным.</span><span class="sxs-lookup"><span data-stu-id="137c0-134">For example, even though [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) is not associated with selection, **Invoke** may cause another control to become selected.</span></span>
-   <span data-ttu-id="137c0-135">Эффекты наведения указателя (или мыши) обычно не составляют **вызванного** события.</span><span class="sxs-lookup"><span data-stu-id="137c0-135">Hover (or mouse-over) effects generally do not constitute an **Invoked** event.</span></span> <span data-ttu-id="137c0-136">Однако элементы управления, выполняющие действие (а не вызывающие визуальные эффекты) на основе состояния наведения, должны поддерживать шаблон элемента управления **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="137c0-136">However, controls that perform an action (as opposed to cause a visual effect) based on the hover state should support the **Invoke** control pattern.</span></span>
    > [!Note]  
    > <span data-ttu-id="137c0-137">Эта реализация считается проблемой специальных возможностей, если элемент управления может быть вызван только в результате побочного эффекта, связанного с мышью.</span><span class="sxs-lookup"><span data-stu-id="137c0-137">This implementation is considered an accessibility issue if the control can be invoked only as a result of a mouse-related side effect.</span></span>

     

-   <span data-ttu-id="137c0-138">Вызов элемента управления отличается от выбора элемента.</span><span class="sxs-lookup"><span data-stu-id="137c0-138">Invoking a control is different from selecting an item.</span></span> <span data-ttu-id="137c0-139">Тем не менее в зависимости от элемента управления его вызов может привести к выбору элемента в качестве побочного эффекта.</span><span class="sxs-lookup"><span data-stu-id="137c0-139">However, depending on the control, invoking it may cause the item to become selected as a side-effect.</span></span> <span data-ttu-id="137c0-140">Например, при вызове элемента списка документов Microsoft Word в папке «Мои документы» выбирается элемент и открывается документ.</span><span class="sxs-lookup"><span data-stu-id="137c0-140">For example, invoking a Microsoft Word document list item in the My Documents folder both selects the item and opens the document.</span></span>
-   <span data-ttu-id="137c0-141">Элемент может исчезнуть из дерева Microsoft UI Automation сразу после вызова.</span><span class="sxs-lookup"><span data-stu-id="137c0-141">An element can disappear from the Microsoft UI Automation tree immediately upon being invoked.</span></span> <span data-ttu-id="137c0-142">В результате запрос информации из элемента, предоставленного обратным вызовом события, может завершиться неудачно.</span><span class="sxs-lookup"><span data-stu-id="137c0-142">Requesting information from the element provided by the event callback may fail as a result.</span></span> <span data-ttu-id="137c0-143">В качестве обходного решения рекомендуется выполнять предварительное кэширование информации.</span><span class="sxs-lookup"><span data-stu-id="137c0-143">Pre-fetching cached information is the recommended workaround.</span></span>
-   <span data-ttu-id="137c0-144">Элементы управления могут реализовывать множество шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="137c0-144">Controls can implement multiple control patterns.</span></span> <span data-ttu-id="137c0-145">Например, элемент управления **Цвет заливки** на панели инструментов Microsoft Excel реализует шаблоны элементов управления Invoke и [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="137c0-145">For example, the **Fill Color** control on the Microsoft Excel toolbar implements both the Invoke and the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control patterns.</span></span> <span data-ttu-id="137c0-146">Шаблон элемента управления ExpandCollapse предоставляет меню, а шаблон элемента управления **вызывает** заливку активного выделения выбранным цветом.</span><span class="sxs-lookup"><span data-stu-id="137c0-146">The ExpandCollapse control pattern exposes the menu and the **Invoke** control pattern fills the active selection with the chosen color.</span></span>

## <a name="required-members-for-iinvokeprovider"></a><span data-ttu-id="137c0-147">Обязательные члены для **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="137c0-147">Required Members for **IInvokeProvider**</span></span>

<span data-ttu-id="137c0-148">Для реализации интерфейса [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) требуется следующий метод.</span><span class="sxs-lookup"><span data-stu-id="137c0-148">The following method is required for implementing the [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) interface.</span></span>



| <span data-ttu-id="137c0-149">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="137c0-149">Required members</span></span>                                | <span data-ttu-id="137c0-150">Тип члена</span><span class="sxs-lookup"><span data-stu-id="137c0-150">Member type</span></span> | <span data-ttu-id="137c0-151">Примечания</span><span class="sxs-lookup"><span data-stu-id="137c0-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="137c0-152">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="137c0-152">**Invoke**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | <span data-ttu-id="137c0-153">Метод</span><span class="sxs-lookup"><span data-stu-id="137c0-153">Method</span></span>      | <span data-ttu-id="137c0-154">**Invoke** является асинхронным вызовом и должен возвращаться немедленно без блокировки.</span><span class="sxs-lookup"><span data-stu-id="137c0-154">**Invoke** is an asynchronous call and must return immediately without blocking.</span></span><br/> <span data-ttu-id="137c0-155">Это особенно важно для элементов управления, которые при вызове прямо или косвенно запускают модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="137c0-155">This behavior is particularly critical for controls that, directly or indirectly, launch a modal dialog when invoked.</span></span> <span data-ttu-id="137c0-156">Любой клиент автоматизации пользовательского интерфейса, инициировавший это событие, будет оставаться заблокированным до закрытия модального диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="137c0-156">Any UI Automation client that instigated the event will remain blocked until the modal dialog is closed.</span></span> <br/> |



 

<span data-ttu-id="137c0-157">Этот шаблон элемента управления не имеет связанных свойств или событий.</span><span class="sxs-lookup"><span data-stu-id="137c0-157">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="137c0-158">См. также</span><span class="sxs-lookup"><span data-stu-id="137c0-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="137c0-159">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="137c0-159">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="137c0-160">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="137c0-160">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="137c0-161">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="137c0-161">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="137c0-162">**UIA \_ Invoke \_ инвокедевентид**</span><span class="sxs-lookup"><span data-stu-id="137c0-162">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)
</dt> </dl>

 

 





