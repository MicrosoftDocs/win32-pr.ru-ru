---
title: Получение свойств элементов модели автоматизации пользовательского интерфейса
description: Свойства объектов Иуиаутоматионелемент содержат сведения об элементах пользовательского интерфейса, обычно элементах управления.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- Клиенты, получение элементов модели автоматизации пользовательского интерфейса
- Клиенты, элементы модели автоматизации пользовательского интерфейса
- Клиенты, свойства
- Клиенты, получение свойств
- Клиенты, свойства модели автоматизации пользовательского интерфейса
- Модель автоматизации пользовательского интерфейса, получение элементов
- Модель автоматизации пользовательского интерфейса, элементы
- Модель автоматизации пользовательского интерфейса, свойства
- Автоматизация пользовательского интерфейса, получение свойств
- получение свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691620"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a><span data-ttu-id="f43ae-113">Получение свойств элементов модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="f43ae-113">Retrieving Properties from UI Automation Elements</span></span>

<span data-ttu-id="f43ae-114">Свойства объектов [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) содержат сведения об элементах пользовательского интерфейса, обычно элементах управления.</span><span class="sxs-lookup"><span data-stu-id="f43ae-114">Properties on [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) objects contain information about UI elements, usually controls.</span></span> <span data-ttu-id="f43ae-115">Свойства элемента являются универсальными; то есть, не относится к типу элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f43ae-115">The properties of an element are generic; that is, not specific to a control type.</span></span> <span data-ttu-id="f43ae-116">Свойства элемента, зависящие от элемента управления, предоставляются интерфейсом шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f43ae-116">Control-specific properties of an element are exposed by its control pattern interfaces.</span></span>

<span data-ttu-id="f43ae-117">Свойства автоматизации пользовательского интерфейса Майкрософт доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f43ae-117">Microsoft UI Automation properties are read-only.</span></span> <span data-ttu-id="f43ae-118">Чтобы задать свойства элемента управления, вы должны использовать методы соответствующего шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f43ae-118">To set properties of a control, you must use the methods of the appropriate control pattern.</span></span> <span data-ttu-id="f43ae-119">Например, используйте [**иуиаутоматионскроллпаттерн:: Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) , чтобы изменить значения позиций прокручиваемого окна.</span><span class="sxs-lookup"><span data-stu-id="f43ae-119">For example, use [**IUIAutomationScrollPattern::Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) to change the position values of a scrolling window.</span></span>

<span data-ttu-id="f43ae-120">Для повышения производительности значения свойств элементов управления и шаблонов элементов управления могут быть кэшированы при извлечении элементов.</span><span class="sxs-lookup"><span data-stu-id="f43ae-120">To improve performance, property values of controls and control patterns can be cached when elements are retrieved.</span></span> <span data-ttu-id="f43ae-121">Дополнительные сведения см. в разделе [кэширование свойств и шаблонов элементов управления автоматизации пользовательского интерфейса](uiauto-cachingforclients.md).</span><span class="sxs-lookup"><span data-stu-id="f43ae-121">For more information, see [Caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).</span></span>

