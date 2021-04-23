---
title: Шаблон элемента управления Table
description: Описывает правила и соглашения для реализации Итаблепровидер, включая сведения о свойствах и методах. Шаблон элемента управления Table используется для поддержки элементов управления, которые действуют как контейнеры для коллекции дочерних элементов.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Table
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Table
- Модель автоматизации пользовательского интерфейса, Итаблепровидер
- ITableProvider
- реализация шаблонов элементов управления таблицы модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Table
- шаблоны элементов управления, Итаблепровидер
- шаблоны элементов управления, реализация таблицы автоматизации пользовательского интерфейса
- шаблоны элементов управления, таблица
- интерфейсы, Итаблепровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104563185"
---
# <a name="table-control-pattern"></a><span data-ttu-id="403e1-114">Шаблон элемента управления Table</span><span class="sxs-lookup"><span data-stu-id="403e1-114">Table Control Pattern</span></span>

<span data-ttu-id="403e1-115">Описывает правила и соглашения для реализации [**итаблепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="403e1-115">Describes guidelines and conventions for implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), including information about properties and methods.</span></span> <span data-ttu-id="403e1-116">Шаблон элемента управления **Table** используется для поддержки элементов управления, которые действуют как контейнеры для коллекции дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="403e1-116">The **Table** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="403e1-117">Дочерние элементы элемента Container должны реализовывать [**итаблеитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) и быть организованы в двухмерной логической системе координат, которую можно просмотреть по строкам и столбцам.</span><span class="sxs-lookup"><span data-stu-id="403e1-117">The children of the container element must implement [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="403e1-118">Этот шаблон элемента управления является аналогом [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) с различием того, что любой элемент управления, реализующий [**итаблепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) , должен также предоставлять связь заголовка столбца и/или строки для каждого дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="403e1-118">This control pattern is analogous to [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) with the distinction that any control implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) must also expose a column and/or row header relationship for each child element.</span></span> <span data-ttu-id="403e1-119">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="403e1-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="403e1-120">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="403e1-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="403e1-121">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="403e1-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="403e1-122">Обязательные члены для **итаблепровидер**</span><span class="sxs-lookup"><span data-stu-id="403e1-122">Required Members for **ITableProvider**</span></span>](#required-members-for-itableprovider)
-   [<span data-ttu-id="403e1-123">См. также</span><span class="sxs-lookup"><span data-stu-id="403e1-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="403e1-124">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="403e1-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="403e1-125">При реализации шаблона элемента управления **Table** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="403e1-125">When implementing the **Table** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="403e1-126">Доступ к содержимому отдельных ячеек осуществляется посредством двухмерной логической системы координат или массива, предоставляемого требуемой параллельной реализацией [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span><span class="sxs-lookup"><span data-stu-id="403e1-126">Access to the content of individual cells is through a two-dimensional logical coordinate system or array provided by the required, concurrent implementation of [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>
-   <span data-ttu-id="403e1-127">Заголовок столбца или строки может содержаться в объекте таблицы или быть отдельным объектом заголовка, связанным с объектом таблицы.</span><span class="sxs-lookup"><span data-stu-id="403e1-127">A column or row header can be contained within a table object or be a separate header object that is associated with a table object.</span></span>
-   <span data-ttu-id="403e1-128">Заголовки столбцов и строк могут включать и основной заголовок, и любые поддерживаемые заголовки.</span><span class="sxs-lookup"><span data-stu-id="403e1-128">Column and row headers may include both a primary header as well as any supporting headers.</span></span>
    > [!Note]  
    > <span data-ttu-id="403e1-129">Эта концепция станет очевидной в электронной таблице Microsoft Excel, где пользователь определил столбец с **именем** .</span><span class="sxs-lookup"><span data-stu-id="403e1-129">This concept becomes evident in a Microsoft Excel spreadsheet where a user has defined a **First name** column.</span></span> <span data-ttu-id="403e1-130">Этот столбец теперь содержит два заголовка, включая **первый заголовок имени** , определенный пользователем, и буквенно-цифровой обозначение для этого столбца, назначенного приложением.</span><span class="sxs-lookup"><span data-stu-id="403e1-130">This column now has two headers, including the **First name** header defined by the user, and the alphanumeric designation for that column assigned by the application.</span></span>

     

-   <span data-ttu-id="403e1-131">См. раздел [шаблон элемента управления Grid](uiauto-implementinggrid.md) для связанных функций сетки.</span><span class="sxs-lookup"><span data-stu-id="403e1-131">See [Grid Control Pattern](uiauto-implementinggrid.md) for related grid functionality.</span></span>

    <span data-ttu-id="403e1-132">На следующем рисунке показана таблица со сложными заголовками столбцов.</span><span class="sxs-lookup"><span data-stu-id="403e1-132">The following image shows a table with complex column headers.</span></span>

    ![Таблица со сложными заголовками столбцов](images/uia-valuepattern-colorpicker.jpg)

    <span data-ttu-id="403e1-134">На следующем рисунке показана таблица с неоднозначным свойством [**итаблепровидер:: роворколумнмажор**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) .</span><span class="sxs-lookup"><span data-stu-id="403e1-134">The following image shows a table with an ambiguous [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) property.</span></span>

    ![Таблица с неоднозначным свойством роворколумнмажор](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a><span data-ttu-id="403e1-136">Обязательные члены для **итаблепровидер**</span><span class="sxs-lookup"><span data-stu-id="403e1-136">Required Members for **ITableProvider**</span></span>

<span data-ttu-id="403e1-137">Для реализации интерфейса [**итаблепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="403e1-137">The following properties and methods are required for implementing the [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) interface.</span></span>



| <span data-ttu-id="403e1-138">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="403e1-138">Required members</span></span>                                                   | <span data-ttu-id="403e1-139">Тип члена</span><span class="sxs-lookup"><span data-stu-id="403e1-139">Member type</span></span> | <span data-ttu-id="403e1-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="403e1-140">Notes</span></span> |
|--------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="403e1-141">**роворколумнмажор**</span><span class="sxs-lookup"><span data-stu-id="403e1-141">**RowOrColumnMajor**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | <span data-ttu-id="403e1-142">Свойство</span><span class="sxs-lookup"><span data-stu-id="403e1-142">Property</span></span>    | <span data-ttu-id="403e1-143">Нет</span><span class="sxs-lookup"><span data-stu-id="403e1-143">None</span></span>  |
| [<span data-ttu-id="403e1-144">**жетколумнхеадерс**</span><span class="sxs-lookup"><span data-stu-id="403e1-144">**GetColumnHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | <span data-ttu-id="403e1-145">Метод</span><span class="sxs-lookup"><span data-stu-id="403e1-145">Method</span></span>      | <span data-ttu-id="403e1-146">Нет</span><span class="sxs-lookup"><span data-stu-id="403e1-146">None</span></span>  |
| [<span data-ttu-id="403e1-147">**жетровхеадерс**</span><span class="sxs-lookup"><span data-stu-id="403e1-147">**GetRowHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | <span data-ttu-id="403e1-148">Метод</span><span class="sxs-lookup"><span data-stu-id="403e1-148">Method</span></span>      | <span data-ttu-id="403e1-149">Нет</span><span class="sxs-lookup"><span data-stu-id="403e1-149">None</span></span>  |



 

<span data-ttu-id="403e1-150">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="403e1-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="403e1-151">См. также</span><span class="sxs-lookup"><span data-stu-id="403e1-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="403e1-152">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="403e1-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="403e1-153">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="403e1-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="403e1-154">Шаблон элемента управления TableItem</span><span class="sxs-lookup"><span data-stu-id="403e1-154">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
</dt> <dt>

[<span data-ttu-id="403e1-155">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="403e1-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="403e1-156">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="403e1-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




