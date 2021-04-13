---
title: Шаблон элемента управления Дроптаржет
description: Содержит правила и соглашения по реализации шаблона элемента управления Дроптаржет с помощью Идроптаржетпровидер, включая сведения о свойствах и методах.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Дроптаржет
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Дроптаржет
- Модель автоматизации пользовательского интерфейса, Идроптаржетпровидер
- IDropTargetProvider
- реализация шаблонов элементов управления Дроптаржет модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Дроптаржет
- шаблоны элементов управления, Идроптаржетпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Дроптаржет
- шаблоны элементов управления, Дроптаржет
- интерфейсы, Идроптаржетпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338188"
---
# <a name="droptarget-control-pattern"></a><span data-ttu-id="7064e-113">Шаблон элемента управления Дроптаржет</span><span class="sxs-lookup"><span data-stu-id="7064e-113">DropTarget Control Pattern</span></span>

<span data-ttu-id="7064e-114">Содержит правила и соглашения по реализации шаблона элемента управления **дроптаржет** с помощью [**идроптаржетпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="7064e-114">Provides guidelines and conventions for implementing the **DropTarget** control pattern by using [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), including information about properties and methods.</span></span> <span data-ttu-id="7064e-115">Шаблон элемента управления **дроптаржет** используется для поддержки элементов управления, которые могут быть целевым объектом операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="7064e-115">The **DropTarget** control pattern is used to support controls that can be the target of a drag-and-drop operation.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="7064e-116">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="7064e-116">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="7064e-117">При реализации шаблона элемента управления **дроптаржет** используйте следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="7064e-117">When implementing the **DropTarget** control pattern, use the following guidelines and conventions:</span></span>

-   <span data-ttu-id="7064e-118">Шаблон **дроптаржет** должен поддерживаться во время выполнения операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="7064e-118">The **DropTarget** pattern must be supported while a drag operation is in progress.</span></span> <span data-ttu-id="7064e-119">Она может поддерживаться даже в том случае, если операция перетаскивания не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7064e-119">It can be supported even when a drag operation is not in progress.</span></span>
-   <span data-ttu-id="7064e-120">Свойство [**идроптаржетпровидер::D роптаржетеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7064e-120">The [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property is required.</span></span>
-   <span data-ttu-id="7064e-121">Свойство [**идроптаржетпровидер::D роптаржетеффектс**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) является обязательным, если для целевого объекта существует несколько возможных эффектов перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="7064e-121">The [**IDropTargetProvider::DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) property is required when there is more than one possible drop effect for the target.</span></span>
-   <span data-ttu-id="7064e-122">Элемент должен вызывать события изменения свойства для свойств **дроптаржетеффект** ([**UIA \_ дроптаржетдроптаржетеффектпропертид**](uiauto-control-pattern-propids.md)) и **дроптаржетеффектс** ([**UIA \_ дроптаржетдроптаржетеффектспропертид**](uiauto-control-pattern-propids.md)) при их изменении.</span><span class="sxs-lookup"><span data-stu-id="7064e-122">The element must raise property changed events for the **DropTargetEffect** ([**UIA\_DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) and **DropTargetEffects** ([**UIA\_DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) properties when they change.</span></span>

## <a name="required-members-for-idroptargetprovider"></a><span data-ttu-id="7064e-123">Обязательные члены для **идроптаржетпровидер**</span><span class="sxs-lookup"><span data-stu-id="7064e-123">Required Members for **IDropTargetProvider**</span></span>

<span data-ttu-id="7064e-124">Для реализации интерфейса [**идроптаржетпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="7064e-124">The following properties and methods are required for implementing the [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) interface.</span></span>



| <span data-ttu-id="7064e-125">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="7064e-125">Required members</span></span>                                                                              | <span data-ttu-id="7064e-126">Тип члена</span><span class="sxs-lookup"><span data-stu-id="7064e-126">Member type</span></span> | <span data-ttu-id="7064e-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="7064e-127">Notes</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="7064e-128">**дроптаржетеффект**</span><span class="sxs-lookup"><span data-stu-id="7064e-128">**DropTargetEffect**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | <span data-ttu-id="7064e-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="7064e-129">Property</span></span>    | <span data-ttu-id="7064e-130">Нет</span><span class="sxs-lookup"><span data-stu-id="7064e-130">None</span></span>                                                                     |
| [<span data-ttu-id="7064e-131">**дроптаржетеффектс**</span><span class="sxs-lookup"><span data-stu-id="7064e-131">**DropTargetEffects**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | <span data-ttu-id="7064e-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="7064e-132">Property</span></span>    | <span data-ttu-id="7064e-133">Требуется, если цель перетаскивания поддерживает несколько возможных эффектов перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="7064e-133">Required if the drop target supports more than one possible drop effect.</span></span> |
| [<span data-ttu-id="7064e-134">**UIA \_ дроптаржет \_ дражентеревентид**</span><span class="sxs-lookup"><span data-stu-id="7064e-134">**UIA\_DropTarget\_DragEnterEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="7064e-135">Событие</span><span class="sxs-lookup"><span data-stu-id="7064e-135">Event</span></span>       | <span data-ttu-id="7064e-136">Нет</span><span class="sxs-lookup"><span data-stu-id="7064e-136">None</span></span>                                                                     |
| [<span data-ttu-id="7064e-137">**UIA \_ дроптаржет \_ драглеавивентид**</span><span class="sxs-lookup"><span data-stu-id="7064e-137">**UIA\_DropTarget\_DragLeaveEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="7064e-138">Событие</span><span class="sxs-lookup"><span data-stu-id="7064e-138">Event</span></span>       | <span data-ttu-id="7064e-139">Нет</span><span class="sxs-lookup"><span data-stu-id="7064e-139">None</span></span>                                                                     |
| [<span data-ttu-id="7064e-140">**UIA \_ дроптаржет \_ дроппедевентид**</span><span class="sxs-lookup"><span data-stu-id="7064e-140">**UIA\_DropTarget\_DroppedEventId**</span></span>](uiauto-event-ids.md)     | <span data-ttu-id="7064e-141">Событие</span><span class="sxs-lookup"><span data-stu-id="7064e-141">Event</span></span>       | <span data-ttu-id="7064e-142">Нет</span><span class="sxs-lookup"><span data-stu-id="7064e-142">None</span></span>                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="7064e-143">См. также</span><span class="sxs-lookup"><span data-stu-id="7064e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7064e-144">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="7064e-144">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="7064e-145">Перетащите шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="7064e-145">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[<span data-ttu-id="7064e-146">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="7064e-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="7064e-147">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="7064e-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="7064e-148">Поддержка модели автоматизации пользовательского интерфейса для перетаскивания</span><span class="sxs-lookup"><span data-stu-id="7064e-148">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 