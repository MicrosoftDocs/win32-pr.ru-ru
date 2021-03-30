---
title: Переключить шаблон элемента управления
description: Описывает правила и соглашения для реализации IToggleProvider, включая сведения о свойствах и методах. Шаблон элемента управления Toggle используется для поддержки элементов управления, которые могут циклически проходить по набору состояний и поддерживать состояние после установки.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Toggle
- Модель автоматизации пользовательского интерфейса, переключить шаблон элемента управления
- Модель автоматизации пользовательского интерфейса, IToggleProvider
- IToggleProvider
- реализация шаблонов элементов управления для модели автоматизации пользовательского интерфейса
- Переключить шаблоны элементов управления
- шаблоны элементов управления, IToggleProvider
- шаблоны элементов управления, реализация переключателя модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, переключатель
- интерфейсы, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410763"
---
# <a name="toggle-control-pattern"></a><span data-ttu-id="0d0e2-114">Переключить шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="0d0e2-114">Toggle Control Pattern</span></span>

<span data-ttu-id="0d0e2-115">Описывает правила и соглашения для реализации [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-115">Describes guidelines and conventions for implementing [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), including information about properties and methods.</span></span> <span data-ttu-id="0d0e2-116">Шаблон элемента управления **Toggle** используется для поддержки элементов управления, которые могут циклически проходить по набору состояний и поддерживать состояние после установки.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-116">The **Toggle** control pattern is used to support controls that can cycle through a set of states and maintain a state once set.</span></span>

<span data-ttu-id="0d0e2-117">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="0d0e2-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="0d0e2-118">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0d0e2-119">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="0d0e2-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="0d0e2-120">Обязательные члены для **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-120">Required Members for **IToggleProvider**</span></span>](#required-members-for-itoggleprovider)
-   [<span data-ttu-id="0d0e2-121">См. также</span><span class="sxs-lookup"><span data-stu-id="0d0e2-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="0d0e2-122">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="0d0e2-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="0d0e2-123">При реализации шаблона элемента управления **Toggle** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-123">When implementing the **Toggle** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="0d0e2-124">Элементы управления, которые не сохраняют состояние при активации, такие как кнопки, кнопки панели инструментов и гиперссылки, должны реализовывать [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .</span><span class="sxs-lookup"><span data-stu-id="0d0e2-124">Controls that do not maintain state when activated, such as buttons, toolbar buttons, and hyperlinks, must implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) instead.</span></span>
-   <span data-ttu-id="0d0e2-125">Элемент управления должен циклически переключаться по его состояниям ([**тогглестате**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) в следующем порядке: **тогглестате \_ On**, **тогглестате \_ Off** и, если поддерживается, **тогглестате \_ неопределенный**.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-125">A control must cycle through its toggle states ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) in the following order: **ToggleState\_On**, **ToggleState\_Off** and, if supported, **ToggleState\_Indeterminate**.</span></span>
-   <span data-ttu-id="0d0e2-126">**Переключатель** не предоставляет метод Set-State из-за проблем, связанных с прямым заданием флажка с тремя состояниями, без прохода по соответствующей последовательности [**тогглестате**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) .</span><span class="sxs-lookup"><span data-stu-id="0d0e2-126">**Toggle** does not provide a set-state method because of issues surrounding the direct setting of a three-state check box without cycling through its appropriate [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) sequence.</span></span>
-   <span data-ttu-id="0d0e2-127">Элемент управления "переключатель" не реализует [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), так как он не способен циклически проходить по его допустимым состояниям.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-127">The radio button control does not implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), because it is not capable of cycling through its valid states.</span></span>

## <a name="required-members-for-itoggleprovider"></a><span data-ttu-id="0d0e2-128">Обязательные члены для **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-128">Required Members for **IToggleProvider**</span></span>

<span data-ttu-id="0d0e2-129">Для реализации интерфейса [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-129">The following properties and methods are required for implementing the [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) interface.</span></span>



| <span data-ttu-id="0d0e2-130">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="0d0e2-130">Required members</span></span>                                          | <span data-ttu-id="0d0e2-131">Тип члена</span><span class="sxs-lookup"><span data-stu-id="0d0e2-131">Member type</span></span> | <span data-ttu-id="0d0e2-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d0e2-132">Notes</span></span> |
|-----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="0d0e2-133">**Переключение**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-133">**Toggle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | <span data-ttu-id="0d0e2-134">Метод</span><span class="sxs-lookup"><span data-stu-id="0d0e2-134">Method</span></span>      | <span data-ttu-id="0d0e2-135">Нет</span><span class="sxs-lookup"><span data-stu-id="0d0e2-135">None</span></span>  |
| [<span data-ttu-id="0d0e2-136">**тогглестате**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-136">**ToggleState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | <span data-ttu-id="0d0e2-137">Свойство</span><span class="sxs-lookup"><span data-stu-id="0d0e2-137">Property</span></span>    | <span data-ttu-id="0d0e2-138">Нет</span><span class="sxs-lookup"><span data-stu-id="0d0e2-138">None</span></span>  |



 

<span data-ttu-id="0d0e2-139">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d0e2-140">См. также</span><span class="sxs-lookup"><span data-stu-id="0d0e2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d0e2-141">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="0d0e2-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="0d0e2-142">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0d0e2-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="0d0e2-143">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0d0e2-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




