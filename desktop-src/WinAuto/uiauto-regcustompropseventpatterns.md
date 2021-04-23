---
title: Регистрация пользовательских свойств, событий и шаблонов элементов управления
description: Прежде чем можно будет использовать пользовательское свойство, событие или шаблон элемента управления, поставщик и клиент должны зарегистрировать свойство, событие или шаблон элемента управления во время выполнения.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Модель автоматизации пользовательского интерфейса, пользовательские свойства
- Модель автоматизации пользовательского интерфейса, общие сведения о событиях
- Модель автоматизации пользовательского интерфейса, общие сведения о шаблонах элементов управления
- Автоматизация пользовательского интерфейса, регистрация пользовательских свойств
- Автоматизация пользовательского интерфейса, регистрация событий
- Автоматизация пользовательского интерфейса, регистрация шаблонов элементов управления
- Пользовательские свойства, регистрация
- события, регистрация
- шаблоны элементов управления, регистрация
- регистрация, пользовательские свойства
- регистрация, события
- регистрация, шаблоны элементов управления
- шаблоны элементов управления, пользовательские
- шаблоны элементов управления, реализация пользовательского
- Реализация пользовательских шаблонов элементов управления
- пользовательские шаблоны элементов управления
- клиентские оболочки
- обработчики шаблонов
- Реализация обработчиков шаблонов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070444"
---
# <a name="register-custom-properties-events-and-control-patterns"></a><span data-ttu-id="fb2ba-122">Регистрация пользовательских свойств, событий и шаблонов элементов управления</span><span class="sxs-lookup"><span data-stu-id="fb2ba-122">Register custom properties, events, and control patterns</span></span>

<span data-ttu-id="fb2ba-123">Прежде чем можно будет использовать пользовательское свойство, событие или шаблон элемента управления, поставщик и клиент должны зарегистрировать свойство, событие или шаблон элемента управления во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-123">Before a custom property, event, or control pattern can be used, both the provider and the client must register the property, event, or control pattern at run time.</span></span> <span data-ttu-id="fb2ba-124">Регистрация действует глобально в рамках процесса приложения и остается эффективной до тех пор, пока процесс не будет закрыт или последний объект элемента автоматизации пользовательского интерфейса Майкрософт ([**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) или [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) выйдет из процесса.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-124">The registration is effective globally within an application process, and remains effective until the process closes or the last Microsoft UI Automation element object ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) or [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) is released within the process.</span></span>

<span data-ttu-id="fb2ba-125">Для этого необходимо передать идентификатор GUID в автоматизацию пользовательского интерфейса, а также подробные сведения о настраиваемом свойстве, событии или шаблоне элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-125">Registation involves passing a GUID to UI Automation, along with detailed information about the custom property, event, or control pattern.</span></span> <span data-ttu-id="fb2ba-126">Попытка зарегистрировать один и тот же GUID во второй раз с теми же сведениями завершится успешно, но попытка зарегистрировать один и тот же GUID в второй раз, но с разными сведениями (например, пользовательское свойство другого типа) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-126">Attempting to register the same GUID a second time with the same information will succeed, but attempting to register the same GUID a second time but with different information (for example, a custom property of a different type) will fail.</span></span> <span data-ttu-id="fb2ba-127">В будущем, если пользовательская спецификация принята и интегрирована в ядро автоматизации пользовательского интерфейса, модель автоматизации пользовательского интерфейса будет проверять пользовательские данные регистрации и использовать уже зарегистрированный код вместо "официальной" реализации платформы, тем самым минимизируя проблемы совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-127">In the future, if the custom specification is accepted and integrated into the UI Automation core, UI Automation will validate the custom registration information and use the already registered code instead of the "official" framework implementation, thereby minimizing application compatibility issues.</span></span> <span data-ttu-id="fb2ba-128">Невозможно удалить уже зарегистрированные свойства, события или шаблоны элементов управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-128">You cannot remove properties, events, or control patterns that are already registered.</span></span>

