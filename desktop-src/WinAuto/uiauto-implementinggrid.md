---
title: Шаблон элемента управления Grid
description: Описывает правила и соглашения для реализации IGridProvider, включая сведения о свойствах и методах. Шаблон элемента управления Grid используется для поддержки элементов управления, которые действуют как контейнеры для коллекции дочерних элементов.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Grid
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Grid
- Модель автоматизации пользовательского интерфейса, IGridProvider
- IGridProvider
- реализация шаблонов элементов управления сетки модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Grid
- шаблоны элементов управления, IGridProvider
- шаблоны элементов управления, реализация сетки автоматизации пользовательского интерфейса
- шаблоны элементов управления, сетка
- интерфейсы, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067737"
---
# <a name="grid-control-pattern"></a><span data-ttu-id="48d67-114">Шаблон элемента управления Grid</span><span class="sxs-lookup"><span data-stu-id="48d67-114">Grid Control Pattern</span></span>

<span data-ttu-id="48d67-115">Описывает правила и соглашения для реализации [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="48d67-115">Describes guidelines and conventions for implementing [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), including information about properties and methods.</span></span> <span data-ttu-id="48d67-116">Шаблон элемента управления **Grid** используется для поддержки элементов управления, которые действуют как контейнеры для коллекции дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="48d67-116">The **Grid** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="48d67-117">Дочерние элементы этого элемента должны реализовать [**игридитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) и быть организованы в двухмерной логической системе координат, которую можно просмотреть по строкам и столбцам.</span><span class="sxs-lookup"><span data-stu-id="48d67-117">The children of this element must implement [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="48d67-118">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="48d67-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="48d67-119">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="48d67-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="48d67-120">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="48d67-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="48d67-121">Обязательные члены для **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="48d67-121">Required Members for **IGridProvider**</span></span>](#required-members-for-igridprovider)
-   [<span data-ttu-id="48d67-122">См. также</span><span class="sxs-lookup"><span data-stu-id="48d67-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="48d67-123">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="48d67-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="48d67-124">При реализации шаблона элемента управления **Grid** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="48d67-124">When implementing the **Grid** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="48d67-125">Координаты сетки отсчитываются от нуля в левом верхнем углу (или в верхней правой ячейке в зависимости от языкового стандарта) с координатами (0, 0).</span><span class="sxs-lookup"><span data-stu-id="48d67-125">Grid coordinates are zero-based with the upper left (or upper right cell depending on locale) having coordinates (0,0).</span></span>
-   <span data-ttu-id="48d67-126">Если ячейка пуста, элемент автоматизации пользовательского интерфейса Майкрософт по-прежнему должен быть возвращен для поддержки свойства [**игридитемпровидер:: контаининггрид**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) этой ячейки.</span><span class="sxs-lookup"><span data-stu-id="48d67-126">If a cell is empty, a Microsoft UI Automation element must still be returned in order to support the [**IGridItemProvider::ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) property for that cell.</span></span> <span data-ttu-id="48d67-127">Это возможно, когда макет дочерних элементов сетки подобен массиву с переменной длиной (см. пример ниже).</span><span class="sxs-lookup"><span data-stu-id="48d67-127">This is possible when the layout of child elements in the grid is similar to a ragged array (see example below).</span></span>

    ![Пример элемента управления "Сетка" с пустыми координатами](images/grid.png)

-   <span data-ttu-id="48d67-129">Сетка с одним элементом по-прежнему необходима для реализации [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , если она логически считается сеткой.</span><span class="sxs-lookup"><span data-stu-id="48d67-129">A grid with a single item is still required to implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) if it is logically considered to be a grid.</span></span> <span data-ttu-id="48d67-130">Количество дочерних элементов в сетке не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="48d67-130">The number of child items in the grid is immaterial.</span></span>
-   <span data-ttu-id="48d67-131">Скрытые строки и столбцы в зависимости от реализации поставщика могут быть загружены в дерево модели автоматизации пользовательского интерфейса, поэтому они будут отражены в свойствах [**IGridProvider:: ROWCOUNT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) и [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) .</span><span class="sxs-lookup"><span data-stu-id="48d67-131">Hidden rows and columns, depending on the provider implementation, may be loaded in the UI Automation tree and will therefore be reflected in the [**IGridProvider::RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) and [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) properties.</span></span> <span data-ttu-id="48d67-132">Если скрытые строки и столбцы еще не загружены, они не должны учитываться.</span><span class="sxs-lookup"><span data-stu-id="48d67-132">If the hidden rows and columns have not yet been loaded, they should not be counted.</span></span>
-   <span data-ttu-id="48d67-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) не включает активную манипуляцию с сеткой; Для включения этой функции необходимо реализовать [**итрансформпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .</span><span class="sxs-lookup"><span data-stu-id="48d67-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not enable active manipulation of a grid; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) must be implemented to enable this functionality.</span></span>
-   <span data-ttu-id="48d67-134">Используйте [**иуиаутоматионструктуречанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) для прослушивания в сетке изменений структуры или макета, например ячеек, которые были добавлены, удалены или объединены.</span><span class="sxs-lookup"><span data-stu-id="48d67-134">Use a [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) to listen for structural or layout changes to the grid such as cells that have been added, removed, or merged.</span></span>
-   <span data-ttu-id="48d67-135">Используйте [**иуиаутоматионфокусчанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) , чтобы отвести обход элементов или ячеек сетки.</span><span class="sxs-lookup"><span data-stu-id="48d67-135">Use a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) to track traversal through the items or cells of a grid.</span></span>

## <a name="required-members-for-igridprovider"></a><span data-ttu-id="48d67-136">Обязательные члены для **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="48d67-136">Required Members for **IGridProvider**</span></span>

<span data-ttu-id="48d67-137">Для реализации интерфейса [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="48d67-137">The following properties and methods are required for implementing the [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) interface.</span></span>



| <span data-ttu-id="48d67-138">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="48d67-138">Required members</span></span>                                        | <span data-ttu-id="48d67-139">Тип члена</span><span class="sxs-lookup"><span data-stu-id="48d67-139">Member type</span></span> | <span data-ttu-id="48d67-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="48d67-140">Notes</span></span> |
|---------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="48d67-141">**Количества**</span><span class="sxs-lookup"><span data-stu-id="48d67-141">**RowCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | <span data-ttu-id="48d67-142">Свойство</span><span class="sxs-lookup"><span data-stu-id="48d67-142">Property</span></span>    | <span data-ttu-id="48d67-143">Нет</span><span class="sxs-lookup"><span data-stu-id="48d67-143">None</span></span>  |
| [<span data-ttu-id="48d67-144">**Число**</span><span class="sxs-lookup"><span data-stu-id="48d67-144">**ColumnCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | <span data-ttu-id="48d67-145">Свойство</span><span class="sxs-lookup"><span data-stu-id="48d67-145">Property</span></span>    | <span data-ttu-id="48d67-146">Нет</span><span class="sxs-lookup"><span data-stu-id="48d67-146">None</span></span>  |
| [<span data-ttu-id="48d67-147">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="48d67-147">**GetItem**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | <span data-ttu-id="48d67-148">Метод</span><span class="sxs-lookup"><span data-stu-id="48d67-148">Method</span></span>      | <span data-ttu-id="48d67-149">Нет</span><span class="sxs-lookup"><span data-stu-id="48d67-149">None</span></span>  |



 

<span data-ttu-id="48d67-150">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="48d67-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48d67-151">См. также</span><span class="sxs-lookup"><span data-stu-id="48d67-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48d67-152">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="48d67-152">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="48d67-153">Шаблон элемента управления GridItem</span><span class="sxs-lookup"><span data-stu-id="48d67-153">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
</dt> <dt>

[<span data-ttu-id="48d67-154">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="48d67-154">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="48d67-155">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="48d67-155">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




