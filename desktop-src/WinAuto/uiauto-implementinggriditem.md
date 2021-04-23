---
title: Шаблон элемента управления GridItem
description: Описывает правила и соглашения для реализации Игридитемпровидер, включая сведения о свойствах. Шаблон элемента управления GridItem используется для поддержки отдельных дочерних элементов управления контейнеров, реализующих IGridProvider.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления GridItem
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления GridItem
- Модель автоматизации пользовательского интерфейса, Игридитемпровидер
- IGridItemProvider
- реализация шаблонов элементов управления GridItem модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления GridItem
- шаблоны элементов управления, Игридитемпровидер
- шаблоны элементов управления, реализация GridItem в модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, GridItem
- интерфейсы, Игридитемпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775230"
---
# <a name="griditem-control-pattern"></a><span data-ttu-id="3e7bb-114">Шаблон элемента управления GridItem</span><span class="sxs-lookup"><span data-stu-id="3e7bb-114">GridItem Control Pattern</span></span>

<span data-ttu-id="3e7bb-115">Описывает правила и соглашения для реализации [**игридитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), включая сведения о свойствах.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-115">Describes guidelines and conventions for implementing [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), including information about properties.</span></span> <span data-ttu-id="3e7bb-116">Шаблон элемента управления **GridItem** используется для поддержки отдельных дочерних элементов управления контейнеров, реализующих [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span><span class="sxs-lookup"><span data-stu-id="3e7bb-116">The **GridItem** control pattern is used to support individual child controls of containers that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>

<span data-ttu-id="3e7bb-117">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="3e7bb-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="3e7bb-118">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3e7bb-119">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="3e7bb-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="3e7bb-120">Обязательные члены для **игридитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="3e7bb-120">Required Members for **IGridItemProvider**</span></span>](#required-members-for-igriditemprovider)
-   [<span data-ttu-id="3e7bb-121">См. также</span><span class="sxs-lookup"><span data-stu-id="3e7bb-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="3e7bb-122">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="3e7bb-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="3e7bb-123">При реализации шаблона элемента управления **GridItem** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-123">When implementing the **GridItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="3e7bb-124">Координаты сетки отсчитываются от нуля, начиная с верхней левой ячейки с координатами (0, 0).</span><span class="sxs-lookup"><span data-stu-id="3e7bb-124">Grid coordinates are zero-based with the upper left cell having coordinates (0, 0).</span></span>
-   <span data-ttu-id="3e7bb-125">Объединенные ячейки будут сообщать о свойствах [**строк**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) и [**столбцов**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) в зависимости от базовой ячейки привязки, как определено поставщиком автоматизации пользовательского интерфейса Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-125">Merged cells will report their [**Row**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) and [**Column**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) properties based on their underlying anchor cell as defined by the Microsoft UI Automation provider.</span></span> <span data-ttu-id="3e7bb-126">Как правило, это будет самая верхняя строка и крайний левый столбец.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-126">Typically, it will be the topmost and leftmost row or column.</span></span>
-   <span data-ttu-id="3e7bb-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) не обеспечивает активную обработку сетки, например объединение или разбиение ячеек.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not provide for active manipulation of the grid such as merging or splitting cells.</span></span>
-   <span data-ttu-id="3e7bb-128">Элементы управления, которые реализуют [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , обычно обходятся (то есть клиент автоматизации пользовательского интерфейса могут переходить к смежным элементам управления) с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-128">Controls that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) can typically be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.</span></span>

## <a name="required-members-for-igriditemprovider"></a><span data-ttu-id="3e7bb-129">Обязательные члены для **игридитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="3e7bb-129">Required Members for **IGridItemProvider**</span></span>

<span data-ttu-id="3e7bb-130">Для реализации интерфейса [**игридитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) требуются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-130">The following properties are required for implementing the [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) interface.</span></span>



| <span data-ttu-id="3e7bb-131">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="3e7bb-131">Required members</span></span>                                                  | <span data-ttu-id="3e7bb-132">Тип члена</span><span class="sxs-lookup"><span data-stu-id="3e7bb-132">Member type</span></span> | <span data-ttu-id="3e7bb-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e7bb-133">Notes</span></span> |
|-------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="3e7bb-134">**Строка**</span><span class="sxs-lookup"><span data-stu-id="3e7bb-134">**Row**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | <span data-ttu-id="3e7bb-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="3e7bb-135">Property</span></span>    | <span data-ttu-id="3e7bb-136">Нет</span><span class="sxs-lookup"><span data-stu-id="3e7bb-136">None</span></span>  |
| [<span data-ttu-id="3e7bb-137">**Столбец**</span><span class="sxs-lookup"><span data-stu-id="3e7bb-137">**Column**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | <span data-ttu-id="3e7bb-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="3e7bb-138">Property</span></span>    | <span data-ttu-id="3e7bb-139">Нет</span><span class="sxs-lookup"><span data-stu-id="3e7bb-139">None</span></span>  |
| [<span data-ttu-id="3e7bb-140">**RowSpan**</span><span class="sxs-lookup"><span data-stu-id="3e7bb-140">**RowSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | <span data-ttu-id="3e7bb-141">Свойство</span><span class="sxs-lookup"><span data-stu-id="3e7bb-141">Property</span></span>    | <span data-ttu-id="3e7bb-142">Нет</span><span class="sxs-lookup"><span data-stu-id="3e7bb-142">None</span></span>  |
| [<span data-ttu-id="3e7bb-143">**ColumnSpan**</span><span class="sxs-lookup"><span data-stu-id="3e7bb-143">**ColumnSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | <span data-ttu-id="3e7bb-144">Свойство</span><span class="sxs-lookup"><span data-stu-id="3e7bb-144">Property</span></span>    | <span data-ttu-id="3e7bb-145">Нет</span><span class="sxs-lookup"><span data-stu-id="3e7bb-145">None</span></span>  |
| [<span data-ttu-id="3e7bb-146">**контаининггрид**</span><span class="sxs-lookup"><span data-stu-id="3e7bb-146">**ContainingGrid**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | <span data-ttu-id="3e7bb-147">Свойство</span><span class="sxs-lookup"><span data-stu-id="3e7bb-147">Property</span></span>    | <span data-ttu-id="3e7bb-148">Нет</span><span class="sxs-lookup"><span data-stu-id="3e7bb-148">None</span></span>  |



 

<span data-ttu-id="3e7bb-149">Этот шаблон элемента управления не имеет связанных методов или событий.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-149">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e7bb-150">См. также</span><span class="sxs-lookup"><span data-stu-id="3e7bb-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e7bb-151">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="3e7bb-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="3e7bb-152">Шаблон элемента управления Grid</span><span class="sxs-lookup"><span data-stu-id="3e7bb-152">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
</dt> <dt>

[<span data-ttu-id="3e7bb-153">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3e7bb-153">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="3e7bb-154">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3e7bb-154">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




