---
title: Шаблон элемента управления Спреадшититем
description: Описывает правила и соглашения для реализации Испреадшититемпровидер, включая сведения о свойствах и методах.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Спреадшититем
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Спреадшититем
- Модель автоматизации пользовательского интерфейса, Испреадшититемпровидер
- ISpreadsheetItemProvider
- Реализация шаблона элемента управления Спреадшититем модели автоматизации пользовательского интерфейса
- Шаблон элемента управления Спреадшититем
- шаблоны элементов управления, Испреадшититемпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Спреадшититем
- шаблоны элементов управления, Спреадшититем
- интерфейсы, Испреадшититемпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070492"
---
# <a name="spreadsheetitem-control-pattern"></a><span data-ttu-id="fae6c-113">Шаблон элемента управления Спреадшититем</span><span class="sxs-lookup"><span data-stu-id="fae6c-113">SpreadsheetItem Control Pattern</span></span>

<span data-ttu-id="fae6c-114">Описывает правила и соглашения для реализации [**испреадшититемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="fae6c-114">Describes guidelines and conventions for implementing [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), including information about properties and methods.</span></span> <span data-ttu-id="fae6c-115">Шаблон элемента управления **спреадшититем** используется для предоставления свойств ячейки электронной таблицы или другого документа, основанного на сетке.</span><span class="sxs-lookup"><span data-stu-id="fae6c-115">The **SpreadsheetItem** control pattern is used to expose the properties of a cell in a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="fae6c-116">Шаблон элемента управления **спреадшититем** тесно связан с шаблоном элемента управления [GridItem](uiauto-implementinggriditem.md) . элементы управления, реализующие шаблон элемента управления **спреадшититем** , должны также реализовать шаблон элемента управления GridItem.</span><span class="sxs-lookup"><span data-stu-id="fae6c-116">The **SpreadsheetItem** control pattern is closely related to the [GridItem](uiauto-implementinggriditem.md) control pattern; controls that implement the **SpreadsheetItem** control pattern should also implement the GridItem control pattern.</span></span> <span data-ttu-id="fae6c-117">Элементы управления могут также реализовывать шаблон элемента управления [TableItem](uiauto-implementingtableitem.md) , если это уместно.</span><span class="sxs-lookup"><span data-stu-id="fae6c-117">Controls can also implement the [TableItem](uiauto-implementingtableitem.md) control pattern, if appropriate.</span></span> <span data-ttu-id="fae6c-118">Примеры элементов управления, реализующих эти шаблоны элементов управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="fae6c-118">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="fae6c-119">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="fae6c-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fae6c-120">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="fae6c-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="fae6c-121">Обязательные члены для **испреадшититемпровидер**</span><span class="sxs-lookup"><span data-stu-id="fae6c-121">Required Members for **ISpreadsheetItemProvider**</span></span>](#required-members-for-ispreadsheetitemprovider)
-   [<span data-ttu-id="fae6c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="fae6c-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="fae6c-123">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="fae6c-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="fae6c-124">При реализации шаблона элемента управления **спреадшититем** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="fae6c-124">When implementing the **SpreadsheetItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="fae6c-125">При реализации методов [**испреадшититемпровидер:: жетаннотатионобжектс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) и [**Испреадшититемпровидер:: жетаннотатионтипес**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) обратитесь к документации по [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="fae6c-125">When implementing the [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) and [**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) methods, please refer to the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) documentation.</span></span> <span data-ttu-id="fae6c-126">Эти методы возвращают массивы, чтобы предоставить поставщикам возможность поддерживать несколько заметок в одной ячейке.</span><span class="sxs-lookup"><span data-stu-id="fae6c-126">These methods both return arrays to enable providers to support multiple annotations on a single cell.</span></span>
-   <span data-ttu-id="fae6c-127">Некоторые типы заметок не нуждаются в полной реализации интерфейса [**ианнотатионпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="fae6c-127">Some kinds of annotations do not require a full implementation of the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) interface.</span></span> <span data-ttu-id="fae6c-128">Например, можно представить простой индикатор орфографической ошибки, [**жетаннотатионтипес**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) возвратить идентификатор атрибута текста [**аннотатионтипе \_ спеллинжеррор**](uiauto-annotation-type-identifiers.md), а [**жетаннотатионобжектс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) возвращать значение null.</span><span class="sxs-lookup"><span data-stu-id="fae6c-128">For example, a simple spelling-error indicator could be represented by having [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) return a text attribute identifier of [**AnnotationType\_SpellingError**](uiauto-annotation-type-identifiers.md), and having [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) return a null value.</span></span>

## <a name="required-members-for-ispreadsheetitemprovider"></a><span data-ttu-id="fae6c-129">Обязательные члены для **испреадшититемпровидер**</span><span class="sxs-lookup"><span data-stu-id="fae6c-129">Required Members for **ISpreadsheetItemProvider**</span></span>

<span data-ttu-id="fae6c-130">Для реализации интерфейса [**испреадшититемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="fae6c-130">The following properties and methods are required for implementing the [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>



| <span data-ttu-id="fae6c-131">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="fae6c-131">Required members</span></span>                                                                         | <span data-ttu-id="fae6c-132">Тип члена</span><span class="sxs-lookup"><span data-stu-id="fae6c-132">Member type</span></span> | <span data-ttu-id="fae6c-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="fae6c-133">Notes</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fae6c-134">**Формула**</span><span class="sxs-lookup"><span data-stu-id="fae6c-134">**Formula**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | <span data-ttu-id="fae6c-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="fae6c-135">Property</span></span>    | <span data-ttu-id="fae6c-136">Реализовать отдельное свойство [**формулы**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) необходимо потому, что свойство [value](value-property.md) ячейки обычно возвращает вычисленное значение ячейки.</span><span class="sxs-lookup"><span data-stu-id="fae6c-136">Implementing a separate [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) property is necessary because a cell’s [Value](value-property.md) property typically returns the computed value of the cell.</span></span> <span data-ttu-id="fae6c-137">Если формула не задана, свойство **формулы** должно иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="fae6c-137">The **Formula** property should be **NULL** if no formula is set.</span></span> |
| [<span data-ttu-id="fae6c-138">**жетаннотатионобжектс**</span><span class="sxs-lookup"><span data-stu-id="fae6c-138">**GetAnnotationObjects**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | <span data-ttu-id="fae6c-139">Метод</span><span class="sxs-lookup"><span data-stu-id="fae6c-139">Method</span></span>      | <span data-ttu-id="fae6c-140">Возвращает массив поставщиков элементов, которые ссылаются на заметки, связанные с этой ячейкой.</span><span class="sxs-lookup"><span data-stu-id="fae6c-140">Returns an array of element providers that refer to the annotations linked to this cell.</span></span> <span data-ttu-id="fae6c-141">Указатели в массиве могут иметь значение null, если в заметке отсутствует связанный поставщик.</span><span class="sxs-lookup"><span data-stu-id="fae6c-141">Pointers within the array can be null if an annotation does not have a linked provider.</span></span>                                                                                                       |
| [<span data-ttu-id="fae6c-142">**жетаннотатионтипес**</span><span class="sxs-lookup"><span data-stu-id="fae6c-142">**GetAnnotationTypes**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | <span data-ttu-id="fae6c-143">Метод</span><span class="sxs-lookup"><span data-stu-id="fae6c-143">Method</span></span>      | <span data-ttu-id="fae6c-144">Возвращает массив идентификаторов типа аннотации, описывающих заметки в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="fae6c-144">Returns an array of annotation type identifiers that describe the annotations on this cell.</span></span> <span data-ttu-id="fae6c-145">Размер массива должен совпадать с размером массива, возвращаемого функцией [**жетаннотатионобжектс**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span><span class="sxs-lookup"><span data-stu-id="fae6c-145">The array must be the same size as the array returned by [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span></span>                                         |



 

<span data-ttu-id="fae6c-146">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="fae6c-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fae6c-147">См. также</span><span class="sxs-lookup"><span data-stu-id="fae6c-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fae6c-148">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="fae6c-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fae6c-149">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="fae6c-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="fae6c-150">Шаблон элемента управления электронной таблицей</span><span class="sxs-lookup"><span data-stu-id="fae6c-150">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
</dt> <dt>

[<span data-ttu-id="fae6c-151">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fae6c-151">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="fae6c-152">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fae6c-152">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 