---
title: Реализация IAccessibleEx для поставщиков
description: В этом разделе объясняется, как добавить возможности поставщика автоматизации пользовательского интерфейса Майкрософт на сервер Microsoft Active Accessibility, реализовав интерфейс IAccessibleEx.
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710296"
---
# <a name="implementing-iaccessibleex-for-providers"></a><span data-ttu-id="18061-103">Реализация IAccessibleEx для поставщиков</span><span class="sxs-lookup"><span data-stu-id="18061-103">Implementing IAccessibleEx for Providers</span></span>

<span data-ttu-id="18061-104">В этом разделе объясняется, как добавить возможности поставщика автоматизации пользовательского интерфейса Майкрософт на сервер Microsoft Active Accessibility, реализовав интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="18061-104">This section explains how to add Microsoft UI Automation provider capabilities to a Microsoft Active Accessibility server by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>

<span data-ttu-id="18061-105">Перед реализацией [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)учитывайте следующие требования.</span><span class="sxs-lookup"><span data-stu-id="18061-105">Before implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), consider the following requirements:</span></span>

-   <span data-ttu-id="18061-106">Базовая иерархия объектов Microsoft Active Accessibility со специальными возможностями должна быть чистой.</span><span class="sxs-lookup"><span data-stu-id="18061-106">The baseline Microsoft Active Accessibility accessible object hierarchy must be clean.</span></span> <span data-ttu-id="18061-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) не может устранить проблемы с существующими иерархиями доступных объектов.</span><span class="sxs-lookup"><span data-stu-id="18061-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) cannot correct problems with existing accessible object hierarchies.</span></span> <span data-ttu-id="18061-108">Перед реализацией **IAccessibleEx** необходимо исправить все проблемы, связанные со структурой объектной модели, в реализации Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="18061-108">Any problems with the object model structure must be corrected in the Microsoft Active Accessibility implementation before implementing **IAccessibleEx**.</span></span>
-   <span data-ttu-id="18061-109">Реализация [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) должна соответствовать спецификации Microsoft Active Accessibility и спецификации автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="18061-109">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation must comply with both the Microsoft Active Accessibility specification and the UI Automation specification.</span></span> <span data-ttu-id="18061-110">Доступны средства для проверки соответствия в обеих спецификациях.</span><span class="sxs-lookup"><span data-stu-id="18061-110">Tools are available to validate compliance under both specifications.</span></span> <span data-ttu-id="18061-111">Дополнительные сведения см. в разделе [средства тестирования](testing-tools.md) и [Автоматизация пользовательского интерфейса Проверка платформы автоматизации тестирования (UIA Verify)](https://www.codeplex.com/UIAutomationVerify/).</span><span class="sxs-lookup"><span data-stu-id="18061-111">For more information, see [Testing Tools](testing-tools.md) and [UI Automation Verify (UIA Verify) Test Automation Framework](https://www.codeplex.com/UIAutomationVerify/).</span></span>

<span data-ttu-id="18061-112">Для реализации [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) необходимо выполнить следующие основные действия.</span><span class="sxs-lookup"><span data-stu-id="18061-112">Implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requires these main steps:</span></span>

-   <span data-ttu-id="18061-113">Реализуйте **IServiceProvider** для доступного объекта, чтобы интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) можно было найти в этом или отдельном объекте.</span><span class="sxs-lookup"><span data-stu-id="18061-113">Implement **IServiceProvider** on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="18061-114">Реализуйте [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для доступного объекта.</span><span class="sxs-lookup"><span data-stu-id="18061-114">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="18061-115">Создайте объекты со специальными возможностями для любых дочерних элементов Microsoft Active Accessibility, которые в Microsoft Active Accessibility представлены интерфейсом [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) родительского объекта (например, элементы списка).</span><span class="sxs-lookup"><span data-stu-id="18061-115">Create accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility are represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="18061-116">Реализуйте [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="18061-116">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="18061-117">Реализуйте [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для всех доступных объектов.</span><span class="sxs-lookup"><span data-stu-id="18061-117">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="18061-118">Реализуйте соответствующие интерфейсы шаблона элемента управления в доступных объектах.</span><span class="sxs-lookup"><span data-stu-id="18061-118">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

### <a name="implementing-the-iserviceprovider-interface"></a><span data-ttu-id="18061-119">Реализация интерфейса IServiceProvider</span><span class="sxs-lookup"><span data-stu-id="18061-119">Implementing the IServiceProvider Interface</span></span>

<span data-ttu-id="18061-120">Поскольку реализация [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для элемента управления может находиться в отдельном объекте, клиентские приложения не могут использовать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="18061-120">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="18061-121">Вместо этого клиенты должны вызывать метод **IServiceProvider:: QueryService**.</span><span class="sxs-lookup"><span data-stu-id="18061-121">Instead, clients are expected to call **IServiceProvider::QueryService**.</span></span> <span data-ttu-id="18061-122">В следующем примере реализации этого метода предполагается, что **IAccessibleEx** не реализован в отдельном объекте. Поэтому метод просто вызывается через **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="18061-122">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
           
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (ppvObject == NULL)
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
        return E_NOINTERFACE;
    }
};      
```



### <a name="implementing-the-iaccessibleex-interface"></a><span data-ttu-id="18061-123">Реализация интерфейса IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="18061-123">Implementing the IAccessibleEx Interface</span></span>

<span data-ttu-id="18061-124">В Microsoft Active Accessibility элемент пользовательского интерфейса всегда определяется интерфейсом [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и идентификатором дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="18061-124">In Microsoft Active Accessibility, a UI element is always identified by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and a child ID.</span></span> <span data-ttu-id="18061-125">Один экземпляр **IAccessible** может представлять несколько элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="18061-125">A single instance of **IAccessible** can represent multiple UI elements.</span></span>

<span data-ttu-id="18061-126">Так как каждый экземпляр [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) представляет только один элемент пользовательского интерфейса, каждая пара идентификаторов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и Child должна быть сопоставлена с одним экземпляром **IAccessibleEx** .</span><span class="sxs-lookup"><span data-stu-id="18061-126">Because each [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance represents only a single UI element, each [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair must be mapped to a single **IAccessibleEx** instance.</span></span> <span data-ttu-id="18061-127">**IAccessibleEx** содержит два метода для решения этого сопоставления:</span><span class="sxs-lookup"><span data-stu-id="18061-127">**IAccessibleEx** includes two methods to handle this mapping:</span></span>

-   <span data-ttu-id="18061-128">[**Жетобжектфорчилд**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)— получает интерфейс [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) для указанного дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="18061-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)—Retrieves the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface for the specified child.</span></span> <span data-ttu-id="18061-129">Этот метод возвращает **значение NULL** , если реализация **IAccessibleEx** не распознает указанный идентификатор дочернего элемента, не имеет **IAccessibleEx** для указанного дочернего элемента или представляет дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="18061-129">This method returns **NULL** if the **IAccessibleEx** implementation does not recognize the specified child ID, does not have an **IAccessibleEx** for the specified child, or represents a child element.</span></span>
-   <span data-ttu-id="18061-130">[**Жетиакцессиблепаир**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)— Извлекает интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и идентификатор потомка для элемента [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="18061-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)—Retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and child ID for the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) element.</span></span> <span data-ttu-id="18061-131">Для реализаций **IAccessible** , не использующих идентификатор дочернего элемента, этот метод извлекает соответствующий объект **IAccessible** и чилдид \_ себя.</span><span class="sxs-lookup"><span data-stu-id="18061-131">For **IAccessible** implementations that do not use a child ID, this method retrieves the corresponding **IAccessible** object and CHILDID\_SELF.</span></span>

<span data-ttu-id="18061-132">В следующем примере показана реализация методов [**жетобжектфорчилд**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) и [**жетиакцессиблепаир**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) для элемента в пользовательском представлении списка.</span><span class="sxs-lookup"><span data-stu-id="18061-132">The following example shows the implementation of the [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) and [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) methods for an item in a custom list view.</span></span> <span data-ttu-id="18061-133">Методы позволяют модели автоматизации пользовательского интерфейса сопоставить пару ИДЕНТИФИКАТОРов [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) и Child с соответствующим экземпляром [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="18061-133">The methods enable UI Automation to map the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair to a corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance.</span></span>


```C++
           
HRESULT CListboxAccessibleObject::GetObjectForChild(
    long idChild, IAccessibleEx **ppRetVal)
{ 
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;
    HRESULT hr = ValidateChildId(vChild);
    if (FAILED(hr))
    {
        return E_INVALIDARG;
    }
    // List item accessible objects are stored as an array of
    // pointers; for the purpose of this example it is assumed that 
    // the list contents will not change. Accessible objects are
    // created only when needed.
    if (itemProviders[idChild - 1] == NULL)
    {
        // Create an object that supports UI Automation and
        // IAccessibleEx for the item.
        itemProviders[idChild - 1] = 
          new CListItemAccessibleObject(idChild, 
          g_pListboxControl);
        if (itemProviders[idChild - 1] == NULL)
        {
            return E_OUTOFMEMORY;
        }
    }
    IAccessibleEx* pAccEx = static_cast<IAccessibleEx*>
      (itemProviders[idChild - 1]);
    if (pAccEx != NULL)
    {
      pAccEx->AddRef();
    }
    *ppRetVal = pAccEx;
    return S_OK; 
}

HRESULT CListItemAccessibleObject::GetIAccessiblePair(
    IAccessible **ppAcc, long *pidChild)
{ 
    if (ppAcc == NULL || pidChild == NULL)
    {
        return E_INVALIDARG;   
    }

                CListboxAccessibleObject* pParent = 
        m_control->GetAccessibleObject();

    HRESULT hr = pParent->QueryInterface( 
        __uuidof(IAccessible), (void**)ppAcc);
    if (FAILED(hr))
    {
        *pidChild = 0;
        return E_NOINTERFACE;
    }
    *pidChild = m_childID; 
    return S_OK; 
}
}
```



<span data-ttu-id="18061-134">Если в реализации доступного объекта не используется идентификатор дочернего элемента, методы могут по-прежнему быть реализованы, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="18061-134">If an accessible object implementation does not use a child ID, the methods can still be implemented as shown in the following code snippet.</span></span>


```C++
           

    // This sample implements IAccessibleEx on the same object; it could use a tear-off
    // or inner object instead.
    class MyAccessibleImpl: public IAccessible,
                        public IAccessibleEx,
                        public IRawElementProviderSimple
    {
    public:
    ...
   HRESULT STDMETHODCALLTYPE GetObjectForChild( long idChild, IAccessibleEx **ppRetVal )
    {
        // This implementation does not support child IDs.
        *ppRetVal = NULL;
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE GetIAccessiblePair( IAccessible ** ppAcc, long * pidChild )
    {
        // This implementation assumes that IAccessibleEx is implemented on same object as
        // IAccessible.
        *ppAcc = static_cast<IAccessible *>(this);
        (*ppAcc)->AddRef();
        *pidChild = CHILDID_SELF;
        return S_OK;
    }
```



### <a name="implement-the-irawelementprovidersimple-interface"></a><span data-ttu-id="18061-135">Реализация интерфейса Иравелементпровидерсимпле</span><span class="sxs-lookup"><span data-stu-id="18061-135">Implement the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="18061-136">Серверы используют [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) для предоставления сведений о свойствах и шаблонах элементов управления модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="18061-136">Servers use [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) to expose information about UI Automation properties and control patterns.</span></span> <span data-ttu-id="18061-137">**Иравелементпровидерсимпле** включает следующие методы:</span><span class="sxs-lookup"><span data-stu-id="18061-137">**IRawElementProviderSimple** includes the following methods:</span></span>

-   <span data-ttu-id="18061-138">[**Жетпаттернпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)— этот метод используется для предоставления интерфейсов шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="18061-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)—This method is used to expose control pattern interfaces.</span></span> <span data-ttu-id="18061-139">Он возвращает объект, который поддерживает указанный шаблон элемента управления, или **значение NULL** , если шаблон элемента управления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="18061-139">It returns an object that supports the specified control pattern, or **NULL** if the control pattern is not supported.</span></span>
-   <span data-ttu-id="18061-140">[**Жетпропертивалуе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)— этот метод используется для предоставления значений свойств модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="18061-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)—This method is used to expose UI Automation property values.</span></span>
-   <span data-ttu-id="18061-141">[**Хостравелементпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)— этот метод не используется с реализациями [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="18061-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>
-   <span data-ttu-id="18061-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)— этот метод не используется с реализациями [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="18061-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>

<span data-ttu-id="18061-143">Сервер [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) предоставляет шаблоны элементов управления, реализуя [**Иравелементпровидерсимпле:: жетпаттернпровидер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span><span class="sxs-lookup"><span data-stu-id="18061-143">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server exposes control patterns by implementing [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span></span> <span data-ttu-id="18061-144">Этот метод принимает целочисленный параметр, указывающий шаблон элемента управления.</span><span class="sxs-lookup"><span data-stu-id="18061-144">This method takes an integer parameter that specifies the control pattern.</span></span> <span data-ttu-id="18061-145">Сервер возвращает **значение NULL** , если шаблон не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="18061-145">The server returns **NULL** if the pattern is not supported.</span></span> <span data-ttu-id="18061-146">Если интерфейс шаблона элемента управления поддерживается, серверы возвращают [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , а клиент вызывает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения соответствующего шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="18061-146">If the control pattern interface is supported, servers return an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) and the client then calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the appropriate control pattern.</span></span>

<span data-ttu-id="18061-147">Сервер [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) может поддерживать свойства модели автоматизации пользовательского интерфейса (например, Лабеледби и исрекуиредфорформ), реализуя [**Иравелементпровидерсимпле:: жетпропертивалуе**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) и предоставляя целое число PROPERTYID, идентифицирующее свойство как параметр.</span><span class="sxs-lookup"><span data-stu-id="18061-147">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server can support UI Automation properties (such as LabeledBy, and IsRequiredForForm) by implementing [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) and supplying an integer PROPERTYID identifying the property as a parameter.</span></span> <span data-ttu-id="18061-148">Этот метод применим только к свойствам модели автоматизации пользовательского интерфейса, которые не включены в интерфейс шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="18061-148">This technique applies only to UI Automation properties that are not included in a control pattern interface.</span></span> <span data-ttu-id="18061-149">Свойства, связанные с интерфейсом шаблона элемента управления, доступны через метод интерфейса шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="18061-149">Properties associated with a control pattern interface are exposed through the control pattern interface method.</span></span> <span data-ttu-id="18061-150">Например, свойство со свойством, которое было выбрано из шаблона элемента управления [SelectionItem](uiauto-implementingselectionitem.md) , было бы предоставлено с помощью [**иселектионитемпровидер:: Get \_**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span><span class="sxs-lookup"><span data-stu-id="18061-150">For example, the IsSelected property from the [SelectionItem](uiauto-implementingselectionitem.md) control pattern would be exposed with [**ISelectionItemProvider::get\_IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span></span>

 

 