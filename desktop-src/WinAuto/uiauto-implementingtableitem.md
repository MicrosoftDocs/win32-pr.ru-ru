---
title: Шаблон элемента управления TableItem
description: Описывает правила и соглашения для реализации Итаблеитемпровидер, включая сведения о методах. Шаблон элемента управления TableItem используется для поддержки дочерних элементов управления контейнеров, реализующих Итаблепровидер.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления TableItem
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления TableItem
- Модель автоматизации пользовательского интерфейса, Итаблеитемпровидер
- ITableItemProvider
- реализация шаблонов элементов управления TableItem модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления TableItem
- шаблоны элементов управления, Итаблеитемпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса TableItem
- шаблоны элементов управления, TableItem
- интерфейсы, Итаблеитемпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774813"
---
# <a name="tableitem-control-pattern"></a><span data-ttu-id="a7cc9-114">Шаблон элемента управления TableItem</span><span class="sxs-lookup"><span data-stu-id="a7cc9-114">TableItem Control Pattern</span></span>

<span data-ttu-id="a7cc9-115">Описывает правила и соглашения для реализации [**итаблеитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), включая сведения о методах.</span><span class="sxs-lookup"><span data-stu-id="a7cc9-115">Describes guidelines and conventions for implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), including information about methods.</span></span> <span data-ttu-id="a7cc9-116">Шаблон элемента управления **TableItem** используется для поддержки дочерних элементов управления контейнеров, реализующих [**итаблепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span><span class="sxs-lookup"><span data-stu-id="a7cc9-116">The **TableItem** control pattern is used to support child controls of containers that implement [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span></span>

<span data-ttu-id="a7cc9-117">Доступ к отдельным функциям ячейки обеспечивается необходимой, параллельной реализацией [**игридитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span><span class="sxs-lookup"><span data-stu-id="a7cc9-117">Access to individual cell functionality is provided by the required, concurrent implementation of [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span></span> <span data-ttu-id="a7cc9-118">Этот шаблон элемента управления является аналогом **игридитемпровидер** с различием того, что любой элемент управления, реализующий [**итаблеитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) , должен программно предоставлять связь между отдельной ячейкой и сведениями о строках и столбцах.</span><span class="sxs-lookup"><span data-stu-id="a7cc9-118">This control pattern is analogous to **IGridItemProvider** with the distinction that any control implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) must programmatically expose the relationship between the individual cell and its row and column information.</span></span> <span data-ttu-id="a7cc9-119">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="a7cc9-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="a7cc9-120">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="a7cc9-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a7cc9-121">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="a7cc9-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="a7cc9-122">Обязательные члены для **итаблеитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="a7cc9-122">Required Members for **ITableItemProvider**</span></span>](#required-members-for-itableitemprovider)
-   [<span data-ttu-id="a7cc9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a7cc9-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a7cc9-124">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="a7cc9-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a7cc9-125">При реализации шаблона элемента управления **TableItem** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="a7cc9-125">When implementing the **TableItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a7cc9-126">Сведения о связанных функциях элементов сетки см. в разделе [шаблон элемента управления GridItem](uiauto-implementinggriditem.md).</span><span class="sxs-lookup"><span data-stu-id="a7cc9-126">For related grid item functionality, see [GridItem Control Pattern](uiauto-implementinggriditem.md).</span></span>

## <a name="required-members-for-itableitemprovider"></a><span data-ttu-id="a7cc9-127">Обязательные члены для **итаблеитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="a7cc9-127">Required Members for **ITableItemProvider**</span></span>

<span data-ttu-id="a7cc9-128">Для реализации интерфейса [**итаблеитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) требуются следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a7cc9-128">The following methods are required for implementing the [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) interface.</span></span>



| <span data-ttu-id="a7cc9-129">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="a7cc9-129">Required members</span></span>                                                               | <span data-ttu-id="a7cc9-130">Тип члена</span><span class="sxs-lookup"><span data-stu-id="a7cc9-130">Member type</span></span> | <span data-ttu-id="a7cc9-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7cc9-131">Notes</span></span> |
|--------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="a7cc9-132">**жетколумнхеадеритемс**</span><span class="sxs-lookup"><span data-stu-id="a7cc9-132">**GetColumnHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | <span data-ttu-id="a7cc9-133">Метод</span><span class="sxs-lookup"><span data-stu-id="a7cc9-133">Method</span></span>      | <span data-ttu-id="a7cc9-134">Нет</span><span class="sxs-lookup"><span data-stu-id="a7cc9-134">None</span></span>  |
| [<span data-ttu-id="a7cc9-135">**жетровхеадеритемс**</span><span class="sxs-lookup"><span data-stu-id="a7cc9-135">**GetRowHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | <span data-ttu-id="a7cc9-136">Метод</span><span class="sxs-lookup"><span data-stu-id="a7cc9-136">Method</span></span>      | <span data-ttu-id="a7cc9-137">Нет</span><span class="sxs-lookup"><span data-stu-id="a7cc9-137">None</span></span>  |



 

<span data-ttu-id="a7cc9-138">Этот шаблон элемента управления не имеет связанных свойств или событий.</span><span class="sxs-lookup"><span data-stu-id="a7cc9-138">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7cc9-139">См. также</span><span class="sxs-lookup"><span data-stu-id="a7cc9-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a7cc9-140">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a7cc9-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a7cc9-141">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="a7cc9-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="a7cc9-142">Шаблон элемента управления Table</span><span class="sxs-lookup"><span data-stu-id="a7cc9-142">Table Control Pattern</span></span>](uiauto-implementingtable.md)
</dt> <dt>

[<span data-ttu-id="a7cc9-143">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a7cc9-143">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="a7cc9-144">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a7cc9-144">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




