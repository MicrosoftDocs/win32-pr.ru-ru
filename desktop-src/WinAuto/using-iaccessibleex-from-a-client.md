---
title: Использование IAccessibleEx из клиента
description: В этом разделе объясняется, как клиенты обращаются к реализации IAccessibleEx сервера и используют его для получения свойств автоматизации пользовательского интерфейса и шаблонов элементов управления для элементов пользовательского интерфейса.
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b14b935bd7ed432ea4d378034763635309213f
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "104414121"
---
# <a name="using-iaccessibleex-from-a-client"></a><span data-ttu-id="e26ea-103">Использование IAccessibleEx из клиента</span><span class="sxs-lookup"><span data-stu-id="e26ea-103">Using IAccessibleEx from a Client</span></span>

<span data-ttu-id="e26ea-104">В этом разделе объясняется, как клиенты обращаются к реализации [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) сервера и используют его для получения свойств автоматизации пользовательского интерфейса и шаблонов элементов управления для элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e26ea-104">This topic explains how clients access the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation of a server and use it to get UI Automation properties and control patterns for UI elements.</span></span>

<span data-ttu-id="e26ea-105">Процедуры и примеры в этом разделе предполагают наличие клиента [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , который уже находится в процессе, и существующего сервера Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="e26ea-105">The procedures and examples in this section assume an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) client that is already in-process, and an existing Microsoft Active Accessibility server.</span></span> <span data-ttu-id="e26ea-106">Кроме того, предполагается, что клиент уже получил объект **IAccessible** с помощью одной из функций платформы специальных возможностей, таких как [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)или [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="e26ea-106">They also assume that the client has already obtained an **IAccessible** object by using one of the accessibility framework functions such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a><span data-ttu-id="e26ea-107">Получение интерфейса IAccessibleEx из интерфейса IAccessible</span><span class="sxs-lookup"><span data-stu-id="e26ea-107">Obtaining an IAccessibleEx Interface from the IAccessible Interface</span></span>

<span data-ttu-id="e26ea-108">Клиент, имеющий интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для доступного объекта, может использовать его для получения соответствующего интерфейса [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e26ea-108">A client that has an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for an accessible object can use it to obtain the corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface by following these steps:</span></span>

-   <span data-ttu-id="e26ea-109">Вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в исходном объекте [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) с идентификатором IID \_ \_ ууидоф (IServiceProvider).</span><span class="sxs-lookup"><span data-stu-id="e26ea-109">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with an IID of \_\_uuidof(IServiceProvider).</span></span>
-   <span data-ttu-id="e26ea-110">Чтобы получить [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), вызовите метод **IServiceProvider:: QueryService** .</span><span class="sxs-lookup"><span data-stu-id="e26ea-110">Call **IServiceProvider::QueryService** to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex).</span></span>

### <a name="handling-the-child-id"></a><span data-ttu-id="e26ea-111">Обработка идентификатора дочернего элемента</span><span class="sxs-lookup"><span data-stu-id="e26ea-111">Handling the Child ID</span></span>

<span data-ttu-id="e26ea-112">Клиенты должны быть подготовлены для серверов с дочерним ИДЕНТИФИКАТОРом, отличным от ЧИЛДИД \_ Self.</span><span class="sxs-lookup"><span data-stu-id="e26ea-112">Clients must be prepared for servers with a child ID other than CHILDID\_SELF.</span></span> <span data-ttu-id="e26ea-113">После получения интерфейса [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) от [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)клиенты должны вызвать [**IAccessibleEx:: жетобжектфорчилд**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) , если дочерний идентификатор не является самочилдид \_ (что указывает на родительский объект).</span><span class="sxs-lookup"><span data-stu-id="e26ea-113">After obtaining an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface from an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), clients must call [**IAccessibleEx::GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) if the child ID is not CHILDID\_SELF (indicating a parent object).</span></span>

