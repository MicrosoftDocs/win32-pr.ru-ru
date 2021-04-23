---
title: Использование MSAA для обеспечения возможности доступа к безоконному элементу управления ActiveX
description: Описывает, как использовать Microsoft Active Accessibility \ 32; API, чтобы обеспечить доступность элемента управления Microsoft ActiveX без окон для клиентских приложений с поддержкой специальных возможностей (AT).
ms.assetid: 30F874F9-EA45-4365-8798-FEA011C62DA9
keywords:
- Элемент управления ActiveX, Специальные возможности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a76aa72fadef502a6a4319284ab34fdd5214d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700903"
---
# <a name="use-msaa-to-make-a-windowless-activex-control-accessible"></a><span data-ttu-id="289be-104">Использование MSAA для обеспечения возможности доступа к безоконному элементу управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="289be-104">Use MSAA to make a windowless ActiveX control accessible</span></span>

<span data-ttu-id="289be-105">Описание использования Microsoft Active Accessibility API для обеспечения доступности элемента управления Microsoft ActiveX без окон для клиентских приложений с поддержкой специальных возможностей (AT).</span><span class="sxs-lookup"><span data-stu-id="289be-105">Describes how to use the Microsoft Active Accessibility API to ensure that your windowless Microsoft ActiveX control is accessible to assistive technology (AT) client applications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="289be-106">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="289be-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="289be-107">Технологии</span><span class="sxs-lookup"><span data-stu-id="289be-107">Technologies</span></span>

-   [<span data-ttu-id="289be-108">Элементы управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="289be-108">ActiveX Controls</span></span>](/windows/desktop/com/activex-controls)
-   [<span data-ttu-id="289be-109">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="289be-109">Microsoft Active Accessibility</span></span>](microsoft-active-accessibility.md)

### <a name="prerequisites"></a><span data-ttu-id="289be-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="289be-110">Prerequisites</span></span>

-   <span data-ttu-id="289be-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="289be-111">C/C++</span></span>
-   <span data-ttu-id="289be-112">Программирование Microsoft Win32 и объектной модели компонентов (COM)</span><span class="sxs-lookup"><span data-stu-id="289be-112">Microsoft Win32 and Component Object Model (COM) programming</span></span>
-   <span data-ttu-id="289be-113">Элементы управления ActiveX без окон</span><span class="sxs-lookup"><span data-stu-id="289be-113">Windowless ActiveX Controls</span></span>
-   <span data-ttu-id="289be-114">Серверы Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="289be-114">Microsoft Active Accessibility servers</span></span>

## <a name="instructions"></a><span data-ttu-id="289be-115">Инструкции</span><span class="sxs-lookup"><span data-stu-id="289be-115">Instructions</span></span>

### <a name="step-1-implement-the-iaccessible-interface"></a><span data-ttu-id="289be-116">Шаг 1. Реализация интерфейса IAccessible.</span><span class="sxs-lookup"><span data-stu-id="289be-116">Step 1: Implement the IAccessible interface.</span></span>

<span data-ttu-id="289be-117">Чтобы сделать безоконный элемент управления ActiveX доступным, необходимо реализовать интерфейс Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) так же, как и для элемента управления на основе окна, за исключением случаев, описанных в следующих шагах.</span><span class="sxs-lookup"><span data-stu-id="289be-117">To make your windowless ActiveX control accessible, you must implement the Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, just as you would for a window-based control, except as described in the following steps.</span></span> <span data-ttu-id="289be-118">Дополнительные сведения о реализации **IAccessible** см. в разделе " [рекомендации разработчика для Active Accessibility серверов](developer-s-guide-for-active-accessibility-servers.md)".</span><span class="sxs-lookup"><span data-stu-id="289be-118">For more information about implementing **IAccessible**, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

### <a name="step-2-implement-the-iserviceprovider-interface"></a><span data-ttu-id="289be-119">Шаг 2. Реализация интерфейса IServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="289be-119">Step 2: Implement the IServiceProvider interface.</span></span>

