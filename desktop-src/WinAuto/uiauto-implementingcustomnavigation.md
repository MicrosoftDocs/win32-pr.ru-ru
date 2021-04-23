---
title: Шаблон элемента управления Кустомнавигатион
description: Описывает правила и соглашения для реализации интерфейса Икустомнавигатионпровидер, включая сведения о свойствах и методах.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253220"
---
# <a name="customnavigation-control-pattern"></a><span data-ttu-id="4d3f9-103">Шаблон элемента управления Кустомнавигатион</span><span class="sxs-lookup"><span data-stu-id="4d3f9-103">CustomNavigation Control Pattern</span></span>

<span data-ttu-id="4d3f9-104">Описывает правила и соглашения для реализации интерфейса **икустомнавигатионпровидер** , включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="4d3f9-104">Describes guidelines and conventions for implementing the **ICustomNavigationProvider** interface, including information about properties and methods.</span></span> <span data-ttu-id="4d3f9-105">Шаблон элемента управления **кустомнавигатион** используется для обеспечения настраиваемой навигации между элементами управления в структурах, аналогичных иерархии, таких как элементы списка, маркированные списки, нумерованные списки и заголовки.</span><span class="sxs-lookup"><span data-stu-id="4d3f9-105">The **CustomNavigation** control pattern is used to enable custom navigation between controls in hierarchy-like structures such as list items, bulleted lists, numbered lists and headings.</span></span> <span data-ttu-id="4d3f9-106">Это позволяет поставщикам описывать структуры или определять связи перемещения, используя только элемент, а не только содержащий его элемент управления.</span><span class="sxs-lookup"><span data-stu-id="4d3f9-106">This enables providers to describe structures or define the navigable relationships using the element alone and not just the containing control.</span></span>

