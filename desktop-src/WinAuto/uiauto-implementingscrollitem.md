---
title: Шаблон элемента управления Скроллитем
description: Описывает правила и соглашения для реализации Искроллитемпровидер, включая сведения о методах.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Скроллитем
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Скроллитем
- Модель автоматизации пользовательского интерфейса, Искроллитемпровидер
- IScrollItemProvider
- реализация шаблонов элементов управления Скроллитем модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Скроллитем
- шаблоны элементов управления, Искроллитемпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Скроллитем
- шаблоны элементов управления, Скроллитем
- интерфейсы, Искроллитемпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258553"
---
# <a name="scrollitem-control-pattern"></a><span data-ttu-id="b2230-113">Шаблон элемента управления Скроллитем</span><span class="sxs-lookup"><span data-stu-id="b2230-113">ScrollItem Control Pattern</span></span>

<span data-ttu-id="b2230-114">Описывает правила и соглашения для реализации [**искроллитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), включая сведения о методах.</span><span class="sxs-lookup"><span data-stu-id="b2230-114">Describes guidelines and conventions for implementing [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), including information about methods.</span></span> <span data-ttu-id="b2230-115">Шаблон элемента управления **скроллитем** используется для поддержки отдельных дочерних элементов управления контейнеров, реализующих [**искроллпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span><span class="sxs-lookup"><span data-stu-id="b2230-115">The **ScrollItem** control pattern is used to support individual child controls of containers that implement [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider).</span></span> <span data-ttu-id="b2230-116">Наличие шаблона элемента управления **скроллитем** в элементе управления не подразумевает, что его контейнер или любой предок должны реализовывать шаблон элемента управления **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="b2230-116">The existence of the **ScrollItem** control pattern on a control does not imply that its container or any ancestor must implement the **Scroll** control pattern.</span></span>

<span data-ttu-id="b2230-117">Когда контейнер реализует шаблон элемента управления **Scroll** , шаблон элемента управления **скроллитем** выступает в качестве коммуникационного канала между дочерним элементом управления и его контейнером, чтобы гарантировать, что контейнер может изменить видимое в настоящий момент содержимое (или область) в своем окне просмотра для отображения дочернего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b2230-117">When the container does implement the **Scroll** control pattern, the **ScrollItem** control pattern acts as a communication channel between a child control and its container to ensure that the container can change the currently visible content (or region) within its viewport to display the child control.</span></span> <span data-ttu-id="b2230-118">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="b2230-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="b2230-119">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="b2230-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b2230-120">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="b2230-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="b2230-121">Обязательные члены для **искроллитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="b2230-121">Required Members for **IScrollItemProvider**</span></span>](#required-members-for-iscrollitemprovider)
-   [<span data-ttu-id="b2230-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b2230-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="b2230-123">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="b2230-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="b2230-124">При реализации шаблона элемента управления **скроллитем** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="b2230-124">When implementing the **ScrollItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="b2230-125">Элементы, содержащиеся в элементе управления [Window](uiauto-supportwindowcontroltype.md) или **Canvas** , не обязательно должны реализовывать интерфейс [**искроллитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="b2230-125">Items contained within a [Window](uiauto-supportwindowcontroltype.md) or **Canvas** control are not required to implement the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span> <span data-ttu-id="b2230-126">Однако в качестве альтернативы необходимо предоставить допустимое расположение для свойства [**иуиаутоматионелемент:: куррентбаундингректангле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (или [**качедбаундингректангле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)).</span><span class="sxs-lookup"><span data-stu-id="b2230-126">As an alternative, however, they must expose a valid location for the [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (or [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) property.</span></span> <span data-ttu-id="b2230-127">Это позволит клиентскому приложению Microsoft UI Automation использовать методы шаблона элемента управления [**иуиаутоматионскроллпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) в контейнере для вывода дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="b2230-127">This will allow a Microsoft UI Automation client application to use the [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) control pattern methods on the container to display the child item.</span></span>

## <a name="required-members-for-iscrollitemprovider"></a><span data-ttu-id="b2230-128">Обязательные члены для **искроллитемпровидер**</span><span class="sxs-lookup"><span data-stu-id="b2230-128">Required Members for **IScrollItemProvider**</span></span>

<span data-ttu-id="b2230-129">Для реализации интерфейса [**искроллитемпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) требуется следующий метод.</span><span class="sxs-lookup"><span data-stu-id="b2230-129">The following method is required for implementing the [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) interface.</span></span>



| <span data-ttu-id="b2230-130">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="b2230-130">Required members</span></span>                                                    | <span data-ttu-id="b2230-131">Тип члена</span><span class="sxs-lookup"><span data-stu-id="b2230-131">Member type</span></span> | <span data-ttu-id="b2230-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2230-132">Notes</span></span> |
|---------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="b2230-133">**скроллинтовиев**</span><span class="sxs-lookup"><span data-stu-id="b2230-133">**ScrollIntoView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | <span data-ttu-id="b2230-134">Метод</span><span class="sxs-lookup"><span data-stu-id="b2230-134">Method</span></span>      | <span data-ttu-id="b2230-135">Нет</span><span class="sxs-lookup"><span data-stu-id="b2230-135">None</span></span>  |



 

<span data-ttu-id="b2230-136">Этот шаблон элемента управления не имеет связанных свойств или событий.</span><span class="sxs-lookup"><span data-stu-id="b2230-136">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2230-137">См. также</span><span class="sxs-lookup"><span data-stu-id="b2230-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2230-138">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="b2230-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="b2230-139">Шаблон элемента управления Selection</span><span class="sxs-lookup"><span data-stu-id="b2230-139">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
</dt> <dt>

[<span data-ttu-id="b2230-140">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="b2230-140">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="b2230-141">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="b2230-141">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




