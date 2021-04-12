---
title: Шаблон элемента управления Window
description: Описывает правила и соглашения для реализации IWindowProvider, включая сведения о свойствах, методах и событиях. Шаблон элемента управления Window поддерживает элементы управления, обеспечивающие фундаментальные функции на основе окна в традиционном графическом интерфейсе пользователя.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Window
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Window
- Модель автоматизации пользовательского интерфейса, IWindowProvider
- IWindowProvider
- реализация шаблонов элементов управления окна модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Window
- шаблоны элементов управления, IWindowProvider
- шаблоны элементов управления, реализация окна модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, окно
- интерфейсы, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332419"
---
# <a name="window-control-pattern"></a><span data-ttu-id="9e0ee-114">Шаблон элемента управления Window</span><span class="sxs-lookup"><span data-stu-id="9e0ee-114">Window Control Pattern</span></span>

<span data-ttu-id="9e0ee-115">Описывает правила и соглашения для реализации [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), включая сведения о свойствах, методах и событиях.</span><span class="sxs-lookup"><span data-stu-id="9e0ee-115">Describes guidelines and conventions for implementing [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="9e0ee-116">Шаблон элемента управления **Window** поддерживает элементы управления, обеспечивающие фундаментальные функции на основе окна в традиционном графическом интерфейсе пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e0ee-116">The **Window** control pattern supports controls that provide fundamental window-based functionality within a traditional GUI.</span></span>

<span data-ttu-id="9e0ee-117">Примеры элементов управления, которые должны реализовывать этот шаблон элемента управления, включают в себя окна приложений верхнего уровня, дочерние окна многодокументного интерфейса (MDI), элементы управления "область разделения" с изменяемыми размерами, модальные диалоговые окна и окна справки.</span><span class="sxs-lookup"><span data-stu-id="9e0ee-117">Examples of controls that must implement this control pattern include top-level application windows, multiple-document interface (MDI) child windows, resizable split pane controls, modal dialogs and balloon help windows.</span></span> <span data-ttu-id="9e0ee-118">Примеры элементов управления, реализующих данный шаблон элемента управления, см. в разделе [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="9e0ee-118">For examples of controls that implement this control pattern, see [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="9e0ee-119">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="9e0ee-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9e0ee-120">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="9e0ee-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="9e0ee-121">Обязательные члены для **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-121">Required Members for **IWindowProvider**</span></span>](#required-members-for-iwindowprovider)
-   [<span data-ttu-id="9e0ee-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9e0ee-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="9e0ee-123">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="9e0ee-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="9e0ee-124">При реализации шаблона элемента управления **Window** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="9e0ee-124">When implementing the **Window** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="9e0ee-125">Чтобы обеспечить возможность изменения размера окна и расположения экрана с помощью автоматизации пользовательского интерфейса Майкрософт, элемент управления должен реализовать [**итрансформпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) в дополнение к [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="9e0ee-125">To support the ability to modify both window size and screen position using Microsoft UI Automation, a control must implement [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) in addition to [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="9e0ee-126">Элементы управления, содержащие заголовки заголовков и элементы заголовка, позволяющие перемещать элемент управления, изменять его размер, разворачивание, свернутый или закрываемый, обычно необходимы для реализации [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="9e0ee-126">Controls that contain title bars, and title bar elements that enable the control to be moved, resized, maximized, minimized, or closed, are typically required to implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="9e0ee-127">Элементы управления, такие как всплывающие подсказки и поля со списком или раскрывающиеся меню, обычно не реализуют [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="9e0ee-127">Controls such as tooltip pop-ups and combo-box or menu drop-downs do not typically implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="9e0ee-128">Всплывающие окна справки изменяются от отображения окон основных всплывающих подсказок за счет предоставления кнопки **закрытия** , подобной окну.</span><span class="sxs-lookup"><span data-stu-id="9e0ee-128">Balloon help windows are differentiated from basic tooltip pop-ups by the provision of a window-like **Close** button.</span></span>
-   <span data-ttu-id="9e0ee-129">Полноэкранный режим не поддерживается [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) , так как он относится к конкретному приложению и не является обычным поведением окна.</span><span class="sxs-lookup"><span data-stu-id="9e0ee-129">Full-screen mode is not supported by [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) as it is feature-specific to an application and is not typical window behavior.</span></span>

## <a name="required-members-for-iwindowprovider"></a><span data-ttu-id="9e0ee-130">Обязательные члены для **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-130">Required Members for **IWindowProvider**</span></span>

<span data-ttu-id="9e0ee-131">Для реализации интерфейса [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) требуются следующие свойства, методы и события.</span><span class="sxs-lookup"><span data-stu-id="9e0ee-131">The following properties, methods, and events are required for implementing the [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) interface.</span></span>



| <span data-ttu-id="9e0ee-132">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="9e0ee-132">Required members</span></span>                                                                            | <span data-ttu-id="9e0ee-133">Тип члена</span><span class="sxs-lookup"><span data-stu-id="9e0ee-133">Member type</span></span> | <span data-ttu-id="9e0ee-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e0ee-134">Notes</span></span>                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="9e0ee-135">**виндовинтерактионстате**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-135">**WindowInteractionState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | <span data-ttu-id="9e0ee-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="9e0ee-136">Property</span></span>    | <span data-ttu-id="9e0ee-137">Не гарантируется, что **виндовинтерактионстате \_ реадифорусеринтерактион**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-137">Is not guaranteed to be **WindowInteractionState\_ReadyForUserInteraction**</span></span> |
| [<span data-ttu-id="9e0ee-138">**Modal**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-138">**IsModal**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | <span data-ttu-id="9e0ee-139">Свойство</span><span class="sxs-lookup"><span data-stu-id="9e0ee-139">Property</span></span>    | <span data-ttu-id="9e0ee-140">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-140">None</span></span>                                                                        |
| [<span data-ttu-id="9e0ee-141">**По верхнему уровню**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-141">**IsTopmost**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | <span data-ttu-id="9e0ee-142">Свойство</span><span class="sxs-lookup"><span data-stu-id="9e0ee-142">Property</span></span>    | <span data-ttu-id="9e0ee-143">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-143">None</span></span>                                                                        |
| [<span data-ttu-id="9e0ee-144">**канмаксимизе**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-144">**CanMaximize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | <span data-ttu-id="9e0ee-145">Свойство</span><span class="sxs-lookup"><span data-stu-id="9e0ee-145">Property</span></span>    | <span data-ttu-id="9e0ee-146">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-146">None</span></span>                                                                        |
| [<span data-ttu-id="9e0ee-147">**канминимизе**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-147">**CanMinimize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | <span data-ttu-id="9e0ee-148">Свойство</span><span class="sxs-lookup"><span data-stu-id="9e0ee-148">Property</span></span>    | <span data-ttu-id="9e0ee-149">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-149">None</span></span>                                                                        |
| [<span data-ttu-id="9e0ee-150">**виндоввисуалстате**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-150">**WindowVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | <span data-ttu-id="9e0ee-151">Свойство</span><span class="sxs-lookup"><span data-stu-id="9e0ee-151">Property</span></span>    | <span data-ttu-id="9e0ee-152">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-152">None</span></span>                                                                        |
| [<span data-ttu-id="9e0ee-153">**Закрыть**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-153">**Close**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | <span data-ttu-id="9e0ee-154">Метод</span><span class="sxs-lookup"><span data-stu-id="9e0ee-154">Method</span></span>      | <span data-ttu-id="9e0ee-155">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-155">None</span></span>                                                                        |
| [<span data-ttu-id="9e0ee-156">**сетвисуалстате**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-156">**SetVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | <span data-ttu-id="9e0ee-157">Метод</span><span class="sxs-lookup"><span data-stu-id="9e0ee-157">Method</span></span>      | <span data-ttu-id="9e0ee-158">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-158">None</span></span>                                                                        |
| [<span data-ttu-id="9e0ee-159">**ваитфоринпутидле**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-159">**WaitForInputIdle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | <span data-ttu-id="9e0ee-160">Метод</span><span class="sxs-lookup"><span data-stu-id="9e0ee-160">Method</span></span>      | <span data-ttu-id="9e0ee-161">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-161">None</span></span>                                                                        |
| [<span data-ttu-id="9e0ee-162">**\_Окно UIA \_ виндовклоседевентид**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-162">**UIA\_Window\_WindowClosedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="9e0ee-163">Событие</span><span class="sxs-lookup"><span data-stu-id="9e0ee-163">Event</span></span>       | <span data-ttu-id="9e0ee-164">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-164">None</span></span>                                                                        |
| [<span data-ttu-id="9e0ee-165">**\_Окно UIA \_ виндовопенедевентид**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-165">**UIA\_Window\_WindowOpenedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="9e0ee-166">Событие</span><span class="sxs-lookup"><span data-stu-id="9e0ee-166">Event</span></span>       | <span data-ttu-id="9e0ee-167">Нет</span><span class="sxs-lookup"><span data-stu-id="9e0ee-167">None</span></span>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="9e0ee-168">См. также</span><span class="sxs-lookup"><span data-stu-id="9e0ee-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9e0ee-169">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9e0ee-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9e0ee-170">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9e0ee-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="9e0ee-171">Сопоставление шаблона элемента управления для клиентов автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9e0ee-171">Control Pattern Mapping for UI Automation Clients</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="9e0ee-172">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9e0ee-172">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




