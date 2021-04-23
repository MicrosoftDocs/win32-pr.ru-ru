---
title: Шаблон элемента управления Мултиплевиев
description: Описывает правила и соглашения для реализации IMultipleViewProvider, включая сведения о свойствах и методах.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Мултиплевиев
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Мултиплевиев
- Модель автоматизации пользовательского интерфейса, IMultipleViewProvider
- IMultipleViewProvider
- реализация шаблонов элементов управления Мултиплевиев модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Мултиплевиев
- шаблоны элементов управления, IMultipleViewProvider
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Мултиплевиев
- шаблоны элементов управления, Мултиплевиев
- интерфейсы, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411093"
---
# <a name="multipleview-control-pattern"></a><span data-ttu-id="797f3-113">Шаблон элемента управления Мултиплевиев</span><span class="sxs-lookup"><span data-stu-id="797f3-113">MultipleView Control Pattern</span></span>

<span data-ttu-id="797f3-114">Описывает правила и соглашения для реализации [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="797f3-114">Describes guidelines and conventions for implementing [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), including information about properties and methods.</span></span> <span data-ttu-id="797f3-115">Ссылки на дополнительные материалы перечислены в конце раздела.</span><span class="sxs-lookup"><span data-stu-id="797f3-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="797f3-116">Шаблон элемента управления **мултиплевиев** используется для поддержки элементов управления, которые предоставляют и могут переключаться между несколькими представлениями одних и тех же сведений или одного набора дочерних элементов управления.</span><span class="sxs-lookup"><span data-stu-id="797f3-116">The **MultipleView** control pattern is used to support controls that provide, and are able to switch between, multiple representations of the same information or the same set of child controls.</span></span>

<span data-ttu-id="797f3-117">Примеры элементов управления, которые могут представлять несколько представлений, включают представление списка (которое может отображать его содержимое в виде эскизов, плитки, значки или сведения), диаграммы Microsoft Excel (круговые, линейные, линейчатые, значения ячеек с формулами), документы Microsoft Word (обычная, веб-макет, макет печати, макет для чтения, контур), календарь Microsoft Outlook (год, месяц, неделя, день) и обложки проигрывателя Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="797f3-117">Examples of controls that can present multiple views include the list view (which can show its contents as thumbnails, tiles, icons, or details), Microsoft Excel charts (pie, line, bar, cell value with a formula), Microsoft Word documents (normal, web layout, print layout, reading layout, outline), Microsoft Outlook calendar (year, month, week, day), and Microsoft Windows Media Player skins.</span></span> <span data-ttu-id="797f3-118">Поддерживаемые представления определяются разработчиками элементов управления и относятся к конкретному элементу управления.</span><span class="sxs-lookup"><span data-stu-id="797f3-118">The supported views are determined by the control developer and are specific to each control.</span></span>

<span data-ttu-id="797f3-119">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="797f3-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="797f3-120">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="797f3-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="797f3-121">Обязательные члены для **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="797f3-121">Required Members for **IMultipleViewProvider**</span></span>](#required-members-for-imultipleviewprovider)
-   [<span data-ttu-id="797f3-122">См. также</span><span class="sxs-lookup"><span data-stu-id="797f3-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="797f3-123">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="797f3-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="797f3-124">При реализации шаблона элемента управления **мултиплевиев** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="797f3-124">When implementing the **MultipleView** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="797f3-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) также должен быть реализован в контейнере, который управляет текущим представлением, если он отличается от элемента управления, предоставляющего текущее представление.</span><span class="sxs-lookup"><span data-stu-id="797f3-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) should also be implemented on a container that manages the current view if it is different from a control that provides the current view.</span></span> <span data-ttu-id="797f3-126">Например, проводник Windows содержит элемент управления "список" для текущего содержимого папки, в то время как представление элемента управления управляется из приложения проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="797f3-126">For example, Windows Explorer contains a list control for the current folder content while the view for the control is managed from the Windows Explorer application.</span></span>
-   <span data-ttu-id="797f3-127">Элемент управления, который может сортировать свое содержимое, не считается поддерживающим несколько представлений.</span><span class="sxs-lookup"><span data-stu-id="797f3-127">A control that is able to sort its content is not considered to support multiple views.</span></span>
-   <span data-ttu-id="797f3-128">Коллекция представлений должна быть идентичной во всех экземплярах.</span><span class="sxs-lookup"><span data-stu-id="797f3-128">The collection of views must be identical across instances.</span></span>
-   <span data-ttu-id="797f3-129">Имена представлений должны быть подходящими для использования в тексте для распознавания речи, шрифта Брайля и других приложений, пригодных для восприятия.</span><span class="sxs-lookup"><span data-stu-id="797f3-129">View names must be suitable for use in text to speech, Braille, and other human-readable applications.</span></span>

## <a name="required-members-for-imultipleviewprovider"></a><span data-ttu-id="797f3-130">Обязательные члены для **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="797f3-130">Required Members for **IMultipleViewProvider**</span></span>

<span data-ttu-id="797f3-131">Для реализации интерфейса [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="797f3-131">The following properties and methods are required for implementing the [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) interface.</span></span>



| <span data-ttu-id="797f3-132">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="797f3-132">Required members</span></span>                                                            | <span data-ttu-id="797f3-133">Тип члена</span><span class="sxs-lookup"><span data-stu-id="797f3-133">Member type</span></span> | <span data-ttu-id="797f3-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="797f3-134">Notes</span></span> |
|-----------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="797f3-135">**куррентвиев**</span><span class="sxs-lookup"><span data-stu-id="797f3-135">**CurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | <span data-ttu-id="797f3-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="797f3-136">Property</span></span>    | <span data-ttu-id="797f3-137">Нет</span><span class="sxs-lookup"><span data-stu-id="797f3-137">None</span></span>  |
| [<span data-ttu-id="797f3-138">**жетсуппортедвиевс**</span><span class="sxs-lookup"><span data-stu-id="797f3-138">**GetSupportedViews**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | <span data-ttu-id="797f3-139">Метод</span><span class="sxs-lookup"><span data-stu-id="797f3-139">Method</span></span>      | <span data-ttu-id="797f3-140">Нет</span><span class="sxs-lookup"><span data-stu-id="797f3-140">None</span></span>  |
| [<span data-ttu-id="797f3-141">**жетвиевнаме**</span><span class="sxs-lookup"><span data-stu-id="797f3-141">**GetViewName**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | <span data-ttu-id="797f3-142">Метод</span><span class="sxs-lookup"><span data-stu-id="797f3-142">Method</span></span>      | <span data-ttu-id="797f3-143">Нет</span><span class="sxs-lookup"><span data-stu-id="797f3-143">None</span></span>  |
| [<span data-ttu-id="797f3-144">**сеткуррентвиев**</span><span class="sxs-lookup"><span data-stu-id="797f3-144">**SetCurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | <span data-ttu-id="797f3-145">Метод</span><span class="sxs-lookup"><span data-stu-id="797f3-145">Method</span></span>      | <span data-ttu-id="797f3-146">Нет</span><span class="sxs-lookup"><span data-stu-id="797f3-146">None</span></span>  |



 

<span data-ttu-id="797f3-147">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="797f3-147">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="797f3-148">См. также</span><span class="sxs-lookup"><span data-stu-id="797f3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="797f3-149">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="797f3-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="797f3-150">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="797f3-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="797f3-151">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="797f3-151">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="797f3-152">Шаблон элемента управления ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="797f3-152">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