<span data-ttu-id="f43ae-122">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="f43ae-122">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f43ae-123">Идентификаторы свойств</span><span class="sxs-lookup"><span data-stu-id="f43ae-123">Property IDs</span></span>](#property-ids)
-   [<span data-ttu-id="f43ae-124">Условия свойств</span><span class="sxs-lookup"><span data-stu-id="f43ae-124">Property Conditions</span></span>](#property-conditions)
-   [<span data-ttu-id="f43ae-125">Получение свойств</span><span class="sxs-lookup"><span data-stu-id="f43ae-125">Retrieving Properties</span></span>](#retrieving-properties)
-   [<span data-ttu-id="f43ae-126">Значения свойств по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f43ae-126">Default Property Values</span></span>](#default-property-values)
-   [<span data-ttu-id="f43ae-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f43ae-127">Related topics</span></span>](#related-topics)

## <a name="property-ids"></a><span data-ttu-id="f43ae-128">Идентификаторы свойств</span><span class="sxs-lookup"><span data-stu-id="f43ae-128">Property IDs</span></span>

<span data-ttu-id="f43ae-129">Идентификаторы свойств определены в UIAutomationClient. h.</span><span class="sxs-lookup"><span data-stu-id="f43ae-129">Property identifiers are defined in Uiautomationclient.h.</span></span> <span data-ttu-id="f43ae-130">Они используются для указания свойств при оформлении подписки на события изменения свойств, извлечения значений свойств и конструирования условий свойств.</span><span class="sxs-lookup"><span data-stu-id="f43ae-130">They are used to specify properties when you subscribe to property-changed events, retrieve property values, and construct property conditions.</span></span> <span data-ttu-id="f43ae-131">Идентификаторы свойств также обозначают свойство, которое было изменено при вызове [**иуиаутоматионпропертичанжедевенсандлер:: хандлепропертичанжедевент**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) .</span><span class="sxs-lookup"><span data-stu-id="f43ae-131">Property identifiers also identify the property that has changed when [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) is called.</span></span>

<span data-ttu-id="f43ae-132">Список идентификаторов свойств модели автоматизации пользовательского интерфейса см. в разделе [идентификаторы свойств](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="f43ae-132">For a list of UI Automation property identifiers, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-conditions"></a><span data-ttu-id="f43ae-133">Условия свойств</span><span class="sxs-lookup"><span data-stu-id="f43ae-133">Property Conditions</span></span>

<span data-ttu-id="f43ae-134">Идентификаторы свойств используются при конструировании объектов [**иуиаутоматионпропертикондитион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) , которые используются для поиска элементов автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f43ae-134">The property IDs are used in constructing [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) objects that are used to find UI Automation elements.</span></span> <span data-ttu-id="f43ae-135">Например, может потребоваться найти элемент с определенным именем или все включенные элементы управления.</span><span class="sxs-lookup"><span data-stu-id="f43ae-135">For example, you might want to find an element that has a certain name, or all controls that are enabled.</span></span> <span data-ttu-id="f43ae-136">Каждое условие свойства указывает идентификатор свойства и значение, которым должно соответствовать свойство.</span><span class="sxs-lookup"><span data-stu-id="f43ae-136">Each property condition specifies a property identifier and the value that the property must match.</span></span>

<span data-ttu-id="f43ae-137">Дополнительные сведения см. в следующих справочных разделах.</span><span class="sxs-lookup"><span data-stu-id="f43ae-137">For more information, see the following reference topics:</span></span>

-   [<span data-ttu-id="f43ae-138">**Иуиаутоматион:: Креатепропертикондитион**</span><span class="sxs-lookup"><span data-stu-id="f43ae-138">**IUIAutomation::CreatePropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [<span data-ttu-id="f43ae-139">**Иуиаутоматион:: Креатепропертикондитионекс**</span><span class="sxs-lookup"><span data-stu-id="f43ae-139">**IUIAutomation::CreatePropertyConditionEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [<span data-ttu-id="f43ae-140">**Иуиаутоматионелемент:: FindFirst**</span><span class="sxs-lookup"><span data-stu-id="f43ae-140">**IUIAutomationElement::FindFirst**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [<span data-ttu-id="f43ae-141">**Иуиаутоматионелемент:: FindAll**</span><span class="sxs-lookup"><span data-stu-id="f43ae-141">**IUIAutomationElement::FindAll**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a><span data-ttu-id="f43ae-142">Получение свойств</span><span class="sxs-lookup"><span data-stu-id="f43ae-142">Retrieving Properties</span></span>

<span data-ttu-id="f43ae-143">Некоторые универсальные свойства и все свойства шаблона элемента управления доступны как свойства в интерфейсе шаблона [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) или элемента управления и могут извлекаться с помощью метода доступа, такого как [**Иуиаутоматионелемент:: куррентнаме**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) или [**качеддоккпоситион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span><span class="sxs-lookup"><span data-stu-id="f43ae-143">Some generic properties, and all control pattern properties, are available as properties on the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) or control pattern interface and can be retrieved by using an accessor, such as [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) or [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span></span>

<span data-ttu-id="f43ae-144">Кроме того, любое текущее или кэшированное свойство (кроме свойств шаблона элемента управления) можно получить с помощью одного из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="f43ae-144">In addition, any current or cached property (other than control pattern properties) can be retrieved by using one of the following methods:</span></span>

-   [<span data-ttu-id="f43ae-145">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="f43ae-145">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [<span data-ttu-id="f43ae-146">**жеткуррентпропертивалуикс**</span><span class="sxs-lookup"><span data-stu-id="f43ae-146">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [<span data-ttu-id="f43ae-147">**жеткачедпропертивалуе**</span><span class="sxs-lookup"><span data-stu-id="f43ae-147">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [<span data-ttu-id="f43ae-148">**жеткачедпропертивалуикс**</span><span class="sxs-lookup"><span data-stu-id="f43ae-148">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

<span data-ttu-id="f43ae-149">Эти методы обеспечивают немного более высокую производительность и доступ к полному спектру свойств.</span><span class="sxs-lookup"><span data-stu-id="f43ae-149">These methods offer slightly better performance and access to the full range of properties.</span></span> <span data-ttu-id="f43ae-150">Однако значения возвращаются в структурах [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , тогда как методы доступа к отдельным свойствам приводят значение к соответствующему типу.</span><span class="sxs-lookup"><span data-stu-id="f43ae-150">However, values are returned in [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structures, whereas the individual property accessors cast the value to the appropriate type.</span></span>

## <a name="default-property-values"></a><span data-ttu-id="f43ae-151">Значения свойств по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f43ae-151">Default Property Values</span></span>

<span data-ttu-id="f43ae-152">Если поставщик автоматизации пользовательского интерфейса не реализует свойство, то модель автоматизации пользовательского интерфейса может предоставить значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f43ae-152">If a UI Automation provider does not implement a property, UI Automation can supply a default value.</span></span> <span data-ttu-id="f43ae-153">Например, если поставщик элемента управления не поддерживает свойство, идентифицируемое [**UIA \_ хелптекстпропертид**](uiauto-automation-element-propids.md), то модель автоматизации пользовательского интерфейса возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="f43ae-153">For example, if the provider for a control does not support the property identified by [**UIA\_HelpTextPropertyId**](uiauto-automation-element-propids.md), UI Automation returns an empty string.</span></span> <span data-ttu-id="f43ae-154">Аналогично, если поставщик не поддерживает свойство, идентифицируемое [**UIA \_ Исдоккпаттернаваилаблепропертид**](uiauto-control-pattern-availability-propids.md), модель автоматизации пользовательского интерфейса возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f43ae-154">Similarly, if the provider does not support the property identified by [**UIA\_IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), UI Automation returns **FALSE**.</span></span>

<span data-ttu-id="f43ae-155">Разница между [**иуиаутоматионелемент:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) и [**жеткуррентпропертивалуикс**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (и между аналогичными парами методов) заключается в том, что метод "ex" может указывать, что значение по умолчанию не возвращается.</span><span class="sxs-lookup"><span data-stu-id="f43ae-155">The difference between [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) and [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (and between similar pairs of methods) is that the "Ex" method can specify that no default value is to be returned.</span></span> <span data-ttu-id="f43ae-156">В этом случае возвращаемое значение является особой уникальной константой, указывающей, что свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f43ae-156">In this case, the return value is a special unique constant, indicating that the property is not supported.</span></span> <span data-ttu-id="f43ae-157">При получении этого значения приложение может предоставить собственное значение или просто игнорировать свойство.</span><span class="sxs-lookup"><span data-stu-id="f43ae-157">On receiving this value, the application can supply its own value or simply ignore the property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f43ae-158">См. также</span><span class="sxs-lookup"><span data-stu-id="f43ae-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f43ae-159">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f43ae-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f43ae-160">Общие сведения о свойствах автоматизированного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="f43ae-160">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="f43ae-161">Идентификаторы свойств</span><span class="sxs-lookup"><span data-stu-id="f43ae-161">Property Identifiers</span></span>](uiauto-entry-propids.md)
</dt> </dl>

 

 