---
title: Шаблон элемента управления Виртуализедитем
description: Описывает правила и соглашения для реализации Ивиртуализедитемпровидер, включая сведения о свойствах и методах.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Виртуализедитем
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Виртуализедитем
- Модель автоматизации пользовательского интерфейса, Ивиртуализедитемпровидер
- IVirtualizedItemProvider
- реализация шаблонов элементов управления Виртуализедитем модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Виртуализедитем
- шаблоны элементов управления, Ивиртуализедитемпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Виртуализедитем
- шаблоны элементов управления, Виртуализедитем
- интерфейсы, Ивиртуализедитемпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259082"
---
# <a name="virtualizeditem-control-pattern"></a><span data-ttu-id="1bf32-113">Шаблон элемента управления Виртуализедитем</span><span class="sxs-lookup"><span data-stu-id="1bf32-113">VirtualizedItem Control Pattern</span></span>

<span data-ttu-id="1bf32-114">Описывает правила и соглашения для реализации [**ивиртуализедитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="1bf32-114">Describes guidelines and conventions for implementing [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), including information about properties and methods.</span></span> <span data-ttu-id="1bf32-115">Шаблон элемента управления **виртуализедитем** используется для поддержки виртуализированных элементов, которые представляют собой элементы, представленные элементами автоматизации заполнителя в дереве Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="1bf32-115">The **VirtualizedItem** control pattern is used to support virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.</span></span>

<span data-ttu-id="1bf32-116">Виртуализированные элементы могут включать элементы, извлеченные из элемента управления, который поддерживает шаблон элемента управления [ItemContainer](uiauto-implementingitemcontainer.md) , или виртуальный внедренный объект, полученный из элемента управления, поддерживающего шаблон элемента управления [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="1bf32-116">Virtualized items can include items retrieved from a control that supports the [ItemContainer](uiauto-implementingitemcontainer.md) control pattern, or a virtualized embedded object retrieved from a control that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span> <span data-ttu-id="1bf32-117">Заполнитель для виртуализированного элемента может не загрузить данные для всех свойств модели автоматизации пользовательского интерфейса, а также может возвращать [**UIA \_ E \_ елементнотаваилабле**](uiauto-error-codes.md) в ответ на запросы недоступных свойств.</span><span class="sxs-lookup"><span data-stu-id="1bf32-117">The placeholder for a virtualized item might not have loaded data for all UI Automation properties, and may return [**UIA\_E\_ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) in response to queries for properties that are not available.</span></span> <span data-ttu-id="1bf32-118">Шаблон элемента управления **виртуализедитем** предоставляет метод для реализации виртуального элемента, чтобы получить доступ к полной информации для элемента, а для элемента в дереве модели автоматизации пользовательского интерфейса можно создать полный элемент автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1bf32-118">The **VirtualizedItem** control pattern provides a method for realizing a virtual item so that full information is made available for the item, and a full automation element can be created for the item in the UI Automation tree.</span></span>

<span data-ttu-id="1bf32-119">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="1bf32-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1bf32-120">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="1bf32-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="1bf32-121">Обязательные члены для **ивиртуализедитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="1bf32-121">Required Members for **IVirtualizedItemProvider**</span></span>](#required-members-for-ivirtualizeditemprovider)
-   [<span data-ttu-id="1bf32-122">См. также</span><span class="sxs-lookup"><span data-stu-id="1bf32-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="1bf32-123">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="1bf32-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="1bf32-124">При реализации шаблона элемента управления **виртуализедитем** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="1bf32-124">When implementing the **VirtualizedItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="1bf32-125">Любой элемент заполнителя модели автоматизации пользовательского интерфейса, который может быть виртуализирован, должен поддерживать шаблон элемента управления **виртуализедитем** , предоставляя интерфейс [**ивиртуализедитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="1bf32-125">Any UI Automation placeholder element that can be virtualized must support the **VirtualizedItem** control pattern by exposing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>
-   <span data-ttu-id="1bf32-126">При вызове [**ивиртуализедитемпровидер:: реализовать**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) объект-заполнитель необходимо обновить с помощью полной реализации его свойств и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="1bf32-126">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the placeholder object must be updated with full implementations of its properties and control patterns.</span></span>
-   <span data-ttu-id="1bf32-127">При вызове [**ивиртуализедитемпровидер:: реализовать**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) поставщик может изменить окно просмотра таким образом, чтобы виртуализированный элемент поступил в представление.</span><span class="sxs-lookup"><span data-stu-id="1bf32-127">When [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) is called, the provider can change the viewport so that the virtualized item comes into view.</span></span> <span data-ttu-id="1bf32-128">Перевод элемента в представление не требуется; Однако невиртуализованные элементы не должны поддерживать метод [**искроллитемпровидер:: скроллинтовиев**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) .</span><span class="sxs-lookup"><span data-stu-id="1bf32-128">Bringing the item into view is not required; however, off-screen, non-virtualized items should support the [**IScrollItemProvider::ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) method.</span></span>

## <a name="required-members-for-ivirtualizeditemprovider"></a><span data-ttu-id="1bf32-129">Обязательные члены для **ивиртуализедитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="1bf32-129">Required Members for **IVirtualizedItemProvider**</span></span>

<span data-ttu-id="1bf32-130">Для реализации интерфейса [**ивиртуализедитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="1bf32-130">The following properties and methods are required for implementing the [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) interface.</span></span>



| <span data-ttu-id="1bf32-131">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="1bf32-131">Required members</span></span>                                           | <span data-ttu-id="1bf32-132">Тип члена</span><span class="sxs-lookup"><span data-stu-id="1bf32-132">Member type</span></span> | <span data-ttu-id="1bf32-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="1bf32-133">Notes</span></span> |
|------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="1bf32-134">**Повысить**</span><span class="sxs-lookup"><span data-stu-id="1bf32-134">**Realize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | <span data-ttu-id="1bf32-135">Метод</span><span class="sxs-lookup"><span data-stu-id="1bf32-135">Method</span></span>      | <span data-ttu-id="1bf32-136">Нет</span><span class="sxs-lookup"><span data-stu-id="1bf32-136">None</span></span>  |



 

<span data-ttu-id="1bf32-137">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="1bf32-137">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bf32-138">См. также</span><span class="sxs-lookup"><span data-stu-id="1bf32-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bf32-139">Реализация шаблона элемента управления ItemContainer модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="1bf32-139">Implementing the UI Automation ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
</dt> <dt>

[<span data-ttu-id="1bf32-140">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="1bf32-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="1bf32-141">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="1bf32-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="1bf32-142">Работа с виртуализированными элементами</span><span class="sxs-lookup"><span data-stu-id="1bf32-142">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




