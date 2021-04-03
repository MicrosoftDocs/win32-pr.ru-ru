---
title: Добавление функций автоматизации пользовательского интерфейса на серверы Active Accessibility
description: Элементы управления, у которых нет поставщика Microsoft UI Automation, но реализующие IAccessible, можно легко обновить, чтобы обеспечить некоторые функции автоматизации пользовательского интерфейса, реализуя интерфейс IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Модель автоматизации пользовательского интерфейса, Active Accessibility серверы
- Модель автоматизации пользовательского интерфейса, серверы Microsoft Active Accessibility
- Модель автоматизации пользовательского интерфейса, IAccessible
- Модель автоматизации пользовательского интерфейса, IAccessibleEx
- Автоматизация пользовательского интерфейса, предоставление IAccessibleEx
- Модель автоматизации пользовательского интерфейса, реализация IAccessibleEx
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- предоставление IAccessibleEx
- Реализация IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987566"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a><span data-ttu-id="da988-115">Добавление функций автоматизации пользовательского интерфейса на серверы Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="da988-115">Adding UI Automation Functionality to Active Accessibility Servers</span></span>

<span data-ttu-id="da988-116">Элементы управления, у которых нет поставщика Microsoft UI Automation, но реализующие [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , можно легко обновить, чтобы обеспечить некоторые функции автоматизации пользовательского интерфейса, реализуя интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="da988-116">Controls that do not have a Microsoft UI Automation provider but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) can easily be upgraded to provide some UI Automation functionality, by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="da988-117">Этот интерфейс позволяет элементу управления предоставлять свойства автоматизации пользовательского интерфейса и шаблоны элементов управления без необходимости полной реализации интерфейсов поставщика автоматизации пользовательского интерфейса, таких как [**иравелементпровидерфрагмент**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="da988-117">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="da988-118">Чтобы реализовать **IAccessibleEx**, базовая иерархия объектов Microsoft Active Accessibility не должна содержать ошибок или несоответствий (например, дочернего объекта, родительский объект которого не является дочерним) и не должен конфликтовать со спецификациями модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="da988-118">To implement **IAccessibleEx**, the baseline Microsoft Active Accessibility object hierarchy must contain no errors or inconsistencies (such as a child object whose parent object does not list it as a child), and must not conflict with UI Automation specifications.</span></span> <span data-ttu-id="da988-119">Если иерархия объектов Microsoft Active Accessibility соответствует этим требованиям, это хороший кандидат на добавление функциональных возможностей с помощью **IAccessibleEx**; в противном случае необходимо реализовать автоматизацию пользовательского интерфейса отдельно или параллельно с реализацией Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="da988-119">If the Microsoft Active Accessibility object hierarchy meets these requirements, it is a good candidate for adding functionality by using **IAccessibleEx**; otherwise, you must implement UI Automation alone or alongside the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="da988-120">Возьмем вариант пользовательского элемента управления, имеющего значение Range.</span><span class="sxs-lookup"><span data-stu-id="da988-120">Take the case of a custom control that has a range value.</span></span> <span data-ttu-id="da988-121">Сервер Microsoft Active Accessibility для элемента управления определяет его роль и может возвращать его текущее значение, но не имеет средств для возврата минимального и максимального значений элемента управления, так как эти свойства не определены в Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="da988-121">The Microsoft Active Accessibility server for the control defines its role, and is able to return its current value, but lacks the means to return the minimum and maximum values of the control, because these properties are not defined in Microsoft Active Accessibility.</span></span> <span data-ttu-id="da988-122">Клиент автоматизации пользовательского интерфейса может получить роль элемента управления, текущее значение и другие свойства Microsoft Active Accessibility, так как ядро автоматизации пользовательского интерфейса может получить их через [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="da988-122">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="da988-123">Однако без доступа к интерфейсу [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) в объекте модель автоматизации пользовательского интерфейса также не может получить максимальное и минимальное значения.</span><span class="sxs-lookup"><span data-stu-id="da988-123">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="da988-124">Разработчик элемента управления может предоставить полный поставщик автоматизации пользовательского интерфейса для элемента управления, но это означает дублирование большинства существующих функциональных возможностей реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : например, навигации и общих свойств.</span><span class="sxs-lookup"><span data-stu-id="da988-124">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="da988-125">Вместо этого разработчик может по-прежнему использовать **IAccessible** для предоставления этой функции, добавляя поддержку свойств конкретного элемента управления через [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="da988-125">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

<span data-ttu-id="da988-126">Для обновления пользовательского элемента управления требуются следующие основные шаги:</span><span class="sxs-lookup"><span data-stu-id="da988-126">Updating the custom control requires these main steps:</span></span>

-   <span data-ttu-id="da988-127">Реализуйте [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) для доступного объекта, чтобы интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) можно было найти в этом или отдельном объекте.</span><span class="sxs-lookup"><span data-stu-id="da988-127">Implement [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="da988-128">Реализуйте [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для доступного объекта.</span><span class="sxs-lookup"><span data-stu-id="da988-128">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="da988-129">Создавайте различные объекты со специальными возможностями для всех дочерних элементов Microsoft Active Accessibility, которые в Microsoft Active Accessibility могли быть представлены интерфейсом [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) родительского объекта (например, элементы списка).</span><span class="sxs-lookup"><span data-stu-id="da988-129">Create distinct accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility might have been represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="da988-130">Реализуйте [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="da988-130">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="da988-131">Реализуйте [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для всех доступных объектов.</span><span class="sxs-lookup"><span data-stu-id="da988-131">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="da988-132">Реализуйте соответствующие интерфейсы шаблона элемента управления в доступных объектах.</span><span class="sxs-lookup"><span data-stu-id="da988-132">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

<span data-ttu-id="da988-133">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="da988-133">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="da988-134">Предоставление IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="da988-134">Exposing IAccessibleEx</span></span>](#exposing-iaccessibleex)
-   [<span data-ttu-id="da988-135">Реализация IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="da988-135">Implementing IAccessibleEx</span></span>](#implementing-iaccessibleex)
-   [<span data-ttu-id="da988-136">См. также</span><span class="sxs-lookup"><span data-stu-id="da988-136">Related topics</span></span>](#related-topics)

## <a name="exposing-iaccessibleex"></a><span data-ttu-id="da988-137">Предоставление IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="da988-137">Exposing IAccessibleEx</span></span>

<span data-ttu-id="da988-138">Поскольку реализация [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для элемента управления может находиться в отдельном объекте, клиентские приложения не могут использовать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="da988-138">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="da988-139">Вместо этого клиенты должны вызывать метод [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da988-139">Instead, clients are expected to call [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span></span> <span data-ttu-id="da988-140">В следующем примере реализации этого метода предполагается, что **IAccessibleEx** не реализован в отдельном объекте. Поэтому метод просто вызывается через **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="da988-140">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a><span data-ttu-id="da988-141">Реализация IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="da988-141">Implementing IAccessibleEx</span></span>

<span data-ttu-id="da988-142">Метод [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , который наиболее интересен, — это [**жетобжектфорчилд**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span><span class="sxs-lookup"><span data-stu-id="da988-142">The method of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) that is of most interest is [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span></span> <span data-ttu-id="da988-143">Этот метод дает серверу Microsoft Active Accessibility возможность создать доступный объект (который предоставляет, как минимум, **IAccessibleEx**) для дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="da988-143">This method gives the Microsoft Active Accessibility server an opportunity to create an accessible object (one that exposes, at a minimum, **IAccessibleEx**) for a child item.</span></span> <span data-ttu-id="da988-144">В Microsoft Active Accessibility дочерние элементы обычно не представляются как объекты со специальными возможностями, но являются дочерними объектами доступного объекта.</span><span class="sxs-lookup"><span data-stu-id="da988-144">In Microsoft Active Accessibility, child items typically are not represented as accessible objects but as children of an accessible object.</span></span> <span data-ttu-id="da988-145">Однако, поскольку модель автоматизации пользовательского интерфейса требует, чтобы каждый элемент представлялся отдельным доступным объектом, **жетобжектфорчилд** должен создать отдельный объект для каждого дочернего элемента по запросу.</span><span class="sxs-lookup"><span data-stu-id="da988-145">However, because UI Automation requires that each element be represented by a separate accessible object, **GetObjectForChild** must create a separate object for each child on demand.</span></span>

<span data-ttu-id="da988-146">В следующем примере реализации возвращается доступный объект для элемента в пользовательском представлении списка.</span><span class="sxs-lookup"><span data-stu-id="da988-146">The following example implementation returns an accessible object for an item in a custom list view.</span></span>


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



<span data-ttu-id="da988-147">Полный пример реализации см. в разделе [обеспечение доступности настраиваемых элементов управления, часть 5. Использование IAccessibleEx для добавления поддержки модели автоматизации пользовательского интерфейса в пользовательский элемент управления](/previous-versions/msdn10/cc307850(v=msdn.10)) в MSDN.</span><span class="sxs-lookup"><span data-stu-id="da988-147">For a complete sample implementation, see [Making Custom Controls Accessible, Part 5: Using IAccessibleEx to Add UI Automation Support to a Custom Control](/previous-versions/msdn10/cc307850(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da988-148">См. также</span><span class="sxs-lookup"><span data-stu-id="da988-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da988-149">Рекомендации программиста поставщика модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="da988-149">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 