<span data-ttu-id="e26ea-114">В следующем примере показано, как получить [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для конкретного объекта [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и идентификатора дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="e26ea-114">The following example shows how to get an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a particular [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span>


```C++
   
HRESULT GetIAccessibleExFromIAccessible(IAccessible * pAcc, long idChild, 
                                           IAccessibleEx ** ppaex)
{
    *ppaex = NULL;

    // First, get IServiceProvider from the IAccessible.
    IServiceProvider * pSp = NULL;
    HRESULT hr = pAcc->QueryInterface(IID_IServiceProvider, (void **) & pSp);
    if(FAILED(hr))
        return hr;
    if(pSp == NULL)
        return E_NOINTERFACE;

    // Next, get the IAccessibleEx for the parent object.
    IAccessibleEx * paex = NULL;
    hr = pSp->QueryService(__uuidof(IAccessibleEx), __uuidof(IAccessibleEx),
                                                                 (void **)&paex);
    pSp->Release();
    if(FAILED(hr))
        return hr;
    if(paex == NULL)
        return E_NOINTERFACE;

    // If this is for CHILDID_SELF, we're done. Otherwise, we have a child ID and 
    // can request the object for child.
    if(idChild == CHILDID_SELF)
    {
        *ppaex = paex;
        return S_OK;
    }
    else
    {
        // Get the IAccessibleEx for the specified child.
        IAccessibleEx * paexChild = NULL;
        hr = paex->GetObjectForChild(idChild, &paexChild);
        paex->Release();
        if(FAILED(hr))
            return hr;
        if(paexChild == NULL)
            return E_NOINTERFACE;
        *ppaex = paexChild;
        return S_OK;
    }
}
```



### <a name="obtaining-the-irawelementprovidersimple-interface"></a><span data-ttu-id="e26ea-115">Получение интерфейса Иравелементпровидерсимпле</span><span class="sxs-lookup"><span data-stu-id="e26ea-115">Obtaining the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="e26ea-116">Если клиент имеет интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , он может использовать QueryInterface для получения интерфейса [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="e26ea-116">If a client has an [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, it can use QueryInterface to get to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, as the following example shows.</span></span>


```C++
HRESULT GetIRawElementProviderFromIAccessible(IAccessible * pAcc, long idChild,
                                                 IRawElementProviderSimple ** ppEl)
{
    * ppEl = NULL;

    // First, get the IAccessibleEx for the IAccessible and child ID pair.
    IAccessibleEx * paex;
    HRESULT hr = GetIAccessibleExFromIAccessible( pAcc, idChild, &paex );
    if(FAILED(hr))
        return hr;

    // Next, use QueryInterface.
    hr = paex->QueryInterface(__uuidof(IRawElementProviderSimple), (void **)ppEl);
    paex->Release();
    return hr;
}
```



### <a name="retrieving-control-patterns"></a><span data-ttu-id="e26ea-117">Получение шаблонов элементов управления</span><span class="sxs-lookup"><span data-stu-id="e26ea-117">Retrieving Control Patterns</span></span>

<span data-ttu-id="e26ea-118">Если у клиента есть доступ к интерфейсу [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , он может получить интерфейсы шаблона элемента управления, которые были реализованы поставщиками, а затем вызвать методы для этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="e26ea-118">If a client has access to the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface, it can retrieve control pattern interfaces that have been implemented by providers, and can then call methods on those interfaces.</span></span> <span data-ttu-id="e26ea-119">В приведенном ниже примере показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="e26ea-119">The following example shows how to do this.</span></span>


```C++
// Helper function to get a pattern interface from an IAccessible and child ID 
// pair. Gets the IAccessibleEx, then calls GetPatternObject and QueryInterface.
HRESULT GetPatternFromIAccessible(IAccessible * pAcc, long idChild,
                                     PATTERNID patternId, REFIID iid, void ** ppv)
{
    // First, get the IAccesibleEx for this IAccessible and child ID pair.
    IRawElementProviderSimple * pel;
    HRESULT hr = GetIRawElementProviderSimpleFromIAccessible(pAcc, idChild, &pel);
    if(FAILED(hr))
        return hr;
    if(pel == NULL)
        return E_NOINTERFACE;

    // Now get the pattern object.
    IUnknown * pPatternObject = NULL;
    hr = pel->GetPatternProvider(patternId, &pPatternObject);
    pel->Release();
    if(FAILED(hr))
        return hr;
    if(pPatternObject == NULL)
        return E_NOINTERFACE;

    // Finally, use QueryInterface to get the correct interface type.
    hr = pPatternObject->QueryInterface(iid, ppv);
    pPatternObject->Release();
    if(*ppv == NULL)
        return E_NOINTERFACE;
    return hr;
}

HRESULT CallInvokePatternMethod(IAccessible * pAcc, long idChild)
{
    IInvokeProvider * pPattern;
    HRESULT hr = GetPatternFromIAccessible(pAcc, varChild,
                                  UIA_InvokePatternId, __uuidof(IInvokeProvider),
                                  (void **)&pPattern);
    if(FAILED(hr))
        return hr;

    hr = pPattern->Invoke();
    pPattern->Release();
    return hr;
}
```



### <a name="retrieving-property-values"></a><span data-ttu-id="e26ea-120">Получение значений свойств</span><span class="sxs-lookup"><span data-stu-id="e26ea-120">Retrieving Property Values</span></span>

<span data-ttu-id="e26ea-121">Если у клиента есть доступ к [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), он может получить значения свойств.</span><span class="sxs-lookup"><span data-stu-id="e26ea-121">If a client has access to [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), it can retrieve property values.</span></span> <span data-ttu-id="e26ea-122">В следующем примере показано, как получить значения для свойств AutomationId и Лабеледби Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="e26ea-122">The following example shows how to get values for the AutomationId and LabeledBy Microsoft UI Automation properties.</span></span>


```C++
#include <initguid.h>
#include <uiautomationcoreapi.h> // Includes the UI Automation property GUID definitions.
#include <uiautomationcoreids.h> // Includes definitions of pattern/property IDs.

// Assume we already have a IRawElementProviderSimple * pEl.

VARIANT varValue;

// Get AutomationId property:
varValue.vt = VT_EMPTY;
HRESULT hr = pEl->GetPropertyValue(UIA_AutomationIdPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_BSTR)
    {
        // AutomationId is varValue.bstrVal.
    }
    VariantClear(&varValue);
}


// Get LabeledBy property:
varValue.vt = VT_EMPTY;
hr = pEl->GetPropertyValue(UIA_LabeledByPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_UNKNOWN || varValue.punkVal != NULL)
    {
        // Use QueryInterface to get IRawElementProviderSimple.
        IRawElementProviderSimple * pElLabel = NULL;
        hr = varValue.punkVal->QueryInterface(__uuidof(IRawElementProviderSimple),
                                              (void**)& pElLabel);
        if (SUCCEEDED(hr))
        {
            if(pElLabel != NULL)
            {
            // Use the pElLabel pointer here.
            pElLabel ->Release();
            }
        }
    }
    VariantClear(&varValue);
}
```



<span data-ttu-id="e26ea-123">Предыдущий пример применяется к свойствам, не связанным с шаблоном элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e26ea-123">The preceding example applies to properties that are not associated with a control pattern.</span></span> <span data-ttu-id="e26ea-124">Чтобы получить доступ к свойствам шаблона управления, клиент должен получить и использовать интерфейс шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e26ea-124">To access control pattern properties, a client must obtain and use a control pattern interface.</span></span>

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a><span data-ttu-id="e26ea-125">Получение интерфейса IAccessible из интерфейса Иравелементпровидерсимпле</span><span class="sxs-lookup"><span data-stu-id="e26ea-125">Retrieving an IAccessible Interface from an IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="e26ea-126">Если клиент получает интерфейс [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для элемента пользовательского интерфейса, клиент может использовать этот интерфейс для получения соответствующего интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента.</span><span class="sxs-lookup"><span data-stu-id="e26ea-126">If a client obtains the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface for a UI element, the client can use that interface to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="e26ea-127">Это полезно, если клиенту требуется доступ к свойствам Microsoft Active Accessibility элемента.</span><span class="sxs-lookup"><span data-stu-id="e26ea-127">This is useful if the client needs to access the Microsoft Active Accessibility properties for the element.</span></span>

<span data-ttu-id="e26ea-128">Клиент может получить интерфейс [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) как значение свойства (например, путем вызова [**Иравелементпровидерсимпле:: жетпропертивалуе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) с UIA \_ лабеледбипропертид) или как элемент, полученный методом (например, путем вызова [**ISelectionProvider::-SELECT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) для получения массива интерфейсов **IRawElementProviderSimple** из выбранных элементов).</span><span class="sxs-lookup"><span data-stu-id="e26ea-128">A client can obtain the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface as a property value (for example, by calling [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) with UIA\_LabeledByPropertyId), or as an item retrieved by a method (for example, by calling [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) to retrieve an array of **IRawElementProviderSimple** interfaces of selected elements).</span></span> <span data-ttu-id="e26ea-129">После получения интерфейса **иравелементпровидерсимпле** клиент может использовать его для получения соответствующего [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e26ea-129">After obtaining the **IRawElementProviderSimple** interface, a client can use it to obtain a corresponding [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) by following these steps:</span></span>

-   <span data-ttu-id="e26ea-130">Попытка использовать QueryInterface для получения интерфейса [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="e26ea-130">Attempt to use QueryInterface to get the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>
-   <span data-ttu-id="e26ea-131">При сбое QueryInterface вызовите [**IAccessibleEx:: конвертретурнеделемент**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) в экземпляре [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , из которого изначально было получено свойство.</span><span class="sxs-lookup"><span data-stu-id="e26ea-131">If QueryInterface fails, call [**IAccessibleEx::ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) on the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance from which the property was originally obtained.</span></span>
-   <span data-ttu-id="e26ea-132">Вызовите метод [**жетиакцессиблепаир**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) в новом экземпляре [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) , чтобы получить идентификатор класса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) интерфае и ИД дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="e26ea-132">Call the [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) method on the new [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance to obtain an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfae and child ID.</span></span>

<span data-ttu-id="e26ea-133">В следующем фрагменте кода показано, как получить интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) из ранее полученного интерфейса [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) .</span><span class="sxs-lookup"><span data-stu-id="e26ea-133">The following code snippet demonstrates how to obtain the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface from a previously-obtained [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface.</span></span>


```C++
// IRawElementProviderSimple * pVal - an element returned by a property or method
// from another IRawElementProviderSimple.

IAccessible * pAcc = NULL;
long idChild;

// First, try to use QueryInterface to get the IAccessibleEx interface.
IAccessibleEx * pAccEx;
HRESULT hr = pVal->QueryInterface(__uuidof(IAccessibleEx), (void**)&pAccEx);
if (SUCCEEDED(hr)
{
    if (!pAccEx)
    {
        // If QueryInterface fails, and the IRawElementProviderSimple was 
              // obtained as a property or return value from another 
              // IRawElementProviderSimple, pass it to the 
              // IAccessibleEx::ConvertReturnedValue method of the
        // originating element.

        pAccExOrig->ConvertReturnedElement(pVal, &pAccEx);
    }

    if (pAccEx)
    {
        // Call GetIAccessiblePair to get an IAccessible interface and 
              // child ID.
        pAccEx->GetIAccessiblePair(&pAcc, &idChild);
    }

    // Finally, use the IAccessible interface and child ID.
    if (pAcc)
    {
        // Use IAccessible methods to get further information about this UI
              // element, or pass it to existing code that works in terms of 
              // IAccessible.
        ...
    }
}    
```



 

 