<span data-ttu-id="4d3f9-107">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="4d3f9-107">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="4d3f9-108">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="4d3f9-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4d3f9-109">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="4d3f9-109">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="4d3f9-110">Обязательные члены для **икустомнавигатионпровидер**</span><span class="sxs-lookup"><span data-stu-id="4d3f9-110">Required Members for **ICustomNavigationProvider**</span></span>](#required-members-for-icustomnavigationprovider)
-   [<span data-ttu-id="4d3f9-111">См. также</span><span class="sxs-lookup"><span data-stu-id="4d3f9-111">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="4d3f9-112">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="4d3f9-112">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="4d3f9-113">При реализации поставщика **кустомнавигатион** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="4d3f9-113">When implementing the **CustomNavigation** provider, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="4d3f9-114">Значения свойств для **поситионинсет**, **sizeof** и **Level** являются целочисленными значениями, основанными на единицах.</span><span class="sxs-lookup"><span data-stu-id="4d3f9-114">Property values for **PositionInSet**, **SizeOfSet**, and **Level** are one-based integer values.</span></span>
-   <span data-ttu-id="4d3f9-115">**Икустомнавигатионпровидер** не обеспечивает активную манипуляцию с элементом управления, например перемещением позиций, добавлением и удалением элементов, а также повышением и понижением уровней.</span><span class="sxs-lookup"><span data-stu-id="4d3f9-115">**ICustomNavigationProvider** does not provide for active manipulation of the control such as moving positions, adding and removing items, or promoting and demoting levels.</span></span>
-   <span data-ttu-id="4d3f9-116">Элементы управления, которые реализуют **икустомнавигатионпровидер** , обычно имеют иерархическую структуру, но могут пропускать уровни с помощью метода **navigate** .</span><span class="sxs-lookup"><span data-stu-id="4d3f9-116">Controls that implement **ICustomNavigationProvider** typically have a hierarchical structure, but can skip levels by using the **Navigate** method.</span></span> <span data-ttu-id="4d3f9-117">Для шаблона требуются свойства **поситионинсет**, **sizeof** и **Level** .</span><span class="sxs-lookup"><span data-stu-id="4d3f9-117">The properties **PositionInSet**, **SizeOfSet**, and **Level** are required on the pattern.</span></span>

## <a name="required-members-for-icustomnavigationprovider"></a><span data-ttu-id="4d3f9-118">Обязательные члены для **икустомнавигатионпровидер**</span><span class="sxs-lookup"><span data-stu-id="4d3f9-118">Required Members for **ICustomNavigationProvider**</span></span>

<span data-ttu-id="4d3f9-119">Для реализации интерфейса **икустомнавигатионпровидер** требуются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4d3f9-119">The following properties are required for implementing the **ICustomNavigationProvider** interface.</span></span>



| <span data-ttu-id="4d3f9-120">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="4d3f9-120">Required members</span></span>                                                                  | <span data-ttu-id="4d3f9-121">Тип члена</span><span class="sxs-lookup"><span data-stu-id="4d3f9-121">Member type</span></span> | <span data-ttu-id="4d3f9-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d3f9-122">Notes</span></span>                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d3f9-123">**качедлевел**</span><span class="sxs-lookup"><span data-stu-id="4d3f9-123">**CachedLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | <span data-ttu-id="4d3f9-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="4d3f9-124">Property</span></span>    | <span data-ttu-id="4d3f9-125">Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="4d3f9-125">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="4d3f9-126">**качедпоситионинсет**</span><span class="sxs-lookup"><span data-stu-id="4d3f9-126">**CachedPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | <span data-ttu-id="4d3f9-127">Свойство</span><span class="sxs-lookup"><span data-stu-id="4d3f9-127">Property</span></span>    | <span data-ttu-id="4d3f9-128">Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="4d3f9-128">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="4d3f9-129">**качедсизеофсет**</span><span class="sxs-lookup"><span data-stu-id="4d3f9-129">**CachedSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | <span data-ttu-id="4d3f9-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="4d3f9-130">Property</span></span>    | <span data-ttu-id="4d3f9-131">Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="4d3f9-131">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="4d3f9-132">**куррентлевел**</span><span class="sxs-lookup"><span data-stu-id="4d3f9-132">**CurrentLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | <span data-ttu-id="4d3f9-133">Свойство</span><span class="sxs-lookup"><span data-stu-id="4d3f9-133">Property</span></span>    | <span data-ttu-id="4d3f9-134">Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="4d3f9-134">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="4d3f9-135">**куррентпоситионинсет**</span><span class="sxs-lookup"><span data-stu-id="4d3f9-135">**CurrentPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | <span data-ttu-id="4d3f9-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="4d3f9-136">Property</span></span>    | <span data-ttu-id="4d3f9-137">Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="4d3f9-137">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="4d3f9-138">**куррентсизеофсет**</span><span class="sxs-lookup"><span data-stu-id="4d3f9-138">**CurrentSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | <span data-ttu-id="4d3f9-139">Свойство</span><span class="sxs-lookup"><span data-stu-id="4d3f9-139">Property</span></span>    | <span data-ttu-id="4d3f9-140">Размещается в интерфейсе [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="4d3f9-140">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="4d3f9-141">**Осуществляется**</span><span class="sxs-lookup"><span data-stu-id="4d3f9-141">**Navigate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | <span data-ttu-id="4d3f9-142">Метод</span><span class="sxs-lookup"><span data-stu-id="4d3f9-142">Method</span></span>      | <span data-ttu-id="4d3f9-143">Нет</span><span class="sxs-lookup"><span data-stu-id="4d3f9-143">None</span></span>                                                                                |



 

<span data-ttu-id="4d3f9-144">Этот шаблон элемента управления не имеет связанных методов или событий.</span><span class="sxs-lookup"><span data-stu-id="4d3f9-144">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d3f9-145">См. также</span><span class="sxs-lookup"><span data-stu-id="4d3f9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d3f9-146">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="4d3f9-146">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="4d3f9-147">Элемент управления ListItem</span><span class="sxs-lookup"><span data-stu-id="4d3f9-147">ListItem Control</span></span>](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="4d3f9-148">Элемент управления HeaderItem</span><span class="sxs-lookup"><span data-stu-id="4d3f9-148">HeaderItem Control</span></span>](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="4d3f9-149">Элемент управления DataItem</span><span class="sxs-lookup"><span data-stu-id="4d3f9-149">DataItem Control</span></span>](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="4d3f9-150">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4d3f9-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




