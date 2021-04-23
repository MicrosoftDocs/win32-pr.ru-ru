---
title: Шаблон элемента управления электронной таблицей
description: Описывает правила и соглашения для реализации Испреадшитпровидер, включая сведения о методах.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления электронной таблицы
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления электронной таблицы
- Модель автоматизации пользовательского интерфейса, Испреадшитпровидер
- ISpreadsheetProvider
- Реализация шаблона элемента управления электронной таблицы модели автоматизации пользовательского интерфейса
- шаблон элемента управления электронной таблицей
- шаблоны элементов управления, Испреадшитпровидер
- шаблоны элементов управления, реализация электронной таблицы модели автоматизации пользовательского интерфейса
- шаблоны элементов управления, электронная таблица
- интерфейсы, Испреадшитпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338329"
---
# <a name="spreadsheet-control-pattern"></a><span data-ttu-id="84aa4-113">Шаблон элемента управления электронной таблицей</span><span class="sxs-lookup"><span data-stu-id="84aa4-113">Spreadsheet Control Pattern</span></span>

<span data-ttu-id="84aa4-114">Описывает правила и соглашения для реализации [**испреадшитпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), включая сведения о методах.</span><span class="sxs-lookup"><span data-stu-id="84aa4-114">Describes guidelines and conventions for implementing [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), including information about methods.</span></span> <span data-ttu-id="84aa4-115">Ссылки на дополнительные материалы перечислены в конце раздела.</span><span class="sxs-lookup"><span data-stu-id="84aa4-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="84aa4-116">Шаблон элемента управления **электронной таблицы** используется для представления содержимого электронной таблицы или другого документа, основанного на сетке.</span><span class="sxs-lookup"><span data-stu-id="84aa4-116">The **Spreadsheet** control pattern is used to expose the contents of a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="84aa4-117">Шаблон элемента управления **электронной таблицы** тесно связан с шаблоном элемента управления [Grid](uiauto-implementinggrid.md) . элементы управления, реализующие шаблон элемента управления **электронной таблицы** , должны также реализовать шаблон элемента управления Grid.</span><span class="sxs-lookup"><span data-stu-id="84aa4-117">The **Spreadsheet** control pattern is closely related to the [Grid](uiauto-implementinggrid.md) control pattern; controls that implement the **Spreadsheet** control pattern should also implement the Grid control pattern.</span></span> <span data-ttu-id="84aa4-118">Элементы управления могут также реализовывать шаблон элемента управления [Table](uiauto-implementingtable.md) , если это уместно.</span><span class="sxs-lookup"><span data-stu-id="84aa4-118">Controls can also implement the [Table](uiauto-implementingtable.md) control pattern, if appropriate.</span></span> <span data-ttu-id="84aa4-119">Примеры элементов управления, реализующих эти шаблоны элементов управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="84aa4-119">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="84aa4-120">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="84aa4-120">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="84aa4-121">При реализации шаблона элемента управления **электронной таблицы** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="84aa4-121">When implementing the **Spreadsheet** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="84aa4-122">Если электронная таблица реализует интерфейс [**испреадшитпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) , ее ячейки должны реализовывать интерфейс [**испреадшититемпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="84aa4-122">If a spreadsheet implements the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface, its cells must implement the [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>
-   <span data-ttu-id="84aa4-123">Метод [**испреадшитпровидер:: жетитембинаме**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) предназначен для обеспечения того же вида навигации, который может быть предоставлен приложением при **переходе к функции Label** .</span><span class="sxs-lookup"><span data-stu-id="84aa4-123">The [**ISpreadsheetProvider::GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) method is intended to provide the same kind of navigation that an application might supply with a **Jump to Label** feature.</span></span> <span data-ttu-id="84aa4-124">Во многих программах электронной таблицы для отдельных ячеек может быть задано понятное имя или подпись.</span><span class="sxs-lookup"><span data-stu-id="84aa4-124">Many spreadsheet programs let specific cells be given a friendly name or label.</span></span> <span data-ttu-id="84aa4-125">**Жетитембинаме** позволяет клиенту искать ячейку на основе ее понятного имени.</span><span class="sxs-lookup"><span data-stu-id="84aa4-125">**GetItemByName** enables the client to look up a cell based on its friendly name.</span></span> <span data-ttu-id="84aa4-126">Этот метод не должен извлекать ячейки, содержащие текст с именем, так как результаты могут быть очень неоднозначными.</span><span class="sxs-lookup"><span data-stu-id="84aa4-126">This method should not retrieve any cells that contain the name text because the results can be highly ambiguous.</span></span> <span data-ttu-id="84aa4-127">Если программа электронной таблицы позволяет нескольким ячейкам в одной таблице иметь одинаковое понятное имя или метку, поведение автоматизации пользовательского интерфейса Майкрософт не определено.</span><span class="sxs-lookup"><span data-stu-id="84aa4-127">If the spreadsheet program allows multiple cells in the same a spreadsheet to have the same friendly name or label, the Microsoft UI Automation behavior is undefined.</span></span>

## <a name="required-members-for-ispreadsheetprovider"></a><span data-ttu-id="84aa4-128">Обязательные члены для **испреадшитпровидер**</span><span class="sxs-lookup"><span data-stu-id="84aa4-128">Required Members for **ISpreadsheetProvider**</span></span>

<span data-ttu-id="84aa4-129">Для реализации интерфейса [**испреадшитпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) требуется следующий метод.</span><span class="sxs-lookup"><span data-stu-id="84aa4-129">The following method is required for implementing the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface.</span></span>



| <span data-ttu-id="84aa4-130">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="84aa4-130">Required members</span></span>                                                       | <span data-ttu-id="84aa4-131">Тип члена</span><span class="sxs-lookup"><span data-stu-id="84aa4-131">Member type</span></span> | <span data-ttu-id="84aa4-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="84aa4-132">Notes</span></span> |
|------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="84aa4-133">**жетитембинаме**</span><span class="sxs-lookup"><span data-stu-id="84aa4-133">**GetItemByName**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | <span data-ttu-id="84aa4-134">Метод</span><span class="sxs-lookup"><span data-stu-id="84aa4-134">Method</span></span>      | <span data-ttu-id="84aa4-135">Нет</span><span class="sxs-lookup"><span data-stu-id="84aa4-135">None</span></span>  |



 

<span data-ttu-id="84aa4-136">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="84aa4-136">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84aa4-137">См. также</span><span class="sxs-lookup"><span data-stu-id="84aa4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84aa4-138">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="84aa4-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="84aa4-139">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="84aa4-139">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="84aa4-140">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="84aa4-140">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 