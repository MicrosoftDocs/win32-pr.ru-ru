---
title: Интерфейс IAccessibleEx
description: Элементы управления, у которых нет поставщика Microsoft UI Automation, но реализующие IAccessible, можно легко обновить, чтобы обеспечить некоторые функции автоматизации пользовательского интерфейса путем реализации интерфейса IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133002"
---
# <a name="the-iaccessibleex-interface"></a><span data-ttu-id="439e2-103">Интерфейс IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="439e2-103">The IAccessibleEx Interface</span></span>

<span data-ttu-id="439e2-104">Элементы управления, у которых нет поставщика Microsoft UI Automation, но реализующие [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), можно легко обновить, чтобы обеспечить некоторые функции автоматизации пользовательского интерфейса путем реализации интерфейса [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="439e2-104">Controls that do not have a Microsoft UI Automation provider, but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), can easily be upgraded to provide some UI Automation functionality by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="439e2-105">Этот интерфейс позволяет элементу управления предоставлять свойства автоматизации пользовательского интерфейса и шаблоны элементов управления без необходимости полной реализации интерфейсов поставщика автоматизации пользовательского интерфейса, таких как [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="439e2-105">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="439e2-106">Чтобы использовать **IAccessibleEx**, **иравелементпровидерфрагмент** и все другие интерфейсы автоматизации пользовательского интерфейса, включите в исходный код файл заголовка UIAutomation. h.</span><span class="sxs-lookup"><span data-stu-id="439e2-106">To use **IAccessibleEx**, **IRawElementProviderFragment**, and all other UI Automation interfaces, include the UIAutomation.h header file in your source code.</span></span>

<span data-ttu-id="439e2-107">Например, рассмотрим пользовательский элемент управления, имеющий значение Range.</span><span class="sxs-lookup"><span data-stu-id="439e2-107">For example, consider a custom control that has a range value.</span></span> <span data-ttu-id="439e2-108">Сервер Microsoft Active Accessibility для элемента управления определяет роль элемента управления и может возвращать его текущее значение.</span><span class="sxs-lookup"><span data-stu-id="439e2-108">The Microsoft Active Accessibility server for the control defines the control's role and is able to return its current value.</span></span> <span data-ttu-id="439e2-109">Однако, поскольку Microsoft Active Accessibility не определяет минимальное и максимальное свойства, сервер не имеет средств для возврата минимального и максимального значений элемента управления.</span><span class="sxs-lookup"><span data-stu-id="439e2-109">However, because Microsoft Active Accessibility does not define minimum and maximum properties, the server lacks the means to return the minimum and maximum values of the control.</span></span> <span data-ttu-id="439e2-110">Клиент автоматизации пользовательского интерфейса может получить роль элемента управления, текущее значение и другие свойства Microsoft Active Accessibility, так как ядро автоматизации пользовательского интерфейса может получить их через [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="439e2-110">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="439e2-111">Однако без доступа к интерфейсу [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) в объекте модель автоматизации пользовательского интерфейса также не может получить максимальное и минимальное значения.</span><span class="sxs-lookup"><span data-stu-id="439e2-111">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="439e2-112">Разработчик элемента управления может предоставить полный поставщик автоматизации пользовательского интерфейса для элемента управления, но это означает дублирование большинства существующих функциональных возможностей реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : например, навигации и общих свойств.</span><span class="sxs-lookup"><span data-stu-id="439e2-112">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="439e2-113">Вместо этого разработчик может по-прежнему использовать **IAccessible** для предоставления этой функции, добавляя поддержку свойств конкретного элемента управления через [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="439e2-113">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="439e2-114">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="439e2-114">In this section</span></span>

-   [<span data-ttu-id="439e2-115">Рекомендации по реализации IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="439e2-115">IAccessibleEx Implementation Guidelines</span></span>](iaccessibleex-implementation-guidelines.md)
-   [<span data-ttu-id="439e2-116">Реализация IAccessibleEx для поставщиков</span><span class="sxs-lookup"><span data-stu-id="439e2-116">Implementing IAccessibleEx for Providers</span></span>](implementing-iaccessibleex-for-providers.md)
-   [<span data-ttu-id="439e2-117">Использование IAccessibleEx из клиента</span><span class="sxs-lookup"><span data-stu-id="439e2-117">Using IAccessibleEx from a Client</span></span>](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a><span data-ttu-id="439e2-118">См. также</span><span class="sxs-lookup"><span data-stu-id="439e2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439e2-119">Общая инфраструктура</span><span class="sxs-lookup"><span data-stu-id="439e2-119">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




