---
title: Шаблон элемента управления Dock
description: Описывает правила и соглашения для реализации IDockProvider, включая сведения о свойствах и методах. Шаблон элемента управления Dock используется для предоставления свойств Dock элемента управления в контейнере закрепления.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Dock
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Dock
- Модель автоматизации пользовательского интерфейса, IDockProvider
- IDockProvider
- реализация шаблонов элементов управления для модели автоматизации пользовательского интерфейса
- закрепление шаблонов элементов управления
- шаблоны элементов управления, IDockProvider
- шаблоны элементов управления, реализация элемента автоматизации пользовательского интерфейса
- шаблоны элементов управления, Dock
- интерфейсы, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888227"
---
# <a name="dock-control-pattern"></a><span data-ttu-id="9c40c-114">Шаблон элемента управления Dock</span><span class="sxs-lookup"><span data-stu-id="9c40c-114">Dock Control Pattern</span></span>

<span data-ttu-id="9c40c-115">Описывает правила и соглашения для реализации [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="9c40c-115">Describes guidelines and conventions for implementing [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), including information about properties and methods.</span></span> <span data-ttu-id="9c40c-116">Шаблон элемента управления **Dock** используется для предоставления свойств Dock элемента управления в контейнере закрепления.</span><span class="sxs-lookup"><span data-stu-id="9c40c-116">The **Dock** control pattern is used to expose the dock properties of a control within a docking container.</span></span>

<span data-ttu-id="9c40c-117">Контейнер закрепления — это элемент управления, который позволяет упорядочить дочерние элементы по горизонтали и по вертикали друг относительно друга.</span><span class="sxs-lookup"><span data-stu-id="9c40c-117">A docking container is a control that allows you to arrange child elements horizontally and vertically, relative to each other.</span></span> <span data-ttu-id="9c40c-118">На следующем рисунке показан контейнер закрепления с двумя дочерними элементами.</span><span class="sxs-lookup"><span data-stu-id="9c40c-118">The following image shows a docking container with two child elements.</span></span> <span data-ttu-id="9c40c-119">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="9c40c-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![снимок экрана с закрепленным контейнером с двумя закрепленными дочерними элементами](images/dockxmpl.jpg)

<span data-ttu-id="9c40c-121">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="9c40c-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9c40c-122">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="9c40c-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="9c40c-123">Обязательные члены для **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="9c40c-123">Required Members for **IDockProvider**</span></span>](#required-members-for-idockprovider)
-   [<span data-ttu-id="9c40c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="9c40c-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="9c40c-125">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="9c40c-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="9c40c-126">При реализации шаблона элемента управления **Dock** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="9c40c-126">When implementing the **Dock** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="9c40c-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) не предоставляет никаких свойств контейнера закрепления или любых свойств элементов управления, которые закреплены рядом с текущим элементом управления в контейнере закрепления.</span><span class="sxs-lookup"><span data-stu-id="9c40c-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) does not expose any properties of the docking container or any properties of controls that are docked adjacent to the current control within the docking container.</span></span>
-   <span data-ttu-id="9c40c-128">Элементы управления закрепляются относительно друг друга в зависимости от их текущего z-порядка; чем больше z-порядок расположения, тем дальше они размещены от заданного края контейнера закрепления.</span><span class="sxs-lookup"><span data-stu-id="9c40c-128">Controls are docked relative to each other based on their current z-order; the higher their z-order placement, the farther they are placed from the specified edge of the docking container.</span></span>
-   <span data-ttu-id="9c40c-129">При изменении размеров контейнера закрепления все закрепленные элементы управления в контейнере будут перенесены с выравниванием по тому же краю, к которому они были первоначально прикреплены.</span><span class="sxs-lookup"><span data-stu-id="9c40c-129">If the docking container is resized, any docked controls within the container will be repositioned flush to the same edge to which they were originally docked.</span></span> <span data-ttu-id="9c40c-130">Закрепленные элементы управления также будут изменять размер для заполнения любого пространства в контейнере в соответствии с поведением закрепления свойства [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) .</span><span class="sxs-lookup"><span data-stu-id="9c40c-130">The docked controls will also resize to fill any space within the container according to the docking behavior of their [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) property.</span></span> <span data-ttu-id="9c40c-131">Например, если задано **DockPosition \_ Top** , то левая и правая стороны элемента управления будут расширяться для заполнения любого доступного пространства.</span><span class="sxs-lookup"><span data-stu-id="9c40c-131">For example, if **DockPosition\_Top** is specified, the left and right sides of the control will expand to fill any available space.</span></span> <span data-ttu-id="9c40c-132">Если указан параметр **DockPosition \_ Fill** , все четыре стороны элемента управления будут расширяться для заполнения любого доступного пространства.</span><span class="sxs-lookup"><span data-stu-id="9c40c-132">If **DockPosition\_Fill** is specified, all four sides of the control will expand to fill any available space.</span></span>
-   <span data-ttu-id="9c40c-133">На системах с несколькими мониторами элементы управления должны закрепляться с левой или правой стороны текущего монитора.</span><span class="sxs-lookup"><span data-stu-id="9c40c-133">On a multi-monitor system, controls should dock to the left or right side of the current monitor.</span></span> <span data-ttu-id="9c40c-134">Если это невозможно, они должны закрепляться с левой стороны крайнего левого монитора или с правой стороны крайнего правого монитора.</span><span class="sxs-lookup"><span data-stu-id="9c40c-134">If that is not possible, they should dock to the left side of the leftmost monitor or the right side of the rightmost monitor.</span></span>

## <a name="required-members-for-idockprovider"></a><span data-ttu-id="9c40c-135">Обязательные члены для **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="9c40c-135">Required Members for **IDockProvider**</span></span>

<span data-ttu-id="9c40c-136">Для реализации интерфейса [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="9c40c-136">The following properties and methods are required for implementing the [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) interface.</span></span>



| <span data-ttu-id="9c40c-137">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="9c40c-137">Required members</span></span>                                                | <span data-ttu-id="9c40c-138">Тип члена</span><span class="sxs-lookup"><span data-stu-id="9c40c-138">Member type</span></span> | <span data-ttu-id="9c40c-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="9c40c-139">Notes</span></span> |
|-----------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="9c40c-140">**DockPosition**</span><span class="sxs-lookup"><span data-stu-id="9c40c-140">**DockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | <span data-ttu-id="9c40c-141">Свойство</span><span class="sxs-lookup"><span data-stu-id="9c40c-141">Property</span></span>    | <span data-ttu-id="9c40c-142">Нет</span><span class="sxs-lookup"><span data-stu-id="9c40c-142">None</span></span>  |
| [<span data-ttu-id="9c40c-143">**сетдоккпоситион**</span><span class="sxs-lookup"><span data-stu-id="9c40c-143">**SetDockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | <span data-ttu-id="9c40c-144">Метод</span><span class="sxs-lookup"><span data-stu-id="9c40c-144">Method</span></span>      | <span data-ttu-id="9c40c-145">Нет</span><span class="sxs-lookup"><span data-stu-id="9c40c-145">None</span></span>  |



 

<span data-ttu-id="9c40c-146">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="9c40c-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c40c-147">См. также</span><span class="sxs-lookup"><span data-stu-id="9c40c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c40c-148">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="9c40c-148">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="9c40c-149">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9c40c-149">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="9c40c-150">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9c40c-150">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




