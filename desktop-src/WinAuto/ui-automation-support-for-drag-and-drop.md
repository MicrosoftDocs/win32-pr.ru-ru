---
title: Поддержка модели автоматизации пользовательского интерфейса для перетаскивания
description: В этом разделе описываются шаблоны элементов управления, которые предоставляют сведения о возможностях перетаскивания элемента.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- Автоматизация пользовательского интерфейса, поддержка перетаскивания
- Модель автоматизации пользовательского интерфейса, обзор шаблона перетаскивания
- Модель автоматизации пользовательского интерфейса, общие сведения о шаблоне Дроптаржет
- Модель автоматизации пользовательского интерфейса, обзор перетаскивания
- шаблоны перетаскивания, сведения
- Перетащите шаблон элемента управления
- Шаблон элемента управления Дроптаржет
- шаблоны элементов управления, перетащите
- шаблоны элементов управления, Дроптаржет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681656"
---
# <a name="ui-automation-support-for-drag-and-drop"></a><span data-ttu-id="111be-112">Поддержка модели автоматизации пользовательского интерфейса для перетаскивания</span><span class="sxs-lookup"><span data-stu-id="111be-112">UI Automation Support for Drag-and-Drop</span></span>

<span data-ttu-id="111be-113">Модель автоматизации пользовательского интерфейса Майкрософт определяет два шаблона элементов управления для поддержки сценариев перетаскивания, шаблона элемента управления [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) и шаблона элемента управления [дроптаржет](/windows/desktop/WinAuto/uiauto-implementingdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="111be-113">Microsoft UI Automation defines two control patterns for supporting drag-and-drop scenarios, the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern, and the [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) control pattern.</span></span> <span data-ttu-id="111be-114">Вы реализуете шаблон элемента управления перетаскиванием для элемента, который можно перетаскивать, и шаблон элемента управления Дроптаржет для элемента, который может получить перетаскиваемый элемент. то есть цель перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="111be-114">You implement the Drag control pattern for an element that can be dragged, and the DropTarget control pattern for an element that can receive a dragged element; that is, a drop target.</span></span> <span data-ttu-id="111be-115">Эти два шаблона элементов управления предоставляют сведения, которые могут использоваться специальными технологиями, чтобы помочь пользователю в выполнении операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="111be-115">The two control patterns expose information that an assistive technology can use to help an accessibility user complete a drag-and-drop operation.</span></span>

-   [<span data-ttu-id="111be-116">Перетаскивание стилей</span><span class="sxs-lookup"><span data-stu-id="111be-116">Dragging Styles</span></span>](#dragging-styles)
    -   [<span data-ttu-id="111be-117">Исходный или конечный стиль</span><span class="sxs-lookup"><span data-stu-id="111be-117">Source/target Style</span></span>](#sourcetarget-style)
    -   [<span data-ttu-id="111be-118">Стиль только исходного кода</span><span class="sxs-lookup"><span data-stu-id="111be-118">Source-only Style</span></span>](#source-only-style)
-   [<span data-ttu-id="111be-119">Перетаскивание нескольких элементов</span><span class="sxs-lookup"><span data-stu-id="111be-119">Dragging Multiple Items</span></span>](#dragging-multiple-items)
-   [<span data-ttu-id="111be-120">Клиентские интерфейсы для перетаскивания</span><span class="sxs-lookup"><span data-stu-id="111be-120">Client Interfaces for Drag-and-Drop</span></span>](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a><span data-ttu-id="111be-121">Перетаскивание стилей</span><span class="sxs-lookup"><span data-stu-id="111be-121">Dragging Styles</span></span>

<span data-ttu-id="111be-122">При реализации шаблона элемента управления [перетаскиванием](/windows/desktop/WinAuto/uiauto-implementingdrag) для перетаскиваемого элемента необходимо решить, следует ли реализовать стиль перетаскивания *исходного или целевого объекта* или *только исходный* стиль перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="111be-122">When you implement the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern for a draggable element, you need to decide whether to implement the *source/target* dragging style, or the *source-only* dragging style.</span></span>

### <a name="sourcetarget-style"></a><span data-ttu-id="111be-123">Исходный или конечный стиль</span><span class="sxs-lookup"><span data-stu-id="111be-123">Source/target Style</span></span>

<span data-ttu-id="111be-124">В исходном или целевом стиле перетаскивания, перетаскиваемый элемент ("источник") и элемент Drop-Target ("цель") различаются, и каждый из них создает отдельный набор событий.</span><span class="sxs-lookup"><span data-stu-id="111be-124">In the source/target style of drag-and-drop, the dragged element (the "source") and the drop-target element (the "target") are distinct, and each raises a distinct set of events.</span></span> <span data-ttu-id="111be-125">Ниже приведен жизненный цикл операции перетаскивания, которая использует исходный или целевой стиль:</span><span class="sxs-lookup"><span data-stu-id="111be-125">Here's the life cycle for a drag operation that uses the source/target style:</span></span> <dl> <span data-ttu-id="111be-126">Когда пользователь запускает операцию перетаскивания:</span><span class="sxs-lookup"><span data-stu-id="111be-126">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="111be-127">Источник создает событие Драгстарт ([**UIA \_ Drag \_ драгстартевентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-127">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="111be-128">Источник задает для свойства [**идрагпровидер::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) **IsTrue значение true**.</span><span class="sxs-lookup"><span data-stu-id="111be-128">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="111be-129">Целевые объекты обновляют свойства [**дроптаржетеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) .</span><span class="sxs-lookup"><span data-stu-id="111be-129">Targets update their [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) properties.</span></span>

  
<span data-ttu-id="111be-130">Когда операция перетаскивания переходит в целевую область:</span><span class="sxs-lookup"><span data-stu-id="111be-130">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="111be-131">Целевой объект вызывает событие DragEnter ([**UIA \_ дроптаржет \_ дражентеревентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-131">The target raises the DragEnter ([**UIA\_DropTarget\_DragEnterEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="111be-132">Когда операция перетаскивания покидает целевую область:</span><span class="sxs-lookup"><span data-stu-id="111be-132">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="111be-133">Целевой объект вызывает событие DragLeave ([**UIA \_ дроптаржет \_ драглеавивентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-133">The target raises the DragLeave ([**UIA\_DropTarget\_DragLeaveEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="111be-134">Когда пользователь отпускает перетаскиваемый элемент на нецелевом:</span><span class="sxs-lookup"><span data-stu-id="111be-134">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="111be-135">Источник создает событие Драгканцел ([**UIA \_ Drag \_ драгканцелевентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-135">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="111be-136">Источник устанавливает свойство [**идрагпровидер::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) **IsFalse в значение false**.</span><span class="sxs-lookup"><span data-stu-id="111be-136">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="111be-137">Когда пользователь отпускает перетаскиваемый элемент на целевом объекте:</span><span class="sxs-lookup"><span data-stu-id="111be-137">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="111be-138">Источник создает событие Драгкомплете ([**UIA \_ Drag \_ драгкомплетивентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-138">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="111be-139">Источник устанавливает свойство [**идрагпровидер::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) **IsFalse в значение false**.</span><span class="sxs-lookup"><span data-stu-id="111be-139">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>
-   <span data-ttu-id="111be-140">Целевой объект задает свойство [**идроптаржетпровидер::D роптаржетеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) , которое указывает на произошедшее воздействие.</span><span class="sxs-lookup"><span data-stu-id="111be-140">The target sets the [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property to indicate the effect that occurred.</span></span>
-   <span data-ttu-id="111be-141">Целевой объект создает событие "удалено" ([**UIA \_ дроптаржет \_ дроппедевентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-141">The target raises the Dropped ([**UIA\_DropTarget\_DroppedEventId**](uiauto-event-ids.md)) event.</span></span>

  
</dl>

<span data-ttu-id="111be-142">События из исходного и целевого объектов тесно связаны, но отличаются друг от друга.</span><span class="sxs-lookup"><span data-stu-id="111be-142">The events from the source and target objects are closely related, but distinct.</span></span> <span data-ttu-id="111be-143">Данные о том, что происходит при перетаскивании, поступают из источника, а данные о том, что могло произойти, поступили из целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="111be-143">The data about what is being dragged comes from the source, while the data about "what could happen" and "what did happen" comes from the target.</span></span>

<span data-ttu-id="111be-144">При выполнении операции перетаскивания перетаскиваемый элемент можно перетаскивать в целевые регионы или из него любое количество раз до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="111be-144">When a drag operation is in progress, the dragged item can be dragged in and out of target regions any number of times before the operation completes.</span></span>

<span data-ttu-id="111be-145">Любая цель перетаскивания, нуждающаяся в обновлении свойства [**идроптаржетпровидер::D роптаржетеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) в режиме реального времени, должна вызвать дополнительное событие изменения свойства для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="111be-145">Any drop target that needs to update its [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property on the fly should raise an additional property changed event on that property.</span></span>

### <a name="source-only-style"></a><span data-ttu-id="111be-146">Стиль только исходного кода</span><span class="sxs-lookup"><span data-stu-id="111be-146">Source-only Style</span></span>

<span data-ttu-id="111be-147">Стиль перетаскивания «только исходный код» позволяет поставщику избегать реализации целевых объектов перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="111be-147">The source-only dragging style lets a provider avoid implementing drop targets.</span></span> <span data-ttu-id="111be-148">Не реализация целевых объектов перетаскивания помогает снизить затраты на реализацию, но не предоставляет клиентским приложениям специальных возможностей сведения об объекте, который получил удаление.</span><span class="sxs-lookup"><span data-stu-id="111be-148">Not implementing drop targets helps lower the implementation cost, but does not give accessibility client applications any information about the object that received the drop.</span></span> <span data-ttu-id="111be-149">Ниже приведен жизненный цикл операции перетаскивания, которая использует только исходный стиль:</span><span class="sxs-lookup"><span data-stu-id="111be-149">Here's the life cycle for a drag operation that uses the source-only style:</span></span> <dl> <span data-ttu-id="111be-150">Когда пользователь запускает операцию перетаскивания:</span><span class="sxs-lookup"><span data-stu-id="111be-150">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="111be-151">Источник создает событие Драгстарт ([**UIA \_ Drag \_ драгстартевентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-151">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="111be-152">Источник задает для свойства [**идрагпровидер::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) **IsTrue значение true**.</span><span class="sxs-lookup"><span data-stu-id="111be-152">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>

  
<span data-ttu-id="111be-153">Когда операция перетаскивания переходит в целевую область:</span><span class="sxs-lookup"><span data-stu-id="111be-153">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="111be-154">Источник задает для свойства [**идрагпровидер::D ропеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="111be-154">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="111be-155">Когда операция перетаскивания покидает целевую область:</span><span class="sxs-lookup"><span data-stu-id="111be-155">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="111be-156">Источник задает для свойства [**идрагпровидер::D ропеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="111be-156">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="111be-157">Когда пользователь отпускает перетаскиваемый элемент на нецелевом:</span><span class="sxs-lookup"><span data-stu-id="111be-157">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="111be-158">Источник создает событие Драгканцел ([**UIA \_ Drag \_ драгканцелевентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-158">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="111be-159">Источник устанавливает свойство [**идрагпровидер::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) **IsFalse в значение false**.</span><span class="sxs-lookup"><span data-stu-id="111be-159">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="111be-160">Когда пользователь отпускает перетаскиваемый элемент на целевом объекте:</span><span class="sxs-lookup"><span data-stu-id="111be-160">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="111be-161">Источник создает событие Драгкомплете ([**UIA \_ Drag \_ драгкомплетивентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-161">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="111be-162">Источник устанавливает свойство [**идрагпровидер::D ропеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) , чтобы указать результат, который выполнялся при удалении элемента.</span><span class="sxs-lookup"><span data-stu-id="111be-162">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to indicate the effect that took place when the item was dropped.</span></span>

  
</dl>

## <a name="dragging-multiple-items"></a><span data-ttu-id="111be-163">Перетаскивание нескольких элементов</span><span class="sxs-lookup"><span data-stu-id="111be-163">Dragging Multiple Items</span></span>

<span data-ttu-id="111be-164">Если поставщик реализует операции перетаскивания, в которых пользователь может одновременно перетаскивать несколько объектов, поставщик использует стили источника/назначения или исходного кода, как описано в предыдущем разделе, но с небольшой разницей.</span><span class="sxs-lookup"><span data-stu-id="111be-164">If a provider implements drag-and-drop operations where the user can drag multiple objects at the same time, the provider uses the source/target or source-only styles as described in the previous section, but with a small difference.</span></span> <span data-ttu-id="111be-165">Когда пользователь начинает операцию перетаскивания, поставщик создает элемент главного источника, представляющий полный набор элементов, которые перетаскиваются.</span><span class="sxs-lookup"><span data-stu-id="111be-165">When the user begins the drag operation, the provider creates a master source element that represents the full set of items that are being dragged.</span></span> <span data-ttu-id="111be-166">Элемент главного источника вызывает все события от имени набора перетаскиваемых элементов. элементы не вызывают никаких собственных событий.</span><span class="sxs-lookup"><span data-stu-id="111be-166">The master source element raises all events on behalf of the set of dragged items; the items don't raise any events of their own.</span></span><dl> <span data-ttu-id="111be-167">Когда пользователь запускает операцию перетаскивания:</span><span class="sxs-lookup"><span data-stu-id="111be-167">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="111be-168">Поставщик создает элемент Master source.</span><span class="sxs-lookup"><span data-stu-id="111be-168">The provider creates the master source element.</span></span>
-   <span data-ttu-id="111be-169">Элемент главного источника вызывает событие Драгстарт ([**UIA \_ Drag \_ драгстартевентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="111be-169">The master source element raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="111be-170">Элемент "Master source" задает для свойства [**идрагпровидер::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) **IsTrue значение true**.</span><span class="sxs-lookup"><span data-stu-id="111be-170">The master source element sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="111be-171">Элемент главного источника обновляет список извлеченных элементов, чтобы включить все перетаскиваемые элементы, чтобы метод [**жетграббедитемс**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) мог получить список.</span><span class="sxs-lookup"><span data-stu-id="111be-171">The master source element updates the list of grabbed items to include all items being dragged so that the [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) method can retrieve the list.</span></span>

  
</dl>

<span data-ttu-id="111be-172">Для этой точки главный элемент Source выполняет ту же роль, что и исходный элемент, как описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="111be-172">For that point on, the master source element performs the same role as that of the source element as described in the previous section.</span></span>

## <a name="client-interfaces-for-drag-and-drop"></a><span data-ttu-id="111be-173">Клиентские интерфейсы для перетаскивания</span><span class="sxs-lookup"><span data-stu-id="111be-173">Client Interfaces for Drag-and-Drop</span></span>

<span data-ttu-id="111be-174">Клиентские приложения модели автоматизации пользовательского интерфейса используют интерфейсы [**иуиаутоматиондрагпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) и [**иуиаутоматиондроптаржетпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) для доступа к сведениям о ПЕРЕТАСКИВАНИИ из элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="111be-174">UI Automation client applications use the [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) and [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) interfaces to access drag-and-drop information from UI elements.</span></span>

 

 