<span data-ttu-id="289be-120">Когда клиент запрашивает сведения о специальных возможностях для безоконного управления, контейнер вызывает метод [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) элемента управления, чтобы получить указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="289be-120">When a client requests accessibility information about your windowless control, the container calls your control's [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method to retrieve the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="289be-121">В этом примере показано, как реализовать метод [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="289be-121">This example shows how to implement the [**QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) method.</span></span>


```C++
STDMETHODIMP CMyAccessibleMSAAControl::QueryService(REFGUID guidService, 
        REFIID riid, void **ppvObject)
{      
    if (ppvObject == NULL)
    {
        return E_INVALIDARG;
    }

    *ppvObject = NULL;  
    HRESULT hr = E_FAIL;  

    if (guidService == __uuidof(IAccessible))
    {  
        hr = QueryInterface(riid, ppvObject);  
    }  
    return hr;  
}
```



### <a name="step-3-delegate-iaccessibleget_accparent-method-calls-to-the-control-sites-iaccessiblewindowlesssitegetparentaccessible-method"></a><span data-ttu-id="289be-122">Шаг 3. Делегат IAccessible:: Get \_ аккпарент вызывает метод иакцессиблевиндовлесссите:: жетпарентакцессибле сайта элемента управления.</span><span class="sxs-lookup"><span data-stu-id="289be-122">Step 3: Delegate IAccessible::get\_accParent method calls to the control site's IAccessibleWindowlessSite::GetParentAccessible method.</span></span>

