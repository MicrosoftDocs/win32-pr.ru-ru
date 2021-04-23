---
title: Общие сведения о свойствах автоматизированного пользовательского интерфейса
description: Поставщики автоматизации пользовательского интерфейса Майкрософт предоставляют свойства элементов автоматизации пользовательского интерфейса. Свойства позволяют клиентским приложениям получать сведения об элементах управления.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Модель автоматизации пользовательского интерфейса, общие сведения о свойствах
- Модель автоматизации пользовательского интерфейса, свойства и события
- Модель автоматизации пользовательского интерфейса, события и свойства
- свойства, сведения
- свойства, идентификаторы
- свойства, значения
- свойства, события
- события, свойства
- свойства, динамические
- динамические свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252706"
---
# <a name="ui-automation-properties-overview"></a><span data-ttu-id="a32ff-114">Общие сведения о свойствах автоматизированного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a32ff-114">UI Automation Properties Overview</span></span>

<span data-ttu-id="a32ff-115">Поставщики автоматизации пользовательского интерфейса Майкрософт предоставляют свойства элементов автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a32ff-115">Microsoft UI Automation providers expose properties on UI Automation elements.</span></span> <span data-ttu-id="a32ff-116">Свойства позволяют клиентским приложениям получать сведения об элементах управления.</span><span class="sxs-lookup"><span data-stu-id="a32ff-116">Properties enable client applications to retrieve information about controls.</span></span>

<span data-ttu-id="a32ff-117">Модель автоматизации пользовательского интерфейса предоставляет два различных вида свойств: *элементы автоматизации и свойства* элементов *управления*.</span><span class="sxs-lookup"><span data-stu-id="a32ff-117">UI Automation exposes two different kinds of properties: *automation element properties*, and *control pattern propertes*.</span></span> <span data-ttu-id="a32ff-118">Свойства элементов автоматизации состоят из общего набора свойств, таких как Name, Акцелераторкэй и ClassName, которые предоставляются всеми элементами модели автоматизации пользовательского интерфейса независимо от типа элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a32ff-118">The automation element properties consist of a common set of properties, such as Name, AcceleratorKey, and ClassName, that are exposed by all UI Automation elements, regardless of the control type.</span></span> <span data-ttu-id="a32ff-119">Большинство свойств элементов автоматизации являются статическими значениями.</span><span class="sxs-lookup"><span data-stu-id="a32ff-119">Most automation element properties are static values.</span></span>

<span data-ttu-id="a32ff-120">Свойства шаблона элемента управления — это те, которые предоставляются элементом управления, поддерживающим определенный шаблон элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a32ff-120">Control pattern properties are those that are exposed by a control that supports a particular control pattern.</span></span> <span data-ttu-id="a32ff-121">Каждый шаблон элемента управления имеет соответствующий набор свойств шаблона элемента управления, который должен предоставлять элемент управления.</span><span class="sxs-lookup"><span data-stu-id="a32ff-121">Each control pattern has a corresponding set of control pattern properties that the control must expose.</span></span> <span data-ttu-id="a32ff-122">Например, элемент управления, поддерживающий шаблон элемента управления [Grid](uiauto-implementinggrid.md) , предоставляет свойства ColumnCount и ROWCOUNT.</span><span class="sxs-lookup"><span data-stu-id="a32ff-122">For example, a control that supports the [Grid](uiauto-implementinggrid.md) control pattern exposes the ColumnCount and RowCount properties.</span></span> <span data-ttu-id="a32ff-123">Большинство свойств шаблона элемента управления являются динамическими значениями.</span><span class="sxs-lookup"><span data-stu-id="a32ff-123">Most control pattern properties are dynamic values.</span></span>