<span data-ttu-id="fb2ba-129">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-129">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="fb2ba-130">Регистрация пользовательских свойств и событий</span><span class="sxs-lookup"><span data-stu-id="fb2ba-130">Registering Custom Properties and Events</span></span>](#registering-custom-properties-and-events)
-   [<span data-ttu-id="fb2ba-131">Реализация пользовательских шаблонов элементов управления</span><span class="sxs-lookup"><span data-stu-id="fb2ba-131">Implementing Custom Control Patterns</span></span>](#implementing-custom-control-patterns)
    -   [<span data-ttu-id="fb2ba-132">Оболочка клиента и обработчик шаблона</span><span class="sxs-lookup"><span data-stu-id="fb2ba-132">The Client Wrapper and the Pattern Handler</span></span>](#the-client-wrapper-and-the-pattern-handler)
    -   [<span data-ttu-id="fb2ba-133">Реализация оболочки клиента</span><span class="sxs-lookup"><span data-stu-id="fb2ba-133">Implementing the Client Wrapper</span></span>](#implementing-the-client-wrapper)
    -   [<span data-ttu-id="fb2ba-134">Реализация обработчика шаблона</span><span class="sxs-lookup"><span data-stu-id="fb2ba-134">Implementing the Pattern Handler</span></span>](#implementing-the-pattern-handler)
    -   [<span data-ttu-id="fb2ba-135">Регистрация пользовательского шаблона элемента управления</span><span class="sxs-lookup"><span data-stu-id="fb2ba-135">Registering a Custom Control Pattern</span></span>](#registering-a-custom-control-pattern)
    -   [<span data-ttu-id="fb2ba-136">Пример реализации пользовательского шаблона элемента управления</span><span class="sxs-lookup"><span data-stu-id="fb2ba-136">Example Implementation of a Custom Control Pattern</span></span>](#example-implementation-of-a-custom-control-pattern)
-   [<span data-ttu-id="fb2ba-137">См. также</span><span class="sxs-lookup"><span data-stu-id="fb2ba-137">Related topics</span></span>](#related-topics)

## <a name="registering-custom-properties-and-events"></a><span data-ttu-id="fb2ba-138">Регистрация пользовательских свойств и событий</span><span class="sxs-lookup"><span data-stu-id="fb2ba-138">Registering Custom Properties and Events</span></span>

<span data-ttu-id="fb2ba-139">Регистрация пользовательского свойства или события позволяет поставщику и клиенту получить идентификатор для свойства или события, которое затем может быть передано различным методам API, принимающим идентификаторы в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-139">Registering a custom property or event enables the provider and client to obtain an ID for the property or event, which can then be passed to various API methods that take IDs as parameters.</span></span>

<span data-ttu-id="fb2ba-140">Чтобы зарегистрировать свойство или событие, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="fb2ba-140">To register a property or event:</span></span>

1.  <span data-ttu-id="fb2ba-141">Определите идентификатор GUID для пользовательского свойства или события.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-141">Define a GUID for the custom property or event.</span></span>
2.  <span data-ttu-id="fb2ba-142">Заполните структуру [**уиаутоматионпропертинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) или [**уиаутоматионевентинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) информацией о свойстве или событии, включая идентификатор GUID и нелокализуемое строку, содержащую имя пользовательского свойства или события.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-142">Fill a [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) or a [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure with information about the property or event, including the GUID and a nonlocalizable string that contains the name of the custom property or event.</span></span> <span data-ttu-id="fb2ba-143">Для пользовательских свойств также требуется указать тип данных свойства, например, содержит ли свойство целое число или строку.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-143">Custom properties also require the data type of the property to be specified, for example, whether the property holds an integer or a string.</span></span> <span data-ttu-id="fb2ba-144">Тип данных должен быть одним из следующих типов, указанных в перечислении [**уиаутоматионтипе**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) .</span><span class="sxs-lookup"><span data-stu-id="fb2ba-144">The data type must be one of the following types specified by the [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) enumeration.</span></span> <span data-ttu-id="fb2ba-145">Другие типы данных для пользовательских свойств не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-145">No other data types are supported for custom properties.</span></span>
    -   <span data-ttu-id="fb2ba-146">**\_Bool уиаутоматионтипе**</span><span class="sxs-lookup"><span data-stu-id="fb2ba-146">**UIAutomationType\_Bool**</span></span>
    -   <span data-ttu-id="fb2ba-147">**Уиаутоматионтипе \_ Double**</span><span class="sxs-lookup"><span data-stu-id="fb2ba-147">**UIAutomationType\_Double**</span></span>
    -   <span data-ttu-id="fb2ba-148">**Уиаутоматионтипе, \_ элемент**</span><span class="sxs-lookup"><span data-stu-id="fb2ba-148">**UIAutomationType\_Element**</span></span>
    -   <span data-ttu-id="fb2ba-149">**Уиаутоматионтипе \_ int**</span><span class="sxs-lookup"><span data-stu-id="fb2ba-149">**UIAutomationType\_Int**</span></span>
    -   <span data-ttu-id="fb2ba-150">**\_Точка уиаутоматионтипе**</span><span class="sxs-lookup"><span data-stu-id="fb2ba-150">**UIAutomationType\_Point**</span></span>
    -   <span data-ttu-id="fb2ba-151">**\_Строка уиаутоматионтипе**</span><span class="sxs-lookup"><span data-stu-id="fb2ba-151">**UIAutomationType\_String**</span></span>
3.  <span data-ttu-id="fb2ba-152">Используйте функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания экземпляра объекта [**куиаутоматионрегистрар**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) и получения указателя на интерфейс [**иуиаутоматионрегистрар**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) объекта.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-152">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
4.  <span data-ttu-id="fb2ba-153">Вызовите метод [**иуиаутоматионрегистрар:: регистерпроперти**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) или [**регистеревент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) и передайте адрес структуры [**уиаутоматионпропертинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) или структуры [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .</span><span class="sxs-lookup"><span data-stu-id="fb2ba-153">Call the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method and pass the address of the [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structure or the [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure.</span></span>

<span data-ttu-id="fb2ba-154">Метод [**иуиаутоматионрегистрар:: регистерпроперти**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) или [**регистеревент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) ВОЗВРАЩАЕТ идентификатор свойства или идентификатор события, который приложение может передать в любой метод автоматизации пользовательского интерфейса, принимающий такой идентификатор в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-154">The [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method returns a property ID or event ID that an application can pass to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="fb2ba-155">Например, можно передать зарегистрированный идентификатор свойства в метод [**иуиаутоматионелемент:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) или метод [**Иуиаутоматион:: креатепропертикондитион**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .</span><span class="sxs-lookup"><span data-stu-id="fb2ba-155">For example, you can pass a registered property ID to the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method or to the [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) method.</span></span>

<span data-ttu-id="fb2ba-156">В следующем примере показано, как зарегистрировать пользовательское свойство.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-156">The following example demonstrates how to register a custom property.</span></span>


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



<span data-ttu-id="fb2ba-157">Идентификаторы свойств и событий, извлекаемых методами [**иуиаутоматионрегистрар:: регистерпроперти**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) и [**регистеревент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) , допустимы только в контексте приложения, которое их извлекает, и только в течение времени существования приложения.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-157">The property and event identifiers retrieved by the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) and [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) methods are valid only in the context of the application that retrieves them, and only for the duration of the application's lifetime.</span></span> <span data-ttu-id="fb2ba-158">Методы регистрации могут возвращать различные целочисленные значения для одного и того же идентификатора GUID при вызове в разных экземплярах среды выполнения одного приложения.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-158">The registration methods can return different integer values for the same GUID when it is called over different runtime instances of the same application.</span></span>

<span data-ttu-id="fb2ba-159">Нет метода, который отменяет регистрацию пользовательского свойства или события.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-159">There is no method that unregisters a custom property or event.</span></span> <span data-ttu-id="fb2ba-160">Вместо этого они неявно отменяют регистрацию при освобождении последнего объекта модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-160">Instead, they are implicitly unregistered when the last UI Automation object is released.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb2ba-161">Если код является клиентом Microsoft Active Accessibility (MSAA), необходимо вызвать функцию [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) при изменении значения пользовательского свойства.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-161">If your code is a Microsoft Active Accessibility (MSAA) client, you must call the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function when you change the value of a custom property.</span></span>

 

## <a name="implementing-custom-control-patterns"></a><span data-ttu-id="fb2ba-162">Реализация пользовательских шаблонов элементов управления</span><span class="sxs-lookup"><span data-stu-id="fb2ba-162">Implementing Custom Control Patterns</span></span>

<span data-ttu-id="fb2ba-163">Пользовательский шаблон элемента управления не включается в API автоматизации пользовательского интерфейса, но предоставляется третьей стороной во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-163">A custom control pattern is not included in the UI Automation API, but is provided by a third party at run time.</span></span> <span data-ttu-id="fb2ba-164">Разработчики приложений клиента и поставщика должны совместно работать с определением пользовательского шаблона элемента управления, включая методы, свойства и события, которые будут поддерживаться шаблоном элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-164">Developers of client and provider applications must work together to define a custom control pattern, including the methods, properties, and events that the control pattern will support.</span></span> <span data-ttu-id="fb2ba-165">После определения шаблона элемента управления клиент и поставщик должны реализовать вспомогательные объекты COM, а также код для регистрации шаблона элемента управления во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-165">After defining the control pattern, both the client and the provider must implement supporting Component Object Model (COM) objects, along with code to register the control pattern at run time.</span></span> <span data-ttu-id="fb2ba-166">Для пользовательского шаблона элемента управления требуется реализация двух COM-объектов: клиентская оболочка и обработчик шаблона.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-166">A custom control pattern requires the implementation of two COM objects: a client wrapper and a pattern handler.</span></span>

> [!Note]  
> <span data-ttu-id="fb2ba-167">В примерах в следующих разделах показано, как реализовать пользовательский шаблон элемента управления, который дублирует функциональные возможности существующего шаблона элемента управления [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="fb2ba-167">The examples in the following topics illustrate how to implement a custom control pattern that duplicates the functionality of the existing [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="fb2ba-168">Эти примеры предназначены только для инструкций.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-168">These examples are for instructional purposes only.</span></span> <span data-ttu-id="fb2ba-169">Реальный шаблон пользовательского элемента управления должен предоставлять функциональные возможности, недоступные из стандартных шаблонов элементов управления модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-169">An actual custom control pattern should provide functionality that is not available from the standard UI Automation control patterns.</span></span>

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a><span data-ttu-id="fb2ba-170">Оболочка клиента и обработчик шаблона</span><span class="sxs-lookup"><span data-stu-id="fb2ba-170">The Client Wrapper and the Pattern Handler</span></span>

<span data-ttu-id="fb2ba-171">Обертка клиента реализует API, который используется клиентом для извлечения свойств и вызова методов, предоставляемых пользовательским шаблоном элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-171">The client wrapper implements the API that is used by the client to retrieve properties and call methods exposed by the custom control pattern.</span></span> <span data-ttu-id="fb2ba-172">API реализован в виде COM-интерфейса, который передает все запросы свойств и вызовы методов в ядро автоматизации пользовательского интерфейса, которое затем маршалирует запросы и вызовы поставщику.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-172">The API is implemented as a COM interface that passes all property requests and method calls to the UI Automation core, which then marshals the requests and calls to the provider.</span></span>

<span data-ttu-id="fb2ba-173">Код, регистрирующий пользовательский шаблон элемента управления, должен предоставить фабрику класса, которую модель автоматизации пользовательского интерфейса может использовать для создания экземпляров объекта-оболочки клиента.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-173">The code that registers a custom control pattern must supply a class factory that UI Automation can use to create instances of the client wrapper object.</span></span> <span data-ttu-id="fb2ba-174">При успешной регистрации пользовательского шаблона элемента управления UI Automation возвращает указатель интерфейса [**иуиаутоматионпаттернинстанце**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , который используется клиентом для переадресации запросов свойств и методов в ядро автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-174">When a custom control pattern is successfully registered, UI Automation returns an [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface pointer that is used by the client to forward property requests and methods calls to the UI Automation core.</span></span>

<span data-ttu-id="fb2ba-175">На стороне поставщика ядро автоматизации пользовательского интерфейса принимает запросы свойств и вызовы методов от клиента и передает их объекту обработчика шаблона.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-175">On the provider side, the UI Automation core takes the property requests and method calls from the client and passes them to the pattern handler object.</span></span> <span data-ttu-id="fb2ba-176">Затем обработчик шаблона вызывает соответствующие методы в интерфейсе поставщика для пользовательского шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-176">The pattern handler then calls the appropriate methods on the provider interface for the custom control pattern.</span></span>

<span data-ttu-id="fb2ba-177">Код, регистрирующий пользовательский шаблон элемента управления, создает объект обработчика шаблона и при регистрации шаблона элемента управления предоставляет автоматизацию пользовательского интерфейса с указателем на интерфейс [**иуиаутоматионпаттернхандлер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) объекта.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-177">The code that registers a custom control pattern creates the pattern handler object and, when registering the control pattern, provides UI Automation with a pointer to the object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span>

<span data-ttu-id="fb2ba-178">На следующей схеме показано, как запрос клиентского свойства или вызов метода передается из оболочки клиента через базовые компоненты модели автоматизации пользовательского интерфейса в обработчик шаблона, а затем в интерфейс поставщика.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-178">The following diagram shows how a client property request or method call flows from the client wrapper, through the UI Automation core components to the pattern handler, and then to the provider interface.</span></span>

![Схема, показывающая поток от клиентской оболочки до обработчика шаблона и поставщика](images/custompatternsupport.jpg)

<span data-ttu-id="fb2ba-180">Объекты, реализующие оболочку клиента и интерфейсы обработчика шаблонов, должны быть свободными потоками.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-180">The objects that implement the client wrapper and pattern handler interfaces must be free-threaded.</span></span> <span data-ttu-id="fb2ba-181">Кроме того, ядро автоматизации пользовательского интерфейса должно иметь возможность вызывать объекты напрямую без какого бы то ни было промежуточного кода.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-181">Also, the UI Automation core must be able to call the objects directly without any intermediate marshaling code.</span></span>

### <a name="implementing-the-client-wrapper"></a><span data-ttu-id="fb2ba-182">Реализация оболочки клиента</span><span class="sxs-lookup"><span data-stu-id="fb2ba-182">Implementing the Client Wrapper</span></span>

<span data-ttu-id="fb2ba-183">Обертка клиента — это объект, предоставляющий интерфейс Икскскспаттерн, используемый клиентом для запроса свойств и вызова методов, поддерживаемых шаблоном пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-183">The client wrapper is an object that exposes an IXxxPattern interface that the client uses to request properties and call methods supported by the custom control pattern.</span></span> <span data-ttu-id="fb2ba-184">Интерфейс состоит из пары методов "Getter" для каждого поддерживаемого свойства (Get \_ курренткскскс и Get \_ качедкскскс) и метода "Caller" для каждого поддерживаемого метода.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-184">The interface consists of a pair of "getter" methods for each supported property (get\_CurrentXxx and get\_CachedXxx method), and a "caller" method for each supported method.</span></span> <span data-ttu-id="fb2ba-185">При создании экземпляра объекта конструктор объекта получает указатель на интерфейс [**иуиаутоматионпаттернинстанце**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , который реализуется ядром автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-185">When the object is instantiated, the object constructor receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface, which is implemented by the UI Automation core.</span></span> <span data-ttu-id="fb2ba-186">Методы интерфейса Икскскспаттерн используют методы [**иуиаутоматионпаттернинстанце::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) и [**каллмесод**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) для пересылки запросов свойств и вызовов методов в ядро автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-186">The methods of the IXxxPattern interface use the [**IUIAutomationPatternInstance::GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) and [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) methods to forward property requests and method calls to the UI Automation core.</span></span>

<span data-ttu-id="fb2ba-187">В следующем примере показано, как реализовать клиентский объект-оболочку для простого шаблона пользовательского элемента управления, поддерживающего одно свойство.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-187">The following example shows how to implement a client wrapper object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="fb2ba-188">Более сложный пример см. в разделе [Пример реализации пользовательского шаблона элемента управления](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="fb2ba-188">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a><span data-ttu-id="fb2ba-189">Реализация обработчика шаблона</span><span class="sxs-lookup"><span data-stu-id="fb2ba-189">Implementing the Pattern Handler</span></span>

<span data-ttu-id="fb2ba-190">Обработчик шаблона — это объект, реализующий интерфейс [**иуиаутоматионпаттернхандлер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) .</span><span class="sxs-lookup"><span data-stu-id="fb2ba-190">The pattern handler is an object that implements the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span> <span data-ttu-id="fb2ba-191">Этот интерфейс имеет два метода: [**иуиаутоматионпаттернхандлер:: креатеклиентвраппер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) и [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span><span class="sxs-lookup"><span data-stu-id="fb2ba-191">This interface has two methods: [**IUIAutomationPatternHandler::CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) and [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span></span> <span data-ttu-id="fb2ba-192">Метод **креатеклиентвраппер** вызывается ядром автоматизации пользовательского интерфейса и получает указатель на интерфейс [**иуиаутоматионпаттернинстанце**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) .</span><span class="sxs-lookup"><span data-stu-id="fb2ba-192">The **CreateClientWrapper** method is called by the UI Automation core and receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface.</span></span> <span data-ttu-id="fb2ba-193">**Креатеклиентвраппер** отвечает на создание экземпляра объекта-оболочки клиента и передачу указателя интерфейса **иуиаутоматионпаттернинстанце** в конструктор оболочки клиента.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-193">**CreateClientWrapper** responds by instantiating the client wrapper object and passing the **IUIAutomationPatternInstance** interface pointer to the client wrapper constructor.</span></span>

<span data-ttu-id="fb2ba-194">Метод [**диспетчеризации**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) используется ядром автоматизации пользовательского интерфейса для передачи запросов свойств и вызовов методов интерфейсу поставщика для пользовательского шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-194">The [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) method is used by the UI Automation core to pass property requests and method calls to the provider interface for the custom control pattern.</span></span> <span data-ttu-id="fb2ba-195">Параметры включают указатель на интерфейс поставщика, отсчитываемый от нуля индекс метода получения или вызываемого свойства, а также массив структур [**уиаутоматионпараметер**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) , содержащих параметры для передачи поставщику.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-195">Parameters include a pointer to the provider interface, the zero-based index of the property getter or method being called, and an array of [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) structures that contain the parameters to pass to the provider.</span></span> <span data-ttu-id="fb2ba-196">Обработчик шаблона отвечает, проверяя параметр index, чтобы определить, какой метод поставщика следует вызвать, а затем вызывает этот интерфейс поставщика, передавая параметры, содержащиеся в структурах **уиаутоматионпараметер** .</span><span class="sxs-lookup"><span data-stu-id="fb2ba-196">The pattern handler responds by checking the index parameter to determine which provider method to call, and then calls that provider interface, passing the parameters contained in the **UIAutomationParameter** structures.</span></span>

<span data-ttu-id="fb2ba-197">Экземпляр объекта обработчика шаблона создается с помощью того же кода, который регистрирует пользовательский шаблон элемента управления перед регистрацией шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-197">The pattern handler object is instantiated by the same code that registers the custom control pattern, before the control pattern is registered.</span></span> <span data-ttu-id="fb2ba-198">Код должен передать указатель интерфейса [**иуиаутоматионпаттернхандлер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) объекта обработчика шаблона в ядро автоматизации пользовательского интерфейса во время регистрации.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-198">The code must pass the pattern handler object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface pointer to the UI Automation core at registration time.</span></span>

<span data-ttu-id="fb2ba-199">В следующем примере показано, как реализовать объект обработчика шаблона для простого пользовательского шаблона элемента управления, поддерживающего одно свойство.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-199">The following example shows how to implement a pattern handler object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="fb2ba-200">Более сложный пример см. в разделе [Пример реализации пользовательского шаблона элемента управления](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="fb2ba-200">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a><span data-ttu-id="fb2ba-201">Регистрация пользовательского шаблона элемента управления</span><span class="sxs-lookup"><span data-stu-id="fb2ba-201">Registering a Custom Control Pattern</span></span>

<span data-ttu-id="fb2ba-202">Прежде чем его можно будет использовать, шаблон пользовательского элемента управления должен быть зарегистрирован как поставщиком, так и клиентом.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-202">Before it can be used, a custom control pattern must be registered by both the provider and the client.</span></span> <span data-ttu-id="fb2ba-203">Регистрация предоставляет базовому интерфейсу автоматизации пользовательского интерфейса подробные сведения о шаблоне элемента управления и предоставляет поставщику или клиенту идентификатор шаблона элемента управления, а также идентификаторы для свойств и событий, поддерживаемых шаблоном элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-203">Registering provides the UI Automation core with detailed information about the control pattern, and supplies the provider or client with the control pattern ID, and IDs for the properties and events that are supported by the control pattern.</span></span> <span data-ttu-id="fb2ba-204">На стороне поставщика пользовательский шаблон элемента управления должен быть зарегистрирован до того, как связанный элемент управления обрабатывает сообщение [**WM \_ GetObject**](wm-getobject.md) или в то же время.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-204">On the provider side, the custom control pattern must be registered before the associated control handles the [**WM\_GETOBJECT**](wm-getobject.md) message, or at the same time.</span></span>

<span data-ttu-id="fb2ba-205">При регистрации пользовательского шаблона элемента управления поставщик или клиент предоставляет следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="fb2ba-205">When registering a custom control pattern, the provider or client supplies the following information:</span></span>

-   <span data-ttu-id="fb2ba-206">Идентификатор GUID пользовательского шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-206">The GUID of the custom control pattern.</span></span>
-   <span data-ttu-id="fb2ba-207">Нелокализованная строка, содержащая имя пользовательского шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-207">A nonlocalizable string containing the name of the custom control pattern.</span></span>
-   <span data-ttu-id="fb2ba-208">Идентификатор GUID интерфейса поставщика, поддерживающего шаблон пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-208">The GUID of the provider interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="fb2ba-209">Идентификатор GUID клиентского интерфейса, поддерживающего шаблон пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-209">The GUID of the client interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="fb2ba-210">Массив структур [**уиаутоматионпропертинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) , описывающих свойства, поддерживаемые шаблоном пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-210">An array of [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structures that describe the properties supported by the custom control pattern.</span></span> <span data-ttu-id="fb2ba-211">Для каждого свойства необходимо указать идентификатор GUID, имя свойства и тип данных.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-211">For each property, the GUID, property name, and data type must be specified.</span></span>
-   <span data-ttu-id="fb2ba-212">Массив структур [**уиаутоматионмесодинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) , описывающих методы, поддерживаемые шаблоном пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-212">An array of [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) structures that describe the methods supported by the custom control pattern.</span></span> <span data-ttu-id="fb2ba-213">Для каждого метода структура включает следующие сведения: имя метода, количество параметров, список типов данных параметров и список имен параметров.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-213">For each method, the structure includes the following information: the method name, a count of parameters, a list of parameter data types, and a list of the parameter names.</span></span>
-   <span data-ttu-id="fb2ba-214">Массив структур [**уиаутоматионевентинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) , описывающих события, создаваемые шаблоном пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-214">An array of [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structures that describe the events raised by the custom control pattern.</span></span> <span data-ttu-id="fb2ba-215">Для каждого события необходимо указать идентификатор GUID и имя события.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-215">For each event, the GUID and event name must be specified.</span></span>
-   <span data-ttu-id="fb2ba-216">Адрес интерфейса [**иуиаутоматионпаттернхандлер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) объекта обработчика шаблона, который делает пользовательский шаблон элемента управления доступным для клиентов.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-216">The address of the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface of the pattern handler object that makes the custom control pattern available to clients.</span></span>

<span data-ttu-id="fb2ba-217">Чтобы зарегистрировать пользовательский шаблон элемента управления, поставщик или клиентский код должен выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-217">To register the custom control pattern, the provider or client code must perform the following steps:</span></span>

1.  <span data-ttu-id="fb2ba-218">Заполните структуру [**уиаутоматионпаттернинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) с помощью предыдущих сведений.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-218">Fill a [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure with the preceding information.</span></span>
2.  <span data-ttu-id="fb2ba-219">Используйте функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания экземпляра объекта [**куиаутоматионрегистрар**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) и получения указателя на интерфейс [**иуиаутоматионрегистрар**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) объекта.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-219">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
3.  <span data-ttu-id="fb2ba-220">Вызовите метод [**иуиаутоматионрегистрар:: регистерпаттерн**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) , передав адрес структуры [**уиаутоматионпаттернинфо**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) .</span><span class="sxs-lookup"><span data-stu-id="fb2ba-220">Call the [**IUIAutomationRegistrar::RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method, passing the address of the [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure.</span></span>

<span data-ttu-id="fb2ba-221">Метод [**регистерпаттерн**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) возвращает идентификатор шаблона элемента управления, а также список идентификаторов свойств и идентификаторов событий.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-221">The [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method returns a control pattern ID, along with a list of property IDs and event IDs.</span></span> <span data-ttu-id="fb2ba-222">Приложение может передавать эти идентификаторы любому методу автоматизации пользовательского интерфейса, который принимает такой идентификатор в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-222">An application can pass these IDs to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="fb2ba-223">Например, можно передать зарегистрированный идентификатор шаблона методу [**иуиаутоматионелемент:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , чтобы получить указатель на интерфейс поставщика для шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-223">For example, you can pass a registered pattern ID to the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method to retrieve a pointer to the provider interface for the control pattern.</span></span>

<span data-ttu-id="fb2ba-224">Нет метода, который отменяет регистрацию пользовательского шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-224">There is no method that unregisters a custom control pattern.</span></span> <span data-ttu-id="fb2ba-225">Вместо этого он неявно отменяет регистрацию при освобождении последнего объекта UI Automation.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-225">Instead, it is implicitly unregistered when the last UI Automation object is released.</span></span>

<span data-ttu-id="fb2ba-226">Пример, демонстрирующий регистрацию пользовательского шаблона элемента управления, см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-226">For an example that shows how to register a custom control pattern, see the following section.</span></span>

### <a name="example-implementation-of-a-custom-control-pattern"></a><span data-ttu-id="fb2ba-227">Пример реализации пользовательского шаблона элемента управления</span><span class="sxs-lookup"><span data-stu-id="fb2ba-227">Example Implementation of a Custom Control Pattern</span></span>

<span data-ttu-id="fb2ba-228">В этом разделе содержится пример кода, демонстрирующий реализацию объектов-оболочек клиента и обработчика шаблона для пользовательского шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb2ba-228">This section contains example code that demonstrates how to implement the client wrapper and pattern handler objects for a custom control pattern.</span></span> <span data-ttu-id="fb2ba-229">В примере реализуется пользовательский шаблон элемента управления, основанный на шаблоне элемента управления [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="fb2ba-229">The example implements a custom control pattern that is based on the [Value](uiauto-implementingvalue.md) control pattern.</span></span>


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fb2ba-230">См. также</span><span class="sxs-lookup"><span data-stu-id="fb2ba-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fb2ba-231">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="fb2ba-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fb2ba-232">Разработка пользовательских свойств, событий и шаблонов элементов управления</span><span class="sxs-lookup"><span data-stu-id="fb2ba-232">Designing Custom Properties, Events, and Control Patterns</span></span>](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[<span data-ttu-id="fb2ba-233">Общие сведения о свойствах автоматизированного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fb2ba-233">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="fb2ba-234">Обзор событий автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fb2ba-234">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="fb2ba-235">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fb2ba-235">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 