<span data-ttu-id="289be-123">Когда клиент запрашивает родительский объект безоконного элемента управления, контейнер вызывает метод [**IAccessible:: Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="289be-123">When a client requests the parent object of your windowless control, the container calls your control's [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span> <span data-ttu-id="289be-124">Реализация **Get \_ аккпарент** должна делегировать методу [**иакцессиблевиндовлесссите:: жетпарентакцессибле**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) контейнера.</span><span class="sxs-lookup"><span data-stu-id="289be-124">Your **get\_accParent** implementation should delegate to the [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) method of the container.</span></span>

<span data-ttu-id="289be-125">В этом примере показано, как реализовать метод [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) .</span><span class="sxs-lookup"><span data-stu-id="289be-125">This example shows how to implement the [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) method.</span></span>


```C++
HRESULT CMyAccessibleMSAAControl::get_accParent(IDispatch **ppdispParent)  
{  
    if (ppdispParent == NULL)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_FALSE;  
    *ppdispParent = NULL;  

    IAccessibleWindowlessSite *pWindowlessSite = NULL;  

    if (SUCCEEDED(m_pClientSite->QueryInterface(IID_PPV_ARGS(&pWindowlessSite))))  
    {  
        IAccessible *pParentAcc = NULL;
        if (SUCCEEDED(pWindowlessSite->GetParentAccessible(&pParentAcc)))
        {
            hr = pParentAcc->QueryInterface(IID_PPV_ARGS(ppdispParent));  
        }
    }  

    SafeRelease(&pWindowlessSite);
    return hr;  
}
```



### <a name="step-4-acquire-a-range-of-object-ids-to-assign-to-the-event-sources-in-your-windowless-control"></a><span data-ttu-id="289be-126">Шаг 4. получение диапазона идентификаторов объектов для назначения источникам событий в безоконном управлении.</span><span class="sxs-lookup"><span data-stu-id="289be-126">Step 4: Acquire a range of object IDs to assign to the event sources in your windowless control.</span></span>

<span data-ttu-id="289be-127">Как и элементы управления на основе окон, элемент управления ActiveX без окон вызывает функцию [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) для уведомления клиентов о важных событиях.</span><span class="sxs-lookup"><span data-stu-id="289be-127">Like window-based controls, a windowless ActiveX control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function to notify clients of important events.</span></span> <span data-ttu-id="289be-128">Параметры функции включают идентификатор объекта элемента, вызывающего событие.</span><span class="sxs-lookup"><span data-stu-id="289be-128">The function parameters include the object ID of the item that is raising the event.</span></span> <span data-ttu-id="289be-129">Элемент управления без окон должен назначать идентификаторы объектов с помощью значения из диапазона, полученного путем вызова метода [**иакцессиблевиндовлесссите:: аккуиреобжектидранже**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) сайта управления.</span><span class="sxs-lookup"><span data-stu-id="289be-129">Your windowless control must assign object IDs by using a value from a range acquired by calling the control site’s [**IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange) method.</span></span>

<span data-ttu-id="289be-130">В этом примере показано, как получить диапазон значений идентификатора объекта из контейнера элемента управления.</span><span class="sxs-lookup"><span data-stu-id="289be-130">This example shows how to acquire a range of object ID values from the control container.</span></span>


```C++
IAccessibleWindowlessSite *pWindowlessSite = NULL;

if (SUCCEEDED(m_pClientSite->QueryInterface(
        IID_PPV_ARGS(&pWindowlessSite))))  
{  
    if (FAILED(pWindowlessSite->AcquireObjectIdRange(100, this, 
            &m_idObjectBase)))  
    {  
        m_idObjectBase = -1;  
    } 
}

SafeRelease(&pWindowlessSite);
```



### <a name="step-5-implement-the-iaccessiblehandler-interface"></a><span data-ttu-id="289be-131">Шаг 5. Реализация интерфейса Иакцессиблехандлер.</span><span class="sxs-lookup"><span data-stu-id="289be-131">Step 5: Implement the IAccessibleHandler interface.</span></span>

<span data-ttu-id="289be-132">Когда безоконный элемент управления вызывает функцию [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) , элемент управления указывает идентификатор объекта элемента пользовательского интерфейса, вызывающего событие, и указывает контейнер элемента управления как окно, которое будет реагировать на сообщения [**WM \_ GetObject**](wm-getobject.md) от имени элемента управления.</span><span class="sxs-lookup"><span data-stu-id="289be-132">When a windowless control calls the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function, the control specifies the object ID of the UI item that is raising the event, and specifies the control container as the window that will respond to [**WM\_GETOBJECT**](wm-getobject.md) messages on behalf of the control.</span></span>

<span data-ttu-id="289be-133">Если клиентское приложение отвечает на событие, контейнер элемента управления получает сообщение [**WM \_ GetObject**](wm-getobject.md) , включающее идентификатор объекта элемента пользовательского интерфейса, вызвавшего событие.</span><span class="sxs-lookup"><span data-stu-id="289be-133">If a client application responds to the event, the control container receives a [**WM\_GETOBJECT**](wm-getobject.md) message that includes the object ID of the UI item that raised the event.</span></span> <span data-ttu-id="289be-134">Контейнер элемента управления отвечает путем поиска безоконного элемента управления, которому "владеет" идентификатор объекта, и последующего вызова метода [**иакцессиблехандлер:: акцессиблеобжектфромид**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="289be-134">The control container responds by looking up the windowless control that "owns" the object ID, and then calling that control's [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) method.</span></span> <span data-ttu-id="289be-135">Метод **акцессиблеобжектфромид** возвращает указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента пользовательского интерфейса, а контейнер элементов управления перенаправляет указатель на клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="289be-135">The **AccessibleObjectFromID** method returns the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the UI item, and the control container forwards the pointer to the client application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="289be-136">См. также</span><span class="sxs-lookup"><span data-stu-id="289be-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="289be-137">Использование модели автоматизации пользовательского интерфейса для обеспечения доступа к безоконному элементу управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="289be-137">Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
</dt> <dt>

[<span data-ttu-id="289be-138">Специальные возможности элемента управления ActiveX без окон</span><span class="sxs-lookup"><span data-stu-id="289be-138">Windowless ActiveX Control Accessibility</span></span>](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 