<span data-ttu-id="a32ff-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="a32ff-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a32ff-125">Идентификаторы свойств</span><span class="sxs-lookup"><span data-stu-id="a32ff-125">Property Identifiers</span></span>](#property-identifiers)
-   [<span data-ttu-id="a32ff-126">Значения свойств</span><span class="sxs-lookup"><span data-stu-id="a32ff-126">Property Values</span></span>](#property-values)
-   [<span data-ttu-id="a32ff-127">Свойства и события</span><span class="sxs-lookup"><span data-stu-id="a32ff-127">Properties and Events</span></span>](#properties-and-events)
-   [<span data-ttu-id="a32ff-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a32ff-128">Related topics</span></span>](#related-topics)

## <a name="property-identifiers"></a><span data-ttu-id="a32ff-129">Идентификаторы свойств</span><span class="sxs-lookup"><span data-stu-id="a32ff-129">Property Identifiers</span></span>

<span data-ttu-id="a32ff-130">Каждое свойство определяется **PROPERTYID** числовым значением, называемым *идентификатором свойства* (ID).</span><span class="sxs-lookup"><span data-stu-id="a32ff-130">Every property is identified by a **PROPERTYID** numeric value called a *property identifier* (ID).</span></span> <span data-ttu-id="a32ff-131">Поставщики и клиенты используют числовые идентификаторы в вызовах методов, таких как [**иравелементпровидерадвисивентс:: адвисивентаддед**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) и [**Иуиаутоматионелемент:: жеткачедпропертивалуе**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) , для идентификации запросов свойств.</span><span class="sxs-lookup"><span data-stu-id="a32ff-131">Providers and clients use the numeric IDs in method calls such as [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) and [**IUIAutomationElement::GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) to identify property requests.</span></span> <span data-ttu-id="a32ff-132">Подробное описание каждого идентификатора свойства модели автоматизации пользовательского интерфейса, включая тип данных и значение по умолчанию для каждого свойства, см. в разделе [идентификаторы свойств](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="a32ff-132">For a detailed description of each UI Automation property identifier, including the data type and default value of each property, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-values"></a><span data-ttu-id="a32ff-133">Значения свойств</span><span class="sxs-lookup"><span data-stu-id="a32ff-133">Property Values</span></span>

<span data-ttu-id="a32ff-134">Все свойства доступны только для чтения, хотя некоторые из них могут быть изменены с помощью методов, действующих в элементе управления, например [**IDockProvider:: сетдоккпоситион**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Provider) или [**Иуиаутоматиондоккпаттерн:: сетдоккпоситион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (клиент).</span><span class="sxs-lookup"><span data-stu-id="a32ff-134">All properties are read-only, although some can be changed by using methods that act on the control, such as [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) or [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).</span></span>

<span data-ttu-id="a32ff-135">Дополнительные сведения о получении значений свойств см. [в разделе Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="a32ff-135">For information about retrieving property values, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>

## <a name="properties-and-events"></a><span data-ttu-id="a32ff-136">Свойства и события</span><span class="sxs-lookup"><span data-stu-id="a32ff-136">Properties and Events</span></span>

<span data-ttu-id="a32ff-137">Тесно связан с свойствами в модели автоматизации пользовательского интерфейса, является концепцией *событий изменения свойств*.</span><span class="sxs-lookup"><span data-stu-id="a32ff-137">Closely associated with the properties in UI Automation is the concept of *property-changed events*.</span></span> <span data-ttu-id="a32ff-138">Для динамических свойств клиентскому приложению требуется способ выяснить, что значение свойства изменилось, чтобы он мог обновить свой кэш информации или реагировать на новые данные каким-либо другим способом.</span><span class="sxs-lookup"><span data-stu-id="a32ff-138">For dynamic properties, a client application needs a way to know that a property value has changed, so that it can update its cache of information or react to the new information in some other way.</span></span> <span data-ttu-id="a32ff-139">Клиенты могут зарегистрироваться для прослушивания событий изменения свойств в любом свойстве.</span><span class="sxs-lookup"><span data-stu-id="a32ff-139">Clients can register to listen for property-changed events on any property.</span></span>

<span data-ttu-id="a32ff-140">Поставщики вызывают события при изменении какого-либо элемента пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a32ff-140">Providers raise events when something in the UI changes.</span></span> <span data-ttu-id="a32ff-141">Например, если флажок установлен или снят, реализация [поставщика для шаблона элемента управления](uiauto-implementingtoggle.md) будет вызывать событие изменения свойства.</span><span class="sxs-lookup"><span data-stu-id="a32ff-141">For example, if a check box is selected or cleared, a property-changed event is raised by the provider implementation of the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="a32ff-142">Поставщики могут вызывать события выборочно, в зависимости от наличия клиентов, прослушивающих события или прослушивающих определенные события.</span><span class="sxs-lookup"><span data-stu-id="a32ff-142">Providers can raise events selectively, depending on whether any clients are listening for events, or listening for specific events.</span></span>

<span data-ttu-id="a32ff-143">Не все изменения свойств порождают события; это полностью зависит от реализации поставщика автоматизации пользовательского интерфейса для элемента.</span><span class="sxs-lookup"><span data-stu-id="a32ff-143">Not all property changes raise events; that is entirely up to the implementation of the UI Automation provider for the element.</span></span> <span data-ttu-id="a32ff-144">Например, стандартные поставщики прокси для списков не вызывают событие изменения свойства при изменении свойства Selection.</span><span class="sxs-lookup"><span data-stu-id="a32ff-144">For example, the standard proxy providers for list boxes do not raise a property-changed event when the Selection property changes.</span></span> <span data-ttu-id="a32ff-145">В этом случае приложение должно прослушивать событие, возникающее при изменении выбора ([**UIA \_ SelectionItem \_ елементселектедевентид**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="a32ff-145">In this case, the application must listen for the event raised when the selection changes ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)).</span></span>

<span data-ttu-id="a32ff-146">Клиенты прослушивают события, подписавшись на них, как описано в разделе [Подписка на события модели автоматизации пользовательского интерфейса](uiauto-eventsforclients.md).</span><span class="sxs-lookup"><span data-stu-id="a32ff-146">Clients listen for events by subscribing to them, as described at [Subscribing to UI Automation Events](uiauto-eventsforclients.md).</span></span> <span data-ttu-id="a32ff-147">В частности, для событий, измененных свойством, клиенты должны реализовать [**иуиаутоматионпропертичанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) и передать интерфейс в [**Иуиаутоматион:: аддпропертичанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) или [**IUIAutomation:: AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span><span class="sxs-lookup"><span data-stu-id="a32ff-147">For property-changed events in particular, clients must implement [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) and pass the interface to [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) or [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a32ff-148">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a32ff-148">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a32ff-149">**Reference**</span><span class="sxs-lookup"><span data-stu-id="a32ff-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a32ff-150">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="a32ff-150">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[<span data-ttu-id="a32ff-151">**жеткуррентпропертивалуикс**</span><span class="sxs-lookup"><span data-stu-id="a32ff-151">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[<span data-ttu-id="a32ff-152">**жеткачедпропертивалуе**</span><span class="sxs-lookup"><span data-stu-id="a32ff-152">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[<span data-ttu-id="a32ff-153">**жеткачедпропертивалуикс**</span><span class="sxs-lookup"><span data-stu-id="a32ff-153">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

<span data-ttu-id="a32ff-154">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a32ff-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a32ff-155">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a32ff-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="a32ff-156">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a32ff-156">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="a32ff-157">Обзор событий автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a32ff-157">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 




